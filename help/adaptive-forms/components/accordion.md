---
title: Accordéon de formulaire adaptatif
description: Utilisez l’accordéon pour organiser et simplifier un formulaire long ou complexe en le divisant en sections plus petites et plus faciles à gérer.
role: Architect, Developer, Admin, User
source-git-commit: 0e4fb8454b7ef84eb5b1b73b01c982a2f9c12381
workflow-type: tm+mt
source-wordcount: '1652'
ht-degree: 3%

---

# Composant d’accordéon  {#accordion-component-adaptive-forms-core-component}

Le composant principal Accordéon permet aux utilisateurs de créer des sections extensibles et réductibles dans un formulaire adaptatif. Il est souvent utilisé pour organiser et simplifier des formulaires longs ou complexes en les divisant en sections plus petites et plus faciles à gérer. Chaque section d’un accordéon est généralement représentée par un en-tête sur lequel l’utilisateur peut cliquer pour développer ou réduire le contenu correspondant. Le contenu peut être n’importe quel composant principal.

## Utilisation {#usage}

Plusieurs raisons expliquent l’intérêt d’inclure un accordéon dans un formulaire adaptatif, notamment :

* **Économie d’espace**: Un accordéon permet aux utilisateurs de développer et de réduire les sections d’un formulaire, réduisant ainsi l’espace nécessaire pour afficher tous les champs du formulaire en même temps.

* **Navigation**: Un accordéon peut être utilisé pour créer une structure de navigation hiérarchique, ce qui facilite la recherche des champs de formulaire dont les utilisateurs ont besoin.

* **Expérience utilisateur**: L’accordéon peut être utilisé pour rendre le formulaire plus convivial en offrant une méthode claire et intuitive d’accès et de remplissage des champs de formulaire.

* **Long Forms**: L’accordéon est un composant idéal pour gérer les formulaires longs, car il permet aux utilisateurs de se concentrer sur une section à la fois, plutôt que d’essayer de traiter de nombreuses informations en même temps.

Vous pouvez utiliser :

* Le [boîte de dialogue de configuration](#configure-dialog) pour spécifier les propriétés du composant d’accordéon.

* Le [Fenêtre contextuelle Sélectionner un panneau](#select-panel-popover)  pour définir l’ordre des panneaux de l’accordéon. Cela permet à l’auteur d’organiser les panneaux dans l’ordre dans lequel ils doivent apparaître.

* Options permettant à un auteur de formulaires d’activer ou de désactiver certaines fonctions dans la variable [boîte de dialogue de conception](#design-dialog). Par exemple, un auteur peut choisir de désactiver certains champs ou sections d’un formulaire. Ces options permettent à l’auteur de mieux contrôler la conception et les fonctionnalités du formulaire, ce qui facilite la création de formulaires adaptés aux besoins spécifiques de l’entreprise.

La boîte de dialogue de configuration, la fenêtre contextuelle de sélection et la boîte de dialogue de conception font toutes partie des composants principaux conçus pour faciliter la création des formulaires et fournir un moyen efficace de créer des formulaires complexes.

## Version et compatibilité {#version-and-compatibility}


Le composant principal d’accordéon Adaptive Forms a été publié en février 2023 dans le cadre de la version 2.0.4 des composants principaux. Voici un tableau présentant toutes les versions prises en charge, la compatibilité AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible avec<br>[version 2.0.4](/help/versions.md) et plus tard | Compatible | Compatible |

Pour plus d’informations sur les versions et versions des composants principaux, reportez-vous à la section [Versions des composants principaux](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Obtenez les dernières informations sur le composant d’accordéon dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/accordion/v1/accordion). Pour plus d’informations sur le développement des composants principaux, consultez la section [Documentation destinée aux développeurs sur les composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser votre expérience d’accordéon pour les visiteurs qui utilisent la boîte de dialogue Configurer . Vous pouvez également définir facilement des éléments d’accordéon, des panneaux, un comportement et une apparence pour une expérience utilisateur transparente.

### Onglet De base {#basic-tab}

![Onglet Simple](/help/adaptive-forms/assets/accordion_basictab.png)

* **Nom** - Vous pouvez identifier facilement un composant de formulaire avec son nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

* **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

* **Masquer le titre** - Sélectionnez l’option pour masquer le titre du composant.

* **Encapsuler des données dans l’objet** - Sélectionnez &quot;Placer les données dans un objet&quot; pour placer les données de champ de l’assistant dans un objet JSON. Si cette option n’est pas sélectionnée, le fichier JSON des données d’envoi présente une structure plate pour les champs de l’assistant.

* **Disposition** - Vous pouvez disposer d’une mise en page fixe (simple) ou d’une mise en page flexible (grille réactive) pour votre assistant. La mise en page simple conserve tout ce qui est fixe, tandis que la grille réactive vous permet d’ajuster la position des composants en fonction de vos besoins. Par exemple, utilisez la grille réactive pour aligner &quot;Prénom&quot;, &quot;Nom intermédiaire&quot; et &quot;Nom&quot; dans un formulaire sur une seule ligne.

* **Référence de liaison** - Une référence de liaison est une référence à un élément de données stocké dans une source de données externe et utilisé dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client dans un formulaire, en fonction de l’identifiant du client saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur transparente pour la collecte et la gestion des données.
* **Masquer le composant** - Sélectionnez l’option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par l’utilisateur.
* **Désactiver le composant** - Sélectionnez l’option pour désactiver le composant. Le composant désactivé n’est pas principal ni modifiable par l’utilisateur final. L’utilisateur peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

### Onglet Éléments {#items-tab}

![Onglet Éléments](/help/adaptive-forms/assets/accordion_itemstab.png)

Le bouton Ajouter vous permet de sélectionner un composant à ajouter sous forme de panneau à partir de la fenêtre de sélection des composants. Après avoir ajouté le composant, vous pouvez voir les options suivantes :

* **Icône** - L’icône identifie le composant du panneau dans la liste. Pointez sur l’icône pour afficher le nom complet du composant sous forme d’info-bulle.
* **Description** - Description utilisée comme texte du panneau. Par défaut, le nom du composant est sélectionné pour le panneau.
* **Supprimer** : appuyez ou cliquez sur cette option pour supprimer le panneau du composant d’accordéon.
* **Réorganiser** : appuyez ou cliquez dessus et faites glisser pour réorganiser l’ordre des panneaux.

### Onglet Contenu de l’aide {#help-content}

![Onglet Contenu de l’aide](/help/adaptive-forms/assets/accordion_helpcontent.png)

* **Description courte** - Une brève description est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez la variable **Toujours afficher une description courte** pour l’afficher sous le composant.

* **Toujours afficher une description courte** - Activez l’option pour afficher la description courte sous le composant.

* **Texte de l’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur clique sur l’icône d’aide (i) placée en regard du composant. Le texte d’aide fournit des informations plus détaillées que le texte d’étiquette ou d’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility}

![Onglet Accessibilité](/help/adaptive-forms/assets/accordion_accessibility.png)

* **Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisé par les malvoyants. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom et tout message pertinent du champ (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs, y compris ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

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

La boîte de dialogue Conception permet aux créateurs de modèles de contrôler l’affichage des éléments par défaut. Pour le composant d’accordéon Forms adaptatif, vous pouvez définir les éléments suivants :

* Type des éléments d’en-tête de HTML autorisés et définis comme valeur par défaut (tels que H1, H2, H3, etc.)
* Composants principaux qu’un créateur de formulaire peut ajouter à l’accordéon dans l’éditeur de Forms adaptatif
* Noms simples pour les styles (classes CSS) qui peuvent être appliqués dans la boîte de dialogue des propriétés du composant d’accordéon dans l’éditeur de Forms adaptatif.

Cela permet de rendre le processus de création et de personnalisation de formulaires plus simple et plus efficace.

### Onglet Propriétés {#properties-tab-design}

L’onglet Propriétés permet aux auteurs de modèles de définir des éléments d’en-tête de HTML par défaut et autorisés pour les auteurs de formulaires :

![Onglet Propriétés de la boîte de dialogue de conception](/help/assets/accordion-design-properties.png)

* **Éléments d’en-tête autorisés**: Liste déroulante comportant plusieurs options permettant à l’auteur du modèle de choisir les en-têtes que l’auteur peut utiliser pour l’accordéon.

* **Elément d’en-tête par défaut**: Une liste déroulante définit l’élément d’en-tête par défaut pour le composant d’accordéon.

### Onglet Composants autorisés {#allowed-components-tab}

Le **Composants autorisés** Cet onglet permet à l’éditeur de modèles de définir les composants qui peuvent être ajoutés en tant qu’éléments aux panneaux dans le composant Accordéon de l’éditeur Forms adaptatif.

### Onglet Styles {#styles-tab}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS d’un composant. Le composant principal Accordéon Forms adaptatif prend en charge l’AEM [Système de style](/help/get-started/authoring.md#component-styling).

**Classes CSS par défaut**: Vous pouvez fournir une classe CSS par défaut pour le composant d’accordéon.

**Styles autorisés**: Vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé &quot;bold text&quot; et fournir la classe CSS &quot;font-weight: bold&quot;. Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de Forms adaptatif. Pour appliquer un style, dans l’éditeur de Forms adaptatif, sélectionnez le composant auquel vous souhaitez appliquer le style, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans le **Styles** liste déroulante. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.


<!-- 

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




