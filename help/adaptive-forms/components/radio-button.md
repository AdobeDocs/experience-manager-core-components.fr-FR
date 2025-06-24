---
title: Composant principal des formulaires adaptatifs - Bouton radio
description: Utilisation ou personnalisation du composant principal « Bouton radio » des formulaires adaptatifs.
role: Architect, Developer, Admin, User
exl-id: 86b5e9ec-58ac-4cd5-9c7c-4269247ec34f
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '2135'
ht-degree: 98%

---


# Composant Bouton radio {#radio-button-adaptive-forms-core-component}

Un bouton radio dans un formulaire adaptatif est un type d’élément d’entrée qui permet à un utilisateur ou une utilisatrice de sélectionner une option dans un groupe d’options associées. Il est représenté par un petit bouton circulaire rempli ou vide pour indiquer si l’option est sélectionnée ou non. Lorsqu’un utilisateur ou une utilisatrice sélectionne un bouton radio, les autres boutons du groupe sont désélectionnés. Les boutons radio sont généralement utilisés lorsqu’il existe plusieurs options s’excluant mutuellement et qu’une seule option peut être sélectionnée à la fois.

{{traditional-aem}}

**Exemple**

![exemple](/help/adaptive-forms/assets/radio-button.png)

**Boîte de dialogue Propriétés**

![exemple](/help/adaptive-forms/assets/radio-button-properties.png)

Dans cet exemple, l’élément Options est utilisé pour associer les boutons radio. L’élément **Texte d’affichage** sert à fournir un libellé pour un élément et **Valeur des données** sert à spécifier la valeur envoyée au serveur lors de l’envoi du formulaire.

Chaque option de bouton radio possède une valeur de données unique et un attribut « Texte d’affichage ». Si un utilisateur ou une utilisatrice sélectionne « 1-10 », la valeur de données correspondante est envoyée au serveur lors de l’envoi du formulaire. Ces données peuvent ensuite être traitées par un script côté serveur afin de déterminer quelles options ont été sélectionnées par l’utilisateur ou l’utilisatrice. Elles peuvent également être utilisées pour effectuer diverses actions, comme mettre à jour d’autres champs du formulaire ou envoyer les données du formulaire à un script côté serveur en vue d’un traitement ultérieur.

En outre, chaque bouton radio peut être configuré pour avoir des valeurs de traitement différentes pour chaque option, et cela peut être défini à l’aide de l’éditeur de règles des formulaires adaptatifs

## Utilisation {#reasons-to-use-radio-button}

Il existe plusieurs raisons d’utiliser des boutons radio dans un formulaire, notamment :

- **Choix limités** : les boutons radio sont utilisés pour fournir une liste d’options prédéfinies parmi lesquelles l’utilisateur ou l’utilisatrice peut choisir, et une seule option peut être sélectionnée à la fois. Cela est utile lorsque le nombre d’options est limité et qu’elles s’excluent mutuellement.

- **Représentation claire** : les boutons radio sont clairs et faciles à comprendre, ce qui permet aux utilisateurs et aux utilisatrices de savoir ce qu’ils ou elles sélectionnent.

- **Cohérence** : l’utilisation des boutons radio permet de présenter de manière cohérente et normalisée les options aux utilisateurs et utilisatrices, ce qui facilite leur compréhension et leur interaction avec le formulaire.

- **Utilisation plus facile** : les boutons radio sont faciles à utiliser, en particulier pour les utilisateurs et utilisatrices qui ne sont pas familiers avec la technologie ou qui ont une mobilité limitée.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Bouton radio pour Forms adaptatif a été publié en février 2023 dans le cadre des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec la <br>[version 2.0.4](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible avec les<br>[versions 1.1.12](/help/adaptive-forms/version.md) à 2.0.0 exclue. |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_fr). -->

## Détails techniques {#technical-details}

Retrouvez les informations les plus récentes sur le composant principal « Bouton radio » des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/radiobutton/v1/radiobutton). Pour plus d’informations sur le développement des composants principaux, consultez la [Documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience du bouton radio pour les visiteurs et les visiteuses en utilisant la boîte de dialogue Configurer. Vous pouvez également définir facilement des options de bouton radio pour une expérience utilisateur fluide.

### Onglet de base

![Onglet De base](/help/adaptive-forms/assets/radiobutton_basictab.png)

- **Nom** - Vous pouvez identifier facilement un composant de formulaire en lui attribuant un nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

- **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.
- **Autoriser le texte enrichi pour le titre** - Cette fonctionnalité permet aux personnes de mettre en forme les titres en texte brut en y incorporant des fonctionnalités telles que le texte en gras, en italique et souligné, diverses polices, tailles de police et couleurs, et d’autres options pour améliorer la présentation visuelle et la personnalisation. Elle offre une plus grande flexibilité et un contrôle créatif pour faire ressortir les titres dans les documents, sites web ou applications.\
  Lorsque vous cochez la case **Autoriser le texte enrichi pour le titre**, les options de formatage deviennent visibles pour appliquer un style au titre du composant. Pour accéder à toutes les options de formatage disponibles, vous pouvez cliquer sur l’onglet ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Prise en charge de texte enrichi](/help/adaptive-forms/assets/richtext-support-title.png)

- **Masquer le titre** - Sélectionnez cette option pour masquer le titre du composant.

- **Options** - Vous pouvez ajouter des valeurs de données et des paires de texte d’affichage à l’aide du bouton **Ajouter**.\
  Lorsqu’une nouvelle option est ajoutée, les actions suivantes peuvent être effectuées :
   - **Valeur des données** - Cette option permet de saisir le contenu à envoyer lorsqu’une option est sélectionnée.
   - **Texte d’affichage** - Cette option permet de saisir le contenu à afficher dans un formulaire adaptatif.
   - **Supprimer** - Appuyez ou cliquez sur supprimer pour supprimer l’option d’un bouton radio.
   - **Réorganiser** - Appuyez ou cliquez et faites glisser pour réorganiser l’ordre des options.
Vous pouvez également mettre en forme les options du groupe de boutons radio à l’aide de **Autoriser le texte enrichi pour les options**.

  ![Prise en charge du texte enrichi pour les options](/help/adaptive-forms/assets/richtext-for-options.png)

  Une fois que vous avez coché la case **Autoriser le texte enrichi pour les options**, les options de formatage deviennent visibles pour appliquer un style aux options du composant. Pour accéder à toutes les options de formatage disponibles, vous pouvez cliquer sur l’onglet `Fullscreen` ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Prise en charge du texte enrichi pour les options](/help/adaptive-forms/assets/richtextoptions-support.png)

- **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.

- **Marquer comme élément de formulaire non lié** : sélectionnez cette option pour configurer un champ de formulaire qui n’est lié à aucun schéma. Cette option vous permet d’enregistrer des données sans mettre à jour la source de données. Elle vous permet également de gérer les données de manière personnalisée, en les séparant de l’intégration de base de données standard.

- **Type de données de la valeur envoyée** - Cette option spécifie le type de données de la valeur envoyée lorsqu’une option est sélectionnée. Si le **type de données de la valeur envoyée** est défini sur `Number` et que vous ajoutez des données de chaîne à la **Valeur des données** dans l’onglet **Options**, l’écran affiche un message d’erreur `Value type mismatch`.

- **Options par défaut** - Cette option vous permet d’ajouter des valeurs par défaut pré-sélectionnées lors du chargement du formulaire. Si le **type de données de la valeur envoyée** est défini sur `Number` et que vous ajoutez des données de chaîne aux **options par défaut**, le message d’erreur suivant s’affiche à l’écran : `Value type mismatch`.

- **Options d’affichage** : cette option permet de définir l’alignement visuel des boutons radio d’un formulaire adaptatif. Les deux options prises en charge sont les suivantes :
   - **Horizontal** : sélectionnez cette option pour afficher les boutons radio de gauche à droite dans un formulaire adaptatif.
   - **Vertical** : sélectionnez cette option pour afficher les boutons radio de haut en bas dans un formulaire adaptatif.
- **Masquer le composant** : sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.
- **Désactiver le composant** - Sélectionnez cette option pour désactiver le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
- **Lecture seule** - Sélectionnez cette option pour rendre le composant non modifiable. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

### Onglet Validation {#validation-tab}

![Onglet Validation](/help/adaptive-forms/assets/radiobutton_validationtab.png)

- **Obligatoire** : Sélectionnez cette option si vous souhaitez afficher le composant dans un formulaire adaptatif. Après avoir sélectionné cette option, vous devez effectuer une sélection avant de poursuivre l’envoi du formulaire. Vous ne pouvez pas sélectionner **Masquer le composant** ou **Désactiver le composant**  dans l’onglet **De base** lorsque cette option est sélectionnée.
- **Message d’erreur** : cette option vous permet de rédiger un message qui s’affiche si la case à cocher **Obligatoire** est activée et le champ de formulaire reste vide.

- **Message de validation de script** : cette option permet de saisir un message à afficher en cas d’échec de la validation du script.

### Onglet Contenu de l’aide {#helpcontent-tab}

![Onglet Contenu d’aide](/help/adaptive-forms/assets/radiobutton_helptab.png)

- **Description courte** : Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez l’option **Toujours afficher une description courte** pour l’afficher sous le composant.

- **Toujours afficher une description courte** - Activez cette option pour afficher la description courte sous le composant.

- **Texte d’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility-tab}

![Onglet Accessibilité](/help/adaptive-forms/assets/radiobutton_accessibilitytab.png)

- **Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.
   - **Texte personnalisé** : sélectionnez cette option pour utiliser le texte personnalisé pour les libellés d’accessibilité ARIA. Cette option affiche la boîte de dialogue Texte personnalisé. Vous pouvez ajouter des informations pertinentes dans la boîte de dialogue Texte personnalisé.
   - **Description** : sélectionnez cette option pour utiliser la description des libellés d’accessibilité ARIA.
   - **Titre** : sélectionnez cette option pour utiliser le titre pour les libellés d’accessibilité ARIA.
   - **Nom** : sélectionnez cette option pour utiliser le nom pour les libellés d’accessibilité ARIA.
   - **Aucun** : sélectionnez cette option si vous ne souhaitez pas ajouter de texte supplémentaire pour les libellés d’accessibilité ARIA.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS du composant Bouton radio.


### Onglet Styles {#styles-tab}

Cet onglet vous permet de définir et de gérer les styles CSS d’un composant. Le composant principal Bouton radio pour les formulaires adaptatifs prend en charge le [Système de style](/help/get-started/authoring.md#component-styling) d’AEM.

![Boîte de dialogue de conception.](/help/adaptive-forms/assets/checkbox-style.png)

- **Classes CSS par défaut** : vous pouvez indiquer une classe CSS par défaut pour le composant principal Bouton radio des formulaires adaptatifs.

- **Styles autorisés** : vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé « texte en gras » et fournir la classe CSS « police d’épaisseur : gras ». Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de formulaires adaptatifs. Pour appliquer un style, sélectionnez le composant auquel vous souhaitez appliquer le style dans l’éditeur de formulaires adaptatifs, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans la liste déroulante **Styles**. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

### Propriétés personnalisées

![Boîte de dialogue Propriétés personnalisées](/help/adaptive-forms/assets/checkbox-customproperties.png)

Les propriétés personnalisées vous permettent d’associer des attributs personnalisés (paires clé-valeur) à un composant principal de formulaire adaptatif à l’aide du modèle de formulaire. Les propriétés personnalisées sont répercutées dans la section des propriétés du rendu déocuplé du composant. Cela permet de créer un comportement de formulaire dynamique qui s’adapte en fonction des valeurs d’attributs personnalisés. Par exemple, les développeurs et développeuses peuvent concevoir plusieurs rendus d’un composant de formulaires découplés pour des plateformes mobiles, de bureau ou web, ce qui améliore considérablement l’expérience client sur un large éventail d’appareils.

- **Nom du groupe** : vous pouvez fournir un nom pour identifier le groupe de propriétés personnalisées. Vous pouvez ajouter, supprimer ou réorganiser plusieurs groupes de propriétés personnalisées. Après avoir ajouté le groupe de propriétés personnalisées, vous pouvez voir les options suivantes :

   - **Paires clé-valeur** : vous pouvez ajouter plusieurs noms et valeurs de propriétés personnalisées en cliquant sur le bouton **Ajouter** pour chaque groupe de propriétés personnalisées.

   - **Supprimer** : appuyez ou cliquez pour supprimer le nom et la valeur des propriétés personnalisées.

   - **Réorganiser** : appuyez ou cliquez et faites glisser pour réorganiser l’ordre du nom et de la valeur des propriétés personnalisées.

## Articles connexes {#related-articles}

{{more-like-this}}

## Voir également {#see-also}

{{see-also}}
