---
title: Embed Component
seo-title: Embed Component
description: The Embed Component enables embedding external content in an AEM content page.
seo-description: The Embed Component enables embedding external content in an AEM content page.
content-type: référence
topic-tags: core-components
translation-type: tm+mt
source-git-commit: d748bf211ec36d12cac016ca9bf707f24db1ce48

---


# Incorporer le composant{#embed-component}

The Core Components Embed Component allows embedding external content in an AEM content page.

## Utilisation {#usage}

Le composant Incorporer du composant principal permet à l’auteur du contenu de définir le contenu externe sélectionné à incorporer dans une page de contenu AEM. En outre, il existe une option permettant de définir du code HTML de forme libre à incorporer.

* The component's properties can be defined in the [configure dialog](#configure-dialog).
* Les valeurs par défaut du composant lors de son ajout à une page peuvent être définies dans la [boîte de dialogue de conception](#design-dialog).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant incorporé est v1, qui a été introduite avec la version 2.7.0 des composants principaux en septembre 2019. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](versions.md).

## Exemple de sortie de composant {#sample-component-output}

To experience the Embed Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/embed.html).

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Incorporer [se trouve sur GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](developing.md).

## Boîte de dialogue de configuration {#configure-dialog}

The configure dialog allows the content author to define the external resource to be embedded on the page. Choisissez d’abord le type de ressource à incorporer : **URL**, **Intégrable** ou **HTML**.

### URL {#url}

L’intégration la plus simple est l’URL. Il vous suffit de coller l’URL de la ressource à incorporer dans le champ **URL** . Le composant tente d’accéder à la ressource et, s’il peut être rendu par l’un des processeurs, affiche un message de confirmation sous le champ **URL** . If not, the field will be marked in error.

Le composant Incorporer est livré avec des processeurs pour les types de ressources suivants :

* Ressources conformes à la norme [oEmbed](https://oembed.com/) , notamment Facebook Post, Instagram, SoundCloud, Twitter et YouTube
* Pinterest

Les développeurs peuvent ajouter d’autres processeurs d’URL en [suivant la documentation du développeur du composant incorporé.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![](assets/screen-shot-2019-09-25-10.08.29.png)

### Élément intégrable {#embeddable}

Les intégrables permettent une personnalisation plus poussée de la ressource incorporée, qui peut être paramétrée et inclure des informations supplémentaires. An author is able to select from pre-configured trusted embeddables and the component ships with a Youtube embeddable out-of-the-box.

The Embeddable field defines the type of processor you want to use. **** Dans le cas de l’intégrable YouTube, vous pouvez ensuite définir :

* **ID** vidéo : identifiant vidéo unique de YouTube de la ressource à incorporer.
* **Width - The width of the embedded video**
* **Hauteur** - Hauteur de la vidéo intégrée

Other embeddables would offer similar fields and can be defined by a developer by following the developer documentation of the Embed Component.[](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![](assets/screen-shot-2019-09-25-10.15.00.png)

>[!NOTE]
>Embeddables must be enabled at the template level via the Design Dialog to be available to the page author.[](#design-dialog)

### HTML {#html}

Vous pouvez ajouter du code HTML de forme libre à votre page à l’aide du composant Incorporer.

![](assets/screen-shot-2019-09-25-10.20.00.png)

>[!NOTE]
>Any unsafe tags such as scripts will be filtered from the entered HTML and will not be rendered on the resulting page.

## Boîte de dialogue de conception {#design-dialog}

The design dialog allows the template author to define the options available to the content author who uses the Embed Component and the defaults set when placing the Embed Component.

![](assets/screen-shot-2019-09-25-10.25.28.png)

* **Disable URL - Disables the URL option for the content author when selected******
* **Désactiver les intégrables** - Désactive l'option **Intégrable** pour l'auteur du contenu lorsqu'elle est sélectionnée, quels que soient les processeurs intégrables autorisés.
* **Désactiver HTML** : désactive l’option **HTML** pour l’auteur du contenu lorsqu’elle est sélectionnée.
* **Embeddables** autorisés - Multislect qui définit les processeurs incorporables accessibles à l’auteur du contenu, à condition que l’option **Embeddable** soit active.
