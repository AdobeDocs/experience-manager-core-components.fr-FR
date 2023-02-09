---
title: Composant principal Adaptive Forms - Entrée téléphonique
description: Utilisation ou personnalisation du composant principal d’entrée Téléphone Forms adaptatif .
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1698'
ht-degree: 1%

---


# Entrée téléphonique {#telephone-input-adaptive-forms-core-component}

Le composant principal d’entrée téléphonique du formulaire adaptatif permet aux utilisateurs de saisir un numéro de téléphone. Le champ de saisie téléphonique affiche les claviers sur les appareils mobiles qui correspondent aux numéros de téléphone. Il peut être personnalisé avec des attributs supplémentaires tels que &quot;motif&quot; et &quot;espace réservé&quot; pour spécifier le format et la description du numéro de téléphone.

Le champ de saisie téléphonique est généralement utilisé dans les formulaires de contact, les formulaires d&#39;enregistrement et autres formulaires où un numéro de téléphone est requis pour le contact. Le champ de saisie téléphonique peut également être utilisé pour s’assurer que l’utilisateur saisit un numéro de téléphone valide, car le navigateur peut imposer certaines contraintes, telles que la longueur et le format du numéro de téléphone, en fonction de l’attribut &quot;pattern&quot;.

## Utilisation {#reasons-to-use-telephone-input}

Les raisons courantes d’utiliser un champ de saisie téléphonique dans un formulaire adaptatif sont les suivantes :

* **Coordonnées**: Un champ de saisie téléphonique est généralement utilisé pour recueillir le numéro de téléphone d’un utilisateur comme moyen de contact.

* **Exactitude des données améliorée**: En utilisant un champ de saisie téléphonique, le formulaire peut imposer certaines contraintes sur le format du numéro de téléphone, ce qui permet de s&#39;assurer que les données saisies sont exactes et complètes.

* **Meilleure expérience utilisateur**: Un champ de saisie téléphonique permet aux utilisateurs d’entrer leur numéro de téléphone de manière claire et intuitive. Il permet également d’améliorer leur expérience en leur permettant de saisir rapidement et facilement leurs coordonnées.

## Version et compatibilité {#version-and-compatibility}

Le composant principal d’entrée Téléphone du Forms adaptatif a été publié en février 2023 dans le cadre des composants principaux 2.0.4. Voici un tableau présentant toutes les versions prises en charge, la compatibilité AEM et les liens vers la documentation correspondante :

|  |  |
|---|---|
| Version du composant | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatible avec<br>[version 2.0.4](/help/versions.md) et plus tard | Compatible | Compatible |

Pour plus d’informations sur les versions et versions des composants principaux, reportez-vous à la section [Versions des composants principaux](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Obtenez les dernières informations sur le composant principal d’entrée Téléphone de Forms adaptatif dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/telephoneinput/v1/telephoneinput). Pour plus d’informations sur le développement des composants principaux, consultez la section [Documentation destinée aux développeurs sur les composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser votre expérience d’entrée Téléphone pour les visiteurs à l’aide de la boîte de dialogue Configurer . Vous pouvez également définir facilement des options de saisie téléphonique pour une expérience utilisateur fluide.

![Onglet De base](/help/adaptive-forms/assets/telephoneinput_basictab.png)

* **Nom** - Vous pouvez identifier facilement un composant de formulaire avec son nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

* **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

* **Masquer le titre** - Sélectionnez l’option pour masquer le titre du composant.

* **Texte d’espace réservé** - Le texte d’espace réservé dans un composant de formulaire fait référence à un libellé court ou à une invite qui apparaît dans un champ de saisie comme conseil à l’utilisateur sur le type d’information à saisir dans ce champ. Le texte d’espace réservé disparaît lorsque l’utilisateur commence à saisir du texte dans le champ et réapparaît si le champ est vide. Il fournit un indice visuel à l’utilisateur, mais n’agit pas comme une étiquette ou une valeur permanente pour le champ.

* **Référence de liaison** - Une référence de liaison est une référence à un élément de données stocké dans une source de données externe et utilisé dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client dans un formulaire, en fonction de l’identifiant du client saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur transparente pour la collecte et la gestion des données.

* **Masquer le composant** - Sélectionnez l’option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par l’utilisateur.

* **Désactiver le composant** - Sélectionnez l’option pour désactiver le composant. Le composant désactivé n’est pas principal ni modifiable par l’utilisateur final. L’utilisateur peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

* **Lecture seule** - Sélectionnez l’option pour rendre le composant non modifiable. L’utilisateur peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

* **Valeur par défaut** - Cette option vous permet d’ajouter une valeur par défaut dans un champ de formulaire. If **Composant désactivé** ou **Composant en lecture seule** est sélectionnée, la valeur par défaut s’affiche à l’écran. Si aucune valeur n’est saisie par l’utilisateur dans le champ de formulaire, cette valeur est envoyée au moment de l’envoi du formulaire.

### Onglet Validation {#validation-tab}

![Onglet Validation](/help/adaptive-forms/assets/telephoneinput_validationtab.png)

* **Obligatoire** - Sélectionnez cette option si vous souhaitez afficher le composant dans un formulaire adaptatif. Vous ne pouvez pas sélectionner la variable **Masquer le composant** ou **Désactiver le composant**  dans le **De base** lorsque cette option est sélectionnée.

* **Message d’erreur** - Cette option vous permet de saisir un message qui s’affiche si la variable **Obligatoire** est cochée et le champ n’est pas renseigné.

* **Message de validation de script** - Cette option permet de saisir un message à afficher en cas d’échec de la validation du script.

* **Nombre maximal de caractères** - Cette option vous permet de spécifier le nombre maximal de caractères autorisés dans le composant. Si vous saisissez des caractères supérieurs à la valeur spécifiée dans **Nombre maximal de caractères**, un message d’erreur s’affiche à l’écran. Le **Message d’erreur de caractères maximum** vous permet d’ajouter un message d’erreur personnalisé.

* **Message d’erreur de caractères maximum** - Le **Message d’erreur de caractères maximum** vous permet d’ajouter un message d’erreur personnalisé si vous saisissez des caractères supérieurs à la valeur spécifiée dans la variable **Nombre maximal de caractères** .

* **Nombre minimum de caractères** - Cette option permet de spécifier le nombre minimum de caractères autorisés dans le champ. Si vous saisissez des caractères inférieurs à la valeur spécifiée dans **Nombre minimum de caractères**, un message d’erreur s’affiche à l’écran. Le **Message d’erreur de caractères minimum** vous permet d’ajouter un message d’erreur personnalisé.

* *Message d’erreur de caractères minimum** - La variable **Message d’erreur de caractères minimum** vous permet d’ajouter un message d’erreur personnalisé si vous saisissez des caractères inférieurs à la valeur spécifiée dans la variable **Nombre minimum de caractères** .

Le **Modèle de validation** permet de saisir un modèle pour valider le numéro de téléphone renseigné. Le numéro de téléphone renseigné est validé par rapport à la valeur renseignée dans la variable **Modèle** . Si le numéro de téléphone n’est pas validé avec la valeur saisie dans **Modèle** , le message d’erreur s’affiche à l’écran.

* **Modèle** - Cette option vous permet de saisir les modèles de vérification autorisés pour les numéros de téléphone. Les expressions régulières sont également autorisées.

* **Message d’erreur** - Cette option permet de saisir un message qui s&#39;affiche à l&#39;écran si le numéro de téléphone saisi n&#39;est pas validé avec la valeur saisie dans la variable **Modèle** option

### Onglet Contenu de l’aide {#help-content-tab}

![Onglet Contenu de l’aide](/help/adaptive-forms/assets/telephoneinput_helptab.png)

* **Description courte** - Une brève description est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez la variable **Toujours afficher une description courte** pour l’afficher sous le composant.

* **Toujours afficher une description courte** - Activez l’option pour afficher la description courte sous le composant.

* **Texte de l’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur clique sur l’icône d’aide (i) placée en regard du composant. Le texte d’aide fournit des informations plus détaillées que le texte d’étiquette ou d’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility-tab}

![Onglet Accessibilité](/help/adaptive-forms/assets/telephoneinput_accessibilitytab.png)

* **Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisé par les malvoyants. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom et tout message pertinent du champ (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs, y compris ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.


## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS pour le composant d’entrée Téléphone.

### Onglet Styles {#styles-tab}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS d’un composant. Le composant principal d’entrée Téléphone de Forms adaptatif prend en charge l’AEM [Système de style](/help/get-started/authoring.md#component-styling).

**Classes CSS par défaut**: Vous pouvez fournir une classe CSS par défaut pour le composant principal d’entrée Téléphone du Forms adaptatif.

**Styles autorisés**: Vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé &quot;bold text&quot; et fournir la classe CSS &quot;font-weight: bold&quot;. Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de Forms adaptatif. Pour appliquer un style, dans l’éditeur de Forms adaptatif, sélectionnez le composant auquel vous souhaitez appliquer le style, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans le **Styles** liste déroulante. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

### Onglet Formats {#format-tab}

L’onglet Formats vous permet de définir des formats de nombres par défaut et personnalisés.
