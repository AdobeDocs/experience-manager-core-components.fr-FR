---
title: Composant de bouton de formulaire (v1)
description: Le composant Masqué du formulaire des composants principaux permet l’inclusion d’un champ masqué dans un formulaire.
index: n
role: Architecte, Développeur, Administrateur, Professionnel
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 98%

---


# Composant de bouton de formulaire (v1) {#form-button-component-v}

Le composant de bouton de formulaire des composants principaux permet l’inclusion d’un champ de bouton dans un formulaire pour déclencher une action.

## Utilisation {#usage}

Le composant de bouton de formulaire des composants principaux permet la création de champs de bouton, souvent pour déclencher l’envoi du formulaire et est destiné à être utilisé avec le [composant de conteneur de formulaires](form-container-v1.md).

Les propriétés de bouton peuvent être définies par l’éditeur de contenu dans la [boîte de dialogue de configuration](#configure-dialog).

## Version et compatibilité {#version-and-compatibility}

Ce document décrit la version v1 du composant de bouton de formulaire, introduite à l’origine avec la version 1.0.0 des composants principaux avec AEM 6.3.

Le tableau ci-après répertorie la compatibilité de la version v1 du composant de bouton de formulaire.

| Version d’AEM | Composant de bouton de formulaire v1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Ce document décrit la version v1 du composant de bouton de formulaire.
>
>Pour plus d’informations sur la version actuelle du composant de bouton de formulaire, voir le document [Composant de bouton de formulaire](/help/components/forms/form-button.md).

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple extrait de [We.Retail](https://helpx.adobe.com/fr/experience-manager/6-4/sites/developing/using/we-retail.html).

### Capture d’écran {#screenshot}

![](/help/assets/chlimage_1-48.png)

### HTML {#html}

```
<div class="cmp cmp-button aem-GridColumn aem-GridColumn--default--12">
    <div class="cmp cmp-button">
        <button type="BUTTON" class="btn btn-action btn-primary" name="loveToast" value="ILoveToast">
            Click here if you love toast!
        </button>
    </div>
</div>
```

### JSON {#json}

```
"container": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "columnCount": 12,
              "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
              ":items": {
                "button": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/button",
                  "name": "loveToast",
                  "jcr:title": "Click here if you love toast!",
                  "type": "submit",
                  "value": "ILoveToast"
                }
              },
              ":itemsOrder": [
                "button"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>L’exportation JSON à partir des composants principaux nécessite la version 1.1.0 des composants principaux. Pour plus d’informations, voir les [informations de compatibilité des composants principaux v1](/help/versions.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de définir les paramètres du bouton.

![](/help/assets/chlimage_1-49.png)

* **Type**
   * **Bouton**
   * **Envoyer**

* **Titre** : texte affiché sur le bouton.
   * Si aucun titre n’est défini, le type de bouton est utilisé par défaut.

* **Nom** : nom du bouton qui est envoyé avec les données de formulaire.
* **Valeur** : valeur du bouton qui est envoyée avec les données de formulaire.

## Boîte de dialogue de conception {#design-dialog}

Il n’existe pas de boîte de dialogue de conception pour le composant de bouton de formulaire.

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant de bouton de formulaire [se trouve sur GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v1/button).

Le projet sur les composants principaux peut être téléchargé depuis GitHub.

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).
