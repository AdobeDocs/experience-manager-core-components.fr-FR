---
title: Composant d’image (v1)
description: Le composant d’image des composants principaux est un composant d’image adaptatif qui permet d’effectuer des modifications statiques.
index: n
role: Architect, Developer, Administrator, Business Practitioner
translation-type: ht
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: ht
source-wordcount: '1234'
ht-degree: 100%

---


# Composant d’image (v1) {#image-component-v}

Le composant d’image des composants principaux est un composant d’image adaptatif qui permet d’effectuer des modifications statiques.

## Utilisation {#usage}

Le composant d’image permet de placer facilement les ressources d’image et permet une édition statique. Il présente une sélection d’image adaptative avec chargement différé et recadrage pour l’auteur du contenu.

Les largeurs d’image autorisées ainsi que le recadrage et les paramètres supplémentaires peuvent être définis par l’auteur du modèle dans la [boîte de dialogue de conception](#design-dialog). L’éditeur de contenu peut télécharger ou sélectionner des ressources dans la [boîte de dialogue de configuration](#configure-dialog) et recadrer l’image dans la [boîte de dialogue de modification](#edit-dialog). Pour plus de commodité, une simple modification statique de l’image est également disponible.

## Version et compatibilité {#version-and-compatibility}

Ce document décrit la version v1 du composant d’image, introduite à l’origine avec la version 1.0.0 des composants principaux avec AEM 6.3.

Le tableau ci-après répertorie la compatibilité de la version v1 du composant d’image.

| Version d’AEM | Composant d’image v1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Ce document décrit la version v1 du composant d’image.
>
>Pour plus d’informations sur la version actuelle du composant d’image, voir le document [Composant d’image](/help/components/image.md).

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple extrait de [We.Retail](https://helpx.adobe.com/fr/experience-manager/6-4/sites/developing/using/we-retail.html).

### Capture d’écran {#screenshot}

![](/help/assets/chlimage_1-7.png)

### HTML {#html}

```
<div class="cmp cmp-image aem-GridColumn aem-GridColumn--default--12">
 
        <noscript data-cmp-image="{&#34;smartImages&#34;:[],&#34;smartSizes&#34;:[],&#34;lazyEnabled&#34;:true}">
            <img src="/content/we-retail/us/en/equipment/_jcr_content/root/responsivegrid/image.img.jpg" alt="Surfboard"/>
        </noscript>

</div>
```

### JSON {#json}

```
"image": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "smartSizes": [],
              "smartImages": [],
              "lazyEnabled": true,
              "src": "/content/we-retail/us/en/equipment/equipment/jcr%3acontent/root/responsivegrid/image.img.jpeg",
              ":type": "weretail/components/content/image"
            }
```

>[!NOTE]
>
>L’exportation JSON à partir des composants principaux nécessite la version 1.1.0 des composants principaux. Pour plus d’informations, voir les [informations de compatibilité des composants principaux v1](/help/versions.md).

## Boîte de dialogue de configuration {#configure-dialog}

Outre la [boîte de dialogue de modification](#edit-dialog) et la [boîte de dialogue de conception](#design-dialog) standard, le composant d’image propose une boîte de dialogue de configuration dans laquelle l’image elle-même est définie avec sa description et ses propriétés de base.

![](/help/assets/chlimage_1-50.png)

* **Ressource image**
   * Déposez un fichier depuis l’[explorateur de ressources](https://helpx.adobe.com/experience-manager/6-3/sites/authoring/using/author-environment-tools.html#main-pars_title) ou appuyez sur l’option **parcourir** pour effectuer un téléchargement à partir d’un système de fichiers local.
   * Appuyez ou cliquez sur **Effacer** pour désélectionner l’image actuellement sélectionnée.
   * Appuyez ou cliquez sur **Modifier** pour [gérer les rendus de la ressource](https://helpx.adobe.com/experience-manager/6-3/assets/using/managing-assets-touch-ui.html#main-pars_title_19) dans l’éditeur de ressources.

* **L’image est décorative** : vérifiez si l’image doit être ignorée par les dispositifs d’assistance et ne requiert donc pas de texte de remplacement. Cela s’applique uniquement aux images décoratives.
* **Texte de remplacement** : alternative textuelle de la signification ou de la fonction de l’image, pour les malvoyants.
* **Lien**
   * Liez l’image à une autre ressource.
   * Utilisez la boîte de dialogue de sélection pour créer un lien vers une autre ressource AEM.
   * Si vous ne créez pas de lien vers une ressource AEM, saisissez l’URL absolue. Les URL non absolues seront interprétées comme relatives à AEM.

* **Légende** : des informations supplémentaires sur l’image sont affichées par défaut sous l’image.
* **Afficher la légende dans une fenêtre contextuelle** : si cette option est activée, la légende ne s’affiche pas sous l’image, mais dans une fenêtre contextuelle dans certains navigateurs lorsque vous pointez sur l’image.

## Boîte de dialogue de modification {#edit-dialog}

La boîte de dialogue de modification permet à l’auteur du contenu de recadrer, de modifier la carte de lancement et de zoomer sur l’image.

![](/help/assets/chlimage_1-8.png)

* Commencer recadrage

   ![](/help/assets/chlimage_1-9.png)

   Cette option ouvre une liste déroulante pour les proportions de recadrage prédéfinies.

   * Choisissez l’option **Main libre** pour définir votre propre recadrage.
   * Choisissez l’option **Supprimer le recadrage** pour afficher la ressource d’origine.

   Une fois qu’une option de recadrage est sélectionnée, utilisez les poignées bleues pour dimensionner le recadrage sur l’image.

   ![](/help/assets/chlimage_1-10.png)

* Rotation à droite

   ![](/help/assets/chlimage_1-11.png)

   Utilisez cette option pour faire pivoter l’image de 90° vers la droite (dans le sens horaire).

* Lancer une Map

   ![](/help/assets/chlimage_1-12.png)

   Utilisez cette option pour appliquer une carte de lancement à l’image. Cette option ouvre une nouvelle fenêtre permettant à l’utilisateur de sélectionner la forme de la carte :

   * **Ajouter une map rectangulaire**
   * **Ajouter une map circulaire**
   * **Ajouter une map polygonal**

      * Par défaut, une carte en triangle est ajoutée. Cliquez deux fois sur une ligne de la forme pour ajouter une nouvelle poignée de redimensionnement bleue d’un nouveau côté.

   Lorsqu’une forme de carte est sélectionnée, elle est superposée sur l’image pour le redimensionnement. Faites glisser les poignées de redimensionnement bleues pour ajuster la forme.

   ![](/help/assets/chlimage_1-13.png)

   Après avoir dimensionné la carte de lancement, cliquez dessus pour ouvrir une barre d’outils flottante afin de définir le chemin du lien.

   * **Chemin**
      * Utilisez l’option Sélecteur de chemin pour sélectionner un chemin dans AEM.
      * Si le chemin d’accès ne figure pas dans AEM, utilisez l’URL absolue. Les chemins non absolus seront interprétés par rapport à AEM.

      * **Texte de remplacement**
Autre description de la destination du chemin.
      * **Cible**
         * **Même onglet**
         * **Nouvel onglet**
         * **Cadre parent**
         * **Cadre supérieur**

   Appuyez ou cliquez sur la coche bleue pour enregistrer, le x noir pour annuler et la corbeille rouge pour supprimer la carte.

   ![](/help/assets/chlimage_1-14.png)

* Réinitialiser le zoom

   ![](/help/assets/chlimage_1-15.png)

   Si l’image a déjà été agrandie, utilisez cette option pour réinitialiser le niveau de zoom.

* Ouvrir le curseur de zoom

   ![](/help/assets/chlimage_1-16.png)

   Utilisez cette option pour afficher un curseur permettant de contrôler le niveau de zoom de l’image.

   ![](/help/assets/chlimage_1-17.png)

L’éditeur statique peut également être utilisé pour modifier l’image. En raison d’un espace limité, seules les options de base sont disponibles en ligne. Pour des options de modification complètes, utilisez le mode Plein écran.

![](/help/assets/chlimage_1-18.png)

>[!NOTE]
>
>Les opérations de modification d’image (recadrage, pivotement, rotation) ne sont pas prises en charge pour les images GIF. Aucune modification de ce type apportée en mode d’édition aux fichiers GIF n’est conservée.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir le recadrage, le téléchargement et la rotation dont dispose l’auteur du contenu lors de l’utilisation de ce composant.

### Principal {#main}

Sur l’onglet **Principal**, vous pouvez définir une liste de largeurs d’image (en pixels) autorisées afin de charger automatiquement la largeur la plus appropriée de la liste.

![](/help/assets/chlimage_1-51.png)

Appuyez ou cliquez sur le bouton Ajouter pour ajouter une autre taille.

* Utilisez les poignées de capture pour réorganiser l’ordre des tailles.
* Utilisez l’icône Supprimer pour supprimer une largeur.

Par défaut, le chargement des images est différé jusqu’à ce qu’elles deviennent visibles. Sélectionnez l’option **Désactiver le chargement différé** pour charger les images au chargement de la page.

### Fonctionnalités {#features}

Sur l’onglet **Fonctionnalités**, vous pouvez définir les options disponibles pour les auteurs de contenu lors de l’utilisation du composant, y compris les options de téléchargement, d’orientation et de recadrage.

* Source

   ![](/help/assets/chlimage_1-19.png)

   Sélectionnez l’option **Autoriser le transfert des ressources depuis le système de fichiers** pour permettre aux auteurs de contenu de télécharger des images à partir de leur ordinateur local. Pour forcer les auteurs de contenu à sélectionner uniquement des ressources à partir d’AEM, désactivez cette option.

* Orientation

   ![](/help/assets/chlimage_1-20.png)

   * **Rotation** : utilisez cette option pour permettre à l’auteur de contenu d’utiliser l’option **Rotation à droite**.
   * **Symétrie** : Utilisez cette option pour permettre à l’auteur de contenu d’appliquer 
les options **Symétrie horizontale** et **Rotation verticale**.
   >[!CAUTION]
   >
   >L’option **Symétrie** est désactivée par défaut. L’activation de cette option affichera les boutons **Symétrie verticale** et **Symétrie horizontale** dans la boîte de dialogue de modification du composant d’image. Toutefois, cette fonction n’est actuellement pas prise en charge par AEM et les modifications effectuées à l’aide de ces options ne seront pas conservées.

* Recadrage

   ![](/help/assets/chlimage_1-21.png)

   Sélectionnez l’option **Autoriser le recadrage** pour permettre à l’auteur du contenu de recadrer l’image dans le composant au sein de la boîte de dialogue de modification.
   * Cliquez sur **Ajouter** pour ajouter des proportions de recadrage prédéfinies.
   * Saisissez un nom descriptif. Celui-ci s’affichera dans la liste déroulante **Commencer recadrage**.
   * Entrez les proportions.
   * Utilisez les poignées de glissement pour réorganiser l’ordre des proportions.
   * Utilisez l’icône de corbeille pour supprimer des proportions.

   >[!CAUTION]
   >
   >Remarque : Dans AEM, les proportions de recadrage sont définies en tant que **hauteur/largeur**. Cela diffère de la définition conventionnelle de la largeur/hauteur. Cela a été créée pour des raisons de compatibilité héritée. Les auteurs de contenu ne verront aucune différence tant que vous indiquez le nom clair des proportions, car le nom s’affiche dans l’interface utilisateur et non les proportions.

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant d’image [se trouve sur GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/image/v1/image).

Le projet sur les composants principaux peut être téléchargé depuis GitHub.

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).
