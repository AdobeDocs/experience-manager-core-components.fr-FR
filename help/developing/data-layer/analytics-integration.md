---
title: Utilisation de la couche de données client Adobe pour intégrer les composants principaux et Adobe Analytics
description: Configuration d’Adobe Analytics pour l’enregistrement de événements de composants principaux
translation-type: tm+mt
source-git-commit: f930a0d6004a29369b189137dd9c52e637ea3a61
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 3%

---


# Utilisation de la couche de données client Adobe pour intégrer les composants principaux et Adobe Analytics {#analytics-integration}

Ce document décrit comment configurer une configuration de bout en bout basée sur AEM, la couche de données du client Adobe, Adobe Launch et Adobe Analytics pour effectuer le suivi :

* ID de page stocké dans la couche de données client Adobe lors du chargement d’une page
* Chemin d’accès à l’image stocké dans la couche de données du client Adobe lorsqu’un utilisateur clique sur une image

Cette méthode utilise les composants principaux comme exemple, mais elle peut être utilisée pour vos propres composants personnalisés.

##  Étape 1 - Création de la suite de rapports dans Adobe Analytics {#create-report-suite}

Pour agrégat et analyser vos données, vous devez d’abord créer une suite de rapports.

1. Accédez à `https://analytics.adobe.com`.
1. Connectez-vous à l’aide de votre identifiant Adobe ID.
1. Click the **Analytics** icon.
1. Accédez à **Admin -> Report Suites**.
1. Click **Create New -> Report Suite**.
1. Remplissez le formulaire :
   1. **Identifiant de la suite de rapports**: `yourSuiteID`
   1. **Titre** du site : `Your suite description`
   1. **Fuseau** horaire : Selon le cas
   1. **Date** Go Live : la date d&#39;aujourd&#39;hui ou selon le cas
   1. **Estimation des Vues de page par jour**: 100 ou selon le cas
1. Cliquez sur **Créer une suite de rapports**.

En cas de réussite, vous recevrez le message suivant en vert : `Report Suite <yourReportSuite> has been successfully created.`

## Étape 2 - Rendre la suite de rapports visible {#make-visible}

Pour utiliser la nouvelle suite de rapports, elle doit être visible.

1. Accédez à `https://adminconsole.adobe.com`.
1. Connectez-vous à l’aide de votre identifiant Adobe ID.
1. Cliquez sur la carte **Adobe Analytics - &lt;votreSite>** .
1. Cliquez sur le lien Analyses **Adobe - &lt;votreSite>** .
1. Select the **Permissions** tab
1. Cliquez sur le bouton **Modifier** de la ligne **Report Suites** .
1. Cliquez sur le bouton **+** de la suite de rapports que vous avez créée à l’ [étape 1](#create-report-suite) pour l’ajouter à la catégorie Éléments **d’autorisation** inclus.
1. Cliquez sur **Enregistrer**.

## Étape 3 - Intégration de votre site AEM au lancement Adobe {#integrate-launch}

Le lancement doit être intégré à votre site AEM pour générer des données.

Suivez les étapes décrites dans la section [Utilisation de la couche de données client Adobe pour intégrer les composants principaux et le document de lancement](launch-integration.md) Adobe.

## Étape 4 - Installation et configuration de l’extension Adobe Analytics dans le lancement de Adobe {#install-extension}

Adobe Analytics Extension permet l’intégration d’Analytics au lancement.

1. Dans Lancement Adobe, sélectionnez la nouvelle propriété ajoutée que vous avez créée à l’ [étape 3.](#integrate-launch)
1. Accédez à l’onglet **Extensions** et sélectionnez **Catalogue**.
1. Recherchez **Adobe Analytics**.
1. Cliquez sur **Installer**.
1. Configurez l&#39;extension.
   1. Saisissez l’identifiant **de suite de rapports** Analytics créé à l’ [étape 1](#create-report-suite) pour les environnements appropriés.
   1. Définir le jeu **de** caractères UTF-8
1. Cliquez sur Enregistrer

## Etape 5 - Création d’un élément de données dans le lancement Adobe pour l’ID de page {#create-data-element}

Un élément de données est requis dans Lancement pour pouvoir effectuer le suivi de l’ID de page.

1. Dans Adobe Launch, sélectionnez la propriété créée à l’ [étape 3.](#integrate-launch)
1. Sélectionnez l’onglet Eléments **de** données et cliquez sur **Ajouter l’élément** de données :
   1. **Nom**: `dl-page-id`
   1. **Extension**: **Core**
   1. **Type** d’élément de données : **Code personnalisé**
1. Cliquez sur **Ouvrir l’éditeur**
1. Dans l’éditeur, saisissez le code : `return adobeDataLayer.getState().page.id;`
1. Cliquez sur **Enregistrer**.
1. Cliquez sur **Enregistrer** pour créer l’élément de données.

## Étape 6 - Création d’une règle dans le lancement Adobe pour effectuer le suivi de l’ID de page dans Analytics {#track-page}

Les règles permettent le suivi des attributs de navigation, tels que l’ID de page dans Analytics.

Répétez les étapes décrites dans la partie 5b de la section [Utilisation de la couche de données client Adobe pour intégrer les composants principaux et le document de lancement](launch-integration.md#launch-rule) Adobe pour ajouter la règle suivante dans le lancement Adobe :

* **Nom**: `track-dl-page-id`
* ÉVÉNEMENTS :
   * **Extension**: **Core**
   * **Type d&#39;événement**: **Bas de page**
* ACTION 1 :
   * **Extension**: **Adobe Analytics**
   * **Type** d&#39;action : **Définition de variables**
   * **prop1**: `%dl-page-id%`
* ACTION 2 :
   * **Extension**: **Adobe Analytics**
   * **Type** d&#39;action : **Envoyer la balise**
   * Vérifier **s.t() : Envoyer des données à Adobe Analytics et les traiter comme une vue de page**

## Etape 7 - Création d’une règle dans le lancement Adobe pour enregistrer le Événement de clic sur l’image {#register-click}

Les règles permettent le suivi des attributs de navigation, tels que les événements de clics dans Analytics.

Répétez les étapes décrites dans la partie 5b de la section [Utilisation de la couche de données client Adobe pour intégrer les composants principaux et le document de lancement](launch-integration.md#launch-rule) Adobe pour ajouter la règle suivante dans le lancement Adobe :

* **Nom**: `register-dl-image-click`
* ÉVÉNEMENTS :
   * **Extension**: **Core**
   * **Type d&#39;événement**: **Bas de page**
* ACTION 1 :
   * **Extension**: **Core**
   * **Type** d&#39;action : **Code personnalisé**
   * Editeur : Entrez le code suivant :

      ```
      var myListener = function(event) {
        _satellite.track('dlImageClicked', event.info.path);
      };
      adobeDataLayer.addEventListener('image clicked', myListener());
      ```

## Etape 8 - Création d’une règle dans le lancement Adobe pour effectuer le suivi du Événement de clics sur l’image dans Analytics {#track-click}

Les règles permettent le suivi des attributs de navigation, tels que les événements de clics dans Analytics.

Répétez les étapes décrites dans la partie 5b de la section [Utilisation de la couche de données client Adobe pour intégrer les composants principaux et le document de lancement](launch-integration.md#launch-rule) Adobe pour ajouter la règle suivante dans le lancement Adobe :

* **Nom**: `track-dl-image-click`
* ÉVÉNEMENTS :
   * **Extension**: **Core**
   * **Type d&#39;événement**: **Appel direct**
   * **Identificateur**: `dlImageClicked`
* ACTION 1 :
   * **Extension**: **Adobe Analytics**
   * **Type** d&#39;action : **Définition de variables**
   * **prop2**: Défini comme `%event.detail%`
* ACTION 2 :
   * **Extension**: **Adobe Analytics**
   * **Type** d&#39;action : **Envoyer la balise**
   * Vérifier **s.t() : Envoyer des données à Adobe Analytics et les traiter comme une vue de page**

## Étape 9 - Publication du code de lancement sur votre site Web {#publish-launch}

Pour activer le suivi de ces règles et propriétés dans Lancement, le code doit être publié.

1. Dans l’onglet Lancement **** Adobe, sélectionnez l’onglet **Publication** .
1. Click **Add New Library**.
1. As **Name** enter: `data-layer-analytics-1`.
1. En tant qu&#39; **Environnement** , sélectionnez **Développement (développement)**.
1. Cliquez sur **Ajouter toutes les ressources** modifiées.
1. Pour chacune des trois règles (`track-dl-page-id`, `register-dl-image-click` et `track-dl-image-click`) :
1. Sélectionnez **Règles -> règle -> Dernière** et cliquez sur **Sélectionner et créer une nouvelle révision**.
1. Cliquez sur **Enregistrer et générer pour le développement**.

## Etape 10 - Déclenchez votre page pour envoyer des informations à Adobe Analytics {#trigger-page}

Au cours de cette étape, vous allez installer l’extension Chrome **Launch et DTM Switch**. Avec cette extension, vous n&#39;avez qu&#39;à créer et déployer le code de lancement sur l&#39;environnement de développement. Il n’est pas nécessaire de déployer les environnements d’évaluation et de production.

1. Installez l’extension Chrome **Launch et le commutateur** DTM Switch from Discovery.
1. Cliquez sur l’icône **Lancer le commutateur** et définissez le débogage sur *ON*.
1. Recharger la page `http://<host>:<port>/content/core-components-examples/library/image.html`.
1. Ouvrez la console du navigateur et vous devriez voir quelque chose de similaire à ce qui suit.

![Sortie de la console Analytics](/help/assets/analytics-console-output.png)

>[!TIP]
>
>Vous pouvez également installer l’extension **Experience Cloud Debugger** pour Chrome à l’vue de Adobe Launch et des informations spécifiques à Analytics sur la page.

## Etape 11 - Vue des informations suivies dans Adobe Analytics {#view-info}

Vous pouvez désormais vue les événements que vous avez déclenchés dans Adobe Analytics.

1. Accédez à `https://analytics.adobe.com`.
1. Connectez-vous à l’aide de votre identifiant Adobe ID.
1. Click the **Analytics** icon.
1. Select the **Reports** tab.
1. Dans la liste déroulante en haut à droite, sélectionnez la suite de rapports que vous avez créée à l’ [étape 1.](#create-report-suite)
1. Dans la première colonne, sélectionnez Trafic **personnalisé -> Trafic personnalisé 1-10 -> Custom Insight 1** pour vue des ID de page (chemins) suivis stockés dans la couche de données. Il devrait ressembler à ce qui suit.

   ![Custom Insight 1](/help/assets/custom-insight-1.png)

1. Accédez à **Custom Insight 2** pour vue des chemins d’image suivis stockés dans la couche de données. Il devrait ressembler à ce qui suit.

   ![Custom Insight 2](/help/assets/custom-insight-2.png)
