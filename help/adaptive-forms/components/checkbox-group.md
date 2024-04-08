---
title: Composant principal des formulaires adaptatifs - Groupe de cases à cocher
description: Utilisation ou personnalisation du composant principal « Groupe de cases à cocher » des formulaires adaptatifs.
role: Architect, Developer, Admin, User
exl-id: 2ced0223-e664-470b-a400-b6865d3a67c9
source-git-commit: e4274194026c3370b52be17171776847374a86b5
workflow-type: tm+mt
source-wordcount: '1869'
ht-degree: 98%

---

# Groupe de cases à cocher {#button-component-adaptive-forms-core-component}

Un groupe de cases à cocher dans un formulaire adaptatif est un ensemble de cases à cocher associées qui permettent aux utilisateurs et aux utilisatrices de sélectionner une ou plusieurs options d’une liste. Chaque case à cocher est représentée par une valeur de données (valeur utilisée pour traiter les éléments d’un groupe de cases à cocher) et une valeur d’affichage (libellé pour chaque élément de case à cocher qui décrit son objectif).

**Exemple**

![exemple de groupe de cases à cocher](/help/adaptive-forms/assets/checkbox-group.png)

**Boîte de dialogue Propriétés**

![boîte de dialogue de propriété du groupe de cases à cocher](/help/adaptive-forms/assets/checkbox-group-properties.png)

Dans cet exemple, l’élément Options est utilisé pour associer les cases à cocher. L’élément **Texte d’affichage** sert à fournir un libellé pour un élément et **Valeur des données** sert à spécifier la valeur envoyée au serveur lors de l’envoi du formulaire.

Chaque option/élément de case à cocher possède une valeur de données unique et un attribut de texte d’affichage. Si un utilisateur ou une utilisatrice coche les cases « Fils » et « Fille », la valeur de données correspondante est envoyée au serveur lors de l’envoi du formulaire. Ces données peuvent ensuite être traitées par un script côté serveur afin de déterminer quelles options ont été sélectionnées par l’utilisateur ou l’utilisatrice. Elles peuvent également être utilisées pour effectuer diverses actions, comme mettre à jour d’autres champs du formulaire ou envoyer les données du formulaire à un script côté serveur en vue d’un traitement ultérieur.

De plus, le groupe de cases à cocher peut être configuré pour avoir différentes valeurs de traitement pour chaque option. Cela peut être défini à l’aide de l’éditeur de règles des formulaires adaptatifs.

## Utilisation {#reasons-to-use-check-box-group}

Il existe plusieurs raisons d’inclure un groupe de cases à cocher dans un formulaire adaptatif, notamment :

- **Sélections multiples** : un groupe de cases à cocher permet aux utilisateurs et aux utilisatrices de sélectionner plusieurs options dans une liste, ce qui peut s’avérer utile dans les cas où plusieurs sélections sont autorisées ou obligatoires.

- **Expérience utilisateur** : le groupe de cases à cocher peut être utilisé pour rendre le formulaire plus convivial en offrant une méthode claire et intuitive de sélection de plusieurs options aux utilisateurs et aux utilisatrices.

- **Analyse des données** : le groupe de cases à cocher peut être utilisé pour collecter des données provenant de diverses sources et les analyser, ou pour les utiliser comme entrée pour un traitement ultérieur.

- **Questionnaires** : le groupe de cases à cocher peut être utilisé dans les enquêtes pour sélectionner plusieurs options pour une question.

- **Préférences utilisateur** : le groupe de cases à cocher peut être utilisé pour collecter les préférences de l’utilisateur ou de l’utilisatrice pour différentes options.

- **Valeur des données** : le groupe de cases à cocher peut également être utilisé pour traiter les éléments d’un groupe de cases à cocher.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Accordéon des formulaires adaptatifs a été publié en février 2023 au sein des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec la <br>[version 2.0.4](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible avec les<br>[versions 1.1.12](/help/adaptive-forms/version.md) à 2.0.0 exclue. |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Retrouvez les dernières informations sur le composant principal « Groupe de cases à cocher » des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkboxgroup/v1/checkboxgroup). Pour plus d’informations sur le développement des composants principaux, consultez la [Documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience des cases à cocher pour les visiteurs et les visiteuses en utilisant la boîte de dialogue Configurer. Vous pouvez également définir facilement des options de case à cocher pour une expérience utilisateur fluide.


### Onglet De base {#basic-tab}

![Onglet De base](/help/adaptive-forms/assets/checkbox_basictab.png)

- **Nom** - Le nom identifie de manière unique le composant dans l’éditeur de règles. Les caractères spéciaux et les espaces ne sont pas autorisés dans les chaînes de nom.

- **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

<!-- **Allow Rich Text for Title** - This features enables users to format plain text titles, incorporating features like bold, italic, underlined text, various fonts, font sizes, colors, and additional option to enhance visual presentation and customization. It offers greater flexibility and creative control in making titles stand out within documents, websites, or applications.  
    Upon selecting the checkbox for **Allow Rich Text for Title** , formatting options become visible to style the component's title. To access all available formatting options, you can click on the `Fullscreen` ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png) tab.
     
     ![Rich text support](/help/adaptive-forms/assets/richtext-support-title.png) -->

- **Masquer le titre** - Sélectionnez cette option pour masquer le titre du composant.

- **Options** - Vous pouvez ajouter des valeurs de données et afficher des paires de texte à l’aide de la variable **Ajouter** bouton .\
  Une fois une nouvelle option ajoutée, les actions suivantes peuvent être effectuées :
   - **Valeur des données** - Cette option permet de saisir le contenu à envoyer lorsqu’une option est sélectionnée.
   - **Texte d’affichage** - Cette option permet de saisir le contenu à afficher dans un formulaire adaptatif.
   - **Supprimer** - Appuyez ou cliquez sur supprimer pour supprimer l’option d’une case à cocher.
   - **Réorganiser** : Appuyez ou cliquez et faites glisser pour réorganiser l’ordre des panneaux.

<!-- You can also format the options for checkbox group using **Allow Rich Text for Options**. 
  
     ![Rich text support for options](/help/adaptive-forms/assets/richtext-for-options.png)

    Once you select the checkbox for **Allow Rich Text for Options** formatting options become visible to style the component's options. To access all available formatting options, you can click on the `Fullscreen` ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png) tab.
     ![Rich text support for options](/help/adaptive-forms/assets/richtextoptions-support.png)

    -->

- **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.

- **Marquer comme élément de formulaire non lié** : sélectionnez cette option pour configurer un champ de formulaire qui n’est lié à aucun schéma. Cette option vous permet d’enregistrer des données sans mettre à jour la source de données. Elle vous permet également de gérer les données de manière personnalisée, en les séparant de l’intégration de base de données standard.

- **Type de données de la valeur envoyée** - Cette option spécifie le type de données de la valeur envoyée lorsqu’une option est sélectionnée. Si le **type de données de la valeur envoyée** est défini sur `Number` et que vous ajoutez des données de chaîne à **Valeur des données** dans l’onglet **Options**, l’écran affiche un message d’erreur `Value type mismatch`.

- **Options d’affichage** - Cette option est utilisée pour définir l’alignement visuel des cases à cocher dans un formulaire adaptatif. Les deux options prises en charge sont les suivantes :
   - **Horizontal** - Lorsque cette option est sélectionnée, les cases à cocher s’affichent de gauche à droite dans un formulaire adaptatif.
   - **Vertical** - Lorsque cette option est sélectionnée, les cases à cocher s’affichent de haut en bas dans un formulaire adaptatif.

- **Options par défaut** - Cette option vous permet d’ajouter des valeurs par défaut présélectionnées au chargement du formulaire. Utilisez l’icône Supprimer pour supprimer les options ajoutées. Si le **type de données de la valeur envoyée** est défini sur `Number` et que vous ajoutez des données de chaîne à **Options par défaut**, l’écran affiche un message d’erreur `Value type mismatch`.
- **Masquer le composant** - Sélectionnez l’option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.
- **Désactiver le composant** - Sélectionnez cette option pour désactiver le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
- **Lecture seule** - Sélectionnez cette option pour rendre le composant non modifiable. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

### Onglet Validation {#validation-tab}

![Onglet Validation](/help/adaptive-forms/assets/checkbox_validationtab.png)

- **Obligatoire** : Sélectionnez cette option si vous souhaitez afficher le composant dans un formulaire adaptatif. Après avoir sélectionné cette option, vous devez effectuer une sélection avant de poursuivre l’envoi du formulaire. Vous ne pouvez pas sélectionner **Masquer le composant** ou **Désactiver le composant**  dans l’onglet **De base** lorsque cette option est sélectionnée.

- **Message d’erreur** : Cette option vous permet de saisir un message qui s’affiche si la case à cocher **Obligatoire** est cochée et que le champ de formulaire reste vide.

- **Message de validation de script** : cette option permet de saisir un message à afficher en cas d’échec de la validation du script.

### Onglet Contenu de l’aide {#helpcontent-tab}

![Onglet Contenu d’aide](/help/adaptive-forms/assets/checkbox_helptab.png)

- **Description courte** : Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez l’option **Toujours afficher une description courte** pour l’afficher sous le composant.

- **Toujours afficher une description courte** - Activez cette option pour afficher la description courte sous le composant.

- **Texte d’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility-tab}

![Onglet Accessibilité](/help/adaptive-forms/assets/checkbox_accessibility.png)

**Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS du composant « Groupe de cases à cocher ».

### Onglet Styles {#styles-tab}

Le composant principal du groupe de cases à cocher des formulaires adaptatifs prend en charge le [système de style](/help/get-started/authoring.md#component-styling) d’AEM.

![Boîte de dialogue de conception.](/help/adaptive-forms/assets/checkbox-style.png)

- **Classes CSS par défaut** : vous pouvez fournir une classe CSS par défaut pour le composant principal du groupe de cases à cocher des formulaires adaptatifs.

- **Styles autorisés** : vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé « texte en gras » et fournir la classe CSS « police d’épaisseur : gras ». Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de formulaires adaptatifs. Pour appliquer un style, sélectionnez le composant auquel vous souhaitez appliquer le style dans l’éditeur de formulaires adaptatifs, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans la liste déroulante **Styles**. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

### Propriétés personnalisées

![Boîte de dialogue Propriétés personnalisées](/help/adaptive-forms/assets/checkbox-customproperties.png)

Les propriétés personnalisées vous permettent d’associer des attributs personnalisés (paires clé-valeur) à un composant principal de formulaire adaptatif à l’aide du modèle de formulaire. Les propriétés personnalisées sont répercutées dans la section des propriétés du rendu déocuplé du composant. Cela permet de créer un comportement de formulaire dynamique qui s’adapte en fonction des valeurs d’attributs personnalisés. Par exemple, les développeurs et développeuses peuvent concevoir plusieurs rendus d’un composant de formulaires découplés pour des plateformes mobiles, de bureau ou web, ce qui améliore considérablement l’expérience client sur un large éventail d’appareils.

- **Nom du groupe** : vous pouvez fournir un nom pour identifier le groupe de propriétés personnalisées. Vous pouvez ajouter, supprimer ou réorganiser plusieurs groupes de propriétés personnalisées. Après avoir ajouté le groupe de propriétés personnalisées, vous pouvez voir les options suivantes :

   - **Paires clé-valeur** : vous pouvez ajouter plusieurs noms et valeurs de propriétés personnalisées en cliquant sur le bouton **Ajouter** pour chaque groupe de propriétés personnalisées.

   - **Supprimer** : appuyez ou cliquez pour supprimer le nom et la valeur des propriétés personnalisées.

   - **Réorganiser** : appuyez ou cliquez et faites glisser pour réorganiser l’ordre du nom et de la valeur des propriétés personnalisées.

## Articles connexes {#related-articles}

{{more-like-this}})

## Voir également {#see-also}

{{see-also}}
