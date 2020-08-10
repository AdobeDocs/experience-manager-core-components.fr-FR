---
title: Utilisation de la couche de données client Adobe pour intégrer les composants principaux et Adobe Launch
description: Configuration d’Adobe Launch pour l’enregistrement des événements des composants principaux
translation-type: ht
source-git-commit: 85fb3612aed12b7bfdc05f0a569ae7c7364e6121
workflow-type: ht
source-wordcount: '1160'
ht-degree: 100%

---


# Utilisation de la couche de données client Adobe pour intégrer les composants principaux et Adobe Launch {#launch-integration}

Les composants principaux peuvent être intégrés à Adobe Launch à l’aide de la couche de données du client Adobe. Ce document décrit comment configurer Adobe Launch de façon à effectuer le suivi des événements de clics pour les composants d’image (à titre d’exemple).

Lorsqu’il est configuré, Launch génère la sortie suivante dans la console du navigateur quand un utilisateur clique sur un composant principal Image.

![Exemple de sortie de console](/help/assets/launch-console-output.png)

## Intégration de Launch à AEM {#launch-aem}

Pour commencer, Adobe Launch doit être intégré à votre site AEM.

### Étape 1 – Création d’une intégration dans Adobe I/O {#create-io-integration}

Connectez-vous d’abord à Adobe I/O pour commencer à configurer une intégration.

1. Accédez à `https://console.adobe.io`.
1. Connectez-vous à l’aide de votre Adobe ID.
1. Dans la section Quick Start (Démarrage rapide), cliquez sur **Create integration** (Créer une intégration).
1. Sélectionnez **Access an API** (Accéder à une API), puis cliquez sur **Continue** (Continuer).
1. Sélectionnez **Experience Platform Launch API** sous Adobe Experience Platform et cliquez sur **Continue** (Continuer).

### Étape 2 – Création d’une configuration IMS dans AEM {#ims-configuration}

Dans AEM, vous devez définir l’intégration que vous avez commencée à configurer dans Adobe I/O.

1. Accédez à la page d’accueil AEM, cliquez sur **Outils -> Sécurité -> Configurations d’Adobe IMS**.
1. Cliquez sur **Créer**.
1. Comme **Solution cloud**, sélectionnez **Adobe Launch**.
1. Cochez la case **Créer un certificat**.
1. Saisissez un alias pour le certificat, par exemple **aem-launch-certificate**.
1. Cliquez sur **Créer un certificat** et dans la fenêtre contextuelle, cliquez sur **OK** pour créer le certificat.
1. Cliquez sur **Télécharger la clé publique** et dans la fenêtre contextuelle, cliquez sur **Télécharger**.

### Étape 3 – Finalisation de la configuration Adobe I/O {#finish-io}

Avec le certificat et la clé créés dans la configuration IMS d’AEM, vous pouvez terminer votre configuration Adobe I/O.

1. Revenez à la console Adobe I/O comme à l’[étape 1.](#create-io-integration)
1. Dans la fenêtre **Create a new integration** (Créer une intégration), saisissez un nom et une description tels que **Couche de données AEM Launch**.
1. Sous **Public keys certificates** (Certificats de clés publiques), chargez le certificat que vous avez créé à l’[étape 2.](#ims-configuration)
1. Sélectionnez le **profil Launch - prod**.
1. Cliquez sur **Create integration** (Créer une intégration).
1. Cliquez sur **Continue to integration details** (Continuer pour accéder aux informations sur l’intégration). Vous aurez besoin de ces informations ultérieurement pour terminer la configuration IMS dans votre instance AEM.

### Étape 4 – Finalisation de la configuration IMS {#finish-ims}

Avec les informations sur l’intégration d’Adobe I/O, vous pouvez terminer la configuration IMS pour AEM.

1. Au niveau de l’onglet AEM, dans l’onglet **Configuration du compte technique Adobe IMS** de l’[étape 2](#ims-configuration), cliquez sur **Suivant**.
1. Saisissez un titre tel que **Configuration IMS pour Adobe Launch**.
1. Dans l’onglet Adobe I/O, copiez la **API Key (Client ID)** (Clé API (ID client)).
1. Dans l’onglet AEM, collez dans le champ **Clé API** la clé que vous venez de copier.
1. Dans Adobe I/O, cliquez sur **Retrieve Client Secret** (Récupérer le secret du client) et copiez-le.
1. Dans l’onglet AEM, collez-la dans le champ **Secret du client**.
1. Dans l’onglet Adobe I/O, sélectionnez l’onglet **JWT** et copiez l’URL telle que `https://ims-na1.adobelogin.com`.
1. Dans l’onglet AEM, collez l’URL dans le champ **Serveur d’autorisation**.
1. Dans l’onglet Adobe I/O, copiez la charge utile JWT (le code entre accolades).
1. Dans l’onglet AEM, collez-la dans le champ **Charge utile**.
1. Cliquez sur **Créer** pour créer la configuration IMS dans AEM.

### Étape 5a – Création d’une propriété dans Adobe Launch {#create-property}

Une propriété définit les fonctionnalités que Launch peut injecter sur votre site.

1. Accédez à Adobe Launch à l’adresse `https://launch.adobe.com`.
1. Connectez-vous à l’aide de votre Adobe ID.
1. Cliquez sur **New Property** (Nouvelle propriété).
1. Saisissez un nom tel que **Couche de données Launch AEM**.
1. Entrez votre domaine.
1. Cliquez sur **Save** (Enregistrer).

### Étape 5b – Création d’une règle dans Launch {#launch-rule}

À l’aide de la propriété que vous avez créée, vous pouvez définir une règle qui spécifie ce qui doit se produire lorsqu’une action a lieu.

1. Cliquez sur la propriété que vous avez ajoutée à l’[étape 5](#create-property) **Couche de données Launch AEM**.
1. Sélectionnez l’onglet **Rules** (Règles), puis cliquez sur **Create New Rule** (Créer une règle).
1. Saisissez un nom tel que **clic-image**.
1. Cliquez sur le bouton **+** sous **Events** (Événements).
1. Sélectionnez **Core** comme **Extension**, **Click** (Clic) comme **Event Type** (Type d’événement) et saisissez **.cmp-image** en tant que **CSS selector** (Sélecteur CSS).
1. Cliquez sur **Keep Changes** (Conserver les modifications).
1. Cliquez sur le bouton **+** sous **Actions**.
1. Sélectionnez **Core** comme **Extension**, **Custom Code** (Code personnalisé) comme **Action Type** (Type d’action) et cliquez sur **Open Editor** (Ouvrir l’éditeur).
1. Dans l’éditeur, saisissez le code suivant : `console.log("DOM click event tracked by Launch for image: ", event.target.src);`
1. Cliquez sur **Save** (Enregistrer).
1. Cliquez sur **Keep Changes** (Conserver les modifications).
1. Cliquez sur **Save** (Enregistrer) pour créer la règle.

### Étape 6 – Publication de la règle Launch {#publish-rule}

Afin de rendre la nouvelle règle disponible pour votre site AEM, vous devez la publier.

1. Dans l’onglet **Adobe Launch**, sélectionnez l’onglet **Publishing** (Publication).
1. Cliquez sur **Add New Library** (Ajouter une nouvelle bibliothèque).
1. Dans le champ **Name** (Nom), saisissez un nom approprié, par exemple **démo-1**.
1. Dans le champ **Environment** (Environnement), sélectionnez l’environnement approprié, par exemple **Development (development)** (Développement).
1. Cliquez sur **Add a Resource** (Ajouter une ressource).
1. Sélectionnez **Rules -> clic-image -> Latest** (Règles -> clic-image -> Dernière) et cliquez sur **Select &amp; Create a New Revision** (Sélectionner et créer une révision).
1. Cliquez sur **Save &amp; Build for Development** (Enregistrer et créer pour le développement).
1. Dans la fenêtre contextuelle, cliquez sur **Apply Updates and Continue** (Appliquer les mises à jour et continuer).
1. Une fois la bibliothèque créée, cliquez sur l’icône représentant des points de suspension et sélectionnez **Submit for Approval** (Envoyer pour approbation).
1. Dans la fenêtre contextuelle, cliquez sur **Submit** (Envoyer).
1. Cliquez sur l’icône représentant des points de suspension et sélectionnez **Build for Staging** (Créer pour l’évaluation).
1. Une fois la création terminée, cliquez sur l’icône représentant des points de suspension et sélectionnez **Approve for Publishing** (Approuver pour publication).
1. Dans la fenêtre contextuelle, cliquez sur **Approve** (Approuver).
1. Cliquez sur l’icône représentant des points de suspension et sélectionnez **Build &amp; Publish to Production** (Créer et publier en production).
1. Dans la fenêtre contextuelle, cliquez sur **Publish** (Publier).

### Étape 7 – Activation des configurations du cloud pour votre site {#enable-configurations}

Pour être utilisée, l’intégration doit être affectée dans AEM en tant que configuration du cloud.

1. Dans la console AEM, cliquez sur **Outils -> Général -> Explorateur de configuration**.
1. Cochez **Exemples de composants de base** et cliquez sur **Propriétés**.
1. Cochez **Configurations de cloud** et cliquez sur **Enregistrer et fermer**.

### Étape 8 – Création d’une intégration Launch avec votre site dans AEM {#create-launch-integration}

Une intégration est nécessaire pour qu’AEM fonctionne avec Launch

1. Dans la console AEM, cliquez sur **Outils -> Cloud Services -> Configurations Adobe Launch**.
1. Sélectionnez **Exemples de composants de base** et cliquez sur **Créer**.
1. Saisissez un **Titre** tel que **Configuration Launch**.
1. Sélectionnez la configuration IMS que vous avez créée à l’[étape 4.](#finish-ims)
1. Comme **Société**, sélectionnez celle qui convient.
1. Comme **Propriété**, sélectionnez la nouvelle propriété Launch créée à l’[étape 5.](#create-property)
1. Déplacez le curseur **Inclure le code de production sur l’auteur** vers la droite et cliquez sur **Suivant**.
1. Cliquez sur **Suivant**.
1. Cliquez sur **Suivant**.
1. Cliquez sur **Créer**.

### Étape 9 – Connexion de votre site AEM à l’intégration Launch {#connect-aem}

Pour qu’AEM utilise l’intégration Launch, elle doit être affectée en tant que configuration du cloud.

1. Dans la console AEM, cliquez sur **Sites** et cochez le site **Composants principaux**.
1. Cliquez sur **Propriétés**.
1. Sélectionnez l’onglet **Avancé**.
1. Comme **Configuration du cloud**, sélectionnez **Exemples de composants de base** et cliquez sur **Sélectionner**.
1. Cliquez sur **Enregistrer et fermer**.

### Étape 10 – Vérification de l’application de la logique Launch à la page {#verify-launch}

Vérifiez que les étapes ont réussi jusqu’à présent.

1. Ouvrez la page Image de la bibliothèque Composants principaux en mode d’aperçu : `http://<lhost&gt;:<port&gt;/editor.html/content/core-components-examples/library/page-authoring/image.html`
1. Cliquez sur une image et vérifiez que le message `A Core Image was clicked` s’affiche dans la console du navigateur.

## Intégration Launch avec AEM et la couche de données {#data-layer-launch}

Maintenant que l’intégration entre AEM et Launch est configurée, nous pouvons l’intégrer à la couche de données.

### Étape 1 – Création d’une règle dans Adobe Launch {#create-rule}

Répétez la procédure de l’[étape 5](#launch-rule) pour ajouter une règle dans Adobe Launch à l’aide des valeurs suivantes.

* Nom (name) : `image-click-data-layer`
* EVENTS (ÉVÉNEMENTS) :
   * Extension : Core
   * Event Type (Type d’événement) : DOM Ready (Compatible DOM)
* ACTIONS :
   * Extension : Core
   * Action Type (Type d’action) : Custom Code (Code personnalisé)
   * Code :

      ```
        function onImageClick(event) {
          console.log("Data layer click event tracked by Launch for image: " + event.info.path);
          console.log("dataLayer.getState(): ", adobeDataLayer.getState()); 
        }
        adobeDataLayer.addEventListener('image clicked', onImageClick);
      ```

### Étape 2 – Publication de la règle Launch afin de la rendre disponible pour votre site AEM {#publish-rule-2}

Répétez la procédure de l’[étape 6](#publish-rule) afin de publier la nouvelle règle.

### Étape 3 – Vérification de l’application de la logique Launch à la page {#verify}

1. Ouvrez la page Image de la bibliothèque Composants principaux en mode d’aperçu : `http://<host&gt;:<port&gt;/editor.html/content/core-components-examples/library/page-authoring/image.html`
1. Cliquez sur une image et vérifiez que le message suivant s’affiche dans la console du navigateur :

   ![Sortie de la console de couche de données](/help/assets/data-layer-console-output.png)
