---
title: Composant Recherche optimisée par l'IA de contenu
description: Le composant Recherche optimisée par l'IA de contenu fournit aux visiteurs de votre site une recherche générée optimisée par l’IA.
role: Developer, Admin, User
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: e721e8b9469646300432b87d42bfb742aaf5f3fb
workflow-type: tm+mt
source-wordcount: 805
ht-degree: 16%

---


# Composant Recherche optimisée par l&#39;IA de contenu {#content-ai-search-component}

Le composant Recherche optimisée par l&#39;IA de contenu fournit aux visiteurs de votre site une recherche générée optimisée par l’IA.

{{traditional-aem}}

## Utilisation {#usage}

Le composant Recherche optimisée par l&#39;IA de contenu permet aux visiteurs de rechercher un [Content Source](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources) directement à partir d’une page et éventuellement d’afficher un résumé des résultats généré par l’IA. Il associe une zone de recherche de texte intégral/sémantique standard à un panneau **Afficher le résumé généré par l’IA** pouvant être activé/désactivé, optimisé par l’IA dédiée au contenu d’AEM.

La boîte de dialogue [Modifier](#edit-dialog) permet à l’auteur de contenu de définir la portée du contenu de la recherche, le comportement de la recherche et les paramètres génératifs. Il n’existe pas de boîte de dialogue de conception, car aucun paramètre n’est disponible au niveau du modèle.

>[!NOTE]
>
>Pour utiliser le composant Recherche optimisée par l&#39;IA de contenu, vous devez avoir accès à un Source IA dédiée au contenu et votre administrateur doit avoir activé le composant pour votre projet. Voir le document [Configuration du composant Recherche optimisée par l&#39;IA de contenu](/help/developing/ai-search.md) pour plus d’informations.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Recherche optimisée par l&#39;IA de contenu est v1. Celle-ci a été introduite avec la version 2.32.0 des composants principaux en juillet 2026. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| v1 | - | - | - | En cours |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document [Versions des composants principaux.](/help/versions.md)

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant Recherche optimisée par l&#39;IA de contenu et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants.](https://adobe.com/go/aem_cmp_library_ai_search)

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Recherche optimisée par l&#39;IA de contenu [se trouve sur GitHub.](https://adobe.com/go/aem_cmp_tech_ai_search_v1).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation relative au développement des composants principaux](/help/developing/overview.md).

## Boîte de dialogue de modification {#edit-dialog}

La boîte de dialogue de modification permet à l’auteur de contenu de définir la portée du contenu de la recherche, le comportement de la recherche et les paramètres de génération. Il n’existe pas de boîte de dialogue de conception, car aucun paramètre n’est disponible au niveau du modèle.

### Onglet Portée du contenu {#content-scope}

![Onglet Portée du contenu de la boîte de dialogue de modification](/help/assets/content-ai-search-edit-content-scope.png)

* **ID** - Cette option permet de contrôler l’identifiant unique du composant dans l’HTML et dans la [couche de données.](/help/developing/data-layer/overview.md)
  * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
  * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
  * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.
* **Type de Source de contenu** - Ce champ définit le type de source de contenu. La sélection d’un type renseigne la liste déroulante Source de contenu **avec les sources correspondantes.**
  * **ACQUISITION** - Valeur par défaut utilisée pour les sources d’accès public et anonyme indexées via un pipeline d’explore/d’acquisition
  * **AEM_AUTHOR** - Source côté IA dédiée au contenu dont le contenu a été ingéré à partir d’une instance d’auteur AEM
  * **AEM_PUBLISH** -Source côté IA dédiée au contenu dont le contenu a été ingéré à partir d’une instance de publication AEM
  * **PERSONNALISÉ** - Une source enregistrée en dehors des pipelines d’ingestion d’AEM
* **Sources de contenu** - Définit le Source de contenu dans lequel ce composant effectue une recherche.
  * Les entrées disponibles correspondent aux sources de contenu qui existent déjà et qui sont **disponibles** et correspondent également au type défini dans **Type de Source de contenu**
  * Pour plus d’informations, consultez le document [Configurer et gérer vos sources d’IA dédiée au contenu](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources).

### Onglet Comportement de recherche {#search-behavior}

![Onglet Comportement de recherche de la boîte de dialogue de modification](/help/assets/content-ai-search-edit-search-behavior.png)

* **Disposition des résultats** - Cette option définit la manière dont les résultats de recherche sont affichés pour le visiteur.
  * **Cartes** - Cette option affiche les résultats sous forme de grille.
  * **Liste** - Cette option affiche les résultats sous forme de liste.
* **Taille des résultats** - Définit le nombre de résultats récupérés par requête de recherche.
  * La valeur par défaut est `12`.
  * Les visiteurs peuvent charger des résultats supplémentaires lorsque d’autres correspondances sont disponibles.
* **Texte d’espace réservé** - Il s’agit du texte affiché dans le champ de saisie de recherche vide avant que le visiteur ne saisisse une requête.

### Onglet Recherche générative {#generative-search}

![Onglet Recherche générative de la boîte de dialogue de modification](/help/assets/content-ai-search-edit-generative-search.png)

* **Afficher le bouton (bascule) du résumé génératif aux visiteurs** - Lorsque cette option est décochée, les visiteurs ne peuvent pas modifier si le résumé de l’IA s’affiche.
  * La valeur par défaut est activée.
* **Afficher le résumé génératif par défaut** - Cette option contrôle l’état par défaut du bouton (bascule) du côté des visiteurs pour le résumé généré par l’IA.
  * La valeur par défaut est activée.
* **Basculement d’erreur GenSearch** - Définit le comportement ou l’erreur de la recherche.
  * **Résultats uniquement (masquer l’erreur)** - En cas d’erreur, afficher uniquement les résultats renvoyés, et non le bouton d’erreur et d’absence de reprise. Il s’agit de la valeur par défaut.
  * **Afficher l’erreur avec une nouvelle tentative** - En cas d’erreur, afficher l’erreur avec un bouton de reprise.
  * **Afficher le message d’erreur uniquement** - En cas d’erreur, afficher uniquement le message d’erreur, aucun résultat.
