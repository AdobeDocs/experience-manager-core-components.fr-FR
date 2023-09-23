---
title: Prise en charge de Dynamic Media de nouvelle génération
description: Découvrez comment configurer les composants Image et Teaser des composants principaux pour prendre en charge les ressources Dynamic Media de génération suivante distantes.
role: Architect, Developer, Admin, User
source-git-commit: 57307b75bd33fd538a1eb704cc37822847c896de
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 3%

---


# Prise en charge de Dynamic Media de nouvelle génération {#next-gen-dm-support}

Découvrez comment configurer les composants Image et Teaser des composants principaux pour prendre en charge les ressources Dynamic Media de génération suivante distantes.

## Obtention de la dernière version d’AEM {#latest}

La prise en charge des ressources distantes Dynamic Media de génération suivante nécessite :

* AEM 6.5 SP 18+ ou AEM as a Cloud Service
* Version 2.23.2 ou ultérieure des composants principaux

## Configurer le HTTPS {#https}

Il est généralement recommandé d’exécuter toutes vos instances d’AEM de production à l’aide de HTTP. Toutefois, vos environnements de développement locaux peuvent ne pas être configurés en tant que tels. Toutefois, les ressources distantes de génération suivante Dynamic Media nécessitent HTTPS pour fonctionner.

[Utiliser ce guide](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/security/use-the-ssl-wizard.html) pour configurer HTTPS partout où vous souhaitez utiliser des ressources distantes, y compris les environnements de développement.

## Configuration d’OSGi {#osgi}

L’emplacement des ressources distantes doit être défini dans une configuration OSGi. Configurez la variable **Configuration Dynamic Media de génération suivante** Configuration OSGi comme suit, en remplaçant les valeurs par celles de votre environnement de ressources distant.

```text
imsClient="<ims-client-name>"
enabled=B"true"
imsOrg="<ims-org>@AdobeOrg"
repositoryId="<repo-id>.adobeaemcloud.com"
```

![Fenêtre de configuration OSGi de la configuration Dynamic Media de génération suivante](/help/assets/remote-assets-osgi.png)

Pour plus d’informations sur la configuration d’OSGi, consultez les documents suivants :

* [Configuration d’OSGi pour Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi.html) pour les AEM as a Cloud Service
* [Configuration d’OSGi](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/configuring/configuring-osgi.html?lang=fr) pour AEM 6.5

## Vérification de la configuration {#verify}

Vous pouvez maintenant vérifier que la fonction Ressources distantes de génération suivante Dynamic Media fonctionne. Pour ce faire, vous pouvez installer l’exemple de site WKND et les composants principaux.

* [Composants principaux](https://github.com/adobe/aem-core-wcm-components/releases/download/core.wcm.components.reactor-2.23.2/core.wcm.components.all-2.23.2.zip) La version 2.23.2 ou ultérieure est requise.
* [Exemple de site WKND](https://github.com/adobe/aem-guides-wknd/releases/download/aem-guides-wknd-3.2.0/aem-guides-wknd.all-3.2.0-classic.zip) La version 3.2.0 ou ultérieure est requise.

Une fois les composants principaux et le site WKND installés, vous pouvez tester la fonctionnalité sur n’importe quelle page WKND.

1. Accédez à l’instance AEM à l’aide de HTTPS.

1. Ouvrez une page de démonstration WKND dans l’éditeur de page, tel que `https://<host>:<httpsPort>/editor.html/content/wknd/language-masters/en/magazine/arctic-surfing.html`

1. Ajoutez un composant d’image à la page.

1. Dans la boîte de dialogue Configurer du composant, désélectionnez l’option . **Hériter de l’image fournie de la page** sur le **Ressource** et cliquez sur **Pick**.

1. Si la configuration est correcte, une liste déroulante s’affiche avec les options . **Local** et **Distant**. Sélectionner **Distant**.

   ![Options de sélection distantes et locales pour la sélection d’images](/help/assets/remote-asset-selection.png)

1. Une boîte de dialogue s’ouvre et vous devez vous authentifier au service distant.

1. Une fois authentifié, un navigateur de ressources du service distant s’ouvre. Sélectionnez la ressource souhaitée, puis appuyez ou cliquez sur **Sélectionner**.

   ![Sélection d’une ressource distante](/help/assets/remote-asset-selection.png)

La ressource distante est ajoutée à votre page d’AEM locale et vous avez vérifié que la fonctionnalité est correctement configurée.

## Utilisation des ressources distantes {#using}

Une fois les ressources distantes configurées, vous pouvez les sélectionner à l’aide des composants principaux, comme dans l’ [Composant d’image](/help/components/image.md) et la variable [Composant Teaser.](/help/components/teaser.md)
