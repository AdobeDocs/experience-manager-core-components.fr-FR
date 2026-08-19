---
title: Configuration du composant Recherche optimisée par l'IA de contenu
description: Le composant Recherche optimisée par l'IA de contenu fournit aux visiteurs de votre site une recherche générée optimisée par l’IA. Découvrez comment activer ce composant pour les auteurs de contenu.
role: Developer, Admin
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: c18d9e03-ac7d-4811-9c92-3e92ddc70ade
source-git-commit: 865622469555a773138d3ff1b54138f2b76994b0
workflow-type: tm+mt
source-wordcount: 485
ht-degree: 2%

---


# Configuration du composant Recherche optimisée par l&#39;IA de contenu {#configure-content-ai-search-component}

Le composant Recherche optimisée par l&#39;IA de contenu fournit aux visiteurs de votre site une recherche générée optimisée par l’IA. Découvrez comment activer ce composant pour les auteurs de contenu.

## Prérequis {#prerequisites}

* Au moins un Source de contenu](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources) déjà créé et avec le statut **Disponible**.[
* La configuration OSGi du client d’IA dédiée au contenu AEM **** (`ContentAIClientImpl`) sur les instances de création et de publication, avec des informations d’identification d’API valides et une valeur **Source de contenu par défaut**. Consultez le document [Configuration d’un projet Adobe Developer Console](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/setup-adc-project) pour savoir comment obtenir des informations d’identification.

## Créer un composant proxy {#proxy-component}

Comme tous les composants principaux, il est recommandé de créer un composant proxy pour le composant Recherche optimisée par l&#39;IA de contenu par défaut fourni avec AEM. En conservant les modifications spécifiques au projet dans le composant proxy sous `/apps`, les composants de base sous `/libs` sont automatiquement mis à jour par Adobe et le composant de projet hérite automatiquement de ces mises à jour. Consultez les documents [Utilisation des composants principaux](/help/get-started/using.md#aemaacs) et [Instructions relatives aux composants](/help/developing/guidelines.md) pour plus d’informations.

## Configuration des bibliothèques clientes {#clientlib}

Le composant Recherche optimisée par l&#39;IA de contenu ne suit pas [le modèle standard d’inclusion des bibliothèques clientes dans les composants principaux](/help/developing/including-clientlibs.md). Suivez plutôt ces étapes.

Ajoutez les éléments suivants au `customheaderlibs.html` de composant de page de votre projet (pour CSS) et `customfooterlibs.html` (pour JS) :

```html
<sly data-sly-use.clientLib="/libs/granite/sightly/templates/clientlib.html"
     data-sly-call="${clientLib.css @ categories='core.wcm.components.contentaisearch.v1'}"></sly>
```

Si votre projet superpose son propre style de marque, ajoutez une deuxième catégorie pour la bibliothèque cliente de votre projet après celle-ci.

## Utilisation du composant Recherche optimisée par l&#39;IA de contenu {#using}

Vos auteurs de contenu peuvent désormais placer le composant Recherche optimisée par l&#39;IA de contenu sur leurs pages. Consultez le document [Composant Recherche optimisée par l&#39;IA de contenu](/help/components/ai-search.md) pour plus d’informations.

## Utilisation de l’IA dédiée au contenu par le composant {#how-it-works}

* Les requêtes de recherche standard sont traitées par la même couche de récupération que l’index de Source de contenu, renvoyant les pages, fragments ou ressources correspondants à partir de la source configurée.
* Lorsque le résumé généré par l’IA est activé, le composant appelle en outre le point d’entrée génératif de l’IA dédiée au contenu d’AEM, ancrant la réponse dans le même contenu indexé, et affiche les sources avec le résumé afin que les visiteurs puissent le vérifier.
* Comme les deux fonctionnalités sont lues à partir du même Source de contenu régi, les résultats et les résumés restent cohérents avec le contenu actuellement indexé. Réexécuter l’acquisition (voir [Contrôle des sources de contenu](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources)) actualise les deux.

## Étapes suivantes {#next-steps}

* [Contrôler vos sources de contenu](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources) — Créez et gérez le Source de contenu dans lequel ce composant effectue des recherches.
* [Configurer un projet Adobe Developer Console](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/setup-adc-project) — Obtenez les informations d’identification utilisées par la configuration du client IA dédiée au contenu OSGi.
* [Référence de l’API IA dédiée au contenu](https://developer.adobe.com/experience-cloud/experience-manager-apis/api/experimental/contentai/) — Comprenez les points d’entrée de recherche et de résumé génératif sous-jacents que ce composant appelle.
