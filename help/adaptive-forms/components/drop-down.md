---
title: Composant principal Forms adaptatif - Liste déroulante
description: Utilisation ou personnalisation du composant principal de liste déroulante Forms adaptative.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1673'
ht-degree: 1%

---


# Liste déroulante {#drop-down-list-adaptive-forms-core-component}

Une liste déroulante dans un formulaire adaptatif permet aux utilisateurs de sélectionner une ou plusieurs options dans une liste d’options prédéfinies. Les options peuvent être de type Chaîne, Nombre ou Valeur booléenne. En outre, le composant Liste déroulante peut être configuré pour avoir différentes valeurs de validation et par défaut.

**Exemple**
![](/help/adaptive-forms/assets/drop-down-list.png)

## Utilisation {#reasons-to-use-drop-down-list}

Il existe plusieurs raisons pour lesquelles il est bénéfique d’inclure une liste déroulante dans un formulaire adaptatif, notamment :

* **Longue liste d’options**: Les listes déroulantes sont utiles dans les cas où une longue liste d’options est disponible pour un champ. Ils occupent moins d’espace sur le formulaire qu’une liste de boutons radio ou de cases à cocher, et peuvent être moins envahissants pour les utilisateurs.

* **Cohérence**: Les listes déroulantes offrent une cohérence dans la conception et la disposition du formulaire, ce qui rend la navigation plus intuitive et plus facile pour les utilisateurs.

* **Clarité**: Les listes déroulantes peuvent rendre le formulaire plus clair et plus facile à comprendre en fournissant une liste claire et concise d’options.

* **Expérience utilisateur**: Les listes déroulantes peuvent être utilisées pour rendre le formulaire plus convivial en offrant une méthode claire et intuitive de sélection des options aux utilisateurs.

* **Analyse des données**: Les listes déroulantes peuvent être utilisées pour collecter des données provenant de diverses sources et les analyser ou les utiliser comme entrées pour un traitement ultérieur.


**Boîte de dialogue Propriétés**

![](/help/adaptive-forms/assets/drop-down-list-properties.png)

Dans cet exemple, l’élément Options est utilisé pour définir les éléments de liste. Le **Afficher le texte** sert à fournir un libellé aux éléments de liste et **Valeur des données** sert à spécifier la valeur envoyée au serveur lors de l’envoi du formulaire.

Chaque option de liste déroulante possède une valeur de données unique et un attribut Texte d’affichage . Si un utilisateur sélectionne l’option &quot;Rouge&quot;, la valeur de données correspondante est envoyée au serveur lors de l’envoi du formulaire. Ces données peuvent ensuite être traitées par un script côté serveur afin de déterminer quelles options ont été sélectionnées par l’utilisateur. Elles peuvent également être utilisées pour effectuer diverses actions, comme mettre à jour d’autres champs du formulaire ou envoyer les données du formulaire à un script côté serveur en vue d’un traitement ultérieur.

En outre, la liste déroulante peut être configurée pour avoir des valeurs de traitement différentes pour chaque option, et cela peut être défini à l’aide de l’éditeur de règles de Forms adaptatif.

## Version et compatibilité {#version-and-compatibility}

La liste déroulante des composants principaux de Forms adaptatif a été publiée en février 2023 dans le cadre de la version 2.0.4 des composants principaux. Voici un tableau présentant toutes les versions prises en charge, la compatibilité AEM et les liens vers la documentation correspondante :

|  |  |
|---|---|
| Version du composant | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatible avec<br>[version 2.0.4](/help/versions.md) et plus tard | Compatible | Compatible |

Pour plus d’informations sur les versions et versions des composants principaux, reportez-vous à la section [Versions des composants principaux](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Obtenez les informations les plus récentes sur le composant principal de liste déroulante Forms adaptative dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/dropdown/v1/dropdown). Pour plus d’informations sur le développement des composants principaux, consultez la section [Documentation destinée aux développeurs sur les composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser votre expérience de liste déroulante pour les visiteurs qui utilisent la boîte de dialogue Configurer . Vous pouvez également définir facilement des options de liste déroulante pour une expérience utilisateur transparente.

![Onglet Simple](/help/adaptive-forms/assets/dropdown_basictab.png)

* **Nom** - Vous pouvez identifier facilement un composant de formulaire avec son nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

* **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

* **Masquer le titre** - Sélectionnez l’option pour masquer le titre du composant.

* **Autoriser la sélection multiple** - Sélectionnez cette option pour sélectionner plusieurs options dans une liste déroulante.

* **Enregistrer la valeur sous** - Cette option spécifie le type de données de la valeur envoyée lorsqu’une option est sélectionnée. Si la variable **Enregistrer la valeur sous** est défini sur `Number` et d’ajouter des données de chaîne à **Valeur des données** &#x200B; &#x200B; sur le **Options** , l’écran affiche une `Value type mismatch` message d’erreur.

   Dans le **Options** , vous pouvez ajouter des valeurs de données et afficher des paires de texte à l’aide de l’onglet **Ajouter** bouton . Une fois qu’une nouvelle option est ajoutée, les actions suivantes sont effectuées :

   * **Valeur des données** - Cette option permet de saisir le contenu à envoyer lorsqu’une option est sélectionnée.
   * **Afficher le texte** - Cette option permet de saisir le contenu à afficher dans un formulaire adaptatif.
   * **Supprimer** - Appuyez ou cliquez sur pour supprimer l’option d’un menu déroulant .
   * **Réorganiser** - Appuyez ou cliquez dessus et faites glisser pour réorganiser l’ordre de l’option d’un menu déroulant.

* **Options par défaut** - Cette option vous permet d’ajouter des valeurs par défaut. Utilisez l’icône Supprimer pour supprimer l’option ajoutée. Si la variable **Enregistrer la valeur sous** est défini sur `Number` et d’ajouter des données de chaîne à **Options par défaut**, l’écran affiche une `Value type mismatch` message d’erreur.

* **Texte d’espace réservé** - Le texte d’espace réservé dans un composant de formulaire fait référence à un libellé court ou à une invite qui apparaît dans un champ de saisie comme conseil à l’utilisateur sur le type d’information à saisir dans ce champ. Le texte d’espace réservé disparaît lorsque l’utilisateur commence à saisir du texte dans le champ et réapparaît si le champ est vide. Il fournit un indice visuel à l’utilisateur, mais n’agit pas comme une étiquette ou une valeur permanente pour le champ.

* **Référence de liaison** - Une référence de liaison est une référence à un élément de données stocké dans une source de données externe et utilisé dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client dans un formulaire, en fonction de l’identifiant du client saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur transparente pour la collecte et la gestion des données.

* **Masquer le composant** - Sélectionnez l’option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par l’utilisateur.
* **Désactiver le composant** - Sélectionnez l’option pour désactiver le composant. Le composant désactivé n’est pas principal ni modifiable par l’utilisateur final. L’utilisateur peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
* **Lecture seule** - Sélectionnez l’option pour rendre le composant non modifiable. L’utilisateur peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

### Onglet Validation {#validation-tab}

![Onglet Validation](/help/adaptive-forms/assets/dropdown_validationtab.png)

* **Obligatoire** - Sélectionnez cette option si vous souhaitez afficher le composant dans un formulaire adaptatif. Vous ne pouvez pas sélectionner la variable **Masquer le composant** ou **Désactiver le composant**  dans le **De base** lorsque cette option est sélectionnée.

* **Message d’erreur** - Cette option vous permet de saisir un message qui s’affiche si la variable **Obligatoire** est cochée et le champ de formulaire reste vide.

* **Message de validation de script** - Cette option permet de saisir un message à afficher en cas d’échec de la validation du script.

### Onglet Contenu de l’aide {#help-content-tab}

![Onglet Contenu de l’aide](/help/adaptive-forms/assets/dropdown_helptab.png)

* **Description courte** - Une brève description est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez la variable **Toujours afficher une description courte** pour l’afficher sous le composant.

* **Toujours afficher une description courte** - Activez l’option pour afficher la description courte sous le composant.

* **Texte de l’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur clique sur l’icône d’aide (i) placée en regard du composant. Le texte d’aide fournit des informations plus détaillées que le texte d’étiquette ou d’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility-tab}

![Onglet Accessibilité](/help/adaptive-forms/assets/dropdown_accessibilitytab.png)

* **Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisé par les malvoyants. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom et tout message pertinent du champ (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs, y compris ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS pour le composant Liste déroulante.


### Onglet Styles {#styles-tab}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS d’un composant. La liste déroulante des composants principaux de Forms adaptatif prend en charge l’AEM [Système de style](/help/get-started/authoring.md#component-styling).

**Classes CSS par défaut**: Vous pouvez fournir une classe CSS par défaut pour le composant principal de la liste déroulante Forms adaptative.

**Styles autorisés**: Vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé &quot;bold text&quot; et fournir la classe CSS &quot;font-weight: bold&quot;. Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de Forms adaptatif. Pour appliquer un style, dans l’éditeur de Forms adaptatif, sélectionnez le composant auquel vous souhaitez appliquer le style, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans le **Styles** liste déroulante. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.


