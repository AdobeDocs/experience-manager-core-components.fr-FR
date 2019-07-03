---
title: Composant Carrousel
seo-title: Composant Carrousel
description: 'null'
seo-description: Le composant Carrousel permet à l’auteur de contenu de présenter le contenu dans un carrousel tournant.
uuid: 34934491-bd85-4f1e-ae22-bb48ed4dbd5c
content-type: référence
topic-tags: core-components
discoiquuid: 3510812b-9d3e-40fe-b986-0f15d40b42ad
disttype: dist5
gnavtheme: light
groupsectionnavitems: non
hidemerchandisingbar: inherit
hidepromocomponent: inherit
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: eef608fb06001485aa2c2c0b574af412ed7f15a4

---


# Composant Carrousel{#carousel-component}

Le composant principal Carrousel permet à l’auteur de contenu de présenter le contenu dans un carrousel navigable.

## Utilisation {#usage}

En utilisation le composant Carrousel, l’auteur de contenu peut organiser le contenu dans un carrousel de diapositives tournant.

La [boîte de dialogue Modifier](#edit-dialog) permet à l’auteur de contenu de créer, nommer et classer plusieurs diapositives et d’activer la transition automatique avec délai. A l’aide de la [boîte de dialogue Conception](#design-dialog), l’auteur du modèle peut définir quels composants peuvent être ajoutés au carrousel, activer ou désactiver les transitions automatiques et personnaliser les styles.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Carrousel est v1, qui a été introduite avec la version 2.2.0 des composants principaux d’octobre 2018 et est décrite dans ce document.

Le tableau suivant détaille toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Composant Version | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Compatible | Compatible | Compatible |

Pour plus d’informations sur les versions et les mises à jour des composants principaux, consultez le document sur les [versions des composants principaux](versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant Carrousel, des exemples d&#39;options de configuration, ainsi que des sorties HTML et JSON, consultez la [Bibliothèque de composants](http://opensource.adobe.com/aem-core-wcm-components/library/carousel.html).

### Détails techniques {#technical-details}

The latest technical documentation about the Carousel Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/carousel/v1/carousel).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](developing.md).

## Boîte de dialogue Modifier {#edit-dialog}

La boîte de dialogue Modifier permet à l’auteur de contenu d’ajouter, de renommer et de réorganiser les diapositives, ainsi que de définir les paramètres de transition automatique.

### Onglet Éléments {#items-tab}

![](assets/screenshot_2018-10-12at102451.png)

Utilisez le bouton **Ajouter** pour ouvrir le sélecteur de composants afin de choisir le composant à ajouter sous forme d’onglet. Une fois ajouté, une entrée est ajoutée à la liste qui contient les colonnes suivantes :

* **Icône** - Icône du type de composant de l’onglet pour une identification facile dans la liste. Placez le pointeur de la souris sur pour afficher le nom complet du composant sous forme d’info-bulle.
* **Description** - Description utilisée comme texte de l’onglet, c’est par défaut le nom du composant sélectionné pour l’onglet.
* **Supprimer** - Appuyez ou cliquez sur pour supprimer l’onglet du composant Onglets.
* **Réorganiser** - Appuyez ou cliquez dessus et faites glisser pour classer les onglets.

### Onglet Propriétés {#properties-tab}

![](assets/screenshot_2018-11-28at141054.png)

Dans l’onglet **Propriétés**, l’auteur du contenu peut définir les diapositives pour la transition automatique.

* **Transition automatique des diapositives** - Lorsqu’activée, le composant avance automatiquement vers la diapositive suivante après un délai spécifié.
* **Délai de transition** - Lorsque la transition automatique des diapositives est sélectionnée, cette valeur est utilisée pour définir le délai entre les transitions (en millisecondes).
* **Désactiver la pause automatique au survol** - Lorsque la **transition automatique des diapositives** est sélectionnée, la transition du carrousel se met automatiquement en pause chaque fois que l’utilisateur survole le carrousel. Sélectionnez cette option pour que la transition ne soit pas interrompue.

>[!NOTE]
>
>Les commandes d’avance de diapositives ne sont pas activées en mode **Édition**. Use [**Preview** mode](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html) or the **[View as Published](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html)** option to interact with the carousel as a reader of the published content would.
>
>La fonction d’avance automatique n’est pas activée en mode **Édition**. Use **[View as Published](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html)** option to see the auto-advance feature as a reader of the published content would.

## Sélectionner un panneau {#select-panel}

L’auteur du contenu peut utiliser l’option **Sélectionner un panneau** de la barre d’outils des composants pour passer à une autre diapositive afin de modifier et de réorganiser facilement l’ordre des diapositives.

![](assets/screenshot_2018-10-11at165417.png)

Lorsque vous sélectionnez l’option **Sélectionner un panneau** dans la barre d’outils des composant, les diapositives configurées s’affichent sous forme de liste déroulante.

* La liste est triée selon la disposition assignée des diapositives et est répercutée dans la numérotation.
* Le type de composant de la diapositive est affiché en premier, suivi de la description de la diapositive en police plus claire.

![](assets/opera_snapshot_2018-11-28141537localhost.png)

* Lorsque vous appuyez ou cliquez sur une entrée dans la liste déroulante, la vue est commutée dans l’éditeur.
* Vous pouvez réorganiser la diapositive en place à l’aide des poignées de glissement.

## Boîte de dialogue Conception {#design-dialog}

La boîte de dialogue Conception permet à l’auteur du modèle de définir les composants qui peuvent être ajoutés en tant que diapositives au composant Carrousel, ainsi que de définir les valeurs par défaut de la transition automatique et les styles personnalisés disponibles pour l’auteur du contenu.

### Onglet Propriétés {#properties-tab-1}

L’onglet **Propriétés** permet de définir les paramètres par défaut des transitions de diapositives lorsqu’un auteur de contenu ajoute le composant Carrousel à une page.

![](assets/screenshot_2018-11-28at141824.png)

* **Transition automatique des diapositives** - Définit si par défaut l’option permettant d’avancer automatiquement le carrousel à la diapositive suivante est activée lorsque l’auteur du contenu ajoute le composant Carrousel à une page.
* **Délai de transition** - Définit la valeur par défaut du délai de transition entre les diapositives (en millisecondes) lorsqu’un auteur de contenu ajoute le composant Carrousel à une page.
* **Désactiver la pause automatique au survol** - Définit si par défaut l’option de désactivation de la pause automatique de la diapositive est activée lorsque la **Transition automatique des diapositives** est activée par l’auteur du contenu.

### Onglet Composants autorisés {#allowed-components-tab}

L’onglet **Composants autorisés** permet de définir les composants pouvant être ajoutés en tant que diapositives au composant Carrousel par l’auteur du contenu.

L’onglet Composants autorisés fonctionne de la même manière que l’onglet du même nom lors [de la définition de la stratégie et des propriétés d’un conteneur de dispositions dans l’éditeur de modèles.](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

### Onglet Styles {#styles-tab}

Le composant Carrousel prend en charge le [système de style](authoring.md#component-styling) AEM.