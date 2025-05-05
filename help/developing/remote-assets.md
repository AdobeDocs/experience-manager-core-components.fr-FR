---
title: Prise en charge des ressources distantes
description: Découvrez comment configurer les composants Image et Teaser des composants principaux pour prendre en charge les ressources distantes à l’aide de Dynamic Media avec OpenAPI.
role: Architect, Developer, Admin, User
exl-id: b462c1f3-a6c8-4a2a-abf4-d08ec82d4371
source-git-commit: 36ef19d5b29fe21f86309719d1e3f6588e31a93b
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 100%

---


# Prise en charge des ressources distantes {#remote-assets-support}

Découvrez comment configurer les composants Image et Teaser des composants principaux pour prendre en charge les ressources distantes à l’aide de Dynamic Media avec OpenAPI.

>[!NOTE]
>
>Dynamic Media avec OpenAPI était auparavant connu sous le nom de Dynamic Media de nouvelle génération. La fonctionnalité et l’utilisation sont identiques.

## Obtenir la dernière version d’AEM {#latest}

La prise en charge des ressources distantes à l’aide de Dynamic Media avec OpenAPI nécessite les éléments suivants :

* AEM 6.5 SP 18+ ou AEM as a Cloud Service
* La version 2.23.2 ou ultérieure des composants principaux

## Configurer le HTTPS {#https}

Il est généralement recommandé d’exécuter toutes vos instances AEM de production avec HTTPS. Toutefois, vos environnements de développement locaux ne sont peut-être pas configurés avec ce protocole. Cependant, les ressources distantes utilisant Dynamic Media avec OpenAPI nécessitent HTTPS pour fonctionner.

[Suivez ce guide](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/security/use-the-ssl-wizard.html?lang=fr) pour configurer HTTPS partout où vous souhaitez utiliser des ressources distantes, y compris les environnements de développement.

## Configurer l’OSGi {#osgi}

L’emplacement des ressources distantes doit être défini dans une configuration OSGi. Définissez la configuration OSGi de la **configuration Dynamic Media de nouvelle génération** comme suit, en remplaçant les valeurs par celles de votre environnement de ressources distantes.

```text
imsClient="<ims-client-name>"
enabled=B"true"
imsOrg="<ims-org>@AdobeOrg"
repositoryId="<repo-id>.adobeaemcloud.com"
```

![Fenêtre de configuration OSGi de la configuration Dynamic Media de nouvelle génération](/help/assets/remote-assets-osgi.png)

Pour plus d’informations sur la configuration d’OSGi, consultez les documents suivants :

* [Configuration d’OSGi pour Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi.html?lang=fr) pour AEM as a Cloud Service
* [Configuration d’OSGi](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/configuring/configuring-osgi.html?lang=fr) pour AEM 6.5

## Vérifier la configuration {#verify}

Vous pouvez désormais vérifier que la fonctionnalité de ressources distantes utilisant Dynamic Media avec OpenAPI fonctionne. Pour ce faire, vous pouvez installer l’exemple de site WKND et les composants principaux.

* La version 2.23.2 ou ultérieure des [composants principaux](https://github.com/adobe/aem-core-wcm-components/releases/download/core.wcm.components.reactor-2.23.2/core.wcm.components.all-2.23.2.zip) est requise.
* La version 3.2.0 ou ultérieure de l’[exemple de site WKND](https://github.com/adobe/aem-guides-wknd/releases/download/aem-guides-wknd-3.2.0/aem-guides-wknd.all-3.2.0-classic.zip) est requise.

Une fois les composants principaux et le site WKND installés, vous pouvez tester la fonctionnalité sur n’importe quelle page WKND.

1. Accédez à l’instance AEM avec HTTPS.

1. Ouvrez une page de démonstration WKND dans l’éditeur de page telle que `https://<host>:<httpsPort>/editor.html/content/wknd/language-masters/en/magazine/arctic-surfing.html`

1. Ajoutez un composant d’image à la page.

1. Dans la boîte de dialogue Configurer du composant, désélectionnez l’option **Récupérer l’image en vedette de la page** sur l’onglet **Ressource**, puis cliquez sur **Sélectionner**.

1. Si la configuration est bonne, une liste déroulante s’affiche avec les options **Locale** et **Distante**. Sélectionnez **Distante**.

   ![Options de sélection distante et locale pour la sélection d’images](/help/assets/remote-asset-selection.png)

1. Une boîte de dialogue s’ouvre et vous devez vous authentifier au service distant.

1. Après votre authentification, un explorateur de ressources du service distant s’ouvre. Sélectionnez la ressource souhaitée, puis appuyez ou cliquez sur **Sélectionner**.

   ![Sélection d’une ressource distante](/help/assets/remote-asset-picker.png)

La ressource distante est ajoutée à votre page AEM locale et vous avez vérifié que la fonctionnalité est correctement configurée.

## Utiliser des ressources distantes {#using}

Une fois les ressources distantes configurées, vous pouvez les sélectionner à l’aide des composants principaux, comme le [composant d’image](/help/components/image.md) et le [composant Teaser.](/help/components/teaser.md)
