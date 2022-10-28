---
title: Composant du titre de l’email
description: Le composant Titre du courrier électronique est un composant d’en-tête de section pour vos courriers électroniques qui permet d’effectuer des modifications statiques.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 51%

---


# Composant du titre de l’email {#email-title-component}

Le composant Titre du courrier électronique est un composant d’en-tête de section pour vos courriers électroniques qui permet d’effectuer des modifications statiques.

## Utilisation {#usage}

Le composant Titre du courrier électronique est conçu pour être utilisé comme titre ou en-tête d’une section d’un courrier électronique.

* Les niveaux d’en-tête disponibles peuvent être définis par l’auteur du modèle dans la [boîte de dialogue de conception.](#design-dialog)
* L’auteur du contenu peut sélectionner les niveaux d’en-têtes disponibles dans la variable [modifier la boîte de dialogue.](#edit-dialog)

Pour plus de commodité, une simple modification statique du texte d’en-tête est également disponible.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Titre du courrier électronique est v1, qui a été introduite avec la version x des composants principaux du courrier électronique en octobre 2022. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatible | Compatible |

Pour plus d’informations sur les versions et versions des composants principaux, consultez le document . [Versions des composants principaux de messagerie](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant du titre et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants.](https://adobe.com/go/aem_cmp_library_email_title)

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Titre [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_email_title_v1).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de modification {#edit-dialog}

La boîte de dialogue de modification permet à l’auteur de contenu de définir le texte du titre et de sélectionner le niveau de titre.

* **Titre** : si ce champ est vide, le titre de la page est utilisé.
   * Cliquez sur l’icône Campagne pour ouvrir la [Sélectionner la variable Adobe Campaign](/help/email/campaign-variables.md) pour insérer du contenu dynamique depuis Adobe Campaign.
* **Type/Taille** : définit le niveau d’en-tête du titre.
* **Lien** : définit le contenu auquel le titre sera associé. Il peut s’agir d’un chemin d’accès à une page de contenu, d’une URL externe ou d’une ancre de page.
   * Cliquez sur l’icône Campagne pour ouvrir la [Sélectionner la variable Adobe Campaign](/help/email/campaign-variables.md) pour insérer du contenu dynamique depuis Adobe Campaign.
* **ID** - Cette option permet de contrôler l’identifiant unique du composant dans le HTML.
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur CSS.

![Boîte de dialogue de modification du composant Titre de l’email](/help/email/assets/email-title-edit.png)

L’éditeur statique peut également être utilisé pour modifier le texte du composant du titre.

![Modification statique du composant Titre de courrier électronique](/help/email/assets/email-title-edit-inline.png)

### Onglet Styles {#styles-tab-edit}

Le composant Titre de courrier électronique prend en charge l’AEM [Système de style.](/help/get-started/authoring.md#component-styling)

Utilisez la liste déroulante pour sélectionner les styles à appliquer au composant. Les sélections effectuées dans la boîte de dialogue de modification ou dans la barre d’outils du composant ont le même effet.

Les styles doivent être configurés pour ce composant dans la variable [boîte de dialogue de conception](#design-dialog) pour que le menu déroulant soit disponible.

![Onglet Styles de la boîte de dialogue de modification du composant Titre](/help/email/assets/email-title-edit-styles.png)

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir le niveau d’en-tête par défaut que les composants de titre auront une fois créés par les auteurs de contenu.

### Onglet Tailles {#sizes-tab}

![Boîte de dialogue de conception du composant Titre](/help/email/assets/email-title-design.png)

* **Types/tailles autorisés pour les auteurs** - Activez ou désactivez les types d’en-tête qui seront disponibles pour les auteurs de contenu lorsqu’ils utilisent le composant Titre de l’email .
* **Type/Taille par défaut** - Définissez le type d’en-tête qui sera automatiquement attribué lorsqu’un auteur de contenu ajoute le composant Titre du courrier électronique à une page.
* **Désactiver le lien** - Désactivez la prise en charge des liens dans le composant Titre du courrier électronique pour interdire aux auteurs de contenu de lier des titres.

### Onglet Styles {#styles-tab}

Le composant Titre de courrier électronique prend en charge l’AEM [Système de style](/help/get-started/authoring.md#component-styling).
