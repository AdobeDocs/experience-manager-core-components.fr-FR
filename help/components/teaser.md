---
title: Composant Teaser
description: Le composant Teaser peut afficher une image, un titre, un texte enrichi et éventuellement un lien vers un contenu supplémentaire.
role: Architect, Developer, Admin, User
exl-id: ec75e168-6f3b-4dff-8df6-06ca7dc18688
source-git-commit: cfc86203051739cbcdc30be0fb10ccffa7d583a5
workflow-type: ht
source-wordcount: '988'
ht-degree: 100%

---

# Composant Teaser {#teaser-component}

Le composant principal Teaser peut afficher une image, un titre, un texte enrichi et éventuellement un lien vers un contenu supplémentaire.

## Utilisation {#usage}

Le composant Teaser permet à l’auteur de contenu de créer facilement un teaser vers un contenu supplémentaire à l’aide d’une image, d’un titre ou d’un texte enrichi et de lier un contenu supplémentaire ou d’autres actions.

L’auteur du modèle peut utiliser la [boîte de dialogue de conception](#design-dialog) définir si les options permettant de créer des actions à appeler et d’ajouter des liens sont disponibles, ainsi que de désactiver diverses options d’affichage. L’auteur du contenu peut utiliser la [boîte de dialogue Configurer](#configure-dialog) pour définir une image, des CTAS, des titres et descriptions et configurer des liens vers le teaser individuel. Vous pouvez accéder à la [boîte de dialogue de modification](image.md#edit-dialog) du [composant Image](image.md) pour modifier l’image de teaser.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Teaser est v2, qui a été introduite avec la version 2.18.0 des composants principaux en février 2022. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v2 | - | Compatible | Compatible |
| [v1](v1/teaser.md) | Compatible | Compatible | Compatible |

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant Teaser et obtenir des exemples de ses options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_teaser_fr).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Teaser [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

L’auteur du contenu peut utiliser la boîte de dialogue de configuration pour définir les propriétés du teaser individuel. Il existe également une [boîte de dialogue de modification](#edit-dialog) pour modifier l’image de teaser si celle-ci est sélectionnée.

### Onglet Liens {#links-tab}

![Onglet Liens de la boîte de dialogue de modification du composant Teaser](/help/assets/teaser-edit-links.png)

Le titre, la description et l’image du teaser peuvent être hérités de la page liée ou de la page liée dans le premier appel à l’action. Si aucun lien ni appel à l’action n’est spécifié, le titre, la description et l’image seront hérités de la page active.

* **Lien** : ce fichier établit un lien vers une page de contenu, une URL externe ou une ancre de page.
* **Ouvrir le lien dans un nouvel onglet** : si cette option est activée, le lien s’ouvre dans un nouvel onglet du navigateur.
* **Appels à l’action** : cette option permet de créer des liens vers plusieurs destinations.
   * La page liée dans le premier appel à l’action est utilisée pour hériter du titre, de la description ou de lʼimage du teaser.

### Onglet Texte {#text-tab}

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

### Onglet Contenu {#asset-tab}

![Onglet Image de la boîte de dialogue de modification du composant Teaser](/help/assets/teaser-edit-image.png)

* **Hériter l’image en vedette de la page** : utilisez l’image définie dans les propriétés de page de la page liée ou de la page active si aucune image n’est trouvée.
* **Ressource image** : déposez un fichier depuis l’[explorateur de ressources](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=fr) ou appuyez sur l’option **parcourir** pour effectuer un chargement à partir d’un système de fichiers local.
   * Appuyez ou cliquez sur **Effacer** pour désélectionner l’image actuellement sélectionnée.
   * Appuyez ou cliquez sur **Modifier** pour [gérer les rendus de la ressource](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=fr) dans l’éditeur de ressources.
* **Texte secondaire pour l’accessibilité** : ce champ vous permet de fournir une description de l’image pour les utilisateurs souffrant de déficience visuelle.
   * **Hériter le texte secondaire de la page** : cette option utilise la description secondaire de la valeur de la ressource liée des métadonnées `dc:description` dans la gestion des ressources numériques (DAM) ou de la page active si aucune ressource n’est liée.
* **Ne pas fournir de texte secondaire** : cette option marque lʼimage afin quʼelle soit ignorée par les technologies dʼassistance, comme les lecteurs dʼécran, dans les cas où lʼimage existe à des fins dʼillustration et ne comporte pas de signification particulière.

### Onglet Styles {#styles-tab-edit}

![Onglet Styles de la boîte de dialogue de modification du composant Liste de teaser](/help/assets/teaser-edit-styles.png)

Le composant Teaser prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

Utilisez la liste déroulante pour sélectionner les styles à appliquer au composant. Les sélections effectuées dans la boîte de dialogue de modification ou dans la barre d’outils du composant ont le même effet.

Pour que le menu déroulant soit disponible, les styles doivent être configurés pour ce composant dans la [boîte de dialogue de conception](#design-dialog).

## Boîte de dialogue de modification {#edit-dialog}

Le composant Teaser délègue le rendu d’image au [Composant Image](image.md). Par conséquent, [la boîte de dialogue de modification](image.md#edit-dialog) du composant Image est accessible à l’auteur du contenu pour manipuler l’image de teaser.

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
* **Type de titre par défaut** : définit la balise H que le titre du teaser doit utiliser.
* **Délégué d’image** : affichage d’informations indiquant à quel composant le teaser délègue la gestion des images.

### Onglet Styles {#styles-tab}

Le composant Teaser prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

## Couche de données client Adobe {#data-layer}

Le composant Teaser prend en charge la [couche de données client Adobe](/help/developing/data-layer/overview.md).
