---
title: Composant de bouton de courrier électronique
description: Le composant Bouton Courrier électronique permet de configurer et d’afficher un élément de bouton dans votre contenu.
role: Architect, Developer, Admin, User
exl-id: b144e8d1-1097-475d-b2eb-3353c176afb9
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 43%

---


# Composant de bouton de courrier électronique {#email-button-component}

Le composant Bouton Courrier électronique permet de configurer et d’afficher un élément de bouton dans votre contenu.

## Utilisation {#usage}

Le composant Bouton Courrier électronique permet d’inclure un bouton dans votre contenu, cliquable par le lecteur de contenu, lié à des ressources supplémentaires.

* Les propriétés du bouton peuvent être définies dans la [boîte de dialogue de configuration.](#configure-dialog)
* Les styles du composant de bouton de courrier électronique peuvent être définis dans la variable [boîte de dialogue de conception.](#design-dialog)

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de bouton de messagerie est v1, qui a été introduite avec la version x des composants principaux de messagerie en octobre 2022. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatible | Compatible |

Pour plus d’informations sur les versions et versions des composants principaux, consultez le document . [Envoi des versions des composants principaux par courrier électronique.](/help/email/versions.md)

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant de bouton de courrier électronique et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [Bibliothèque de composants.](https://adobe.com/go/aem_cmp_library_email_button)

## Détails techniques {#technical-details}

Documentation technique la plus récente sur le composant de bouton de courrier électronique [est disponible sur GitHub.](https://adobe.com/go/aem_cmp_tech_email_button_v1)

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux.](/help/developing/overview.md)

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de définir le bouton et la manière dont il se comporte et apparaît pour un lecteur de votre contenu.

### Onglet Propriétés {#properties-tab}

![Onglet Propriétés de la boîte de dialogue de modification du composant Bouton](/help/email/assets/email-button-edit-properties.png)

* **Texte** : texte à afficher sur le bouton.
   * Cliquez sur l’icône Campagne pour ouvrir la [Sélectionner la variable Adobe Campaign](/help/email/campaign-variables.md) pour insérer du contenu dynamique depuis Adobe Campaign.
* **Lien** : lien vers une page de contenu dans AEM, une ressource externe ou une ancre.
   * Utilisez la **boîte de dialogue de sélection** pour choisir un chemin dans AEM.
   * Cliquez sur l’icône Campagne pour ouvrir la [Sélectionner la variable Adobe Campaign](/help/email/campaign-variables.md) pour insérer du contenu dynamique depuis Adobe Campaign.
* **Icône** : identificateur pour l’affichage d’une icône dans le bouton.
* **ID** - Cette option permet de contrôler l’identifiant unique du composant dans le HTML.
   * Si rien n’est indiqué, un identifiant unique est automatiquement généré et peut être trouvé en examinant le contenu qui en résulte.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur CSS.
* **Ouvrir le lien dans un nouvel onglet** : si cette option est cochée, le lien s’ouvre dans un nouvel onglet du navigateur.

### Onglet Accessibilité {#accessibility-tab}

![Onglet Accessibilité de la boîte de dialogue de modification du composant Bouton](/help/email/assets/email-button-edit-accessibility.png)

Dans l’onglet **Accessibilité**, les valeurs peuvent être définies pour les étiquettes d’[accessibilité ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) du composant.

* **Étiquette** : Valeur d’un attribut de étiquette ARIA pour le composant

### Onglet Styles {#styles-tab-edit}

Le composant de bouton de courrier électronique prend en charge l’AEM [Système de style.](/help/get-started/authoring.md#component-styling).

Utilisez la liste déroulante pour sélectionner les styles à appliquer au composant. Les sélections effectuées dans la boîte de dialogue de modification ou dans la barre d’outils du composant ont le même effet.

Les styles doivent être configurés pour ce composant dans la variable [boîte de dialogue de conception](#design-dialog) pour que l’onglet soit disponible.

## Boîte de dialogue de conception {#design-dialog}

### Onglet Styles {#styles-tab}

Le composant de bouton de courrier électronique prend en charge l’AEM [Système de style](/help/get-started/authoring.md#component-styling).
