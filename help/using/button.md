---
title: Composant de bouton
seo-title: Composant de bouton
description: 'null'
seo-description: Le composant de bouton des composants principaux permet de créer et d’afficher un bouton.
uuid: ec807de9-f76c-4850-9ece-c3e439a1d626
contentOwner: Utilisateur
content-type: référence
topic-tags: création
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: f093f58e-9755-4a4f-803a-ab93a50e6870
translation-type: ht
source-git-commit: d37cde072dea612ccb55ad31b4aaf42f17839cb4

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

| Version du composant | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant de bouton et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [Bibliothèque de composants](http://opensource.adobe.com/aem-core-wcm-components/library/button.html).

## Détails techniques {#technical-details}

Vous trouverez la documentation technique la plus récente sur le composant de bouton [sur GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/button/v1/button).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](developing.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur du contenu de définir le bouton et la façon dont il se comporte et apparaît pour un visiteur sur la page.

### Onglet Propriétés {#properties-tab}

![](assets/screen-shot-2019-08-29-12.19.32.png)

* **Texte** : texte à afficher sur le bouton.
* **Lien** : lien vers une page de contenu dans AEM, une ressource externe ou une ancre.
   * Utilisez la **boîte de dialogue de sélection** pour choisir un chemin dans AEM.
* **Icône** : identificateur pour l’affichage d’une icône dans le bouton.

### Onglet Accessibilité {#accessibility-tab}

![](assets/screen-shot-2019-08-29-12.19.43.png)

Dans l’onglet **Accessibilité**, les valeurs peuvent être définies pour les libellés d’[accessibilité ARIA]( https://www.w3.org/WAI/standards-guidelines/aria/) du composant.

* **Libellé** - Valeur d’un attribut de libellé ARIA pour le composant

## Boîte de dialogue de conception {#design-dialog}

### Onglet Styles {#styles-tab}

Le composant d’image prend en charge le [système de style](authoring.md#component-styling) AEM.
