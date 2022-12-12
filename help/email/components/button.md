---
title: Composant Bouton d’e-mail
description: Le composant Bouton d’e-mail permet de configurer et d’afficher un élément de bouton dans votre contenu.
role: Architect, Developer, Admin, User
exl-id: b144e8d1-1097-475d-b2eb-3353c176afb9
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 100%

---


# Composant Bouton d’e-mail {#email-button-component}

Le composant Bouton d’e-mail permet de configurer et d’afficher un élément de bouton dans votre contenu.

## Utilisation {#usage}

Le composant Bouton d’e-mail permet d’inclure un bouton dans votre contenu. Le lecteur de contenu peut cliquer dessus et ainsi accéder à des ressources supplémentaires.

* Les propriétés du bouton peuvent être définies dans la [boîte de dialogue de configuration.](#configure-dialog)
* Les styles du composant Bouton d’e-mail peuvent être définis dans la [boîte de dialogue de conception.](#design-dialog)

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Bouton d’e-mail est v1. Celle-ci a été introduite avec la version X des composants principaux d’e-mail en octobre 2022. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux d’e-mail.](/help/email/versions.md)

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant Bouton d’e-mail et obtenir des exemples de ses options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants.](https://adobe.com/go/aem_cmp_library_email_button)

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Bouton d’e-mail [se trouve sur GitHub.](https://adobe.com/go/aem_cmp_tech_email_button_v1)

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux.](/help/developing/overview.md)

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet au créateur de contenu de définir le bouton et la manière dont il se comporte et apparaît comme un lecteur de votre contenu.

### Onglet Propriétés {#properties-tab}

![Onglet Propriétés de la boîte de dialogue de modification du composant Bouton](/help/email/assets/email-button-edit-properties.png)

* **Texte** : texte à afficher sur le bouton.
   * Cliquez sur l’icône Campagne pour ouvrir la boîte de dialogue [Sélectionner la variable Adobe Campaign](/help/email/campaign-variables.md) pour insérer du contenu dynamique depuis Adobe Campaign.
* **Lien** : lien vers une page de contenu dans AEM, une ressource externe ou une ancre.
   * Utilisez la **boîte de dialogue de sélection** pour choisir un chemin dans AEM.
   * Cliquez sur l’icône Campagne pour ouvrir la boîte de dialogue [Sélectionner la variable Adobe Campaign](/help/email/campaign-variables.md) et insérer du contenu dynamique depuis Adobe Campaign.
* **Icône** : identificateur pour l’affichage d’une icône dans le bouton.
* **ID** : Cette option permet de contrôler l’identifiant unique du composant dans le HTML.
   * Si rien n’est indiqué, un ID unique est généré automatiquement pour vous. Vous le trouverez en examinant le contenu obtenu.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur CSS.
* **Ouvrir le lien dans un nouvel onglet** : si cette option est cochée, le lien s’ouvre dans un nouvel onglet du navigateur.

### Onglet Accessibilité {#accessibility-tab}

![Onglet Accessibilité de la boîte de dialogue de modification du composant Bouton](/help/email/assets/email-button-edit-accessibility.png)

Dans l’onglet **Accessibilité**, les valeurs peuvent être définies pour les étiquettes d’[accessibilité ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) du composant.

* **Étiquette** : Valeur d’un attribut de étiquette ARIA pour le composant

### Onglet Styles {#styles-tab-edit}

Le composant Bouton d’e-mail prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

Utilisez la liste déroulante pour sélectionner les styles à appliquer au composant. Les sélections effectuées dans la boîte de dialogue de modification ou dans la barre d’outils du composant ont le même effet.

Pour accéder à l’onglet, les styles doivent être configurés pour ce composant dans la [boîte de dialogue de conception](#design-dialog).

## Boîte de dialogue de conception {#design-dialog}

### Onglet Styles {#styles-tab}

Le composant Bouton d’e-mail prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.
