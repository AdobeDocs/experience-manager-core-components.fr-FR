---
title: Composant principal des formulaires adaptatifs - Bouton radio
description: Utilisation ou personnalisation du composant principal « Bouton radio » des formulaires adaptatifs.
role: Architect, Developer, Admin, User
exl-id: 86b5e9ec-58ac-4cd5-9c7c-4269247ec34f
source-git-commit: 7888cfa0f1358ce8018fc1e3cc3b19eb66a82b9d
workflow-type: ht
source-wordcount: '1703'
ht-degree: 100%

---

# Bouton Radio {#radio-button-adaptive-forms-core-component}

Un bouton radio dans un formulaire adaptatif est un type d’élément d’entrée qui permet à un utilisateur ou une utilisatrice de sélectionner une option dans un groupe d’options associées. Il est représenté par un petit bouton circulaire rempli ou vide pour indiquer si l’option est sélectionnée ou non. Lorsqu’un utilisateur ou une utilisatrice sélectionne un bouton radio, les autres boutons du groupe sont désélectionnés. Les boutons radio sont généralement utilisés lorsqu’il existe plusieurs options s’excluant mutuellement et qu’une seule option peut être sélectionnée à la fois.

**Exemple**

![](/help/adaptive-forms/assets/radio-button.png)

**Boîte de dialogue Propriétés**

![](/help/adaptive-forms/assets/radio-button-properties.png)

Dans cet exemple, l’élément Options est utilisé pour associer les boutons radio. L’élément **Texte d’affichage** sert à fournir un libellé pour un élément et **Valeur des données** sert à spécifier la valeur envoyée au serveur lors de l’envoi du formulaire.

Chaque option de bouton radio possède une valeur de données unique et un attribut « Texte d’affichage ». Si un utilisateur ou une utilisatrice sélectionne « 1-10 », la valeur de données correspondante est envoyée au serveur lors de l’envoi du formulaire. Ces données peuvent ensuite être traitées par un script côté serveur afin de déterminer quelles options ont été sélectionnées par l’utilisateur ou l’utilisatrice. Elles peuvent également être utilisées pour effectuer diverses actions, comme mettre à jour d’autres champs du formulaire ou envoyer les données du formulaire à un script côté serveur en vue d’un traitement ultérieur.

En outre, chaque bouton radio peut être configuré pour avoir des valeurs de traitement différentes pour chaque option, et cela peut être défini à l’aide de l’éditeur de règles des formulaires adaptatifs.

## Utilisation {#reasons-to-use-radio-button}

Il existe plusieurs raisons d’utiliser des boutons radio dans un formulaire, notamment :

* **Choix limités** : les boutons radio sont utilisés pour fournir une liste d’options prédéfinies parmi lesquelles l’utilisateur ou l’utilisatrice peut choisir, et une seule option peut être sélectionnée à la fois. Cela est utile lorsque le nombre d’options est limité et qu’elles s’excluent mutuellement.

* **Représentation claire** : les boutons radio sont clairs et faciles à comprendre, ce qui permet aux utilisateurs et aux utilisatrices de savoir ce qu’ils ou elles sélectionnent.

* **Cohérence** : l’utilisation des boutons radio permet de présenter de manière cohérente et normalisée les options aux utilisateurs et utilisatrices, ce qui facilite leur compréhension et leur interaction avec le formulaire.

* **Utilisation plus facile** : les boutons radio sont faciles à utiliser, en particulier pour les utilisateurs et utilisatrices qui ne sont pas familiers avec la technologie ou qui ont une mobilité limitée.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Accordéon des formulaires adaptatifs a été publié en février 2023 au sein des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec la <br>[version 2.0.4](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible avec les<br>[versions 1.1.12](/help/adaptive-forms/version.md) à 2.0.0 exclue. |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Retrouvez les informations les plus récentes sur le composant principal « Bouton radio » des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/radiobutton/v1/radiobutton). Pour plus d’informations sur le développement des composants principaux, consultez la [Documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience du bouton radio pour les visiteurs et les visiteuses en utilisant la boîte de dialogue Configurer. Vous pouvez également définir facilement des options de bouton radio pour une expérience utilisateur fluide.

![Onglet De base](/help/adaptive-forms/assets/radiobutton_basictab.png)

* **Nom** - Vous pouvez identifier facilement un composant de formulaire en lui attribuant un nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

* **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

* **Masquer le titre** - Sélectionnez cette option pour masquer le titre du composant.

  Dans l’onglet **Options**, vous pouvez ajouter des valeurs de données et afficher des paires de texte à l’aide du bouton **Ajouter**. Une fois qu’une nouvelle option est ajoutée, les actions suivantes peuvent être effectuées :

   * **Valeur des données** - Cette option permet de saisir le contenu à envoyer lorsqu’une option est sélectionnée.
   * **Texte d’affichage** - Cette option permet de saisir le contenu à afficher dans un formulaire adaptatif.
   * **Supprimer** - Appuyez ou cliquez sur supprimer pour supprimer l’option d’un bouton radio.
   * **Réorganiser** - Appuyez ou cliquez et faites glisser pour réorganiser l’ordre des options.

* **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.

* **Type de données de la valeur envoyée** - Cette option spécifie le type de données de la valeur envoyée lorsqu’une option est sélectionnée. Si le **type de données de la valeur envoyée** est défini sur `Number` et que vous ajoutez des données de chaîne à la **Valeur des données** dans l’onglet **Options**, l’écran affiche un message d’erreur `Value type mismatch`.

* **Options par défaut** - Cette option vous permet d’ajouter des valeurs par défaut pré-sélectionnées lors du chargement du formulaire. Si le **type de données de la valeur envoyée** est défini sur `Number` et que vous ajoutez des données de chaîne aux **options par défaut**, le message d’erreur suivant s’affiche à l’écran : `Value type mismatch`.

* **Options d’affichage** : cette option permet de définir l’alignement visuel des boutons radio d’un formulaire adaptatif. Les deux options prises en charge sont les suivantes :
   * **Horizontal** : sélectionnez cette option pour afficher les boutons radio de gauche à droite dans un formulaire adaptatif.
   * **Vertical** : sélectionnez cette option pour afficher les boutons radio de haut en bas dans un formulaire adaptatif.
* **Masquer le composant** : sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.
* **Désactiver le composant** - Sélectionnez cette option pour désactiver le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
* **Lecture seule** - Sélectionnez cette option pour rendre le composant non modifiable. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

### Onglet Validation {#validation-tab}

![Onglet Validation](/help/adaptive-forms/assets/radiobutton_validationtab.png)

* **Obligatoire** : Sélectionnez cette option si vous souhaitez afficher le composant dans un formulaire adaptatif. Vous ne pouvez pas sélectionner **Masquer le composant** ou **Désactiver le composant**  dans l’onglet **De base** lorsque cette option est sélectionnée.

* **Message d’erreur** - Cette option vous permet de saisir un message qui s’affiche si la case à cocher **Obligatoire** est cochée et que le champ de formulaire reste vide.

* **Message de validation de script** : cette option permet de saisir un message à afficher en cas d’échec de la validation du script.

### Onglet Contenu de l’aide {#helpcontent-tab}

![Onglet Contenu d’aide](/help/adaptive-forms/assets/radiobutton_helptab.png)

* **Description courte** : Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez l’option **Toujours afficher une description courte** pour l’afficher sous le composant.

* **Toujours afficher une description courte** - Activez cette option pour afficher la description courte sous le composant.

* **Texte d’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility-tab}

![Onglet Accessibilité](/help/adaptive-forms/assets/radiobutton_accessibilitytab.png)

**Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS du composant Bouton radio.


### Onglet Styles {#styles-tab}

Cet onglet vous permet de définir et de gérer les styles CSS d’un composant. Le composant principal Bouton radio pour les formulaires adaptatifs prend en charge le [Système de style](/help/get-started/authoring.md#component-styling) d’AEM.

![Boîte de dialogue Conception de style.](/help/adaptive-forms/assets/radiobutton_designdialog.png)

* **Classes CSS par défaut** : vous pouvez indiquer une classe CSS par défaut pour le composant principal Bouton radio pour les formulaires adaptatifs.

* **Styles autorisés** : vous pouvez définir des styles en indiquant un nom et la classe CSS du style. Par exemple, vous pouvez créer un style nommé « texte en gras » et fournir la classe CSS « police d’épaisseur : gras ». Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de formulaires adaptatifs. Pour appliquer un style, sélectionnez le composant auquel vous souhaitez appliquer le style dans l’éditeur de formulaires adaptatifs, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans la liste déroulante **Styles**. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

## Article connexe {#related-article}

* [Création d’un formulaire adaptatif dans une page AEM Sites ou un fragment d’expérience](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=fr)

* [Création d’un formulaire adaptatif autonome](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=fr)
