---
title: Composant de conteneur de formulaires
description: Le composant de conteneur de formulaires des composants principaux permet la création de formulaires d’envoi simples.
translation-type: tm+mt
source-git-commit: 95c0621f5423bfa515fe5e8b693e127ea56b4ae0

---


# Composant de conteneur de formulaires {#form-container-component}

Le composant de conteneur de formulaires des composants principaux permet la création de formulaires d’envoi simples.

## Utilisation {#usage}

Le composant de conteneur de formulaires a permis la création de formulaires et de fonctionnalités d’envoi d’informations simples en prenant en charge les formulaires WCM simples et en utilisant une structure imbriquée pour autoriser des composants de formulaire supplémentaires.

En utilisant la [boîte de dialogue de configuration](#configure-dialog), l’éditeur de contenu peut définir l’action déclenchée par l’envoi du formulaire, l’emplacement de stockage du contenu envoyé et si un workflow doit être déclenché. L’auteur du modèle peut utiliser la [boîte de dialogue de conception](#design-dialog) pour définir les composants autorisés et leurs mappages similaires à la boîte de dialogue de conception du [conteneur de mises en page standard dans l’éditeur de modèles](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!NOTE]
>
>Le composant de conteneur de formulaires des composants principaux prend uniquement en charge l’utilisation d’autres composants de formulaire (bouton, texte, masqué, etc.). L’utilisation des composants de formulaire des [composants de base](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) dans le conteneur de formulaires (et vice versa) n’est pas prise en charge.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de conteneur de formulaires est v2, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Compatible | Compatible | Compatible | Compatible |
| [v1](/help/components/v1/form-container-v1.md) | Compatible | Compatible | Compatible | - |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

To experience the Form Container Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_form_container).

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant de conteneur de formulaires [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_form_container_v2).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de définir les actions effectuées lors de l’envoi du composant.

![](/help/assets/screen_shot_2018-01-12at122046.png)

Selon le **type d’action** sélectionné, les options disponibles dans le conteneur changent. Les types d’actions disponibles sont les suivants :

* [Courrier](#mail)
* [Stocker le contenu](#store-content)
* [Envoyer la commande](#submit-order)
* [Mettre à jour la commande](#update-order)

Quel que soit le type, il existe des [paramètres généraux](#general-settings) qui s’appliquent à chaque action.

### Courrier {#mail}

Lorsque le formulaire est envoyé, le type d’action courrier envoie un e-mail aux destinataires désignés.

![](/help/assets/screen_shot_2018-01-12at122554.png)

* **Objet**
Objet de l’e-mail qui sera envoyé lors de l’envoi du formulaire.
* **De**
Adresse e-mail de l’expéditeur de l’e-mail qui sera envoyé lors de l’envoi du formulaire.
* **À**
Adresses des destinataires qui recevront un e-mail lors de l’envoi du formulaire.

   * Appuyez ou cliquez sur le bouton **Ajouter** pour ajouter d’autres adresses.
   * Appuyez ou cliquez sur le bouton **Supprimer** pour supprimer une adresse e-mail.
* **Cc**
Les adresses des destinataires qui recevront une copie carbone de l’e-mail envoyé lors de l’envoi du formulaire.
   * Appuyez ou cliquez sur le bouton **Ajouter** pour ajouter d’autres adresses.
   * Appuyez ou cliquez sur le bouton **Supprimer** pour supprimer une adresse e-mail.

### Stocker le contenu {#store-content}

Lorsque le formulaire est envoyé, le contenu du formulaire est stocké dans un emplacement de référentiel désigné.

![](/help/assets/screen_shot_2018-01-12at122538.png)

* **Chemin d’accès au contenu**
Chemin d’accès au référentiel de contenu où le contenu envoyé est stocké.
* **Afficher les données**
Appuyez ou cliquez sur cette option pour afficher les données envoyées stockées sous la forme JSON.
* **Démarrer le processus**
Configurez cette option pour démarrer un workflow avec le contenu stocké comme charge utile lors de l’envoi du formulaire.

### Envoyer la commande {#submit-order}

Lorsque le formulaire est envoyé, la commande est envoyée.

![](/help/assets/chlimage_1-3.png)

### Mettre à jour la commande {#update-order}

Lorsque le formulaire est envoyé, la commande est mise à jour.

![](/help/assets/chlimage_1-4.png)

### Paramètres généraux {#general-settings}

Quelle que soit le type d’action sélectionné, une page de remerciement peut toujours être définie.

![](/help/assets/chlimage_1-5.png)

L’utilisateur est redirigé vers la page spécifiée une fois l’envoi du formulaire terminé.

* Utilisez la boîte de dialogue de sélection pour sélectionner une ressource dans AEM.
* Si la page de remerciement ne figure pas dans AEM, indiquez l’URL absolue. Les URL non absolues seront interprétées par rapport à AEM.
* Laissez vide pour réafficher le formulaire après envoi.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les composants autorisés et leurs mappages pour le conteneur similaires à la boîte de dialogue de conception du [conteneur de mises en page standard dans l’éditeur de modèles](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).