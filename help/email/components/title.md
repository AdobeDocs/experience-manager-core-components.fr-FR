---
title: Composant Titre de l’e-mail
description: Le composant Titre de l’e-mail est un composant En-tête de section pour vos e-mails. Il permet d’effectuer des modifications statiques.
role: Architect, Developer, Admin, User
exl-id: f65b6973-bb36-406f-bbea-f85a23f5340b
index: false
source-git-commit: eb77567dc32cccb81a9fc131493d11fb55b7e93b
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Composant Titre de l’e-mail {#email-title-component}

Le composant Titre de l’e-mail est un composant En-tête de section pour vos e-mails. Il permet d’effectuer des modifications statiques.

## Utilisation {#usage}

Le composant Titre de l’e-mail est conçu pour être utilisé comme titre ou en-tête d’une section d’un e-mail.

* Les niveaux d’en-tête disponibles peuvent être définis par le créateur du modèle dans la [boîte de dialogue de conception.](#design-dialog)
* Le créateur de contenu peut sélectionner les niveaux d’en-têtes disponibles dans la [boîte de dialogue de modification.](#edit-dialog)

Pour plus de commodité, une simple modification statique du texte d’en-tête est également disponible.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Titre de l’e-mail est v1. Celle-ci a été introduite avec la version X des composants principaux d’e-mail en octobre 2022. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatible | - | - |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux d’e-mail](/help/versions.md).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Titre [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_email_title_v1_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de modification {#edit-dialog}

La boîte de dialogue de modification permet à l’auteur de contenu de définir le texte du titre et de sélectionner le niveau de titre.

* **Titre** : si ce champ est vide, le titre de la page est utilisé.
   * Cliquez sur l’icône Campagne pour ouvrir la boîte de dialogue [Sélectionner la variable Adobe Campaign](/help/email/campaign-variables.md) et insérer du contenu dynamique depuis Adobe Campaign.
* **Type/Taille** : définit le niveau d’en-tête du titre.
* **Lien** : définit le contenu auquel le titre sera associé. Il peut s’agir d’un chemin d’accès à une page de contenu, d’une URL externe ou d’une ancre de page.
   * Cliquez sur l’icône Campagne pour ouvrir la boîte de dialogue [Sélectionner la variable Adobe Campaign](/help/email/campaign-variables.md). Vous pouvez alors insérer du contenu dynamique depuis Adobe Campaign.
* **ID** : Cette option permet de contrôler l’identifiant unique du composant dans le HTML.
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur CSS.

![Boîte de dialogue de modification du composant Titre de l’e-mail](/help/email/assets/email-title-edit.png)

L’éditeur statique peut également être utilisé pour modifier le texte du composant du titre.

![Modification statique du composant Titre de l’e-mail](/help/email/assets/email-title-edit-inline.png)

### Onglet Styles {#styles-tab-edit}

Le composant Titre de l’e-mail prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

Utilisez la liste déroulante pour sélectionner les styles à appliquer au composant. Les sélections effectuées dans la boîte de dialogue de modification ou dans la barre d’outils du composant ont le même effet.

Pour accéder au menu déroulant, les styles doivent être configurés pour ce composant dans la [boîte de dialogue de conception](#design-dialog).

![Onglet Styles de la boîte de dialogue de modification du composant Titre](/help/email/assets/email-title-edit-styles.png)

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir le niveau d’en-tête par défaut que les composants de titre auront une fois créés par les auteurs de contenu.

### Onglet Tailles {#sizes-tab}

![Boîte de dialogue de conception du composant Titre](/help/email/assets/email-title-design.png)

* **Types/tailles autorisés pour les auteurs** : Activez ou désactivez les types d’en-têtes qui seront disponibles pour les créateurs de contenu lorsqu’ils utilisent le composant Titre de l’e-mail.
* **Type par défaut/taille** : Définissez le type d’en-tête qui sera automatiquement attribué lorsqu’un créateur de contenu ajoute le composant Titre de l’e-mail à une page.
* **Désactiver le lien** : Désactivez la prise en charge des liens dans le composant Titre de l’e-mail pour interdire aux créateurs de contenu de lier des titres.

### Onglet Styles {#styles-tab}

Le composant Titre de l’e-mail prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.
