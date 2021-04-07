---
title: Composant de chemin de navigation (v1)
description: Le composant de chemin de navigation des composants principaux est un composant de navigation qui crée un chemin de navigation des liens en fonction de l’emplacement de la page dans la hiérarchie du contenu.
index: n
role: Architecte, développeur, administrateur, professionnel
translation-type: ht
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: ht
source-wordcount: '551'
ht-degree: 100%

---


# Composant de chemin de navigation (v1) {#breadcrumb-component-v}

Le composant de chemin de navigation des composants principaux est un composant de navigation qui crée un chemin de navigation des liens en fonction de l’emplacement de la page dans la hiérarchie du contenu.

## Utilisation {#usage}

Le composant de chemin de navigation affiche la position de la page actuelle dans la hiérarchie du site, ce qui permet aux visiteurs de la page de parcourir la hiérarchie de celle-ci à partir de leur emplacement actuel. Cela est souvent intégré dans les en-têtes ou pieds de page.

Les options disponibles, telles que le niveau de navigation par défaut et la possibilité d’afficher la page active ou les pages masquées, peuvent être définies par l’auteur du modèle dans la [boîte de dialogue de conception](#design-dialog). L’éditeur de contenu peut ensuite choisir si les pages masquées doivent être affichées ou non et le niveau de navigation actuel du composant dans la [boîte de dialogue de modification](#edit-dialog).

## Version et compatibilité {#version-and-compatibility}

Ce document décrit la version v1 du composant de chemin de navigation, introduite à l’origine avec la version 1.0.0 des composants principaux avec AEM 6.3.

Le tableau ci-après répertorie la compatibilité de la version v1 du composant de chemin de navigation.

| Version d’AEM | Composant de chemin de navigation v1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Ce document décrit la version v1 du composant de chemin de navigation.
>Pour plus d’informations sur la version actuelle du composant de chemin de navigation, voir le document [Composant de chemin de navigation](/help/components/breadcrumb.md).

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple extrait de [We.Retail](https://helpx.adobe.com/fr/experience-manager/6-4/sites/developing/using/we-retail.html).

### Capture d’écran {#screenshot}

![](/help/assets/chlimage_1-33.png)

### HTML {#html}

```
<div class="cmp cmp-breadcrumb aem-GridColumn aem-GridColumn--default--12">

<ol class="breadcrumb">
    <li class="breadcrumb-item ">
        <a href="/content/we-retail/us.html">
            United States
        </a>
    </li>

    <li class="breadcrumb-item ">
        <a href="/content/we-retail/us/en.html">
            English
        </a>
    </li>

    <li class="breadcrumb-item active">
        
            Experience
        
    </li>
</ol>
 
</div>
```

### JSON {#json}

```
"breadcrumb": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "weretail/components/content/breadcrumb"
            }
```

>[!NOTE]
>
>L’exportation JSON à partir des composants principaux nécessite la version 1.1.0 des composants principaux. Pour plus d’informations, voir les [informations de compatibilité des composants principaux v1](/help/versions.md).

## Boîte de dialogue de modification {#edit-dialog}

La boîte de dialogue de modification permet à l’auteur de contenu de supprimer les pages masquées et actives dans les chemins de navigation ainsi que la profondeur de la hiérarchie qu’elle doit afficher.

![](/help/assets/chlimage_1-34.png)

* **Niveau de navigation au début** : à quel niveau dans la hiérarchie le composant de chemin de navigation doit commencer à descendre jusqu’à la page actuelle. Par exemple, dans We.Retail :

   * 1 commence à `/content/we-retail`
   * 2 commence à `/content/we-retail/<country>`

* **Afficher les éléments masqués** : affichez les pages marquées comme étant masquées dans le chemin de navigation (elles ne sont pas affichées par défaut).
* **Masquer éléments actuels** : supprimez la page actuelle dans le chemin de navigation (par défaut, elle s’affiche).

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les valeurs par défaut des options de suppression des pages masquées et actives dans les chemins de navigation, ainsi que la profondeur de la hiérarchie qu’elle doit afficher.

![](/help/assets/chlimage_1-35.png)

* **Niveau de navigation au début** : définit la valeur par défaut à partir de laquelle le composant de chemin de navigation doit commencer à se déplacer jusqu’à la page actuelle lorsqu’il est ajouté à une page.
* **Afficher les éléments masqués** : définit la valeur par défaut de l’option **Afficher les éléments masqués** lorsque le composant de chemin de navigation est ajouté à une page.

   * Cela n’active ou ne désactive pas l’option de l’auteur. Cela définit uniquement la valeur par défaut.

* **Masquer éléments actuels** : définit la valeur par défaut de l’option **Masquer éléments actuels** lorsque le composant de chemin de navigation est ajouté à une page.

   * Cela n’active ou ne désactive pas l’option de l’auteur. Cela définit uniquement la valeur par défaut.

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant de chemin de navigation [se trouve sur GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v1/breadcrumb).

Le projet sur les composants principaux peut être téléchargé depuis GitHub.

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).
