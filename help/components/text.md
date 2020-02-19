---
title: Composant textuel
description: Le composant Texte est un composant d’édition et de composition de texte enrichi qui propose une édition statique.
translation-type: tm+mt
source-git-commit: fe8a121520000ffd56ae3347469590e89121eaf0

---


# Composant textuel{#text-component}

Le composant Texte des composants principaux est un composant d’édition et de composition de texte enrichi qui propose une édition statique.

## Utilisation {#usage}

Le composant Texte propose un puissant éditeur de texte enrichi qui permet d’apporter facilement des modifications de texte dans un éditeur en ligne simplifié, ainsi qu’un format plein écran.

La [boîte de dialogue de modification](#edit-dialog) permet de modifier en ligne les options limitées avec des fonctionnalités complètes disponibles dans la boîte de dialogue de modification en plein écran. À l’aide de la [boîte de dialogue de conception](#design-dialog), les options de mise en forme de texte telles que les en-têtes, les caractères spéciaux et les styles de paragraphe peuvent être configurées pour le modèle de l’auteur du contenu.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de texte est v2, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018 et est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.3 | AEM 6.4 | AEM 6.5 |  d’AEM en tant que Cloud Service |
|---|---|---|---|---|
| v2 | Compatible | Compatible | Compatible | Compatible |
| [v1](v1/text-v1.md) | Compatible | Compatible | Compatible | - |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant de texte, des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [Bibliothèque de  composants](https://adobe.com/go/aem_cmp_library_text).

### Détails techniques {#technical-details}

The latest technical documentation about the Text Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_text_v2).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Composant Texte et Éditeur de texte enrichi {#the-text-component-and-the-rich-text-editor}

Le composant principal Texte tire parti de l’éditeur de texte enrichi AEM (RTE). L’éditeur de texte enrichi met à la disposition des auteurs de nombreuses fonctionnalités pour modifier leur contenu textuel. L’éditeur de texte enrichi est très flexible dans sa configuration et offre plusieurs options. Further details about how the RTE can be configured can be found in the articles [Configure the Rich Text Editor](https://docs.adobe.com/content/help/en/experience-manager-65/administering/operations/rich-text-editor.html) and [Configure the Rich Text Editor plug-ins](https://docs.adobe.com/content/help/en/experience-manager-65/administering/operations/configure-rich-text-editor-plug-ins.html).

Le reste de cet article illustre la configuration standard du composant principal Texte avec la configuration prête à l’emploi de l’éditeur de texte enrichi.

>[!NOTE]
>
>Only options enabled by [UI configurations of the RTE](https://docs.adobe.com/content/help/en/experience-manager-65/administering/operations/configure-rich-text-editor-plug-ins.html) are available by in the Text Component.

## Boîte de dialogue de modification {#edit-dialog}

La boîte de dialogue de modification propose les outils standard de mise en forme de texte enrichi qu’un utilisateur devrait utiliser pour composer du texte.

![](/help/assets/screen_shot_2018-01-11at143025.png)

### Gras

![](/help/assets/screen_shot_2018-01-11at125602.png)

Utilisé pour appliquer une mise en forme gras au texte sélectionné ou au texte gras saisi après le curseur.

**Ctrl + B** peut être utilisé comme raccourci clavier.

### Italique

![](/help/assets/screen_shot_2018-01-11at125609.png)

Utilisé pour appliquer une mise en forme en italique au texte sélectionné ou mettre en italique le texte saisi après le curseur.

**Ctrl + I** peut être utilisé comme raccourci clavier.

### Souligné

![](/help/assets/screen_shot_2018-01-11at125615.png)

Utilisé pour appliquer une mise en forme soulignée au texte ou au texte souligné sélectionné après le curseur.

**Ctrl + U** peut être utilisé comme raccourci clavier.

### Indice

![](/help/assets/screen_shot_2018-01-11at125703.png)

Utilisé pour mettre en forme le texte ou le texte sélectionné après le curseur comme indice.

### Exposant

![](/help/assets/screen_shot_2018-01-11at125708.png)

Utilisé pour mettre en forme le texte ou le texte sélectionné après le curseur comme exposant.

### Coller en tant que texte

![](/help/assets/screen_shot_2018-01-11at125713.png)

Colle le texte copié en tant que texte brut sans mise en forme.

Lorsque vous sélectionnez cette option, une fenêtre s’ouvre où le texte peut être collé en tant que texte brut sans formatage en tant qu’aperçu avant d’être inséré dans le texte. Acceptez en appuyant ou en cliquant sur la coche, annulez en appuyant ou en cliquant sur le x.

![](/help/assets/screen_shot_2018-01-11at143234.png)

### Coller à partir de Word

![](/help/assets/screen_shot_2018-01-11at125717.png)

Lorsque vous sélectionnez cette option, une fenêtre s’ouvre où le texte peut être collé, en conservant sa mise en forme en tant qu’aperçu avant de l’insérer dans le texte. Acceptez en appuyant ou en cliquant sur la coche, annulez en appuyant ou en cliquant sur le x.

![](/help/assets/screen_shot_2018-01-11at143250.png)

### Lien hypertexte

![](/help/assets/screen_shot_2018-01-11at125839.png)

Utilisez cette option pour convertir le texte sélectionné en hyperlien ou modifier un lien déjà défini. Cette option est uniquement active lorsque le texte est déjà sélectionné et ouvre une fenêtre avec des options supplémentaires pour définir le lien.

![](/help/assets/screen_shot_2018-01-11at130003.png)

* Saisissez l’emplacement.
   * Utilisation de la boîte de dialogue Ouvrir la sélection pour choisir un chemin dans AEM
   * Si le lien ne figure pas dans AEM, saisissez l’URL absolue (les chemins non absolus sont interprétés comme relatifs par rapport à AEM).
* Saisissez un autre texte descriptif pour le lien.
* Sélectionner le comportement des liens
   * Cible
   * Même onglet
   * Nouvel onglet
   * Cadre parent
   * Cadre supérieur
   Appuyez ou cliquez sur la coche pour appliquer le lien ou sur le x pour annuler.

### Dissocier

![](/help/assets/screen_shot_2018-01-11at125901.png)

Utilisez cette option pour supprimer un lien déjà appliqué au texte sélectionné. Cette option est uniquement active lorsqu’un lien est déjà sélectionné.

### Rechercher

![](/help/assets/screen_shot_2018-01-11at125906.png)

Utilisez cette option pour rechercher le texte d’occurrence d’une chaîne de texte spécifiée. Cette option permet d’ouvrir une fenêtre pour définir les options de recherche.

![](/help/assets/screen_shot_2018-01-11at130107.png)

Entrez le texte pour lequel vous souhaitez effectuer des recherches et appuyez ou cliquez sur **Rechercher** pour lancer la recherche. Appuyez ou cliquez sur le x pour annuler.
Si vous souhaitez effectuer une correspondance exacte, sélectionnez l’option **Correspondance avec la casse** avant de lancer la recherche.
Si une correspondance est trouvée, elle est mise en surbrillance et le dialogue de recherche est grisé. Appuyez ou cliquez à nouveau sur le bouton **Rechercher** dans la boîte de dialogue grisée pour rechercher l’occurrence suivante.

![](/help/assets/screen_shot_2018-01-11at130145.png)

Si aucune occurrence supplémentaire n’est trouvée, un message s’affiche et la recherche redémarre à partir du début du texte.

![](/help/assets/screen_shot_2018-01-11at130241.png)

### Remplacer

![](/help/assets/screen_shot_2018-01-11at125910.png)

Utilisez cette option pour rechercher dans le texte des occurrences d’une chaîne de texte spécifiée et remplacer les correspondances par une autre chaîne. Cette option ouvre une fenêtre permettant de spécifier les options de recherche et de remplacement.

![](/help/assets/screen_shot_2018-01-11at130441.png)

Entrez le texte à rechercher ainsi que le texte avec lequel le remplacer.

Appuyez ou cliquez sur **Rechercher** pour lancer la recherche. Cliquez ou appuyez sur le x pour annuler.

Si vous souhaitez effectuer une correspondance exacte, sélectionnez l’option **Correspondance avec la casse** avant de lancer la recherche.

Si une correspondance est trouvée, elle est mise en surbrillance et le dialogue de recherche est grisé. Cliquez à nouveau sur le bouton **Rechercher** dans la boîte de dialogue grisée pour rechercher l’occurrence suivante ou sélectionner le bouton **Remplacer** pour remplacer le texte mis en surbrillance. Notez que le bouton **Remplacer** n’est actif qu’une fois qu’une correspondance est trouvée.

Sélectionnez **Remplacer tout** pour remplacer toutes les occurrences du texte à la fois.

### Aligner le texte à gauche

![](/help/assets/screen_shot_2018-01-11at142012.png)

Utilisé pour aligner le texte sur la marge gauche.

### Texte centré

![](/help/assets/screen_shot_2018-01-11at142017.png)

Utilisé pour centrer le texte.

### Aligner le texte à droite

![](/help/assets/screen_shot_2018-01-11at142021.png)

Utilisé pour aligner le texte sur la marge droite.

### Puce

![](/help/assets/screen_shot_2018-01-11at142025.png)

Utilisé pour formater le texte sélectionné sous forme d’une liste à puces ou commencer l’insertion d’une liste à puces après le curseur.

Pour mettre fin à une liste à puces, appuyez ou cliquez de nouveau sur le bouton **Puces** ou saisissez deux retours chariot.

### Numérotée

![](/help/assets/screen_shot_2018-01-11at142030.png)

Utilisé pour mettre en forme le texte sélectionné sous forme de liste numérotée ou commencer l’insertion d&#39;une liste numérotée après le curseur.

Pour mettre fin à une liste numérotée, appuyez ou cliquez de nouveau sur le bouton **Numérotée** ou saisissez deux retours chariot.

### Retrait négatif

![](/help/assets/screen_shot_2018-01-11at141917.png)

Utilisé pour diminuer le niveau de mise en retrait du texte sélectionné ou du texte entré après le curseur.

Uniquement actif si le texte ou la position sélectionnés du curseur est déjà mis en retrait.

### Retrait

![](/help/assets/screen_shot_2018-01-11at141922.png)

Utilisé pour augmenter le niveau de mise en retrait du texte ou du texte sélectionnés après le curseur.

### Tableau

![](/help/assets/screen_shot_2018-01-11at141928.png)

Utilisé pour insérer un tableau dans le texte. Cette option permet d’ouvrir une fenêtre pour indiquer les détails du tableau.

![](/help/assets/screen_shot_2018-01-11at142405.png)

* **Colonnes**
Le nombre de colonnes du tableau (obligatoire).
* **Lignes**
Le nombre de lignes du tableau (obligatoire).
* **Largeur**
Largeur totale du tableau.
* **Hauteur**
Hauteur totale du tableau.
* **Marge intérieure de la cellule**
Espace autour du contenu de la cellule.
* **Espacement des cellules**
Espacement entre les cellules.
* **Bordure**
L’épaisseur des lignes de bordure du tableau.
* Si pour l’en-tête du tableau :
   * La première ligne doit être utilisée
   * La première colonne doit être utilisée
   * La première ligne et la première colonne doivent être utilisées
   * Ou aucun en-tête ne doit être utilisé.
* **Légende**
La légende du tableau.

### Vérifier l’orthographe

![](/help/assets/screen_shot_2018-01-11at141935.png)

Permet de vérifier l’orthographe du contenu du texte. Les fautes de frappe possibles sont soulignées avec des lignes rouges rompues.

Further details about spell checking and customizing spell check dictionaries can be found in the document [Configure the Rich Text Editor Plug-Ins](https://docs.adobe.com/content/help/en/experience-manager-65/administering/operations/configure-rich-text-editor-plug-ins.html).

### Caractères spéciaux {#special-characters}

![](/help/assets/screen_shot_2018-01-11at142600.png)

Utilisé pour insérer des caractères spéciaux dans le texte. Cette option ouvre une fenêtre où les caractères disponibles sont affichés.

![](/help/assets/screen_shot_2018-01-11at142635.png)

Appuyez ou cliquez sur le caractère souhaité pour l’insérer dans le texte après le curseur. Plusieurs caractères peuvent être insérés. Appuyez ou cliquez sur le x pour fermer la fenêtre de sélection.

### Modification de la source

![](/help/assets/screen_shot_2018-01-11at142746.png)

Utilisé pour afficher et modifier la source HTML du texte.

Appuyez ou cliquez sur l’icône **Modifier la source** pour modifier le contenu du texte à partir de la vue formatée pour afficher le code HTML brut. Dans ce mode, toutes les autres options de formatage sont désactivées. Appuyez ou cliquez de nouveau sur l’icône **Modifier la source** pour revenir à la vue formatée.

>[!CAUTION]
>
>Comme c’est toujours le cas avec l’accès au code HTML brut, vous devez faire preuve de prudence lors de l’utilisation de l’option **Modifier la source**.
>
>Le code HTML saisi via l’option **Modifier la source** est analysé pour les risques XSS et tous les scripts insérés sont supprimés et ne s’affichent pas sur la page produite. Cependant, le code HTML mal formé saisi dans **Modifier la source** peut casser le modèle de la page, ce qui entraîne une mise en forme inattendue ou un rendu inutilisable de la page obtenue.

>[!NOTE]
>
>Étant donné que le code HTML saisi via l’option **Modifier la source** est analysé pour les risques XSS et les scripts et les supprime automatiquement, le contenu persistant persistant peut différer de celui saisi dans **Modifier la source**. Pour cette raison, pour enregistrer les modifications effectuées à l’aide de l’option **Modifier la source**, vous devez d’abord quitter **Modifier la source** pour afficher le texte dans l’éditeur normal avant l’enregistrement.

### Format de paragraphe

![](/help/assets/screen_shot_2018-01-11at142752.png)

Utilisé pour appliquer le formatage des paragraphes au texte sélectionné ou au texte inséré après le curseur. La sélection de cette option ouvre une liste déroulante à partir de laquelle le format de paragraphe est sélectionné.

![](/help/assets/screen_shot_2018-01-11at142828.png)

Le composant de texte peut également être modifié en ligne mais en raison des contraintes d’espace, toutes les options de formatage ne sont pas disponibles en ligne. Pour afficher toutes les options, passez en mode plein écran.

![](/help/assets/screen_shot_2018-01-11at142921.png)

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir quelles options de formatage de texte sont disponibles pour les auteurs de contenu.

### Onglet Plugins {#plugins-tab}

L’onglet Plugins permet d’activer et de désactiver diverses options de formatage de texte disponibles pour les auteurs de contenu.

### Fonctionnalités {#features}

![](/help/assets/chlimage_1-28.png)

Les fonctionnalités suivantes peuvent être activées ou désactivées pour le composant.

* Coller du texte brut
* Coller à partir de Word
* Rechercher et remplacer
* Vérificateur orthographique
* Modification de la source

### Formatage {#formatting}

![](/help/assets/chlimage_1-29.png)

Les options de formatage suivantes peuvent être activées ou désactivées pour le composant.

* Tableau
* Listes
* Alignement
* Gras, italique, souligné
* Liens
* Indice/exposant

### Styles de paragraphe {#paragraph-styles}

![](/help/assets/chlimage_1-30.png)

Les styles de paragraphe peuvent être activés ou désactivés pour le composant. Lorsque cette option est activée, les formats autorisés peuvent être définis.

* Appuyez ou cliquez sur le bouton **Ajouter** pour insérer un nouveau style.
* Entrez le code du style et une description qui s’affichera dans la boîte de dialogue de modification.
* Pour supprimer un style, appuyez ou cliquez sur le bouton **Supprimer**.
* Pour réorganiser l’ordre des formats, appuyez ou cliquez et faites glisser les poignées.

### Configuration des caractères spéciaux {#configuring-special-characters}

![](/help/assets/chlimage_1-31.png)

L’option permettant d’insérer des caractères spéciaux peut être activée ou désactivée pour le composant. Lorsque cette option est activée, les caractères autorisés peuvent être définis.

* Appuyez ou cliquez sur le bouton **Ajouter** pour insérer un nouveau caractère.
* Entrez le code HTML du caractère et une description qui s’afficheront dans la boîte de dialogue de modification.
* Pour supprimer un caractère, appuyez ou cliquez sur le bouton **Supprimer**.
* Pour réorganiser l’ordre des caractères, appuyez ou cliquez et faites glisser les poignées.

## Onglet Styles {#styles-tab}

Le composant Texte prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.