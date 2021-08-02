---
title: Composant de téléchargement
description: Le composant de téléchargement des composants principaux permet la création d’une option de téléchargement sur une page.
role: Architect, Developer, Admin, User
exl-id: 48e7ade0-b849-4d1f-b836-51196e5ac507
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '687'
ht-degree: 100%

---

# Composant de téléchargement{#download-component}

Le composant de téléchargement des composants principaux permet la création d’une option de téléchargement sur une page.

## Utilisation {#usage}

Le composant de téléchargement des composants principaux permet d’inclure une option de téléchargement et sa ressource associée dans une page.

* Les propriétés de l’option de téléchargement peuvent être sélectionnées dans la [boîte de dialogue de configuration](#configure-dialog).
* Les valeurs par défaut du composant de téléchargement peuvent être définies dans la [boîte de dialogue de conception](#design-dialog).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de téléchargement est v1, qui a été introduite avec la version 2.5.0 des composants principaux en février 2019. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant de téléchargement et voir des exemples de ses options de configuration, ainsi que la sortie HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_download).

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant de téléchargement [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_download_v1).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur du contenu de définir l’élément de téléchargement et la façon dont il se comporte et apparaît pour un visiteur sur la page.

![Onglet Ressource de la boîte de dialogue de modification du composant Téléchargement](/help/assets/download-edit-asset.png)

### Onglet Ressources {#asset-tab}

La sélection d’une ressource de téléchargement est très similaire à la fonctionnalité du [composant d’image](image.md) et utilise également la fonctionnalité DAM d’AEM.

* **Télécharger la ressource**
   * Déposez un fichier depuis l’[explorateur de ressources](https://docs.adobe.com/content/help/fr-FR/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) ou appuyez sur l’option **parcourir** pour effectuer un téléchargement à partir d’un système de fichiers local.
   * Appuyez ou cliquez sur **Effacer** pour désélectionner l’image actuellement sélectionnée.
   * Appuyez ou cliquez sur **Modifier** pour [gérer les rendus de la ressource](https://docs.adobe.com/content/help/fr-FR/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) dans l’éditeur de ressources.

### Onglet Propriétés {#properties-tab}

![Onglet Propriétés de la boîte de dialogue de modification du composant Téléchargement](/help/assets/download-edit-properties.png)

* **Titre** : s’affiche sous forme de titre pour l’élément de téléchargement.
   * **Obtenir le titre auprès d’une ressource DAM** : lorsqu’il est sélectionné, le titre est automatiquement renseigné avec celui de la ressource DAM.
* **Description** : s’affiche sous forme de sous-titre descriptif de l’élément de téléchargement.
   * **Obtenir la description auprès d’une ressource DAM** : lorsqu’elle est sélectionnée, la description est automatiquement renseignée avec la description de la ressource DAM.
* **Texte d’action** : s’affiche sous forme de texte d’action pour l’élément de téléchargement.
   * Ce champ est obligatoire lors du téléchargement d’une ressource depuis le système de fichiers.
   * **Afficher en ligne** : lorsque cette option est sélectionnée, le **texte d’action** fourni s’affiche en ligne.
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les options disponibles pour l’auteur du contenu qui utilise le composant de téléchargement.

### Onglet Propriétés {#properties-tab-design}

![Boîte de dialogue de conception du composant Téléchargement](/help/assets/download-design.png)

* **Autoriser le transfert depuis le système de fichiers** : permet à l’auteur du contenu de télécharger une ressource depuis son système de fichiers local comme ressource de téléchargement.
   * La valeur par défaut n’est pas sélectionnée.
* **Type de titre** : élément HTML utilisé pour le titre du composant de téléchargement.
   * Si aucune valeur n’est sélectionnée, la valeur par défaut est H3.
* **Afficher la taille du fichier** : lorsque cette option est sélectionnée, la taille de fichier de la ressource est affichée dans le composant de téléchargement.
   * La valeur par défaut est sélectionnée.
* **Afficher le format du fichier** : lorsque cette option est sélectionnée, le format de fichier de la ressource est affiché dans le composant de téléchargement.
   * La valeur par défaut est sélectionnée.
* **Afficher le nom de fichier** : lorsque cette option est sélectionnée, le nom de fichier de la ressource est affiché dans le composant de téléchargement.
   * La valeur par défaut est sélectionnée.

### Onglet Styles {#styles-tab}

Le composant d’image prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.
