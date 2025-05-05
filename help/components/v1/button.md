---
title: Composant de bouton (v1)
description: Le composant Bouton des composants principaux permet de créer et d’afficher un bouton.
role: Architect, Developer, Admin, User
exl-id: 63af16e4-dd4d-426d-88ef-769ecd1b3175
source-git-commit: e291d4c1bfd37292d68c236178f9681c4e5ee741
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 98%

---

# Composant de bouton (v1) {#button-component}

Le composant Bouton des composants principaux permet de configurer et d’afficher un élément de bouton sur une page.

## Utilisation {#usage}

Le composant Bouton des composants principaux permet l’inclusion d’un bouton sur une page.

* Les propriétés du bouton peuvent être définies dans la [boîte de dialogue de configuration](#configure-dialog).
* Les styles du composant de bouton peuvent être définis dans la [boîte de dialogue de conception](#design-dialog).

## Version et compatibilité {#version-and-compatibility}

Le document décrit la version v1 du composant Bouton, qui a été introduite avec la version 2.5.0 des composants principaux en juin 2019.

>[!CAUTION]
>
>Ce document décrit la version v1 du composant Bouton.
>
>Pour plus d’informations sur la version actuelle du composant Bouton, consultez le document [Composant Bouton](/help/components/button.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant de bouton et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_button).

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant de bouton [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_button_v1_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur du contenu de définir le bouton et la façon dont il se comporte et apparaît pour un visiteur sur la page.

### Onglet Propriétés {#properties-tab}

![Onglet Propriétés de la boîte de dialogue de modification du composant Bouton](/help/assets/button-edit-properties.png)

* **Texte** : texte à afficher sur le bouton.
* **Lien** : lien vers une page de contenu dans AEM, une ressource externe ou une ancre.
   * Utilisez la **boîte de dialogue de sélection** pour choisir un chemin dans AEM.
* **Icône** : identificateur pour l’affichage d’une icône dans le bouton.
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

### Onglet Accessibilité {#accessibility-tab}

![Onglet Accessibilité de la boîte de dialogue de modification du composant Bouton](/help/assets/button-edit-accessibility.png)

Dans l’onglet **Accessibilité**, les valeurs peuvent être définies pour les étiquettes d’[accessibilité ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) du composant.

* **Étiquette** : Valeur d’un attribut de étiquette ARIA pour le composant

## Boîte de dialogue de conception {#design-dialog}

### Onglet Styles {#styles-tab}

Le composant Bouton prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

## Couche de données client Adobe {#data-layer}

Le composant Bouton prend en charge la [couche de données client Adobe](/help/developing/data-layer/overview.md).
