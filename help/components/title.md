---
title: Composant du titre
description: Le composant Titre des composants principaux est un composant d’en-tête de section qui comporte des fonctions d’édition statique.
role: Architect, Developer, Admin, User
exl-id: 393af72c-549f-4609-afb0-2712f827b549
source-git-commit: 16930ccaa281f9d9c4ddbb890d4222e128557580
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 100%

---

# Composant du titre{#title-component}

Le composant Titre des composants principaux est un composant d’en-tête de section qui comporte des fonctions d’édition statique.

## Utilisation {#usage}

Le composant du titre est conçu pour être utilisé comme titre ou en-tête d’une section de contenu. Les niveaux d’en-tête disponibles peuvent être définis par l’auteur du modèle dans la [boîte de dialogue de conception](#design-dialog). L’éditeur de contenu peut sélectionner les niveaux d’en-têtes disponibles dans la [boîte de dialogue de modification](#edit-dialog). Pour plus de commodité, une simple modification statique du texte d’en-tête est également disponible.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Titre est v3, qui a été introduite avec la version 2.18.0 des composants principaux en février 2022. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v3 | - | Compatible | Compatible |
| [v2](v2/title.md) | Compatible | Compatible | Compatible |
| [v1](v1/title-v1.md) | Compatible | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant du titre et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_title_fr).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Titre [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_title_v2_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de modification {#edit-dialog}

La boîte de dialogue de modification permet à l’auteur de contenu de définir le texte du titre et de sélectionner le niveau de titre.

* **Titre** : si ce champ est vide, le titre de la page est utilisé.
* **Type/Taille** : définit le niveau d’en-tête du titre.
* **Lien** : définit le contenu auquel le titre sera associé. Il peut s’agir d’un chemin d’accès à une page de contenu, d’une URL externe ou d’une ancre de page.
* **Ouvrir le lien dans un nouvel onglet** : lorsque cette option est cochée, le lien s’ouvre dans un nouvel onglet du navigateur.
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

![Boîte de dialogue de modification du composant Titre](/help/assets/title-edit.png)

L’éditeur statique peut également être utilisé pour modifier le texte du composant du titre.

![Modification statique du composant Titre](/help/assets/title-edit-inline.png)

### Onglet Styles {#styles-tab-edit}

Le composant Titre prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

Utilisez la liste déroulante pour sélectionner les styles à appliquer au composant. Les sélections effectuées dans la boîte de dialogue de modification ou dans la barre d’outils du composant ont le même effet.

Pour que le menu déroulant soit disponible, les styles doivent être configurés pour ce composant dans la [boîte de dialogue de conception](#design-dialog).

![Onglet Styles de la boîte de dialogue de modification du composant Titre](/help/assets/title-edit-styles.png)

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir le niveau d’en-tête par défaut que les composants de titre auront une fois créés par les auteurs de contenu.

### Onglet Tailles {#sizes-tab}

![Boîte de dialogue de conception du composant Titre](/help/assets/title-design.png)

* **Types/tailles autorisés pour les auteurs** : Activez ou désactivez les types d’en-têtes qui seront disponibles pour les auteurs de contenu lorsqu’ils utilisent le composant du titre.
* **Type par défaut/taille** - Définissez le type d’en-tête qui sera automatiquement attribué lorsqu’un auteur de contenu ajoute le composant du titre à une page.
* **Désactiver le lien** - Désactivez la prise en charge des liens dans le composant du titre pour interdire aux auteurs de contenu de lier des titres.

### Onglet Styles {#styles-tab}

Le composant Titre prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

## Couche de données client Adobe {#data-layer}

Le composant Titre prend en charge la [couche de données client Adobe](/help/developing/data-layer/overview.md).
