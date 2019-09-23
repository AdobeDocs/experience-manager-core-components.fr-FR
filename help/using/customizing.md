---
title: Personnalisation des composants principaux
seo-title: Personnalisation des composants principaux
description: Les composants principaux implémentent plusieurs modèles permettant une personnalisation facile, depuis l’application d’un style simple jusqu’à la réutilisation de fonctionnalités avancées.
seo-description: Les composants principaux d’AEM implémentent plusieurs modèles permettant une personnalisation facile, depuis l’application d’un style simple jusqu’à la réutilisation de fonctionnalités avancées.
uuid: 38d22b85-4867-4716-817a-10ee2f8de6f5
contentOwner: Utilisateur
content-type: référence
topic-tags: développement
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 3c9e0ade-1ce0-4e34-ae04-8da63f9b6c4f
translation-type: tm+mt
source-git-commit: 62643e5bd49ab006230f65004bb9374822dcc017

---


# Personnalisation des composants principaux{#customizing-core-components}

Les [composants principaux](developing.md) implémentent plusieurs modèles permettant une personnalisation facile, depuis l’application d’un style simple jusqu’à la réutilisation de fonctionnalités avancées.

## Flexibilité de l'architecture {#flexible-architecture}

Les composants principaux ont été conçus pour être des outils flexibles et configurables. Une analyse de leur architecture permet de voir où des personnalisations peuvent être effectuées.

![Architecture des composants principaux](assets/screen_shot_2018-12-07at093742.png)

* La [boîte de dialogue de conception](authoring.md#edit-and-design-dialogs) définit ce que les auteurs peuvent effectuer ou non dans la boîte de dialogue de modification.
* Pour les auteurs, la [boîte de dialogue de modification](authoring.md#edit-and-design-dialogs) affiche uniquement les options qu’ils sont autorisés à utiliser.
* [Le modèle Sling](#customizing-the-logic-of-a-core-component) vérifie et prépare le contenu pour l’affichage (modèle).
* [Le résultat du modèle Sling](#customizing-the-logic-of-a-core-component) peut être sérialisé en JSON dans les cas d’utilisation des applications monopages.
* [Le code HTL effectue le rendu HTML](#customizing-the-markup) côté serveur pour un rendu classique côté serveur.
* [La sortie HTML](#customizing-the-markup) est sémantique, accessible, optimisée pour le moteur de recherche et facile à mettre en forme.

De plus, tous les composants principaux implémentent le [système de style](customizing.md).

## Modèles de personnalisation {#customization-patterns}

### Personnalisation des boîtes de dialogue {#customizing-dialogs}

Il peut être souhaitable de personnaliser les options de configuration disponibles dans la boîte de dialogue d’un composant principal, qu’il s'agisse de [la boîte de dialogue de conception ou de modification](authoring.md).

Chaque boîte de dialogue possède une structure de nœud cohérente. It is recommended that this structure is replicated in an inheriting component so that [Sling Resource Merger](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/sling-resource-merger.html) and [Hide Conditions](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/hide-conditions.html) can be used to hide, replace, or reorder sections of the original dialog. La structure à répliquer est définie comme tous les éléments jusqu’au niveau de nœud de l’élément d’onglet.

Pour être entièrement compatibles avec toutes les modifications apportées à une boîte de dialogue sur sa version actuelle, il est important que les structures sous le niveau de l’élément d’onglet ne soient pas touchées (masquées, ajoutées, remplacées, réorganisées, etc.). Instead, a tab item from the parent should be hidden via the `sling:hideResource` property (see [Sling Resource Merger Properties](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/sling-resource-merger.html)), and new tab items added that contain the bespoke configuration fields. `sling:orderBefore` peut être utilisé pour réorganiser les éléments d’onglet si nécessaire.

La boîte de dialogue ci-dessous illustre la structure de la boîte de dialogue recommandée et montre comment masquer et remplacer un onglet hérité comme décrit ci-dessus :

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T17:43:20.265-0400

Should we provide guidance on how to name their CSS classes, etc. to align to component re-usability best-practices? We tout that we follow bootstrap css naming, should we be counseling customers to align similarly? .cmp- 
<component name="">
  -- 
 <element>
   - 
  <element descriptor="">
    ? 
  </element> 
 </element> 
</component>

 -->

```xml
<?xml version="1.0" encoding="UTF-8"?>
<jcr:root xmlns:sling="https://sling.apache.org/jcr/sling/1.0"
          xmlns:jcr="https://www.jcp.org/jcr/1.0"
          xmlns:nt="https://www.jcp.org/jcr/nt/1.0"
          xmlns:granite="https://www.adobe.com/jcr/granite/1.0"
          jcr:primaryType="nt:unstructured">
    <content jcr:primaryType="nt:unstructured">
        <items jcr:primaryType="nt:unstructured">
            <tabs jcr:primaryType="nt:unstructured">
                <items jcr:primaryType="nt:unstructured">
                        <originalTab
                                jcr:primaryType="nt:unstructured"
                                sling:hideResource="true"/>
                        </originalTab>
                        <myTab
                               jcr:primaryType="nt:unstructured"
                               jcr:title="My Tab"
                               sling:resourceType="granite/ui/components/coral/foundation/container"/>
                               <!-- myTab content -->
                        </myTab>
                </items>
            </basic>
        </items>
    </content>
</jcr:root>
```

### Personnalisation de la logique d’un composant principal {#customizing-the-logic-of-a-core-component}

La logique métier des composants principaux est appliquée aux modèles Sling. Cette logique peut être étendue à l’aide d’un modèle de délégation Sling.

Par exemple, le composant principal de titre utilise la propriété `jcr:title` de la ressource demandée pour fournir le texte du titre. Si aucune propriété `jcr:title` n’est définie, une version de secours du titre de la page active est implémentée. Nous voulons modifier le comportement afin que le titre de la page active soit toujours affiché.

L’implémentation des modèles de composants principaux étant privée, ils doivent être étendus avec un modèle de délégation.

```java
@Model(adaptables = SlingHttpServletRequest.class,
       adapters = Title.class,
       resourceType = "myproject/components/pageHeadline")
public class PageHeadline implements Title {
    @ScriptVariable private Page currentPage;
    @Self @Via(type = ResourceSuperType.class)
    private Title title;
    @Override public String getText() {
        return currentPage.getTitle();
    }
    @Override public String getType() {
        return title.getType();
    }
}
```

For further details about the delegation pattern see the Core Components GitHub Wiki article [Delegation Pattern for Sling Models](https://github.com/adobe/aem-core-wcm-components/wiki/Delegation-Pattern-for-Sling-Models).

### Personnalisation du balisage {#customizing-the-markup}

L’application d’un style avancé requiert parfois une structure de balisage différente du composant.

Cela peut facilement être réalisé en copiant les fichiers HTL qui doivent être modifiés du composant principal vers le composant proxy.

En reprenant l’exemple du composant principal de chemin de navigation, pour personnaliser sa sortie de balisage, le fichier `breadcrumb.html` doit être copié dans le composant spécifique au site qui possède un `sling:resourceSuperTypes` pointant vers le composant principal de chemin de navigation.

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T17:43:20.265-0400

Should we provide guidance on how to name their CSS classes, etc. to align to component re-usability best-practices? We tout that we follow bootstrap css naming, should we be counseling customers to align similarly? .cmp- 
<component name="">
  -- 
 <element>
   - 
  <element descriptor="">
    ? 
  </element> 
 </element> 
</component>

 -->

### Style des composants {#styling-the-components}

Le premier type de personnalisation consiste à appliquer des styles CSS.

Pour faciliter cette opération, les composants principaux affichent un balisage sémantique et suivent une convention d’affectation de nom normalisée inspirée par [Bootstrap](https://getbootstrap.com/). De plus, pour cibler et placer facilement dans l’espace de noms les styles pour les composants, chaque composant principal est encapsulé dans un élément DIV avec les classes « `cmp` » et « `cmp-<name>` ».

For instance, looking at the HTL file of the v1 Core Breadcrumb Component: [breadcrumb.html](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb/breadcrumb.html), we see that the hierarchy of elements output are `ol.breadcrumb > li.breadcrumb-item > a`. Pour vous assurer qu’une règle CSS a uniquement un impact sur la classe de chemin de navigation de ce composant, toutes les règles doivent être placées dans l’espace de noms comme illustré ci-dessous :

```shell
.cmp-breadcrumb .breadcrumb {}  
.cmp-breadcrumb .breadcrumb-item {}  
.cmp-breadcrumb a {}
```

Additionally, each of the Core Components leverage the AEM [Style System feature](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/style-system.html) that allows template authors to define additional CSS class names that can be applied to the component by the page authors. Cela permet de définir pour chaque modèle une liste de styles de composants autorisés et de déterminer si l’un d'entre eux doit s’appliquer par défaut à tous les composants de ce type.

## Compatibilité de la mise à niveau des personnalisations {#upgrade-compatibility-of-customizations}

Trois types de mises à niveau sont possibles :

* mise à niveau de la version d’AEM
* mise à niveau des composants principaux vers une nouvelle version mineure
* mise à niveau des composants principaux vers une version majeure

En règle générale, la mise à niveau d’AEM vers une nouvelle version n’affecte pas les composants principaux ou les personnalisations, à condition que les versions des composants prennent également en charge la nouvelle version d’AEM vers laquelle est effectuée la migration et que les personnalisations n’utilisent pas d’API [obsolètes ou supprimées](https://helpx.adobe.com/experience-manager/6-5/release-notes/deprecated-removed-features.html).

La mise à niveau des composants principaux sans passer à une version majeure plus récente ne devrait pas affecter les personnalisations tant que les modèles de personnalisation décrits dans cette page sont utilisés.

Le passage à une nouvelle version majeure des composants principaux est compatible uniquement avec la structure de contenu, mais il est possible que des personnalisations doivent être rééffectuées. Des journaux de modifications clairs seront publiés pour chaque version de composant afin de mettre en évidence les modifications qui peuvent avoir une incidence sur le type de personnalisations décrit dans cette page.

## Prise en charge des personnalisations {#support-of-customizations}

Comme pour tout composant AEM, il existe un certain nombre d’éléments à prendre en compte concernant les personnalisations :

1. **Ne modifiez jamais directement le code des composants principaux.**

   Ils ne seraient plus entièrement pris en charge et les mises à jour ultérieures deviendraient problématiques. Utilisez plutôt les méthodes de personnalisation décrites dans cette page.

1. **Vous êtes seul responsable du code personnalisé.**

   Notre programme d’assistance ne couvre pas le code personnalisé. De plus, les problèmes signalés qui ne peuvent pas être reproduits avec les composants principaux Vanilla [utilisés comme documentés](using.md) ne sont pas pris en compte.

1. **Consultez régulièrement les fonctionnalités obsolètes et supprimées.**

   Avec chaque nouvelle version d’AEM vers laquelle est effectuée une mise à niveau, vérifiez que toutes les API utilisées sont toujours d’actualité en gardant un œil sur la page [Fonctionnalités obsolètes et supprimées](https://helpx.adobe.com/experience-manager/6-5/release-notes/deprecated-removed-features.html).

Consultez aussi la section [Prise en charge des composants principaux](developing.md#core-component-support).

**À lire aussi :**

* [Utilisation des composants principaux](using.md) : rendez opérationnels les composants principaux de votre propre projet.
* [Instructions sur les composants](guidelines.md) : pour connaître les schémas d’implémentation des composants principaux.
