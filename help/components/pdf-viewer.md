---
title: Composant Visionneuse PDF
description: Le composant Visionneuse PDF permet l’affichage d’un document PDF.
role: Architect, Developer, Admin, User
exl-id: deb635f5-2b73-4e7a-9838-3a941e39e898
source-git-commit: 9767a3a10cb9a77f385edc0ac3fb00096c0087af
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 99%

---

# Composant Visionneuse PDF {#pdf-viewer-component}

Le composant Visionneuse PDF des composants principaux permet l’inclusion d’un document PDF sur une page.

## Utilisation {#usage}

Le composant Visionneuse PDF des composants principaux incorpore une visionneuse pour afficher les fichiers PDF stockés en tant que ressources sur la page.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Visionneuse PDF est v1, introduite avec la version 2.10.0 des composants principaux en juin 2020. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible avec<br>[version 2.17.4](/help/versions.md) et précédent | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant Visionneuse PDF et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_pdfviewer_fr).

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Visionneuse PDF [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

>[!NOTE]
>
>Le composant Visionneuse PDF utilise les [API Document Services d’Adobe](https://www.adobe.io/apis/documentcloud/dcsdk.html) et nécessite que votre administrateur configure une [configuration basée sur le contexte](/help/developing/context-aware-configs.md) pour utiliser ces services. Consultez la documentation technique du composant pour [plus de détails sur cette configuration.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur du contenu de définir la visionneuse et la façon dont elle se comporte et apparaît pour un visiteur sur la page.

### Onglet Configuration {#configuration-tab}

L’onglet Configuration permet à l’auteur de définir le PDF à afficher. Le chemin d’accès peut être défini sous la forme d’une ressource dans AEM ou d’un chemin absolu vers une autre ressource.

![Onglet Configuration de la boîte de dialogue Modifier du composant Visionneuse PDF](/help/assets/pdf-viewer-edit-configuration.png)

### Onglet Personnaliser {#customize-tab}

L’onglet Personnaliser permet à l’auteur de définir les options disponibles dans la visionneuse pour le lecteur et la manière dont elle doit être présentée.

![Onglet Personnaliser de la boîte de dialogue de modification du composant Visionneuse PDF](/help/assets/pdf-viewer-edit-customize.png)

Le nombre d’options disponibles dépend du **type** sélectionné.

* [Fenêtre complète](#full-window) : la zone d’affichage s’affiche dans le navigateur complet. Cela convient particulièrement aux applications de stockage et de productivité.
* [Conteneur dimensionné](#sized-container) : la zone d’affichage s’affiche dans le navigateur complet. Cela convient particulièrement aux applications de stockage et de productivité.
* [En ligne](#in-line) : toutes les pages PDF affichées en ligne dans une page web. Cela convient particulièrement aux applications de lecture.

#### Fenêtre complète {#full-window}

La zone d’affichage s’affiche dans le navigateur complet. Cela convient particulièrement aux applications de stockage et de productivité.

![Option Fenêtre complète de l’onglet Personnaliser de la boîte de dialogue de modification du composant Visionneuse PDF](/help/assets/pdf-viewer-edit-customize-full.png)

* **Mode d’affichage par défaut** : manière dont la visionneuse est adaptée à la page sur laquelle elle est affichée.
   * Page entière
   * Pleine largeur
* **Plein écran** : lorsque cette option est activée, la visionneuse prend la pleine hauteur/largeur de la fenêtre d’affichage.
* **Outils d’annotation** : lorsque cette option est activée, les outils d’annotation sont disponibles.
* **Panneau de gauche** : lorsque cette option est activée, le panneau de gauche s’affiche.
* **Télécharger le PDF** : lorsque cette option est activée, le bouton de téléchargement s’affiche.
* **Imprimer le PDF** : lorsque cette option est activée, le bouton d’impression s’affiche.
* **Contrôles de page** : fait basculer le comportement des contrôles de page.
   * Ancrer
   * Détacher

#### Conteneur dimensionné {#sized-container}

La zone d’affichage s’affiche dans le navigateur complet. Cela convient particulièrement aux applications de stockage et de productivité.

![Option Conteneur dimensionné de l’onglet Personnaliser de la boîte de dialogue de modification du composant Visionneuse PDF](/help/assets/pdf-viewer-edit-customize-sized-container.png)

* **Plein écran** : lorsque cette option est activée, la visionneuse prend la pleine hauteur/largeur de la fenêtre d’affichage.
* **Télécharger le PDF** : lorsque cette option est activée, le bouton de téléchargement s’affiche.
* **Imprimer le PDF** : lorsque cette option est activée, le bouton d’impression s’affiche.
* **Contrôles de page** : fait basculer le comportement des contrôles de page.
   * Ancrer
   * Détacher

#### En ligne {#in-line}

Toutes les pages PDF affichées en ligne dans une page web. Cela convient particulièrement aux applications de lecture.

![Option Conteneur dimensionné de l’onglet Personnaliser de la boîte de dialogue de modification du composant Visionneuse PDF](/help/assets/pdf-viewer-edit-customize-inline.png)

* **Télécharger le PDF** : lorsque cette option est activée, le bouton de téléchargement s’affiche.
* **Imprimer le PDF** : lorsque cette option est activée, le bouton d’impression s’affiche.

## Boîte de dialogue de conception {#design-dialog}

Il n’existe pas de boîte de dialogue de conception pour le composant Visionneuse PDF.
