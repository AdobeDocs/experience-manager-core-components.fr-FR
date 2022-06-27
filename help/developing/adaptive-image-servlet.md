---
title: Servlet d’image adaptative
description: Découvrez comment les composants principaux utilisent la servlet d’image adaptative pour la diffusion d’images et comment optimiser son utilisation.
role: Architect, Developer, Admin, User
source-git-commit: 3ff1343ab4ef7a52f910984a0bcd8fc4201441bf
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 58%

---


# Servlet d’image adaptative {#adaptive-image-servlet}

Découvrez comment les composants principaux utilisent la servlet d’image adaptative pour la diffusion d’images et comment optimiser son utilisation.

## Adaptive Image Server ou diffusion d’images optimisée pour le web ? {#options}

Le composant principal Image peut utiliser deux méthodes pour diffuser des images.

* La servlet d’image adaptative est la valeur par défaut.
* [Diffusion d&#39;images optimisées pour le web](/help/developing/web-optimized-image-delivery.md) est disponible pour AEMaaCS et réduit la taille du téléchargement de 25 % en moyenne.

Ce document décrit la servlet d’image adaptative par défaut.

## Présentation {#overview}

Par défaut, le composant d’image utilise la servlet d’image adaptative du composant principal pour diffuser des images. La [servlet d’image adaptative](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) est en charge du traitement des images et de leur diffusion en continu. Les développeurs peuvent l’utiliser dans le cadre de leur [personnalisation des composants principaux](/help/developing/customizing.md).

## Optimisation de la sélection du rendu {#optimizing-rendition-selection}

La servlet d’image adaptative tente de sélectionner le meilleur rendu pour la taille et le type d’image demandés. Il est recommandé de définir les rendus DAM et les largeurs autorisées des composants Image de façon synchronisée afin que la servlet d’image adaptative effectue le moins de traitement possible.

Cela améliore les performances et évite que certaines images ne soient pas correctement traitées par la bibliothèque de traitement des images sous-jacente.

## Utilisation des en-têtes modifiés pour la dernière fois {#last-modified}

Les requêtes conditionnelles effectuées par le biais de `Last-Modified` en-tête sont prises en charge par la servlet d’image adaptative, mais la mise en cache de l’en-tête `Last-Modified` [doit être activée dans Dispatcher](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=fr#caching-http-response-headers).

L’exemple de configuration de Dispatcher d’[AEM Project Archetype](/help/developing/archetype/overview.md) contient déjà cette configuration.
