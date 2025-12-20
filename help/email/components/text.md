---
title: Composant Texte d’e-mail
description: Le composant Texte d’e-mail est un composant d’édition et de composition de texte enrichi qui propose une édition statique.
role: Architect, Developer, Admin, User
exl-id: 4aa192f6-8314-40e7-8732-c6626d647986
index: false
source-git-commit: eb77567dc32cccb81a9fc131493d11fb55b7e93b
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Composant Texte d’e-mail {#email-text-component}

Le composant Texte d’e-mail est un composant d’édition et de composition de texte enrichi qui propose une édition statique.

## Utilisation {#usage}

Le composant Texte d’e-mail propose un puissant éditeur de texte enrichi qui permet d’apporter facilement des modifications de texte dans un éditeur en ligne simplifié, ainsi qu’un format plein écran.

* La [boîte de dialogue de modification](#edit-dialog) permet de modifier en ligne les options limitées avec des fonctionnalités complètes disponibles dans la boîte de dialogue de modification en plein écran.
* À l’aide de la [boîte de dialogue de conception](#design-dialog), les options de formatage de texte telles que les en-têtes, les caractères spéciaux et les styles de paragraphe peuvent être configurées pour le modèle de l’auteur de contenu.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Texte d’e-mail est v1. Celle-ci a été introduite avec la version X des composants principaux d’e-mail en octobre 2022. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatible | - | - |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux d’e-mail.](/help/email/versions.md)

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Texte d’e-mail [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_email_text_v1_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Composant Texte d’e-mail et Éditeur de texte enrichi {#the-text-component-and-the-rich-text-editor}

Le composant Texte d’e-mail tire parti de l’éditeur de texte enrichi (RTE) AEM. L’éditeur de texte enrichi met à la disposition des auteurs de nombreuses fonctionnalités pour modifier leur contenu textuel. L’éditeur de texte enrichi est très flexible dans sa configuration et offre plusieurs options. Vous trouverez plus d’informations sur la configuration de l’éditeur de texte enrichi dans les articles [Configuration de l’éditeur de texte enrichi](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/rich-text-editor.html?lang=fr) et [Configuration des modules externes d’éditeur de texte enrichi](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html?lang=fr).

Le reste de ce document illustre la configuration standard du composant Texte d’e-mail avec la configuration prête à l’emploi de l’éditeur de texte enrichi.

>[!NOTE]
>
>Seules les options activées par les [configurations de l’interface utilisateur de l’éditeur de texte enrichi](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html?lang=fr) sont disponibles dans le composant Texte d’e-mail.

## Boîte de dialogue de modification {#edit-dialog}

![Boîte de dialogue de modification du composant Texte](/help/email/assets/email-text-edit.png)

### Options de formatage {#options}

La boîte de dialogue de modification propose les outils de formatage de texte standard et enrichis auxquels un utilisateur s’attend pour composer du texte.

#### Gras

![Icône Gras](/help/assets/text-bold.png)

Utilisé pour appliquer une mise en forme gras au texte sélectionné ou au texte gras saisi après le curseur.

**Ctrl + B** peut être utilisé comme raccourci clavier.

#### Italique

![Icône Italique](/help/assets/text-italic.png)

Utilisé pour appliquer une mise en forme en italique au texte sélectionné ou mettre en italique le texte saisi après le curseur.

**Ctrl + I** peut être utilisé comme raccourci clavier.

#### Souligné

![Icône Souligné](/help/assets/text-underline.png)

Utilisé pour appliquer une mise en forme soulignée au texte ou au texte souligné sélectionné après le curseur.

**Ctrl + U** peut être utilisé comme raccourci clavier.

#### Indice

![Icône Indice](/help/assets/text-subscript.png)

Utilisé pour mettre en forme le texte ou le texte sélectionné après le curseur comme indice.

#### Exposant

![Icône Exposant](/help/assets/text-superscript.png)

Utilisé pour mettre en forme le texte ou le texte sélectionné après le curseur comme exposant.

#### Coller en tant que texte

![Icône Coller en tant que texte](/help/assets/text-paste-text.png)

Colle le texte copié en tant que texte brut sans mise en forme.

Lorsque vous sélectionnez cette option, vous ouvrez une fenêtre dans laquelle vous pouvez coller le texte en tant que texte brut sans formatage, à titre d’aperçu avant de l’insérer dans le texte. Acceptez en appuyant ou en cliquant sur la coche, annulez en appuyant ou en cliquant sur le x.

![Exemple de collage en tant que texte](/help/assets/text-paste-text-example.png)

#### Coller à partir de Word

![Icône Coller à partir de Word](/help/assets/text-paste-word.png)

Lorsque vous sélectionnez cette option, vous ouvrez une fenêtre dans laquelle vous pouvez coller le texte tout en conservant sa mise en forme, à titre d’aperçu avant de l’insérer dans le texte. Acceptez en appuyant ou en cliquant sur la coche, annulez en appuyant ou en cliquant sur le x.

![Exemple de collage à partir de Word](/help/assets/text-paste-word-example.png)

#### Lien hypertexte

![Icône Hyperlien](/help/assets/text-hyperlink.png)

Utilisez cette option pour convertir le texte sélectionné en hyperlien ou modifier un lien déjà défini. Cette option ouvre une fenêtre offrant des options supplémentaires pour définir le lien.

![Exemple d’hyperlien](/help/assets/text-hyperlink-example.png)

* Entrez le chemin.
   * Utilisez la boîte de dialogue **Ouvrir la sélection** pour choisir un chemin dans AEM.
   * Si le lien ne se trouve pas dans AEM, saisissez l’URL absolue.
      * Les chemins non absolus sont interprétés comme relatifs à AEM.
* Saisissez un autre texte descriptif pour le lien.
* Sélectionner le comportement des liens
   * Cible
   * Même onglet
   * Nouvel onglet
   * Cadre parent
   * Cadre supérieur

Appuyez ou cliquez sur la coche pour appliquer le lien ou sur le x pour annuler.

#### Dissocier

![Icône Dissocier](/help/assets/text-unlink.png)

Utilisez cette option pour supprimer un lien déjà appliqué au texte sélectionné. Cette option est uniquement active lorsqu’un lien est déjà sélectionné.

#### Ancrer {#anchor}

![Icône d’ancrage](/help/email/assets/anchor.png)

Utilisez cette option pour insérer une ancre dans le texte.

#### Rechercher

![Icône Rechercher](/help/assets/text-find.png)

Utilisez cette option pour rechercher le texte d’occurrence d’une chaîne de texte spécifiée. Cette option permet d’ouvrir une fenêtre pour définir les options de recherche.

![Exemple de recherche](/help/assets/text-find-example.png)

Entrez le texte pour lequel vous souhaitez effectuer des recherches et appuyez ou cliquez sur **Rechercher** pour lancer la recherche. Appuyez ou cliquez sur le x pour annuler.
Si vous souhaitez effectuer une correspondance exacte, sélectionnez l’option **Respecter la casse** avant de lancer la recherche.
Si une correspondance est trouvée, elle est mise en surbrillance et le dialogue de recherche est grisé. Appuyez ou cliquez à nouveau sur le bouton **Rechercher** dans la boîte de dialogue grisée pour rechercher l’occurrence suivante.

![Exemple de recherche fructueuse](/help/assets/text-find-example-found.png)

Si aucune occurrence supplémentaire n’est trouvée, un message s’affiche et la recherche redémarre à partir du début du texte.

![Exemple de recherche sans occurrence restante](/help/assets/text-find-example-found-end.png)

#### Remplacer

![Icône Remplacer](/help/assets/text-replace.png)

Utilisez cette option pour rechercher dans le texte des occurrences d’une chaîne de texte spécifiée et remplacer les correspondances par une autre chaîne. Cette option ouvre une fenêtre permettant de spécifier les options de recherche et de remplacement.

![Exemple de remplacement](/help/assets/text-replace-example.png)

Entrez le texte à rechercher ainsi que le texte avec lequel le remplacer.

* Appuyez ou cliquez sur **Rechercher** pour lancer la recherche. Cliquez ou appuyez sur le x pour annuler.
* Si vous souhaitez effectuer une correspondance exacte, sélectionnez l’option **Respecter la casse** avant de lancer la recherche.
* Sélectionnez **Tout remplacer** pour remplacer toutes les occurrences du texte à la fois.

Si une correspondance est trouvée, elle est mise en surbrillance et le dialogue de recherche est grisé. Cliquez à nouveau sur le bouton **Rechercher** dans la boîte de dialogue grisée pour rechercher l’occurrence suivante ou sélectionner le bouton **Remplacer** pour remplacer le texte mis en surbrillance. Notez que le bouton **Remplacer** n’est actif que lorsqu’une correspondance est trouvée.

La boîte de dialogue de recherche et de remplacement devient transparente lorsque l’utilisateur clique sur Rechercher et devient opaque lorsque l’utilisateur clique sur Remplacer. Cela permet à l’auteur de vérifier le texte qui sera remplacé.

>[!NOTE]
>
>Lors de l’utilisation de la fonctionnalité de remplacement, la chaîne à remplacer doit être saisie en même temps que la chaîne à trouver. Cependant, vous pouvez toujours cliquer sur Rechercher pour rechercher la chaîne avant de la remplacer. Si la chaîne de remplacement est saisie après avoir cliqué sur Rechercher, la recherche est réinitialisée au début du texte.

#### Annuler

![Icône Annuler](/help/email/assets/undo.png)

Permet d’annuler la dernière modification dans l’éditeur de texte enrichi.

#### Rétablir

![Icône Rétablir](/help/email/assets/redo.png)

Permet d’annuler une modification annulée à l’aide de l’icône Annuler.

#### Aligner le texte à gauche

![Icône Aligner à gauche](/help/assets/text-left.png)

Utilisé pour aligner le texte sur la marge gauche.

#### Texte centré

![Icône Texte centré](/help/assets/text-center.png)

Utilisé pour centrer le texte.

#### Aligner le texte à droite

![Icône Aligner à droite](/help/assets/text-right.png)

Utilisé pour aligner le texte sur la marge droite.

#### Puce

![Icône Puce](/help/assets/text-bullet.png)

Utilisé pour formater le texte sélectionné sous forme d’une liste à puces ou commencer l’insertion d’une liste à puces après le curseur.

Pour mettre fin à une liste à puces, appuyez ou cliquez de nouveau sur le bouton **Puces** ou saisissez deux retours chariot.

#### Numérotée

![Icône Liste numérotée](/help/assets/text-numbered.png)

Utilisé pour mettre en forme le texte sélectionné sous forme de liste numérotée ou commencer l’insertion d’une liste numérotée après le curseur.

Pour mettre fin à une liste numérotée, appuyez ou cliquez de nouveau sur le bouton **Numérotée** ou saisissez deux retours chariot.

#### Retrait négatif

![Icône Retrait négatif](/help/assets/text-outdent.png)

Utilisé pour diminuer le niveau de mise en retrait du texte sélectionné ou du texte entré après le curseur.

Uniquement actif si le texte ou la position sélectionnés du curseur est déjà mis en retrait.

#### Retrait

![Icône Retrait](/help/assets/text-indent.png)

Utilisé pour augmenter le niveau de mise en retrait du texte ou du texte sélectionnés après le curseur.

#### Tableau

![Icône Tableau](/help/assets/text-table.png)

Utilisé pour insérer un tableau dans le texte. Cette option permet d’ouvrir une fenêtre pour indiquer les détails du tableau.

![Exemple de tableau](/help/assets/text-table-example.png)

* **Colonnes** : Nombre de colonnes du tableau (obligatoire).
* **Lignes** : Nombre de lignes du tableau (obligatoire).
* **Largeur** : Largeur totale du tableau.
* **Hauteur** : Hauteur totale du tableau.
* **Marge intérieure des cellules** : espace autour du contenu de la cellule.
* **Espacement des cellules** : Espacement entre les cellules.
* **Bordure** : Épaisseur des lignes de bordure du tableau.
   * Si pour l’en-tête du tableau :
      * La première ligne doit être utilisée
      * La première colonne doit être utilisée
      * La première ligne et la première colonne doivent être utilisées
      * Ou aucun en-tête ne doit être utilisé
* **Légende** : Légende du tableau.

#### Image

![Icône Image](/help/email/assets/image-icon.png)

Utilisé pour aligner une image insérée.

#### Vérifier l’orthographe

![Icône Vérifier l’orthographe](/help/assets/text-spellcheck.png)

Permet de vérifier l’orthographe du contenu du texte. Les fautes de frappe possibles sont soulignées avec des lignes rouges rompues.

Vous trouverez plus d’informations sur la vérification orthographique et la personnalisation des dictionnaires orthographiques dans le document [Configuration des modules de l’éditeur de texte enrichi](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html?lang=fr).

#### Caractères spéciaux {#special-characters}

![Icône Caractères spéciaux](/help/assets/text-special-characters.png)

Utilisé pour insérer des caractères spéciaux dans le texte. Cette option ouvre une fenêtre où les caractères disponibles sont affichés.

![Exemple de caractères spéciaux](/help/assets/text-special-characters-example.png)

Appuyez ou cliquez sur le caractère souhaité pour l’insérer dans le texte après le curseur. Plusieurs caractères peuvent être insérés. Appuyez ou cliquez sur le x pour fermer la fenêtre de sélection.

#### Modification de la source

![Icône Modification de la source](/help/assets/text-source.png)

Utilisé pour afficher et modifier la source HTML du texte.

Appuyez ou cliquez sur l’icône **Modifier la source** pour modifier le contenu du texte à partir de la vue formatée pour afficher le code HTML brut. Dans ce mode, toutes les autres options de formatage sont désactivées. Appuyez ou cliquez de nouveau sur l’icône **Modifier la source** pour revenir à la vue formatée.

>[!CAUTION]
>
>Comme c’est toujours le cas avec l’accès au code HTML brut, vous devez faire preuve de prudence lors de l’utilisation de l’option **Modifier la source**.
>
>Le code HTML saisi via l’option **Modifier la source** est analysé pour les risques XSS et tous les scripts insérés sont supprimés et ne s’affichent pas sur la page produite. Cependant, le code HTML mal formé saisi dans l’option **Modifier la source** peut casser le modèle de la page, ce qui entraîne une mise en forme inattendue ou un rendu inutilisable de la page obtenue.

>[!NOTE]
>
>Étant donné que le code HTML saisi via l’option **Modifier la source** est analysé pour les risques XSS et les scripts, et les supprime automatiquement, le contenu persistant peut différer de celui saisi dans **Modifier la source**. Pour cette raison, pour enregistrer les modifications effectuées à l’aide de l’option **Modifier la source**, vous devez d’abord quitter **Modifier la source** pour afficher le texte dans l’éditeur normal avant l’enregistrement.

#### Format de paragraphe

![Icône Format de paragraphe](/help/assets/text-paragraph.png)

Utilisé pour appliquer le formatage des paragraphes au texte sélectionné ou au texte inséré après le curseur. La sélection de cette option ouvre une liste déroulante à partir de laquelle le format de paragraphe est sélectionné.

![Exemple de format de paragraphe](/help/assets/text-paragraph-example.png)

#### Sélectionner la variable Adobe Campaign

![Icône Sélectionner la variable Adobe Campaign](/help/email/assets/select-adobe-campaign-variable-icon.png)

Ouvre la boîte de dialogue [Sélectionner la variable Adobe Campaign](/help/email/campaign-variables.md) pour insérer du contenu dynamique depuis Adobe Campaign.

### Modification en ligne {#in-line-editing}

Le composant de texte peut également être modifié en ligne. Pour modifier en ligne, sélectionnez le composant Texte d’e-mail sur la page de contenu.

![Sélectionner le composant Texte d’e-mail](/help/email/assets/email-text-select-component.png)

Ensuite, appuyez ou cliquez sur l’icône **Modifier** dans la barre d’outils qui apparaît au-dessus du composant. La barre d’outils se modifie pour afficher des options de formatage limitées (y compris l’accès à l’option **Sélectionner la variable Adobe Campaign**) et vous pouvez modifier le texte en ligne.

![Exemple de modification en ligne](/help/email/assets/email-text-edit-inline-example.png)

Appuyez ou cliquez sur la coche dans la barre d’outils pour enregistrer vos modifications ou sur le X pour ignorer.

En raison des contraintes d’espace, les options de formatage ne sont pas toutes disponibles en ligne. Pour afficher toutes les options, passez en mode plein écran.

### Définition d’un ID {#setting-id}

Cette option permet de contrôler l’identifiant unique du composant dans le HTM.

* Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
* Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
* La modification de l’ID peut avoir un impact sur CSS.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir quelles options de formatage de texte sont disponibles pour les auteurs de contenu.

### Onglet Modules externes {#plugins-tab}

L’onglet **Modules externes** permet d’activer et de désactiver diverses options de formatage de texte disponibles pour les auteurs de contenu.

### Fonctions {#features}

![Fonctionnalités de la boîte de dialogue de conception](/help/assets/text-design-features.png)

Les fonctionnalités suivantes peuvent être activées ou désactivées pour le composant.

* Coller du texte brut
* Coller à partir de Word
* Rechercher et remplacer
* Annuler et rétablir
* Vérificateur orthographique
* Options de modification des images insérées
* Modification de la source HTML

### Mise en forme {#formatting}

![Mise en forme de la boîte de dialogue de conception](/help/assets/text-design-formatting.png)

Les options de formatage suivantes peuvent être activées ou désactivées pour le composant.

* Tableau
* Listes (puce, numéro, retrait, retrait négatif)
* Alignement (gauche, droite, centré)
* Gras, italique, souligné
* Lien (et dissociation)
* Indice/exposant

### Styles de paragraphe {#paragraph-styles}

![Styles de paragraphe de la boîte de dialogue de conception](/help/assets/text-design-paragraph.png)

Les styles de paragraphe peuvent être activés ou désactivés pour le composant. Lorsque cette option est activée, les formats autorisés peuvent être définis.

* Appuyez ou cliquez sur le bouton **Ajouter** pour insérer un nouveau style.
* Entrez le code du style et une description qui s’affichera dans la boîte de dialogue de modification.
* Pour supprimer un style, appuyez ou cliquez sur le bouton **Supprimer**.
* Pour réorganiser l’ordre des formats, appuyez ou cliquez sur les poignées et faites-les glisser.

### Caractères spéciaux {#configuring-special-characters}

![Caractères spéciaux de la boîte de dialogue de conception](/help/assets/text-design-special-characters.png)

L’option permettant d’insérer des caractères spéciaux peut être activée ou désactivée pour le composant. Lorsque cette option est activée, les caractères autorisés peuvent être définis.

* Appuyez ou cliquez sur le bouton **Ajouter** pour insérer un nouveau caractère.
* Entrez le code HTML du caractère et une description qui s’afficheront dans la boîte de dialogue de modification.
* Pour supprimer un caractère, appuyez ou cliquez sur le bouton **Supprimer**.
* Pour réorganiser l’ordre des caractères, appuyez ou cliquez sur les poignées et faites-les glisser.

## Onglet Styles {#styles-tab}

Le composant Texte d’e-mail prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.
