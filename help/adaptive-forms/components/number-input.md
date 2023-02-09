---
title: Composant principal Adaptive Forms - Entrée de numéro
description: Utilisation ou personnalisation du composant principal d’entrée Numéro de Forms adaptatif .
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1780'
ht-degree: 1%

---


# Entrée numérique {#number-input-adaptive-forms-core-component}

Un composant de saisie numérique dans un formulaire adaptatif est un type de champ de formulaire qui permet aux utilisateurs de saisir des valeurs numériques. Le composant est généralement représenté par un champ de texte avec une flèche vers le haut et vers le bas pour incrémenter et décrémenter le nombre.

Il peut également être utilisé avec des attributs tels que min, max, step, value, etc. Ces attributs peuvent être utilisés pour définir les valeurs minimale et maximale autorisées dans le champ, l’intervalle d’étape pour incrémenter ou décrémenter le nombre et la valeur par défaut du champ.

Ce composant peut être utilisé pour collecter des données numériques telles que l’âge, la quantité, etc. et peuvent également être utilisés pour effectuer des opérations mathématiques comme l’addition et la soustraction. Ce composant peut également être utilisé pour valider les données numériques saisies par l’utilisateur.

Pour l’accessibilité, il est important de spécifier un &quot;libellé&quot; qui décrit l’objectif du champ de saisie numérique et le type d’entrée attendu.

**Exemple**

![](/help/adaptive-forms/assets/numeric-stepper.png)

## Utilisation {#reasons-to-use-number-input-numeric-stepper}

Il existe plusieurs raisons pour lesquelles il est bénéfique d’inclure un composant d’entrée numérique dans un formulaire adaptatif, notamment :

* **Opérations mathématiques**: Les champs numériques peuvent être utilisés pour effectuer des opérations mathématiques telles que l’addition, la soustraction, la multiplication et la division.

* **Plage de données**: Les champs numériques peuvent être utilisés pour définir une plage de valeurs valides à l’aide des attributs min, max et step.

* **Contenu dynamique**: Un composant numérique peut être utilisé pour afficher des données dynamiques en fonction des champs du formulaire.


## Version et compatibilité {#version-and-compatibility}

Le composant principal d’entrée Numéro de Forms adaptatif a été publié en février 2023 dans le cadre des composants principaux 2.0.4. Voici un tableau présentant toutes les versions prises en charge, la compatibilité AEM et les liens vers la documentation correspondante :

|  |  |
|---|---|
| Version du composant | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatible avec<br>[version 2.0.4](/help/versions.md) et plus tard | Compatible | Compatible |

Pour plus d’informations sur les versions et versions des composants principaux, reportez-vous à la section [Versions des composants principaux](/help/versions.md) document.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Obtenez les dernières informations sur le composant principal d’entrée Numéro de Forms adaptatif dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/numberinput/v1/numberinput). Pour plus d’informations sur le développement des composants principaux, consultez la section [Documentation destinée aux développeurs sur les composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser votre expérience d’entrée numérique pour les visiteurs à l’aide de la boîte de dialogue Configurer . Vous pouvez également définir facilement des options de saisie numérique pour une expérience utilisateur transparente.

### Onglet De base {#basic-tab}

![Onglet De base](/help/adaptive-forms/assets/numberinput_basictab.png)

* **Nom** - Vous pouvez identifier facilement un composant de formulaire avec son nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

* **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

* **Masquer le titre** - Sélectionnez l’option pour masquer le titre du composant.

* **Texte d’espace réservé** - Le texte d’espace réservé dans un composant de formulaire fait référence à un libellé court ou à une invite qui apparaît dans un champ de saisie comme conseil à l’utilisateur sur le type d’information à saisir dans ce champ. Le texte d’espace réservé disparaît lorsque l’utilisateur commence à saisir du texte dans le champ et réapparaît si le champ est vide. Il fournit un indice visuel à l’utilisateur, mais n’agit pas comme une étiquette ou une valeur permanente pour le champ.
* **Référence de liaison** - Une référence de liaison est une référence à un élément de données stocké dans une source de données externe et utilisé dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client dans un formulaire, en fonction de l’identifiant du client saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur transparente pour la collecte et la gestion des données.
* **Masquer le composant** - Sélectionnez l’option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par l’utilisateur.
* **Désactiver le composant** - Sélectionnez l’option pour désactiver le composant. Le composant désactivé n’est pas principal ni modifiable par l’utilisateur final. L’utilisateur peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
* **Lecture seule** - Sélectionnez l’option pour rendre le composant non modifiable. L’utilisateur peut voir la valeur du champ mais ne peut pas le modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
* **Type de nombre** - Cette option permet de sélectionner le type de valeurs numériques &#x200B; champ de formulaire autorisé. Vous pouvez sélectionner les types Décimal ou Entier dans le menu déroulant.
* **Valeur par défaut** - Cette option vous permet d’ajouter une valeur par défaut dans un champ de formulaire. If **Composant désactivé** ou **Composant en lecture seule** est sélectionnée, la valeur par défaut s’affiche à l’écran. Si aucune valeur n’est saisie par l’utilisateur dans le champ de formulaire, cette valeur est envoyée au moment de l’envoi du formulaire.

### Onglet Validation {#validation-tab}

![Onglet Validation](/help/adaptive-forms/assets/numberinput_validationtab.png)

* **Obligatoire** - Sélectionnez cette option si vous souhaitez afficher le composant dans un formulaire adaptatif. Vous ne pouvez pas sélectionner la variable **Masquer le composant** ou **Désactiver le composant**  dans le **De base** lorsque cette option est sélectionnée.

* **Message d’erreur** - Cette option vous permet de saisir un message qui s’affiche si la variable **Obligatoire** est cochée et le champ n’est pas renseigné.

* **Message de validation de script** - Cette option permet de saisir un message à afficher en cas d’échec de la validation du script.

* **Numéro le plus bas / Numéro le plus petit** - Utilisez cette option pour sélectionner le nombre minimum autorisé à renseigner dans le champ de formulaire. Si la valeur est inférieure au nombre spécifié dans **Numéro le plus bas / Numéro le plus petit** est saisie dans le champ de formulaire, le message d’erreur s’affiche.

* **Message d’erreur minimal** - Cette option vous permet de saisir un message d’erreur qui s’affiche lorsque l’utilisateur saisit une valeur inférieure à celle spécifiée dans la variable **Nombre minimum/Nombre minimum** .

* **Exclure la valeur minimale** - Cochez cette case si vous ne souhaitez pas que la valeur minimale indiquée dans la variable **Numéro le plus bas / Numéro le plus petit** à inclure dans la plage de valeurs &#x200B; à renseigner dans le champ du formulaire.

* **Nombre le plus élevé / Nombre le plus grand** - Utilisez cette option pour sélectionner le nombre maximal autorisé à renseigner dans le champ de formulaire. Si le nombre est supérieur au nombre spécifié dans **Nombre le plus élevé / Nombre le plus grand** est saisie dans le champ de formulaire, le message d’erreur s’affiche.

* **Message d’erreur maximum** - Cette option vous permet de saisir un message d’erreur qui s’affiche lorsque l’utilisateur saisit une valeur supérieure à celle spécifiée dans la variable **Nombre le plus élevé / Nombre le plus grand** .

* **Exclure la valeur maximale** - Cochez cette case si vous ne souhaitez pas que la valeur maximale indiquée dans la variable **Nombre le plus élevé / Nombre le plus grand** à inclure dans la plage de valeurs à renseigner dans le champ du formulaire.

### Onglet Contenu de l’aide {#help-content}

![Onglet Contenu de l’aide](/help/adaptive-forms/assets/numberinput_helptab.png)

* **Description courte** - Une brève description est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez la variable **Toujours afficher une description courte** pour l’afficher sous le composant.

* **Toujours afficher une description courte** - Activez l’option pour afficher la description courte sous le composant.

* **Texte de l’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur clique sur l’icône d’aide (i) placée en regard du composant. Le texte d’aide fournit des informations plus détaillées que le texte d’étiquette ou d’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility}

![Onglet Accessibilité](/help/adaptive-forms/assets/numberinput_accessibility.png)

* **Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisé par les malvoyants. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom et tout message pertinent du champ (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs, y compris ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

### Onglet Formats {#formats-tab}

![Onglet Accessibilité](/help/adaptive-forms/assets/numberinput_formattab.png)


* **Format d’affichage** - Cette option vous permet de sélectionner une option dans différents formats de types numériques entiers pour l’affichage. Lorsque l’utilisateur sélectionne une option dans la variable **Type** , le menu déroulant **Format** devient visible dans le panneau. Vous pouvez choisir un format spécifique dans lequel les nombres s’affichent pour l’utilisateur.

* **Nombre de chiffres avant le séparateur décimal (1234.000)** - Utilisez cette option pour spécifier le nombre de chiffres à afficher avant la décimale.

* **Nombre de chiffres après le séparateur décimal (1234.000)** - Utilisez cette option pour spécifier le nombre de chiffres à afficher après la virgule.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS pour le composant d’entrée Number.


### Onglet Styles {#styles-tab}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS d’un composant. Le composant principal d’entrée Numéro de Forms adaptatif prend en charge l’AEM [Système de style](/help/get-started/authoring.md#component-styling).

**Classes CSS par défaut**: Vous pouvez fournir une classe CSS par défaut pour le composant principal d’entrée Numéro de Forms adaptatif.

**Styles autorisés**: Vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé &quot;bold text&quot; et fournir la classe CSS &quot;font-weight: bold&quot;. Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de Forms adaptatif. Pour appliquer un style, dans l’éditeur de Forms adaptatif, sélectionnez le composant auquel vous souhaitez appliquer le style, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans le **Styles** liste déroulante. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

### Onglet Formats {#format-tab}

L’onglet Formats vous permet de définir des formats de nombres par défaut et personnalisés.
