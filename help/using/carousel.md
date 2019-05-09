---
title: Composant du carrousel
seo-title: Composant du carrousel
description: 'null'
seo-description: Le composant de carrousel permet à l'auteur de contenu de présenter le contenu dans un carrousel tournant.
uuid: 34934491-bd 85-4 f 1 e-ae 22-bb 48 ed 4 dbd 5 c
content-type: référence
topic-tags: core-components
discoiquuid: 3510812 b -9 d 3 e -40 fe-b 986-0 f 15 d 40 b 42
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
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Composant du carrousel{#carousel-component}

Le composant de carrousel de composant principal permet à l&#39;auteur de contenu de présenter le contenu dans un carrousel navigable.

## Utilisation {#usage}

Utilisation du composant de carrousel, auteur de contenu pour organiser le contenu dans un carrousel de diapositives tournant.

Le dialogue [Modifier](#edit-dialog) permet à l&#39;auteur de contenu de créer, nommer et classer plusieurs diapositives et d&#39;activer la transition automatique avec délai. A l&#39;aide de [la boîte de dialogue de conception](#design-dialog), l&#39;auteur du modèle peut définir quels composants peuvent être ajoutés au carrousel, activer ou désactiver les transitions automatiques et personnaliser les styles.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Carrousel est v 1, qui a été introduite avec la version 2.2.0 des composants principaux d&#39;octobre 2018 et est décrite dans ce document.

Le tableau suivant détaille toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Compatible | Compatible | Compatible |

Pour plus d&#39;informations sur les versions et les versions des composants principaux, consultez les versions des composants de Document [principaux](versions.md).

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple tiré de [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Capture d’écran {#screenshot}

![](assets/screenshot_2018-11-28at140433.png)

### Bibliothèque de composants {#component-library}

Pour tester le composant de carrousel ainsi que des exemples d&#39;options de configuration, ainsi que des sorties HTML et JSON, consultez la bibliothèque [de composants](http://opensource.adobe.com/aem-core-wcm-components/library/carousel.html).

### Détails techniques {#technical-details}

Vous trouverez la documentation technique la plus récente sur le composant [de carrousel sur github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/carousel/v1/carousel).

Vous trouverez plus d&#39;informations sur le développement des composants principaux dans la documentation destinée aux développeurs de composants [principaux](developing.md).

## Modifier le dialogue {#edit-dialog}

Le dialogue Modifier permet à l&#39;auteur de contenu d&#39;ajouter, de renommer et de réorganiser les diapositives, ainsi que de définir les paramètres de transition automatique.

### Onglet Eléments {#items-tab}

![](assets/screenshot_2018-10-12at102451.png)

Utilisez le bouton **Ajouter** pour ouvrir le sélecteur de composants afin de choisir le composant à ajouter sous forme d&#39;onglet. Une fois ajouté, une entrée est ajoutée à la liste qui contient les colonnes suivantes :

* **Icône** - Icône du type de composant de l&#39;onglet pour une identification facile dans la liste. Placez le pointeur de la souris sur pour afficher le nom complet du composant sous forme d&#39;info-bulle.
* **Description** : description utilisée comme texte de l&#39;onglet, par défaut au nom du composant sélectionné pour l&#39;onglet.
* **Supprimer** : appuyez ou cliquez sur pour supprimer l&#39;onglet du composant de onglets.
* **Réorganiser** : appuyez sur ou cliquez et faites glisser pour classer les onglets.

### Onglet Propriétés {#properties-tab}

![](assets/screenshot_2018-11-28at141054.png)

Dans l&#39;onglet **Propriétés** , l&#39;auteur du contenu peut définir les diapositives pour la transition automatique.

* **Diapositives de transition automatiquement** : lorsqu&#39;elles sont actives, le composant avance automatiquement vers la diapositive suivante après un délai spécifié.
* **Délai de transition** - Lorsque la transition automatique des diapositives est sélectionnée, cette valeur est utilisée pour définir le délai entre les transitions (en millisecondes).
* **Désactiver la pause automatique au survol** - Lorsque **la transition automatique des diapositives** est sélectionnée, la transition du carrousel se met automatiquement en pause chaque fois que l&#39;utilisateur survole le carrousel. Sélectionnez cette option pour que la transition ne soit pas interrompue.

>[!NOTE]
>
>Les commandes d&#39;avance de diapositives ne sont pas activées en mode **d&#39;édition** . Utilisez [**le mode Aperçu**](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html) ou **[l&#39;option Afficher comme publié](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html)** pour interagir avec le carrousel comme lecteur du contenu publié.
>
>La fonction d&#39;avance automatique n&#39;est pas activée en mode **d&#39;édition** . Utilisez **[l&#39;option Affichage comme publié](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html)** pour afficher la fonctionnalité d&#39;avance automatique en tant que lecteur du contenu publié.

## Sélectionner un panneau {#select-panel}

L&#39;auteur du contenu peut utiliser l&#39;option **Sélectionner un panneau** de la barre d&#39;outils de composants pour passer à une autre diapositive pour modification et réorganiser facilement l&#39;ordre des diapositives.

![](assets/screenshot_2018-10-11at165417.png)

Lorsque vous sélectionnez l&#39;option **Sélectionner un panneau** dans la barre d&#39;outils de composant, les diapositives configurées s&#39;affichent sous forme de liste déroulante.

* La liste est triée selon la disposition des diapositives assignée et est répercutée dans la numérotation.
* Le type de composant de la diapositive est affiché en premier, suivi de la description de la diapositive en police plus claire.

![](assets/opera_snapshot_2018-11-28141537localhost.png)

* Lorsque vous appuyez ou cliquez sur une entrée dans la liste déroulante, la vue est commutée dans l&#39;éditeur.
* Vous pouvez réorganiser la diapositive en place à l&#39;aide des poignées de glissement.

## Créer un dialogue {#design-dialog}

Le dialogue de conception permet à l&#39;auteur du modèle de définir les composants qui peuvent être ajoutés en tant que diapositives au composant de carrousel, ainsi que de définir les valeurs par défaut de la transition automatique et les styles personnalisés disponibles pour l&#39;auteur du contenu.

### Onglet Propriétés {#properties-tab-1}

L&#39;onglet **Propriétés** permet de définir les paramètres par défaut des transitions de diapositives lorsqu&#39;un auteur de contenu ajoute le composant Carrousel à une page.

![](assets/screenshot_2018-11-28at141824.png)

* **Transitions automatiquement propagées** : définit si par défaut l&#39;option permettant d&#39;avancer automatiquement le carrousel à la diapositive suivante est activée lorsque l&#39;auteur du contenu ajoute le composant Carrousel à une page.
* **Délai de transition** : définit la valeur par défaut du délai de transition entre les diapositives (en millisecondes) lorsqu&#39;un auteur de contenu ajoute le composant Carrousel à une page.
* **Désactiver la pause automatique au survol** : définit si par défaut l&#39;option de désactivation de la suspension automatique de la diapositive est activée lorsque **la sélection automatique des diapositives** de transition est activée par l&#39;auteur du contenu.

### Onglet Composants autorisés {#allowed-components-tab}

L&#39;onglet **Composants** autorisés permet de définir les composants pouvant être ajoutés en tant que diapositives au composant Carrousel par l&#39;auteur du contenu.

L&#39;onglet Composants autorisés fonctionne de la même manière que l&#39;onglet du même nom lors [de la définition de la stratégie et des propriétés d&#39;un conteneur de dispositions dans l&#39;éditeur de modèles.](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

### Onglet Styles {#styles-tab}

Le composant de carrousel prend en charge le système [de style AEM](authoring.md#component-styling).