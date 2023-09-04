---
title: Formulaire adaptatif - Accordéon
description: Utilisez l’accordéon pour organiser et simplifier un formulaire long ou complexe en le divisant en sections plus petites et plus faciles à gérer.
role: Architect, Developer, Admin, User
exl-id: 0ed38eee-fc22-4708-82eb-3fb1839b1ff2
source-git-commit: ad3e3bca5cb46f14e864e4704c90ac3b62779794
workflow-type: tm+mt
source-wordcount: '2088'
ht-degree: 99%

---

# Composant Accordéon {#accordion-component-adaptive-forms-core-component}

Le composant principal « Accordéon » permet aux utilisateurs et aux utilisatrices de créer des sections extensibles et réductibles dans un formulaire adaptatif. Il est souvent utilisé pour organiser et simplifier des formulaires longs ou complexes en les divisant en sections plus petites et plus faciles à gérer. Chaque section d’un accordéon est généralement représentée par un en-tête sur lequel l’utilisateur ou l’utilisatrice peut cliquer pour développer ou réduire le contenu correspondant. Le contenu peut être n’importe quel composant principal.

## Utilisation {#usage}

Il existe plusieurs raisons d’inclure un accordéon dans un formulaire adaptatif, notamment :

* **Gain de place** : un accordéon permet aux utilisateurs et aux utilisatrices de modifier la taille des sections d’un formulaire, et d’avoir besoijn de moins de place pour afficher tous les champs du formulaire en même temps.

* **Navigation** : un accordéon peut être utilisé pour créer une structure de navigation hiérarchique, ce qui facilite la recherche des champs de formulaire dont les utilisateurs et les utilisatrices ont besoin.

* **Expérience utilisateur** : l’accordéon peut être utilisé pour rendre le formulaire plus convivial en offrant une méthode claire et intuitive d’accès et de remplissage des champs de formulaire.

* **Formulaires longs** : l’accordéon est un composant idéal pour gérer les formulaires longs, car il permet aux utilisateurs et aux utilisatrices de se concentrer sur une section à la fois, plutôt que d’essayer de traiter de nombreuses informations en même temps.

Vous pouvez utiliser :

* La [boîte de dialogue de configuration](#configure-dialog) pour spécifier les propriétés du composant Accordéon.

* La [fenêtre contextuelle Sélectionner un panneau](#select-panel-popover) pour définir l’ordre des panneaux de l’accordéon. Cela permet au créateur ou à la créatrice d’organiser les panneaux dans l’ordre dans lequel ils doivent apparaître.

* Options permettant à un créateur ou à une créatrice de formulaires d’activer ou de désactiver certaines fonctions dans la [boîte de dialogue de conception](#design-dialog). Par exemple, un créateur ou une créatrice peut choisir de désactiver certains champs ou sections d’un formulaire. Ces options permettent au créateur ou à la créatrice de mieux contrôler la conception et les fonctionnalités du formulaire, ce qui facilite la création de formulaires adaptés aux besoins spécifiques de l’entreprise.

La boîte de dialogue de configuration, la fenêtre contextuelle de sélection et la boîte de dialogue de conception font toutes partie des composants principaux conçus pour faciliter la création des formulaires et fournir un moyen efficace de créer des formulaires complexes.

## Version et compatibilité {#version-and-compatibility}


Le composant principal « Accordéon » pour les formulaires adaptatifs a été publié en février 2023 dans le cadre de la version 2.0.4 des composants principaux. Voici un tableau présentant toutes les versions prises en charge, la compatibilité AEM et les liens vers la documentation correspondante :

|  |  |
|---|---|
| Version du composant | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatible avec la <br>[version 2.0.4](/help/versions.md) et les versions ultérieures | Compatible | Compatible |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/versions.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Retrouvez les informations les plus récentes sur le composant « Accordéon » dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/accordion/v1/accordion). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience d’accordéon pour les visiteurs et les visiteuses en utilisant la boîte de dialogue Configurer. Vous pouvez également définir facilement des éléments d’accordéon, des panneaux, un comportement et une apparence pour une expérience utilisateur fluide.

### Onglet De base {#basic-tab}

![Onglet De base](/help/adaptive-forms/assets/acc-basic.png)

* **Nom** - Vous pouvez identifier facilement un composant de formulaire en lui attribuant un nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

* **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

* **Masquer le titre** - Sélectionnez cette option pour masquer le titre du composant.

* **Associer les données des composants enfants lors de l’envoi du formulaire (encapsuler les données dans l’objet)** : lorsque l’option est sélectionnée, les données de ses composants enfants sont imbriquées dans l’objet JSON du composant parent. Cependant, si l’option n’est pas sélectionnée, les données JSON envoyées ont une structure plate, sans objet pour le composant parent. Par exemple :

   * Lorsque cette option est sélectionnée, les données des composants enfants (par exemple, Rue, Ville et Code postal) sont imbriquées dans le composant parent (Adresse) sous la forme d’un objet JSON. Cela crée une structure hiérarchique et les données sont organisées sous le composant parent.

     Structure des données envoyées :

     ```JSON
     { "Address":
     
     { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     
     }
     ```

   * Lorsque l’option n’est pas sélectionnée, les données JSON envoyées ont une structure plate sans objet pour le composant parent (Adresse). Toutes les données se trouvent au même niveau, sans organisation hiérarchique.


     Structure des données envoyées :

     ```JSON
        { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     ```

* **Disposition** - Vous pouvez utiliser une disposition fixe (simple) ou une disposition flexible (grille réactive) pour votre assistant. La disposition simple conserve tout ce qui est fixe, tandis que la grille réactive vous permet d’ajuster la position des composants en fonction de vos besoins. Par exemple, utilisez la grille réactive pour aligner « Prénom », « Deuxième prénom » et « Nom » dans un formulaire sur une seule ligne.

* **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.

* **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.

* **Désactiver le composant** - Sélectionnez cette option pour désactiver le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

### Répéter l’accordéon {#repeat-accordion}

![repeat-accordion](/help/adaptive-forms/assets/repeat-accordion.png)

Vous pouvez utiliser les options de répétition pour dupliquer les panneaux d’accordéon et ses composants enfants, définir un nombre de répétitions minimal et maximal et faciliter la réplication de sections similaires dans un formulaire. Lors de l’interaction avec le composant Accordéon et de l’accès à ses paramètres, les options suivantes s’affichent :

* **Rendre l’accordéon répétable** : fonctionnalité de basculement qui permet aux utilisateurs et utilisatrices d’activer ou de désactiver la fonctionnalité de répétabilité.
* **Nombre minimal de répétitions** : définit le nombre minimal de répétitions possibles du panneau d’accordéon. La valeur zéro indique que le panneau d’accordéon n’est pas répété. La valeur par défaut est zéro.
* **Nombre maximal de répétitions** : définit le nombre maximal de répétitions possibles du panneau d’accordéon. Par défaut, cette valeur est illimitée.

Pour gérer efficacement les sections répétables dans l’accordéon, procédez comme indiqué dans l’article [Création de formulaires avec des sections répétables](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html?lang=fr).

### Onglet Éléments {#items-tab}

![Onglet Éléments](/help/adaptive-forms/assets/acc-items.png)

Le bouton Ajouter vous permet de sélectionner un composant à ajouter sous forme de panneau à partir de la fenêtre de sélection des composants. Après avoir ajouté le composant, vous pouvez voir les options suivantes :

* **Icône** : L’icône identifie le composant du panneau dans la liste. Pointez sur l’icône pour afficher le nom complet du composant sous forme d’info-bulle.
* **Description** : Description utilisée comme texte du panneau. Par défaut, le nom du composant est sélectionné pour le panneau.
* **Supprimer** : Appuyez ou cliquez sur cette option pour supprimer le panneau du composant d’accordéon.
* **Réorganiser** : Appuyez ou cliquez et faites glisser pour réorganiser l’ordre des panneaux.

### Onglet Contenu de l’aide {#help-content}

![Onglet Contenu d’aide](/help/adaptive-forms/assets/acc-helpcontent.png)

* **Description courte** : Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez l’option **Toujours afficher une description courte** pour l’afficher sous le composant.

* **Toujours afficher une description courte** - Activez cette option pour afficher la description courte sous le composant.

* **Texte d’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility}

![Onglet Accessibilité](/help/adaptive-forms/assets/acc-accessisbilty.png)

Dans l’onglet **Accessibilité**, les valeurs peuvent être définies pour les libellés d’[accessibilité ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) du composant. Plusieurs options sont disponibles pour l’utilisation du texte pour le lecteur d’écran :

* **Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.


   * **Texte personnalisé** : sélectionnez cette option pour utiliser le texte personnalisé pour les libellés d’accessibilité ARIA. Cette option affiche la boîte de dialogue Texte personnalisé. Vous pouvez ajouter des informations pertinentes dans la boîte de dialogue Texte personnalisé.
   * **Description** : sélectionnez cette option pour utiliser la description des libellés d’accessibilité ARIA.
   * **Titre** : sélectionnez cette option pour utiliser le titre pour les libellés d’accessibilité ARIA.
   * **Nom** : sélectionnez cette option pour utiliser le nom pour les libellés d’accessibilité ARIA.
   * **Aucun** : sélectionnez cette option si vous ne souhaitez pas l’ajouter pour les libellés d’accessibilité ARIA.

<!--

### Properties Tab {#properties-tab}

![Properties tab of the edit dialog of the Accordion Component](/help/assets/accordion-edit-properties.png)

*   **Single item expansion** - When selected, this option forces a single accordion item to be expanded at a time. Expanding one item will then collapse all others.
*   **Expanded items** - This option defines the items that are expanded by default when the page is loaded.
    * When **Single item expansion** is selected, one panel must be selected. By default the first panel is selected.
    * When **Single item expansion** is not selected, this option is a multi-select and is optional.
*   **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
    * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
    * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
    * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

## Select Panel Popover {#select-panel-popover}

The **Select Panel** option (![Select panel icon](/help/assets/select-panel-icon.png)) on the component toolbar enables content authors to modify the panels in an accordion with ease. By selecting this option, the author can switch to a different panel for editing and rearrange the order of the panels in the accordion. The configured panels will be displayed in a drop-down menu for the author to choose from. This feature optimizes the editing process and makes it user-friendly for content authors.

![Select panel popover](/help/assets/select-panel-popover.png)


* The panels are displayed in a numbered list, reflecting the assigned arrangement.
* Each panel is listed with its component type in bold, followed by a brief description in lighter font.
* By clicking or tapping on a panel in the drop-down, you can easily switch the view in the editor to that specific panel.
* To rearrange the panels, simply use the drag handles to move them into the desired order. -->

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue Conception permet aux créateurs et aux créatrices de modèles de contrôler l’affichage des éléments par défaut. Pour le composant « Accordéon » des formulaires adaptatifs, vous pouvez définir les éléments suivants :

* Le type des éléments d’en-tête HTML autorisés et définis comme valeur par défaut (tels que H1, H2, H3, etc.)
* Les composants principaux qu’un créateur ou une créatrice de formulaire peut ajouter à l’accordéon dans l’éditeur de formulaires adaptatifs
* Les noms simples pour les styles (classes CSS) qui peuvent être appliqués dans la boîte de dialogue des propriétés du composant « Accordéon » dans l’éditeur de formulaires adaptatifs.

Cela permet de rendre le processus de création et de personnalisation de formulaires plus simple et plus efficace.

### Onglet Propriétés {#properties-tab-design}

L’onglet Propriétés permet aux créateurs et aux créatrices de modèles de définir et d’autoriser des éléments d’en-tête HTML par défaut pour les créateurs et créatrices de formulaires :

![Onglet Propriétés de la boîte de dialogue de conception](/help/assets/accordion-design-properties.png)

* **Éléments d’en-tête autorisés** : une liste déroulante comportant plusieurs options permettant au créateur ou à la créatrice du modèle de choisir les en-têtes quu peuvent être utilisés pour l’accordéon.

* **Élément d’en-tête par défaut** : une liste déroulante qui définit l’élément d’en-tête par défaut pour le composant « Accordéon ».

### Onglet Composants autorisés {#allowed-components-tab}

L’onglet **Composants autorisés** permet à l’éditeur de modèles de définir les composants qui peuvent être ajoutés en tant qu’éléments aux panneaux dans le composant « Accordéon » de l’éditeur de formulaires adaptatifs.

### Onglet Styles {#styles-tab}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS d’un composant. Le composant principal « Accordéon » des formulaires adaptatifs prend en charge le [Système de style](/help/get-started/authoring.md#component-styling) d’AEM.

**Classes CSS par défaut** : vous pouvez fournir une classe CSS par défaut pour le composant « Accordéon ».

**Styles autorisés** : vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé « texte en gras » et fournir la classe CSS « police d’épaisseur : gras ». Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de formulaires adaptatifs. Pour appliquer un style, sélectionnez le composant auquel vous souhaitez appliquer le style dans l’éditeur de formulaires adaptatifs, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans la liste déroulante **Styles**. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.


<!--- 

The design dialog allows the template author to define the options available to the content author who uses the Accordion Component and the defaults set when placing the Accordion Component.


### Properties Tab {#properties-tab-design}

![Design dialog properties tab](/help/assets/accordion-design-properties.png)

* **Allowed Heading Elements** - This multi-select drop-down defines the accordion item heading HTML elements that are allowed to be selected by an author.
* **Default Heading Element** - This drop-down defines the default accordion item heading HTML element.

### Allowed Components Tab {#allowed-components-tab}

The **Allowed Components** tab is used to define which components can be added as items to panels in the Accordion Component by the content author.

The Allowed Components tab functions in the same way as the tab of the same name when [defining the policy and properties of a Layout Container in the Template Editor.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-layout-template-author)

### Styles Tab {#styles-tab}

The Accordion Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

The Accordion Component supports the [Adobe Client Data Layer.](/help/developing/data-layer/overview.md) 


-->

## Article connexe {#related-article}

* [Création d’un formulaire adaptatif dans une page AEM Sites ou un fragment d’expérience](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=fr)

* [Création d’un formulaire adaptatif autonome](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=fr)

## Voir aussi {#see-also}

* [Bouton](/help/adaptive-forms/components/button.md)
* [Case à cocher Groupe](/help/adaptive-forms/components/checkbox-group.md)
* [Sélecteur de date](/help/adaptive-forms/components/date-picker.md)
* [Liste déroulante](/help/adaptive-forms/components/drop-down.md)
* [Entrée d’e-mail](/help/adaptive-forms/components/email-input.md)
* [Conteneur de formulaires](/help/adaptive-forms/components/form-container.md)
* [Pièce jointe](/help/adaptive-forms/components/file-attachment.md)
* [Pied de page](/help/adaptive-forms/components/footer.md)
* [En-tête](/help/adaptive-forms/components/header.md)
* [Onglets horizontaux](/help/adaptive-forms/components/horizontal-tabs.md)
* [Image](/help/adaptive-forms/components/image.md)
* [Entrée de nombre](/help/adaptive-forms/components/number-input.md)
* [Conteneur de panneau](/help/adaptive-forms/components/panel-container.md)
* [Bouton radio](/help/adaptive-forms/components/radio-button.md)
* [Bouton de réinitialisation](/help/adaptive-forms/components/reset-button.md)
* [Bouton Envoyer](/help/adaptive-forms/components/submit-button.md)
* [Entrée téléphonique](/help/adaptive-forms/components/telephone-input.md)
* [Entrée de texte](/help/adaptive-forms/components/text-input.md)
* [Texte](/help/adaptive-forms/components/text.md)
* [Titre](/help/adaptive-forms/components/title.md)
* [Assistant](/help/adaptive-forms/components/wizard.md)