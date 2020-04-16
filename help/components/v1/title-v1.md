---
title: Composant du titre (v1)
description: Le composant du titre des composants principaux est un composant d’en-tête de section qui comporte des fonctions d’édition statique.
index: n
translation-type: ht
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Composant du titre (v1) {#title-component-v}

Le composant du titre des composants principaux est un composant d’en-tête de section qui comporte des fonctions d’édition statique.

## Utilisation {#usage}

Le composant du titre est conçu pour être utilisé comme titre ou en-tête d’une section de contenu.

Les niveaux d’en-tête disponibles peuvent être définis par l’auteur du modèle dans la [boîte de dialogue de conception](#design-dialog). L’éditeur de contenu peut sélectionner les niveaux d’en-têtes disponibles dans la [boîte de dialogue de modification](#edit-dialog). Pour plus de commodité, une simple modification statique du texte d’en-tête est également disponible.

## Version et compatibilité {#version-and-compatibility}

Ce document décrit la version v1 du composant du titre, introduite à l’origine avec la version 1.0.0 des composants principaux avec AEM 6.3.

Le tableau suivant répertorie la compatibilité de la version v1 du composant Titre.

| Version d’AEM | Composant Titre v1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Ce document décrit la version 1 du composant Titre.
>
>Pour plus d’informations sur la version actuelle du composant Titre, voir le document [Composant Titre](/help/components/title.md).

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple extrait de [We.Retail](https://helpx.adobe.com/fr/experience-manager/6-4/sites/developing/using/we-retail.html).

### Capture d’écran {#screenshot}

![](/help/assets/chlimage_1-36.png)

### HTML {#html}

```
<div class="cmp cmp-title aem-GridColumn aem-GridColumn--default--12">
     <h2>Welcome! This is our finest equipment!</h2>
</div>
```

### JSON {#json}

```
"title": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "weretail/components/content/title",
              "jcr:title": "Welcome! This is our finest equipment!",
              "type": "h2"
            }
```

>[!NOTE]
>
>L’exportation JSON à partir des composants principaux nécessite la version 1.1.0 des composants principaux. Pour plus d’informations, voir les [informations de compatibilité des composants principaux v1](/help/versions.md).

## Boîte de dialogue de modification {#edit-dialog}

La boîte de dialogue de modification permet à l’auteur de contenu de définir le texte du titre et de sélectionner le niveau de titre.

>[!NOTE]
>
>Une valeur vide pour le titre provoque l’affichage du titre de la page.

![](/help/assets/chlimage_1-91.png)

L’éditeur statique peut également être utilisé pour modifier le texte du composant du titre.

![](/help/assets/chlimage_1-37.png)

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir le niveau d’en-tête par défaut que les composants de titre auront lorsqu’ils sont créés par les auteurs de contenu.

![](/help/assets/chlimage_1-92.png)

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Titre [se trouve sur GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v1/title).

Le projet sur les composants principaux peut être téléchargé depuis GitHub.

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).
