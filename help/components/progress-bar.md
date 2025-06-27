---
title: Composant Barre de progression
description: Le composant Barre de progression représente visuellement la progression par rapport à un objectif
role: Architect, Developer, Admin, User
exl-id: 47afc5a6-ac57-4b6c-92c4-015ca956a20b
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Composant Barre de progression {#progress-bar-component}

Le composant Barre de progression des composants principaux représente visuellement la progression par rapport à un objectif.

{{traditional-aem}}

## Utilisation {#usage}

Le composant Barre de progression permet à l’auteur de contenu de créer facilement une barre de progression en définissant un pourcentage d’achèvement, de façon à disposer d’un affichage intuitif de la progression par rapport à un objectif.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Barre de progression est v1. Elle a été introduite avec la version 2.9.0 des composants principaux en mai 2020 et elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| v1 | Compatible avec la <br>[version 2.17.4](/help/versions.md) et versions antérieures | Compatible | Compatible | Compatible |

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant Barre de progression et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_progressbar_fr).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Barre de progression [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_progress_v1).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

![Boîte de dialogue de modification du composant Barre de progression](/help/assets/progress-bar-edit.png)

* **Achèvement** : progression représentée par un pourcentage
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les styles appliqués au composant Barre de progression.

### Onglet Styles {#styles-tab}

Le composant Barre de progression prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

## Couche de données client Adobe {#data-layer}

Le composant Barre de progression prend en charge la [couche de données client Adobe](/help/developing/data-layer/overview.md).
