---
title: Composant Liste (v1)
description: Le composant principal Liste permet de créer facilement des listes dynamiques et statiques.
index: n
translation-type: tm+mt
source-git-commit: 5439f90faef28c72367419bb7429a3a880b65229

---


# Composant Liste (v1){#list-component-v}

Le composant principal Liste permet de créer facilement des listes dynamiques et statiques.

## Utilisation {#usage}

Le composant Liste peut servir à créer, par exemple, une liste dynamique de pages enfants ou une liste statique d’éléments définis de manière arbitraire.

Le type de liste disponible et les options de mise en forme peuvent être définis par l’auteur du modèle dans la [boîte de dialogue de conception](list-v1.md#main-pars_title_1995166862). L’éditeur de contenu peut sélectionner les types de liste disponibles et mettre en forme les éléments de liste dans la [boîte de dialogue de modification](list-v1.md#main-pars_title).

## Version et compatibilité {#version-and-compatibility}

Ce document décrit la version v1 du composant Liste, introduite à l’origine avec la version 1.0.0 des composants principaux avec AEM 6.3.

Le tableau suivant répertorie la compatibilité de la version v1 du composant Liste.

| Version d’AEM | Composant Liste v1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Ce document décrit la version v1 du composant Liste.
>
>Pour plus d’informations sur la version actuelle du composant Liste, voir [le document Composant Liste](list.md).

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple extrait de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>L’exportation JSON à partir des composants principaux nécessite la version 1.1.0 des composants principaux. Pour plus d’informations, voir les [informations de compatibilité des composants principaux v1](versions.md#main-pars_title_236368006).

## Boîte de dialogue de modification {#edit-dialog}

La boîte de dialogue de modification permet à l’auteur du contenu de configurer la liste et les éléments de la liste.

### Paramètres de liste {#list-settings}

La liste peut être générée de différentes manières.

* [Pages enfants](list-v1.md#main-pars_title_1861279796)
* [Liste fixe](list-v1.md#main-pars_title_1227896889)
* [Recherche](list-v1.md#main-pars_title_1224003560)
* [Balises](list-v1.md#main-pars_title_700759533)

Quelle que soit la création de la liste, il existe des [Options de tri](list-v1.md#main-pars_title_1568376452) qui peuvent toujours être configurées.

![](assets/chlimage_1-38.png)

Selon la manière dont l’auteur du contenu choisit de construire la liste, les options de configuration supplémentaires changent.

#### Pages enfants {#child-pages}

La liste peut être créée à partir des pages enfants de la page active ou d’une autre page.

![](assets/chlimage_1-39.png)

* **Page parente**
   * Page dont les pages enfants doivent faire la liste.
   * Laissez vide pour utiliser la page active.
* **Profondeur -enfant** - Nombre de niveaux vers le bas dans la hiérarchie.

#### Liste fixe {#fixed-list}

La liste peut être créée à l’aide d’une liste fixe d’éléments.

![](assets/chlimage_1-40.png)

Appuyez ou cliquez sur le bouton **Ajouter** pour insérer un nouvel élément dans la liste.

* Entrez le texte de l’élément dans la liste ou utilisez la **boîte de dialogue Sélection** pour choisir un élément dans AEM.
* Utilisez la poignée de glisser-déplacer pour réorganiser les éléments de la liste.
* Utilisez l’icône de corbeille pour supprimer les éléments de la liste.

#### Recherche {#search}

La liste peut être créée à l’aide des résultats d’une recherche de contenu AEM.

![](assets/chlimage_1-41.png)

* **Requête de recherche** - Chaîne pour laquelle une recherche de texte intégral est exécutée pour générer les éléments de la liste.
* **Rechercher dans** - Emplacement où la recherche doit être exécutée.
   * Utilisez la **boîte de dialogue Sélection** pour choisir l’emplacement dans AEM.
   * Utilisez la page active si laissée vide.

#### Balises {#tags}

La liste peut être créée à l’aide de pages qui correspondent à certaines balises sous un emplacement particulier.

![](assets/chlimage_1-42.png)

* **Page parente** - Emplacement où la correspondance des balises doit commencer.
   * Utilisez la **la boîte de dialogue Sélection** pour choisir l’emplacement dans AEM.
   * Utilisez la page active si laissée vide.
* **Balises** - Quelles balises doivent correspondre.
   * Utilisez la boîte de dialogue **Parcourir** pour sélectionner les balises.
* **Correspondance** - Définissez le type de correspondance à associer à une page à inclure dans la liste.
   * **n’importe quelle balise**
   * **toutes les balises**

#### Options de tri {#sort-options}

Quelle que soit la manière dont vous choisissez de créer la liste, certaines options de tri peuvent toujours être définies.

![](assets/chlimage_1-43.png)

* **Trier par** - Comment les éléments doivent être triés.
   * **Titre**
   * **Date de dernière modification**
* **Ordre de tri** - Ordre dans lequel les éléments doivent être triés.
   * **croissant**
   * **décroissant**
* **Nombre maximal d’éléments** - Nombre maximal d’éléments affichés dans la liste.
   * Laissez vide pour renvoyer tous les éléments.

### Paramètres d’élément {#item-settings}

À l’aide de l’onglet **Paramètres d’élément**, la mise en forme des éléments de liste peut être configurée.

![](assets/chlimage_1-44.png)

* **Lier des éléments**
Liez des éléments à la page correspondante.
* **Afficher la description**
Affichez les descriptions de l’élément de lien.
* **Afficher la date**
Permet d’afficher la date de modification de l’élément de lien.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les types de listes à autoriser aux auteurs de contenu ainsi que les paramètres d’éléments disponibles.

### Paramètres de liste {#list-settings-1}

Dans l’onglet **Paramètres de liste**, le format de date peut être défini et le type de liste doit être disponible dans le composant pour les auteurs de contenu.

![](assets/chlimage_1-45.png)

* **Format de date** - Format à utiliser pour l’affichage de la date de la dernière modification.
* **Désactiver les enfants** - Désactivez le type de liste enfants dans le composant.
* **Désactiver statique** - Désactivez le type de liste statique dans le composant.
* **Désactiver la recherche** - Désactivez le type de liste de recherche dans le composant.
* **Désactiver les balises** - Désactivez le type de liste des balises dans le composant.

### Paramètres d’élément {#item-settings-1}

Dans l’onglet **Paramètres d’élément**, les options de formatage des éléments de liste individuels qui doivent être disponibles dans le composant pour les auteurs de contenu peuvent être définies.

![](assets/chlimage_1-46.png)

* **Éléments de lien** - Activez l’option Éléments de lien dans la [boîte de dialogue de modification](list-v1.md#main-pars_title_550499279).
* **Afficher les descriptions** - Activez l’option Afficher les descriptions dans la [boîte de dialogue de modification](list-v1.md#main-pars_title_550499279).
* **Afficher la date** - Activez l’option Afficher la date dans la [boîte de dialogue de modification](list-v1.md#main-pars_title_550499279).

## Détails techniques {#technical-details}

The latest technical documentation about the List Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v1/list).

Le projet sur les composants principaux peut être téléchargé depuis GitHub.

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](developing.md).
