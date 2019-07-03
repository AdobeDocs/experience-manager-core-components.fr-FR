---
title: Composant Onglets
seo-title: Composant Onglets
description: Le composant Onglets permet la création de plusieurs onglets pour disposer le contenu sur une page.
seo-description: Le composant Onglets permet la création de plusieurs onglets pour disposer le contenu sur une page.
uuid: 46f71233-8b12-4887-a0c6-ad24dc469cb1
content-type: référence
topic-tags: core-components
discoiquuid: 966d47fb-d35d-4103-b29d-4ef0aa739f24
translation-type: tm+mt
source-git-commit: eef608fb06001485aa2c2c0b574af412ed7f15a4

---


# Composant Onglets

Le composant principal Composant Onglets permet l’organisation de contenu sur plusieurs onglets.

## Utilisation {#usage}

Le composant Onglets permet à l’auteur de contenu d’organiser le contenu de la page dans plusieurs onglets.

La [boîte de dialogue Modifier](#edit-dialog) permet à l’auteur de contenu de définir plusieurs onglets et de définir l’onglet actif. A l’aide de [la boîte de dialogue Conception](#design-dialog), l’auteur du modèle peut définir les composants qui peuvent être ajoutés aux onglets et personnaliser les styles.

>[!NOTE]
>
>Les composants d’onglets imbriqués (onglets dans les onglets) sont pris en charge.
>
>Simple (non-nested) tab components can be located/selected using the [content tree](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/author-environment-tools.html), however nested tabs can not be.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Onglets est v1, qui a été introduite avec la version 2.2.0 des composants principaux d’octobre 2018 et est décrite dans ce document.

Le tableau suivant détaille toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Composant Version | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Compatible | Compatible | Compatible |

Pour plus d’informations sur les versions et les mises à jour des composants principaux, consultez le document sur les [versions des composants principaux](versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant Onglets, des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [Bibliothèque de composants](http://opensource.adobe.com/aem-core-wcm-components/library/tabs.html).

### Détails techniques {#technical-details}

The latest technical documentation about the Tabs Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/tabs/v1/tabs).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](developing.md).

## Boîte de dialogue Modifier{#edit-dialog}

La boîte de dialogue Modifier permet à l’auteur de contenu de créer, renommer et réorganiser les onglets et de définir l’onglet actif.

### Onglet Éléments {#items-tab}

![](assets/screenshot_2018-10-11at153557.png)

Utilisez le bouton **Ajouter** pour ouvrir le sélecteur de composants afin de choisir le composant à ajouter sous forme d’onglet. Une fois ajouté, une entrée est ajoutée à la liste qui contient les colonnes suivantes :

* **Icône** - Icône du type de composant de l’onglet pour une identification facile dans la liste. Placez le pointeur de la souris sur pour afficher le nom complet du composant sous forme d’info-bulle.
* **Description** - Description utilisée comme texte de l’onglet, par défaut au nom du composant sélectionné pour l’onglet.
* **Supprimer** - Appuyez ou cliquez dessus pour supprimer l’onglet du composant Onglets.
* **Réorganiser** - Appuyez ou cliquez dessus et faites glisser pour réorganiser l’ordre des onglets.

### Onglet Propriétés {#properties-tab}

![](assets/screenshot_2018-10-19at140646.png)

Dans l’onglet **Propriétés**, l’auteur du contenu peut définir quel onglet est actif lorsque la page est chargée. Avec l’option **Par défaut**, le premier onglet est sélectionné.

## Sélectionner un panneau {#select-panel}

L’auteur du contenu peut utiliser l’option **Sélectionner un panneau** la barre d’outils du composant pour choisir un panneau différent, ainsi que pour réorganiser l’ordre des onglets.

![](assets/screenshot_2018-10-11at165417.png)

Lorsque vous sélectionnez l’option **Sélectionner un panneau** dans la barre d’outils du composant, les onglets configurés s’affichent sous forme de liste déroulante.

* La liste est classée en fonction de la disposition des onglets et est reflétée dans la numérotation.
* Le type de composant de l’onglet est affiché en premier, suivi de la description de l’onglet une police plus claire.

![](assets/screenshot_2018-10-11at165154.png)

* Vous pouvez commuter la vue de l’éditeur dans cet onglet en appuyant ou en cliquant sur une entrée dans la liste déroulante.
* Vous pouvez réorganiser les onglets statiques à l’aide des poignées de glissement.

>[!NOTE]
>
>Les onglets ne sont pas sélectionnables par l’auteur en mode **Édition**. Use [**Preview** mode](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html) or the **[View as Published](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html)** option to interact with the tabs as a reader of the published content would.

## Boîte de dialogue Conception {#design-dialog}

La boîte de dialogue Conception permet à l’auteur du modèle de définir quels composants peuvent être ajoutés en tant qu’éléments au composant Onglets et de définir les styles personnalisés disponibles pour l’auteur du contenu.

### Onglet Composants autorisés {#allowed-components-tab}

L’onglet **Composants autorisés** permet de définir quels composants peuvent être ajoutés en tant qu’éléments au composant Onglets par l’auteur du contenu.

L’onglet Composants autorisés fonctionne de la même manière que l’onglet du même nom lors [de la définition de la stratégie et des propriétés d’un conteneur de disposition dans l’éditeur de modèles.](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

### Onglet Styles {#styles-tab}

Le composant Onglets prend en charge le [Système de style](authoring.md#component-styling) AEM.