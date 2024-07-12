---
title: Composant Conteneur d’e-mail
description: Le composant Conteneur d’e-mail permet la création d’un conteneur pour plusieurs composants supplémentaires dans votre contenu d’e-mail.
role: Architect, Developer, Admin, User
exl-id: 3b271e95-0093-4cb1-bb83-8446ba12a821
source-git-commit: 3abc29e0c186a84f079d5938b8b716f4c7378d65
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 100%

---


# Composant Conteneur d’e-mail {#email-container-component}

Le composant Conteneur d’e-mail permet la création d’un conteneur pour plusieurs composants supplémentaires dans votre contenu d’e-mail.

## Utilisation {#usage}

Le composant Conteneur d’e-mail permet la création d’un conteneur pour plusieurs autres composants supplémentaires dans un contenu d’e-mail et peut servir à regrouper d’autres composants et à appliquer une mise en page ou un style communs.

* Les propriétés du conteneur peuvent être sélectionnées dans la [boîte de dialogue de configuration.](#configure-dialog)
* Les valeurs par défaut du composant Conteneur d’e-mail lors de son ajout à une page peuvent être définies dans la [boîte de dialogue de conception.](#design-dialog)

Une fois qu’un composant Conteneur d’e-mail est ajouté à une page, un créateur de contenu peut y glisser-déposer des composants supplémentaires.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Conteneur d’e-mail est v1. Celle-ci a été introduite avec la version X des composants principaux d’e-mail en octobre 2022. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatible | - |

Pour plus d’informations sur les versions et les publications des composants principaux d’e-mail, voir le document sur les [versions des composants principaux d’e-mail](/help/email/versions.md).

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant de conteneur [se trouve sur GitHub.](https://adobe.com/go/aem_cmp_tech_email_container_v1)

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux.](/help/developing/overview.md)

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet au créateur de contenu de définir l’élément de conteneur et la manière dont il se comporte et apparaît dans votre contenu.

![Boîte de dialogue de modification du composant Conteneur d’e-mail](/help/email/assets/email-container-configure.png)

* **Mise en page** : cette option définit le comportement ou le comportement de mise en page du composant Conteneur d’e-mail.
   * **pleine largeur**
   * **moitié|moitié**
   * **un tiers|deux tiers**
   * **deux tiers|un tiers**
   * **tiers|tiers|tiers**
* **Couleur d’arrière-plan** : définissable en tant que valeurs RVB de forme libre ou en utilisant le sélecteur de couleurs, [selon la configuration](#container-settings-tab)
* **Image d’arrière-plan** : Définit une couleur d’arrière-plan pour le conteneur, [selon la configuration](#container-settings-tab).
* **ID** : Cette option permet de contrôler l’identifiant unique du composant dans le HTML.
   * Si rien n’est indiqué, un ID unique est généré automatiquement pour vous. Vous le trouverez en examinant le contenu obtenu.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur CSS.

### Onglet Styles {#styles-tab-edit}

Le composant Conteneur d’e-mail prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

Utilisez la liste déroulante pour sélectionner les styles à appliquer au composant. Les sélections effectuées dans la boîte de dialogue de modification ou dans la barre d’outils du composant ont le même effet.

Pour accéder à l’onglet, les styles doivent être configurés pour ce composant dans la [boîte de dialogue de conception](#design-dialog).

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet au créateur du modèle de définir les options disponibles pour le créateur contenu qui utilise le composant Conteneur d’e-mail.

### Onglet Composants autorisés {#allowed-components-tab}

L’onglet **Composants autorisés** permet de définir quels composants peuvent être ajoutés en tant qu’éléments au composant Conteneur d’e-mail par le créateur de contenu.

L’onglet **Composants autorisés** fonctionne de la même manière que l’onglet du même nom lors de la [définition de la politique et des propriétés d’un conteneur de mise en page dans l’éditeur de modèles.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=fr)

### Onglet Composants par défaut {#default-components-tab}

L’onglet **Composants par défaut** permet de définir quel composant est ajouté au composant lorsqu’un type de ressource particulier est déposé sur le conteneur, comme [la définition des composants par défaut sur le modèle de page.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=fr)

### Onglet Paramètres de conteneur {#container-settings-tab}

L’onglet **Paramètres de conteneur** définit si le créateur peut définir une image ou une couleur d’arrière-plan.

![L’onglet Paramètres de conteneur de la boîte de dialogue de conception du composant Conteneur d’e-mail](/help/email/assets/email-container-design-container-settings.png)

* **Image d’arrière-plan**
   * **Activer l’image d’arrière-plan** : sélectionnez cette option pour permettre à l’auteur de contenu de définir une image d’arrière-plan pour le conteneur.
* **Couleur d’arrière-plan**
   * **Activer la couleur d’arrière-plan** : sélectionnez cette option pour permettre à l’auteur du contenu de définir une couleur d’arrière-plan pour le conteneur.
   * **Échantillons uniquement** : sélectionnez cette option pour permettre uniquement à l’auteur de contenu de sélectionner des échantillons de couleurs prédéfinis pour la couleur d’arrière-plan du conteneur.
      * Cette option est uniquement disponible lorsque l’option **Activer la couleur d’arrière-plan** est sélectionnée.
* **Échantillons autorisés** : définissez des couleurs prédéfinies à partir desquelles l’auteur de contenu peut sélectionner la couleur d’arrière-plan du conteneur.
   * Utilisez le bouton **Ajouter** pour ajouter un échantillon de couleur prédéfini. Une fois le composant ajouté, une entrée est ajoutée à la liste qui contient les colonnes suivantes :
   * **Valeur** : définissez manuellement la couleur via les valeurs RVB.
      * Appuyez ou cliquez sur le sélecteur de couleurs pour sélectionner plus facilement une couleur en réglant chaque valeur RVB ou en définissant une valeur hexadécimale.
   * **Supprimer** : appuyez ou cliquez sur cette option pour supprimer un échantillon.
   * **Réorganiser** : Appuyez ou cliquez sur les nuanciers et faites-les glisser pour les réorganiser.

### Onglet Styles {#styles-tab}

Le composant Conteneur d’e-mail prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.
