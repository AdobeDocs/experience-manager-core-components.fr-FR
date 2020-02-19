---
title: Composant Onglets
description: Le composant Onglets permet la création de plusieurs onglets pour disposer le contenu sur une page.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Composant Onglets

Le composant Onglets des composants principaux permet l’organisation de contenu sur plusieurs onglets.

## Utilisation {#usage}

Le composant Onglets permet à l’auteur de contenu d’organiser le contenu de la page dans plusieurs onglets.

La [boîte de dialogue de modification](#edit-dialog) permet à l’auteur de contenu de définir plusieurs onglets et de définir l’onglet actif. À l’aide de [la boîte de dialogue de conception](#design-dialog), l’auteur du modèle peut définir les composants qui peuvent être ajoutés aux onglets et personnaliser les styles.

>[!NOTE]
>
>Les composants d’onglets imbriqués (onglets dans les onglets) sont pris en charge.
>
>Les composants des onglets simples (non imbriqués) peuvent être localisés/sélectionnés à l’aide de l’[arborescence de contenu](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html#content-tree), mais les onglets imbriqués ne peuvent pas l’être.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Onglets est v1, qui a été introduite avec la version 2.2.0 des composants principaux d’octobre 2018. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.3 | AEM 6.4 | AEM 6.5 |  d’AEM en tant que Cloud Service |
|--- |--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant Onglets, des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [Bibliothèque de composants](https://adobe.com/go/aem_cmp_library_tabs).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Onglets [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_tabs_v1).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de modification{#edit-dialog}

La boîte de dialogue de modification permet à l’auteur de contenu de créer, renommer et réorganiser les onglets et de définir l’onglet actif.

### Onglet Éléments {#items-tab}

![](/help/assets/screen-shot-2019-08-29-12.28.16.png)

Utilisez le bouton **Ajouter** pour ouvrir le sélecteur de composants afin de choisir le composant à ajouter sous forme d’onglet. Une fois le composant ajouté, une entrée est ajoutée à la liste qui contient les colonnes suivantes :

* **Icône** : icône du type de composant de l’onglet pour une identification facile dans la liste. Pointez dessus pour afficher le nom complet du composant sous forme d’info-bulle.
* **Description** : description utilisée comme texte de l’onglet. Par défaut, il s’agit du nom du composant sélectionné pour l’onglet.
* **Supprimer** : appuyez ou cliquez dessus pour supprimer l’onglet du composant Onglets.
* **Réorganiser** : appuyez ou cliquez dessus et faites glisser pour réorganiser l’ordre des onglets.

>[!TIP]
>
>Si la fenêtre d’affichage de la page est réduite, de sorte que la boîte de dialogue de modification s’affiche en plein écran, le bouton **Ajouter** est masqué. Vous pouvez toujours ajouter des composants au composant Onglets en [les faisant glisser depuis l’explorateur de composants et en les déposant ensuite sur le composant Onglets dans l’éditeur de page](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component).

### Onglet Propriétés {#properties-tab}

![](/help/assets/screen-shot-2019-08-29-12.28.32.png)

Dans l’onglet **Propriétés**, l’auteur du contenu peut définir quel onglet est actif lorsque la page est chargée. Avec l’option **Par défaut**, le premier onglet est sélectionné.

### Onglet Accessibilité {#accessibility-tab}

![](/help/assets/screen-shot-2019-08-29-12.28.40.png)

Dans l’onglet **Accessibilité**, les valeurs peuvent être définies pour les libellés d’[accessibilité ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) du composant.

* **Libellé** - Valeur d’un attribut de libellé ARIA pour le composant

## Sélectionner un panneau {#select-panel}

L’auteur du contenu peut utiliser l’option **Sélectionner un panneau** la barre d’outils du composant pour choisir un panneau différent, ainsi que pour réorganiser l’ordre des onglets.

![](/help/assets/screenshot_2018-10-11at165417.png)

Lorsque vous sélectionnez l’option **Sélectionner un panneau** dans la barre d’outils du composant, les onglets configurés s’affichent sous forme de liste déroulante.

* La liste est classée en fonction de la disposition des onglets et est reflétée dans la numérotation.
* Le type de composant de l’onglet est affiché en premier, suivi de la description de l’onglet une police plus claire.

![](/help/assets/screenshot_2018-10-11at165154.png)

* Vous pouvez commuter la vue de l’éditeur dans cet onglet en appuyant ou en cliquant sur une entrée dans la liste déroulante.
* Vous pouvez réorganiser les onglets statiques à l’aide des poignées de glissement.

>[!NOTE]
>
>Les onglets ne sont pas sélectionnables par l’auteur en mode **Édition**. Utilisez le mode **[Aperçu](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#preview-mode)**ou l’option**[ Afficher comme publié(e)](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** pour interagir avec les onglets comme un lecteur du contenu publié.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir quels composants peuvent être ajoutés en tant qu’éléments au composant Onglets et de définir les styles personnalisés disponibles pour l’auteur du contenu.

### Onglet Composants autorisés {#allowed-components-tab}

L’onglet **Composants autorisés** permet de définir quels composants peuvent être ajoutés en tant qu’éléments au composant Onglets par l’auteur du contenu.

L’onglet Composants autorisés fonctionne de la même manière que l’onglet du même nom lors de la [définition de la stratégie et des propriétés d’un conteneur de mises en page dans l’éditeur de modèles](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

### Onglet Styles {#styles-tab}

Le composant Onglets prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.
