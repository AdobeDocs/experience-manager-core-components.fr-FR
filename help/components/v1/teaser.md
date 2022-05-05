---
title: Composant Teaser (v1)
description: Le composant Teaser peut afficher une image, un titre, un texte enrichi et éventuellement un lien vers un contenu supplémentaire.
role: Architect, Developer, Admin, User
exl-id: 48e56938-660a-43e7-9e62-8069283ae73f
source-git-commit: 84e09fa64b3a7ae40ff3ff1a04ea1c7504db29d2
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 97%

---

# Composant Teaser (v1) {#teaser-component}

Le composant principal Teaser peut afficher une image, un titre, un texte enrichi et éventuellement un lien vers un contenu supplémentaire.

## Utilisation {#usage}

Le composant Teaser permet à l’auteur de contenu de créer facilement un teaser vers un contenu supplémentaire à l’aide d’une image, d’un titre ou d’un texte enrichi et de lier un contenu supplémentaire ou d’autres actions.

L’auteur du modèle peut utiliser la [boîte de dialogue de conception](#design-dialog) définir si les options permettant de créer des actions à appeler et d’ajouter des liens sont disponibles, ainsi que de désactiver diverses options d’affichage. L’auteur du contenu peut utiliser la [boîte de dialogue Configurer](#configure-dialog) pour définir une image, des CTAS, des titres et descriptions et configurer des liens vers le teaser individuel. Vous pouvez accéder à la [boîte de dialogue de modification](image-v1.md#edit-dialog) du [composant Image](image-v1.md) pour modifier l’image de teaser.

## Version et compatibilité {#version-and-compatibility}

Ce document décrit la version v1 du composant Teaser, qui a été introduite avec la version 2.1.0 des composants principaux en juillet 2018.

>[!CAUTION]
>
>Ce document décrit la version v1 du composant Teaser.
>
>Pour plus d’informations sur la version actuelle du composant Teaser, consultez le document [Composant Teaser](/help/components/teaser.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant Teaser et obtenir des exemples de ses options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_teaser_fr).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Teaser [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

L’auteur du contenu peut utiliser la boîte de dialogue de configuration pour définir les propriétés du teaser individuel. Il existe également une [boîte de dialogue de modification](#edit-dialog) pour modifier l’image de teaser si celle-ci est sélectionnée.

### Image {#image}

![Onglet Image de la boîte de dialogue de modification du composant Teaser](/help/assets/teaser-edit-image.png)

* **Ressource image**
   * Déposez un fichier depuis l’[explorateur de ressources](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=fr) ou appuyez sur l’option **parcourir** pour effectuer un téléchargement à partir d’un système de fichiers local.
   * Appuyez ou cliquez sur **Effacer** pour désélectionner l’image actuellement sélectionnée.
   * Appuyez ou cliquez sur **Modifier** pour [gérer les rendus de la ressource](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=fr) dans l’éditeur de ressources.

>[!NOTE]
>
>Actuellement, les [fonctionnalités Dynamic Media](image-v1.md#dynamic-media) ne sont pas disponibles dans le composant Teaser.

### Texte {#text}

![Onglet Texte de la boîte de dialogue de modification du composant Teaser](/help/assets/teaser-edit-text.png)

* **Prétitre** : s’affiche avant le titre du teaser.
* **Titre** : titre à afficher comme titre du teaser.
   * **Obtenir le titre depuis la page liée** : lorsque cette option est cochée, le titre de la page liée est utilisé comme titre.
* **Description** : définit une description à afficher sous forme de sous-titre du teaser.
   * **Obtenir la description depuis la page liée** : lorsque cette option est cochée, la description de la page liée est utilisée comme description.
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

### Liens et actions {#links-actions}

![Onglet Lien de la boîte de dialogue de modification du composant Teaser](/help/assets/teaser-edit-link.png)

* **Lien** : lien appliqué au teaser. Utilisez le navigateur de chemins pour sélectionner la cible du lien.
* **Activer les appels à l’action** : lorsque cette option est cochée, elle permet la définition d’appels à l’action. Le premier lien Appel à action de la liste est utilisé comme lien pour d’autres éléments de teaser.

## Boîte de dialogue de modification {#edit-dialog}

Le composant Teaser délègue le rendu d’image au [Composant Image](image-v1.md). Par conséquent, la variable [Modifier la boîte de dialogue](image-v1.md#edit-dialog) L’auteur du contenu peut utiliser du composant Image pour manipuler l’image de teaser.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les options de teaser que l’auteur du contenu a définies lors de l’utilisation de ce composant.

### Onglet Teaser {#teaser-tab}

![Boîte de dialogue de conception du composant Teaser](/help/assets/teaser-design.png)

* **Appels à l’action**
   * **Désactiver les appels à l’action** : masque l’option **Appels à l’action** pour les auteurs de contenu.
* **Éléments**
   * **Masquer le prétitre** : masque l’option **Prétitre** pour les auteurs de contenu.
   * **Masquer le titre** : masque l’option **Titre** pour les auteurs de contenu.
      * Lorsque cette option est sélectionnée, le **Type de titre** est masqué.
   * **Masquer la description** : masque l’option **Description** pour les auteurs de contenu.
* **Type de titre** : définit la balise H que le titre du teaser doit utiliser.
* **Liens**
   * **Ne pas lier l’image** : lorsque cette option est sélectionnée, l’image de teaser n’est pas liée.
   * **Ne pas lier le titre** : lorsque cette option est sélectionnée, le titre du teaser n’est pas lié.
* **Délégué d’image** : affichage d’informations indiquant à quel composant le teaser délègue la gestion des images.

### Onglet Styles {#styles-tab}

Le composant Teaser prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

## Couche de données client Adobe {#data-layer}

Le composant Teaser prend en charge la [couche de données client Adobe](/help/developing/data-layer/overview.md).
