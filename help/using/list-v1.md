---
title: Composant List (v 1)
seo-title: Composant List (v 1)
description: 'null'
seo-description: Le composant Liste des composants principaux permet de créer facilement des listes dynamiques et statiques.
uuid: 06658 c 9 d-cbf 2-4 bfe-b 425-d 980 d 1181908
content-type: référence
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 7 c 130 ccc -83 ff -464 d-b 58 f-d 581 f 4365 dbd
disttype: dist5
gnavtheme: light
groupsectionnavitems: non
hidemerchandisingbar: inherit
hidepromocomponent: inherit
modalsize: 426x240
noindex: 'true'
index: n
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 4e74f10e2a4119484a597178dc4577b399833dbf

---


# Composant List (v 1){#list-component-v}

Le composant Liste des composants principaux permet de créer facilement des listes dynamiques et statiques.

## Utilisation {#usage}

Le composant Liste peut servir à créer, par exemple, une liste dynamique de pages enfants ou une liste statique d&#39;éléments définis de manière arbitraire.

Le type de liste disponible et les options de formatage peuvent être définies par l&#39;auteur du modèle dans la boîte de dialogue [de conception](list-v1.md#main-pars_title_1995166862). L&#39;éditeur de contenu peut sélectionner les types de liste disponibles et formater les éléments de liste dans la boîte de dialogue [Modifier](list-v1.md#main-pars_title).

## Version et compatibilité {#version-and-compatibility}

Ce document décrit la version v 1 du composant Liste, introduite à l&#39;origine avec la version 1.0.0 des composants principaux avec AEM 6.3.

Le tableau suivant répertorie la compatibilité de la version v 1 du composant Liste.

| Version d’AEM | Composant de liste v 1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Ce document décrit la version v 1 du composant de liste.
>
>Pour plus d&#39;informations sur la version actuelle du composant Liste, voir [le document Composant](list.md) Liste.

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple tiré de [We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Capture d’écran {#screenshot}

![](assets/chlimage_1-47.png)

### HTML {#html}

```
<div class="cmp cmp-list aem-GridColumn aem-GridColumn--default--12">

<ul>
    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/arctic-surfing-in-lofoten.html">
            <span class="cmp-list--item-title">Arctic Surfing In Lofoten</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/summit-success-in-the-himalayas.html">
            <span class="cmp-list--item-title">Summit Success in the Himalayas</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/climbing-on-kalymnos-island--greece.html">
            <span class="cmp-list--item-title">Climbing on Kalymnos Island, Greece</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/running-at-the-great-wall-marathon.html">
            <span class="cmp-list--item-title">Running at the Great Wall Marathon</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/skiing-deep-powder-in-siberia.html">
            <span class="cmp-list--item-title">Skiing deep powder in Siberia</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/climbing-in-the-massif-du-mont-blanc.html">
            <span class="cmp-list--item-title">Climbing in the Massif du Mont Blanc</span>
            
        </a>
        
    </article>
</li>
</ul>

</div>
```

### JSON {#json}

```
"articles_list": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "weretail/components/content/articleslist",
              "tagsMatch": "any",
              "displayAs": "teaser",
              "feedEnabled": "true",
              "listFrom": "children",
              "limit": "0",
              "orderBy": "cq:lastModified",
              "pageMax": "0"
            }
```

>[!NOTE]
>
>L&#39;exportation JSON à partir des composants principaux nécessite la version 1.1.0 des composants principaux. Pour plus d&#39;informations, consultez les [informations de compatibilité des composants principaux v 1](versions.md#main-pars_title_236368006) .

## Modifier le dialogue {#edit-dialog}

Le dialogue Modifier permet à l&#39;auteur du contenu de configurer la liste et les éléments de la liste.

### Paramètres de liste {#list-settings}

La liste peut être générée de différentes manières.

* [Pages enfants](list-v1.md#main-pars_title_1861279796)
* [Liste fixe](list-v1.md#main-pars_title_1227896889)
* [Rechercher](list-v1.md#main-pars_title_1224003560)
* [Balises](list-v1.md#main-pars_title_700759533)

Quelle que soit la création de la liste, il existe des options [de tri](list-v1.md#main-pars_title_1568376452) qui peuvent toujours être configurées.

![](assets/chlimage_1-38.png)

Selon la manière dont l&#39;auteur du contenu choisit de construire la liste, les options de configuration supplémentaires changent.

#### Pages enfants {#child-pages}

La liste peut être créée des pages enfants de la page active ou d&#39;une autre page.

![](assets/chlimage_1-39.png)

* **Page parente**
   * Page dont les pages enfants doivent faire la liste
   * Laisser vide pour utiliser la page active
* **Profondeur de l&#39;enfant** - Nombre de niveaux vers le bas dans la hiérarchie

#### Liste fixe {#fixed-list}

La liste peut être créée à l&#39;aide d&#39;une liste fixe d&#39;éléments.

![](assets/chlimage_1-40.png)

Appuyez ou cliquez sur le **bouton Ajouter** pour insérer un nouvel élément dans la liste.

* Entrez le texte de l&#39;élément dans la liste ou utilisez le dialogue **de sélection** pour choisir un élément dans AEM.
* Utilisez la poignée de glisser-déplacer pour réorganiser les éléments de la liste.
* Utilisez l&#39;icône de corbeille pour supprimer les éléments de la liste.

#### Recherche {#search}

La liste peut être créée à l&#39;aide des résultats d&#39;une recherche de contenu AEM.

![](assets/chlimage_1-41.png)

* **Requête de recherche** - chaîne pour laquelle une recherche de texte intégral est exécutée pour générer les éléments de la liste
* **Recherche dans** - Emplacement où la recherche doit être exécutée
   * Utilisation de **la boîte de dialogue** de sélection pour choisir l&#39;emplacement dans AEM
   * Utiliser la page active si laissée vide

#### Balises {#tags}

La liste peut être créée à l&#39;aide de pages qui correspondent à certaines balises sous un emplacement particulier.

![](assets/chlimage_1-42.png)

* **Page parente** - Emplacement où la correspondance des balises doit commencer
   * Utilisation de **la boîte de dialogue** de sélection pour choisir l&#39;emplacement dans AEM
   * Utiliser la page active si laissée vide
* **Balises** - Quelles balises doivent correspondre
   * Utilisez le dialogue **Parcourir** pour sélectionner les balises.
* **Correspondance** - Définir le type de correspondance à associer à une page à inclure dans la liste
   * **n’importe quelle balise**
   * **toutes les balises**

#### Options de tri {#sort-options}

Quelle que soit la manière dont vous choisissez de créer la liste, certaines options de tri peuvent toujours être définies.

![](assets/chlimage_1-43.png)

* **Ordre par** - Comment les éléments doivent être triés
   * **Titre**
   * **Date de dernière modification**
* **Ordre de tri** : ordre dans lequel les éléments doivent être triés
   * **croissant**
   * **décroissant**
* **Nombre max. d&#39;éléments** - Nombre maximal d&#39;éléments affichés dans la liste.
   * Laisser vide pour renvoyer tous les éléments.

### Paramètres d’élément {#item-settings}

A l&#39;aide **de l&#39;onglet Paramètres** d&#39;élément, la mise en forme des éléments de liste peut être configurée.

![](assets/chlimage_1-44.png)

* **Lien Éléments**
de lien vers la page correspondante
* **Afficher Description**
Afficher les descriptions de l&#39;élément de lien
* **Afficher la date de modification de la date**
de modification de l&#39;élément de lien

## Créer un dialogue {#design-dialog}

Le dialogue de conception permet à l&#39;auteur du modèle de définir les types de listes à autoriser aux auteurs de contenu ainsi que les paramètres d&#39;éléments disponibles.

### Paramètres de liste {#list-settings-1}

Dans **l&#39;onglet Paramètres** de liste, le format de date peut être défini et le type de liste doit être disponible dans le composant aux auteurs de contenu.

![](assets/chlimage_1-45.png)

* **Format de date** - Format à utiliser pour l&#39;affichage de la date de dernière modification
* **Désactiver les enfants** - Désactiver le type de liste des enfants dans le composant
* **Désactiver statique** - Désactiver le type de liste statique dans le composant
* **Désactiver la recherche** - Désactiver le type de liste de recherche dans le composant
* **Désactiver les balises** : désactive le type de liste des balises dans le composant

### Paramètres d’élément {#item-settings-1}

Dans **l&#39;onglet Paramètres** d&#39;élément, les options de formatage des éléments de liste individuels qui doivent être disponibles dans le composant pour les auteurs de contenu peuvent être définies.

![](assets/chlimage_1-46.png)

* **Eléments de lien** - Activer l&#39;option Éléments de lien dans [le dialogue Modifier](list-v1.md#main-pars_title_550499279)
* **Afficher les descriptions** - Activer l&#39;option Afficher les descriptions dans la [boîte de dialogue Modifier](list-v1.md#main-pars_title_550499279)
* **Afficher la date** - Activer l&#39;option Afficher la date dans le [dialogue Modifier](list-v1.md#main-pars_title_550499279)

## Détails techniques {#technical-details}

Vous trouverez la documentation technique la plus récente sur le composant [de liste sur github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v1/list).

Le projet de composants principaux peut être téléchargé depuis github.

Vous trouverez plus d&#39;informations sur le développement des composants principaux dans la documentation destinée aux développeurs de composants [principaux](developing.md).
