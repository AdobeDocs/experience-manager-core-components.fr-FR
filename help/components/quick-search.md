---
title: Composant Recherche rapide
description: Le composant Recherche rapide fournit des fonctionnalités de recherche à un site web et présente les résultats de recherche afin que les visiteurs puissent effectuer des recherches sur le site et filtrer les résultats.
role: Architect, Developer, Admin, User
exl-id: fc40ce1d-e69a-4a40-853e-67a37228271b
source-git-commit: 327c239b02e0aecee878784c918bfa98d960530e
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 100%

---

# Composant Recherche rapide {#quick-search-component}

Le composant Recherche rapide fournit des fonctionnalités de recherche à un site web et présente les résultats de recherche afin que les visiteurs puissent facilement trouver le contenu correspondant et afficher les résultats.

## Utilisation {#usage}

Le composant Recherche rapide permet aux visiteurs du site de rechercher du contenu, d’afficher les résultats en place et de naviguer facilement vers les pages correspondantes. De nouveaux résultats sont extraits dynamiquement lorsque l’utilisateur fait défiler les résultats de la recherche.

La [boîte de dialogue de modification](#edit-dialog) permet à l’auteur de contenu de définir l’emplacement où doit commencer la recherche dans l’arborescence de contenu. À l’aide de la [boîte de dialogue de conception](#design-dialog), l’auteur du modèle peut définir la valeur par défaut pour laquelle la recherche doit commencer dans l’arborescence de contenu, ainsi qu’une taille de jeu de résultats maximale et une durée minimale de recherche.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Recherche rapide est v2, qui a été introduite avec la version 2.18.0 des composants principaux en janvier 2018 et est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | - | Compatible | Compatible |
| [v1](/help/components/v1/quick-search.md) | Compatible avec la <br>[version 2.17.4](/help/versions.md) et versions antérieures. | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

### Détails techniques {#technical-details}

>[!NOTE]
>
>La protection du composant Recherche ou de toute application basée sur AEM par rapport aux attaques DOS doit être implémentée à un niveau supérieur, par exemple à l’aide de `mod_security` sur le Dispatcher.

La documentation technique la plus récente sur le composant Recherche rapide [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_search_v2_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de modification {#edit-dialog}

La boîte de dialogue de modification permet à l’auteur de contenu de définir l’emplacement où doit commencer la recherche dans l’arborescence de contenu.

![Boîte de dialogue de modification du composant Recherche rapide](/help/assets/quick-search-edit.png)

**Rechercher à la racine** - Page racine d’où lancer la recherche. Rechercher à la racine peut être un gabarit principal, une page principale ou une page normale.
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

>[!NOTE]
>
>Si la **Racine de la recherche** n’est pas configurée ou ne peut pas être résolue, la recherche rapide effectue par défaut une recherche sous la page active.

## Boîte de dialogue de conception {#design-dialog}

À l’aide de la boîte de dialogue de conception, l’auteur du modèle peut définir la valeur par défaut pour laquelle, dans l’arborescence de contenu, la recherche doit commencer, ainsi qu’une taille de jeu de résultats maximale et la longueur minimale du terme. La boîte de dialogue de conception permet à l’auteur du modèle de définir quelles options de mise en forme de texte sont disponibles pour les auteurs de contenu.

### Onglet Propriétés {#properties-tab}

![Boîte de dialogue de conception du composant Recherche rapide](/help/assets/quick-search-design.png)

* **Rechercher à la racine**
La valeur par défaut de la racine de recherche lorsqu’un auteur de contenu place le composant Recherche rapide sur une page de contenu.
* **Taille des résultats**
Le nombre maximal de résultats extraits par une requête de recherche.
* **Longueur minimale du terme de recherche**
Longueur minimale du terme de recherche pour lancer la recherche.

>[!NOTE]
>
>La **Taille des résultats** et la **Longueur minimum du terme de recherche** ne peuvent être définies qu’en mode conception et, par conséquent, au niveau du modèle, ce qui signifie que les auteurs de contenu ne peuvent pas modifier ces valeurs.

>[!CAUTION]
>
>La **Taille des résultats** et la **Longueur minimale du terme de recherche** peuvent avoir un impact sur les performances si elles sont trop élevées ou trop faibles, respectivement.

### Onglet Styles {#styles-tab}

Le composant Recherche rapide prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.
