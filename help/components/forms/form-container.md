---
title: Composant de conteneur de formulaires
description: Le composant de conteneur de formulaires des composants principaux permet la création de formulaires d’envoi simples.
role: Architect, Developer, Administrator, Business Practitioner
exl-id: 552f9dd5-6a3a-42d9-9969-e62a1f36e811
translation-type: ht
source-git-commit: 8ff36ca143af9496f988b1ca65475497181def1d
workflow-type: ht
source-wordcount: '956'
ht-degree: 100%

---

# Composant de conteneur de formulaires {#form-container-component}

Le composant de conteneur de formulaires des composants principaux permet la création de formulaires d’envoi simples.

## Utilisation {#usage}

Le composant de conteneur de formulaires a permis la création de formulaires et de fonctionnalités d’envoi d’informations simples en prenant en charge les formulaires WCM simples et en utilisant une structure imbriquée pour autoriser des composants de formulaire supplémentaires.

En utilisant la [boîte de dialogue de configuration](#configure-dialog), l’éditeur de contenu peut définir l’action déclenchée par l’envoi du formulaire, l’URL chargé de cet envoi, et si un workflow doit être déclenché. L’auteur du modèle peut utiliser la [boîte de dialogue de conception](#design-dialog) pour définir les composants autorisés et leurs mappages similaires à la boîte de dialogue de conception du [conteneur de mises en page standard dans l’éditeur de modèles](https://docs.adobe.com/content/help/fr-FR/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!NOTE]
>
>Le composant de conteneur de formulaires des composants principaux prend uniquement en charge l’utilisation d’autres composants de formulaire (bouton, texte, masqué, etc.). L’utilisation des composants de formulaire des [composants de base](https://docs.adobe.com/content/help/fr-FR/experience-manager-65/authoring/siteandpage/default-components-foundation.html) dans le conteneur de formulaires (et vice versa) n’est pas prise en charge.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de conteneur de formulaires est v2, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatible | Compatible | Compatible |
| [v1](/help/components/v1/form-container-v1.md) | Compatible | Compatible | - |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant de conteneur de formulaires et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_form_container_fr).

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant de conteneur de formulaires [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_form_container_v2_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de définir les actions effectuées lors de l’envoi du composant.

Selon le **type d’action** sélectionné, les options disponibles dans le conteneur changent. Les types d’actions disponibles sont les suivants :

* [Publier les données de formulaire (Post Form Data)](#post-data)
* [Courrier](#mail)
* [Stocker le contenu](#store-content)

Quel que soit le type, il existe des [paramètres généraux](#general-settings) qui s’appliquent à chaque action.

### Publier les données de formulaire (Post Form Data) {#post-data}

Lorsque le formulaire est envoyé, le type d’action Publier les données de formulaire transmet les données envoyées à un tiers au format JSON pour qu’elles soient traitées.

![Options Publier les données de formulaire dans la boîte de dialogue de modification du composant Conteneur de formulaire](/help/assets/form-container-edit-post.png)

* **Point de terminaison** : service HTTPS complet qui traitera les données
* **Message d’erreur** : message qui s’affiche si l’envoi échoue

>[!TIP]
>Un administrateur système peut paramétrer d’autres options de délai d’expiration pour gérer le traitement des données de formulaire transférées. [Consultez la documentation technique sur GitHub pour plus d’informations.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/actions/rpc)

### Courrier {#mail}

Lorsque le formulaire est envoyé, le type d’action courrier envoie un e-mail aux destinataires désignés.

![Options de courrier dans la boîte de dialogue de modification du composant Conteneur de formulaire](/help/assets/form-container-edit-mail.png)

* **Objet** : objet de l’e-mail qui sera envoyé lors de l’envoi du formulaire.
* **De** : adresse e-mail de l’expéditeur de l’e-mail qui sera envoyé lors de l’envoi du formulaire.
* **À** : adresse des destinataires qui recevront un e-mail lors de l’envoi du formulaire.
   * Appuyez ou cliquez sur le bouton **Ajouter** pour ajouter d’autres adresses.
   * Appuyez ou cliquez sur le bouton **Supprimer** pour supprimer une adresse e-mail.
* **Cc** : adresses des destinataires qui recevront une copie carbone de l’e-mail envoyé lors de l’envoi du formulaire.
   * Appuyez ou cliquez sur le bouton **Ajouter** pour ajouter d’autres adresses.
   * Appuyez ou cliquez sur le bouton **Supprimer** pour supprimer une adresse e-mail.

### Stocker le contenu {#store-content}

Lorsque le formulaire est envoyé, le contenu du formulaire est stocké dans un emplacement de référentiel désigné.

![Options de stockage du contenu dans la boîte de dialogue de modification du conteneur de formulaire](/help/assets/form-container-edit-store.png)

* **Chemin d’accès au contenu** : chemin d’accès au référentiel de contenu où le contenu envoyé est stocké.
* **Afficher les données** : appuyez ou cliquez sur cette option pour afficher les données envoyées stockées sous la forme JSON.
* **Démarrer le processus** : configurez cette option pour démarrer un workflow avec le contenu stocké comme charge utile lors de l’envoi du formulaire.

>[!NOTE]
>
>Afin de simplifier la gestion des données utilisateur et d’imposer la séparation des préoccupations, il est généralement déconseillé de stocker le contenu créé par l’utilisateur dans le référentiel.
>
>Utilisez plutôt le type d’action [Publier les données de formulaire](#post-data) pour transmettre le contenu utilisateur à un prestataire dédié.

### Paramètres généraux {#general-settings}

Quelle que soit le type d’action sélectionné, une page de remerciement peut toujours être définie.

![Options générales dans la boîte de dialogue de modification du composant Conteneur de formulaire](/help/assets/form-container-edit-general.png)

* **Page de remerciement** : l’utilisateur est redirigé vers la page spécifiée une fois l’envoi du formulaire terminé.
   * Utilisez la boîte de dialogue de sélection pour sélectionner une ressource dans AEM.
   * Si la page de remerciement ne figure pas dans AEM, indiquez l’URL absolue. Les URL non absolues seront interprétées par rapport à AEM.
   * Laissez vide pour réafficher le formulaire après envoi.
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les composants autorisés et leurs mappages pour le conteneur similaires à la boîte de dialogue de conception du [conteneur de mises en page standard dans l’éditeur de modèles](https://docs.adobe.com/content/help/fr-FR/experience-manager-cloud-service/sites/authoring/features/templates.html).

### Onglet Styles {#styles-tab}

Le composant Conteneur de formulaire prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.
