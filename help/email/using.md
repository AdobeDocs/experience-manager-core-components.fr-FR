---
title: Utilisation des composants principaux d’e-mail
description: Découvrez l’installation, la configuration et l’utilisation de base des composants principaux d’e-mail.
role: Architect, Developer, Admin, User
exl-id: 0e79ca8f-eb0a-4519-b1e8-a9d3b0b99987
index: false
source-git-commit: eb77567dc32cccb81a9fc131493d11fb55b7e93b
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Utilisation des composants principaux d’e-mail {#using}

Découvrez l’installation, la configuration et l’utilisation de base des composants principaux d’e-mail.

## Installation des composants principaux d’e-mail {#installation}

Les composants principaux d’e-mail peuvent être utilisés avec AEM 6.5. Voir la section [Conditions requises du document Présentation des composants principaux d’e-mail](introduction.md#requirements) pour plus d’informations.

### Installer les composants principaux {#core-components}

Les composants principaux d’e-mail sont créés sur les composants principaux d’AEM. Comme les composants principaux ne sont pas fournis avec AEM 6.5, vous devez d’abord installer les composants principaux AEM avant d’installer les composants principaux d’e-mail.

Consultez la section [Téléchargement et installation](/help/get-started/using.md#download-and-install) du document Utilisation des composants principaux pour plus d’informations sur l’installation des composants principaux.

### Installer les composants principaux d’e-mail {#email-core-components}

Une fois les composants principaux installés dans votre instance, vous devez également installer les composants principaux d’e-mail. Les composants principaux d’e-mail ne font pas encore partie de l’archétype du projet AEM. Vous devrez donc les ajouter manuellement à votre projet. Consultez la documentation de la section [wiki GitHub des composants principaux d’e-mail à installer.](https://github.com/adobe/aem-core-email-components/wiki/Adding-to-Existing-Project)

Vous pouvez suivre les mêmes instructions si vous souhaitez adapter un projet existant pour utiliser les composants principaux d’e-mail.

## Configuration {#configuration}

Après avoir installé les composants principaux, vous devez effectuer deux importantes étapes de configuration.

### Configurer Campaign {#configure-campaign}

Vous devez configurer l’intégration AEM-Adobe Campaign pour que les deux solutions communiquent.

* Configurez votre intégration Adobe Campaign
   * Adobe Campaign Classic : [Intégration à Adobe Campaign Classic](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignonpremise.html?lang=fr)
   * Adobe Campaign Standard : [Intégration à Adobe Campaign Standard](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html?lang=fr)
* [Lier la configuration de l’intégration Adobe Campaign](/help/email/components/page.md#cloud-services-tab) sur la page de contenu où vous utiliserez les composants principaux d’e-mail.

### Ajouter le filtre de type de ressource AEM pour les composants d’e-mail {#aem-resource-filter}

Pour qu’Adobe Campaign puisse générer des e-mails en fonction des composants principaux d’e-mail, un filtre doit être ajusté dans Campaign.

1. Connectez-vous à Adobe Campaign en tant qu’administrateur à l’aide de la console cliente.

1. Sélectionnez **Outils** -> **Explorateur** dans la barre de menus.

1. Dans l’explorateur, accédez au nœud **Administration** -> **Plateforme** -> **Options**.

1. Dans la liste, sélectionnez l’option `AEMResourceTypeFilter`.

1. Dans le champ **Valeur**, ajoutez `core/email/components/page/<v1>/page` s’il n’est pas déjà présent.

   * Remplacez `<v1>` par la version actuelle des composants principaux d’e-mail [Composant de page](/help/email/components/page.md), comme `v1`.
   * Notez que les valeurs dans le champ **Valeurs** doivent être délimitées par des virgules.

1. Cliquez sur **Enregistrer**.

## Utilisation des composants principaux d’e-mail {#using-components}

Une fois les composants d’e-mail installés et l’intégration à Adobe Campaign configurée, vous pouvez utiliser les composants d’e-mail pour créer du contenu d’e-mail dans AEM, puis envoyer ce contenu aux destinataires à l’aide d’Adobe Campaign. Voici un aperçu du workflow.

| Étape | Description | Solution |
|---|---|---|
| 1 | Les créateurs créent une structure hiérarchique libre de dossiers et de contenu d’e-mail sous forme de pages. | AEM |
| 2 | En utilisant l’[éditeur de modèles](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=fr), les créateurs configurent un en-tête ou un pied de page d’e-mail qui serait partagé dans toutes les pages d’e-mail résultant de ce modèle de page. | AEM |
| 3 | Les créateurs utilisent l’[éditeur de page](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/editing-content.html?lang=fr) pour créer du contenu d’e-mail à l’aide de l’éditeur de texte dans lequel ils peuvent sélectionner des variables Adobe Campaign et utiliser le composant Segmentation pour afficher sous condition les informations si le destinataire répond à certains critères. | AEM |
| 4 | Une fois le contenu de l’e-mail terminé, [un workflow est exécuté](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/workflows/overview.html?lang=fr) pour approuver le contenu et l’envoyer à Campaign. | AEM |
| 5 | Une diffusion est créée, définissant une liste de destinataires. | Campaign |
| 6 | Le contenu créé dans AEM est sélectionné comme contenu de la diffusion. | Campaign |
| 7 | Le contenu est envoyé aux destinataires, et remplace les variables Adobe Campaign par les informations personnalisées des destinataires. | Campaign |

Pour obtenir un exemple de création de contenu d’e-mail dans AEM et de diffusion dans Adobe Campaign, reportez-vous aux ressources suivantes.

* AEM 6.5 : [Utilisation d’Adobe Campaign Classic et d’Adobe Campaign Standard](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/aem-adobe-campaign/campaign.html?lang=fr)
