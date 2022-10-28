---
title: Composant Conteneur de courrier électronique
description: Le composant Conteneur de courrier électronique permet la création d’un conteneur pour plusieurs composants supplémentaires dans votre contenu de courrier électronique.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 40%

---


# Composant Conteneur de courrier électronique {#email-container-component}

Le composant Conteneur de courrier électronique permet la création d’un conteneur pour plusieurs composants supplémentaires dans votre contenu de courrier électronique.

## Utilisation {#usage}

Le composant Conteneur de courrier électronique permet la création d’un conteneur pour plusieurs composants supplémentaires dans le contenu de votre courrier électronique. Il peut être utilisé pour regrouper d’autres composants et appliquer un style ou une mise en page communs.

* Les propriétés du conteneur peuvent être définies dans la [boîte de dialogue de configuration.](#configure-dialog)
* Les valeurs par défaut du composant Conteneur de courrier électronique lors de son ajout à une page peuvent être définies dans la variable [boîte de dialogue de conception.](#design-dialog)

Une fois qu’un composant Conteneur de courrier électronique est ajouté à une page, un auteur de contenu peut y faire glisser des composants supplémentaires.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de conteneur de courrier électronique est v1, qui a été introduite avec la version X des composants principaux de courrier électronique en octobre 2022. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatible | Compatible |

Pour plus d’informations sur les versions et versions des composants principaux d’email, consultez le document . [Envoi des versions des composants principaux par courrier électronique.](/help/email/versions.md)

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant de conteneur de courrier électronique et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la page [Bibliothèque de composants.](https://adobe.com/go/aem_cmp_library_email_container)

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant de conteneur [se trouve sur GitHub.](https://adobe.com/go/aem_cmp_tech_email_container_v1)

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux.](/help/developing/overview.md)

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de définir l’élément de conteneur et la manière dont il se comporte et apparaît dans votre contenu.

![Boîte de dialogue de modification du composant Conteneur de courrier électronique](/help/email/assets/email-container-configure.png)

* **Disposition** - Cette option définit le comportement ou le comportement de mise en page du composant Conteneur de courrier électronique.
   * **pleine largeur**
   * **moitié|moitié**
   * **un tiers|deux-tiers**
   * **deux tiers|un tiers**
   * **third|third**
* **Couleur d’arrière-plan** : définissable en tant que valeurs RVB de forme libre ou en utilisant le sélecteur de couleurs, [selon la configuration](#container-settings-tab)
* **Image d’arrière-plan** - Définit une image d’arrière-plan pour le conteneur, [selon la configuration](#container-settings-tab)
* **ID** - Cette option permet de contrôler l’identifiant unique du composant dans le HTML.
   * Si rien n’est indiqué, un identifiant unique est automatiquement généré et peut être trouvé en examinant le contenu qui en résulte.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur CSS.

### Onglet Styles {#styles-tab-edit}

Le composant Conteneur de courrier électronique prend en charge l’AEM [Système de style.](/help/get-started/authoring.md#component-styling)

Utilisez la liste déroulante pour sélectionner les styles à appliquer au composant. Les sélections effectuées dans la boîte de dialogue de modification ou dans la barre d’outils du composant ont le même effet.

Les styles doivent être configurés pour ce composant dans la variable [boîte de dialogue de conception](#design-dialog) pour que l’onglet soit disponible.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les options disponibles pour l’auteur du contenu qui utilise le composant Conteneur de courrier électronique.

### Onglet Composants autorisés {#allowed-components-tab}

Le **Composants autorisés** Cet onglet permet de définir quels composants peuvent être ajoutés en tant qu’éléments au composant Conteneur de courrier électronique par l’auteur du contenu.

Le **Composants autorisés** fonctionne de la même manière que l’onglet du même nom lorsque [définition de la stratégie et des propriétés d’un conteneur de mises en page dans l’éditeur de modèles.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=fr)

### Onglet Composants par défaut {#default-components-tab}

Le **Composants par défaut** sert à définir quel composant est ajouté au composant lorsqu’un type de ressource particulier est déposé sur le conteneur, comme [la manière dont les composants par défaut sont définis sur le modèle de page.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Onglet Paramètres du conteneur {#container-settings-tab}

Le **Paramètres du conteneur** définit si l’auteur peut définir une image ou une couleur d’arrière-plan.

![Onglet Paramètres de conteneur de la boîte de dialogue de conception du composant Conteneur de courrier électronique](/help/email/assets/email-container-design-container-settings.png)

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
   * **Réorganiser** - Appuyez ou cliquez dessus et faites glisser pour réorganiser les échantillons.

### Onglet Styles {#styles-tab}

Le composant Conteneur de courrier électronique prend en charge l’AEM [Système de style.](/help/get-started/authoring.md#component-styling)