---
title: Composant Conteneur de formulaires (v 1)
seo-title: Composant Conteneur de formulaires (v 1)
description: Le composant Conteneur de formulaires de composants principaux permet la création de formulaires d'envoi simples.
seo-description: Le composant Conteneur de formulaires de composants principaux permet la création de formulaires d'envoi simples.
uuid: 075 d 83 ed-de 40-414 e-a 18 f -46 b 3 a 857 acba
content-type: référence
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: Ad 800 c 064 e -2 ad 5-41 f 3-9 cef-b 025 a 555 efd 9
index: n
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Composant Conteneur de formulaires (v 1){#form-container-component-v}

Le composant Conteneur de formulaires de composants principaux permet la création de formulaires d&#39;envoi simples.

## Utilisation {#usage}

Le composant Conteneur de formulaires a permis la création de formulaires et de fonctionnalités d&#39;envoi d&#39;informations simples en prenant en charge les formulaires WCM simples et en utilisant une structure imbriquée pour permettre des composants de formulaire supplémentaires.

En utilisant le [paramètre](form-container-v1.md#main-pars_title) de dialogue défini, l&#39;éditeur de contenu peut définir le type d&#39;envoi d&#39;envoi de formulaire d&#39;action, l&#39;emplacement du contenu envoyé et le déclenchement d&#39;un flux de travail. L&#39;auteur du modèle peut utiliser le dialogue [de conception](form-container-v1.md#main-pars_title_1995166862) pour définir les composants et leurs mappages similaires à la boîte de dialogue de conception du conteneur de dispositions [standard dans l&#39;éditeur de modèles](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html#main-pars_title_1754153843).

## Version et compatibilité {#version-and-compatibility}

Ce document décrit la version v 1 du composant Conteneur de formulaires, introduite à l&#39;origine avec la version 1.0.0 des composants principaux avec AEM 6.3.

Le tableau suivant répertorie la compatibilité de la version v 1 du composant Conteneur de formulaires.

| Version d’AEM | Composant de conteneur de formulaires v 1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Ce document décrit la version v 1 du composant Conteneur de formulaires.
>
>Pour plus d&#39;informations sur la version actuelle du composant Conteneur de formulaires, voir [le document Composant](form-container.md) du conteneur de formulaires.

## Dialogue Paramètres {#settings-dialog}

Le dialogue des paramètres permet à l&#39;auteur de contenu de définir les actions effectuées lors de l&#39;envoi du composant.

![](assets/chlimage_1.png)

Selon le type **d&#39;action sélectionné**, les options disponibles dans le conteneur changent. Les types d&#39;action disponibles sont les suivants :

* [Courrier](form-container-v1.md#main-pars_title_966511656)
* [Stocker le contenu](form-container-v1.md#main-pars_title_2065985840)
* [Envoyer la commande](form-container-v1.md#main-pars_title_686874527)
* [Mettre à jour la commande](form-container-v1.md#main-pars_title_410109286)

Quel que soit le type, il existe des paramètres [généraux](form-container-v1.md#main-pars_title_375403046) qui s&#39;appliquent à chaque action.

### Courrier {#mail}

Lorsque le formulaire est envoyé, le type d&#39;action Courrier électronique envoie un courrier électronique aux destinataires désignés.

![](assets/chlimage_1-1.png)

* **Objet** - Objet du courrier électronique qui sera envoyé lors de l&#39;envoi du formulaire
* **From** - The from email address of the email that will be send on form envoi
* **To** - Adresse des destinataires qui recevront un courrier électronique lors de l&#39;envoi du formulaire
   * Appuyez sur le bouton **Ajouter** ou cliquez dessus pour ajouter d&#39;autres adresses.
   * Appuyez sur le bouton **Supprimer** ou cliquez dessus pour supprimer une adresse électronique.
* **CC** - Les adresses des destinataires qui recevront une copie carbone du courrier électronique envoyé lors de l&#39;envoi du formulaire
   * Appuyez sur le bouton **Ajouter** ou cliquez dessus pour ajouter d&#39;autres adresses.
   * Appuyez sur le bouton **Supprimer** ou cliquez dessus pour supprimer une adresse électronique.

### Stocker le contenu {#store-content}

Lorsque le formulaire est envoyé, le contenu du formulaire est stocké dans un emplacement référentiel désigné.

![](assets/chlimage_1-2.png)

* **Chemin de contenu** - Chemin du référentiel de contenu où le contenu envoyé est stocké
* **Afficher les données** - Appuyez ou cliquez pour afficher les données envoyées stockées sous la forme JSON
* **Démarrer le processus** : configurer pour démarrer un flux de travail avec le contenu stocké comme charge utile lors de l&#39;envoi du formulaire

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

Le dialogue de conception permet à l&#39;auteur du modèle de définir les composants autorisés et leurs correspondances pour le conteneur du même type que la boîte de dialogue de conception du conteneur de dispositions [standard dans l&#39;éditeur de modèles](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html#main-pars_title_1754153843).

## Détails techniques {#technical-details}

Vous trouverez la documentation technique la plus récente sur le composant [de conteneur de formulaires sur github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v1/container).

Le projet de composants principaux peut être téléchargé depuis github.

Vous trouverez plus d&#39;informations sur le développement des composants principaux dans la documentation destinée aux développeurs de composants [principaux](developing.md).
