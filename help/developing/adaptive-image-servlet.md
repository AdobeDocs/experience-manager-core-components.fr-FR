---
title: Servlet Image adaptative
description: Découvrez comment les composants principaux utilisent le servlet Image adaptative pour la diffusion d’images et comment optimiser son utilisation.
role: Architect, Developer, Admin, User
exl-id: d9199d51-6f09-4000-9525-afc30474437e
source-git-commit: dd07fa714a23759d43ca491232674d88bc7bf88e
workflow-type: ht
source-wordcount: '254'
ht-degree: 100%

---

# Servlet Image adaptative {#adaptive-image-servlet}

Découvrez comment les composants principaux utilisent le servlet Image adaptative pour la diffusion d’images et comment optimiser son utilisation.

## Servlet Image adaptative ou diffusion d’images optimisées pour le web ? {#options}

Le composant Image principal peut utiliser deux méthodes pour diffuser des images.

* Le servlet Image adaptative est la valeur par défaut.
* [Diffusion d’images optimisées pour le web](/help/developing/web-optimized-image-delivery.md) est disponible pour AEMaaCS et réduit la taille du téléchargement de 25 % en moyenne.

Ce document décrit le servlet Image adaptative par défaut.

## Présentation {#overview}

Par défaut, le composant d’image utilise le servlet Image adaptative du composant principal pour diffuser des images. La [servlet Image adaptative](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) est en charge du traitement des images et de leur diffusion en continu. Les développeurs peuvent l’utiliser dans le cadre de leur [personnalisation des composants principaux](/help/developing/customizing.md).

## Optimisation de la sélection du rendu {#optimizing-rendition-selection}

La servlet d’image adaptative tente de sélectionner le meilleur rendu pour la taille et le type d’image demandés. Il est recommandé de définir les rendus DAM et les largeurs autorisées des composants Image de façon synchronisée afin que la servlet d’image adaptative effectue le moins de traitement possible.

Cela améliore les performances et évite que certaines images ne soient pas correctement traitées par la bibliothèque de traitement des images sous-jacente.

## Utiliser les derniers en-têtes modifiés {#last-modified}

Les requêtes conditionnelles effectuées par le biais de `Last-Modified` en-tête sont prises en charge par la servlet d’image adaptative, mais la mise en cache de l’en-tête `Last-Modified` [doit être activée dans Dispatcher](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=fr#caching-http-response-headers).

L’exemple de configuration de Dispatcher d’[AEM Project Archetype](/help/developing/archetype/overview.md) contient déjà cette configuration.
