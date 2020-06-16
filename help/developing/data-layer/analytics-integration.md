---
title: Utilisation de la couche de données client Adobe pour intégrer les composants principaux et Adobe Analytics
description: Configuration d’Adobe Analytics pour l’enregistrement des événements de composants principaux
translation-type: ht
source-git-commit: f930a0d6004a29369b189137dd9c52e637ea3a61
workflow-type: ht
source-wordcount: '1000'
ht-degree: 100%

---


# Utilisation de la couche de données client Adobe pour intégrer les composants principaux et Adobe Analytics {#analytics-integration}

Ce document décrit comment configurer une configuration de bout en bout basée sur AEM, la couche de données client Adobe, Adobe Launch et Adobe Analytics pour effectuer le suivi des éléments suivants :

* L’ID de page stocké dans la couche de données client Adobe lors du chargement d’une page
* Le chemin d’accès à l’image stocké dans la couche de données client Adobe lorsqu’un utilisateur clique sur une image

Cette méthode utilise les composants principaux comme exemple, mais elle peut être utilisée pour vos propres composants personnalisés.

## Étape 1 – Création de la suite de rapports dans Adobe Analytics {#create-report-suite}

Pour agréger et analyser vos données, vous devez d’abord créer une suite de rapports.

1. Accédez à `https://analytics.adobe.com`.
1. Connectez-vous à l’aide de votre Adobe ID.
1. Cliquez sur l’icône **Analytics**.
1. Accédez à **Admin -> Suites de rapports**.
1. Cliquez sur **Créer -> Suite de rapports**.
1. Remplissez le formulaire :
   1. **Identifiant de suite de rapports** : `yourSuiteID`
   1. **Titre du site** : `Your suite description`
   1. **Fuseau horaire** : selon le cas
   1. **Date d’activation** : la date d’aujourd’hui ou selon le cas
   1. **Estimation du nombre de pages vues par jour** : 100 ou selon le cas
1. Cliquez sur **Créer une suite de rapports**.

En cas de réussite, vous verrez le message suivant en vert : `Report Suite <yourReportSuite> has been successfully created.`

## Étape 2 – Rendre la suite de rapports visible {#make-visible}

Pour utiliser la nouvelle suite de rapports, celle-ci doit être visible.

1. Accédez à `https://adminconsole.adobe.com`.
1. Connectez-vous à l’aide de votre Adobe ID.
1. Cliquez sur la carte **Adobe Analytics - &lt;votreSite>**.
1. Cliquez sur le lien **Adobe Analytics - &lt;votreSite>**.
1. Sélectionnez l’onglet **Autorisations**.
1. Cliquez sur le bouton **Modifier** de la ligne **Suite de rapports**.
1. Cliquez sur le bouton **+** de la suite de rapports que vous avez créée à l’[étape 1](#create-report-suite) pour l’ajouter à la catégorie **Éléments d’autorisation inclus**.
1. Cliquez sur **Enregistrer**.

## Étape 3 – Intégration de votre site AEM à Adobe Launch {#integrate-launch}

Launch doit être intégré à votre site AEM pour générer des données.

Suivez les étapes décrites dans le document [Utilisation de la couche de données client Adobe pour intégrer les composants principaux et Adobe Launch](launch-integration.md).

## Étape 4 – Installation et configuration de l’extension Adobe Analytics dans Adobe Launch {#install-extension}

L’extension Adobe Analytics permet l’intégration d’Analytics à Launch.

1. Dans Adobe Launch, sélectionnez la propriété créée à l’[étape 3.](#integrate-launch)
1. Accédez à l’onglet **Extensions** et sélectionnez **Catalogue**.
1. Recherchez **Adobe Analytics**.
1. Cliquez sur **Installer**.
1. Configurez l’extension.
   1. Saisissez l’**Identifiant de suite de rapports Analytics** créé à l’[étape 1](#create-report-suite) pour les environnements appropriés.
   1. Définissez le **Jeu de caractères** sur UTF-8.
1. Cliquez sur Enregistrer

## Étape 5 – Création d’un élément de données dans Adobe Launch pour l’ID de page {#create-data-element}

Un élément de données est requis dans Launch pour effectuer le suivi de l’ID de page.

1. Dans Adobe Launch, sélectionnez la propriété créée à l’[étape 3.](#integrate-launch)
1. Sélectionnez l’onglet **Data Elements** (Éléments de données) et cliquez sur **Add Data Element** (Ajouter un élément de données) :
   1. **Name** (Nom) : `dl-page-id`
   1. **Extension** : **Core**
   1. **Data Element Type** (Type d’élément de données) : **Custom Code** (Code personnalisé)
1. Cliquez sur **Open Editor** (Ouvrir l’éditeur)
1. Dans l’éditeur, saisissez le code : `return adobeDataLayer.getState().page.id;`
1. Cliquez sur **Save** (Enregistrer).
1. Cliquez sur **Save** (Enregistrer) pour créer l’élément de données.

## Étape 6 – Création d’une règle dans Adobe Launch pour le suivi de l’ID de page dans Analytics {#track-page}

Les règles permettent le suivi des attributs de navigation, tels que l’ID de page dans Analytics.

Répétez les étapes décrites dans la partie 5b du document [Utilisation de la couche de données client Adobe pour intégrer les composants principaux Adobe Launch](launch-integration.md#launch-rule) afin d’ajouter la règle suivante dans Adobe Launch :

* **Name** (Nom) : `track-dl-page-id`
* EVENTS (ÉVÉNEMENTS) :
   * **Extension** : **Core**
   * **Event Type** (Type d’événement) : **Page Bottom** (Bas de page)
* ACTION 1 :
   * **Extension** : **Adobe Analytics**
   * **Action Type** (Type d’action) : **Set Variables** (Définir des variables)
   * **prop1** : `%dl-page-id%`
* ACTION 2 :
   * **Extension** : **Adobe Analytics**
   * **Action Type** (Type d’action) : **Send Beacon** (Envoyer une balise)
   * Cochez **s.t() : Send Data to Adobe Analytics and treat it as a page view** (Envoyer les données à Adobe Analytics et les traiter comme une page vue)

## Étape 7 – Création d’une règle dans Adobe Launch pour enregistrer l’événement de clic sur image {#register-click}

Les règles permettent le suivi des attributs de navigation, tels que les événements de clics dans Analytics.

Répétez les étapes décrites dans la partie 5b du document [Utilisation de la couche de données client Adobe pour intégrer les composants principaux Adobe Launch](launch-integration.md#launch-rule) afin d’ajouter la règle suivante dans Adobe Launch :

* **Name** (Nom) : `register-dl-image-click`
* EVENTS (ÉVÉNEMENTS) :
   * **Extension** : **Core**
   * **Event Type** (Type d’événement) : **Page Bottom** (Bas de page)
* ACTION 1 :
   * **Extension** : **Core**
   * **Action Type** (Type d’action) : **Custom Code** (Code personnalisé)
   * Editor (Éditeur) : entrez le code suivant :

      ```
      var myListener = function(event) {
        _satellite.track('dlImageClicked', event.info.path);
      };
      adobeDataLayer.addEventListener('image clicked', myListener());
      ```

## Étape 8 – Création d’une règle dans Adobe Launch pour suivre l’événement de clic sur image dans Analytics {#track-click}

Les règles permettent le suivi des attributs de navigation, tels que les événements de clics dans Analytics.

Répétez les étapes décrites dans la partie 5b du document [Utilisation de la couche de données client Adobe pour intégrer les composants principaux Adobe Launch](launch-integration.md#launch-rule) afin d’ajouter la règle suivante dans Adobe Launch :

* **Name** (Nom) : `track-dl-image-click`
* EVENTS (ÉVÉNEMENTS) :
   * **Extension** : **Core**
   * **Event Type** (Type d’événement) : **Direct Call** (Appel direct)
   * **Identifier** (Identifiant) : `dlImageClicked`
* ACTION 1 :
   * **Extension** : **Adobe Analytics**
   * **Action Type** (Type d’action) : **Set Variables** (Définir des variables)
   * **prop2** : défini comme `%event.detail%`
* ACTION 2 :
   * **Extension** : **Adobe Analytics**
   * **Action Type** (Type d’action) : **Send Beacon** (Envoyer une balise)
   * Cochez **s.t() : Send Data to Adobe Analytics and treat it as a page view** (Envoyer les données à Adobe Analytics et les traiter comme une page vue)

## Étape 9 – Publication du code Launch sur votre site web {#publish-launch}

Pour activer le suivi de ces règles et propriétés dans Launch, le code doit être publié.

1. Dans l’onglet **Adobe Launch**, sélectionnez l’onglet **Publishing** (Publication).
1. Cliquez sur **Add New Library** (Ajouter une nouvelle bibliothèque).
1. Dans le champ **Nom** (Nom), entrez : `data-layer-analytics-1`.
1. Dans le champ **Environnement** (Environnement), sélectionnez **Development (development)** (Développement).
1. Cliquez sur **Add All Changed Resources** (Ajouter toutes les ressources modifiées).
1. Pour chacune des trois règles (`track-dl-page-id`, `register-dl-image-click` et `track-dl-image-click`) :
1. Sélectionnez **Rules -> règle -> Latest** (Règles -> règle -> Dernière) et cliquez sur **Select &amp; Create a New Revision** (Sélectionner et créer une révision).
1. Cliquez sur **Save &amp; Build for Development** (Enregistrer et créer pour le développement).

## Étape 10 – Déclenchement de votre page pour envoyer des informations à Adobe Analytics {#trigger-page}

Au cours de cette étape, vous allez installer l’extension Chrome **Launch et DTM Switch**. Avec cette extension, il vous suffit de créer le code Launch et de le déployer sur l’environnement de développement. Il n’est pas nécessaire de déployer sur les environnements d’évaluation et de production.

1. Installez l’extension Chrome **Launch et DTM Switch** de Discovery.
1. Cliquez sur l’icône **Launch Switch** (Lancer le commutateur) et définissez le débogage sur *ON* (Activé).
1. Rechargez la page `http://<host>:<port>/content/core-components-examples/library/image.html`.
1. Ouvrez la console du navigateur et vous devriez voir quelque chose de ce type.

![Sortie de la console Analytics](/help/assets/analytics-console-output.png)

>[!TIP]
>
>Vous pouvez également installer l’extension **Experience Cloud Debugger** pour Chrome afin d’afficher les informations spécifiques à Adobe Launch et Analytics concernant la page.

## Étape 11 – Affichage des informations suivies dans Adobe Analytics {#view-info}

Vous pouvez désormais afficher les événements que vous avez déclenchés dans Adobe Analytics.

1. Accédez à `https://analytics.adobe.com`.
1. Connectez-vous à l’aide de votre Adobe ID.
1. Cliquez sur l’icône **Analytics**.
1. Sélectionnez l’onglet **Rapports**.
1. Dans la liste déroulante en haut à droite, sélectionnez la suite de rapports que vous avez créée à l’[étape 1.](#create-report-suite)
1. Dans la première colonne, sélectionnez **Trafic personnalisé -> Trafic personnalisé 1-10 -> Custom Insight 1** pour afficher les ID des pages suivies (chemins) stockés dans la couche de données. Cela devrait ressembler à ce qui suit.

   ![Custom Insight 1](/help/assets/custom-insight-1.png)

1. Accédez à **Custom Insight 2** pour afficher les chemins des images suivies stockés dans la couche de données. Cela devrait ressembler à ce qui suit.

   ![Custom Insight 2](/help/assets/custom-insight-2.png)
