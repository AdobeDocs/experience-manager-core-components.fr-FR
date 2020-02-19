---
title: Composant de texte de formulaire
description: Le composant de texte de formulaire des composants principaux permet l’entrée de texte de formulaire pour envoi.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Composant de texte de formulaire{#form-text-component}

Le composant de texte de formulaire des composants principaux permet l’entrée de texte de formulaire pour envoi.

## Utilisation {#usage}

Le composant de texte de formulaire permet l’envoi de différents types de texte et est conçu pour être utilisé avec le [composant de conteneur de formulaires](form-container.md). Le type de validation de texte, d’étiquettes et de messages d’aide peut être défini par l’éditeur de contenu dans la [boîte de dialogue de configuration](#configure-dialog).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de texte de formulaire est v2, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.3 | AEM 6.4 | AEM 6.5 |  d’AEM en tant que Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Compatible | Compatible | Compatible | Compatible |
| [v1](/help/components/v1/form-text-v1.md) | Compatible | Compatible | Compatible | - |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple extrait de [We.Retail](https://docs.adobe.com/content/help/en/experience-manager-65/developing/bestpractices/we-retail/we-retail.html).

### Capture d’écran {#screenshot}

![](/help/assets/chlimage_1-22.png)

### HTML {#html}

```
<div class="text aem-GridColumn aem-GridColumn--default--12">
   <div class="cmp-form-text">
      <label for="form-text-2146967">How many pieces of toast would you like?
      </label>
   <input class="cmp-form-text__text" type="number" id="form-text-2146967" name="pieces">
   </div>
</div>
```

### JSON {#json}

```
"text":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     "id":"form-text-2146967",
                     "title":"How many pieces of toast would you like?",
                     "name":"pieces",
                     "value":"",
                     "helpMessage":"",
                     "type":"number",
                     "readOnly":false,
                     "required":false,
                     "requiredMessage":"",
                     "constraintMessage":"",
                     "rows":2,
                     "defaultValue":"",
                     ":type":"core/wcm/components/form/text/v2/text"
                  }
```

### Détails techniques {#technical-details}

The latest technical documentation about the Form Text Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_form_text_v2).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de définir le type de texte à saisir, ainsi que les valeurs et étiquettes par défaut.

### Onglet Principal {#main-tab}

![](/help/assets/chlimage_1-23.png)

* **Contrainte**
Type de texte à saisir et par rapport auquel il sera validé.
   * **Texte**
   * **Zone de texte**
   * **Courriel**
   * **Téléphone**
   * **Date**
   * **Nombre**
   * **Mot de passe**
* **Lignes de texte**
Nombre de lignes à afficher dans la zone de texte (affiché uniquement lorsque la **contrainte** est définie sur **Zone de texte**).
* **Étiquette**
Libellé qui s’affiche pour le champ.
* **Masquer l’étiquette**
Nécessaire si l’étiquette est requise uniquement à des fins d’accessibilité et ne transmet aucune information visuelle supplémentaire sur le champ.
* **Nom de l’élément**
Nom du champ qui est envoyé avec les données de formulaire.
* **Valeur**
Valeur par défaut prérenseignée dans le champ.

### Onglet À propos {#about-tab}

![](/help/assets/chlimage_1-24.png)

* **Message d’aide**
Conseil à l’intention de l’utilisateur sur ce qui peut être entré dans le champ.
* **Afficher le message d’aide comme espace réservé**
Indique s’il convient d’afficher le message d’aide dans l’entrée de formulaire lorsqu’elle est vide et désactivée.

### Onglet Contraintes {#constraints-tab}

![](/help/assets/chlimage_1-25.png)

* **Message de contrainte**
   * Message affiché sous forme d’info-bulle lors de l’envoi du formulaire si la valeur ne valide pas le type sélectionné
   * Non affiché pour les types de contraintes **Texte** et **Zone de texte**.
* **Requis**
Indique si l’utilisateur doit renseigner une valeur avant d’envoyer le formulaire.
* **Rendre en lecture seule**
Si cette option est sélectionnée, l’utilisateur ne peut pas modifier la valeur du champ.

## Boîte de dialogue de conception {#design-dialog}

Il n’existe pas de boîte de dialogue de conception pour le composant de texte de formulaire.
