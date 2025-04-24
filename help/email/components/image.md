---
title: Composant Image d’e-mail
description: Le composant Image d’e-mail est un composant d’image adaptatif qui permet d’effectuer des modifications statiques.
role: Architect, Developer, Admin, User
exl-id: f5d40047-3082-4edd-a5f6-6ab3e33997f9
source-git-commit: 91969e4956bef1a511b8d588d5290a7999bf86ec
workflow-type: tm+mt
source-wordcount: '1624'
ht-degree: 99%

---


# Composant Image d’e-mail {#email-image-component}

Le composant Image d’e-mail est un composant d’image adaptatif qui permet d’effectuer des modifications statiques.

## Utilisation {#usage}

Le composant Image d’e-mail comprend une sélection d’images adaptative, un comportement réactif avec chargement différé pour le visiteur de la page, ainsi qu’un placement et une configuration d’images faciles par glisser-déposer pour le créateur de contenu.

* Les largeurs d’image et les paramètres supplémentaires peuvent être définis par le créateur du modèle dans la [boîte de dialogue de conception.](#design-dialog)
* L’éditeur de contenu peut charger ou sélectionner des ressources dans la [boîte de dialogue de configuration.](#configure-dialog)

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Image d’e-mail est v1. Celle-ci a été introduite avec la version X des composants principaux d’e-mail en octobre 2022. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatible | - | - |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux d’e-mail](/help/email/versions.md).

## Fonctions réactives {#responsive-features}

Le composant Image d’e-mail s’accompagne de fonctions réactives, efficaces et prêtes à l’emploi. Au niveau du modèle de page, la [boîte de dialogue de conception](#design-dialog) permet de définir les largeurs par défaut du fichier image. Le composant Image d’e-mail charge alors automatiquement la largeur correcte à afficher en fonction de la taille de la fenêtre du navigateur. Lorsque la fenêtre est redimensionnée, le composant Image d’e-mail charge dynamiquement la taille d’image à la volée. Les développeurs de composants n’ont pas à définir des requêtes multimédias personnalisées, puisque le composant Image d’e-mail est déjà optimisé pour charger le contenu.

En outre, le composant Image d’e-mail prend en charge le chargement différé, de façon à différer le chargement du fichier image réel jusqu’à ce qu’il soit visible dans le navigateur. Cela a pour effet d’augmenter la réactivité votre contenu.

>[!TIP]
>
>Par défaut, le composant Image d’e-mail est optimisé par le servlet d’image adaptative. Veuillez consulter le document [Servlet d’image adaptative](#adaptive-image-servlet) pour plus d’informations sur son fonctionnement.

## Prise en charge de Dynamic Media {#dynamic-media}

Le composant Image d’e-mail prend en charge les ressources [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/dynamic-media.html?lang=fr#dynamicmedia). [Lorsqu’elles sont activées](#design-dialog), ces fonctionnalités offrent la possibilité d’ajouter des fichiers d’image Dynamic Media par un simple glisser-déposer ou par le biais du navigateur de ressources, comme vous le feriez pour toute autre image. En outre, les modificateurs d’image, les paramètres d’image prédéfinis et les recadrages intelligents sont également pris en charge.

Vos expériences e-mail créées avec les composants principaux d’e-mail bénéficient des fonctionnalités d’image Dynamic Media sur plusieurs plateformes. Elles sont hautement performantes, robustes, enrichies et optimisées par Sensei.

## Prise en charge SVG {#svg-support}

Les formats SVG (Scalable Vector Graphics) sont pris en charge par le composant Image d’e-mail.

* Les opérations de glisser-déplacer d’une ressource SVG à partir de DAM et le chargement d’un fichier SVG depuis un système de fichiers local sont pris en charge.
* Le fichier SVG d’origine est diffusé en continu (les transformations sont ignorées).
* Pour une image SVG, les « images intelligentes » et les « tailles intelligentes » sont définies sur un tableau vide dans le modèle d’image.

### Sécurité {#security}

Pour des raisons de sécurité, l’éditeur d’image ne fait jamais appel au fichier SVG d’origine. Il est appelé par `<img src=“path-to-component”>`. Cela empêche le navigateur d’exécuter les scripts incorporés dans le fichier SVG.

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Image d’e-mail [se trouve sur GitHub.](https://adobe.com/go/aem_cmp_tech_email_image_v1)

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux.](/help/developing/overview.md)

Le composant d’image prend en charge les [microdonnées schema.org.](https://schema.org)

## Boîte de dialogue de configuration {#configure-dialog}

Le composant Image d’e-email comprend une boîte de dialogue de configuration, qui fournit la définition, la description ainsi que les propriétés de base de lʼimage.

### Onglet Contenu {#asset-tab}

![Onglet Contenu de la boîte de dialogue de configuration du Composant Image d’e-mail](/help/email/assets/email-image-configure-asset.png)

* **Hériter l’image en vedette de la page** : si vous cochez cette option, lʼ[image en vedette de la page liée](page.md) ou l’image de la page active si l’image n’est pas liée est utilisée.

* **Texte secondaire pour l’accessibilité** : ce champ vous permet de fournir une description de l’image pour les utilisateurs souffrant de déficience visuelle.

   * **Hériter le texte secondaire de la page** : cette option utilise la description secondaire de la valeur de la ressource liée des métadonnées `dc:description` dans la gestion des ressources numériques (DAM) ou de la page active si aucune ressource n’est liée.

* **Ressource image**
   * Déposez un fichier depuis l’[explorateur de ressources](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=fr) ou appuyez sur l’option **parcourir** pour effectuer un téléchargement à partir d’un système de fichiers local.
   * Appuyez ou cliquez sur **Effacer** pour désélectionner l’image actuellement sélectionnée.
   * Appuyez ou cliquez sur **Modifier** pour [gérer les rendus de la ressource](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=fr) dans l’éditeur de ressources.

* **Ne pas fournir de texte secondaire** : cette option marque lʼimage afin quʼelle soit ignorée par les technologies dʼassistance, comme les lecteurs dʼécran, dans les cas où lʼimage existe à des fins dʼillustration et ne comporte pas de signification particulière.

* **Désactiver le chargement différé** : Cette option précharge tous les composants d’image sans les charger au besoin.

### Onglet Métadonnées {#metadata-tab}

![Onglet Métadonnées de la boîte de dialogue de configuration du composant Image](/help/email/assets/email-image-configure-metadata.png)

* **Type de paramètre prédéfini** : définit les types de paramètres d’image prédéfinis disponibles, soit **Paramètre d’image prédéfini** ou **Recadrage intelligent** et n’est disponible que lorsque les [fonctionnalités de Dynamic Media](#dynamic-meida) sont activées.
   * **Paramètre d’image prédéfini** : lorsque **Type de paramètre prédéfini** dans **Paramètre d’image prédéfini** est sélectionné, la liste déroulante **Paramètre d’image prédéfini** est disponible, ce qui permet de sélectionner les paramètres prédéfinis Dynamic Media disponibles. Cette option n’est disponible que si des paramètres prédéfinis sont définis pour la ressource sélectionnée.
   * **Recadrage intelligent** : lorsque **Type de paramètre prédéfini** dans **Recadrage intelligent** est sélectionné, la liste déroulante **Rendu** est disponible, ce qui permet de sélectionner les rendus disponibles de la ressource sélectionnée. Cette option n’est disponible que si des rendus sont définis pour la ressource sélectionnée.
   * **Modificateurs d’images** : il est possible de définir ici d’autres commandes de traitement d’images Dynamic Media, séparées par des caractères `&`, quel que soit le **type de paramètre prédéfini** sélectionné.
* **Légende** : des informations supplémentaires sur l’image sont affichées par défaut sous l’image.
   * **Obtenir la légende à partir de DAM** : lorsque cette option est cochée, le texte de légende de l’image est renseigné avec la valeur des métadonnées `dc:title` dans la gestion des ressources numériques. Disponible uniquement lorsqu’une ressource est sélectionnée dans la gestion des ressources numériques.
   * **Afficher la légende dans un pop-up** : si cette option est activée, la légende ne s’affiche pas sous l’image, mais dans un pop-up, dans certains navigateurs, lorsque vous pointez sur l’image.
* **Lien** : lier l’image à une autre ressource.
   * Utilisez la boîte de dialogue de sélection pour créer un lien vers une autre ressource AEM.
   * Si vous ne créez pas de lien vers une ressource AEM, saisissez l’URL absolue. Les URL non absolues seront interprétées comme relatives à AEM.
   * **Ouvrir le lien dans un nouvel onglet** : cette option ouvre le lien dans une nouvelle fenêtre du navigateur.
* **ID** : Cette option permet de contrôler l’identifiant unique du composant dans le HTML.
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur CSS.
* **Largeur** : Cette option définit la largeur en pixels de l’image.
* **Mettre l’image à l’échelle en fonction de la largeur disponible** : Cette option applique `"width":"100%"` à l’attribut de style de l’image.

>[!TIP]
>
>Les options **Recadrage intelligent** et **Paramètre d’image prédéfini** s’excluent mutuellement. Si un auteur doit utiliser un paramètre d’image prédéfini associé à un rendu avec recadrage dynamique, il devra utiliser les **modificateurs d’image** pour ajouter manuellement ce paramètre.

### Onglet Styles {#styles-tab-edit}

![Onglet Styles de la boîte de dialogue de modification du composant Image d’e-mail](/help/assets/image-configure-styles.png)

Le composant Image d’e-mail prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

Utilisez la liste déroulante pour sélectionner les styles à appliquer au composant. Les sélections effectuées dans la boîte de dialogue de modification ou dans la barre d’outils du composant ont le même effet.

Pour accéder à l’onglet, les styles doivent être configurés pour ce composant dans la [boîte de dialogue de conception](#design-dialog).

## Boîte de dialogue de conception {#design-dialog}

### Onglet Principal {#main-tab}

![Onglet principal de la boîte de dialogue de conception du composant Image](/help/email/assets/email-image-design-main.png)

* **Activer les fonctionnalités DM** : lorsque cette option est cochée, les [fonctionnalités Dynamic Media](#dynamic-media) sont disponibles.
   * Dynamic Media doit être activé dans l’environnement pour que cette option apparaisse.
* **Activer les images optimisées pour le web** : lorsque cette case est cochée, [le service de diffusion d’images optimisées pour le web](/help/developing/web-optimized-image-delivery.md) ; diffusera les images au format WebP, réduisant ainsi la taille moyenne des images de 25 %.
   * Cette option est disponible uniquement dans AEMaaCS.
   * Lorsque cette option est décochée ou que le service de diffusion d’images optimisées pour le web n’est pas disponible, le [Servlet Image adaptative](/help/developing/adaptive-image-servlet.md) est utilisé.
* **L’image est décorative** : définissez si l’option d’image décorative est activée automatiquement lors de l’ajout du composant d’image à une page.
* **Obtenir un texte alternatif à partir de DAM** : définissez si l’option permettant de récupérer le texte de remplacement de DAM est automatiquement activée lors de l’ajout du composant d’image à une page.
* **Obtenir la légende à partir de DAM** : définissez si l’option permettant de récupérer la légende à partir de DAM est automatiquement activée lors de l’ajout du composant d’image à une page.
* **Afficher la légende dans un pop-up** : définissez si l’option permettant d’afficher la légende d’image est automatiquement activée lors de l’ajout du composant d’image à une page.
* **Redimensionner la largeur** : cette valeur est utilisée pour redimensionner la largeur des images de base qui sont des ressources DAM.
   * Les proportions des images sont conservées.
   * Si la valeur est supérieure à la largeur de l’image, cette valeur nʼa aucun effet.
   * Cette valeur n’a aucun effet sur les images au format SVG.

Vous pouvez définir une liste de largeurs en pixels pour l’image, le composant chargera alors automatiquement la largeur la plus appropriée en fonction de la taille du navigateur. Il s’agit d’une partie importante des [fonctions réactives](#responsive-features) du composant Image d’e-mail.

* **Largeurs** : définit une liste de largeurs en pixels pour l’image ; le composant charge automatiquement la largeur la plus appropriée en fonction de la taille du navigateur.
   * Appuyez ou cliquez sur le bouton **Ajouter** pour ajouter une autre taille.
      * Utilisez les poignées de capture pour réorganiser l’ordre des tailles.
      * Utilisez l’icône **Supprimer** pour supprimer une largeur.
   * Par défaut, le chargement des images est différé jusqu’à ce qu’elles deviennent visibles.
      * Sélectionnez l’option **Désactiver le chargement différé** pour charger les images au chargement de la page.
* **Qualité JPEG** : facteur de qualité (exprimé par un pourcentage entre 0 et 100) pour les images JPEG transformées (mises à l’échelle ou recadrées, par exemple).
* **Largeur par défaut** : La largeur par défaut des images, exprimée en pixels, qui sera utilisée dans la boîte de dialogue de conception

>[!TIP]
>
>Reportez-vous au document [Servlet Image adaptative](/help/developing/adaptive-image-servlet.md) pour obtenir des conseils sur l’optimisation de la sélection du rendu en définissant soigneusement vos largeurs.

### Onglet Styles {#styles-tab}

Le composant Image d’e-mail prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.
