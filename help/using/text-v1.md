---
title: Composant de texte (v 1)
seo-title: Composant de texte (v 1)
description: 'null'
seo-description: Le composant Text Component est un composant de modification et de composition de texte enrichi qui permet d'effectuer des modifications en place.
uuid: b 787 ebac-fa 85-416 a-b 96 b -9 d 2 ee 85428 ec
content-type: référence
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: d 5 e 37 dc 7-dfd 4-4 a 44-89 b 6-c 15651472 c 43
disttype: dist5
gnavtheme: light
groupsectionnavitems: non
hidemerchandisingbar: inherit
hidepromocomponent: inherit
modalsize: 426x240
noindex: 'true'
index: n
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Composant de texte (v 1){#text-component-v}

Le composant Text Component est un composant de modification et de composition de texte enrichi qui permet d&#39;effectuer des modifications en place.

## Utilisation {#usage}

Le composant Texte propose un puissant éditeur de texte enrichi qui permet d&#39;apporter facilement des modifications de texte dans un éditeur en ligne simplifié, ainsi qu&#39;un format plein écran.

La boîte de dialogue [Modifier la boîte de dialogue](text-v1.md#main-pars_title) permet de modifier en ligne les options limitées avec des fonctionnalités complètes disponibles dans la boîte de dialogue de modification en plein écran. A l&#39;aide de [la boîte de dialogue de conception](text-v1.md#main-pars_title_1995166862), les options de formatage de texte telles que les en-têtes, les caractères spéciaux et les styles de paragraphe peuvent être configurées pour le modèle de l&#39;auteur du contenu.

## Version et compatibilité {#version-and-compatibility}

Ce document décrit la version v 1 du composant de texte, introduite à l&#39;origine avec la version 1.0.0 des composants principaux avec AEM 6.3.

Le tableau suivant répertorie la compatibilité de la version v 1 du composant de texte.

| Version d’AEM | Composant de texte v 1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Ce document décrit la version v 1 du composant de texte.
>
>Pour plus d&#39;informations sur la version actuelle du composant de texte, voir [le document Composant](text.md) Texte.

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple tiré de [We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Capture d’écran {#screenshot}

![](assets/chlimage_1-27.png)

### HTML {#html}

```
<div class="cmp cmp-text aem-GridColumn aem-GridColumn--default--12">
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer porttitor ante a tortor volutpat maximus. Donec eu porta eros. Aenean sit amet eleifend arcu, eu vestibulum magna. Fusce eget nisi tincidunt, tristique felis quis, tincidunt est. Aliquam consequat aliquam quam non eleifend. Phasellus ut magna luctus, aliquam risus eget, fermentum augue. Aliquam lobortis accumsan magna, quis efficitur enim dictum eu. Pellentesque iaculis felis eget felis commodo, non euismod dolor euismod. Quisque nec arcu rutrum, mollis tortor non, sollicitudin odio. Sed dictum nulla mauris, eu pretium dui vulputate a. Maecenas lacus massa, egestas vitae tincidunt eu, interdum et magna. Lorem ipsum dolor sit amet, consectetur adipiscing elit. In eleifend ex lacus, in consectetur nunc interdum et. Donec interdum mi vitae dolor pretium mattis. In quis arcu sapien. Phasellus at metus vitae nisi tincidunt varius.<br />
</p>
</div>
```

### JSON {#json}

```
"text": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "text": "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer porttitor ante a tortor volutpat maximus. Donec eu porta eros. Aenean sit amet eleifend arcu, eu vestibulum magna. Fusce eget nisi tincidunt, tristique felis quis, tincidunt est. Aliquam consequat aliquam quam non eleifend. Phasellus ut magna luctus, aliquam risus eget, fermentum augue. Aliquam lobortis accumsan magna, quis efficitur enim dictum eu. Pellentesque iaculis felis eget felis commodo, non euismod dolor euismod. Quisque nec arcu rutrum, mollis tortor non, sollicitudin odio. Sed dictum nulla mauris, eu pretium dui vulputate a. Maecenas lacus massa, egestas vitae tincidunt eu, interdum et magna. Lorem ipsum dolor sit amet, consectetur adipiscing elit. In eleifend ex lacus, in consectetur nunc interdum et. Donec interdum mi vitae dolor pretium mattis. In quis arcu sapien. Phasellus at metus vitae nisi tincidunt varius.</p>\n",
              "richText": true,
              ":type": "weretail/components/content/text"
            }
```

>[!NOTE]
>
>L&#39;exportation JSON à partir des composants principaux nécessite la version 1.1.0 des composants principaux. Pour plus d&#39;informations, consultez les [informations de compatibilité des composants principaux v 1](versions.md#main-pars_title_236368006) .

## Modifier le dialogue {#edit-dialog}

La boîte de dialogue Modifier propose les outils standard de formatage de texte enrichi qu&#39;un utilisateur devrait utiliser pour composer du texte.

![](assets/chlimage_1-52.png)

* Gras

   ![](assets/chlimage_1-53.png)

   Utilisé pour appliquer une mise en forme gras au texte sélectionné ou au texte gras saisi après le curseur.

   **Ctrl + B** peut être utilisé comme raccourci clavier.

* Italique

   ![](assets/chlimage_1-54.png)

   Utilisé pour appliquer une mise en forme en italique au texte sélectionné ou mettre en italique le texte saisi après le curseur.

   **Ctrl + Je** peut être utilisé comme raccourci clavier.

* Souligné

   ![](assets/chlimage_1-55.png)

   Utilisé pour appliquer une mise en forme soulignée au texte ou au texte souligné sélectionné après le curseur.

   **Ctrl + U** peut être utilisé comme raccourci clavier.

* Indice

   ![](assets/chlimage_1-56.png)

   Utilisé pour mettre en forme le texte ou le texte sélectionné après le curseur comme indice.

* Exposant

   ![](assets/chlimage_1-57.png)

   Utilisé pour mettre en forme le texte ou le texte sélectionné après le curseur comme exposant.

* Coller en tant que texte

   ![](assets/chlimage_1-58.png)

   Colle le texte copié en tant que texte brut sans mise en forme.

   Lorsque vous sélectionnez cette option, une fenêtre s&#39;ouvre lorsque le texte peut être collé en texte brut sans mise en forme pour être inséré dans le texte. Acceptez en appuyant ou en cliquant sur la coche, annulez en appuyant ou en cliquant sur le x.

   ![](assets/chlimage_1-59.png)

* Coller à partir de Word

   ![](assets/chlimage_1-60.png)

   Lorsque vous sélectionnez cette option, une fenêtre s&#39;ouvre lorsque vous pouvez coller le texte en conservant sa mise en forme comme prévisualisation avant sa insertion dans le texte. Acceptez en appuyant ou en cliquant sur la coche, annulez en appuyant ou en cliquant sur le x.

   ![](assets/chlimage_1-61.png)

* Lien hypertexte

   ![](assets/chlimage_1-62.png)

   Utilisez cette option pour convertir le texte sélectionné en hyperlien ou modifier un lien déjà défini. Cette option est uniquement active lorsque le texte est déjà sélectionné et ouvre une fenêtre avec des options supplémentaires pour définir le lien.

   ![](assets/chlimage_1-63.png)

   * Saisissez l&#39;emplacement

      * Utilisation de la boîte de dialogue Ouvrir la sélection pour choisir un chemin dans AEM
      * Si le lien ne figure pas dans AEM, saisissez l&#39;URL absolue (les chemins non absolus sont interprétés comme relatifs par rapport à AEM)
   * Saisissez un autre texte descriptif pour le lien.
   * Sélectionner le comportement des liens

      * Cible
      * Même onglet
      * Nouvel onglet
      * Cadre parent
      * Cadre supérieur
   Appuyez ou cliquez sur la coche pour appliquer le lien ou le x à annuler.

* Dissocier

   ![](assets/chlimage_1-64.png)

   Utilisez cette option pour supprimer un lien déjà appliqué au texte sélectionné. Cette option est uniquement active lorsqu&#39;un lien est déjà sélectionné.

* Recherche

   ![](assets/chlimage_1-65.png)

   Utilisez cette option pour rechercher le texte des occurrences d&#39;une chaîne de texte spécifiée. Cette option permet d&#39;ouvrir une fenêtre pour définir les options de recherche.

   ![](assets/chlimage_1-66.png)

   Entrez le texte pour lequel vous souhaitez effectuer des recherches et appuyez ou cliquez sur **Rechercher** pour lancer la recherche. Appuyez ou cliquez sur le x pour annuler.

   Si vous souhaitez effectuer une correspondance exacte, sélectionnez l&#39;option **Correspondance avec la casse** avant de lancer la recherche.

   Si une correspondance est trouvée, elle est mise en surbrillance et le dialogue de recherche est grisé. Appuyez ou cliquez à nouveau sur le **bouton Rechercher** dans le dialogue grisé pour rechercher l&#39;occurrence suivante.

   ![](assets/chlimage_1-67.png)

   Si aucune occurrence supplémentaire n&#39;est trouvée, un message s&#39;affiche et la recherche redémarre à partir du début du texte.

   ![](assets/chlimage_1-68.png)

* Remplacer

   ![](assets/chlimage_1-69.png)

   Utilisez cette option pour rechercher dans le texte des occurrences d&#39;une chaîne de texte spécifiée et remplacer les correspondances par une autre chaîne. Cette option ouvre une fenêtre permettant de spécifier les options de recherche et de remplacement.

   ![](assets/chlimage_1-70.png)

   Entrez le texte à rechercher ainsi que le texte à remplacer.

   Appuyez ou cliquez **sur Rechercher** pour lancer la recherche. Cliquez ou appuyez sur le x pour annuler.

   Si vous souhaitez effectuer une correspondance exacte, sélectionnez l&#39;option **Correspondance avec la casse** avant de lancer la recherche.

   Si une correspondance est trouvée, elle est mise en surbrillance et le dialogue de recherche est grisé. Cliquez à nouveau sur le **bouton Rechercher** dans le dialogue grisé pour rechercher l&#39;occurrence suivante ou sélectionner le bouton **Remplacer** pour remplacer le texte mis en surbrillance. Notez que le bouton **Remplacer** n&#39;est actif qu&#39;une fois qu&#39;une correspondance est trouvée.

   Sélectionnez **Remplacer tout** pour remplacer toutes les occurrences du texte à la fois.

* Aligner le texte à gauche

   ![](assets/chlimage_1-71.png)

   Utilisé pour aligner le texte sur la marge gauche.

* Texte centré

   ![](assets/chlimage_1-72.png)

   Utilisé pour centrer le texte.

* Aligner le texte à droite

   ![](assets/chlimage_1-73.png)

   Utilisé pour aligner le texte sur la marge droite.

* Puce

   ![](assets/chlimage_1-74.png)

   Utilisé pour formater le texte sélectionné sous forme d&#39;une liste à puces ou commencer l&#39;insertion d&#39;une liste à puces après le curseur.

   Pour mettre fin à une liste à puces, appuyez ou cliquez de nouveau sur le **bouton Puces** ou saisissez deux retours chariot.

* Numérotée

   ![](assets/chlimage_1-75.png)

   Utilisé pour mettre en forme le texte sélectionné sous forme de liste numérotée ou commencer l&#39;insertion d&#39;une liste numérotée après le curseur.

   Pour mettre fin à une liste numérotée, appuyez ou cliquez de nouveau sur le **bouton Numéroté** ou saisissez deux retours chariot.

* Retrait négatif

   ![](assets/chlimage_1-76.png)

   Utilisé pour diminuer le niveau de retrait du texte ou du texte sélectionné après le curseur.

   Uniquement actif si le texte ou la position sélectionné du curseur est déjà mis en retrait.

* Retrait

   ![](assets/chlimage_1-77.png)

   Utilisé pour augmenter le niveau de retrait du texte ou du texte sélectionné après le curseur.

* Tableau

   ![](assets/chlimage_1-78.png)

   Utilisé pour insérer un tableau dans le texte. Cette option permet d&#39;ouvrir une fenêtre pour indiquer les détails du tableau.

   ![](assets/chlimage_1-79.png)

   * **Colonnes** - Nombre de colonnes du tableau (obligatoire)
   * **Lignes** - Nombre de rangées du tableau (obligatoire)
   * **Largeur** - Largeur du tableau
   * **Hauteur** - Hauteur du tableau
   * **Marge intérieure** des cellules - Espace autour du contenu de la cellule
   * **Espacement des cellules** - Espacement entre les cellules
   * **Bordure** - Poids des lignes de bordure du tableau
   * If for the header of the table :

      * La première ligne doit être utilisée
      * La première colonne doit être utilisée
      * La première ligne et la première colonne doivent être utilisées
      * Ou aucun en-tête ne doit être utilisé.
   * **Légende** - Légende du tableau


* Vérifier l’orthographe

   ![](assets/chlimage_1-80.png)

   permet de vérifier l&#39;orthographe du contenu du texte. Les fautes de frappe possibles sont soulignées avec des lignes rouges rompues.

* Caractères spéciaux

   ![](assets/chlimage_1-81.png)

   Utilisé pour insérer des caractères spéciaux dans le texte. Cette option ouvre une fenêtre où les caractères disponibles sont affichés.

   ![](assets/chlimage_1-82.png)

   Appuyez ou cliquez sur le caractère souhaité pour l&#39;insérer dans le texte après le curseur. Plusieurs caractères peuvent être insérés. Appuyez ou cliquez sur le x pour fermer la fenêtre de sélection.

* Modification de la source

   ![](assets/chlimage_1-83.png)

   Utilisé pour afficher et modifier la source HTML du texte.

   Appuyez ou cliquez sur l&#39;icône **Modifier la** source pour modifier le contenu du texte à partir de la vue formatée pour afficher le code HTML brut. Dans ce mode, toutes les autres options de formatage sont désactivées. Appuyez ou cliquez de nouveau sur l&#39; **icône Modifier** la source pour revenir à la vue formatée.

   >[!CAUTION]
   >
   >Comme toujours le cas avec l&#39;accès au code HTML brut, vous devez veiller à utiliser l&#39;option **Source Edit** !
   >
   >
   >Le code HTML saisi via **la fonctionnalité Source Edit** est analysé pour les risques XSS et tous les scripts insérés sont supprimés et ne s&#39;affichent pas sur la page produite. Cependant, le code HTML mal formé saisi dans **la modification** source peut rompre le modèle de la page, ce qui entraîne une mise en forme inattendue ou un rendu inattendu de la page résultante.

* Format de paragraphe

   ![](assets/chlimage_1-84.png)

   Utilisé pour appliquer le formatage des paragraphes au texte sélectionné ou au texte inséré après le curseur. La sélection de cette option ouvre une liste déroulante à partir de laquelle le format de paragraphe est sélectionné.

   ![](assets/chlimage_1-85.png)

Le composant de texte peut également être modifié en ligne mais en raison des contraintes d&#39;espace, toutes les options de formatage ne sont pas disponibles en ligne. Pour afficher toutes les options, passez en mode plein écran.

![](assets/chlimage_1-86.png)

## Créer un dialogue {#design-dialog}

Le dialogue de conception permet à l&#39;auteur du modèle de définir quelles options de formatage de texte sont disponibles pour les auteurs de contenu.

### Fonctionnalités {#features}

![](assets/chlimage_1-28.png)

Les fonctionnalités suivantes peuvent être activées ou désactivées pour le composant.

* Coller du texte brut
* Passé du mot
* Rechercher et remplacer
* Vérificateur orthographique
* Modification source

### Formatage {#formatting}

![](assets/chlimage_1-29.png)

Les options de formatage suivantes peuvent être activées ou désactivées pour le composant.

* Tableau
* Listes
* Alignement
* Gras, italique, soulignement
* Liens
* Sous/exposant

### Styles de paragraphe {#paragraph-styles}

![](assets/chlimage_1-30.png)

Les styles de paragraphe peuvent être activés ou désactivés pour le composant. Lorsque cette option est activée, les formats autorisés peuvent être définis.

* Appuyez sur le bouton **Ajouter** ou cliquez dessus pour insérer un nouveau style.
* Entrez le code du style et une description qui s&#39;affichera dans la boîte de dialogue Modifier.
* Pour supprimer un style de style ou cliquez sur le **bouton Supprimer** .
* Pour réorganiser l&#39;ordre des formats, appuyez ou cliquez et faites glisser les poignées.

### Caractères spéciaux {#special-characters}

![](assets/chlimage_1-31.png)

L&#39;option permettant d&#39;insérer des caractères spéciaux peut être activée ou désactivée pour le composant. Lorsque cette option est activée, les caractères autorisés peuvent être définis.

* Appuyez sur le bouton **Ajouter** ou cliquez dessus pour insérer un nouveau caractère.
* Entrez le code HTML du caractère et une description qui s&#39;afficheront dans la boîte de dialogue Modifier.
* Pour supprimer un taquet de caractères ou cliquez sur le **bouton Supprimer** .
* Pour réorganiser l&#39;ordre des caractères, appuyez ou cliquez et faites glisser les poignées.

## Détails techniques {#technical-details}

Vous trouverez la documentation technique la plus récente sur le composant [de texte sur github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v1/text).

Le projet de composants principaux peut être téléchargé depuis github.

Vous trouverez plus d&#39;informations sur le développement des composants principaux dans la documentation destinée aux développeurs de composants [principaux](developing.md).
