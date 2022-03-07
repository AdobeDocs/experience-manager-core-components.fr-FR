---
title: Composant d’image
description: Le composant Image des composants principaux est un composant d’image adaptatif qui permet d’effectuer des modifications statiques.
role: Architect, Developer, Admin, User
exl-id: c5e57f4b-139f-40e7-8d79-be9a74360b63
source-git-commit: 395a1669cf3e17f649c23852addc37316b923bfd
workflow-type: ht
source-wordcount: '1796'
ht-degree: 100%

---

# Composant d’image {#image-component}

Le composant Image des composants principaux est un composant d’image adaptatif qui permet d’effectuer des modifications statiques.

## Utilisation {#usage}

Le composant Image comprend une sélection des images adaptatives et un comportement réactif avec chargement différé pour le visiteur de la page, ainsi qu’un positionnement et un recadrage des images faciles pour l’auteur du contenu.

Les largeurs d’image et les paramètres supplémentaires peuvent être définis par l’auteur du modèle dans la [boîte de dialogue de conception](#design-dialog). L’éditeur de contenu peut charger ou sélectionner des ressources dans la [boîte de dialogue de configuration.](#configure-dialog)

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Image est v3, qui a été introduite avec la version 2.18.0 des composants principaux en février 2022. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v3 | - | Compatible | Compatible |
| [v2](v2/image.md) | Compatible | Compatible | Compatible |
| [v1](v1/image-v1.md) | Compatible | Compatible | - |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Fonctions réactives {#responsive-features}

Le composant d’image s’accompagne de fonctions réactives efficaces prêtes à l’emploi. Au niveau du modèle de page, la [boîte de dialogue de conception](#design-dialog) permet de définir les largeurs par défaut du fichier image. Le composant d’image charge alors automatiquement la largeur correcte à afficher en fonction de la taille de la fenêtre du navigateur. Lorsque la fenêtre est redimensionnée, le composant d’image charge dynamiquement la taille d’image correcte, instantanément. Les développeurs de composants n’ont pas à définir des requêtes multimédias personnalisées, puisque le composant d’image est déjà optimisé pour charger le contenu.

En outre, le composant d’image prend en charge le chargement différé afin de différer le chargement du fichier image réel jusqu’à ce qu’il soit visible dans le navigateur, ce qui augmente la réactivité des pages.

>[!TIP]
>
>Consultez la section [Servlet d’image adaptative](#adaptive-image-servlet) pour plus d’informations techniques sur ces fonctionnalités et des conseils sur l’optimisation de la sélection du rendu.

## Prise en charge de Dynamic Media {#dynamic-media}

Le composant d’image (à partir de la [version 2.13.0](/help/versions.md)) prend en charge les ressources [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/dynamic-media.html?lang=fr#dynamicmedia). [Lorsqu’elles sont activées](#design-dialog), ces fonctionnalités offrent la possibilité d’ajouter des fichiers d’image Dynamic Media par un simple glisser-déposer ou par le biais du navigateur de ressources, comme vous le feriez pour toute autre image. En outre, les modificateurs d’image, les paramètres d’image prédéfinis et les recadrages intelligents sont également pris en charge.

Vos expériences web créées avec les composants principaux bénéficient des fonctionnalités d’image Dynamic Media sur plusieurs plateformes, hautement performantes, robustes, enrichies et optimisées par Sensei.

## Prise en charge SVG {#svg-support}

Les composants SVG (Scalable Vector Graphics) sont pris en charge par le composant d’image.

* Les opérations de glisser-déplacer d’une ressource SVG à partir de DAM et le téléchargement d’un fichier SVG depuis un système de fichiers local sont pris en charge.
* La servlet d’image adaptative diffuse le fichier SVG d’origine en flux continu (les transformations sont ignorées).
* Pour une image SVG, les « images intelligentes » et les « tailles intelligentes » sont définies sur un tableau vide dans le modèle d’image.

### Sécurité {#security}

Pour des raisons de sécurité, l’éditeur d’image ne fait jamais appel au fichier SVG d’origine. Il est appelé par `<img src=“path-to-component”>`. Cela empêche le navigateur d’exécuter les scripts incorporés dans le fichier SVG.

>[!NOTE]
>
>La prise en charge de SVG nécessite la version 2.1.0, ou ultérieure, des composants principaux et le [Service Pack 2](https://experienceleague.adobe.com/docs/experience-manager-64/release-notes/sp-release-notes.html?lang=fr) pour AEM 6.4, ou version ultérieure, pour être compatible avec les [fonctionnalités de l’éditeur d’image](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/components-templates/image-editor.html?lang=fr) d’AEM.

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant d’image et voir des exemples de ses options de configuration, ainsi que la sortie HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_image_fr).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant d’image [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_image_v2_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

Le composant d’image prend en charge les [microdonnées schéma.org](https://schema.org).

## Boîte de dialogue de configuration {#configure-dialog}

Le composant Image comprend une boîte de dialogue de configuration, qui fournit la définition, la description ainsi que les propriétés de base de lʼimage.

### Onglet Contenu {#asset-tab}

![Onglet Contenu de la boîte de dialogue de configuration du composant Image](/help/assets/image-configure-asset.png)

* **Hériter l’image en vedette de la page** : si vous cochez cette option, lʼ[image en vedette de la page liée](page.md) ou l’image de la page active si l’image n’est pas liée est utilisée.

* **Texte secondaire pour l’accessibilité** : ce champ vous permet de fournir une description de l’image pour les utilisateurs souffrant de déficience visuelle.

   * **Hériter le texte secondaire de la page** : cette option utilise la description secondaire de la valeur de la ressource liée des métadonnées `dc:description` dans la gestion des ressources numériques (DAM) ou de la page active si aucune ressource n’est liée.

* **Ressource image**
   * Déposez un fichier depuis l’[explorateur de ressources](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=fr) ou appuyez sur l’option **parcourir** pour effectuer un téléchargement à partir d’un système de fichiers local.
   * Appuyez ou cliquez sur **Effacer** pour désélectionner l’image actuellement sélectionnée.
   * Appuyez ou cliquez sur **Modifier** pour [gérer les rendus de la ressource](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=fr) dans l’éditeur de ressources.

* **Ne pas fournir de texte secondaire** : cette option marque lʼimage afin quʼelle soit ignorée par les technologies dʼassistance, comme les lecteurs dʼécran, dans les cas où lʼimage existe à des fins dʼillustration et ne comporte pas de signification particulière.

### Onglet Métadonnées {#metadata-tab}

![Onglet Métadonnées de la boîte de dialogue de configuration du composant Image](/help/assets/image-configure-metadata.png)

* **Type de paramètre prédéfini** : définit les types de paramètres d’image prédéfinis disponibles, soit **Paramètre d’image prédéfini** ou **Recadrage intelligent** et n’est disponible que lorsque les [fonctionnalités de Dynamic Media](#dynamic-meida) sont activées.
   * **Paramètre d’image prédéfini** : lorsque **Type de paramètre prédéfini** dans **Paramètre d’image prédéfini** est sélectionné, la liste déroulante **Paramètre d’image prédéfini** est disponible, ce qui permet de sélectionner les paramètres prédéfinis Dynamic Media disponibles. Cette option n’est disponible que si des paramètres prédéfinis sont définis pour la ressource sélectionnée.
   * **Recadrage intelligent** : lorsque **Type de paramètre prédéfini** dans **Recadrage intelligent** est sélectionné, la liste déroulante **Rendu** est disponible, ce qui permet de sélectionner les rendus disponibles de la ressource sélectionnée. Cette option n’est disponible que si des rendus sont définis pour la ressource sélectionnée.
   * **Modificateurs d’images** : il est possible de définir ici d’autres commandes de traitement d’images Dynamic Media, séparées par des caractères `&`, quel que soit le **type de paramètre prédéfini** sélectionné.
* **Légende** : des informations supplémentaires sur l’image sont affichées par défaut sous l’image.
   * **Obtenir la légende à partir de DAM** : lorsque cette option est cochée, le texte de légende de l’image est renseigné avec la valeur des métadonnées `dc:title` dans DAM.
   * **Afficher la légende dans une fenêtre contextuelle** : si cette option est activée, la légende ne s’affiche pas sous l’image, mais dans une fenêtre contextuelle, dans certains navigateurs, lorsque vous pointez sur l’image.
* **Lien** : lier l’image à une autre ressource.
   * Utilisez la boîte de dialogue de sélection pour créer un lien vers une autre ressource AEM.
   * Si vous ne créez pas de lien vers une ressource AEM, saisissez l’URL absolue. Les URL non absolues seront interprétées comme relatives à AEM.
   * **Ouvrir le lien dans un nouvel onglet** : cette option ouvre le lien dans une nouvelle fenêtre du navigateur.
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

>[!TIP]
>
>Les options **Recadrage intelligent** et **Paramètre d’image prédéfini** s’excluent mutuellement. Si un auteur doit utiliser un paramètre d’image prédéfini associé à un rendu avec recadrage dynamique, il devra utiliser les **modificateurs d’image** pour ajouter manuellement ce paramètre.

### Onglet Styles {#styles-tab-edit}

![Onglet Styles de la boîte de dialogue de modification du composant Image](/help/assets/image-configure-styles.png)

Le composant Image prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

Utilisez la liste déroulante pour sélectionner les styles à appliquer au composant. Les sélections effectuées dans la boîte de dialogue de modification ou dans la barre d’outils du composant ont le même effet.

Pour que le menu déroulant soit disponible, les styles doivent être configurés pour ce composant dans la [boîte de dialogue de conception](#design-dialog).

## Boîte de dialogue de conception {#design-dialog}

![Onglet principal de la boîte de dialogue de conception du composant Image](/help/assets/image-design-main.png)

* **Activer les fonctionnalités DM** : lorsque cette option est cochée, les [fonctionnalités Dynamic Media](#dynamic-media) sont disponibles.
   * Dynamic Media doit être activé dans l’environnement pour que cette option apparaisse.
* **Désactiver le chargement différé** : lorsque cette option est cochée, le composant précharge toutes les images sans chargement différé.
* **L’image est décorative** : définissez si l’option d’image décorative est activée automatiquement lors de l’ajout du composant d’image à une page.
* **Obtenir un texte alternatif à partir de DAM** : définissez si l’option permettant de récupérer le texte de remplacement de DAM est automatiquement activée lors de l’ajout du composant d’image à une page.
* **Obtenir la légende à partir de DAM** : définissez si l’option permettant de récupérer la légende à partir de DAM est automatiquement activée lors de l’ajout du composant d’image à une page.
* **Afficher la légende dans une fenêtre contextuelle** : définissez si l’option permettant d’afficher la légende d’image est automatiquement activée lors de l’ajout du composant d’image à une page.
* **Redimensionner la largeur** : cette valeur est utilisée pour redimensionner la largeur des images de base qui sont des ressources DAM.
   * Les proportions des images sont conservées.
   * Si la valeur est supérieure à la largeur de l’image, cette valeur nʼa aucun effet.
   * Cette valeur n’a aucun effet sur les images au format SVG.

Vous pouvez définir une liste de largeurs en pixels pour l’image, le composant chargera alors automatiquement la largeur la plus appropriée en fonction de la taille du navigateur. Il s’agit d’une partie importante des [fonctions réactives](#responsive-features) du composant d’image.

* **Largeurs** : définit une liste de largeurs en pixels pour l’image ; le composant charge automatiquement la largeur la plus appropriée en fonction de la taille du navigateur.
   * Appuyez ou cliquez sur le bouton **Ajouter** pour ajouter une autre taille.
      * Utilisez les poignées de capture pour réorganiser l’ordre des tailles.
      * Utilisez l’icône **Supprimer** pour supprimer une largeur.
   * Par défaut, le chargement des images est différé jusqu’à ce qu’elles deviennent visibles.
      * Sélectionnez l’option **Désactiver le chargement différé** pour charger les images au chargement de la page.
* **Qualité JPEG** : facteur de qualité (exprimé par un pourcentage entre 0 et 100) pour les images JPEG transformées (mises à l’échelle ou recadrées, par exemple).

>[!TIP]
>
>Consultez la section [Servlet d’image adaptative](#adaptive-image-servlet) pour plus d’informations techniques sur ses fonctionnalités et des conseils sur l’optimisation de la sélection du rendu en définissant soigneusement vos largeurs.

### Onglet Styles {#styles-tab}

Le composant d’image prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

## Servlet d’image adaptative {#adaptive-image-servlet}

Le composant d’image utilise la servlet d’image adaptative des composants principaux. [La servlet d’image adaptative](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) est en charge du traitement des images et de leur diffusion en flux continu. Les développeurs peuvent l’utiliser dans le cadre de leur [personnalisation des composants principaux](/help/developing/customizing.md).

### Optimisation de la sélection du rendu {#optimizing-rendition-selection}

La servlet d’image adaptative tente de sélectionner le meilleur rendu pour la taille et le type d’image demandés. Il est recommandé de définir les rendus DAM et les largeurs autorisées des composants Image de façon synchronisée afin que la servlet d’image adaptative effectue le moins de traitement possible.

Cela améliore les performances et évite que certaines images ne soient pas correctement traitées par la bibliothèque de traitement des images sous-jacente.

>[!NOTE]
>
>Les requêtes conditionnelles effectuées par le biais de `Last-Modified` en-tête sont prises en charge par la servlet d’image adaptative, mais la mise en cache de l’en-tête `Last-Modified` [doit être activée dans Dispatcher](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=fr#caching-http-response-headers).
>
>L’exemple de configuration de Dispatcher d’[AEM Project Archetype](/help/developing/archetype/overview.md) contient déjà cette configuration.

## Couche de données client Adobe {#data-layer}

Le composant Image prend en charge la [couche de données client Adobe](/help/developing/data-layer/overview.md).
