---
title: Composant Conteneur de formulaires
seo-title: Composant Conteneur de formulaires
description: 'null'
seo-description: Le composant Conteneur de formulaires de composants principaux permet la création de formulaires d'envoi simples.
uuid: 9 d 556 daf -3 fe 7-4 b 2 a-b 5 ae -6926 acb 267 a 9
contentOwner: Utilisateur
content-type: référence
topic-tags: création
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 3 d 33 fe 60-a 0 ac -4 ff 2-a 865-d 600 b 5448 aeb
disttype: dist5
gnavtheme: light
groupsectionnavitems: non
hidemerchandisingbar: inherit
hidepromocomponent: inherit
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 62643e5bd49ab006230f65004bb9374822dcc017

---


# Composant Conteneur de formulaires{#form-container-component}

Le composant Conteneur de formulaires de composants principaux permet la création de formulaires d&#39;envoi simples.

## Utilisation {#usage}

Le composant Conteneur de formulaires permet la création de formulaires et de fonctionnalités d&#39;envoi d&#39;informations simples en prenant en charge les formulaires WCM simples et en utilisant une structure imbriquée pour autoriser des composants de formulaire supplémentaires.

[En configurant la boîte de dialogue](#configure-dialog) de configuration, l&#39;éditeur de contenu peut définir l&#39;action déclenchée par l&#39;envoi du formulaire, l&#39;emplacement du contenu envoyé et le déclenchement d&#39;un flux de travail. L&#39;auteur du modèle peut utiliser le dialogue [de conception](#design-dialog) pour définir les composants autorisés et leurs mappages similaires à la boîte de dialogue de conception pour le conteneur de dispositions [standard dans l&#39;éditeur de modèles](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html).

>[!NOTE]
>
>Le composant de conteneur de formulaires principaux ne prend en charge que l&#39;utilisation des composants de formulaire de composants principaux (bouton, texte, masqué, etc.). L&#39;utilisation [des composants](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-foundation.html) de formulaire de base dans le conteneur de formulaires principaux des composants (et vice versa) n&#39;est pas prise en charge.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Conteneur de formulaires est v 2, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018 et est décrite dans ce document.

Le tableau suivant détaille toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatible | Compatible | Compatible |
| [v1](form-container-v1.md) | Compatible | Compatible | Compatible |

Pour plus d&#39;informations sur les versions et les versions des composants principaux, consultez les versions des composants de Document [principaux](versions.md).

## Détails techniques {#technical-details}

Vous trouverez la documentation technique la plus récente sur le composant [de conteneur de formulaires sur github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v2/container).

Vous trouverez plus d&#39;informations sur le développement des composants principaux dans la documentation destinée aux développeurs de composants [principaux](developing.md).

## Configurer le dialogue {#configure-dialog}

La configuration de la boîte de dialogue Configurer permet à l&#39;auteur de contenu de définir les actions effectuées lors de l&#39;envoi du composant.

![](assets/screen_shot_2018-01-12at122046.png)

Selon le type **d&#39;action sélectionné**, les options disponibles dans le conteneur changent. Les types d&#39;action disponibles sont les suivants :

* [Courrier](#mail)
* [Stocker le contenu](#store-content)
* [Envoyer la commande](#submit-order)
* [Mettre à jour la commande](#update-order)

Quel que soit le type, il existe des paramètres [généraux](#general-settings) qui s&#39;appliquent à chaque action.

### Courrier {#mail}

Lorsque le formulaire est envoyé, le type d&#39;action Courrier électronique envoie un courrier électronique aux destinataires désignés.

![](assets/screen_shot_2018-01-12at122554.png)

* **Objet**
Sujet du courrier électronique qui sera envoyé lors de l&#39;envoi du formulaire
* **A partir**
de l&#39;adresse électronique de l&#39;expéditeur du courrier électronique qui sera envoyé lors de l&#39;envoi du formulaire
* **Aux**
adresses des destinataires qui recevront un courrier électronique lors de l&#39;envoi du formulaire

   * Appuyez sur le bouton **Ajouter** ou cliquez dessus pour ajouter d&#39;autres adresses.
   * Appuyez sur le bouton **Supprimer** ou cliquez dessus pour supprimer une adresse électronique.
* **CC**
Les adresses des destinataires qui recevront une copie carbone du courrier électronique envoyé lors de l&#39;envoi du formulaire
   * Appuyez sur le bouton **Ajouter** ou cliquez dessus pour ajouter d&#39;autres adresses.
   * Appuyez sur le bouton **Supprimer** ou cliquez dessus pour supprimer une adresse électronique.

### Stocker le contenu {#store-content}

Lorsque le formulaire est envoyé, le contenu du formulaire est stocké dans un emplacement référentiel désigné.

![](assets/screen_shot_2018-01-12at122538.png)

* **Chemin du référentiel Content Path**
Content dans lequel le contenu envoyé est stocké
* **Afficher**l&#39;appui des données
ou cliquer pour afficher les données envoyées stockées sous la forme JSON
* **Démarrer**la configuration de processus
pour démarrer un flux de travail avec le contenu stocké comme charge utile lors de l&#39;envoi du formulaire

### Envoyer la commande {#submit-order}

Lorsque le formulaire est envoyé, la commande est envoyée.

![](assets/chlimage_1-3.png)

### Mettre à jour la commande {#update-order}

Lorsque le formulaire est envoyé, la commande est mise à jour.

![](assets/chlimage_1-4.png)

### Paramètres généraux {#general-settings}

Quelle que soit le type d&#39;action sélectionné, une page de remerciement peut toujours être définie.

![](assets/chlimage_1-5.png)

L&#39;utilisateur est redirigé vers la page spécifiée une fois l&#39;envoi du formulaire terminé.

* Utilisez le dialogue de sélection pour sélectionner une ressource dans AEM.
* Si la page de remerciement ne figure pas dans AEM, indiquez l&#39;URL absolue. Les URL non absolues seront interprétées par rapport à AEM.
* Laissez vide pour réafficher le formulaire après envoi.

## Créer un dialogue {#design-dialog}

Le dialogue de conception permet à l&#39;auteur du modèle de définir les composants autorisés et leurs correspondances pour le conteneur du même type que la boîte de dialogue de conception du conteneur de dispositions [standard dans l&#39;éditeur de modèles](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html).