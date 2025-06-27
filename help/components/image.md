---
title: Composant d’image
description: Le composant Image des composants principaux est un composant d’image adaptatif.
role: Architect, Developer, Admin, User
exl-id: c5e57f4b-139f-40e7-8d79-be9a74360b63
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Composant d’image  {#image-component}

Le composant Image des composants principaux est un composant d’image adaptatif.

{{traditional-aem}}

## Utilisation {#usage}

Le composant d’image comprend une sélection d’images adaptatives et un comportement réactif avec chargement différé pour la personne visitant la page, ainsi qu’un placement facile des images pour la personne créant le contenu.

L’auteur ou l’autrice du contenu peut utiliser la [boîte de dialogue de modification](#edit-dialog) pour modifier le fichier image, par exemple en effectuant un recadrage ou en faisant pivoter l’image.

Les largeurs d’image et les paramètres supplémentaires peuvent être définis par l’auteur du modèle dans la [boîte de dialogue de conception](#design-dialog). L’éditeur de contenu peut charger ou sélectionner des ressources dans la [boîte de dialogue de configuration.](#configure-dialog)

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Image est v3, qui a été introduite avec la version 2.18.0 des composants principaux en février 2022. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v3 | - | Compatible | Compatible | Compatible |
| [v2](v2/image.md) | Compatible | Compatible | - | Compatible |
| [v1](v1/image-v1.md) | Compatible | Compatible | - | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Fonctions réactives {#responsive-features}

Le composant d’image s’accompagne de fonctions réactives efficaces prêtes à l’emploi. Au niveau du modèle de page, la [boîte de dialogue de conception](#design-dialog) permet de définir les largeurs par défaut du fichier image. Le composant d’image charge automatiquement la largeur correcte à afficher en fonction de la taille de la fenêtre du navigateur. Lorsque la fenêtre est redimensionnée, le composant d’image charge dynamiquement la taille d’image correcte, instantanément. Les développeurs de composants n’ont pas à définir des requêtes multimédias personnalisées, puisque le composant d’image est déjà optimisé pour charger le contenu.

En outre, le composant d’image prend en charge le chargement différé afin de différer le chargement du fichier image réel jusqu’à ce qu’il soit visible dans le navigateur, ce qui augmente la réactivité des pages.

>[!TIP]
>
>Par défaut, le composant d’image est optimisé par le servlet d’image adaptative. Veuillez consulter le document [Servlet Image adaptative](/help/developing/adaptive-image-servlet.md) pour plus d’informations sur son fonctionnement.

### Différences avec la version 2 {#v2-differences}

Contrairement à la version 2 du composant Image, la version 3 utilise la réactivité native du navigateur. Cela signifie qu’elle fournit au navigateur un ensemble de sources pour une image sur différentes largeurs et que le navigateur sélectionne la meilleure image.

La plupart du temps, les navigateurs préfèrent réduire localement une largeur plus grande pour l’adapter à une fenêtre d’affichage plus petite au lieu de récupérer l’image de plus petite largeur à partir du serveur. Cela est normal et c’est la raison pour laquelle le composant Image ne doit pas être utilisé pour la direction graphique (différentes images/recadrages pour différentes fenêtres).

Pour plus d’informations, [consultez la documentation GitHub du composant.](https://github.com/adobe/aem-core-wcm-components/tree/main/content/src/content/jcr_root/apps/core/wcm/components/image/v3/image#javascript-data-attribute-bindings).

## Prise en charge de Dynamic Media {#dynamic-media}

Le composant d’image (à partir de la [version 2.13.0](/help/versions.md)) prend en charge les ressources [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media.html?lang=fr). [Lorsqu’elles sont activées](#design-dialog), ces fonctionnalités offrent la possibilité d’ajouter des fichiers d’image Dynamic Media par un simple glisser-déposer ou par le biais du navigateur de ressources, comme vous le feriez pour toute autre image. En outre, les modificateurs d’image, les paramètres d’image prédéfinis et les recadrages intelligents sont également pris en charge.

Vos expériences web créées avec les composants principaux bénéficient des fonctionnalités d’image Dynamic Media sur plusieurs plateformes, hautement performantes, robustes, enrichies et optimisées par Sensei.

## Prise en charge des ressources distantes {#remote-assets}

Le composant Image (à partir de la [version 2.23.2](/help/versions.md)) prend en charge les ressources distantes. [Une fois la configuration effectuée,](/help/developing/remote-assets.md) vous pouvez sélectionner des ressources à partir d’un service distant pour votre composant Image.

## Prise en charge SVG {#svg-support}

Les composants SVG (Scalable Vector Graphics) sont pris en charge par le composant d’image.

* Les opérations de glisser-déposer d’une ressource SVG à partir de la gestion des ressources numériques et le chargement d’un fichier SVG depuis un système de fichiers local sont pris en charge.
* Le fichier SVG d’origine est diffusé en continu (les transformations sont ignorées).
* Pour une image SVG, les « images intelligentes » et les « tailles intelligentes » sont définies sur un tableau vide dans le modèle d’image.

### Sécurité {#security}

Pour des raisons de sécurité, l’éditeur d’image ne fait jamais appel au fichier SVG d’origine. Il est appelé par `<img src="path-to-component">`. Cela empêche le navigateur d’exécuter les scripts incorporés dans le fichier SVG.

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant d’image et voir des exemples de ses options de configuration, ainsi que la sortie HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_image_fr).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant d’image [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_image_v3_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

Le composant d’image prend en charge les [microdonnées schéma.org](https://schema.org).

## Boîte de dialogue de modification {#edit-dialog}

La boîte de dialogue de modification permet à l’auteur ou l’autrice du contenu de recadrer et de faire un zoom sur l’image.

Selon que [Dynamic Media](#dynamic-media) ou la [Prise en charge des ressources distantes](#remote-assets) sont activés, les options disponibles pour la retouche des images diffèrent.

### Modification des ressources standards {#standard-assets}

Si vous modifiez des ressources AEM standards, vous pouvez cliquer sur l’icône **Modifier** dans le menu contextuel du composant Image.

![Boîte de dialogue de modification du composant Image](/help/assets/image-edit.png)

* Commencer recadrage

  ![Icône Commencer recadrage](/help/assets/image-start-crop.png)

  Cette option ouvre une liste déroulante pour les proportions de recadrage prédéfinies.

   * Choisissez l’option **Supprimer le recadrage** pour afficher la ressource d’origine.

  Une fois qu’une option de recadrage est sélectionnée, utilisez les poignées bleues pour dimensionner le recadrage sur l’image.

  ![Options de recadrage](/help/assets/image-crop-options.png)

* Rotation à droite

  ![Icône Rotation à droite](/help/assets/image-rotate-right.png)

  Utilisez cette option pour faire pivoter l’image de 90° vers la droite (dans le sens des aiguilles d&#39;une montre).

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
>Les opérations de modification d’image ne sont pas prises en charge pour les images GIF. Aucune modification de ce type apportée en mode d’édition aux fichiers GIF n’est conservée.

### Modification des ressources Dynamic Media {#dynamic-media-assets}

Si les [fonctionnalités de Dynamic Media sont activées,](#dynamic-media) l’édition de l’image doit être effectuée dans la console Ressources.

## Boîte de dialogue de configuration {#configure-dialog}

Le composant Image comprend une boîte de dialogue de configuration, qui fournit la définition, la description ainsi que les propriétés de base de lʼimage.

### Onglet Contenu {#asset-tab}

![Onglet Contenu de la boîte de dialogue de configuration du composant Image](/help/assets/image-configure-asset.png)

* **Hériter l’image en vedette de la page** : si vous cochez cette option, lʼ[image en vedette de la page liée](page.md) ou l’image de la page active si l’image n’est pas liée est utilisée.

* **Ressource image** : cette valeur est automatiquement renseignée si **Récupérer l’image en vedette de la page** est sélectionnée. Désélectionnez cette option pour configurer manuellement l’image en définissant les options suivantes.

   * Déposez une ressource depuis l’[explorateur de ressources](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/environment-tools.html?lang=fr) ou appuyez sur l’option **Parcourir** pour effectuer un chargement à partir d’un système de fichiers local.
   * Appuyez ou cliquez sur **Effacer** pour désélectionner l’image actuellement sélectionnée.
   * Appuyez ou cliquez sur **Sélectionner** pour ouvrir l’[explorateur de ressources](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/environment-tools.html?lang=fr) et sélectionner une image.
      * Si la [Prise en charge des ressources distantes](#remote-assets) est activée, vous disposez de plusieurs options pour sélectionner une ressource :
         * **Locale** permet de sélectionner dans la bibliothèque de ressources AEM locale.
         * **Distante** permet de sélectionner à partir d’une bibliothèque Dynamic Media en dehors de votre instance AEM.
   * Appuyez ou cliquez sur **Modifier** pour [gérer les rendus de la ressource](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets.html?lang=fr) dans l’éditeur de ressources.

* **Texte secondaire pour l’accessibilité** : ce champ vous permet de fournir une description de l’image pour les utilisateurs souffrant de déficience visuelle.

   * **Hériter le texte secondaire de la page** : cette option utilise la description secondaire de la valeur de la ressource liée des métadonnées `dc:description` dans la gestion des ressources numériques (DAM) ou de la page active si aucune ressource n’est liée.

* **Ne pas fournir de texte secondaire** : marque lʼimage afin quʼelle soit ignorée par les technologies dʼassistance comme les lecteurs dʼécran, dans les cas où lʼimage existe à des fins dʼillustration et ne comporte pas dʼinformations supplémentaires pour la page.

### Onglet Métadonnées {#metadata-tab}

![Onglet Métadonnées de la boîte de dialogue de configuration du composant Image](/help/assets/image-configure-metadata.png)

* **Type de paramètre prédéfini** : définit les types de paramètres d’image prédéfinis disponibles, soit **Paramètre d’image prédéfini** ou **Recadrage intelligent** et n’est disponible que lorsque les [fonctionnalités de Dynamic Media](#dynamic-meida) sont activées.
   * **Paramètre d’image prédéfini** : lorsque **Type de paramètre prédéfini** dans **Paramètre d’image prédéfini** est sélectionné, la liste déroulante **Paramètre d’image prédéfini** est disponible, ce qui permet de sélectionner les paramètres prédéfinis Dynamic Media disponibles. Cette option n’est disponible que si des paramètres prédéfinis sont définis pour la ressource sélectionnée.
   * **Recadrage intelligent** : lorsque **Type de paramètre prédéfini** dans **Recadrage intelligent** est sélectionné, la liste déroulante **Rendu** est disponible, ce qui permet de sélectionner les rendus disponibles de la ressource sélectionnée. Cette option n’est disponible que si des rendus sont définis pour la ressource sélectionnée.
   * **Modificateurs d’images** : il est possible de définir ici d’autres commandes de traitement d’images Dynamic Media, séparées par des caractères `&`, quel que soit le **type de paramètre prédéfini** sélectionné.
* **Légende** : des informations supplémentaires sur l’image sont affichées par défaut sous l’image.
   * **Obtenir la légende à partir de la gestion des ressources numériques** : lorsque cette option est cochée, le texte de légende de l’image est renseigné avec la valeur des métadonnées `dc:title` dans la gestion des ressources numériques.
   * **Afficher la légende dans un pop-up** : si cette option est activée, la légende ne s’affiche pas sous l’image, mais dans un pop-up (pour certains navigateurs), lorsque vous pointez sur l’image.
* **Lien** : lier l’image à une autre ressource.
   * Utilisez la boîte de dialogue de sélection pour créer un lien vers une autre ressource AEM.
   * Si vous ne créez pas de lien vers une ressource AEM, saisissez l’URL absolue. Les URL non absolues sont interprétées comme relatives à AEM.
   * **Ouvrir le lien dans un nouvel onglet** : cette option ouvre le lien dans une nouvelle fenêtre du navigateur.
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

>[!TIP]
>
>Les options **Recadrage intelligent** et **Paramètre d’image prédéfini** s’excluent mutuellement. Si un auteur ou une autrice doit utiliser un paramètre d’image prédéfini associé à un rendu avec recadrage dynamique, il ou elle doit utiliser les **modificateurs d’image** pour ajouter manuellement ce paramètre.

### Onglet Styles {#styles-tab-edit}

![Onglet Styles de la boîte de dialogue de modification du composant Image](/help/assets/image-configure-styles.png)

Le composant d’image prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

Utilisez la liste déroulante pour sélectionner les styles à appliquer au composant. Les sélections effectuées dans la boîte de dialogue de modification ou dans la barre d’outils du composant ont le même effet.

Pour accéder au menu déroulant, les styles doivent être configurés pour ce composant dans la [boîte de dialogue de conception](#design-dialog).

## Boîte de dialogue de conception {#design-dialog}

### Onglet Principal {#main-tab}

![Onglet principal de la boîte de dialogue de conception du composant Image](/help/assets/image-design-main.png)

* **Activer les fonctionnalités DM** : lorsque cette option est cochée, les [fonctionnalités Dynamic Media](#dynamic-media) sont disponibles.
   * Dynamic Media doit être activé dans l’environnement pour que cette option apparaisse.
* **Activer les images optimisées pour le web** : lorsque cette case est cochée, [le service de diffusion d’images optimisées pour le web](/help/developing/web-optimized-image-delivery.md) diffuse les images au format WebP, réduisant ainsi la taille moyenne des images de 25 %.
   * Cette option est disponible uniquement dans AEMaaCS.
   * Lorsque cette option est décochée ou que le service de diffusion d’images optimisées pour le web n’est pas disponible, le [servlet Image adaptative](/help/developing/adaptive-image-servlet.md) est utilisé.
* **Désactiver le chargement différé** : lorsque cette option est cochée, le composant précharge toutes les images sans chargement différé.
* **L’image est décorative** : définissez si l’option d’image décorative est activée automatiquement lors de l’ajout du composant d’image à une page.
* **Obtenir un texte alternatif à partir de DAM** : définissez si l’option permettant de récupérer le texte de remplacement de DAM est automatiquement activée lors de l’ajout du composant d’image à une page.
* **Obtenir la légende à partir de DAM** : définissez si l’option permettant de récupérer la légende à partir de DAM est automatiquement activée lors de l’ajout du composant d’image à une page.
* **Afficher la légende dans un pop-up** : définissez si l’option permettant d’afficher la légende d’image est automatiquement activée lors de l’ajout du composant d’image à une page.
* **Redimensionner la largeur** : cette valeur est utilisée pour redimensionner la largeur des images de base qui sont des ressources DAM.
   * Le format des images est conservé.
   * Si la valeur est supérieure à la largeur de l’image, elle nʼa aucun effet.
   * Cette valeur n’a aucun effet sur les images au format SVG.

Vous pouvez définir une liste de largeurs en pixels pour l’image. Le composant charge alors automatiquement la largeur la plus appropriée en fonction de la taille du navigateur. Il s’agit d’une partie importante des [fonctions réactives](#responsive-features) du composant d’image.

* **Largeurs** : définit une liste de largeurs en pixels pour l’image ; le composant charge automatiquement la largeur la plus appropriée en fonction de la taille du navigateur.
   * Appuyez ou cliquez sur le bouton **Ajouter** pour ajouter une autre taille.
      * Utilisez les poignées de capture pour réorganiser l’ordre des tailles.
      * Utilisez l’icône **Supprimer** pour supprimer une largeur.
   * Par défaut, le chargement des images est différé jusqu’à ce qu’elles deviennent visibles.
      * Sélectionnez l’option **Désactiver le chargement différé** pour charger les images au chargement de la page.
* **Qualité JPEG** : facteur de qualité (exprimé par un pourcentage entre 0 et 100) pour les images JPEG transformées (mises à l’échelle ou recadrées, par exemple).

>[!TIP]
>
>Reportez-vous au document [Servlet Image adaptative](/help/developing/adaptive-image-servlet.md) pour obtenir des conseils sur l’optimisation de la sélection du rendu en définissant soigneusement vos largeurs.

### Onglet Styles {#styles-tab}

Le composant d’image prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

## Couche de données client Adobe {#data-layer}

Le composant Image prend en charge la [couche de données client Adobe](/help/developing/data-layer/overview.md).
