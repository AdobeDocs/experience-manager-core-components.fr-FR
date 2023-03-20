---
title: Composant principal Adaptive Forms - Sélecteur de date
description: Utilisation ou personnalisation du composant principal Sélecteur de date de Forms adaptatif .
role: Architect, Developer, Admin, User
exl-id: aa9402de-ca57-4c19-8d36-2dd0a78d6806
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '1666'
ht-degree: 1%

---

# Sélecteur de date {#date-picker-adaptive-forms-core-component}

Un composant de sélecteur de date dans un formulaire adaptatif est un élément de l’interface utilisateur qui permet aux utilisateurs de sélectionner une date dans un calendrier ou en saisissant manuellement une date dans un format spécifique. Le composant Sélecteur de date peut être configuré pour avoir différentes valeurs de mise en forme, de validation et par défaut.

**Exemple**

![](/help/adaptive-forms/assets/date-picker.png)

## Utilisation {#reasons-to-use-drop-date-picker}

Plusieurs raisons expliquent l’intérêt d’inclure un sélecteur de date dans un formulaire adaptatif, notamment :

* **Convivialité**: Un composant de sélecteur de date permet aux utilisateurs de sélectionner facilement une date d’un calendrier sans avoir à saisir manuellement la date dans un champ de texte. Cela peut vous faire gagner du temps et réduire les erreurs.

* **Expérience utilisateur**: Le composant Sélecteur de date peut être utilisé pour rendre le formulaire plus convivial en offrant une méthode claire et intuitive de sélection de date pour les utilisateurs.

* **Analyse des données**: Le composant Sélecteur de date peut être utilisé pour collecter des données provenant de diverses sources et les analyser, ou pour les utiliser comme entrée pour un traitement ultérieur.

* **Gestion des événements**: Le composant Sélecteur de date peut être utilisé dans les sites web de gestion des événements pour sélectionner la date de l’événement.

* **Réservation et réservation**: Le composant Sélecteur de date peut être utilisé dans les sites web de réservation et de réservation pour sélectionner les dates d’enregistrement et de passage en caisse.

* **Format de date**: Le composant Sélecteur de date peut être utilisé pour corriger le format d’affichage et de saisie de la date. Assurez-vous que le format de date est cohérent dans l’ensemble du formulaire pour garantir une expérience utilisateur cohérente.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Accordéon de Forms adaptatif a été publié en février 2023 dans le cadre des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Voici un tableau de toutes les versions prises en charge, de la compatibilité AEM et des liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec<br>[version 2.0.4](/help/adaptive-forms/version.md) et plus tard | Compatible avec<br>[version 1.1.12](/help/adaptive-forms/version.md) et plus tard, mais moins de 2.0.0. |

Pour plus d’informations sur les versions et versions des composants principaux, reportez-vous à la section [Versions des composants principaux](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Détails techniques {#technical-details}

Obtenez les dernières informations sur le composant principal Sélecteur de date de Forms adaptatif dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/datepicker/v1/datepicker). Pour plus d’informations sur le développement des composants principaux, consultez la section [Documentation destinée aux développeurs sur les composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser votre expérience de sélecteur de date pour les visiteurs à l’aide de la boîte de dialogue Configurer . Vous pouvez également définir facilement des options de sélecteur de date pour une expérience utilisateur transparente.

### Onglet De base {#basic-tab}

![Onglet Simple](/help/adaptive-forms/assets/datepicker_basictab.png)

* **Nom** - Le nom identifie de manière unique le composant dans l’éditeur de règles. Les caractères spéciaux et les espaces ne sont pas autorisés dans les chaînes de nom.

* **Titre** - Le titre est une chaîne qui s’affiche en haut d’un composant dans un formulaire adaptatif. Le titre identifie de manière unique le composant dans l’arborescence d’un formulaire adaptatif. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

* **Masquer le titre** - Sélectionnez cette option pour masquer le titre du type de composant dans un formulaire adaptatif.

* **Texte d’espace réservé** - Le texte d’espace réservé dans un composant de formulaire fait référence à un libellé court ou à une invite qui apparaît dans un champ de saisie comme conseil à l’utilisateur sur le type d’information à saisir dans ce champ. Le texte d’espace réservé disparaît lorsque l’utilisateur commence à saisir du texte dans le champ et réapparaît si le champ est vide. Il fournit un indice visuel à l’utilisateur, mais n’agit pas comme une étiquette ou une valeur permanente pour le champ.

* **Masquer le composant** - Sélectionnez l’option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par l’utilisateur.
* **Désactiver le composant** - Sélectionnez l’option pour désactiver le composant. Le composant désactivé n’est pas principal ni modifiable par l’utilisateur final. L’utilisateur peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
* **Lecture seule** - Sélectionnez l’option pour rendre le composant non modifiable. L’utilisateur peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
* **Date par défaut** - Cette option vous permet d’ajouter une date au champ de formulaire. La date saisie s’affiche par défaut à l’emplacement du composant. Si aucune date n’est saisie par l’utilisateur, cette valeur est envoyée au moment de l’envoi du formulaire. Dans le cas **Composant désactivé** ou **Composant en lecture seule** est sélectionnée, la date par défaut s’affiche à l’écran et est envoyée au moment de l’envoi du formulaire.


### Onglet Validation {#validation-tab}

![Onglet Validation](/help/adaptive-forms/assets/datepicker_validation.png)

* **Obligatoire** - Sélectionnez cette option si vous souhaitez afficher le composant dans un formulaire adaptatif. Vous ne pouvez pas sélectionner la variable **Masquer le composant** ou **Désactiver le composant** dans le **De base** lorsque cette option est sélectionnée.

* **Message d’erreur** - Cette option vous permet de saisir un message qui s’affiche si la variable **Obligatoire** est cochée et le champ de formulaire reste vide.

* **Message de validation de script** - Cette option permet de saisir un message à afficher en cas d’échec de la validation du script.

* **Date minimale** - Cette option vous permet de saisir la date minimale requise. Si vous saisissez une date antérieure à la date spécifiée dans Date minimale, un message d’erreur s’affiche à l’écran. Le **Message d’erreur minimal** vous permet d’ajouter un message d’erreur personnalisé.

* **Message d’erreur minimal** - Le **Message d’erreur minimal** vous permet d’ajouter un message d’erreur personnalisé à afficher, si vous saisissez une date antérieure à celle spécifiée dans le **Date minimale** .

* **Date maximale** - Cette option vous permet de saisir la date maximale requise. Si vous saisissez une date ultérieure à celle spécifiée dans Date maximale, un message d’erreur s’affiche à l’écran. Le **Message d’erreur maximal** vous permet d’ajouter un message d’erreur personnalisé.

* **Message d’erreur maximal** - Le **Message d’erreur maximal** vous permet d’ajouter un message d’erreur personnalisé à afficher, si vous saisissez une date ultérieure à celle spécifiée dans le **Date maximale** .


### Onglet Contenu de l’aide {#help-content-tab}

![Onglet Contenu de l’aide](/help/adaptive-forms/assets/datepicker_helptab.png)

* **Description courte** - Une brève description est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez la variable **Toujours afficher une description courte** pour l’afficher sous le composant.

* **Toujours afficher une description courte**- Activez l’option pour afficher la description courte sous le composant.

* **Texte de l’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur clique sur l’icône d’aide (i) placée en regard du composant. Le texte d’aide fournit des informations plus détaillées que le texte d’étiquette ou d’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.


### Onglet Accessibilité {#accessibility-tab}

![Onglet Accessibilité](/help/adaptive-forms/assets/datepicker_accessibilitytab.png)

**Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisé par les malvoyants. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom et tout message pertinent du champ (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs, y compris ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

### Onglet Formats {#format-tab}

![Onglet Formats](/help/adaptive-forms/assets/datepicker_formattab.png)

* **Format d’affichage** - Il représente le format de date affiché pour l’utilisateur. Le **Type** permet à l’utilisateur de sélectionner le format de date. Vous pouvez également personnaliser le format de date à l’aide du **Personnalisé** dans le **Type** menu déroulant.

* **Modifier le format** - Il représente un format de date dans lequel l’utilisateur peut modifier la date. Le **Type** permet à l’utilisateur de sélectionner le format de date. Vous pouvez également personnaliser le format de date à l’aide du **Personnalisé** dans le **Type** menu déroulant.

* **Format d’affichage** - Il représente le format de date affiché pour l’utilisateur. L’option Type permet à l’utilisateur de sélectionner le format de date. Vous pouvez également personnaliser le format de date à l’aide du **Personnalisé** dans le **Type** menu déroulant.

* **Modifier le format** - Il représente un format de date dans lequel l’utilisateur modifie la date. L’option Type permet à l’utilisateur de sélectionner le format de date. Vous pouvez également personnaliser le format de date à l’aide du **Personnalisé** dans le **Type** menu déroulant.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS du composant Sélecteur de date.

### Onglet Styles {#styles-tab}

L’onglet permet de définir et de gérer les styles CSS d’un composant. Le composant principal Sélecteur de date de Forms adaptatif prend en charge l’AEM [Système de style](/help/get-started/authoring.md#component-styling).

![Onglet Style](/help/adaptive-forms/assets/datepicker_styletab.png)

* **Classes CSS par défaut**: Vous pouvez fournir une classe CSS par défaut pour le composant principal Sélecteur de date du Forms adaptatif .

* **Styles autorisés**: Vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé &quot;bold text&quot; et fournir la classe CSS &quot;font-weight: bold&quot;. Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de Forms adaptatif. Pour appliquer un style, dans l’éditeur de Forms adaptatif, sélectionnez le composant auquel vous souhaitez appliquer le style, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans le **Styles** liste déroulante. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

### Onglet Formats {#formats-tab}

L’onglet Formats vous permet de définir des formats de date par défaut et personnalisés.

![Formatonglet](/help/adaptive-forms/assets/datepicker_formatpolicy.png)

