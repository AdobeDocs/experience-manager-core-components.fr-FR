---
title: Composant de texte de formulaire (v1)
description: Le composant de texte de formulaire des composants principaux permet l’entrée de texte de formulaire pour envoi.
index: n
role: Architect, Developer, Admin, User
exl-id: d6fbc596-cb42-4478-8a3c-aa5aead3be0a
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 100%

---

# Composant de texte de formulaire (v1) {#form-text-component-v}

Le composant de texte de formulaire des composants principaux permet l’entrée de texte de formulaire pour envoi.

## Utilisation {#usage}

Le composant de texte de formulaire permet l’envoi de différents types de texte et est conçu pour être utilisé avec le [composant de conteneur de formulaires](form-container-v1.md).

Le type de validation de texte, d’étiquettes et de messages d’aide peut être défini par l’éditeur de contenu dans la [boîte de dialogue de configuration](#configure-dialog).

## Version et compatibilité {#version-and-compatibility}

Ce document décrit la version v1 du composant de texte de formulaire, introduite à l’origine avec la version 1.0.0 des composants principaux avec AEM 6.3.

Le tableau ci-après répertorie la compatibilité de la version v1 du composant de texte de formulaire.

| Version d’AEM | Composant de texte de formulaire v1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Ce document décrit la version v1 du composant de texte de formulaire.
>
>Pour plus d’informations sur la version actuelle du composant de texte de formulaire, voir le document [Composant de texte de formulaire](/help/components/forms/form-text.md).

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple extrait de [We.Retail](https://helpx.adobe.com/fr/experience-manager/6-4/sites/developing/using/we-retail.html).

### Capture d’écran {#screenshot}

![](/help/assets/chlimage_1-22.png)

### HTML {#html}

```
<div class="cmp cmp-form aem-GridColumn aem-GridColumn--default--12">
 <form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
     <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
     <div class="cmp cmp-form-field aem-GridColumn aem-GridColumn--default--12">
   <div class="form-group">
       <label for="form-text-978484744">How many pieces of toast would you like?</label>
          <input type="number" id="form-text-978484744" name="pieces">
   </div>
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
                "text": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/text",
                  "name": "piecesOfToast",
                  "jcr:title": "How many pieces of toast would you like?",
                  "type": "number",
                  "rows": "2"
                }
              },
              ":itemsOrder": [
                "text"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>L’exportation JSON à partir des composants principaux nécessite la version 1.1.0 des composants principaux. Pour plus d’informations, voir les [informations de compatibilité des composants principaux v1](/help/versions.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de définir le type de texte à saisir, ainsi que les valeurs et étiquettes par défaut.

### Principal {#main}

![](/help/assets/chlimage_1-23.png)

* **Contrainte** : type de texte à saisir et par rapport auquel il sera validé.

   * **Texte**
   * **Zone de texte**
   * **Courriel**
   * **Téléphone**
   * **Date**
   * **Nombre**
   * **Mot de passe**

* **Lignes de texte** : nombre de lignes à afficher dans la zone de texte (affiché uniquement lorsque la **contrainte** est définie sur **Zone de texte**).

* **Étiquette** : libellé qui s’affiche pour le champ.
* **Masquer l’étiquette** : nécessaire si l’étiquette est requise uniquement à des fins d’accessibilité et ne transmet aucune information visuelle supplémentaire sur le champ.
* **Nom de l’élément** : nom du champ qui est envoyé avec les données de formulaire.
* **Valeur** : valeur par défaut prérenseignée dans le champ.

### À propos {#about}

![](/help/assets/chlimage_1-24.png)

* **Message d’aide** : conseil à l’intention de l’utilisateur sur ce qui peut être entré dans le champ.
* **Afficher le message d’aide comme espace réservé** : indique s’il convient d’afficher le message d’aide dans l’entrée de formulaire lorsqu’elle est vide et désactivée.

### Contraintes {#constraints}

![](/help/assets/chlimage_1-25.png)

* **Message de contrainte**

   * Message affiché sous forme d’info-bulle lors de l’envoi du formulaire si la valeur ne valide pas le type sélectionné
   * Non affiché pour les types de contraintes **Texte** et **Zone de texte**.

* **Obligatoire** : indique si l’utilisateur doit renseigner une valeur avant d’envoyer le formulaire.
* **Rendre en lecture seule** : si cette option est sélectionnée, l’utilisateur ne peut pas modifier la valeur du champ.

## Boîte de dialogue de conception {#design-dialog}

Il n’existe pas de boîte de dialogue de conception pour le composant de texte de formulaire.

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant de texte de formulaire [se trouve sur GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v1/text).

Le projet sur les composants principaux peut être téléchargé depuis GitHub.

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).
