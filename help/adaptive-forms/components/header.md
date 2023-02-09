---
title: Composant principal Adaptive Forms - En-tête
description: Utilisation ou personnalisation du composant principal En-tête de Forms adaptatif .
role: Architect, Developer, Admin, User
source-git-commit: 7f680eac1da61b55f9d90db6c0842421d03ac1dc
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 7%

---


# En-tête {#header-adaptive-forms-core-component}

Un composant d’en-tête d’un formulaire adaptatif est une section située en haut du formulaire et qui comprend généralement le titre, le logo ou le nom du formulaire. L’en-tête peut également inclure d’autres informations, telles qu’une brève description de l’objectif du formulaire, le nom de l’organisation qui a créé le formulaire ou des coordonnées pour obtenir de l’aide sur le formulaire. L’en-tête est utilisé pour donner aux utilisateurs un aperçu du formulaire et fournir un contexte pour les informations qu’ils sont sur le point de remplir. Il est utilisé pour aider les utilisateurs à comprendre l’objectif du formulaire et comment le remplir correctement.

**Exemple**

![](/help/adaptive-forms/assets/header.png)

## Utilisation {#reasons-to-use-header}

* **Marques**: Un en-tête peut être utilisé pour afficher le logo ou le nom de l’organisation qui a créé le formulaire, ce qui contribue à établir la reconnaissance et la crédibilité de la marque.

* **Contexte**: Un en-tête peut fournir une brève description de l’objectif du formulaire, aidant ainsi les utilisateurs à comprendre le contexte dans lequel le formulaire est utilisé.

* **Navigation**: Un en-tête peut inclure des liens ou des boutons qui permettent aux utilisateurs de naviguer vers d’autres parties du site web ou de l’application.

* **Informations**: Un en-tête peut inclure des coordonnées ou des liens vers des ressources d’aide, ce qui facilite l’obtention de l’aide par les utilisateurs qui en ont besoin.

* **Expérience utilisateur**: Un en-tête peut être utilisé pour rendre le formulaire plus convivial en offrant une méthode claire et intuitive d’accès et de remplissage des champs de formulaire.

## Version et compatibilité {#version-and-compatibility}

Le composant principal d’en-tête de Forms adaptatif a été publié en février 2023 dans le cadre des composants principaux 2.0.4. Voici un tableau présentant toutes les versions prises en charge, la compatibilité AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible avec<br>[version 2.0.4](/help/versions.md) et plus tard | Compatible | Compatible |

Pour plus d’informations sur les versions et versions des composants principaux, reportez-vous à la section [Versions des composants principaux](/help/versions.md) document.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Détails techniques {#technical-details}

Découvrez les informations les plus récentes sur le composant principal d’en-tête de Forms adaptatif dans la documentation technique de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageheader/v1/pageheader). Pour plus d’informations sur le développement des composants principaux, consultez la section [Documentation destinée aux développeurs sur les composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser votre expérience d’en-tête pour les visiteurs qui utilisent la boîte de dialogue Configurer . Vous pouvez également définir facilement des options d’en-tête pour une expérience utilisateur fluide.

### Onglet Image {#image-tab}

Cette partie de l’en-tête contient le titre et l’image de l’en-tête.

![Imagetab](/help/adaptive-forms/assets/header_image.png)

* **Ressource image** - Cette option permet de déposer une ressource telle qu’une image par glisser-déposer de la souris. Vous pouvez également télécharger un fichier à partir d’un système de fichiers local à l’aide de la fonction **Parcourir** bouton . Après l’ajout d’une image, trois boutons s’affichent au bas de l’image. Après l’ajout d’une image, trois boutons s’affichent au bas de l’image :
   * **Modifier** - Appuyez ou cliquez sur **Modifier** pour gérer les rendus de la ressource dans l’éditeur de ressources.
   * **Effacer** - Appuyez ou cliquez sur **Effacer** pour désélectionner l’image actuellement sélectionnée.
   * **Pick** - Appuyez ou cliquez sur **Pick**  pour sélectionner une autre image dans le dossier Ressources.

* **Titre** - Cette option est utilisée pour ajouter le titre à l’en-tête. Le texte prédéfini est inclus dans la boîte de dialogue et peut être modifié par l’utilisateur.
* **Lier à** - Vous pouvez lier l’en-tête au dossier à l’aide du **Parcourir** icône .
* **Description** - Une description est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’une image spécifique.
* **Taille (px)** - Cela permet d’ajuster la longueur et la largeur de l’image en augmentant ou en réduisant les pixels.

![accessible, onglet](/help/adaptive-forms/assets/header_accessibility.png)

* **Texte de remplacement** - Cette option est utilisée pour saisir le texte qui fournit un texte de remplacement court et descriptif pour l’image, qui décrit l’image aux utilisateurs malvoyants.

* **L’image est décorative** : vérifiez si l’image doit être ignorée par les dispositifs d’assistance et ne requiert donc pas de texte de remplacement. Cela s’applique uniquement aux images décoratives.

### Onglet Texte {#text-tab}

Cette section permet de saisir le texte à inclure dans l’en-tête.

## Boîte de dialogue de conception {#design-dialog}


