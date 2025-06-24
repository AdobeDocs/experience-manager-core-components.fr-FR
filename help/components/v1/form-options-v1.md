---
title: Composant des options de formulaire (v1)
description: Le composant des options de formulaire des composants principaux permet la sélection d’options prédéfinies dans divers formats.
index: n
role: Architect, Developer, Admin, User
exl-id: a5e8656b-eddd-48ec-876b-39bbaa70edf6
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Composant des options de formulaire (v1) {#form-options-component-v}

Le composant des options de formulaire des composants principaux permet la sélection d’options prédéfinies dans divers formats.

## Utilisation {#usage}

Le composant des options de formulaire des composants principaux permet l’envoi de différents types d’options présentés de différentes manières. Il est destiné à être utilisé avec le [composant de conteneur de formulaires](form-container-v1.md).

La présentation des options, des étiquettes et des options individuelles peut être définie par l’éditeur de contenu dans la [boîte de dialogue de configuration](#configure-dialog).

## Version et compatibilité {#version-and-compatibility}

Ce document décrit la version v1 du composant des options de formulaire, introduite à l’origine avec la version 1.0.0 des composants principaux avec AEM 6.3.

Le tableau ci-après répertorie la compatibilité de la version v1 du composant des options de formulaire.

| Version du composant | AEM 6.3 | AEM 6.4 |
|--- |--- |--- |
| v2 | Compatible | Compatible |
| v1 | Compatible | Compatible |

>[!CAUTION]
>
>Ce document décrit la version v1 du composant des options de formulaire.
>
>Pour plus d’informations sur la version actuelle du composant des options de formulaire, voir le document [Composant des options de formulaire](/help/components/forms/form-options.md).

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple extrait de [We.Retail](https://helpx.adobe.com/fr/experience-manager/6-4/sites/developing/using/we-retail.html).

### Capture d’écran {#screenshot}

![](/help/assets/chlimage_1-89.png)

### HTML {#html}

```
<div class="cmp cmp-form aem-GridColumn aem-GridColumn--default--12">
<form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
    <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
    
    <div class="cmp cmp-options aem-GridColumn aem-GridColumn--default--12">

    <fieldset class="form-group checkbox">
        <legend>What is your favorite type of toast?</legend>
        
        <div class="checkbox-item">
            <label>
              <input type="checkbox" name="toasttypes" value="dry">
              Plain dry toast
            </label>
        </div>
<div class="checkbox-item">
            <label>
              <input type="checkbox" name="toasttypes" value="french">
              French toast
            </label>
        </div>
<div class="checkbox-item">
            <label>
              <input type="checkbox" name="toasttypes" value="texas">
              Texas toast
            </label>
        </div>

    </fieldset>
    
</div>
    
</form></div>
```

### JSON {#json}

```
"container": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "columnCount": 12,
              "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
              ":items": {
                "options": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/options",
                  "name": "toastTypes",
                  "jcr:title": "What is your favorite type of toast?",
                  "source": "local",
                  "type": "checkbox"
                }
              },
              ":itemsOrder": [
                "options"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>L’exportation JSON à partir des composants principaux nécessite la version 1.1.0 des composants principaux. Pour plus d’informations, voir les [informations de compatibilité des composants principaux v1](/help/versions.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de définir le type d’options qui doit être présenté, les étiquettes et les options disponibles.

![](/help/assets/chlimage_1-90.png)

* **Types**
Présentation des options.

   * **Cases à cocher**
   * **Boutons radio**
   * **Liste déroulante**
   * **Liste déroulante à sélection multiple**

* **Titre** : titre qui s’affiche comme libellé pour les options.
* **Nom** : nom du champ qui est envoyé avec les données de formulaire.
* **Source** : emplacement de définition des options.

   * **Local** : défini dans le composant.
      * Appuyez ou cliquez sur le bouton **Ajouter** pour ajouter une valeur. Sinon, appuyez ou cliquez sur **Supprimer** pour supprimer une valeur.
      * **Valeur** : valeur enregistrée lorsque cette option est sélectionnée lors de l’envoi du formulaire.
      * **Texte** : libellé de l’option affichée sur le formulaire.
      * **En cours** : l’option est marquée comme étant sélectionnée lors du chargement du formulaire.
      * **Désactivé** : l’option n’est pas sélectionnable mais toujours affichée.
      * **Liste** : liste statique définie ailleurs dans AEM est utilisée pour l’option.
         * **Liste** : chemin d’accès à la liste statique dans AEM.
            * Utilisez le bouton Parcourir pour localiser la ressource de liste.
      * **Source de données** : une source de données est utilisée pour les options.
         * **Source de données** : type de ressource de la source de données.
* **Message d’aide** : conseil à l’intention de l’utilisateur sur ce qui peut être entré dans le champ.

## Boîte de dialogue de conception {#design-dialog}

Il n’existe pas de boîte de dialogue de conception pour le composant des options de formulaire.

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Options du formulaire [se trouve sur GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v1/options).

Le projet sur les composants principaux peut être téléchargé depuis GitHub.

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).
