---
title: Utilisation des composants principaux de messagerie
description: Découvrez l’installation, la configuration et l’utilisation de base des composants principaux d’email.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 7%

---


# Utilisation des composants principaux de messagerie {#using}

Découvrez l’installation, la configuration et l’utilisation de base des composants principaux d’email.

## Installation des composants principaux du courrier électronique {#installation}

Les composants principaux d’email peuvent être utilisés avec AEM 6.5. Voir la section [Section Conditions requises du document Présentation des composants principaux d’email](introduction.md#requirements) pour plus d’informations.

### Installation des composants principaux {#core-components}

Les composants principaux d’email sont créés sur les composants principaux d’AEM. Comme les composants principaux ne sont pas fournis avec AEM, vous devez d’abord installer les composants principaux AEM avant d’installer les composants principaux du courrier électronique.

Voir la section [Téléchargement et installation](/help/get-started/using.md#download-and-install) section du document Utilisation des composants principaux pour plus d’informations sur l’installation des composants principaux.

### Installation des composants principaux de messagerie {#email-core-components}

Une fois les composants principaux installés dans votre instance, vous devez également installer les composants principaux d’email. Les composants principaux de messagerie ne font pas encore partie de l’archétype de projet AEM. Vous devrez donc les ajouter manuellement à votre projet. Consultez la documentation de la section [le wiki GitHub des composants principaux du courrier électronique à installer.](https://github.com/adobe/aem-core-email-components/wiki/Adding-to-Existing-Project)

Vous pouvez suivre les mêmes instructions si vous souhaitez adapter un projet existant pour utiliser les composants principaux d’email.

## Configuration {#configuration}

Après avoir installé les composants principaux, vous devez effectuer deux étapes de configuration importantes.

### Configuration de Campaign {#configure-campaign}

Vous devez configurer l’intégration AEM-Adobe Campaign pour que les deux solutions communiquent.

* Configuration de votre intégration Adobe Campaign
   * Adobe Campaign Classic : [Intégration à Adobe Campaign Classic](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignonpremise.html)
   * Adobe Campaign Standard : [Intégration à Adobe Campaign Standard](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html)
* [Lier la configuration de l’intégration Adobe Campaign](/help/email/components/page.md#cloud-services-tab) sur la page de contenu où vous utiliserez les composants principaux de messagerie.

### Ajout d’AEM filtre de type de ressource pour les composants de messagerie {#aem-resource-filter}

Pour qu’Adobe Campaign puisse générer des emails en fonction des composants principaux des emails, un filtre doit être ajusté dans Campaign.

1. Connectez-vous à Adobe Campaign en tant qu’administrateur à l’aide de la console cliente.

1. Sélectionnez **Outils** -> **Explorateur** dans la barre de menus.

1. Dans l’explorateur, accédez au **Administration** -> **Plateforme** -> **Options** noeud .

1. Sélectionnez la `AEMResourceTypeFilter` dans la liste.

1. Dans le **Valeur** champ, ajouter `core/email/components/page/<v1>/page` s’il n’est pas déjà présent.

   * Remplacer `<v1>` avec la version actuelle des composants principaux d’email [Composant de page](/help/email/components/page.md) par exemple `v1`.
   * Notez que les valeurs de la variable **Valeurs** doit être délimité par des virgules.

1. Cliquez sur **Enregistrer**.

## Utilisation des composants principaux de messagerie {#using-components}

Une fois les composants de messagerie installés et l’intégration à Adobe Campaign configurée, vous pouvez utiliser les composants de messagerie pour créer du contenu d’email dans AEM, puis envoyer ce contenu aux destinataires à l’aide d’Adobe Campaign. Voici un aperçu du workflow.

| Étape | Description | Solution |
|---|---|---|
| 1 | Les auteurs créent une structure hiérarchique libre de dossiers et de contenu d’email sous forme de pages. | AEM |
| 2 | En utilisant la variable [éditeur de modèles,](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=fr) Les auteurs configurent un en-tête et/ou un pied de page d’email qui serait partagé dans toutes les pages de messagerie résultant de ce modèle de page. | AEM |
| 3 | Les auteurs utilisent la variable [éditeur de page](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/editing-content.html) pour créer du contenu d’email à l’aide de l’éditeur de texte dans lequel ils peuvent sélectionner des variables Adobe Campaign et utiliser le composant Segmentation pour afficher sous condition les informations si le destinataire répond à certains critères. | AEM |
| 4 | Une fois le contenu de l&#39;email terminé, [un workflow est exécuté.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/workflows/overview.html) pour valider le contenu et l&#39;envoyer à Campaign. | AEM |
| 5 | Une diffusion est créée, définissant une liste de destinataires. | Campaign |
| 6 | Le contenu créé dans AEM est sélectionné comme contenu de la diffusion. | Campagne |
| 7 | Le contenu est envoyé aux destinataires, en remplaçant les variables Adobe Campaign par les informations personnalisées des destinataires. | Campagne |

Pour obtenir un exemple de création de contenu d’email dans AEM et de diffusion dans Adobe Campaign, reportez-vous aux ressources suivantes.

* AEM as a Cloud Service : [Création de newsletters Campaign avec AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/campaign/creating-newsletters.html)
* AEM 6.5 : [Utilisation de Adobe Campaign Classic et Adobe Campaign Standard](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/aem-adobe-campaign/campaign.html)

