---
title: Servlet Image adaptative
description: Découvrez comment les composants principaux utilisent le servlet Image adaptative pour la diffusion d’images et comment optimiser son utilisation.
role: Architect, Developer, Admin, User
exl-id: d9199d51-6f09-4000-9525-afc30474437e
source-git-commit: 87a96c1c9476b9d66fdc94d6c24123cdf24b9d91
workflow-type: ht
source-wordcount: '457'
ht-degree: 100%

---

# Servlet Image adaptative {#adaptive-image-servlet}

Découvrez comment les composants principaux utilisent le servlet Image adaptative pour la diffusion d’images et comment optimiser son utilisation.

>[!WARNING]
>
>Pour des raisons de performances, il est vivement recommandé de stocker les images dans DAM et d’utiliser la diffusion d’images optimisée pour le web.
>
>Le stockage des images directement sous le nœud de composant est destiné à une utilisation occasionnelle. Il ne tire pas parti des rendus DAM pour réduire le traitement dans le servlet Image adaptative et ne permet pas de bénéficier des avantages de performances de la diffusion d’images optimisée pour le web, ce qui peut entraîner des problèmes de performances.

## Servlet Image adaptative ou diffusion d’images optimisée pour le web ? {#options}

Le composant Image principal peut utiliser deux méthodes pour diffuser des images.

* Le servlet Image adaptative est la valeur par défaut.
* [Diffusion d’images optimisées pour le web](/help/developing/web-optimized-image-delivery.md) est disponible pour AEMaaCS et réduit la taille du téléchargement de 25 % en moyenne.

Ce document décrit le servlet Image adaptative par défaut.

## Présentation {#overview}

Par défaut, le composant d’image utilise le servlet Image adaptative du composant principal pour diffuser des images. La [servlet Image adaptative](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) est en charge du traitement des images et de leur diffusion en continu. Les développeurs peuvent l’utiliser dans le cadre de leur [personnalisation des composants principaux](/help/developing/customizing.md).

## Sélection du rendu {#rendition-selection}

Le servlet d’image adaptative sélectionne automatiquement le rendu le plus approprié à afficher en fonction de la taille du conteneur dans lequel il s’affiche. Le processus de sélection du rendu est le suivant.

1. Le servlet d’image adaptative examine tous les rendus disponibles de la ressource d’image.
1. Il sélectionne uniquement les ressources de même type/MIME de la ressource référencée d’origine.
   * Par exemple, si la ressource d’origine était un fichier PNG, elle ne prendra en compte que les rendus PNG.
1. De ces rendus, elle prend en compte les dimensions et les compare à la taille du conteneur dans lequel l’image doit s’afficher.
   1. Si le rendu est >= à la taille du conteneur, il est ajouté à une liste de rendus candidats.
   1. Si le rendu est &lt; à la taille du conteneur, il n’est pas pris en compte.
   1. Ces critères garantissent que le rendu ne sera pas amélioré, ce qui aurait un impact sur la qualité de l’image.
1. Le servlet d’image adaptative sélectionne ensuite le rendu ayant la plus petite taille de fichier dans la liste des candidats.

## Optimisation de la sélection du rendu {#optimizing-rendition-selection}

La servlet d’image adaptative tente de sélectionner le meilleur rendu pour la taille et le type d’image demandés. Il est recommandé de définir les rendus DAM et les largeurs autorisées des composants Image de façon synchronisée afin que la servlet d’image adaptative effectue le moins de traitement possible.

Cela améliore les performances et évite que certaines images ne soient pas correctement traitées par la bibliothèque de traitement des images sous-jacente.

## Utiliser les derniers en-têtes modifiés {#last-modified}

Les requêtes conditionnelles effectuées par le biais de `Last-Modified` en-tête sont prises en charge par la servlet d’image adaptative, mais la mise en cache de l’en-tête `Last-Modified` [doit être activée dans Dispatcher](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=fr#caching-http-response-headers).

L’exemple de configuration de Dispatcher d’[AEM Project Archetype](/help/developing/archetype/overview.md) contient déjà cette configuration.
