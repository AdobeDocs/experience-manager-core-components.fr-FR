---
title: Composant Teaser de message électronique
description: Le composant Teaser de courrier électronique peut afficher une image, un titre, du texte enrichi et éventuellement un lien vers un contenu supplémentaire.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '1056'
ht-degree: 53%

---


# Composant Teaser de message électronique {#email-teaser-component}

Le composant Teaser de courrier électronique peut afficher une image, un titre, du texte enrichi et éventuellement un lien vers un contenu supplémentaire.

## Utilisation {#usage}

Le composant Teaser de message électronique permet à l’auteur de contenu de créer facilement un teaser à l’aide d’une image, d’un titre ou d’un texte enrichi, et de lier un contenu supplémentaire ou d’autres actions.

* L’auteur du modèle peut utiliser la [boîte de dialogue de conception](#design-dialog) définir si les options permettant de créer des actions à appeler et d’ajouter des liens sont disponibles, ainsi que de désactiver diverses options d’affichage.
* L’auteur du contenu peut utiliser la [boîte de dialogue Configurer](#configure-dialog) pour définir une image, des CTAS, des titres et descriptions et configurer des liens vers le teaser individuel.
* Le [Modifier la boîte de dialogue](image.md#edit-dialog) de [Composant d’image de message électronique](image.md) est accessible pour modifier l’image de teaser.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Teaser d’email est v1, qui a été introduite avec la version x des composants principaux d’email en octobre 2022. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatible | Compatible |

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant Teaser d’email et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [Bibliothèque de composants.](https://adobe.com/go/aem_cmp_library_email_teaser)

### Détails techniques {#technical-details}

Documentation technique la plus récente sur le composant Teaser d’email [est disponible sur GitHub.](https://adobe.com/go/aem_cmp_tech_email_teaser_v1)

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux.](/help/developing/overview.md)

## Boîte de dialogue de configuration {#configure-dialog}

L’auteur du contenu peut utiliser la boîte de dialogue de configuration pour définir les propriétés du teaser individuel. Il existe également une [boîte de dialogue de modification](#edit-dialog) pour modifier l’image de teaser si celle-ci est sélectionnée.

### Onglet Liens {#links-tab}

![Onglet Liens de la boîte de dialogue de modification du composant Teaser de courrier électronique](/help/email/assets/email-teaser-edit-links.png)

Le titre, la description et l’image du teaser peuvent être hérités du contenu lié ou du contenu lié dans le premier appel à l’action. Si aucun lien ni appel à l’action n’est spécifié, le titre, la description et l’image seront hérités du contenu actuel.

* **Lien** - Ce fichier est lié au contenu, à l’URL externe ou à l’ancre.
   * Cliquez sur l’icône Campagne pour ouvrir la [Sélectionner la variable Adobe Campaign](/help/email/campaign-variables.md) pour insérer du contenu dynamique depuis Adobe Campaign.
* **Appels à l’action** : cette option permet de créer des liens vers plusieurs destinations.
   * La page liée dans le premier appel à l’action est utilisée pour hériter du titre, de la description ou de lʼimage du teaser.
   * Cliquez sur l’icône Campagne pour ouvrir la [Sélectionner la variable Adobe Campaign](/help/email/campaign-variables.md) pour insérer du contenu dynamique depuis Adobe Campaign.

### Onglet Texte {#text-tab}

![Onglet Texte de la boîte de dialogue de modification du composant Teaser de courrier électronique](/help/email/assets/email-teaser-edit-text.png)

* **Prétitre** : s’affiche avant le titre du teaser.
* **Titre** : titre à afficher comme titre du teaser.
   * Cliquez sur l’icône Campagne pour ouvrir la [Sélectionner la variable Adobe Campaign](/help/email/campaign-variables.md) pour insérer du contenu dynamique depuis Adobe Campaign.
   * **Obtenir le titre depuis la page liée** : lorsque cette option est cochée, le titre de la page liée est utilisé comme titre.
* **Description** : définit une description à afficher sous forme de sous-titre du teaser.
   * Cliquez sur le bouton **Sélectionner la variable Adobe Campaign** pour ouvrir la [Sélectionner la variable Adobe Campaign](/help/email/campaign-variables.md) pour insérer du contenu dynamique depuis Adobe Campaign.
   * **Obtenir la description depuis la page liée** : lorsque cette option est cochée, la description de la page liée est utilisée comme description.
* **ID** - Cette option permet de contrôler l’identifiant unique du composant dans le HTML.
   * Si rien n’est indiqué, un identifiant unique est automatiquement généré et peut être trouvé en examinant le contenu qui en résulte.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur CSS.

### Onglet Contenu {#asset-tab}

![Onglet Image de la boîte de dialogue de modification du composant Teaser d’email](/help/email/assets/email-teaser-edit-image.png)

* **Hériter l’image en vedette de la page** : utilisez l’image définie dans les propriétés de page de la page liée ou de la page active si aucune image n’est trouvée.
* **Ressource image** : déposez un fichier depuis l’[explorateur de ressources](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=fr) ou appuyez sur l’option **parcourir** pour effectuer un chargement à partir d’un système de fichiers local.
   * Appuyez ou cliquez sur **Effacer** pour désélectionner l’image actuellement sélectionnée.
   * Appuyez ou cliquez sur **Modifier** to [gestion des rendus de la ressource](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=fr) dans l’Éditeur de ressources.
* **Texte secondaire pour l’accessibilité** : ce champ vous permet de fournir une description de l’image pour les utilisateurs souffrant de déficience visuelle.
   * **Hériter le texte secondaire de la page** : cette option utilise la description secondaire de la valeur de la ressource liée des métadonnées `dc:description` dans la gestion des ressources numériques (DAM) ou de la page active si aucune ressource n’est liée.
* **Ne pas fournir de texte secondaire** : cette option marque lʼimage afin quʼelle soit ignorée par les technologies dʼassistance, comme les lecteurs dʼécran, dans les cas où lʼimage existe à des fins dʼillustration et ne comporte pas de signification particulière.

>[!NOTE]
>
>Actuellement, les [fonctionnalités Dynamic Media](image.md#dynamic-media) ne sont pas disponibles dans le composant Teaser.

### Onglet Styles {#styles-tab-edit}

Le composant Teaser de courrier électronique prend en charge l’AEM [Système de style.](/help/get-started/authoring.md#component-styling)

Utilisez la liste déroulante pour sélectionner les styles à appliquer au composant. Les sélections effectuées dans la boîte de dialogue de modification ou dans la barre d’outils du composant ont le même effet.

Les styles doivent être configurés pour ce composant dans la variable [boîte de dialogue de conception](#design-dialog) pour que l’onglet soit disponible.

## Boîte de dialogue de modification {#edit-dialog}

Le composant Teaser de courrier électronique délègue le rendu de l’image à la fonction [Composant d’image](image.md). Par conséquent, la [boîte de dialogue Modifier](image.md#edit-dialog) du composant Image est accessible pour permettre à l’auteur du contenu de manipuler l’image de teaser.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les options de teaser que l’auteur du contenu a définies lors de l’utilisation de ce composant.

### Onglet Teaser {#teaser-tab}

![Boîte de dialogue de conception du composant Email Teaser](/help/email/assets/email-teaser-design.png)

* **Éléments d’en-tête autorisés** - Utilisez la liste déroulante pour définir les éléments de HTML d’en-tête qui peuvent être sélectionnés par un auteur pour le type de titre du teaser.
* **Elément d’en-tête par défaut du titre** : élément de HTML d’en-tête par défaut utilisé pour le type de titre du teaser.
* **Appels à l’action**
   * **Désactiver les appels à l’action** : masque l’option **Appels à l’action** pour les auteurs de contenu.
* **Éléments**
   * **Masquer le prétitre** : masque l’option **Prétitre** pour les auteurs de contenu.
   * **Masquer le titre** : masque l’option **Titre** pour les auteurs de contenu.
      * Lorsque cette option est sélectionnée, le **Type de titre** est masqué.
   * **Afficher le type de titre**
   * **Masquer la description** : masque l’option **Description** pour les auteurs de contenu.
* **Délégation d’image** - Affichage d’informations indiquant à quel composant le teaser de message électronique délègue la gestion des images.

### Onglet Styles {#styles-tab}

Le composant Teaser de courrier électronique prend en charge l’AEM [Système de style.](/help/get-started/authoring.md#component-styling)
