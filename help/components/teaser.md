---
title: Composant Teaser
description: Le composant Teaser peut afficher une image, un titre, un texte enrichi et éventuellement un lien vers un contenu supplémentaire.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 64%

---


# Composant Teaser {#teaser-component}

Le composant principal Teaser peut afficher une image, un titre, un texte enrichi et éventuellement un lien vers un contenu supplémentaire.

## Utilisation {#usage}

Le composant Teaser permet à l’auteur de contenu de créer facilement un teaser vers un contenu supplémentaire à l’aide d’une image, d’un titre ou d’un texte enrichi et de lier un contenu supplémentaire ou d’autres actions.

L’auteur du modèle peut utiliser la [boîte de dialogue de conception](#design-dialog) définir si les options permettant de créer des actions à appeler et d’ajouter des liens sont disponibles, ainsi que de désactiver diverses options d’affichage. L’auteur du contenu peut utiliser la [boîte de dialogue Configurer](#configure-dialog) pour définir une image, des CTAS, des titres et descriptions et configurer des liens vers le teaser individuel. Vous pouvez accéder à la [boîte de dialogue de modification](image.md#edit-dialog) du [composant Image](image.md) pour modifier l’image de teaser.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Teaser est v1, qui a été introduite avec la version 2.1.0 des composants principaux de juillet 2018 et est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatible | Compatible | Compatible |

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant Teaser et obtenir des exemples de ses options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_teaser).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant du teaser [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

L’auteur du contenu peut utiliser la boîte de dialogue de configuration pour définir les propriétés du teaser individuel. Il existe également une [boîte de dialogue de modification](#edit-dialog) pour modifier l’image de teaser si celle-ci est sélectionnée.

### Image {#image}

![Onglet d’image de la boîte de dialogue de modification du composant Teaser](/help/assets/teaser-edit-image.png)

* **Ressource image**
   * Déposez un fichier depuis l’[explorateur de ressources](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) ou appuyez sur l’option **parcourir** pour effectuer un téléchargement à partir d’un système de fichiers local.
   * Appuyez ou cliquez sur **Effacer** pour désélectionner l’image actuellement sélectionnée.
   * Appuyez ou cliquez sur **Modifier** pour [gérer les rendus de la ressource](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) dans l’éditeur de ressources.

### Texte {#text}

![Onglet Modifier la boîte de dialogue du composant Teaser](/help/assets/teaser-edit-text.png)

* **Prétitre** - Le prétitre s&#39;affiche avant le titre du teaser.
* **Titre** - Définit un titre à afficher en tant que titre pour le teaser.
   * **Obtenir le titre de la page** liée : lorsque cette option est sélectionnée, le titre est renseigné avec le titre de la page liée.
* **Description** - Définit une description à afficher en tant que sous-titre du teaser.
   * **Obtenir la description à partir de la page** liée : si cette option est cochée, la description sera renseignée avec la description de la page liée.
* **ID** : cette option permet de contrôler l&#39;identifiant unique du composant dans le code HTML et dans la couche [de](/help/developing/data-layer/overview.md)données.
   * Si rien n’est indiqué, un identifiant unique est automatiquement généré et peut être trouvé en examinant la page qui en résulte.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

### Liens et actions {#links-actions}

![Onglet de lien de la boîte de dialogue Modifier du composant Teaser](/help/assets/teaser-edit-link.png)

* **Lien** - Lien appliqué au teaser. Utilisez le navigateur de chemins pour sélectionner la cible du lien.
* **Activer les appels à l&#39;action** : lorsque cette option est cochée, elle active la définition des appels à l&#39;action. Le premier lien Appel à action de la liste est utilisé comme lien pour d’autres éléments de teaser.

## Boîte de dialogue de modification {#edit-dialog}

Le composant Teaser délègue le rendu d’image au [Composant Image](image.md). Par conséquent, [la boîte de dialogue de modification] (image.md#edit-dialog du composant Image est accessible à l’auteur du contenu pour manipuler l’image de teaser).

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les options de teaser que l’auteur du contenu a définies lors de l’utilisation de ce composant.

### Onglet Teaser {#teaser-tab}

![Boîte de dialogue de conception du composant Teaser](/help/assets/teaser-design.png)

* **Appels à l’action**
   * **Désactiver les appels à l&#39;action** - Masquer l&#39;option **Appel à l&#39;action** pour les auteurs de contenu
* **Eléments**
   * **Masquer le prétitre** - Masque l’option de **prétitre** pour les auteurs de contenu
   * **Masquer le titre** - Masque l&#39;option **Titre** pour les auteurs de contenu
      * Lorsqu’il est sélectionné, **le type de titre** est masqué.
   * **Masquer la description** - Masquer l&#39;option **Description** pour les auteurs de contenu
* **Type** de titre : définit la balise H à utiliser par le titre du teaser.
* **Liens**
   * **Ne pas lier l&#39;image** : lorsque cette option est sélectionnée, l&#39;image de teaser n&#39;est pas liée.
   * **Ne pas lier le titre** - Lorsqu&#39;il est sélectionné, le titre du teaser n&#39;est pas lié
* **Image Delegate** - Affichage d’informations indiquant à quel composant le Teaser délègue la gestion des images.

### Onglet Styles {#styles-tab}

Le composant Teaser prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.
