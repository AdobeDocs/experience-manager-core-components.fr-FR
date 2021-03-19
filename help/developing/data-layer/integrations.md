---
title: Intégrations et couche de données client Adobe
description: Découvrez comment la couche de données client Adobe peut s’intégrer à vos composants personnalisés et comment les intégrations avec Adobe Analytics et Adobe Target peuvent vous aider à obtenir des informations sur votre site web
feature: Composants principaux, couche de données client Adobe
role: Architecte, développeur, administrateur
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 97%

---


# Intégrations à la couche de données client Adobe {#integrations}

La couche de données client Adobe réduit les efforts d’instrumentalisation des sites web en fournissant une méthode normalisée afin d’exposer et d’accéder à tout type de données pour tout script.

La couche de données client Adobe peut s’intégrer à vos composants personnalisés et les intégrations avec Adobe Analytics et Adobe Target peuvent vous aider à obtenir des informations sur votre site web.

## Activation de la couche de données pour les composants personnalisés {#enabling-custom-components}

Pour ajouter automatiquement un composant personnalisé à la couche de données :

1. définissez les propriétés du modèle de composant personnalisé qui doit être suivi ;
1. ajoutez l’attribut `data-cmp-data-layer` au composant personnalisé HTL. Par exemple, `data-cmp-data-layer="${mycomponent.data.json}"`.

Pour que la couche de données déclenche automatiquement un événement `cmp:click` à chaque clic sur un élément spécifique du composant personnalisé, ajoutez l’attribut `data-cmp-clickable` à l’élément à suivre dans le composant personnalisé HTL.

L’attribut `data-cmp-data-layer-enabled` peut être interrogé côté client pour vérifier si la couche de données est activée.

>[!TIP]
>
>Pour obtenir des détails techniques sur l’intégration de la couche de données client Adobe avec les composants principaux et sur l’activation de la couche de données pour vos composants personnalisés, consultez le fichier [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) dans le référentiel des composants principaux.

## Intégration avec Adobe Analytics et Adobe Target {#analytics-target}

Associée à Adobe Analytics et Adobe Target, la couche de données client Adobe devient la base d’un ensemble d’outils très puissant et flexible permettant de mieux comprendre vos expériences numériques. Les tutoriels suivants vous guident à travers des exemples d’intégration.

### Collecte de données de page avec Adobe Analytics {#collect-page-data}

Découvrez comment utiliser les fonctionnalités intégrées de la couche de données client Adobe avec les composants principaux d’AEM pour collecter des données sur une page dans Adobe Experience Manager Sites. Experience Platform Launch et l’extension Adobe Analytics seront utilisés pour créer des règles permettant d’envoyer des données de page à Adobe Analytics.

[Afficher le tutoriel ici.](https://docs.adobe.com/content/help/fr-FR/experience-manager-learn/sites/integrations/analytics/collect-data-analytics.html)

### Suivi des composants cliqués avec Adobe Analytics {#track-clicked-components}

Utilisez la couche de données client Adobe orientée sur les événements avec les composants principaux d’AEM pour effectuer le suivi des clics effectués sur des composants spécifiques sur un site Adobe Experience Manager. Découvrez comment utiliser des règles dans Experience Platform Launch pour écouter les événements de clics, filtrer par composant et envoyer les données à une instance Adobe Analytics avec une balise de lien de suivi.

[Afficher le tutoriel ici.](https://docs.adobe.com/content/help/fr-FR/experience-manager-learn/sites/integrations/analytics/track-clicked-component.html)
