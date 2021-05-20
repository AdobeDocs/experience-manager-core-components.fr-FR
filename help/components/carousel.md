---
title: Composant du carrousel
description: Le composant du carrousel permet à l’auteur de contenu de présenter le contenu dans un carrousel rotatif.
role: Architect, Developer, Administrator, Business Practitioner
exl-id: 3331214c-a05c-47e1-b54c-fbfd1045bd60
source-git-commit: 8ff36ca143af9496f988b1ca65475497181def1d
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 100%

---

# Composant du carrousel {#carousel-component}

Le composant du carrousel des composants principaux permet à l’auteur de contenu de présenter le contenu dans un carrousel navigable.

## Utilisation {#usage}

En utilisation le composant du carrousel, l’auteur de contenu peut organiser le contenu dans un carrousel de diapositives rotatif.

La [boîte de dialogue de modification](#edit-dialog) permet à l’auteur de contenu de créer, nommer et classer plusieurs diapositives et d’activer la transition automatique avec délai. À l’aide de la [boîte de dialogue de conception](#design-dialog), l’auteur du modèle peut définir quels composants peuvent être ajoutés au carrousel, activer ou désactiver les transitions automatiques et personnaliser les styles.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant du carrousel est v1, qui a été introduite avec la version 2.2.0 des composants principaux d’octobre 2018. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant du carrousel, des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_carousel_fr).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant du carrousel [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_carousel_v1_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de modification {#edit-dialog}

La boîte de dialogue de modification permet à l’auteur de contenu d’ajouter, de renommer et de réorganiser les diapositives, ainsi que de définir les paramètres de transition automatique.

### Onglet Éléments {#items-tab}

![Onglet Éléments de la boîte de dialogue de modification du composant Carrousel](/help/assets/carousel-edit-items.png)

Utilisez le bouton **Ajouter** pour ouvrir le sélecteur de composants afin de choisir le composant à ajouter sous forme d’onglet. Une fois le composant ajouté, une entrée est ajoutée à la liste qui contient les colonnes suivantes :

* **Icône** : icône du type de composant de l’onglet pour une identification facile dans la liste. Pointez dessus pour afficher le nom complet du composant sous forme d’info-bulle.
* **Description** : description utilisée comme texte de l’onglet. Par défaut, il s’agit du nom du composant sélectionné pour l’onglet.
* **Supprimer** : appuyez ou cliquez sur cette option pour supprimer l’onglet du composant Onglets.
* **Réorganiser** : appuyez ou cliquez sur cette option et faites glisser pour classer les onglets.

>[!TIP]
>
>Si la fenêtre d’affichage de la page est réduite, de sorte que la boîte de dialogue de modification s’affiche en plein écran, le bouton **Ajouter** est masqué. Vous pouvez toujours ajouter des composants au composant du carrousel en [les faisant glisser depuis l’explorateur de composants et en les déposant ensuite sur le composant du carrousel dans l’éditeur de page](https://docs.adobe.com/content/help/fr-FR/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component-from-the-components-browser).

### Onglet Propriétés {#properties-tab}

![Onglet Propriétés de la boîte de dialogue de modification du composant Carrousel](/help/assets/carousel-edit-properties.png)

Dans l’onglet **Propriétés**, l’auteur du contenu peut définir les diapositives pour la transition automatique.

* **Transition automatique des diapositives** : lorsque cette option est activée, le composant passe automatiquement à la diapositive suivante après un délai spécifié.
* **Délai de transition** : lorsque la transition automatique des diapositives est sélectionnée, cette valeur est utilisée pour définir le délai entre les transitions (en millisecondes).
* **Désactiver la pause automatique lors du survol** : lorsque l’option **Transition automatique des diapositives** est sélectionnée, la transition du carrousel se met automatiquement en pause chaque fois que l’utilisateur survole le carrousel. Sélectionnez cette option pour que la transition ne soit pas interrompue.
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

>[!NOTE]
>
>Les commandes d’avance de diapositives ne sont pas activées en mode **Édition**. Utilisez le mode [**Aperçu**](https://docs.adobe.com/content/help/fr-FR/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#preview-mode) ou l’option **[Afficher comme publié(e)](https://docs.adobe.com/content/help/fr-FR/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** pour interagir avec le carrousel en tant que lecteur du contenu publié.
>
>La fonction d’avance automatique n’est pas activée en mode **Édition**. Utilisez l’option **[Afficher comme publié(e)](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** pour afficher la fonctionnalité d’avance automatique en tant que lecteur du contenu publié.

### Onglet Accessibilité {#accessibility-tab}

![Onglet Accessibilité de la boîte de dialogue de modification du composant Carrousel](/help/assets/carousel-edit-accessibility.png)

Dans l’onglet **Accessibilité**, les valeurs peuvent être définies pour les étiquettes d’[accessibilité ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) du composant.

* **Étiquette** : Valeur d’un attribut de étiquette ARIA pour le composant

## Sélectionner un panneau {#select-panel}

L’auteur du contenu peut utiliser l’option **Sélectionner un panneau** de la barre d’outils des composants pour passer à une autre diapositive afin de modifier et de réorganiser facilement l’ordre des diapositives.

![Icône Sélectionner un panneau](/help/assets/select-panel-icon.png)

Lorsque vous sélectionnez l’option **Sélectionner un panneau** dans la barre d’outils des composants, les diapositives configurées s’affichent sous forme de liste déroulante.

* La liste est triée selon la disposition assignée des diapositives et est répercutée dans la numérotation.
* Le type de composant de la diapositive est affiché en premier, suivi de la description de la diapositive en police plus claire.

![Sélectionner un panneau](/help/assets/select-panel-popover.png)

* Lorsque vous appuyez ou cliquez sur une entrée dans la liste déroulante, la vue est commutée dans l’éditeur.
* Vous pouvez réorganiser la diapositive en place à l’aide des poignées de glissement.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les composants qui peuvent être ajoutés en tant que diapositives au composant du carrousel, ainsi que de définir les valeurs par défaut de la transition automatique et les styles personnalisés disponibles pour l’auteur du contenu.

### Onglet Propriétés {#properties-tab-1}

L’onglet **Propriétés** permet de définir les paramètres par défaut des transitions de diapositives lorsqu’un auteur de contenu ajoute le composant du carrousel à une page.

![Boîte de dialogue de conception du composant Carrousel](/help/assets/carousel-design.png)

* **Transition automatique des diapositives** : définit si par défaut l’option permettant d’avancer automatiquement le carrousel à la diapositive suivante est activée lorsque l’auteur du contenu ajoute le composant du carrousel à une page.
* **Délai de transition** : définit la valeur par défaut du délai de transition entre les diapositives (en millisecondes) lorsqu’un auteur de contenu ajoute le composant du carrousel à une page.
* **Désactiver la pause automatique lors du survol** : définit si par défaut l’option de désactivation de la pause automatique de la diapositive est activée lorsque l’option **Transition automatique des diapositives** est activée par l’auteur du contenu.

### Onglet Composants autorisés {#allowed-components-tab}

L’onglet **Composants autorisés** permet de définir les composants pouvant être ajoutés en tant que diapositives au composant du carrousel par l’auteur du contenu.

L’onglet Composants autorisés fonctionne de la même manière que l’onglet du même nom lors de la [définition de la stratégie et des propriétés d’un conteneur de mises en page dans l’éditeur de modèles](https://docs.adobe.com/content/help/fr-FR/experience-manager-cloud-service/sites/authoring/features/templates.html).

### Onglet Styles {#styles-tab}

Le composant du carrousel prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

## Couche de données client Adobe {#data-layer}

Le composant Carrousel prend en charge la [couche de données client Adobe](/help/developing/data-layer/overview.md).
