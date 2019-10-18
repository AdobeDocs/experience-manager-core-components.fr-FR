---
title: Instructions relatives aux composants
seo-title: Instructions relatives aux composants
description: Les composants principaux suivent des modèles de mise en œuvre modernes qui sont très différents des composants de base.
seo-description: Les composants principaux suivent des modèles de mise en œuvre modernes qui sont très différents des composants de base.
uuid: b1daea89-da3c-454f-8ab5-d75a19412954
contentOwner: Utilisateur
content-type: référence
topic-tags: développement
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 170dba8f-a2ed-442e-a56e-1126b338c36e
translation-type: tm+mt
source-git-commit: 683b4f4705c226275439a408423cbf1b23bea66f

---


# Instructions relatives aux composants {#component-guidelines}

Les [composants principaux](developing.md) suivent des modèles de mise en œuvre modernes qui sont très différents des composants de base.

Cette page explique ces modèles et à quel moment les utiliser pour créer vos propres composants. La première section [Modèles généraux de composants](guidelines.md) s’applique à n’importe quel type de composant, tandis que la deuxième section [Modèles de composants réutilisables](guidelines.md) s’applique aux composants destinés à être réutilisés sur plusieurs sites ou projets, comme les composants principaux d’une instance.

## Modèles généraux de composants {#general-component-patterns}

Les instructions de cette section sont recommandées pour tout type de composant, que le composant soit spécifique à un projet unique ou qu’il soit censé être largement réutilisé sur plusieurs sites ou projets.

### Composants configurables {#configurable-components}

Les composants peuvent avoir des boîtes de dialogue avec diverses options. Ces boîtes de dialogue doivent être utilisées pour rendre les composants souples et configurables et éviter de mettre en œuvre plusieurs composants qui sont principalement des variantes les uns des autres.

En règle générale, si une structure filaire ou une conception contient des variantes d’éléments similaires, ces variantes ne doivent pas être implémentées comme des composants différents, mais comme un composant avec des options pour choisir entre les variantes.

Pour aller plus loin, si les composants sont réutilisés sur plusieurs sites ou projets, reportez-vous à la section [Fonctionnalités préconfigurables](#pre-configurable-capabilities).

### Séparation des préoccupations {#separation-of-concerns}

Le maintien de la logique (ou du modèle) d’un composant distinct du modèle de balisage (ou affichage) est généralement une bonne pratique. There are several ways to achieve that, however the recommended one is to use [Sling Models](https://sling.apache.org/documentation/bundles/models.html) for the logic and the [HTML Template Language](https://helpx.adobe.com/experience-manager/htl/using/overview.html) (HTL) for the markup, like the Core Components also do.

Les modèles Sling sont un ensemble d’annotations Java permettant d’accéder facilement aux variables nécessaires à partir des POJO. Ils offrent par conséquent une méthode simple, puissante et performante pour implémenter la logique Java pour les composants.

HTL a été conçu pour être un langage de modèle sécurisé et simple adapté à AEM. Il peut appeler de nombreuses formes de logique, ce qui le rend très souple.

## Modèles de composants réutilisables {#reusable-component-patterns}

Les instructions de cette section peuvent également être utilisées pour tout type de composant, mais elles sont plus logiques pour les composants destinés à être réutilisés sur plusieurs sites ou projets, comme les composants principaux d’une instance. Ces instructions peuvent donc être ignorées pour les composants qui ne sont utilisés que sur un seul site ou projet.

### Fonctionnalités préconfigurables {#pre-configurable-capabilities}

Outre la boîte de dialogue de modification utilisée par les auteurs de pages, les composants peuvent également avoir une boîte de dialogue de conception pour les auteurs de modèles afin de les préconfigurer. The [Template Editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) allows to setup all these pre-configurations, which are called "Policies".

Pour rendre les composants aussi réutilisables que possible, ils doivent être fournis avec des options significatives pour la préconfiguration. Cela permet d’activer ou de désactiver les fonctionnalités des composants pour répondre aux besoins spécifiques des différents sites.

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T17:49:04.584-0400

Unclear how I can add my own capability toggle (for example, if i extend a component and want to toggle that extended functionality ... )

 -->

### Modèle de composant proxy {#proxy-component-pattern}

Comme chaque ressource de contenu possède une propriété `sling:resourceType` qui référence le composant pour son rendu, il est généralement recommandé que ces propriétés pointent vers des composants spécifiques au site au lieu de pointer vers des composants partagés par plusieurs sites. Ceci offre davantage de souplesse et évite la restructuration du contenu si un site nécessite un comportement différent pour un composant, car cette personnalisation peut alors être obtenue sur le composant spécifique au site sans affecter les autres sites.

Toutefois, pour que les composants spécifiques au projet ne dupliquent aucun code, chacun d’entre eux doit faire référence au composant parent partagé avec la propriété `sling:resourceSuperType`. Ces composants spécifiques au projet qui font principalement référence aux composants parents sont appelés « composants proxy ». Les composants proxy peuvent être complètement vides s’ils héritent entièrement de la fonctionnalité ou ils peuvent redéfinir certains aspects du composant.

### Contrôle de version des composants {#component-versioning}

Les composants doivent être maintenus entièrement compatibles. Toutefois, des modifications qui ne peuvent pas être toujours compatibles sont parfois nécessaires. Une solution à ces besoins contradictoires consiste à introduire le contrôle de version des composants en ajoutant un numéro dans leur chemin d’accès au type de ressource et dans les noms complets de classe Java de leurs implémentations. This version number represents a major version as defined by [semantic versioning guidelines](https://semver.org/), which is incremented only for changes that are not backward-compatible.

Les modifications incompatibles aux aspects suivants des composants entraîneront une nouvelle version :

* Modèles Sling (suivant les directives de contrôle de version sémantique)
* Scripts et modèles HTL
* Balises HTML et sélecteurs CSS
* Représentation JSON
* Boîtes de dialogue

For further details, see the [Versioning Policies](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-Policies) document in GitHub.

Le contrôle de version des composants crée une forme de contrat qui est importante pour les mises à niveau car elle clarifie le moment où il est nécessaire de restructurer un élément. Consultez aussi la section [Compatibilité des mises à niveau des personnalisations](customizing.md#upgrade-compatibility-of-customizations), qui explique quels sont les différents types de personnalisations requis pour une mise à niveau.

Pour éviter des migrations de contenu complexes, il est important de ne jamais pointer directement vers les composants versionnés des ressources de contenu. En règle générale, une `sling:resourceType` du contenu ne doit jamais comporter de numéro de version, ou la mise à niveau des composants nécessite que le contenu soit également restructuré. Le meilleur moyen pour éviter cela est de suivre le [modèle de composant proxy](#proxy-component-pattern) décrit ci-dessus.

### Interfaces de modèles {#model-interfaces}

Il s’agit de l’instruction `data-sly-use` du code HTL de pointer vers une interface Java, tandis que l’implémentation du modèle Sling s’enregistre également auprès du type de ressource du composant.

Lorsqu’elle est combinée avec le [modèle de composant proxy](#proxy-component-pattern) décrit ci-dessus, cette forme de liaison double offre des points d’extension suivants :

1. Un site peut redéfinir l’implémentation d’un modèle Sling en l’enregistrant auprès du type de ressource du composant proxy, sans avoir à tenir compte du fichier HTL qui peut toujours pointer vers l’interface.
1. Un site peut redéfinir le balisage HTL d’un composant, sans avoir à tenir compte de la logique d’implémentation vers lequel il doit pointer.

## Assemblage {#putting-it-all-together}

Vous trouverez ci-dessous un aperçu de la structure entière de liaison de type de ressource, en prenant l’exemple du composant principal du titre. Il illustre la manière dont un composant proxy spécifique au site permet de résoudre le contrôle des composants, afin d’éviter que la ressource de contenu contienne un numéro de version. It then shows how the component's `title.html` [HTL](https://helpx.adobe.com/experience-manager/htl/using/overview.html) file uses to the model interface, while the implementation binds to the specific version of the component through [Sling Model](https://sling.apache.org/documentation/bundles/models.html) annotations.

![Présentation de la liaison des ressources](assets/chlimage_1-32.png)

Below is another overview, which doesn't show the details of the implementation POJO, but reveals how the associated [templates and policies](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/page-templates-editable.html) are referenced.

La propriété `cq:allowedTemplates` indique les modèles qui peuvent être utilisés pour un site et la propriété `cq:template` indique pour chaque page quel est le modèle associé. Chaque modèle est composé de trois parties :

* **structure**
Contient les ressources qui seront forcées à être présentes sur chaque page et que l’auteur de la page ne pourra pas supprimer, comme par exemple les composants d’en-tête de page et de pied de page.
* **initial**
Contient le contenu initial qui sera dupliqué dans la page lors de sa création.
* **policies**
Contient pour chaque composant le mappage à une stratégie, qui est la préconfiguration du composant. Ce mappage permet de réutiliser les stratégies dans les modèles et donc de les gérer de manière centralisée.

![Présentation des modèles et de la stratégie](assets/screen_shot_2018-12-07at093102.png)

## Archétype de projet AEM {#aem-project-archetype}

[L’archétype](overview.md) de projet AEM crée un projet Adobe Experience Manager minimal comme point de départ pour vos propres projets, y compris un exemple de composant HTML personnalisé avec SlingModels pour la logique et l’implémentation appropriée des composants principaux avec le modèle de proxy recommandé.

**À lire aussi :**

* [Utilisation des composants principaux](using.md) : rendez opérationnels les composants principaux de votre propre projet.
* [Personnalisation des composants principaux](customizing.md) : pour savoir comment appliquer un style aux composants principaux et les personnaliser.
