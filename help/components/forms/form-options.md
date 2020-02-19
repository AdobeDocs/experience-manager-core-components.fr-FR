---
title: Composant des options de formulaire
description: Le composant des options de formulaire des composants principaux permet la sélection d’options prédéfinies dans divers formats.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Composant des options de formulaire {#form-options-component}

Le composant des options de formulaire des composants principaux permet la sélection d’options prédéfinies dans divers formats.

## Utilisation {#usage}

Le composant des options de formulaire des composants principaux permet l’envoi de différents types d’options présentés de différentes manières. Il est destiné à être utilisé avec le [composant de conteneur de formulaires](form-container.md).

La présentation des options, des étiquettes et des options individuelles peut être définie par l’éditeur de contenu dans la [boîte de dialogue de configuration](#configure-dialog).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant des options de formulaire est v2, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.3 | AEM 6.4 | AEM 6.5 |  d’AEM en tant que Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Compatible | Compatible | Compatible | Compatible |
| [v1](/help/components/v1/form-options-v1.md) | Compatible | Compatible | Compatible | - |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple extrait de [We.Retail](https://docs.adobe.com/content/help/en/experience-manager-65/developing/bestpractices/we-retail/we-retail.html).

### Capture d’écran {#screenshot}

![](/help/assets/screen_shot_2018-01-12at113648.png)

### HTML {#html}

```
<form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="cmp-form aem-Grid aem-Grid--12 aem-Grid--default--12">
    <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
    
    <div class="hidden aem-GridColumn aem-GridColumn--default--12">
<input type="hidden" id="form-hidden-66464844" name="hidden">

</div>
<div class="hidden aem-GridColumn aem-GridColumn--default--12">
<input type="hidden" id="form-hidden-858231075" name="hidden">

</div>
<div class="hidden aem-GridColumn aem-GridColumn--default--12">
<input type="hidden" id="form-hidden-862566768" name="hidden">

</div>
<div class="container responsivegrid aem-GridColumn aem-GridColumn--default--12">

    <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container/container">
    
    <div class="options aem-GridColumn aem-GridColumn--default--12">

    <fieldset class="cmp-form-options">
        
            <legend class="cmp-form-options__legend">What is your favorite type of toast?</legend>
            <label class="cmp-form-options__field-label">
                <input class="cmp-form-options__field cmp-form-options__field--radio" type="radio" name="favToast" value="dryToast">
                Plain dry toast
            </label>
<label class="cmp-form-options__field-label">
                <input class="cmp-form-options__field cmp-form-options__field--radio" type="radio" name="favToast" value="frenchToast">
                French Toast
            </label>
<label class="cmp-form-options__field-label">
                <input class="cmp-form-options__field cmp-form-options__field--radio" type="radio" name="favToast" value="texasToast">
                Texas Toast
            </label>

    </fieldset>

</div>

</div></form>
```

### JSON {#json}

```
"container":{  
                           "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                           "columnCount":12,
                           "gridClassNames":"aem-Grid aem-Grid--12 aem-Grid--default--12",
                           ":items":{  
                              "options_816658469":{  
                                 "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                                 "id":"form-options-269951232",
                                 "title":"What is your favorite type of toast?",
                                 "name":"favToast",
                                 "type":"RADIO",
                                 "items":[  
                                    {  
                                       "value":"dryToast",
                                       "text":"Plain dry toast",
                                       "selected":false,
                                       "disabled":false
                                    },
                                    {  
                                       "value":"frenchToast",
                                       "text":"French Toast",
                                       "selected":false,
                                       "disabled":false
                                    },
                                    {  
                                       "value":"texasToast",
                                       "text":"Texas Toast",
                                       "selected":false,
                                       "disabled":false
                                    }
                                 ],
                                 ":type":"core/wcm/sandbox/components/form/options/v2/options"
                              }
                           },
                           ":itemsOrder":[  
                              "options_816658469"
                           ],
                           ":type":"core/wcm/sandbox/components/form/container/v2/container"
                        }
```

### Détails techniques {#technical-details}

The latest technical documentation about the Form Options Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_form_options_v2).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de définir le type d’options qui doit être présenté, les étiquettes et les options disponibles.

![](/help/assets/screen_shot_2018-01-12at113153.png)

* **Types** : présentation des options.
   * **Cases à cocher**
   * **Boutons radio**
   * **Liste déroulante**
   * **Liste déroulante à sélection multiple**
* **Titre**
Titre affiché comme libellé pour les options.
* **Nom**
Nom du champ qui est envoyé avec les données de formulaire.
* **Source**
Emplacement de définition des options.
   * **Local**
Défini dans le composant.
      * Appuyez ou cliquez sur le bouton **Ajouter** pour ajouter une valeur. Sinon, appuyez ou cliquez sur **Supprimer** pour supprimer une valeur.
      * **Valeur**
Valeur enregistrée lorsque cette option est sélectionnée lors de l’envoi du formulaire.
      * **Texte**
Libellé de l’option affichée sur le formulaire.
      * **Active**
L’option est marquée comme étant sélectionnée lors du chargement du formulaire.
      * **Désactivé**
L’option n’est pas sélectionnable mais elle est toujours affichée.
      * **Liste**
Liste statique définie ailleurs dans AEM est utilisée pour les options.
         * **Liste**
Chemin d’accès à la liste statique dans AEM.
            * Utilisez le bouton Parcourir pour localiser la ressource de liste.
      * **Source des données**
Une source de données est utilisée pour les options.
         * **Source des données**
Type de ressource de la source de données.
* **Message d’aide**
Conseil à l’intention de l’utilisateur sur ce qui peut être entré dans le champ.

## Boîte de dialogue de conception {#design-dialog}

### Onglet Styles {#styles-tab}

Le composant des options de formulaire prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.
