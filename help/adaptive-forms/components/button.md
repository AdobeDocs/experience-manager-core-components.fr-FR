---
title: Composant principal de Forms adaptatif - Bouton
description: Utilisation ou personnalisation du composant principal du bouton Forms adaptatif .
role: Architect, Developer, Admin, User
source-git-commit: 1e6460d318f4f9a5dfdcbb81723da01b51b72f3f
workflow-type: tm+mt
source-wordcount: '1491'
ht-degree: 2%

---


# Composant de bouton  {#button-component-adaptive-forms-core-component}

Un bouton d’un formulaire adaptatif est un élément de l’interface utilisateur qui permet aux utilisateurs de lancer une action lorsqu’ils cliquent dessus. L’élément de bouton peut être utilisé pour envoyer un formulaire, réinitialiser un formulaire ou effectuer d’autres actions, comme accéder à une autre page ou déclencher un code personnalisé. Le bouton peut être créé à l’aide du composant principal Bouton .

L’éditeur de règles de Forms adaptatif permet aux utilisateurs de définir diverses actions pour le composant de bouton. Ces actions comprennent l’ouverture d’un site web, l’affichage ou le masquage de composants de formulaire, l’ajout d’une instance d’un panneau ou d’un composant, l’envoi ou la réinitialisation d’un formulaire, etc.

Les Forms adaptatives fournissent également des composants de bouton distincts pour l’envoi ou la réinitialisation d’un formulaire, mais le composant de bouton peut également être configuré pour effectuer ces actions si nécessaire.

Les utilisateurs peuvent accéder à la liste complète des actions prises en charge pour le composant de bouton à l’aide de l’éditeur de règles de Forms adaptatif. L’éditeur de règles permet aux utilisateurs de créer des règles qui sont déclenchées par divers événements, par exemple lorsqu’un utilisateur clique sur un bouton, lorsqu’un formulaire est chargé ou lorsqu’une valeur de champ change. Ces règles peuvent ensuite être utilisées pour effectuer diverses actions, telles que l’affichage ou le masquage de composants, la définition de valeurs de champ ou l’envoi du formulaire.

## Utilisation {#reasons-to-use-button}

Il existe plusieurs raisons pour lesquelles il est bénéfique d’inclure un bouton dans un formulaire adaptatif, notamment :

* **Envoi de formulaire**: Un bouton est généralement utilisé pour envoyer un formulaire, ce qui permet aux utilisateurs d’envoyer les données qu’ils ont saisies au serveur pour traitement.

* **Réinitialisation du formulaire**: Vous pouvez également utiliser des boutons pour réinitialiser un formulaire, effaçant toutes les données saisies par l’utilisateur.

* **Navigation**: Vous pouvez utiliser des boutons pour naviguer entre les différentes sections d’un formulaire ou entre différentes pages d’un site web.

* **Gestion des événements**: Vous pouvez utiliser des boutons pour déclencher différents événements, tels que l’ouverture d’un site web, l’affichage/le masquage de composants, l’ajout d’une instance d’un panneau ou d’un composant au bouton.

* **Interactivité**: Vous pouvez utiliser des boutons pour créer des formulaires interactifs. Par exemple, un bouton peut être utilisé pour ouvrir une boîte de dialogue modale ou pour activer/désactiver une section du formulaire.

## Version et compatibilité {#version-and-compatibility}

Le composant principal de bouton de Forms adaptatif v1 a été publié en février 2023 dans le cadre des composants principaux 2.0.4. Voici un tableau présentant toutes les versions prises en charge, la compatibilité AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible avec<br>[version 2.0.4](/help/versions.md) et plus tard | Compatible | Compatible |

Pour plus d’informations sur les versions et versions des composants principaux, reportez-vous à la section [Versions des composants principaux](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Découvrez les informations les plus récentes sur le composant principal de bouton de Forms adaptatif dans la documentation technique de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/button/v1/button). Pour plus d’informations sur le développement des composants principaux, consultez la section [Documentation destinée aux développeurs sur les composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser votre expérience de bouton pour les visiteurs qui utilisent la boîte de dialogue Configurer . Vous pouvez également définir facilement les propriétés des boutons pour une expérience utilisateur transparente.

### Onglet De base {#basic-tab}

![Onglet De base](/help/adaptive-forms/assets/button_basictab.png)

* **Nom** - Vous pouvez identifier facilement un composant de formulaire avec son nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

* **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

* **Référence de liaison** - Une référence de liaison est une référence à un élément de données stocké dans une source de données externe et utilisé dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client dans un formulaire, en fonction de l’identifiant du client saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur transparente pour la collecte et la gestion des données.

* **Référence de liaison de document d’enregistrement** - Cette option vous permet d’associer un champ Formulaire adaptatif au champ Document d’enregistrement. Lorsque l’utilisateur saisit une valeur dans un champ lié d’un formulaire adaptatif, cette valeur apparaît également dans le champ lié du document d’enregistrement correspondant. Par exemple, une référence de liaison de document d’enregistrement peut être utilisée pour afficher le nom et l’adresse d’un client dans un document d’enregistrement, en fonction de l’identifiant du client saisi dans le formulaire. Ainsi, AEM Forms vous permet de générer un document d’enregistrement et offre une expérience utilisateur transparente pour la collecte et la gestion des données.

* **Masquer le composant** - Sélectionnez l’option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par l’utilisateur.
* **Désactiver le composant** - Sélectionnez l’option pour désactiver le composant. Le composant désactivé n’est pas principal ni modifiable par l’utilisateur final. L’utilisateur peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
* **Lecture seule** - Sélectionnez l’option pour rendre le composant non modifiable. L’utilisateur peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

### Onglet Contenu de l’aide {#help-content}

![Onglet Contenu de l’aide](/help/adaptive-forms/assets/button_helptab.png)

* **Description courte** - Une brève description est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez la variable **Toujours afficher une description courte** pour l’afficher sous le composant.

* **Toujours afficher une description courte** - Activez l’option pour afficher la description courte sous le composant.

* **Texte de l’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur clique sur l’icône d’aide (i) placée en regard du composant. Le texte d’aide fournit des informations plus détaillées que le texte d’étiquette ou d’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Accessibilité {#accessibility}

![Onglet Accessibilité](/help/adaptive-forms/assets/button_accessibilitytab.png)


* **Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisé par les malvoyants. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom et tout message pertinent du champ (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs, y compris ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

Sur le **Accessibilité** , les valeurs sont définies pour [Accessibilité ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) libellés du composant. Plusieurs options sont disponibles pour l’utilisation du texte pour le lecteur d’écran :

* **Texte personnalisé**: Sélectionnez cette option pour utiliser le texte personnalisé pour les étiquettes d’accessibilité ARIA. Cette option affiche la boîte de dialogue Texte personnalisé . Vous pouvez ajouter des informations pertinentes dans la boîte de dialogue Texte personnalisé .
* **Description**: Sélectionnez cette option pour utiliser la description des étiquettes d’accessibilité ARIA.
* **Titre**: Sélectionnez cette option pour utiliser le titre pour les étiquettes d’accessibilité ARIA.
* **Nom**: Sélectionnez cette option pour utiliser le nom des étiquettes d’accessibilité ARIA.
* **Aucun**: Sélectionnez cette option si vous ne souhaitez pas ajouter pour les étiquettes d’accessibilité ARIA.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS du composant de bouton.

### Onglet Styles {#styles-tab}

Le composant principal de bouton Forms adaptatif prend en charge l’AEM [Système de style](/help/get-started/authoring.md#component-styling).

**Classes CSS par défaut**: Vous pouvez fournir une classe CSS par défaut pour le composant principal Bouton de Forms adaptatif .

**Styles autorisés**: Vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé &quot;bold text&quot; et fournir la classe CSS &quot;font-weight: bold&quot;. Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de Forms adaptatif. Pour appliquer un style, dans l’éditeur de Forms adaptatif, sélectionnez le composant auquel vous souhaitez appliquer le style, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans le **Styles** liste déroulante. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

