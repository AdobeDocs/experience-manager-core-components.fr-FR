---
title: Composant d’image de message électronique
description: Le composant d’image de courrier électronique est un composant d’image adaptatif qui permet d’effectuer des modifications statiques.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '1683'
ht-degree: 63%

---


# Composant d’image de message électronique {#email-image-component}

Le composant d’image de courrier électronique est un composant d’image adaptatif qui permet d’effectuer des modifications statiques.

## Utilisation {#usage}

Le composant d’image de courrier électronique comprend une sélection d’image adaptative et un comportement réactif avec chargement différé pour le visiteur de la page, ainsi qu’un placement d’image par glisser-déposer et une configuration simples pour l’auteur du contenu.

* Les largeurs d’image et les paramètres supplémentaires peuvent être définis par l’auteur du modèle dans la [boîte de dialogue de conception.](#design-dialog)
* L’éditeur de contenu peut charger ou sélectionner des ressources dans la [boîte de dialogue de configuration.](#configure-dialog)

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant d’image d’email est v1, qui a été introduite avec la version x des composants principaux d’email en octobre 2022. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatible | Compatible |

Pour plus d’informations sur les versions et versions des composants principaux, consultez le document . [Courrier électronique des versions des composants principaux](/help/email/versions.md).

## Fonctions réactives {#responsive-features}

Le composant d’image d’email est fourni avec des fonctionnalités réactives puissantes prêtes à l’emploi. Au niveau du modèle de page, la [boîte de dialogue de conception](#design-dialog) permet de définir les largeurs par défaut du fichier image. Le composant d’image de courrier électronique charge alors automatiquement la largeur correcte à afficher en fonction de la taille de la fenêtre du navigateur. Lorsque la fenêtre est redimensionnée, le composant d’image d’email charge dynamiquement la taille d’image correcte à la volée. Les développeurs de composants n’ont pas besoin de se soucier de la définition de requêtes multimédias personnalisées, car le composant d’image d’email est déjà optimisé pour charger votre contenu.

En outre, le composant d’image de courrier électronique prend en charge le chargement différé pour différer le chargement de la ressource d’image réelle jusqu’à ce qu’elle soit visible dans le navigateur, ce qui augmente la réactivité de votre contenu.

>[!TIP]
>
>Par défaut, le composant d’image de courrier électronique est optimisé par la servlet d’image adaptative. Veuillez consulter le document [Servlet d’image adaptative](#adaptive-image-servlet) pour plus d’informations sur son fonctionnement.

## Prise en charge de Dynamic Media {#dynamic-media}

Le composant Image de courrier électronique prend en charge [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/dynamic-media.html?lang=fr#dynamicmedia) ressources. [Lorsqu’elles sont activées](#design-dialog), ces fonctionnalités offrent la possibilité d’ajouter des fichiers d’image Dynamic Media par un simple glisser-déposer ou par le biais du navigateur de ressources, comme vous le feriez pour toute autre image. En outre, les modificateurs d’image, les paramètres d’image prédéfinis et les recadrages intelligents sont également pris en charge.

Vos expériences e-mail créées à l’aide des composants principaux d’email peuvent offrir des fonctionnalités d’image Dynamic Media sur plusieurs plateformes riches, optimisées par Sensei, robustes, hautement performantes.

## Prise en charge SVG {#svg-support}

Les graphiques vectoriels évolutifs (SVG) sont pris en charge par le composant Image d’email.

* Les opérations de glisser-déplacer d’une ressource SVG à partir de DAM et le chargement d’un fichier SVG depuis un système de fichiers local sont pris en charge.
* Le fichier SVG d’origine est diffusé en continu (les transformations sont ignorées).
* Pour une image SVG, les « images intelligentes » et les « tailles intelligentes » sont définies sur un tableau vide dans le modèle d’image.

### Sécurité {#security}

Pour des raisons de sécurité, l’éditeur d’image ne fait jamais appel au fichier SVG d’origine. Il est appelé par `<img src=“path-to-component”>`. Cela empêche le navigateur d’exécuter les scripts incorporés dans le fichier SVG.

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant d’image d’email et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la page [Bibliothèque de composants.](https://adobe.com/go/aem_cmp_library_email_image)

### Détails techniques {#technical-details}

Documentation technique la plus récente sur le composant Image d’email [est disponible sur GitHub.](https://adobe.com/go/aem_cmp_tech_email_image_v1)

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux.](/help/developing/overview.md)

Le composant d’image prend en charge les [microdonnées schéma.org.](https://schema.org)

## Boîte de dialogue de configuration {#configure-dialog}

Le composant d’image de courrier électronique propose une boîte de dialogue de configuration dans laquelle l’image elle-même est définie, ainsi que sa description et ses propriétés de base.

### Onglet Contenu {#asset-tab}

![Onglet Ressource de la boîte de dialogue de configuration du composant Image de courrier électronique](/help/email/assets/email-image-configure-asset.png)

* **Hériter l’image en vedette de la page** : si vous cochez cette option, lʼ[image en vedette de la page liée](page.md) ou l’image de la page active si l’image n’est pas liée est utilisée.

* **Texte secondaire pour l’accessibilité** : ce champ vous permet de fournir une description de l’image pour les utilisateurs souffrant de déficience visuelle.

   * **Hériter le texte secondaire de la page** : cette option utilise la description secondaire de la valeur de la ressource liée des métadonnées `dc:description` dans la gestion des ressources numériques (DAM) ou de la page active si aucune ressource n’est liée.

* **Ressource image**
   * Déposez un fichier depuis l’[explorateur de ressources](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=fr) ou appuyez sur l’option **parcourir** pour effectuer un téléchargement à partir d’un système de fichiers local.
   * Appuyez ou cliquez sur **Effacer** pour désélectionner l’image actuellement sélectionnée.
   * Appuyez ou cliquez sur **Modifier** to [gestion des rendus de la ressource](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=fr) dans l’Éditeur de ressources.

* **Ne pas fournir de texte secondaire** : cette option marque lʼimage afin quʼelle soit ignorée par les technologies dʼassistance, comme les lecteurs dʼécran, dans les cas où lʼimage existe à des fins dʼillustration et ne comporte pas de signification particulière.

* **Désactiver le chargement différé** - Cette option précharge tous les composants d’image sans les charger au besoin.

### Onglet Métadonnées {#metadata-tab}

![Onglet Métadonnées de la boîte de dialogue de configuration du composant Image](/help/email/assets/email-image-configure-metadata.png)

* **Type de paramètre prédéfini** : définit les types de paramètres d’image prédéfinis disponibles, soit **Paramètre d’image prédéfini** ou **Recadrage intelligent** et n’est disponible que lorsque les [fonctionnalités de Dynamic Media](#dynamic-meida) sont activées.
   * **Paramètre d’image prédéfini** - Lorsque **Type de paramètre prédéfini** de **Paramètre d’image prédéfini** est sélectionné, la liste déroulante **Paramètre d’image prédéfini** est disponible, ce qui permet de sélectionner les paramètres prédéfinis Dynamic Media disponibles. Cette option n’est disponible que si des paramètres prédéfinis sont définis pour la ressource sélectionnée.
   * **Recadrage intelligent** - Lorsque **Type de paramètre prédéfini** de **Recadrage intelligent** est sélectionné dans la liste déroulante **Rendu** est disponible, ce qui permet de sélectionner les rendus disponibles de la ressource sélectionnée. Cette option n’est disponible que si des rendus sont définis pour la ressource sélectionnée.
   * **Modificateurs d’image** - D’autres commandes de service d’images Dynamic Media peuvent être définies ici, séparées par des `&`, quelle que soit la **Type de paramètre prédéfini** est sélectionnée.
* **Légende** : des informations supplémentaires sur l’image sont affichées par défaut sous l’image.
   * **Obtenir la légende à partir de DAM** : lorsque cette option est cochée, le texte de légende de l’image est renseigné avec la valeur des métadonnées `dc:title` dans DAM. Disponible uniquement lorsqu’une ressource est sélectionnée dans la gestion des ressources numériques.
   * **Afficher la légende dans une fenêtre contextuelle** : si cette option est activée, la légende ne s’affiche pas sous l’image, mais dans une fenêtre contextuelle, dans certains navigateurs, lorsque vous pointez sur l’image.
* **Lien** : lier l’image à une autre ressource.
   * Utilisez la boîte de dialogue de sélection pour créer un lien vers une autre ressource AEM.
   * Si vous ne créez pas de lien vers une ressource AEM, saisissez l’URL absolue. Les URL non absolues seront interprétées comme relatives à AEM.
   * **Ouvrir le lien dans un nouvel onglet** : cette option ouvre le lien dans une nouvelle fenêtre du navigateur.
* **ID** - Cette option permet de contrôler l’identifiant unique du composant dans le HTML.
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur CSS.
* **Corrigé en** - Cette option définit la largeur en pixels de l’image.
* **Mettre l’image à l’échelle en fonction de la largeur disponible** - Cette option s’applique `"width":"100%"` à l’attribut de style d’image.

>[!TIP]
>
>Les options **Recadrage intelligent** et **Paramètre d’image prédéfini** s’excluent mutuellement. Si un auteur doit utiliser un paramètre d’image prédéfini associé à un rendu avec recadrage dynamique, il devra utiliser les **modificateurs d’image** pour ajouter manuellement ce paramètre.

### Onglet Styles {#styles-tab-edit}

![Onglet Styles de la boîte de dialogue de modification du composant Image d’email](/help/assets/image-configure-styles.png)

Le composant Image de courrier électronique prend en charge l’AEM [Système de style.](/help/get-started/authoring.md#component-styling)

Utilisez la liste déroulante pour sélectionner les styles à appliquer au composant. Les sélections effectuées dans la boîte de dialogue de modification ou dans la barre d’outils du composant ont le même effet.

Les styles doivent être configurés pour ce composant dans la variable [boîte de dialogue de conception](#design-dialog) pour que l’onglet soit disponible.

## Boîte de dialogue de conception {#design-dialog}

### Onglet Principal {#main-tab}

![Onglet principal de la boîte de dialogue de conception du composant Image](/help/email/assets/email-image-design-main.png)

* **Activer les fonctionnalités DM** : lorsque cette option est cochée, les [fonctionnalités Dynamic Media](#dynamic-media) sont disponibles.
   * Dynamic Media doit être activé dans l’environnement pour que cette option apparaisse.
* **Activer les images optimisées pour le web** : lorsque cette case est cochée, [le service de diffusion d’images optimisées pour le web](/help/developing/web-optimized-image-delivery.md) ; diffusera les images au format WebP, réduisant ainsi la taille moyenne des images de 25 %.
   * Cette option est disponible uniquement dans AEMaaCS.
   * Si cette option est décochée ou si le service de diffusion d’images optimisé pour le web n’est pas disponible, la variable [Servlet d’image adaptative](/help/developing/adaptive-image-servlet.md) est utilisée.
* **L’image est décorative** : définissez si l’option d’image décorative est activée automatiquement lors de l’ajout du composant d’image à une page.
* **Obtenir un texte alternatif à partir de DAM** : définissez si l’option permettant de récupérer le texte de remplacement de DAM est automatiquement activée lors de l’ajout du composant d’image à une page.
* **Obtenir la légende à partir de DAM** : définissez si l’option permettant de récupérer la légende à partir de DAM est automatiquement activée lors de l’ajout du composant d’image à une page.
* **Afficher la légende dans une fenêtre contextuelle** : définissez si l’option permettant d’afficher la légende d’image est automatiquement activée lors de l’ajout du composant d’image à une page.
* **Redimensionner la largeur** : cette valeur est utilisée pour redimensionner la largeur des images de base qui sont des ressources DAM.
   * Les proportions des images sont conservées.
   * Si la valeur est supérieure à la largeur de l’image, cette valeur nʼa aucun effet.
   * Cette valeur n’a aucun effet sur les images au format SVG.

Vous pouvez définir une liste de largeurs en pixels pour l’image, le composant chargera alors automatiquement la largeur la plus appropriée en fonction de la taille du navigateur. Il s’agit d’une partie importante de la [fonctionnalités réactives](#responsive-features) du composant Image de courrier électronique.

* **Largeurs** : définit une liste de largeurs en pixels pour l’image ; le composant charge automatiquement la largeur la plus appropriée en fonction de la taille du navigateur.
   * Appuyez ou cliquez sur le bouton **Ajouter** pour ajouter une autre taille.
      * Utilisez les poignées de capture pour réorganiser l’ordre des tailles.
      * Utilisez l’icône **Supprimer** pour supprimer une largeur.
   * Par défaut, le chargement des images est différé jusqu’à ce qu’elles deviennent visibles.
      * Sélectionnez l’option **Désactiver le chargement différé** pour charger les images au chargement de la page.
* **Qualité JPEG** : facteur de qualité (exprimé par un pourcentage entre 0 et 100) pour les images JPEG transformées (mises à l’échelle ou recadrées, par exemple).
* **Largeur par défaut** - Largeur par défaut des images, exprimée en pixels, qui sera utilisée dans la boîte de dialogue de conception

>[!TIP]
>
>Reportez-vous au document [Servlet Image adaptative](/help/developing/adaptive-image-servlet.md) pour obtenir des conseils sur l’optimisation de la sélection du rendu en définissant soigneusement vos largeurs.

### Onglet Styles {#styles-tab}

Le composant Image de courrier électronique prend en charge l’AEM [Système de style](/help/get-started/authoring.md#component-styling).