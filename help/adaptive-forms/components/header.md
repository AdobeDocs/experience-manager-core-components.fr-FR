---
title: Composant principal des formulaires adaptatifs - En-tête
description: Utilisation ou personnalisation du composant principal « En-tête » des formulaires adaptatifs.
role: Architect, Developer, Admin, User
exl-id: aa18def9-0bec-4475-8dde-213860621ef5
source-git-commit: 93acf5f6f11da42a7834bbb11b15a36db1e03dc9
workflow-type: ht
source-wordcount: '679'
ht-degree: 100%

---

# En-tête {#header-adaptive-forms-core-component}

Le composant « En-tête » d’un formulaire adaptatif est une section située en haut du formulaire et qui comprend généralement le titre, le logo ou le nom du formulaire. L’en-tête peut également inclure d’autres informations, telles qu’une brève description de l’objectif du formulaire, le nom de l’organisation qui a créé le formulaire ou des coordonnées pour obtenir de l’aide sur le formulaire. L’en-tête est utilisé pour donner aux utilisateurs et aux utilisatrices un aperçu du formulaire et fournir un contexte pour les informations qu’ils ou elles sont sur le point de remplir. Il est utilisé pour aider les utilisateurs et les utilisatrices à comprendre l’objectif du formulaire et comment le remplir correctement.

**Exemple**

![](/help/adaptive-forms/assets/header.png)

## Utilisation {#reasons-to-use-header}

- **Image de marque** : un en-tête peut être utilisé pour afficher le logo ou le nom de l’organisation qui a créé le formulaire, ce qui contribue à établir la reconnaissance et la crédibilité de la marque.

- **Contexte** : un en-tête peut fournir une brève description de l’objectif du formulaire, aidant ainsi les utilisateurs et les utilisatrices à comprendre le contexte dans lequel le formulaire est utilisé.

- **Navigation** : un en-tête peut inclure des liens ou des boutons qui permettent aux utilisateurs et aux utilisatrices de naviguer vers d’autres parties du site Web ou de l’application.

- **Informations** : un en-tête peut inclure des coordonnées ou des liens vers des ressources d’aide pour les utilisateurs et les utilisatrices qui en ont besoin.

- **Expérience utilisateur** : un en-tête peut être utilisé pour rendre le formulaire plus convivial en offrant une méthode claire et intuitive d’accès et de remplissage des champs de formulaire.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Accordéon des formulaires adaptatifs a été publié en février 2023 au sein des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec la <br>[version 2.0.4](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible avec les<br>[versions 1.1.12](/help/adaptive-forms/version.md) à 2.0.0 exclue. |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Détails techniques {#technical-details}

Retrouvez les informations les plus récentes sur le composant principal « En-tête » des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageheader/v1/pageheader). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience d’en-tête pour les visiteurs et les visiteuses en utilisant la boîte de dialogue Configurer. Vous pouvez également définir facilement des options d’en-tête pour une expérience utilisateur fluide.

### Onglet Image {#image-tab}

Cette partie de l’en-tête contient le titre et l’image de l’en-tête.

![Onglet Image](/help/adaptive-forms/assets/header_image.png)

- **Ressources Image** - Cette option permet de déposer une ressource telle qu’une image par glisser-déposer. Vous pouvez également télécharger un fichier à partir d’un système de fichiers local à l’aide du bouton **Parcourir**. Après avoir ajouté une image, trois boutons s’affichent au bas de l’image. Après avoir ajouté une image, trois boutons s’affichent au bas de l’image :
   - **Modifier** - Appuyez ou cliquez sur **Modifier** pour gérer les rendus de la ressource dans l’éditeur de ressources.
   - **Effacer** - Appuyez ou cliquez sur **Effacer** pour désélectionner l’image actuellement sélectionnée.
   - **Sélection** - Appuyez ou cliquez sur **Sélection** pour sélectionner une autre image dans le dossier Ressources.

- **Titre** - Cette option est utilisée pour ajouter le titre à l’en-tête. Le texte prédéfini est inclus dans la boîte de dialogue et peut être modifié par l’utilisateur ou l’utilisatrice.
- **Lier à** - Vous pouvez lier l’en-tête au dossier à l’aide de l’icône **Parcourir**.
- **Description** - Une description est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’une image spécifique.
- **Taille (px)** - Cela permet d’ajuster la longueur et la largeur de l’image en augmentant ou en réduisant les pixels.

![Onglet Accessibilité](/help/adaptive-forms/assets/header_accessibility.png)

- **Texte secondaire** - Cette option est utilisée pour saisir un texte de remplacement court et descriptif pour décire l’image aux personnes malvoyantes.

- **L’image est décorative** : vérifiez si l’image doit être ignorée par les dispositifs d’assistance et ne requiert donc pas de texte de remplacement. Cela s’applique uniquement aux images décoratives.

### Onglet Texte {#text-tab}

Cette section permet de saisir le texte à inclure dans l’en-tête.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Articles connexes {#related-articles}

{{more-like-this}}

## Voir également {#see-also}

{{see-also}}
