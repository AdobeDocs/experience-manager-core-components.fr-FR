---
title: Composant principal Adaptive Forms - Groupe de cases à cocher
description: Utilisation ou personnalisation du composant principal Groupe de cases à cocher de Forms adaptatif .
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1683'
ht-degree: 2%

---


# Groupe de cases à cocher {#button-component-adaptive-forms-core-component}

Un groupe de cases à cocher dans un formulaire adaptatif est un ensemble de cases à cocher associées qui permettent aux utilisateurs de sélectionner une ou plusieurs options d’une liste. Chaque case à cocher est représentée par une valeur de données (valeur utilisée pour traiter les éléments d’un groupe de cases à cocher) et une valeur d’affichage (libellé pour chaque élément de case à cocher qui décrit son objectif).

**Exemple**

![](/help/adaptive-forms/assets/checkbox-group.png)

**Boîte de dialogue Propriétés**

![](/help/adaptive-forms/assets/checkbox-group-properties.png)

Dans cet exemple, l’élément Options est utilisé pour regrouper les cases à cocher. Le **Afficher le texte** sert à fournir un libellé pour un élément et **Valeur des données** sert à spécifier la valeur envoyée au serveur lors de l’envoi du formulaire.

Chaque option/élément de case à cocher possède une valeur de données unique et un attribut de texte d’affichage. Si un utilisateur coche les cases &quot;Son&quot; et &quot;Fille&quot;, la valeur de données correspondante est envoyée au serveur lors de l’envoi du formulaire. Ces données peuvent ensuite être traitées par un script côté serveur afin de déterminer quelles options ont été sélectionnées par l’utilisateur. Elles peuvent également être utilisées pour effectuer diverses actions, comme mettre à jour d’autres champs du formulaire ou envoyer les données du formulaire à un script côté serveur en vue d’un traitement ultérieur.

En outre, le groupe de cases à cocher peut être configuré pour avoir différentes valeurs de traitement pour chaque option, et cela peut être défini à l’aide de l’éditeur de règles de Forms adaptatif.

## Utilisation {#reasons-to-use-check-box-group}

Il existe plusieurs raisons pour lesquelles il est bénéfique d’inclure un groupe de cases à cocher dans un formulaire adaptatif, notamment :

* **Sélections multiples**: Un groupe de cases à cocher permet aux utilisateurs de sélectionner plusieurs options dans une liste, ce qui peut s’avérer utile dans les cas où plusieurs sélections sont autorisées ou obligatoires.

* **Expérience utilisateur**: Le groupe de cases à cocher peut être utilisé pour rendre le formulaire plus convivial en offrant une méthode claire et intuitive de sélection de plusieurs options aux utilisateurs.

* **Analyse des données**: Le groupe de cases à cocher peut être utilisé pour collecter des données provenant de diverses sources et les analyser, ou pour les utiliser comme entrée pour un traitement ultérieur.

* **Questionnaires**: Le groupe de cases à cocher peut être utilisé dans les enquêtes pour sélectionner plusieurs options pour une question.

* **Préférences utilisateur**: Le groupe de cases à cocher peut être utilisé pour collecter les préférences de l’utilisateur pour différentes options.

* **Valeur des données**: Le groupe de cases à cocher peut également être utilisé pour traiter les éléments d’un groupe de cases à cocher.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Groupe de cases à cocher Adaptive Forms a été publié en février 2023 dans le cadre de la version 2.0.4 des composants principaux. Voici un tableau présentant toutes les versions prises en charge, la compatibilité AEM et les liens vers la documentation correspondante :

|  |  |
|---|---|
| Version du composant | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatible avec<br>[version 2.0.4](/help/versions.md) et plus tard | Compatible | Compatible |

Pour plus d’informations sur les versions et versions des composants principaux, reportez-vous à la section [Versions des composants principaux](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Obtenez les dernières informations sur le composant principal Groupe de cases à cocher Adaptive Forms dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkboxgroup/v1/checkboxgroup). Pour plus d’informations sur le développement des composants principaux, consultez la section [Documentation destinée aux développeurs sur les composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience de votre case à cocher pour les visiteurs qui utilisent la boîte de dialogue Configurer . Vous pouvez également définir facilement des options de case à cocher pour une expérience utilisateur transparente.


### Onglet De base {#basic-tab}

![Onglet Simple](/help/adaptive-forms/assets/checkbox_basictab.png)

* **Nom** - Le nom identifie de manière unique le composant dans l’éditeur de règles. Les caractères spéciaux et les espaces ne sont pas autorisés dans les chaînes de nom.

* **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

* **Masquer le titre** - Sélectionnez l’option pour masquer le titre du composant.

* **Options** - Vous pouvez ajouter des valeurs de données et afficher des paires de texte à l’aide de la variable **Ajouter** bouton . Une fois qu’une nouvelle option est ajoutée, les actions suivantes peuvent être effectuées :

   * **Valeur des données** - Cette option permet de saisir le contenu à envoyer lorsqu’une option est sélectionnée.
   * **Afficher le texte** - Cette option permet de saisir le contenu à afficher dans un formulaire adaptatif.
   * **Supprimer** - Appuyez ou cliquez sur pour supprimer l’option d’une case à cocher.
   * **Réorganiser** : appuyez ou cliquez dessus et faites glisser pour réorganiser l’ordre des panneaux.

* **Référence de liaison** - Une référence de liaison est une référence à un élément de données stocké dans une source de données externe et utilisé dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client dans un formulaire, en fonction de l’identifiant du client saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur transparente pour la collecte et la gestion des données.

* **Type de données de la valeur envoyée** - Cette option spécifie le type de données de la valeur envoyée lorsqu’une option est sélectionnée. Si la variable **type de données de la valeur envoyée** est défini sur `Number` et d’ajouter des données de chaîne à **Valeur des données** &#x200B; &#x200B; sur le **Options** , l’écran affiche une `Value type mismatch` message d’erreur.

* **Options d’affichage** - Cette option est utilisée pour définir l’alignement visuel des cases à cocher dans un formulaire adaptatif. Les deux options prises en charge sont les suivantes :
   * **Horizontal** - Lorsque cette option est sélectionnée, les cases à cocher s’affichent de gauche à droite dans un formulaire adaptatif.
   * **Vertical** - Lorsque cette option est sélectionnée, les cases à cocher s’affichent de haut en bas dans un formulaire adaptatif.

* **Options par défaut** - Cette option vous permet d’ajouter des valeurs par défaut présélectionnées au chargement du formulaire. Utilisez l’icône Supprimer pour supprimer les options ajoutées. Si la variable **type de données de la valeur envoyée** est défini sur `Number` et d’ajouter des données de chaîne à **Options par défaut**, l’écran affiche une `Value type mismatch` message d’erreur.
* **Masquer le composant** - Sélectionnez l’option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par l’utilisateur.
* **Désactiver le composant** - Sélectionnez l’option pour désactiver le composant. Le composant désactivé n’est pas principal ni modifiable par l’utilisateur final. L’utilisateur peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
* **Lecture seule** - Sélectionnez l’option pour rendre le composant non modifiable. L’utilisateur peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

### Onglet Validation {#validation-tab}

![Onglet Validation](/help/adaptive-forms/assets/checkbox_validationtab.png)

* **Obligatoire** - Sélectionnez cette option si vous souhaitez afficher le composant dans un formulaire adaptatif. Vous ne pouvez pas sélectionner la variable **Masquer le composant** ou **Désactiver le composant**  dans le **De base** lorsque cette option est sélectionnée.

* **Message d’erreur** - Cette option vous permet de saisir un message qui s’affiche si la variable **Obligatoire** est cochée et le champ de formulaire reste vide.

* **Message de validation de script** - Cette option permet de saisir un message à afficher en cas d’échec de la validation du script.

### Onglet Contenu de l’aide {#helpcontent-tab}

![Onglet Contenu de l’aide](/help/adaptive-forms/assets/checkbox_helptab.png)

* **Description courte** - Une brève description est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez la variable **Toujours afficher une description courte** pour l’afficher sous le composant.

* **Toujours afficher une description courte** - Activez l’option pour afficher la description courte sous le composant.

* **Texte de l’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur clique sur l’icône d’aide (i) placée en regard du composant. Le texte d’aide fournit des informations plus détaillées que le texte d’étiquette ou d’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility-tab}

![Onglet Accessibilité](/help/adaptive-forms/assets/checkbox_accessibility.png)

Sur le **Accessibilité** , les valeurs sont définies pour [Accessibilité ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) libellés du composant. Plusieurs options sont disponibles pour l’utilisation du texte pour le lecteur d’écran :

* **Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisé par les malvoyants. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom et tout message pertinent du champ (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs, y compris ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

   * **Texte personnalisé**: Sélectionnez cette option pour utiliser le texte personnalisé pour les étiquettes d’accessibilité ARIA. Cette option affiche la boîte de dialogue Texte personnalisé . Vous pouvez ajouter des informations pertinentes dans la boîte de dialogue Texte personnalisé .

   * **Titre**: Sélectionnez cette option pour utiliser le titre pour les étiquettes d’accessibilité ARIA.


## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS du composant Groupe de cases à cocher.

### Onglet Styles {#styles-tab}

Le composant principal Groupe de cases à cocher Adaptive Forms prend en charge l’AEM [Système de style](/help/get-started/authoring.md#component-styling).

**Classes CSS par défaut**: Vous pouvez fournir une classe CSS par défaut pour le composant principal Groupe de cases à cocher du Forms adaptatif .

**Styles autorisés**: Vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé &quot;bold text&quot; et fournir la classe CSS &quot;font-weight: bold&quot;. Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de Forms adaptatif. Pour appliquer un style, dans l’éditeur de Forms adaptatif, sélectionnez le composant auquel vous souhaitez appliquer le style, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans le **Styles** liste déroulante. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

