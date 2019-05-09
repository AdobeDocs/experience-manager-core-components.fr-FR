---
title: Composant de l’image
seo-title: Composant de l’image
description: Le composant d'image de composant de base est un composant d'image adaptative qui permet d'effectuer des modifications en place.
seo-description: Le composant d'image de composant de base est un composant d'image adaptative qui permet d'effectuer des modifications en place.
uuid: 1 a 229 d 42-2428-43 aa -895 a -9 b 7 c 1 bf 02834
contentOwner: Utilisateur
content-type: référence
topic-tags: création
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: d 4684 f 33-2 fb 5-4 f 32-866 f -7136 cf 1800 d 7
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Composant de l’image{#image-component}

Le composant d&#39;image de composant de base est un composant d&#39;image adaptative qui comporte des modifications en place.

## Utilisation {#usage}

Le composant Image permet un placement facile des fichiers d&#39;image et offre une modification statique. Il présente une sélection d&#39;image adaptative avec chargement différé et recadrage pour l&#39;auteur du contenu.

Les largeurs de l&#39;image ainsi que le recadrage et les paramètres supplémentaires peuvent être définis par l&#39;auteur du modèle dans le dialogue [de conception](#design-dialog). L&#39;éditeur de contenu peut télécharger ou sélectionner des fichiers dans la [boîte de dialogue de configuration](#configure-dialog) et recadrer l&#39;image dans la boîte de dialogue [Modifier](#edit-dialog). Pour plus de commodité, une simple modification statique de l&#39;image est également disponible.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Image est v 2, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018 et est décrite dans ce document.

Le tableau suivant détaille toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatible | Compatible | Compatible |
| [v1](image-v1.md) | Compatible | Compatible | Compatible |

Pour plus d&#39;informations sur les versions et les versions des composants principaux, consultez les versions des composants de Document [principaux](versions.md).

## Prise en charge SVG {#svg-support}

Les composants SVG (Scalable Vector Graphics) sont pris en charge par le composant Image.

* Les opérations de glisser-déplacer d&#39;un fichier SVG à partir de DAM et le transfert d&#39;un fichier SVG depuis un système de fichiers local sont prises en charge.
* La servlet d&#39;image adaptative diffuse le fichier SVG d&#39;origine en flux continu (les transformations sont ignorées).
* Pour une image SVG, les « images intelligentes » et les « tailles intelligentes » sont définies sur un tableau vide dans le modèle d&#39;image.

### Sécurité {#security}

Pour des raisons de sécurité, le SVG d&#39;origine n&#39;est jamais appelé directement par l&#39;éditeur d&#39;images. It is called through `<img src=“path-to-component”>`. Par conséquent, le navigateur empêche l&#39;exécution des scripts incorporés dans le fichier SVG.

>[!CAUTION]
>
>La prise en charge SVG requiert la version 2.1.0 des composants principaux ou supérieurs avec [Service Pack 2](https://helpx.adobe.com/experience-manager/6-4/release-notes/sp-release-notes.html) pour AEM 6.4 ou [Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) pour AEM 6.3 ou une version ultérieure pour prendre en charge [les nouvelles fonctionnalités d&#39;éditeur d&#39;images](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/image-editor.html) dans AEM.

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple tiré de [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Capture d’écran {#screenshot}

![](assets/chlimage_1-7.png)

### Bibliothèque de composants

Pour tester le composant Image ainsi que les exemples d&#39;options de configuration, ainsi que la sortie HTML et JSON, consultez la [bibliothèque Composant](http://opensource.adobe.com/aem-core-wcm-components/library/image.html).

### Détails techniques {#technical-details}

Vous trouverez la documentation technique la plus récente sur le composant [Image sur github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/image/v2/image).

Vous trouverez plus d&#39;informations sur le développement des composants principaux dans la documentation destinée aux développeurs de composants [principaux](developing.md).

>[!NOTE]
>
>A compter de la version 2.1.0 de Core Components, le composant Image prend en charge [schema.org des microdonnées](https://schema.org).

## Configurer le dialogue {#configure-dialog}

Outre la boîte [de dialogue](#edit-dialog) de modification et la boîte de dialogue [de conception standard](#design-dialog), le composant d&#39;image propose un dialogue de configuration dans lequel l&#39;image elle-même est définie avec sa description et ses propriétés de base.

### Onglet Ressources {#asset-tab}

![](assets/screen_shot_2018-01-08at114245.png)

* **Ressource image**
   * Déposez un fichier depuis l&#39;explorateur [de ressources](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/author-environment-tools.html) ou appuyez sur l&#39;option **de navigation** à télécharger à partir d&#39;un système de fichiers local.
   * Appuyez ou cliquez **sur Effacer** pour désélectionner l&#39;image actuellement sélectionnée.
   * Appuyez ou cliquez **sur Modifier** pour [gérer les rendus de la ressource](https://helpx.adobe.com/experience-manager/6-5/assets/using/managing-assets-touch-ui.html) dans l&#39;éditeur de ressources.

### Onglet Métadonnées {#metadata-tab}

![](assets/screen_shot_2018-01-08at114527.png)

* **L&#39;image est un**contrôle décoratif
si l&#39;image doit être ignorée par les technologies d&#39;assistance et ne nécessite donc pas de texte alternatif. Cela s&#39;applique uniquement aux images décoratives.
* **Remplacement** textuel textuel de la signification ou de la fonction de l&#39;image, pour les malvoyants.
   * Obtenir un texte alternatif à partir de DAM : lorsque vous cochez le texte alternatif de l&#39;image, la valeur des `dc:description` métadonnées dans DAM est renseignée.

* **Légende**
d&#39;autres informations sur l&#39;image, affichées par défaut sous l&#39;image.
   * **Obtenir une légende à partir de DAM**
Lorsque le texte de légende de l&#39;image est vérifié, la valeur des `dc:title` métadonnées dans DAM est renseignée.
   * **Afficher la légende en tant que fenêtre contextuelle** lorsque cette option est cochée, la légende ne s&#39;affiche pas sous l&#39;image, mais comme fenêtre contextuelle affichée par certains navigateurs lorsque vous passez la souris sur l&#39;image.

* **Lien**
   * Liez l&#39;image à une autre ressource.
   * Utilisez le dialogue de sélection pour créer un lien vers une autre ressource AEM.
   * Si vous ne créez pas de lien vers une ressource AEM, saisissez l&#39;URL absolue. Les URL non solutionnées seront interprétées comme par rapport à AEM.

## Modifier le dialogue {#edit-dialog}

La boîte de dialogue Modifier permet à l&#39;auteur du contenu de recadrer, de modifier le plan de lancement et de zoomer sur l&#39;image.

![](assets/chlimage_1-8.png)

* Commencer recadrage

   ![](assets/chlimage_1-9.png)

   Cette option ouvre une liste déroulante pour les proportions de recadrage prédéfinies.

   * Choisissez l&#39;option Main **libre** pour définir votre propre recadrage.
   * Choisissez l&#39;option **Supprimer le recadrage** pour afficher la ressource d&#39;origine.
   Une fois qu&#39;une option de recadrage est sélectionnée, utilisez les poignées bleue pour dimensionner le recadrage sur l&#39;image.

   ![](assets/chlimage_1-10.png)

* Rotation à droite

   ![](assets/chlimage_1-11.png)

   Utilisez cette option pour faire pivoter l&#39;image de 90 ° vers la droite (dans le sens horaire).

* Rotation horizontale

   ![](assets/screen_shot_2018-04-16at091404.png)

   Utilisez cette option pour retourner l&#39;image horizontalement ou faire pivoter l&#39;image de 180 ° sur l&#39;axe y.

* Rotation verticale

   ![](assets/screen_shot_2018-04-16at091410.png)

   Utilisez cette option pour retourner l&#39;image verticalement ou faire pivoter l&#39;image de 180 ° sur l&#39;axe X.

* Lancer une Map

   >[!CAUTION]
   >
   >La fonctionnalité de Carte de lancement requiert la version 2.1.0 des composants principaux ou ultérieure avec [Service Pack 2](https://helpx.adobe.com/experience-manager/6-4/release-notes/sp-release-notes.html) pour AEM 6.4 ou [Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) pour AEM 6.3 ou une version ultérieure pour prendre en charge [les nouvelles fonctionnalités d&#39;éditeur d&#39;images](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/image-editor.html) dans AEM.

   ![](assets/chlimage_1-12.png)

   Utilisez cette option pour appliquer un mappage de lancement à l&#39;image. Cette option permet d&#39;ouvrir une nouvelle fenêtre permettant à l&#39;utilisateur de sélectionner la forme de la carte :

   * **Ajouter une map rectangulaire**
   * **Ajouter une map circulaire**
   * **Ajouter une map polygonal**
      * Par défaut, un triangle est ajouté. Cliquez deux fois sur une ligne de la forme pour ajouter une nouvelle poignée de redimensionnement bleu d&#39;un nouveau côté.
   Lorsqu&#39;une forme de mappage est sélectionnée, elle est superposée sur l&#39;image pour le redimensionnement. Faites glisser et déposez les poignées de redimensionnement bleu pour ajuster la forme.

   ![](assets/chlimage_1-13.png)

   Après avoir dimensionné le mappage de lancement, cliquez dessus pour ouvrir une barre d&#39;outils flottante afin de définir le chemin du lien.

   * **Chemin**
      * Utilisation de l&#39;option Sélecteur de chemin pour sélectionner un chemin dans AEM
      * Si le chemin d&#39;accès ne figure pas dans AEM, utilisez l&#39;URL absolue. Les chemins non absolus seront interprétés par rapport à AEM.
   * **Texte**
de remplacement Description de la destination du chemin
   * **Cible**
      * **Même onglet**
      * **Nouvel onglet**
      * **Cadre parent**
      * **Cadre supérieur**
   Appuyez ou cliquez sur la coche bleue à enregistrer, le x noir à annuler et la corbeille rouge permet de supprimer la carte.

   ![](assets/chlimage_1-14.png)

* Réinitialiser le zoom

   ![](assets/chlimage_1-15.png)

   Si l&#39;image a déjà été agrandie, utilisez cette option pour réinitialiser le niveau de zoom.

* Ouvrir le curseur de zoom

   ![](assets/chlimage_1-16.png)

   Utilisez cette option pour afficher un curseur permettant de contrôler le niveau de zoom de l&#39;image.

   ![](assets/chlimage_1-17.png)

L&#39;éditeur statique peut également être utilisé pour modifier l&#39;image. En raison des limitations de l&#39;espace, seules les options de base sont disponibles en ligne. Pour des options de modification complètes, utilisez le mode Plein écran.

![](assets/chlimage_1-18.png)

>[!NOTE]
>
>Les opérations de modification d&#39;image (recadrage, basculement, rotation) ne sont pas prises en charge pour les images GIF. Aucune modification de ce type apportée en mode d&#39;édition aux fichiers GIF n&#39;est conservée.

## Créer un dialogue {#design-dialog}

Le dialogue de conception permet à l&#39;auteur du modèle de définir les options de recadrage, de téléchargement et de rotation et de transfert que l&#39;auteur du contenu a pour utiliser ce composant.

### Onglet principal {#main-tab}

Sur l&#39;onglet **Principal** , vous pouvez définir une liste de largeurs en pixels pour que l&#39;image charge automatiquement la largeur la plus appropriée dans la liste.

En outre, vous pouvez définir quelles options de composant générales sont automatiquement ou désactivées lorsque l&#39;auteur ajoute le composant à une page.

![](assets/screenshot_2018-10-19at102756.png)

* **Activez le chargement
différé** de l&#39;option Définir si l&#39;option de chargement différé est activée automatiquement lors de l&#39;ajout du composant d&#39;image à une page.
* **Image est décorative**
Définissez si l&#39;option d&#39;image décorative est activée automatiquement lors de l&#39;ajout du composant d&#39;image à une page.
* **Obtenir un texte alternatif de DAM**
Définissez si l&#39;option permettant de récupérer le texte alternatif du DAM est automatiquement activée lors de l&#39;ajout du composant d&#39;image à une page.
* **Obtenir une légende à partir de DAM**
Définissez si l&#39;option permettant de récupérer la légende à partir du DAM est automatiquement activée lors de l&#39;ajout du composant d&#39;image à une page.
* **Afficher la légende sous forme de fenêtre contextuelle** Définissez si l&#39;option permettant d&#39;afficher la légende d&#39;image est automatiquement activée lors de l&#39;ajout du composant d&#39;image à une page.
* **Désactivez la vérification du suivi**
UUID pour désactiver le suivi de l&#39;UUID du fichier d&#39;image.

* **Largeurs**
Définit une liste de largeurs en pixels pour que l&#39;image charge automatiquement la largeur la plus appropriée dans la liste.
   * Appuyez ou cliquez sur le **bouton Ajouter** pour ajouter une autre taille.
      * Utilisez les poignées de capture pour réorganiser l&#39;ordre des tailles.
      * Utilisez l&#39;icône **Supprimer** pour supprimer une largeur.
   * Par défaut, le chargement des images est ddeferredjusqu&#39;à ce qu&#39;ils deviennent visibles.
      * Sélectionnez l&#39;option **Désactiver le chargement différé** pour charger les images au chargement de la page.
* **Qualité**
JPEG Le facteur de qualité (en pourcentage compris entre 0 et 100) pour les images JPEG transformés (redimensionnées ou recadrées, par exemple).

>[!CAUTION]
>
>L&#39;option Qualité JPEG est disponible à compter de la version 2.2.0 des composants principaux.

>[!NOTE]
>
>A compter de la version 2.2.0 des composants principaux, le composant Image ajoute l&#39;attribut UUID unique `data-asset-id` à la ressource d&#39;image afin d&#39;autoriser le suivi et l&#39;analyse du nombre de vues reçues par les ressources individuelles.

### Onglet Fonctionnalités {#features-tab}

Sur l&#39;onglet **Fonctionnalités** , vous pouvez définir les options disponibles pour les auteurs de contenu lors de l&#39;utilisation du composant, y compris les options de transfert, d&#39;orientation et de recadrage.

* Source

   ![](assets/chlimage_1-19.png)

   Sélectionnez l&#39;option **Autoriser le téléchargement de fichiers à partir du système** de fichiers pour permettre aux auteurs de contenu de télécharger des images à partir de son ordinateur local. Pour forcer les auteurs de contenu à sélectionner uniquement des fichiers à partir d&#39;AEM, désactivez cette option.

* Orientation

   ![](assets/chlimage_1-20.png)

* **Rotation**
Utilisez cette option pour permettre à l&#39;auteur de contenu d&#39;utiliser l&#39;option **Pivoter à droite** .
* **Utiliser**
cette option pour permettre à l&#39;auteur de contenu d&#39;utiliser les options **Retourner horizontalement** et **Retourner verticalement** .

   >[!CAUTION]
   >
   >L&#39;option **Retourner** est désactivée par défaut. L&#39;activation de ces boutons affichera les **boutons Retourner verticalement** et **Retourner horizontalement** dans la boîte de dialogue Modifier le composant d&#39;image. Toutefois, cette fonction n&#39;est actuellement pas prise en charge par AEM et les modifications effectuées à l&#39;aide de ces options ne seront pas conservées.

<!-- 
Comment Type: remark
Last Modified By: Chris Bohnert (bohnert)
Last Modified Date: 2017-11-20T05:51:34.378-0500

<p>Added caution based on CQDOC-11457. Hid the flip options in the procedure using the <strong>Draft</strong> option so that when this feature is implemented in CQ-4221539, the <strong>Draft</strong> property can simply be removed along with the caution.</p>
 -->

* Recadrage

   ![](assets/chlimage_1-21.png)

   Sélectionnez l&#39;option **Autoriser le recadrage** pour permettre à l&#39;auteur du contenu de recadrer l&#39;image dans le composant dans la boîte de dialogue Modifier.
   * Cliquez **sur Ajouter** pour ajouter un rapport L/H de recadrage prédéfini.
   * Saisissez un nom descriptif qui s&#39;affiche dans la liste déroulante **Début du recadrage** .
   * Entrez le rapport numérique de l&#39;aspect.
   * Utilisez les poignées de glissement pour réorganiser l&#39;ordre des proportions.
   * Utilisez l&#39;icône de corbeille pour supprimer un rapport L/H.
   >[!CAUTION]
   >
   >Notez que dans AEM, les proportions de recadrage sont définies comme **hauteur/largeur**. Cette valeur diffère de la définition conventionnelle de largeur/hauteur et est effectuée pour des raisons de compatibilité héritées. Les auteurs de contenu ne connaîtront aucune différence tant que vous fournissez un nom clair du rapport dans la mesure où le nom s&#39;affiche dans l&#39;interface utilisateur et non le ratio lui-même.

### Onglet Styles {#styles-tab-1}

Le composant Image prend en charge le système [de style AEM](authoring.md#component-styling).