---
title: Composant Formulaire masqué (v1)
description: Le composant Formulaire masqué des composants principaux permet l’affichage d’un champ masqué.
index: n
role: Architect, Developer, Admin, User
exl-id: 8e30dac0-5b4b-4fc7-af99-5791c98c90bf
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Composant Formulaire masqué (v1) {#form-hidden-component-v}

Le composant Formulaire masqué des composants principaux permet l’affichage d’un champ masqué.

## Utilisation {#usage}

Le composant Formulaire masqué des composants principaux permet la création de champs masqués pour transmettre des informations sur la page actuelle à AEM. Il est destiné à être utilisé avec le [composant de conteneur de formulaires](form-container-v1.md).

Les propriétés de champ peuvent être définies par l’éditeur de contenu dans la [boîte de dialogue de configuration](#configure-dialog).

## Version et compatibilité {#version-and-compatibility}

Ce document décrit la version v1 du composant Formulaire masqué, introduite à l’origine avec la version 1.0.0 des composants principaux avec AEM 6.3.

Le tableau ci-après répertorie la compatibilité de la version v1 du composant Formulaire masqué.

| Version d’AEM | Composant Formulaire masqué v1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Ce document décrit la version v1 du composant Formulaire masqué.
>
>Pour plus d’informations sur la version actuelle du composant Formulaire masqué, voir le document [Composant Formulaire masqué](/help/components/forms/form-hidden.md).

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple extrait de [We.Retail](https://helpx.adobe.com/fr/experience-manager/6-4/sites/developing/using/we-retail.html).

### HTML {#html}

```
<div class="cmp cmp-form aem-GridColumn aem-GridColumn--default--12">
 <form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
  <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
   <div class="visible aem-GridColumn aem-GridColumn--default--12">
    <input type="hidden" id="ghostToast" name="Invisible Toast" value="ghostToast">
   </div>
 </form>
</div>
```

### JSON {#json}

```
"container": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "columnCount": 12,
              "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
              ":items": {
                "hidden": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/hidden",
                  "name": "Invisible Toast",
                  "id": "ghostToast",
                  "value": "ghostToast"
                }
              },
              ":itemsOrder": [
                "hidden"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>L’exportation JSON à partir des composants principaux nécessite la version 1.1.0 des composants principaux. Pour plus d’informations, voir les [informations de compatibilité des composants principaux v1](/help/versions.md#release-history-and-compatibility).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de définir les paramètres du champ masqué.

![](/help/assets/chlimage_1-26.png)

* **Nom** : nom du champ qui est envoyé avec les données de formulaire.
* **Valeur** : valeur du champ qui est envoyée avec les données de formulaire.
* **Identifiant** : l’identifiant doit être unique sur la page et peut être utilisé pour lier les scripts à ce champ de formulaire.

## Boîte de dialogue de conception {#design-dialog}

Il n’existe pas de boîte de dialogue de conception pour le composant Formulaire masqué.

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Formulaire masqué [se trouve sur GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v1/hidden).

Le projet sur les composants principaux peut être téléchargé depuis GitHub.

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).
