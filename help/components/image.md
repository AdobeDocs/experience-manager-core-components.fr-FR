---
title: Composant d’image
description: Le composant Image des composants principaux est un composant d’image adaptatif.
role: Architect, Developer, Admin, User
exl-id: c5e57f4b-139f-40e7-8d79-be9a74360b63
source-git-commit: a10c98aecf6d3c0d989f2e3c18affc51850f60bc
workflow-type: tm+mt
source-wordcount: '2061'
ht-degree: 61%

---


# Composant d’image  {#image-component}

Le composant Image des composants principaux est un composant d’image adaptatif.

## Utilisation {#usage}

Le composant d’image comprend une sélection d’images adaptatives et un comportement réactif avec chargement différé pour le visiteur de la page et un placement d’image facile pour l’auteur du contenu.

L’auteur du contenu peut utiliser la variable [Modifier la boîte de dialogue](#edit-dialog) pour modifier la ressource image, par exemple en appliquant un recadrage ou en faisant pivoter l’image.

Les largeurs d’image et les paramètres supplémentaires peuvent être définis par l’auteur du modèle dans la [boîte de dialogue de conception](#design-dialog). L’éditeur de contenu peut charger ou sélectionner des ressources dans la [boîte de dialogue de configuration.](#configure-dialog)

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Image est v3, qui a été introduite avec la version 2.18.0 des composants principaux en février 2022. Elle est décrite dans ce document.

Le tableau suivant décrit toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v3 | - | Compatible | Compatible |
| [v2](v2/image.md) | Compatible | Compatible | Compatible |
| [v1](v1/image-v1.md) | Compatible | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Fonctions réactives {#responsive-features}

Le composant d’image s’accompagne de fonctions réactives efficaces prêtes à l’emploi. Au niveau du modèle de page, la [boîte de dialogue de conception](#design-dialog) permet de définir les largeurs par défaut du fichier image. Le composant d’image charge automatiquement la largeur correcte à afficher en fonction de la taille de la fenêtre du navigateur. Lorsque la fenêtre est redimensionnée, le composant d’image charge dynamiquement la taille d’image correcte, instantanément. Les développeurs de composants n’ont pas à définir des requêtes multimédias personnalisées, puisque le composant d’image est déjà optimisé pour charger le contenu.

En outre, le composant d’image prend en charge le chargement différé afin de différer le chargement du fichier image réel jusqu’à ce qu’il soit visible dans le navigateur, ce qui augmente la réactivité des pages.

>[!TIP]
>
>Par défaut, le composant d’image est optimisé par le servlet d’image adaptative. Voir [Servlet d’image adaptative](/help/developing/adaptive-image-servlet.md) pour plus d’informations sur son fonctionnement.

## Prise en charge de Dynamic Media {#dynamic-media}

Le composant d’image (à partir de la [version 2.13.0](/help/versions.md)) prend en charge les ressources [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media.html). [Lorsqu’elles sont activées](#design-dialog), ces fonctionnalités offrent la possibilité d’ajouter des fichiers d’image Dynamic Media par un simple glisser-déposer ou par le biais du navigateur de ressources, comme vous le feriez pour toute autre image. En outre, les modificateurs d’image, les paramètres d’image prédéfinis et les recadrages intelligents sont également pris en charge.

Vos expériences web créées avec les composants principaux bénéficient des fonctionnalités d’image Dynamic Media sur plusieurs plateformes, hautement performantes, robustes, enrichies et optimisées par Sensei.

## Prise en charge de Dynamic Media de nouvelle génération {#next-gen-dm}

Le composant d’image (à partir de [version 2.23.2](/help/versions.md)) prend en charge les ressources distantes Dynamic Media de génération suivante.

[Une fois la configuration effectuée,](/help/developing/next-gen-dm.md) vous pouvez sélectionner des ressources à partir d’un service Dynamic Media de génération suivante distant pour votre composant d’image.

## Prise en charge SVG {#svg-support}

Les composants SVG (Scalable Vector Graphics) sont pris en charge par le composant d’image.

* Le glisser-déposer d’une ressource de SVG à partir de DAM et le chargement d’un fichier de SVG chargé à partir d’un système de fichiers local sont tous deux pris en charge.
* Le fichier SVG d’origine est diffusé en continu (les transformations sont ignorées).
* Pour une image SVG, les « images intelligentes » et les « tailles intelligentes » sont définies sur un tableau vide dans le modèle d’image.

### Sécurité {#security}

Pour des raisons de sécurité, l’éditeur d’image ne fait jamais appel au fichier SVG d’origine. Il est appelé par `<img src="path-to-component">`. Cela empêche le navigateur d’exécuter les scripts incorporés dans le fichier SVG.

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant d’image et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la page [Bibliothèque de composants](https://adobe.com/go/aem_cmp_library_image_fr).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant d’image [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_image_v3_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

Le composant d’image prend en charge les [microdonnées schéma.org](https://schema.org).

## Boîte de dialogue de modification {#edit-dialog}

La boîte de dialogue de modification permet à l’auteur de contenu de recadrer et de zoomer sur l’image.

Selon si vous disposez de la variable [Dynamic Media](#dynamic-media) activé ou [Dynamic Media de génération suivante](#next-gen-dm) fonctions activées, les options disponibles pour la modification des images diffèrent.

### Modification de ressources standard {#standard-assets}

Si vous modifiez des AEM standard, vous pouvez cliquer sur le bouton **Modifier** dans le menu contextuel du composant image.

![Boîte de dialogue de modification du composant Image](/help/assets/image-edit.png)

* Commencer recadrage

  ![Icône Commencer recadrage](/help/assets/image-start-crop.png)

  Cette option ouvre une liste déroulante pour les proportions de recadrage prédéfinies.

   * Choisissez l’option **Supprimer le recadrage** pour afficher la ressource d’origine.

  Une fois qu’une option de recadrage est sélectionnée, utilisez les poignées bleues pour dimensionner le recadrage sur l’image.

  ![Options de recadrage](/help/assets/image-crop-options.png)

* Rotation à droite

  ![Icône Rotation à droite](/help/assets/image-rotate-right.png)

  Utilisez cette option pour faire pivoter l’image de 90° vers la droite (dans le sens horaire).

* Réinitialiser le zoom

  ![Icône Réinitialiser le zoom](/help/assets/image-reset-zoom.png)

  Si l’image a déjà été agrandie, utilisez cette option pour réinitialiser le niveau de zoom.

* Ouvrir le curseur de zoom

  ![Icône Ouvrir le curseur de zoom](/help/assets/image-zoom.png)

  Utilisez cette option pour afficher un curseur permettant de contrôler le niveau de zoom de l’image.

  ![Commande du curseur de zoom](/help/assets/image-zoom-slider.png)

L’éditeur statique peut également être utilisé pour modifier l’image. En raison d’un espace limité, seules les options de base sont disponibles en ligne. Pour des options de modification complètes, utilisez le mode Plein écran.

![Options de modification statique des images](/help/assets/image-in-place-edit.png)

>[!NOTE]
>
>Les opérations de modification d’image ne sont pas prises en charge pour les images de GIF. Les modifications de ce type effectuées en mode d’édition sur GIF ne sont pas conservées.

### Modification des ressources Dynamic Media {#dynamic-media-assets}

Si vous avez [Fonctionnalités Dynamic Media activées,](#dynamic-media) l’édition de l’image elle-même doit être effectuée dans la console ressources.

### Modification des ressources Dynamic Media de nouvelle génération {#next-gen-dm-assets}

Si vous avez [Dynamic Media de génération suivante configurée,](#next-gen-dm) la valeur **Recadrage intelligent** est disponible dans les menus contextuels du composant.

![Recadrage intelligent](/help/assets/image-smart-crop.png)

Utilisez la boîte de dialogue pour ajuster le recadrage intelligent.

![Boîte de dialogue Recadrage intelligent](/help/assets/image-smart-crop-dialog.png)

>[!TIP]
>
>Pour plus d’informations sur le recadrage intelligent, voir [cette vidéo sur la fonctionnalité.](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/dynamic-media/images/smart-crop-feature-video-use.html?lang=fr)

## Boîte de dialogue de configuration {#configure-dialog}

Le composant Image comprend une boîte de dialogue de configuration, qui fournit la définition, la description ainsi que les propriétés de base de lʼimage.

### Onglet Contenu {#asset-tab}

![Onglet Contenu de la boîte de dialogue de configuration du composant Image](/help/assets/image-configure-asset.png)

* **Hériter l’image en vedette de la page** : si vous cochez cette option, lʼ[image en vedette de la page liée](page.md) ou l’image de la page active si l’image n’est pas liée est utilisée.

* **Ressource image** - Cette valeur est automatiquement renseignée si **Hériter de l’image fournie de la page** est sélectionnée. Désélectionnez cette option pour définir manuellement l’image en définissant les options suivantes.

   * Déposez une ressource du [explorateur de ressources](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/environment-tools.html) ou appuyez sur **parcourir** pour que vous puissiez effectuer un téléchargement à partir d’un système de fichiers local.
   * Appuyez ou cliquez sur **Effacer** pour désélectionner l’image actuellement sélectionnée.
   * Appuyez ou cliquez sur **Pick** pour ouvrir le [explorateur de ressources](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/environment-tools.html) pour sélectionner une image.
      * If [Fonctionnalités Dynamic Media de nouvelle génération](#next-gen-dm) sont activées, vous disposez de plusieurs options pour sélectionner une ressource :
         * **Local** sélectionne dans la bibliothèque de ressources d’AEM locale.
         * **Distant** fait une sélection à partir d’une bibliothèque Dynamic Media en dehors de votre instance AEM.
   * Appuyez ou cliquez sur **Modifier** pour [gérer les rendus de la ressource](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets.html) dans l’éditeur de ressources.

* **Texte secondaire pour l’accessibilité** : ce champ vous permet de fournir une description de l’image pour les utilisateurs souffrant de déficience visuelle.

   * **Hériter le texte secondaire de la page** : cette option utilise la description secondaire de la valeur de la ressource liée des métadonnées `dc:description` dans la gestion des ressources numériques (DAM) ou de la page active si aucune ressource n’est liée.

* **Ne pas fournir de texte de remplacement** - Marque l’image à ignorer par les technologies d’assistance telles que les lecteurs d’écran pour les cas où l’image est purement décorative ou ne transmet aucune information supplémentaire à la page.

### Onglet Métadonnées {#metadata-tab}

![Onglet Métadonnées de la boîte de dialogue de configuration du composant Image](/help/assets/image-configure-metadata.png)

* **Type de paramètre prédéfini** : définit les types de paramètres d’image prédéfinis disponibles, soit **Paramètre d’image prédéfini** ou **Recadrage intelligent** et n’est disponible que lorsque les [fonctionnalités de Dynamic Media](#dynamic-meida) sont activées.
   * **Paramètre d’image prédéfini** : lorsque **Type de paramètre prédéfini** dans **Paramètre d’image prédéfini** est sélectionné, la liste déroulante **Paramètre d’image prédéfini** est disponible, ce qui permet de sélectionner les paramètres prédéfinis Dynamic Media disponibles. Cette option n’est disponible que si des paramètres prédéfinis sont définis pour la ressource sélectionnée.
   * **Recadrage intelligent** - Lorsque **Type de paramètre prédéfini** de **Recadrage intelligent** est sélectionné, la liste déroulante **Rendu** est disponible, ce qui permet de sélectionner les rendus disponibles de la ressource sélectionnée. Cette option n’est disponible que si des rendus sont définis pour la ressource sélectionnée.
   * **Modificateurs d’images** : il est possible de définir ici d’autres commandes de traitement d’images Dynamic Media, séparées par des caractères `&`, quel que soit le **type de paramètre prédéfini** sélectionné.
* **Légende** : des informations supplémentaires sur l’image sont affichées par défaut sous l’image.
   * **Obtenir la légende à partir de DAM** : lorsque cette case est cochée, le texte de la légende de l’image est renseigné avec la valeur de la propriété `dc:title` métadonnées dans la gestion des ressources numériques.
   * **Afficher la légende dans une fenêtre contextuelle** - Lorsque cette option est cochée, la légende n’est pas affichée sous l’image, mais dans une fenêtre contextuelle affichée par certains navigateurs lorsque vous pointez sur l’image.
* **Lien** : lier l’image à une autre ressource.
   * Utilisez la boîte de dialogue de sélection pour créer un lien vers une autre ressource AEM.
   * Si vous ne créez pas de lien vers une ressource AEM, saisissez l’URL absolue. Les URL non résolues sont interprétées comme relatives à l’AEM.
   * **Ouvrir le lien dans un nouvel onglet** : cette option ouvre le lien dans une nouvelle fenêtre du navigateur.
* **ID** - Cette option permet de contrôler l’identifiant unique du composant dans le HTML et dans la variable [Couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

>[!TIP]
>
>Les options **Recadrage intelligent** et **Paramètre d’image prédéfini** s’excluent mutuellement. Si un auteur doit utiliser un paramètre d’image prédéfini avec un rendu avec recadrage intelligent, il doit utiliser la variable **Modificateurs d’image** pour ajouter manuellement des paramètres prédéfinis.

### Onglet Styles {#styles-tab-edit}

![Onglet Styles de la boîte de dialogue de modification du composant Image](/help/assets/image-configure-styles.png)

Le composant d’image prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

Utilisez la liste déroulante pour sélectionner les styles à appliquer au composant. Les sélections effectuées dans la boîte de dialogue de modification ou dans la barre d’outils du composant ont le même effet.

Les styles doivent être configurés pour ce composant dans la variable [boîte de dialogue de conception](#design-dialog) pour que le menu déroulant soit disponible.

## Boîte de dialogue de conception {#design-dialog}

### Onglet Principal {#main-tab}

![Onglet principal de la boîte de dialogue de conception du composant Image](/help/assets/image-design-main.png)

* **Activer les fonctionnalités DM** : lorsque cette option est cochée, les [fonctionnalités Dynamic Media](#dynamic-media) sont disponibles.
   * Dynamic Media doit être activé dans l’environnement pour que cette option apparaisse.
* **Activer les images optimisées pour le web** - Lorsque coché, [le service de diffusion d’images optimisé pour le web ;](/help/developing/web-optimized-image-delivery.md) diffuse des images au format WebP, réduisant la taille moyenne des images de 25 %.
   * Cette option est disponible uniquement dans AEMaaCS.
   * Si cette option n’est pas cochée ou si le service de diffusion d’images optimisé pour le web n’est pas disponible, la variable [Servlet d’image adaptative](/help/developing/adaptive-image-servlet.md) est utilisée.
* **Désactiver le chargement différé** - Lorsque cette case est cochée, le composant précharge toutes les images sans chargement différé.
* **L’image est décorative** : définissez si l’option d’image décorative est activée automatiquement lors de l’ajout du composant d’image à une page.
* **Obtenir un texte alternatif à partir de DAM** : définissez si l’option permettant de récupérer le texte de remplacement de DAM est automatiquement activée lors de l’ajout du composant d’image à une page.
* **Obtenir la légende à partir de DAM** : définissez si l’option permettant de récupérer la légende à partir de DAM est automatiquement activée lors de l’ajout du composant d’image à une page.
* **Afficher la légende dans un pop-up** : définissez si l’option permettant d’afficher la légende d’image est automatiquement activée lors de l’ajout du composant d’image à une page.
* **Redimensionner la largeur** : cette valeur est utilisée pour redimensionner la largeur des images de base qui sont des ressources DAM.
   * Les proportions des images sont conservées.
   * Si la valeur est supérieure à la largeur réelle de l’image, cette valeur n’a aucun effet.
   * Cette valeur n’a aucun effet sur les images au format SVG.

Vous pouvez définir une liste de largeurs en pixels pour l’image ; le composant charge automatiquement la largeur la plus appropriée en fonction de la taille du navigateur. Il s’agit d’une partie importante des [fonctions réactives](#responsive-features) du composant d’image.

* **Largeurs** : définit une liste de largeurs en pixels pour l’image ; le composant charge automatiquement la largeur la plus appropriée en fonction de la taille du navigateur.
   * Appuyez ou cliquez sur le bouton **Ajouter** pour ajouter une autre taille.
      * Utilisez les poignées de capture pour réorganiser l’ordre des tailles.
      * Utilisez l’icône **Supprimer** pour supprimer une largeur.
   * Par défaut, le chargement des images est différé jusqu’à ce qu’elles deviennent visibles.
      * Sélectionner l’option **Désactiver le chargement différé** afin que vous puissiez charger les images au chargement de la page.
* **Qualité du JPEG** - Facteur de qualité (en pourcentage entre 0 et 100) pour les images de JPEG transformées (mises à l’échelle ou recadrées, par exemple).

>[!TIP]
>
>Reportez-vous au document [Servlet Image adaptative](/help/developing/adaptive-image-servlet.md) pour obtenir des conseils sur l’optimisation de la sélection du rendu en définissant soigneusement vos largeurs.

### Onglet Styles {#styles-tab}

Le composant d’image prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

## Couche de données client Adobe {#data-layer}

Le composant Image prend en charge la [couche de données client Adobe](/help/developing/data-layer/overview.md).
