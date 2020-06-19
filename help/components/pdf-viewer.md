---
title: Composant du lecteur PDF
description: Le composant PDF Viewer permet l’affichage d’un document PDF.
translation-type: tm+mt
source-git-commit: b08fc5ec49126f7be19b7433a3d71de877d9e442
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 13%

---


# Composant du lecteur PDF {#pdf-viewer-component}


Le composant Core Component PDF Viewer permet l’inclusion d’un document PDF sur une page.

## Utilisation {#usage}

Le composant Core Component PDF Viewer incorpore une visionneuse pour afficher les fichiers PDF stockés en tant que fichiers sur la page.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant PDF Viewer est la version 1, introduite avec la version 2.10.0 des composants principaux en juin 2020. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

To experience the PDF Viewer Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_pdfviewer).

## Détails techniques {#technical-details}

The latest technical documentation about the PDF Viewer Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur du contenu de définir la visionneuse et son comportement et son apparence pour un visiteur de la page.

### Configuration Tab {#configuration-tab}

L’onglet Configuration permet à l’auteur de définir le PDF à afficher. Le chemin d’accès peut être défini comme un actif dans AEM ou comme un chemin absolu vers une autre ressource.

![Onglet Configuration de la boîte de dialogue Modifier du composant PDF Viewer](/help/assets/pdf-viewer-edit-configuration.png)

### Onglet Personnaliser {#customize-tab}

L’onglet Personnaliser permet à l’auteur de définir les options disponibles dans la visionneuse pour le lecteur et la manière dont la visionneuse doit être présentée.

![Personnaliser l’onglet de la boîte de dialogue de modification du composant PDF Viewer](/help/assets/pdf-viewer-edit-customize.png)

Le nombre d’options disponibles dépend du **type** sélectionné.

* [Fenêtre](#full-window) complète : la zone d&#39;affichage est affichée dans le navigateur complet. Il convient particulièrement aux applications d&#39;enregistrement et de productivité.
* [Conteneur](#sized-container) de taille : la zone d&#39;affichage est affichée dans le navigateur complet. Il convient particulièrement aux applications d&#39;enregistrement et de productivité.
* [En ligne](#in-line) : toutes les pages PDF affichées en ligne dans une page Web. Il convient le mieux aux applications de lecture.

#### Fenêtre complète {#full-window}

La zone d’affichage s’affiche dans le navigateur complet. Il convient particulièrement aux applications d&#39;enregistrement et de productivité.

![Personnaliser l’option de fenêtre de l’onglet dans la boîte de dialogue de modification du composant PDF Viewer](/help/assets/pdf-viewer-edit-customize-full.png)

* **Mode** de Vue par défaut : comment le lecteur peut-il être adapté à la page où il est affiché ?
   * Page entière
   * Pleine largeur
* **Plein écran** - Lorsqu’il est activé, le lecteur prend la pleine hauteur/largeur de la fenêtre d’affichage.
* **Outils** d&#39;annotation : lorsqu&#39;ils sont activés, les outils d&#39;annotation sont disponibles.
* **Panneau** Main gauche - Lorsqu&#39;il est activé, le panneau Main gauche s&#39;affiche.
* **Télécharger un fichier PDF** : lorsque cette option est activée, le bouton de téléchargement s’affiche.
* **Imprimer un fichier PDF** : lorsque cette option est activée, le bouton Imprimer s’affiche.
* **Contrôles** de page : bascule le comportement des contrôles de page.
   * Ancrage
   * Déplacer

#### Conteneur dimensionné {#sized-container}

La zone d’affichage s’affiche dans le navigateur complet. Il convient particulièrement aux applications d&#39;enregistrement et de productivité.

![Personnaliser l’option de conteneur de la taille d’une tabulation dans la boîte de dialogue de modification du composant PDF Viewer](/help/assets/pdf-viewer-edit-customize-sized-container.png)

* **Plein écran** - Lorsqu’il est activé, le lecteur prend la pleine hauteur/largeur de la fenêtre d’affichage.
* **Télécharger un fichier PDF** : lorsque cette option est activée, le bouton de téléchargement s’affiche.
* **Imprimer un fichier PDF** : lorsque cette option est activée, le bouton Imprimer s’affiche.
* **Contrôles** de page : bascule le comportement des contrôles de page.
   * Ancrage
   * Déplacer

#### En ligne {#in-line}

Toutes les pages PDF affichées en ligne dans une page Web. Il convient le mieux aux applications de lecture.

![Personnaliser l’option de conteneur de la taille d’une tabulation dans la boîte de dialogue de modification du composant PDF Viewer](/help/assets/pdf-viewer-edit-customize-inline.png)

* **Télécharger un fichier PDF** : lorsque cette option est activée, le bouton de téléchargement s’affiche.
* **Imprimer un fichier PDF** : lorsque cette option est activée, le bouton Imprimer s’affiche.

## Boîte de dialogue de conception {#design-dialog}

Il n’existe pas de boîte de dialogue de conception pour le composant PDF Viewer.
