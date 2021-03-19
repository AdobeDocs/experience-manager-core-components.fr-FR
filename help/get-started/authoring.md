---
title: Création à l’aide des composants principaux
description: 'Dans AEM, les composants sont les éléments structurels qui constituent le contenu des pages créées : les composants principaux offrent une fonctionnalité de création flexible et riche en fonctionnalités.'
role: Architecte, Développeur, Administrateur, Professionnel
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 99%

---


# Création à l’aide des composants principaux

Dans Adobe Experience Manager, les composants sont des éléments structurels qui constituent le contenu des pages en cours de création.

Les composants principaux offrent une fonctionnalité de création flexible et riche en fonctionnalités. Le [site de référence WKND](https://wknd.site) illustre comment les composants principaux peuvent être utilisés pour mettre en œuvre une expérience web riche.

Pour tester les composants principaux et consulter des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library).

Pour une présentation plus détaillée et plus orientée vers les développeurs de l’implémentation des composants principaux dans un projet AEM utilisant l’[archétype de projet AEM](/help/developing/archetype/overview.md), consultez [le tutoriel WKND.](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

>[!NOTE]
>
>Les auteurs ne peuvent pas disposer immédiatement de ces composants principaux. En effet, l’[équipe de développement doit d’abord les intégrer dans leur environnement](/help/get-started/using.md). Une fois intégrés, ils peuvent être rendus disponibles et préconfigurés dans l’[éditeur de modèles](https://docs.adobe.com/content/help/fr-FR/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!CAUTION]
>
>Les composants principaux [requièrent AEM 6.4 ou version ultérieure](/help/versions.md), ainsi que l’utilisation de [modèles modifiables](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html). Ils ne fonctionnent pas avec l’interface utilisateur classique ni avec les modèles statiques.

## Création à l’aide des composants principaux {#authoring-with-core-components}

En tant qu’auteur, vous remarquerez que les composants principaux présentent quelques avantages. En voici un aperçu :

* Simples d’utilisation et bien intégrés à l’[éditeur de page](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html)

* Riches en fonctionnalités pour répondre à de nombreux cas d’utilisation, comme illustré sur le [site de référence WKND](https://wknd.site), ainsi que dans la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library)

* [Préconfigurables](#pre-configuring-core-components) afin de définir les fonctionnalités disponibles pour les auteurs de pages au moyen de l’[éditeur de modèles](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

* Conçus selon les [consignes d’accessibilité](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html)

* Conçus pour prendre en charge la [mise en page réactive](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html)

* Conçus pour prendre en charge la [localisation facile](localization.md)

Les composants sont disponibles dans l’onglet **Composants** du panneau latéral de l’éditeur de page lors de la [modification d’une page](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html).

Les composants sont regroupés selon des catégories appelées groupes de composants afin de les organiser et de les filtrer facilement. Le nom du groupe de composants s’affiche avec le composant dans l’[explorateur de composants](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html) et il est également possible de filtrer par groupe pour trouver facilement le composant approprié.

>[!NOTE]
>
>Les composants principaux sont par défaut associés à un groupe masqué et ne sont pas visibles dans l’explorateur de composants.
>
>Ajoutez les composants requis à un groupe visible ou personnalisez-les pour qu’ils soient disponibles pour les auteurs.

## Préconfiguration des composants principaux {#pre-configuring-core-components}

La configuration des composants de base a été la tâche d’un développeur. Toutefois, avec les composants principaux, un auteur de modèles peut maintenant configurer plusieurs fonctionnalités via l’éditeur de modèles.

Par exemple, si un composant d’image n’autorise pas le chargement d’images à partir du système de fichiers ou si un composant textuel autorise uniquement la mise en forme des paragraphes, ces fonctions peuvent être activées ou désactivées en un seul clic.

Pour plus d’informations, voir [Création de modèles de page](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

### Boîtes de dialogue de modification et de conception {#edit-and-design-dialogs}

Les composants principaux pouvant être préconfigurés par les auteurs de modèles pour définir les options autorisées dans le cadre d’un modèle, puis configurés par l’auteur de la page pour définir le contenu réel de la page, chaque composant peut avoir des options dans deux boîtes de dialogue différentes.

|  | Description | Éléments contrôlés | Exemples |
|--- |--- |--- |--- |
| **Boîte de dialogue de modification** | Options qu’un **auteur de page** peut modifier lors de l’édition normale des pages pour les composants placés. | Contenu affiché par le composant et mode d’affichage final sur la page. | Mise en forme du texte du contenu, rotation d’une image sur une page. |
| **Boîte de dialogue de conception** | Options qu’un **auteur de modèles** peut modifier lors de la configuration d’un modèle de page. | Options disponibles pour l’auteur de la page lors de l’édition du composant | Options de mise en forme de texte disponibles, options d’image statiques disponibles |

### Style des composants {#component-styling}

Les styles de la plupart des composants principaux peuvent être définis à l’aide du système de style AEM.

* Un auteur de modèles peut définir les styles disponibles pour un composant particulier dans la boîte de dialogue de conception de ce composant.
* L’auteur du contenu peut ensuite choisir les styles à appliquer lors de l’ajout du composant et la création de contenu.

Pour plus d’informations, consultez la documentation [Système de style](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/style-system.html).

## Références pour les développeurs {#developer-resources}

Pour obtenir des informations techniques sur les composants principaux, voir la documentation pour les développeurs [Développement des composants principaux](/help/developing/overview.md).
