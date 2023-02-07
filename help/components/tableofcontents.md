---
title: Composant Table des matières
description: Le composant Table des matières permet de créer une table des matières basée sur les titres du contenu de votre page. Vos lecteurs peuvent ainsi naviguer rapidement dans la page.
role: Architect, Developer, Admin, User
exl-id: 006adde2-ebff-4e74-8e79-325cccd43e8f
source-git-commit: 8beae61676340e8aafaee469018d865ea7ed934e
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 95%

---

# Composant Table des matières {#table-of-contents-component}

Le composant Table des matières permet de créer une table des matières basée sur les titres du contenu de votre page. Vos lecteurs peuvent ainsi naviguer rapidement dans la page.

## Utilisation {#usage}

Le composant Table des matières offre aux visiteurs du site la possibilité de naviguer rapidement dans le contenu de votre page, grâce à une table des matières générée efficacement à partir des titres du contenu des pages.

* La table des matières est générée côté serveur.
* Elle est entièrement mise en cache par le Dispatcher pour une diffusion rapide.
* Elle fonctionne avec tous les composants de la page, et pas seulement avec les composants principaux.

La [boîte de dialogue de modification](#edit-dialog) permet au créateur du contenu de définir les différents niveaux de titres qui doivent être repris dans la table des matières. À l’aide de la [boîte de dialogue de conception](#design-dialog), le créateur du modèle peut définir la valeur par défaut des titres lorsqu’un créateur de contenu ajoute un composant Table des matières à une page. Il peut également restreindre les titres inclus dans la table des matières en fonction des noms de classe.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Table des matières est v1. Elle a été introduite avec la version 2.20.0 des composants principaux en mai 2022 et elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

>[!NOTE]
>
>Sur AEM as a Cloud Service, votre administrateur doit activer un filtre pour le composant afin qu’il effectue le rendu du contenu du composant.
>
>[Consultez la documentation GitHub du composant.](https://adobe.com/go/aem_cmp_tech_tableofcontents_v1) pour plus d’informations.

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Table des matières [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_tableofcontents_v1).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de modification {#edit-dialog}

La boîte de dialogue de modification permet au créateur du contenu de définir les différentes plages de niveaux de titres qui doivent être repris dans la table des matières par le composant Table des matières.

![Boîte de dialogue de modification du composant Table des matières](/help/assets/tableofcontents-edit.png)

**Type de liste** : cette option définit si la liste doit être une liste à puces ou une liste numérotée.
* **Niveau de début du titre** : cette option définit le niveau le plus élevé des titres que le composant Table des matières doit reprendre.
* **Niveau d’arrêt du titre** : cette option définit le niveau le plus bas des titres que le composant Table des matières doit reprendre.
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

## Boîte de dialogue de conception {#design-dialog}

À l’aide de la boîte de dialogue de conception, le créateur du modèle peut définir la valeur par défaut de la plage de titres du composant Table des matières et restreindre les titres inclus dans la table des matières en fonction des noms de classe.

### Onglet Propriétés {#properties-tab}

![Boîte de dialogue de conception du composant Recherche rapide](/help/assets/tableofcontents-design.png)

* **Restreindre le type de liste** : cette option définit le type de liste que le composant va générer. La sélection de cette option restreint la capacité du créateur du contenu à choisir un autre type de liste.
* **Restreindre le niveau de départ** : cette option définit le niveau de titre le plus élevé que le créateur de contenu peut sélectionner pour définir la table des matières.
* **Restreindre le niveau d’arrêt** : cette option définit le niveau de titre le plus bas que le créateur de contenu peut sélectionner pour définir la table des matières.
* **Inclure les noms de classe** : si cette option est définie, seuls les titres ayant les noms de classe spécifiés ou contenus dans des éléments des noms de classe spécifiés seront pris en compte par le composant Table des matières.
   * Appuyez ou cliquez sur l’icône **Ajouter** pour ajouter un ou plusieurs noms de classe.
   * Appuyez ou cliquez sur l’icône **Supprimer** en regard d’un nom de classe pour le supprimer.
* **Ignorer les noms de classe** : si cette option est définie, les titres portant les noms de classe spécifiés ou contenus dans des éléments des noms de classe spécifiés seront ignorés par le composant Table des matières.
   * Appuyez ou cliquez sur l’icône **Ajouter** pour ajouter un ou plusieurs noms de classe.
   * Appuyez ou cliquez sur l’icône **Supprimer** en regard d’un nom de classe pour le supprimer.

### Onglet Styles {#styles-tab}

Le composant Table des matières prend en charge le [Système de style](/help/get-started/authoring.md#component-styling) AEM.

## Couche de données client Adobe {#data-layer}

Le composant Table des matières prend en charge la [Couche de données client Adobe](/help/developing/data-layer/overview.md).
