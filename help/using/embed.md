---
title: Embed Component
seo-title: Incorporer le composant
description: Le composant Incorporer permet d’incorporer du contenu externe dans une page de contenu AEM.
seo-description: Le composant Incorporer permet d’incorporer du contenu externe dans une page de contenu AEM.
content-type: référence
topic-tags: core-components
translation-type: tm+mt
source-git-commit: 6882a0d8247328c403dc11a25ed9d079aefede69

---


# Incorporer le composant{#embed-component}

Le composant Incorporer les composants principaux permet d’incorporer du contenu externe dans une page de contenu AEM.

## Utilisation {#usage}

Le composant Incorporer du composant principal permet à l’auteur du contenu de définir le contenu externe sélectionné à incorporer dans une page de contenu AEM. En outre, il existe une option permettant de définir du code HTML de forme libre à incorporer.

* Les propriétés du composant peuvent être définies dans la [boîte de dialogue de configuration](#configure-dialog).
* Les valeurs par défaut du composant lors de son ajout à une page peuvent être définies dans la [boîte de dialogue de conception](#design-dialog).

## Version et compatibilité {#version-and-compatibility}

The current version of the Embed Component is v1, which was introduced with release 2.7.0 of the Core Components in September 2019, and is described in this document.

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

La boîte de dialogue de configuration permet à l’auteur du contenu de définir la ressource externe à incorporer dans la page. Choisissez d’abord le type de ressource à incorporer : **URL**, **Intégrable** ou **HTML**.

### URL {#url}

L’intégration la plus simple est l’URL. Il vous suffit de coller l’URL de la ressource à incorporer dans le champ **URL** . Le composant tente d’accéder à la ressource et, s’il peut être rendu par l’un des processeurs, affiche un message de confirmation sous le champ **URL** . Si ce n’est pas le cas, le champ est marqué par erreur.

Le composant Incorporer est livré avec des processeurs pour les types de ressources suivants :

* Ressources conformes à la norme [oEmbed](https://oembed.com/) , notamment Facebook Post, Instagram, SoundCloud, Twitter et YouTube
* Pinterest

Les développeurs peuvent ajouter d’autres processeurs d’URL en [suivant la documentation du développeur du composant incorporé.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![](assets/screen-shot-2019-09-25-10.08.29.png)

### Incorporable {#embeddable}

Les intégrables permettent une personnalisation plus poussée de la ressource incorporée, qui peut être paramétrée et inclure des informations supplémentaires. Un auteur peut sélectionner des éléments incorporables approuvés préconfigurés et le composant est livré avec un processeur YouTube prêt à l’emploi.

Le champ **Embeddable** définit le type de processeur à utiliser. Dans le cas du processeur YouTube, vous pouvez ensuite définir ce qui suit :

* **ID** vidéo : identifiant vidéo unique de YouTube de la ressource à incorporer.
* **Largeur** - Largeur de la vidéo incorporée
* **Hauteur** - Hauteur de la vidéo intégrée

D'autres processeurs proposent des champs similaires et peuvent être définis par un développeur en [suivant la documentation du développeur du composant intégré.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![](assets/screen-shot-2019-09-25-10.15.00.png)

>[!NOTE]
>Embedded processors must be enabled at the template level via the Design Dialog to be avaialble to the page author.[](#design-dialog)

### HTML {#html}

You can add free-form HTML to your page using the Embed Component.

![](assets/screen-shot-2019-09-25-10.20.00.png)

>[!NOTE]
>Any unsafe tags such as scripts will be filtered from the entered HTML and will not be rendered on the resulting page.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les options disponibles pour l’auteur du contenu qui utilise le composant incorporé et les valeurs par défaut définies lors du placement du composant incorporé.

![](assets/screen-shot-2019-09-25-10.25.28.png)

* **Désactiver l’URL** : désactive l’option **URL** de l’auteur du contenu lorsqu’elle est sélectionnée.
* **Désactiver les intégrables** - Désactive l'option **Intégrable** pour l'auteur du contenu lorsqu'elle est sélectionnée, quels que soient les processeurs intégrables autorisés.
* **Disable HTML - Disables the HTML option for the content author when selected.******
* **Allowed Embeddables - Multislect that defines which embeddable processors are avaiable to the content author, provided that the Embeddable option is active.******
