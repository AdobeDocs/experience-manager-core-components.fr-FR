---
title: Composant de barre de progression
description: Le composant de la barre de progression représente visuellement la progression vers un objectif
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 22%

---


# Composant de barre de progression {#progress-bar-component}

Le composant de la barre de progression du composant principal représente visuellement la progression vers un objectif.

## Utilisation {#usage}

Le composant de la barre de progression permet à l’auteur du contenu de créer facilement une barre de progression en définissant un pourcentage d’achèvement, ce qui permet d’afficher visuellement intuitivement les progrès vers un objectif.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de barre de progression est la version 1, qui a été introduite avec la version 2.9.0 des composants principaux en mai 2020, et est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatible | Compatible | Compatible |

## Exemple de sortie de composant {#sample-component-output}

To experience the Progress Bar Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_progress).

### Détails techniques {#technical-details}

The latest technical documentation about the Progress Bar Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_progress_v1).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

![Boîte de dialogue de modification du composant de la barre de progression](/help/assets/progress-bar-edit.png)

* **Achèvement** - Progression représentée par un pourcentage
* **ID** : cette option permet de contrôler l&#39;identifiant unique du composant dans le code HTML et dans la couche [de](/help/developing/data-layer/overview.md)données.
   * Si rien n’est indiqué, un identifiant unique est automatiquement généré et peut être trouvé en examinant la page qui en résulte.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les styles appliqués au composant de la barre de progression.

### Onglet Styles {#styles-tab}

The Progress Bar Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).
