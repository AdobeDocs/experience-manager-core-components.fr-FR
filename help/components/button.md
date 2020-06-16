---
title: Composant de bouton
description: Le composant de bouton des composants principaux permet de créer et d’afficher un bouton.
translation-type: ht
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: ht
source-wordcount: '438'
ht-degree: 100%

---


# Composant de bouton{#button-component}

Le composant de bouton des composants principaux permet de configurer et d’afficher un élément de bouton sur une page.

## Utilisation {#usage}

Le composant de bouton des composants principaux permet l’inclusion d’un bouton sur une page.

* Les propriétés du bouton peuvent être définies dans la [boîte de dialogue de configuration](#configure-dialog).
* Les styles du composant de bouton peuvent être définis dans la [boîte de dialogue de conception](#design-dialog).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de bouton est v1, qui a été introduite avec la version 2.5.0 des composants principaux en février 2019. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant de bouton et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_button).

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant de bouton [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_button_v1).

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

Dans l’onglet **Accessibilité**, les valeurs peuvent être définies pour les libellés d’[accessibilité ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) du composant.

* **Libellé** - Valeur d’un attribut de libellé ARIA pour le composant

## Boîte de dialogue de conception {#design-dialog}

### Onglet Styles {#styles-tab}

Le composant d’image prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.
