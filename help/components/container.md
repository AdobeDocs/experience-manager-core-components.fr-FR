---
title: 'Composant de conteneur '
description: Le composant de conteneur des composants principaux permet la création d’un conteneur pour plusieurs autres composants sur une page.
role: Architect, Developer, Admin, User
exl-id: 53c7190d-44cb-42ff-bc1a-483c7875bcf8
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 100%

---


# Composant de conteneur {#container-component}

Le composant de conteneur des composants principaux permet la création d’un conteneur pour plusieurs autres composants sur une page.

{{traditional-aem}}

## Utilisation {#usage}

Le composant de conteneur des composants principaux permet la création d’un conteneur pour plusieurs autres composants sur une page et peut servir à regrouper d’autres composants et à appliquer un style ou une mise en page communs.

* Les propriétés du conteneur peuvent être définies dans la [boîte de dialogue de configuration](#configure-dialog).
* Les valeurs par défaut du composant de conteneur lors de son ajout à une page peuvent être définies dans la [boîte de dialogue de conception](#design-dialog).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de conteneur est v1, qui a été introduite avec la version 2.5.0 des composants principaux en février 2019. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |---|---|---|
| v1 | Compatible avec la <br>[version 2.17.4](/help/versions.md) et versions antérieures | Compatible | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant de conteneur et voir des exemples de ses options de configuration, ainsi que la sortie HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_container_fr).

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant de conteneur [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_container_v1_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur du contenu de définir l’élément de conteneur et la façon dont il se comporte et apparaît pour un visiteur sur la page.

![Boîte de dialogue de modification du composant Conteneur](/help/assets/container-edit.png)

* **Disposition** : cette option définit le comportement ou le comportement de mise en page du composant de conteneur.
   * **Simple** : définit un conteneur en tant qu’ensemble simple de composants.
   * **Grille réactive** : définit un conteneur en tant que [mise en page réactive AEM.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html?lang=fr)
* **Couleur d’arrière-plan** : définissable en tant que valeurs RVB de forme libre ou en utilisant le sélecteur de couleurs, [selon la configuration](#background-tab)
* **Image d’arrière-plan** : définit une couleur d’arrière-plan pour le conteneur, [selon la configuration](#background-tab)
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les options disponibles pour l’auteur du contenu qui utilise le composant de conteneur.

### Onglet Composants autorisés {#allowed-components-tab}

L’onglet **Composants autorisés** permet de définir quels composants peuvent être ajoutés en tant qu’éléments au composant de conteneur par l’auteur du contenu.

L’onglet Composants autorisés fonctionne de la même manière que l’onglet du même nom lors de la [définition de la stratégie et des propriétés d’un conteneur de mise en page dans l’éditeur de modèles](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=fr).

### Onglet Composants par défaut {#default-components-tab}

L’onglet Composants par défaut permet de définir quel composant est ajouté au composant lorsqu’un type de ressource particulier est déposé sur le conteneur, comme [la définition des composants par défaut sur le modèle de page](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=fr).

### Onglet Paramètres réactifs {#responsive-settings-tab}

![Onglet Paramètres réactifs de la boîte de dialogue de conception du composant Conteneur](/help/assets/container-design-responsive.png)

* **Colonnes** : définit le nombre de colonnes dans la grille du conteneur obtenu.

### Onglet Arrière-plan {#background-tab}

![Onglet Arrière-plan de la boîte de dialogue de conception du composant Conteneur](/help/assets/container-design-background.png)

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
   * **Réorganiser** : appuyez ou cliquez dessus et faites glisser pour réorganiser l’ordre des échantillons.

### Onglet Styles {#styles-tab}

Le composant de conteneur prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.
