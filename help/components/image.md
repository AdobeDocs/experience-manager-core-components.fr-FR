---
title: Composant d’image
description: Le composant d’image des composants principaux est un composant d’image adaptatif qui permet d’effectuer des modifications statiques.
translation-type: ht
source-git-commit: d3ebcea5fa1523c1a986841cd3d1a64e16e85f6d
workflow-type: ht
source-wordcount: '2170'
ht-degree: 100%

---


# Composant d’image {#image-component}

Le composant d’image des composants principaux est un composant d’image adaptatif qui permet d’effectuer des modifications statiques.

## Utilisation {#usage}

Le composant d’image comprend une sélection des images adaptatives et un comportement réactif avec chargement différé pour le visiteur de la page, ainsi qu’un positionnement et un recadrage des images faciles pour l’auteur du contenu.

Les largeurs d’image ainsi que le recadrage et les paramètres supplémentaires peuvent être définis par l’auteur du modèle dans la [boîte de dialogue de conception](#design-dialog). L’éditeur de contenu peut télécharger ou sélectionner des ressources dans la [boîte de dialogue de configuration](#configure-dialog) et recadrer l’image dans la [boîte de dialogue de modification](#edit-dialog). Pour plus de commodité, une simple modification statique de l’image est également disponible.

## Fonctions réactives {#responsive-features}

Le composant d’image s’accompagne de fonctions réactives efficaces prêtes à l’emploi. Au niveau du modèle de page, la [boîte de dialogue de conception](#design-dialog) permet de définir les largeurs par défaut du fichier image. Le composant d’image charge alors automatiquement la largeur correcte à afficher en fonction de la taille de la fenêtre du navigateur. Lorsque la fenêtre est redimensionnée, le composant d’image charge dynamiquement la taille d’image correcte, instantanément. Les développeurs de composants n’ont pas à définir des requêtes multimédias personnalisées, puisque le composant d’image est déjà optimisé pour charger le contenu.

En outre, le composant d’image prend en charge le chargement différé afin de différer le chargement du fichier image réel jusqu’à ce qu’il soit visible dans le navigateur, ce qui augmente la réactivité des pages.

## Prise en charge de Dynamic Media {#dynamic-media}

Le composant d’image (à partir de la [version 2.13.0](/help/versions.md)) prend en charge les ressources [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/dynamic-media.html?lang=fr#dynamicmedia). [Lorsqu’elles sont activées](#design-dialog), ces fonctionnalités offrent la possibilité d’ajouter des fichiers d’image Dynamic Media par un simple glisser-déposer ou par le biais du navigateur de ressources, comme vous le feriez pour toute autre image. En outre, les modificateurs d’image, les paramètres d’image prédéfinis et les recadrages intelligents sont également pris en charge.

Vos expériences web créées avec les composants principaux bénéficient des fonctionnalités d’image Dynamic Media sur plusieurs plateformes, hautement performantes, robustes, enrichies et optimisées par Sensei.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant d’image est v2, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatible | Compatible | Compatible |
| [v1](v1/image-v1.md) | Compatible | Compatible | - |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Prise en charge SVG {#svg-support}

Les composants SVG (Scalable Vector Graphics) sont pris en charge par le composant d’image.

* Les opérations de glisser-déplacer d’une ressource SVG à partir de DAM et le téléchargement d’un fichier SVG depuis un système de fichiers local sont pris en charge.
* La servlet d’image adaptative diffuse le fichier SVG d’origine en flux continu (les transformations sont ignorées).
* Pour une image SVG, les « images intelligentes » et les « tailles intelligentes » sont définies sur un tableau vide dans le modèle d’image.

### Sécurité {#security}

Pour des raisons de sécurité, l’éditeur d’image ne fait jamais appel au fichier SVG d’origine. Il est appelé par `<img src=“path-to-component”>`. Cela empêche le navigateur d’exécuter les scripts incorporés dans le fichier SVG.

>[!CAUTION]
>
>La prise en charge de SVG nécessite la version 2.1.0, ou ultérieure, des composants principaux et le [Service Pack 2](https://docs.adobe.com/content/help/fr-FR/experience-manager-64/release-notes/sp-release-notes.html) pour AEM 6.4, ou version ultérieure, pour être compatible avec les [fonctionnalités de l’éditeur d’image](https://docs.adobe.com/content/help/fr-FR/experience-manager-cloud-service/implementing/components-templates/image-editor.html) d’AEM.

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant d’image et voir des exemples de ses options de configuration, ainsi que la sortie HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_image_fr).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant d’image [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_image_v2).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

Le composant d’image prend en charge les [microdonnées schéma.org](https://schema.org).

## Boîte de dialogue de configuration {#configure-dialog}

Outre la [boîte de dialogue de modification](#edit-dialog) et la [boîte de dialogue de conception](#design-dialog) standard, le composant d’image propose une boîte de dialogue de configuration dans laquelle l’image elle-même est définie avec sa description et ses propriétés de base.

### Onglet Ressources {#asset-tab}

![Onglet Ressource de la boîte de dialogue de configuration du composant Image](/help/assets/image-configure-asset.png)

* **Ressource image**
   * Déposez un fichier depuis l’[explorateur de ressources](https://docs.adobe.com/content/help/fr-FR/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) ou appuyez sur l’option **parcourir** pour effectuer un téléchargement à partir d’un système de fichiers local.
   * Appuyez ou cliquez sur **Effacer** pour désélectionner l’image actuellement sélectionnée.
   * Appuyez ou cliquez sur **Modifier** pour [gérer les rendus de la ressource](https://docs.adobe.com/content/help/fr-FR/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) dans l’éditeur de ressources.

### Onglet Métadonnées {#metadata-tab}

![Onglet Métadonnées de la boîte de dialogue de configuration du composant Image](/help/assets/image-configure-metadata.png)

* **Type de paramètre prédéfini** : définit les types de paramètres d’image prédéfinis disponibles, soit **Paramètre d’image prédéfini** ou **Recadrage intelligent** et n’est disponible que lorsque les [fonctionnalités de Dynamic Media](#dynamic-meida) sont activées.
   * **Paramètre d’image prédéfini** : lorsque **Type de paramètre prédéfini** dans **Paramètre d’image prédéfini** est sélectionné, la liste déroulante **Paramètre d’image prédéfini** est disponible, ce qui permet de sélectionner les paramètres prédéfinis Dynamic Media disponibles. Cette option n’est disponible que si des paramètres prédéfinis sont définis pour la ressource sélectionnée.
   * **Recadrage intelligent** : lorsque **Type de paramètre prédéfini** dans **Recadrage intelligent** est sélectionné, la liste déroulante **Rendu** est disponible, ce qui permet de sélectionner les rendus disponibles de la ressource sélectionnée. Cette option n’est disponible que si des rendus sont définis pour la ressource sélectionnée.
   * **Modificateurs d’images** : il est possible de définir ici d’autres commandes de traitement d’images Dynamic Media, séparées par des caractères `&`, quel que soit le **type de paramètre prédéfini** sélectionné.
* **L’image est décorative** : vérifiez si l’image doit être ignorée par les dispositifs d’assistance et ne requiert donc pas de texte de remplacement. Cela s’applique uniquement aux images décoratives.
* **Texte de remplacement** : alternative textuelle de la signification ou de la fonction de l’image, pour les malvoyants.
   * **Obtenir un texte alternatif à partir de DAM** : lorsque cette option est cochée, le texte de remplacement de l’image est renseigné avec la valeur des métadonnées `dc:description` dans DAM.
* **Légende** : des informations supplémentaires sur l’image sont affichées par défaut sous l’image.
   * **Obtenir la légende à partir de DAM** : lorsque cette option est cochée, le texte de légende de l’image est renseigné avec la valeur des métadonnées `dc:title` dans DAM.
   * **Afficher la légende dans une fenêtre contextuelle** : si cette option est activée, la légende ne s’affiche pas sous l’image, mais dans une fenêtre contextuelle, dans certains navigateurs, lorsque vous pointez sur l’image.
* **Lien** : lier l’image à une autre ressource.
   * Utilisez la boîte de dialogue de sélection pour créer un lien vers une autre ressource AEM.
   * Si vous ne créez pas de lien vers une ressource AEM, saisissez l’URL absolue. Les URL non absolues seront interprétées comme relatives à AEM.
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

>[!TIP]
>
>Les options **Recadrage intelligent** et **Paramètre d’image prédéfini** s’excluent mutuellement. Si un auteur doit utiliser un paramètre d’image prédéfini associé à un rendu avec recadrage dynamique, il devra utiliser les **modificateurs d’image** pour ajouter manuellement ce paramètre.

## Boîte de dialogue de modification {#edit-dialog}

La boîte de dialogue de modification permet à l’auteur du contenu de recadrer, de modifier la carte de lancement et de zoomer sur l’image.

>[!NOTE]
>
>Les fonctions de recadrage, de rotation et de zoom ne s’appliquent pas aux ressources Dynamic Media. Si les [fonctions de Dynamic Media](#dynamic-media) sont activées, les modifications des ressources Dynamic Media sont effectuées à l’aide de la [boîte de dialogue Configuration](#configure-dialog).

![Boîte de dialogue de modification du composant Image](/help/assets/image-edit.png)

* Commencer recadrage

   ![Icône Commencer recadrage](/help/assets/image-start-crop.png)

   Cette option ouvre une liste déroulante pour les proportions de recadrage prédéfinies.

   * Choisissez l’option **Main libre** pour définir votre propre recadrage.
   * Choisissez l’option **Supprimer le recadrage** pour afficher la ressource d’origine.

   Une fois qu’une option de recadrage est sélectionnée, utilisez les poignées bleues pour dimensionner le recadrage sur l’image.

   ![Options de recadrage](/help/assets/image-crop-options.png)

* Rotation à droite

   ![Icône Rotation à droite](/help/assets/image-rotate-right.png)

   Utilisez cette option pour faire pivoter l’image de 90° vers la droite (dans le sens horaire).

* Symétrie horizontale

   ![Icône Symétrie horizontale](/help/assets/image-flip-horizontal.png)

   Utilisez cette option pour retourner l’image horizontalement ou faire pivoter l’image de 180° sur l’axe Y.

* Symétrie verticale

   ![Icône Symétrie verticale](/help/assets/image-flip-vertical.png)

   Utilisez cette option pour retourner l’image verticalement ou faire pivoter l’image de 180° sur l’axe X.

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
>Les opérations de modification d’image (recadrage, pivotement, rotation) ne sont pas prises en charge pour les images GIF. Aucune modification de ce type apportée en mode d’édition aux fichiers GIF n’est conservée.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir le recadrage, le téléchargement et la rotation dont dispose l’auteur du contenu lors de l’utilisation de ce composant.

### Onglet principal {#main-tab}

Dans l’onglet **Principal**, vous pouvez définir une liste de largeurs en pixels pour l’image ; le composant chargera automatiquement la largeur la plus appropriée en fonction de la taille du navigateur. Il s’agit d’une partie importante des [fonctions réactives](#responsive-features) du composant d’image.

En outre, vous pouvez définir quelles options de composant générales sont automatiquement activées ou désactivées lorsque l’auteur ajoute le composant à une page.

![Onglet principal de la boîte de dialogue de conception du composant Image](/help/assets/image-design-main.png)

* **Activer les fonctionnalités DM** : lorsque cette option est cochée, les fonctionnalités [d’activation de Dynamic Media](#dynamic-media) sont disponibles.
* **Activer le chargement différé** : définissez si l’option de chargement différé est activée automatiquement lors de l’ajout du composant d’image à une page.
* **L’image est décorative** : définissez si l’option d’image décorative est activée automatiquement lors de l’ajout du composant d’image à une page.
* **Obtenir un texte alternatif à partir de DAM** : définissez si l’option permettant de récupérer le texte de remplacement de DAM est automatiquement activée lors de l’ajout du composant d’image à une page.
* **Obtenir la légende à partir de DAM** : définissez si l’option permettant de récupérer la légende à partir de DAM est automatiquement activée lors de l’ajout du composant d’image à une page.
* **Afficher la légende dans une fenêtre contextuelle** : définissez si l’option permettant d’afficher la légende d’image est automatiquement activée lors de l’ajout du composant d’image à une page.
* **Désactiver le suivi d’UUID** : cochez cette option pour désactiver le suivi de l’UUID de la ressource d’image.
* **Largeurs** : définit une liste de largeurs en pixels pour l’image ; le composant charge automatiquement la largeur la plus appropriée en fonction de la taille du navigateur.
   * Appuyez ou cliquez sur le bouton **Ajouter** pour ajouter une autre taille.
      * Utilisez les poignées de capture pour réorganiser l’ordre des tailles.
      * Utilisez l’icône **Supprimer** pour supprimer une largeur.
   * Par défaut, le chargement des images est différé jusqu’à ce qu’elles deviennent visibles.
      * Sélectionnez l’option **Désactiver le chargement différé** pour charger les images au chargement de la page.
* **Qualité JPEG** : facteur de qualité (exprimé par un pourcentage entre 0 et 100) pour les images JPEG transformées (mises à l’échelle ou recadrées, par exemple).

### Onglet Fonctions {#features-tab}

Sur l’onglet **Fonctions**, vous pouvez définir les options disponibles pour les auteurs de contenu lors de l’utilisation du composant, y compris les options de téléchargement, d’orientation et de recadrage.

* Source

   ![Onglet Fonctions de la boîte de dialogue de conception du composant Image](/help/assets/image-design-features-source.png)

   Sélectionnez l’option **Autoriser le transfert des ressources depuis le système de fichiers** pour permettre aux auteurs de contenu de télécharger des images à partir de leur ordinateur local. Pour forcer les auteurs de contenu à sélectionner uniquement des ressources à partir d’AEM, désactivez cette option.

* Orientation

   ![Onglet Fonctions de la boîte de dialogue de conception du composant Image](/help/assets/image-design-features-orientation.png)

* **Rotation**
Utilisez cette option pour permettre à l’auteur de contenu d’appliquer l’option 
**Rotation à droite**.
* **Symétrie**
Utilisez cette option pour permettre à l’auteur de contenu d’appliquer 
les options **Symétrie horizontale** et **Rotation verticale**.

   >[!CAUTION]
   >
   >L’option **Symétrie** est désactivée par défaut. L’activation de cette option affichera les boutons **Symétrie verticale** et **Symétrie horizontale** dans la boîte de dialogue de modification du composant d’image. Toutefois, cette fonction n’est actuellement pas prise en charge par AEM et les modifications effectuées à l’aide de ces options ne seront pas conservées.

* Recadrage

   ![Onglet Fonctions de la boîte de dialogue de conception du composant Image](/help/assets/image-design-features-cropping.png)

   Sélectionnez l’option **Autoriser le recadrage** pour permettre à l’auteur du contenu de recadrer l’image dans le composant au sein de la boîte de dialogue de modification.
   * Cliquez sur **Ajouter** pour ajouter des proportions de recadrage prédéfinies.
   * Saisissez un nom descriptif. Celui-ci s’affichera dans la liste déroulante **Commencer recadrage**.
   * Entrez les proportions.
   * Utilisez les poignées de glissement pour réorganiser l’ordre des proportions.
   * Utilisez l’icône de corbeille pour supprimer des proportions.

   >[!CAUTION]
   >
   >Remarque : Dans AEM, les proportions de recadrage sont définies en tant que **hauteur/largeur**. Cela diffère de la définition conventionnelle de la largeur/hauteur. Cela a été créée pour des raisons de compatibilité héritée. Les auteurs de contenu ne verront aucune différence tant que vous indiquez le nom clair des proportions, car le nom s’affiche dans l’interface utilisateur et non les proportions.

### Onglet Styles {#styles-tab-1}

Le composant d’image prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

## Servlet d’image adaptative {#adaptive-image-servlet}

Le composant d’image utilise la servlet d’image adaptative des composants principaux. [La servlet d’image adaptative](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) est en charge du traitement des images et de leur diffusion en flux continu. Les développeurs peuvent l’utiliser dans le cadre de leur [personnalisation des composants principaux](/help/developing/customizing.md).

>[!NOTE]
>
>Les requêtes conditionnelles effectuées par le biais de `Last-Modified` en-tête sont prises en charge par la servlet d’image adaptative, mais la mise en cache de l’en-tête `Last-Modified` [doit être activée dans Dispatcher](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=fr#caching-http-response-headers).
>
>L’exemple de configuration de Dispatcher d’[AEM Project Archetype](/help/developing/archetype/overview.md) contient déjà cette configuration.

## Couche de données client Adobe {#data-layer}

Le composant Image prend en charge la [couche de données client Adobe](/help/developing/data-layer/overview.md).
