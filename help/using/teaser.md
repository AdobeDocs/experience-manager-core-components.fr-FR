---
title: Composant Teaser
seo-title: Composant Teaser
description: Le composant Teaser peut afficher une image, un titre, un texte enrichi et éventuellement un lien vers un contenu supplémentaire.
seo-description: Le composant Teaser peut afficher une image, un titre, un texte enrichi et éventuellement un lien vers un contenu supplémentaire.
uuid: 46989314-df37-448b-8562-c707043f2160
contentOwner: bohnert
content-type: référence
topic-tags: core-components
discoiquuid: e597c18e-3643-41be-9878-4a7872f1ab90
translation-type: ht
source-git-commit: eef608fb06001485aa2c2c0b574af412ed7f15a4

---


# Composant Teaser{#teaser-component}

Le composant principal Teaser peut afficher une image, un titre, un texte enrichi et éventuellement un lien vers un contenu supplémentaire.

## Utilisation {#usage}

Le composant Teaser permet à l’auteur de contenu de créer facilement un teaser vers un contenu supplémentaire à l’aide d’une image, d’un titre ou d’un texte enrichi et de lier un contenu supplémentaire ou d’autres actions.

L’auteur du modèle peut utiliser la [boîte de dialogue de conception](#design-dialog) définir si les options permettant de créer des actions à appeler et d’ajouter des liens sont disponibles, ainsi que de désactiver diverses options d’affichage. L’auteur du contenu peut utiliser la [boîte de dialogue Configurer](#configure-dialog) pour définir une image, des CTAS, des titres et descriptions et configurer des liens vers le teaser individuel. Vous pouvez accéder à la [boîte de dialogue de modification](image.md#edit-dialog) du [composant Image](image.md) pour modifier l’image de teaser.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Teaser est v1, qui a été introduite avec la version 2.1.0 des composants principaux de juillet 2018 et est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|---|---|---|---|
| v1 | Compatible | Compatible | Compatible |

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant Teaser, des exemples de ses options de configuration, ainsi que des sorties HTML et JSON, consultez la [Bibliothèque de composants](http://opensource.adobe.com/aem-core-wcm-components/library/teaser.html).

### Détails techniques {#technical-details}

Vous trouverez la documentation technique la plus récente sur le composant Teaser [sur GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/teaser/v1/teaser).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](developing.md).

## Boîte de dialogue de configuration {#configure-dialog}

L’auteur du contenu peut utiliser la boîte de dialogue de configuration pour définir les propriétés du teaser individuel. Il existe également une [boîte de dialogue de modification](#edit-dialog) pour modifier l’image de teaser si celle-ci est sélectionnée.

### Image {#image}

![](assets/screen_shot_2018-07-03at104125.png)

* **Ressource image**
   * Déposez un fichier depuis l’[explorateur de ressources](https://helpx.adobe.com/fr/experience-manager/6-5/sites/authoring/using/author-environment-tools.html) ou appuyez sur l’option **parcourir** pour effectuer un téléchargement à partir d’un système de fichiers local.
   * Appuyez ou cliquez sur **Effacer** pour désélectionner l’image actuellement sélectionnée.
   * Appuyez ou cliquez sur **Modifier** pour [gérer les rendus de la ressource](https://helpx.adobe.com/fr/experience-manager/6-5/assets/using/managing-assets-touch-ui.html) dans l’éditeur de ressources.

### Texte {#text}

![](assets/screen_shot_2018-07-03at104138.png)

* **Titre**
Titre à afficher comme titre du teaser.
* **Obtenir le titre de la page liée**
Lorsque cette option est cochée, le titre est renseigné avec le titre de la page liée.
* **Description**
Définit une description à afficher sous forme de sous-titre du teaser.
* **Obtenir la description de la page liée**
Lorsque cette option est cochée, la description est renseignée avec la description de la page liée.

### Liens et actions {#links-actions}

![](assets/screen_shot_2018-07-03at104146.png)

* **Lien**
Lien appliqué au teaser. Utilisez le navigateur de chemins pour sélectionner la cible du lien.
* **Activation de l’option Appel à des actions**
Lorsqu’elle est cochée, elle active la définition d’appel à actions. Le premier lien Appel à action de la liste est utilisé comme lien pour d’autres éléments de teaser.

## Boîte de dialogue Modifier {#edit-dialog}

Le composant Teaser délègue le rendu d’image au [Composant Image](image.md). Par conséquent, [la boîte de dialogue Modifier] (image.md#edit-dialog du composant Image est accessible à l’auteur du contenu pour manipuler l’image de teaser).

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les options de teaser que l’auteur du contenu a définies lors de l’utilisation de ce composant.

### Onglet Teaser {#teaser-tab}

![](assets/screen_shot_2018-07-03at105958.png)

* **Appels à l’action**
   * **Désactivation des appels à actions**
Masquez l’option **Appel à actions** pour les auteurs de contenu.
* **Eléments**
   * **Masquer le titre**
      * Masque l’option **Titre** pour les auteurs de contenu.
      * Lorsqu’il est sélectionné, **le type de titre** est masqué.
   * **Masquer la description**
Masquez l’option **Description** pour les auteurs de contenu.
* **Type de titre**
Définit la balise H à utiliser par le titre du teaser.
* **Liens**
   * **Ne pas lier l’image**
Lorsque cette option est sélectionnée, l’image de teaser n’est pas liée.
   * **Ne pas lier le titre**
Lorsque sélectionné, le titre du teaser n’est pas lié.

### Onglet Styles {#styles-tab}

Le composant Teaser prend en charge le [système de style](authoring.md#component-styling) AEM.
