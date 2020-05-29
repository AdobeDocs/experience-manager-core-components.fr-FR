---
title: Utilisation de la couche de données client Adobe pour intégrer les composants principaux et lancer Adobe
description: Configuration du lancement Adobe pour enregistrer les événements de composants principaux à l’aide du lancement Adobe
translation-type: tm+mt
source-git-commit: f930a0d6004a29369b189137dd9c52e637ea3a61
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 2%

---


# Utilisation de la couche de données client Adobe pour intégrer les composants principaux et lancer Adobe {#launch-integration}

Les composants principaux peuvent être intégrés à Adobe Launch à l’aide de la couche de données du client Adobe. Ce document décrit comment configurer Adobe Launch pour effectuer le suivi des événements de clics pour les composants d’image.

Lorsqu’il est configuré, Launch génère la sortie suivante dans la console du navigateur lorsqu’un utilisateur clique sur un composant Image principale.

![Exemple de sortie de console](/help/assets/launch-console-output.png)

## Lancement de l’intégration avec AEM {#launch-aem}

Le premier lancement Adobe doit être intégré à votre site AEM.

### Étape 1 - Création d&#39;une intégration dans les E/S Adobe {#create-io-integration}

Connectez-vous d&#39;abord à Adobe E/S pour début de configuration d&#39;une intégration.

1. Accédez à `https://console.adobe.io`.
1. Connectez-vous à l’aide de votre identifiant Adobe ID.
1. Dans la section Début rapide, cliquez sur **Créer une intégration**.
1. Select **Access an API** and click **Continue**.
1. Sélectionnez **Experience Platform Launch API** sous Adobe Experience Platform et cliquez sur **Continuer**.

### Etape 2 - Création d’une configuration IMS dans AEM {#ims-configuration}

Dans AEM, vous devez définir l’intégration que vous avez commencée à configurer dans les E/S Adobe.

1. Accédez à la page d&#39;accueil AEM, cliquez sur **Outils -> Sécurité -> Adobe IMS Configurations**.
1. Cliquez sur **Créer**.
1. En tant que solution **** Cloud, sélectionnez Lancement **** Adobe.
1. Cochez la case **Créer un nouveau certificat**.
1. Saisissez un alias pour le certificat, par exemple **aem-launch-certificate**.
1. Cliquez sur **Créer un certificat** et dans la fenêtre contextuelle, cliquez sur **OK** pour créer le certificat.
1. Cliquez sur **Télécharger la clé** publique et dans la fenêtre contextuelle, cliquez sur **Télécharger**.

### Étape 3 - Terminer la configuration des E/S Adobe {#finish-io}

Avec le certificat et la clé créés dans la configuration IMS d’AEM, vous pouvez terminer votre configuration d’E/S Adobe.

1. Revenez à la console d&#39;E/S Adobe comme à l&#39; [étape 1.](#create-io-integration)
1. Dans la fenêtre **Créer une nouvelle intégration** , saisissez un nom et une description tels que la couche **de données de lancement d’** AEM.
1. Sous Certificats **de clés** publiques, téléchargez le certificat que vous avez créé à l’ [étape 2.](#ims-configuration)
1. Sélectionnez **Lancement - profil** de produit.
1. Cliquez sur **Créer une intégration**.
1. Cliquez sur **Continuer pour accéder aux détails** de l’intégration. Vous aurez besoin de ces informations ultérieurement pour terminer la configuration IMS dans votre instance AEM.

### Étape 4 - Fin de la configuration IMS {#finish-ims}

Avec les détails de l’intégration des E/S Adobe, vous pouvez terminer la configuration d’AEM IMS.

1. Dans l’onglet AEM, dans l’onglet Configuration **du compte technique** Adobe IMS de l’ [étape 2,](#ims-configuration) cliquez sur **Suivant**.
1. Saisissez un titre tel que la configuration **IMS pour le lancement** Adobe.
1. Dans l&#39;onglet E/S Adobe, copiez la clé d&#39; **API (ID client)**.
1. Dans l’onglet AEM, collez l’ancienne clé copiée dans le champ **Clé d’** API.
1. Dans E/S Adobe, cliquez sur **Récupérer la clé secrète** client et copiez-la.
1. Dans l’onglet AEM, collez-le dans le champ Secret **** client.
1. Dans l’onglet E/S Adobe, sélectionnez l’onglet **JWT** et copiez l’URL telle que `https://ims-na1.adobelogin.com`.
1. Dans l’onglet AEM, collez l’URL dans le champ Serveur **d’** autorisation.
1. Dans l’onglet E/S Adobe, copiez la charge utile JWT (le code entre les accolades).
1. Dans l’onglet AEM, collez-le dans le champ **Charge** .
1. Cliquez sur **Créer** pour créer la configuration IMS dans AEM.

### Etape 5a - Création d’une propriété dans le lancement Adobe {#create-property}

Une propriété définit les fonctionnalités que Launch peut injecter sur votre site.

1. Accédez à Adobe Launch à `https://launch.adobe.com`.
1. Connectez-vous à l’aide de votre identifiant Adobe ID.
1. Cliquez sur **Nouvelle propriété**.
1. Saisissez un nom tel que **Lancer la couche** de données AEM.
1. Entrez votre domaine.
1. Cliquez sur **Enregistrer**.

### Étape 5b - Création d&#39;une règle au lancement {#launch-rule}

A l’aide de la propriété que vous avez créée, vous pouvez définir une règle qui spécifie ce qui doit se produire lorsqu’une action se produit.

1. Cliquez sur la propriété nouvellement ajoutée à l’ [étape 5](#create-property) **Lancer la couche** de données AEM.
1. Sélectionnez l’onglet **Règles** , puis cliquez sur **Créer une règle**.
1. Saisissez un nom tel que **Image-click**.
1. Cliquez sur le bouton **+** sous **Événements**.
1. Sélectionnez **Core** as **Extension**, **cliquez sur** as **Type d&#39;événement et saisissez .cmp-image en tant que sélecteur CSS .**********
1. Cliquez sur **Conserver les modifications**.
1. Cliquez sur le bouton **+** ci-dessous **Actions**.
1. Sélectionnez **Core** as **Extension**, **Custom Code** as **Action Type et cliquez sur Ouvrir l’éditeur.******
1. Dans l’éditeur, saisissez le code suivant : `console.log("DOM click event tracked by Launch for image: ", event.target.src);`
1. Cliquez sur **Enregistrer**.
1. Cliquez sur **Conserver les modifications**.
1. Cliquez sur **Enregistrer** pour créer la nouvelle règle.

### Étape 6 - Publication de la règle de lancement {#publish-rule}

Pour rendre la nouvelle règle disponible pour votre site AEM, vous devez la publier.

1. Dans l’onglet Lancement **** Adobe, sélectionnez l’onglet **Publication** .
1. Click **Add New Library**.
1. Entrez un **nom** , par exemple **demo-1**.
1. Pour **l’Environnement** , sélectionnez le cas échéant, par exemple **Développement (développement)**.
1. Cliquez sur **Ajouter une ressource**.
1. Sélectionnez **Règles -> Image-click -> Dernière** et cliquez sur **Sélectionner et créer une nouvelle révision**.
1. Cliquez sur **Enregistrer et générer pour le développement**.
1. Dans la fenêtre contextuelle, cliquez sur **Appliquer les mises à jour et Continuer**.
1. Une fois la bibliothèque créée, cliquez sur l’icône représentant des points de suspension et sélectionnez **Envoyer pour approbation**.
1. Dans la fenêtre contextuelle, cliquez sur **Envoyer**.
1. Cliquez sur l’icône représentant des points de suspension et sélectionnez **Créer pour l’évaluation**.
1. Une fois la compilation terminée, cliquez sur l’icône représentant des points de suspension et sélectionnez **Approuver pour publication**.
1. Dans la fenêtre contextuelle, cliquez sur **Approuver**.
1. Cliquez sur l’icône représentant des points de suspension et sélectionnez **Créer et publier en production**.
1. Dans la fenêtre contextuelle, cliquez sur **Publier**.

### Étape 7 - Activation des configurations de cloud pour votre site {#enable-configurations}

Pour utiliser l’intégration, elle doit être affectée dans AEM en tant que configuration de cloud.

1. Dans la console AEM, cliquez sur **Outils -> Général -> Navigateur** de configuration.
1. Vérifiez les exemples **de composants** principaux et cliquez sur **Propriétés**.
1. Vérifiez les Configurations **de** Cloud et cliquez sur **Enregistrer et fermer**.

### Etape 8 - Création d’une intégration de lancement avec votre site dans AEM {#create-launch-integration}

Une intégration de lancement est nécessaire pour qu’AEM fonctionne avec le lancement

1. Dans la console AEM, cliquez sur **Outils -> Services Cloud -> Configurations** de lancement Adobe.
1. Sélectionnez Exemples **de composants** principaux et cliquez sur **Créer**.
1. Saisissez un **titre** tel que la configuration **** de lancement.
1. Sélectionnez la configuration IMS que vous avez créée à l’ [étape 4.](#finish-ims)
1. Au fur et à mesure que **la Société** se présente, sélectionnez le cas échéant.
1. En tant que **propriété** , sélectionnez la nouvelle propriété Launch créée à l’ [étape 5.](#create-property)
1. Déplacez le curseur **Inclure le code de production sur l’auteur** vers la droite et cliquez sur **Suivant**.
1. Cliquez sur **Suivant**.
1. Cliquez sur **Suivant**.
1. Cliquez sur **Créer**.

### Étape 9 - Connexion de votre site AEM au lancement de l’intégration {#connect-aem}

Pour qu’AEM utilise l’intégration de lancement, elle doit être affectée en tant que configuration de cloud.

1. Dans la console AEM, cliquez sur **Sites** et vérifiez le site **Core** Components.
1. Cliquez sur **Propriétés**.
1. Select the **Advanced** tab.
1. En tant que configuration **** Cloud, sélectionnez les exemples **de composants** principaux et cliquez sur **Sélectionner**.
1. Cliquez sur **Enregistrer et fermer**.

### Etape 10 - Vérification de l’application de la logique de lancement à la page {#verify-launch}

Testez que les étapes jusqu&#39;à présent ont été couronnées de succès.

1. Ouvrez la page Image de la bibliothèque de composants principaux en mode prévisualisation : `http://<lhost&gt;:<port&gt;/editor.html/content/core-components-examples/library/page-authoring/image.html`
1. Cliquez sur une image et vérifiez que le message `A Core Image was clicked` s’affiche dans la console du navigateur.

## Lancement de l’intégration avec AEM et la couche de données {#data-layer-launch}

Maintenant que l’intégration entre AEM et Launch est configurée, nous pouvons l’intégrer à la couche de données.

### Etape 1 - Création d’une règle dans le lancement Adobe {#create-rule}

Répétez les étapes de l’ [étape 5](#launch-rule) pour ajouter une nouvelle règle dans Adobe Launch à l’aide des valeurs suivantes.

* Nom: `image-click-data-layer`
* ÉVÉNEMENTS :
   * Extension : Core
   * Type d&#39;événement : Compatible DOM
* ACTIONS:
   * Extension : Core
   * Type d&#39;action : Code personnalisé
   * Code:

      ```
        function onImageClick(event) {
          console.log("Data layer click event tracked by Launch for image: " + event.info.path);
          console.log("dataLayer.getState(): ", adobeDataLayer.getState()); 
        }
        adobeDataLayer.addEventListener('image clicked', onImageClick);
      ```

### Étape 2 - Publication de la règle de lancement pour la rendre disponible pour votre site AEM {#publish-rule-2}

Répétez les étapes de l’ [étape 6](#publish-rule) pour publier la nouvelle règle.

### Étape 3 - Vérification de l&#39;application de la logique de lancement à la page {#verify}

1. Ouvrez la page Image de la bibliothèque de composants principaux en mode prévisualisation : `http://<host&gt;:<port&gt;/editor.html/content/core-components-examples/library/page-authoring/image.html`
1. Cliquez sur une image et vérifiez que le message suivant s’affiche dans la console du navigateur :

   ![Sortie de la console de couche de données](/help/assets/data-layer-console-output.png)
