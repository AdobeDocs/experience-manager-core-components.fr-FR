---
title: Composant accordéon
seo-title: Composant accordéon
description: 'null'
seo-description: Le composant Accordion Composant principal permet la création d'une collection de panneaux organisés dans un accordéon sur une page.
uuid: ec807de9-f76c-4850-9ece-c3e439a1d626
contentOwner: Utilisateur
content-type: référence
topic-tags: création
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: f093f58e-9755-4a4f-803a-ab93a50e6870
translation-type: tm+mt
source-git-commit: bbd54d433cbeee5395dc8b90bc47f9b44747e25b

---


# Accordion Component{#accordion-component}

Le composant Accordion Composant principal permet la création d&#39;une collection de panneaux organisés dans un accordéon sur une page.

## Utilisation {#usage}

The Core Component Accordion component allows for the creation of a collection of components, composed as panels, and arranged in an accordion on a page, similar to the [Tabs Component](tabs.md), but allows for expanding and collapsing of the panels.

* The accordion&#39;s properties can be defined in the [configure dialog](#configure-dialog).
* The order of the panels of the accordion can be defined in the configure dialog as well as the [select panel popover](#select-planel.md).
* Defaults for the Accordion Component when adding it to a page can be defined in the [design dialog](#design-dialog).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Accordéon est v 1, qui a été introduite avec la version 2.5.0 des composants principaux en juin 2019 et est décrite dans ce document.

Le tableau suivant détaille toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Composant Version | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

Pour plus d’informations sur les versions et les mises à jour des composants principaux, consultez le document sur les [versions des composants principaux](versions.md).

## Exemple de sortie de composant {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/accordion.html).

## Détails techniques {#technical-details}

The latest technical documentation about the Accordion Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/accordion/v1/accordion).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](developing.md).

## Boîte de dialogue Configurer {#configure-dialog}

La boîte de dialogue Configurer permet à l&#39;auteur de contenu de définir l&#39;élément d&#39;accordéon, ses panneaux et son comportement et s&#39;affichant pour un visiteur sur la page.

### Onglet Éléments {#items-tab}

![](assets/screen-shot-2019-06-21-08.26.38.png)

Use the **Add** button to open the component selector to choose which component to add as a panel. Une fois ajouté, une entrée est ajoutée à la liste qui contient les colonnes suivantes :

* **Icône** - Icône du type de composant du panneau pour une identification facile dans la liste. Placez le pointeur de la souris sur pour afficher le nom complet du composant sous forme d’info-bulle.
* **Description** : description utilisée comme texte du panneau, par défaut au nom du composant sélectionné pour le panneau.
* **Supprimer** : appuyez ou cliquez sur pour supprimer le panneau du composant accordéon.
* **Réorganiser** : appuyez sur ou cliquez et faites glisser pour réorganiser l&#39;ordre des panneaux.

### Onglet Propriétés {#properties-tab}

![](assets/screen-shot-2019-06-21-08.26.53.png)

* **Extension d&#39;élément unique** : lorsqu&#39;elle est sélectionnée, cette option force le développement d&#39;un seul élément d&#39;accordéon à la fois. La développement d&#39;un élément réduit alors tous les autres.
* **Éléments développés** : cette option définit les éléments qui sont développés par défaut lorsque la page est chargée.
   * When **Single item expansion** is selected, one panel must be selected. Par défaut, le premier panneau est sélectionné.
   * When **Single item expansion** is not selected, this option is a multi-select and is optional.

## Select Panel Popover {#seelct-panel-popover}

The content author can use the **Select Panel** option on the component toolbar to change to a different panel for editing as well as to easily rearrange the order of the panels within the accordion.

![](assets/screen-shot-2019-06-21-08.49.36.png)

Once selecting the **Select Panel** option in the component toolbar, the configured accordion panels are displayed as a drop-down.

![](assets/screen-shot-2019-06-21-08.52.14.png)

* La liste est triée selon la disposition des panneaux assignée et se reflète dans la numérotation.
* Le type de composant du panneau s&#39;affiche en premier, suivi de la description du panneau dans la police plus claire.
* Lorsque vous appuyez ou cliquez sur une entrée dans la liste déroulante, la vue de l&#39;éditeur est commutée dans ce panneau.
* Les panneaux peuvent être réorganisés en place à l&#39;aide des poignées de glissement.

## Boîte de dialogue Conception {#design-dialog}

Le dialogue de conception permet à l&#39;auteur du modèle de définir les options disponibles pour l&#39;auteur du contenu qui utilise le composant Accordéon et les valeurs par défaut définies lors de l&#39;importation du composant Accordéon.

### Onglet Propriétés {#properties-tab-design}

![](assets/screen-shot-2019-06-21-08.58.11.png)

* **Eléments d&#39;en-tête autorisés** : cette liste déroulante à sélection multiple définit les éléments d&#39;en-tête de l&#39;élément d&#39;accordéon qui sont autorisés à être sélectionnés par un auteur.
* **Elément d&#39;en-tête par défaut** : cette liste déroulante définit l&#39;en-tête d&#39;en-tête de l&#39;élément d&#39;accordéon par défaut HTML.

### Onglet Composants autorisés {#allowed-components-tab}

The **Allowed Components** tab is used to define which components can be added as items to panels in the Accordion Component by the content author.

L’onglet Composants autorisés fonctionne de la même manière que l’onglet du même nom lors [de la définition de la stratégie et des propriétés d’un conteneur de dispositions dans l’éditeur de modèles.](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

### Onglet Styles {#styles-tab}

The Accordion Component supports the AEM [Style System](authoring.md#component-styling).
