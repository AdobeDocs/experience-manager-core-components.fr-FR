---
title: Composant principal Forms adaptatif - Saisie de texte (zone de texte)
description: Utilisation ou personnalisation du composant principal d’entrée de texte Forms adaptatif .
role: Architect, Developer, Admin, User
exl-id: 49d9fe69-0578-4489-beaa-a18cdb14add7
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '1750'
ht-degree: 1%

---

# Saisie de texte (zone de texte) {#text-input-adaptive-forms-core-component}

Un composant de saisie de texte (zone de texte) permet à l’utilisateur de saisir et de modifier une ou plusieurs lignes de texte, selon l’attribut type de l’élément de saisie. Le composant de saisie de texte peut être placé dans un formulaire et est généralement étiqueté avec un texte utile qui identifie facilement son objectif. Il s’agit d’un élément fondamental de tout formulaire, largement utilisé pour collecter différents types de données auprès des utilisateurs. Ces éléments sont simples, flexibles et peuvent être configurés pour valider les entrées et améliorer la précision de la collecte de données.


**Exemple**

![](/help/adaptive-forms/assets/text-input.png)


## Utilisation {#reasons-to-use-text-input-field}

Il existe plusieurs raisons d’utiliser le composant de saisie de texte dans un formulaire adaptatif :

* **Collecte de données**: Les champs de saisie de texte sont l’un des éléments de formulaire les plus courants pour collecter un large éventail d’informations auprès des utilisateurs, tels que les noms, adresses électroniques, numéros de téléphone et autres types de données textuelles.

* **convivial**: Les champs de saisie de texte sont simples et faciles à utiliser, ce qui permet aux utilisateurs de saisir et de modifier facilement du texte.

* **Flexibilité**: Les champs de saisie de texte peuvent être utilisés pour collecter un large éventail d’informations, depuis les entrées de texte courtes sur une seule ligne jusqu’aux entrées de texte plus longues sur plusieurs lignes.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Accordéon de Forms adaptatif a été publié en février 2023 dans le cadre des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Voici un tableau de toutes les versions prises en charge, de la compatibilité AEM et des liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec<br>[version 2.0.4](/help/adaptive-forms/version.md) et plus tard | Compatible avec<br>[version 1.1.12](/help/adaptive-forms/version.md) et plus tard, mais moins de 2.0.0. |

Pour plus d’informations sur les versions et versions des composants principaux, reportez-vous à la section [Versions des composants principaux](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Obtenez les dernières informations sur les onglets de Forms adaptatif sur le composant principal supérieur dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput). Pour plus d’informations sur le développement des composants principaux, consultez la section [Documentation destinée aux développeurs sur les composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser votre expérience de saisie de texte pour les visiteurs qui utilisent la boîte de dialogue Configurer . Vous pouvez également définir facilement des options de saisie de texte pour une expérience utilisateur fluide.

![Onglet De base](/help/adaptive-forms/assets/textinput_basictab.png)

* **Nom** - Vous pouvez identifier facilement un composant de formulaire avec son nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

* **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

* **Masquer le titre** - Sélectionnez l’option pour masquer le titre du composant.

* **Texte d’espace réservé** - Le texte d’espace réservé dans un composant de formulaire fait référence à un libellé court ou à une invite qui apparaît dans un champ de saisie comme conseil à l’utilisateur sur le type d’information à saisir dans ce champ. Le texte d’espace réservé disparaît lorsque l’utilisateur commence à saisir du texte dans le champ et réapparaît si le champ est vide. Il fournit un indice visuel à l’utilisateur, mais n’agit pas comme une étiquette ou une valeur permanente pour le champ.

* **Référence de liaison** - Une référence de liaison est une référence à un élément de données stocké dans une source de données externe et utilisé dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client dans un formulaire, en fonction de l’identifiant du client saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur transparente pour la collecte et la gestion des données.

* **Masquer le composant** - Sélectionnez l’option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par l’utilisateur.

* **Désactiver le composant** - Sélectionnez l’option pour désactiver le composant. Le composant désactivé n’est pas principal ni modifiable par l’utilisateur final. L’utilisateur peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

* **Lecture seule** - Sélectionnez l’option pour rendre le composant non modifiable. L’utilisateur peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

* **Valeur par défaut** - Cette option vous permet d’ajouter une valeur par défaut dans un champ de formulaire. Le texte disparaît lorsque l’utilisateur commence à saisir du texte dans le champ. If **Composant désactivé** ou **Composant en lecture seule** est sélectionnée, la valeur par défaut s’affiche à l’écran. Si aucune valeur n’est saisie par l’utilisateur dans le champ de formulaire, cette valeur est envoyée au moment de l’envoi du formulaire.

* **Permettre des lignes multiples** - Cette option permet à l’utilisateur de saisir plusieurs lignes dans un champ de formulaire.

* **Autoriser le texte enrichi** - La boîte de dialogue de modification fournit des outils de mise en forme de texte enrichi standard qui permettent à l’utilisateur de mettre du texte en forme.

* **Attribut de remplissage automatique** - L’option de remplissage automatique remplit le champ de formulaire selon un modèle ou un texte saisi précédemment. Lorsque l’utilisateur commence à saisir du texte dans le champ de formulaire, les suggestions s’affichent dans une liste déroulante à partir de laquelle il peut sélectionner l’option appropriée.

### Onglet Validation {#validation-tab}

![Onglet Validation](/help/adaptive-forms/assets/textinput_validationtab.png)

* **Obligatoire** - Sélectionnez cette option si vous souhaitez afficher le composant dans un formulaire adaptatif. Vous ne pouvez pas sélectionner la variable **Masquer le composant** ou **Désactiver le composant**  dans le **De base** lorsque cette option est sélectionnée.

* **Message d’erreur** - Cette option vous permet de saisir un message qui s’affiche si la variable **Obligatoire** est cochée et le champ n’est pas renseigné.

* **Message de validation de script** - Cette option permet de saisir un message à afficher en cas d’échec de la validation du script.

* **Nombre maximal de caractères** - Cette option vous permet de spécifier le nombre maximal de caractères autorisés dans le composant. Si vous saisissez des caractères supérieurs à la valeur spécifiée dans **Nombre maximal de caractères**, un message d’erreur s’affiche à l’écran. Le **Message d’erreur de caractères maximum** vous permet d’ajouter un message d’erreur personnalisé.

* **Message d’erreur de caractères maximum** - Le **Message d’erreur de caractères maximum** vous permet d’ajouter un message d’erreur personnalisé si vous saisissez des caractères supérieurs à la valeur spécifiée dans la variable **Nombre maximal de caractères** .

* **Nombre minimum de caractères** - Cette option permet de spécifier le nombre minimum de caractères autorisés dans le champ. Si vous saisissez des caractères inférieurs à la valeur spécifiée dans **Nombre minimum de caractères**, un message d’erreur s’affiche à l’écran. Le **Message d’erreur de caractères minimum** vous permet d’ajouter un message d’erreur personnalisé.

* **Message d’erreur de caractères minimum** - Le **Message d’erreur de caractères minimum** vous permet d’ajouter un message d’erreur personnalisé si vous saisissez des caractères inférieurs à la valeur spécifiée dans la variable **Nombre minimum de caractères** .

Le **Modèle de validation** vous permet de saisir un modèle pour valider le texte saisi. Si la validation du texte échoue avec la valeur saisie dans **Modèle** , le message d’erreur s’affiche à l’écran.

* **Modèle** - Cette option vous permet de saisir les modèles de vérification autorisés pour le texte. Les expressions régulières sont également autorisées.

* **Message d’erreur** - Cette option permet de saisir un message qui s&#39;affiche à l&#39;écran si la validation du texte saisi échoue avec la valeur saisie dans la variable **Modèle** option

### Onglet Contenu de l’aide {#help-content-tab}

![Onglet Contenu de l’aide](/help/adaptive-forms/assets/textinput_helptab.png)

* **Description courte** - Une brève description est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez la variable **Toujours afficher une description courte** pour l’afficher sous le composant.

* **Toujours afficher une description courte** - Activez l’option pour afficher la description courte sous le composant.

* **Texte de l’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur clique sur l’icône d’aide (i) placée en regard du composant. Le texte d’aide fournit des informations plus détaillées que le texte d’étiquette ou d’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility-tab}

![Onglet Accessibilité](/help/adaptive-forms/assets/textinput_accessibiltytab.png)

**Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisé par les malvoyants. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom et tout message pertinent du champ (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs, y compris ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS du composant Zone de texte.

### Onglet Styles {#styles-tab}

L’onglet permet de définir et de gérer les styles CSS d’un composant. Le composant principal de la zone de texte Forms adaptative prend en charge l’AEM [Système de style](/help/get-started/authoring.md#component-styling).

![Boîte de dialogue de conception](/help/adaptive-forms/assets/telephoneinput_designdialog.png)

* **Classes CSS par défaut**: Vous pouvez fournir une classe CSS par défaut pour le composant principal de la zone de texte Forms adaptatif.

* **Styles autorisés**: Vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé &quot;bold text&quot; et fournir la classe CSS &quot;font-weight: bold&quot;. Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de Forms adaptatif. Pour appliquer un style, dans l’éditeur de Forms adaptatif, sélectionnez le composant auquel vous souhaitez appliquer le style, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans le **Styles** liste déroulante. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

### Onglet Formats {#format-tab}

L’onglet Formats vous permet de définir des formats de nombres par défaut et personnalisés.

![Onglet Format](/help/adaptive-forms/assets/telephoneinput_format.png)
