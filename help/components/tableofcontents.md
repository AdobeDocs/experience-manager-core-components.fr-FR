---
title: Composant Table des matières
description: Le composant Table des matières crée une table des matières d’après les titres du contenu de votre page, ce qui permet à vos lecteurs de parcourir rapidement la page.
role: Architect, Developer, Admin, User
exl-id: 006adde2-ebff-4e74-8e79-325cccd43e8f
source-git-commit: 394a8b968d7bcde7e766ed719c5914ec5cb60744
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 22%

---

# Composant Table des matières {#table-of-contents-component}

Le composant Table des matières crée une table des matières d’après les titres du contenu de votre page, ce qui permet à vos lecteurs de parcourir rapidement la page.

## Utilisation {#usage}

Le composant Table des matières permet aux visiteurs du site de parcourir rapidement le contenu de votre page par le biais d’une table des matières générée de manière efficace en fonction des titres du contenu de la page.

* La table des matières est générée côté serveur.
* Il est entièrement mis en cache par Dispatcher pour une diffusion rapide.
* Il fonctionne avec tous les composants de la page, et pas seulement avec les composants principaux.

Le [Modifier la boîte de dialogue](#edit-dialog) permet à l’auteur de contenu de définir la plage de titres à utiliser dans la table des matières. En utilisant la variable [boîte de dialogue de conception](#design-dialog), l’auteur du modèle peut définir la valeur par défaut des titres lorsqu’un auteur de contenu ajoute un composant Table des matières à une page et limite les titres inclus dans la table des matières en fonction des noms de classe.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Table des matières est v1, qui a été introduite avec la version 2.20.0 des composants principaux en mai 2022. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant Table des matières et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la page [Bibliothèque de composants](https://adobe.com/go/aem_cmp_library_tableofcontents).

### Détails techniques {#technical-details}

Documentation technique la plus récente sur le composant Table des matières [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_tableofcontents_v1).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de modification {#edit-dialog}

La boîte de dialogue de modification permet à l’auteur de contenu de définir les plages de niveaux de titre que le composant Table of Contents doit afficher sous la forme d’une table des matières.

![Boîte de dialogue de modification du composant Table des matières](/help/assets/tableofcontents-edit.png)

**Type de liste** - Cette option définit si la liste doit être une liste à puces ou une liste numérotée.
* **Niveau de départ du titre** - Cette option définit le niveau de titres le plus élevé que le composant Table des matières doit générer.
* **Niveau d’arrêt du titre** - Cette option définit le niveau de titres le plus bas que le composant Table des matières doit générer.
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

## Boîte de dialogue de conception {#design-dialog}

À l’aide de la boîte de dialogue de conception, l’auteur du modèle peut définir la valeur par défaut pour la plage de titres du composant Table des matières et limiter les titres inclus dans la table des matières en fonction des noms de classe.

### Onglet Propriétés {#properties-tab}

![Boîte de dialogue de conception du composant Recherche rapide](/help/assets/tableofcontents-design.png)

* **Restreindre le type de liste** - Cette option définit le type de liste que le composant va générer. La sélection de cette option limite la capacité de l’auteur du contenu à choisir un type de liste différent.
* **Limitation du niveau de départ** - Cette option définit le niveau de titre le plus élevé que l’auteur du contenu peut sélectionner pour définir la table des matières.
* **Limitation du niveau d’arrêt** - Cette option définit le niveau de titre le plus bas que l’auteur du contenu peut sélectionner pour définir la table des matières.
* **Inclure les noms de classe** - Si cette option est définie, seuls les titres avec les noms de classe spécifiés ou contenus dans des éléments des noms de classe spécifiés seront pris en compte par le composant Table of Contents.
   * Appuyez ou cliquez sur le bouton **Ajouter** pour ajouter un ou plusieurs noms de classe.
   * Appuyez ou cliquez sur le bouton **Supprimer** en regard d’un nom de classe pour le supprimer.
* **Ignorer les noms de classe** - Si cette option est définie, les titres avec les noms de classe spécifiés ou contenus dans les éléments des noms de classe spécifiés seront ignorés par le composant Table of Contents.
   * Appuyez ou cliquez sur le bouton **Ajouter** pour ajouter un ou plusieurs noms de classe.
   * Appuyez ou cliquez sur le bouton **Supprimer** en regard d’un nom de classe pour le supprimer.

### Onglet Styles {#styles-tab}

Le composant Table des matières prend en charge l’AEM [Système de style](/help/get-started/authoring.md#component-styling).

## Couche de données client Adobe {#data-layer}

Le composant Table des matières prend en charge la variable [Adobe de la couche de données client.](/help/developing/data-layer/overview.md)
