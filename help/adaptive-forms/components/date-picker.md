---
title: Composant principal des formulaires adaptatifs - Sélecteur de date
description: Utilisation ou personnalisation du composant principal Sélecteur de date des formulaires adaptatifs.
role: Architect, Developer, Admin, User
exl-id: aa9402de-ca57-4c19-8d36-2dd0a78d6806
source-git-commit: b4a66a407e92398a98441c65ab588b9720777dfa
workflow-type: tm+mt
source-wordcount: '2299'
ht-degree: 100%

---

# Composant Sélecteur de date{#date-picker-adaptive-forms-core-component}

Un composant de sélecteur de date dans un formulaire adaptatif est un élément de l’interface utilisateur qui permet aux utilisateurs et aux utilisatrices de sélectionner une date dans un calendrier ou de saisir manuellement une date dans un format spécifique. Le composant Sélecteur de date peut être configuré pour avoir différentes valeurs de mise en forme, de validation et par défaut.

**Exemple**

![exemple](/help/adaptive-forms/assets/date-picker.png)

## Utilisation {#reasons-to-use-drop-date-picker}

Plusieurs raisons expliquent l’intérêt d’inclure un sélecteur de date dans un formulaire adaptatif, notamment :

- **Convivialité** : un composant de sélecteur de date permet aux utilisateurs et aux utilisatrices de sélectionner facilement une date d’un calendrier sans avoir à saisir manuellement cette date dans un champ de texte. Cela peut vous faire gagner du temps et réduire les erreurs.

- **Expérience utilisateur** : le composant Sélecteur de date peut être utilisé pour rendre le formulaire plus convivial en offrant une méthode claire et intuitive de sélection de date pour les utilisateurs et les utilisatrices.

- **Analyse des données** : le composant Sélecteur de date peut être utilisé pour collecter des données provenant de diverses sources et les analyser, ou pour les utiliser comme entrée pour un traitement ultérieur.

- **Gestion des événements** : le composant Sélecteur de date peut être utilisé dans les sites Web de gestion des événements pour sélectionner la date de l’événement.

- **Réservations** : le composant Sélecteur de date peut être utilisé dans les sites Web de réservation pour sélectionner les dates d’entrée et de sortie.

- **Format de date** : le composant Sélecteur de date peut être utilisé pour corriger le format d’affichage et de saisie de la date. Assurez-vous que le format de date est cohérent dans l’ensemble du formulaire pour garantir une expérience utilisateur cohérente.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Accordéon des formulaires adaptatifs a été publié en février 2023 au sein des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec la <br>[version 2.0.4](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible avec les<br>[versions 1.1.12](/help/adaptive-forms/version.md) à 2.0.0 exclue. |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Obtenez les dernières informations sur le composant principal Sélecteur de date des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/datepicker/v1/datepicker). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser votre expérience de sélecteur de date pour les visiteurs et les visiteuses à l’aide de la boîte de dialogue de configuration. Vous pouvez également définir facilement des options de sélecteur de date pour une expérience utilisateur transparente.

### Onglet De base {#basic-tab}

![Onglet De base](/help/adaptive-forms/assets/datepicker_basictab.png)

- **Nom** - Le nom identifie de manière unique le composant dans l’éditeur de règles. Les caractères spéciaux et les espaces ne sont pas autorisés dans les chaînes de nom.

- **Titre** - Le titre est une chaîne qui s’affiche en haut d’un composant dans un formulaire adaptatif. Le titre identifie de manière unique le composant dans l’arborescence d’un formulaire adaptatif. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.
- **Autoriser le texte enrichi pour le titre** - Cette fonctionnalité permet aux personnes de mettre en forme les titres en texte brut en y incorporant des fonctionnalités telles que le texte en gras, en italique et souligné, diverses polices, tailles de police et couleurs, et d’autres options pour améliorer la présentation visuelle et la personnalisation. Elle offre une plus grande flexibilité et un contrôle créatif pour faire ressortir les titres dans les documents, sites web ou applications.\
  Lorsque vous cochez la case **Autoriser le texte enrichi pour le titre**, les options de formatage deviennent visibles pour appliquer un style au titre du composant. Pour accéder à toutes les options de formatage disponibles, vous pouvez cliquer sur l’onglet ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Prise en charge de texte enrichi](/help/adaptive-forms/assets/richtext-support-title.png)

- **Masquer le titre** - Sélectionnez cette option pour masquer le titre du type de composant dans un formulaire adaptatif.

- **Texte d’espace réservé** - Le texte d’espace réservé dans un composant de formulaire fait référence à un libellé court ou à une invite qui apparaît dans un champ de saisie comme conseil à l’utilisateur ou à l’utilisatrice sur le type d’information à saisir dans ce champ. Le texte d’espace réservé disparaît lorsque l’utilisateur ou l’utilisatrice commence à saisir du texte dans le champ et réapparaît si le champ est vide. Il fournit un indice visuel à l’utilisateur ou à l’utilisatrice, mais n’agit pas comme une valeur ou un libellé permanent pour le champ.
- **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.

- **Marquer comme élément de formulaire non lié** : sélectionnez cette option pour configurer un champ de formulaire qui n’est lié à aucun schéma. Cette option vous permet d’enregistrer des données sans mettre à jour la source de données. Elle vous permet également de gérer les données de manière personnalisée, en les séparant de l’intégration de base de données standard.

- **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.
- **Désactiver le composant** - Sélectionnez cette option pour désactiver le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
- **Lecture seule** - Sélectionnez cette option pour rendre le composant non modifiable. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
- **Date par défaut** - Cette option vous permet d’ajouter une date au champ de formulaire. La date saisie s’affiche par défaut à l’emplacement du composant. Si aucune date n’est saisie par l’utilisateur ou l’utilisatrice, cette valeur est envoyée au moment de l’envoi du formulaire. Dans le cas où **Composant désactivé** ou **Composant en lecture seule** est sélectionné, la date par défaut s’affiche à l’écran et est envoyée au moment de l’envoi du formulaire.


### Onglet Validation {#validation-tab}

![Onglet Validation](/help/adaptive-forms/assets/datepicker_validation.png)

- **Obligatoire** : Sélectionnez cette option si vous souhaitez afficher le composant dans un formulaire adaptatif. Après avoir sélectionné cette option, vous devez effectuer une sélection avant de poursuivre l’envoi du formulaire. Vous ne pouvez pas sélectionner **Masquer le composant** ou **Désactiver le composant** sous l’onglet **De base** lorsque cette option est sélectionnée.

- **Message d’erreur** : cette option vous permet de rédiger un message qui s’affiche si la case à cocher **Obligatoire** est activée et le champ de formulaire reste vide.

- **Message de validation de script** - Cette option permet de saisir un message à afficher en cas d’échec de la validation du script.

- **Date minimale** : cette option vous permet de saisir la date minimale requise. Si vous saisissez une date antérieure à la date spécifiée dans Date minimale, un message d’erreur s’affiche à l’écran. La boîte de dialogue **Message d’erreur avec date minimale** vous permet d’ajouter un message d’erreur personnalisé.

- **Message d’erreur avec date minimal** : le **Message d’erreur avec date minimale** vous permet d’ajouter un message d’erreur personnalisé à afficher, si vous saisissez une date antérieure à celle spécifiée dans la **Date minimale**.
- **Exclure la date minimale** - Cette option permet d’omettre la date minimale d’une plage ou d’un jeu de dates donné.

- **Date maximale** : cette option vous permet de saisir la date maximale requise. Si vous saisissez une date ultérieure à celle spécifiée dans la Date maximale, un message d’erreur s’affiche à l’écran. Le **Message d’erreur avec date maximale** vous permet d’ajouter un message d’erreur personnalisé.

- **Message d’erreur avec date maximale** : le **Message d’erreur avec date maximale** vous permet d’ajouter un message d’erreur personnalisé à afficher, si vous saisissez une date ultérieure à celle spécifiée dans la **Date maximale**.

- **Exclure la date maximale** - Cette option permet d’omettre la date maximale d’une plage ou d’un jeu de dates donné.

### Onglet Contenu de l’aide {#help-content-tab}

![Onglet Contenu d’aide](/help/adaptive-forms/assets/datepicker_helptab.png)

- **Description courte** : Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Sélectionnez l’option **Toujours afficher la description courte** pour l’afficher sous le composant.

- **Toujours afficher la description courte** : sélectionnez cette option pour afficher la description courte sous le composant.

- **Texte de l’aide** : le texte d’aide prodigue des informations supplémentaires ou des conseils à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.


### Onglet Accessibilité {#accessibility-tab}

![Onglet Accessibilité](/help/adaptive-forms/assets/datepicker_accessibilitytab.png)

- **Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.
   - **Texte personnalisé** : sélectionnez cette option pour utiliser le texte personnalisé pour les libellés d’accessibilité ARIA. Cette option affiche la boîte de dialogue Texte personnalisé. Vous pouvez ajouter des informations pertinentes dans la boîte de dialogue Texte personnalisé.
   - **Description** : sélectionnez cette option pour utiliser la description des libellés d’accessibilité ARIA.
   - **Titre** : sélectionnez cette option pour utiliser le titre pour les libellés d’accessibilité ARIA.
   - **Nom** : sélectionnez cette option pour utiliser le nom pour les libellés d’accessibilité ARIA.
   - **Aucun** : sélectionnez cette option si vous ne souhaitez pas ajouter de texte supplémentaire pour les libellés d’accessibilité ARIA.

### Onglet Formats {#format-tab}

![Onglet Formats](/help/adaptive-forms/assets/datepicker_formattab.png)

- **Format d’affichage** : il s’agit du format de date affiché pour l’utilisateur ou l’utilisatrice. L’option **Type** permet à l’utilisateur ou à l’utilisatrice de sélectionner le format de date. Vous pouvez également personnaliser le format de date à l’aide de l’option **Personnaliser** dans le menu déroulant **Type**.

- **Modifier le format** : il s’agit d’un format de date dans lequel l’utilisateur ou l’utilisatrice peut modifier la date. L’option **Type** permet à l’utilisateur ou à l’utilisatrice de sélectionner le format de date. Vous pouvez également personnaliser le format de date à l’aide de l’option **Personnaliser** dans le menu déroulant **Type**.
- **Message d’erreur de format** : cette option permet de saisir le message affiché à l’écran lorsque la date saisie n’est pas au format correct.
- **Langue** : cette fonctionnalité est utilisée pour mettre en forme le champ spécifique. Lorsqu’une personne sélectionne une option de langue dans le menu déroulant **Type**, l’option **Balise de langue IETF BCP 47** s’affiche dans le panneau. Vous pouvez choisir la langue de formatage des champs lors de la traduction d’un formulaire adaptatif dans une langue spécifique.

L’ensemble de langues n’est pas visible par défaut, mais les personnes peuvent saisir une **Balise de langue IETF BCP 47** en mettant à jour la politique des modèles :

1. Ouvrez le modèle correspondant associé à un formulaire adaptatif dans l’éditeur de modèles.
2. Sélectionnez la politique existante `datepicker-default-policy` dans le menu déroulant.

   ![Politique des modèles de sélecteur de date](/help/adaptive-forms/assets/date-picker-template-policy.png)

3. Cliquez sur **Terminé**.

   >[!NOTE]
   >
   > Pour plus d’informations sur la façon de convertir un formulaire adaptatif en un paramètre régional spécifique, [cliquez ici](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/supporting-new-language-localization-core-components).

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS du composant Sélecteur de date.

### Onglet Styles {#styles-tab}

Cet onglet vous permet de définir et de gérer les styles CSS d’un composant. Le composant principal Sélecteur de date des formulaires adaptatifs prend en charge le [Système de style](/help/get-started/authoring.md#component-styling) d’AEM.

![Onglet Styles.](/help/adaptive-forms/assets/datepicker_styletab.png)

- **Classes CSS par défaut** : vous pouvez indiquer une classe CSS par défaut pour le composant principal Sélecteur de date des formulaires adaptatifs.

- **Styles autorisés** : vous pouvez appliquer des styles en indiquant un nom et la classe CSS du style. Par exemple, vous pouvez créer un style nommé « texte en gras » et fournir la classe CSS « police d’épaisseur : gras ». Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de formulaires adaptatifs. Pour appliquer un style, sélectionnez le composant auquel vous souhaitez appliquer le style dans l’éditeur de formulaires adaptatifs, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans la liste déroulante **Styles**. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

### Propriétés personnalisées

![Boîte de dialogue Propriétés personnalisées](/help/adaptive-forms/assets/datepicker_customproperties.png)

Les propriétés personnalisées vous permettent d’associer des attributs personnalisés (paires clé-valeur) à un composant principal de formulaire adaptatif à l’aide du modèle de formulaire. Les propriétés personnalisées sont répercutées dans la section des propriétés du rendu déocuplé du composant. Cela permet de créer un comportement de formulaire dynamique qui s’adapte en fonction des valeurs d’attributs personnalisés. Par exemple, les développeurs et développeuses peuvent concevoir plusieurs rendus d’un composant de formulaires découplés pour des plateformes mobiles, de bureau ou web, ce qui améliore considérablement l’expérience client sur un large éventail d’appareils.

- **Nom du groupe** : vous pouvez fournir un nom pour identifier le groupe de propriétés personnalisées. Vous pouvez ajouter, supprimer ou réorganiser plusieurs groupes de propriétés personnalisées. Après avoir ajouté le groupe de propriétés personnalisées, vous pouvez voir les options suivantes :

   - **Paires clé-valeur** : vous pouvez ajouter plusieurs noms et valeurs de propriétés personnalisées en cliquant sur le bouton **Ajouter** pour chaque groupe de propriétés personnalisées.

   - **Supprimer** : appuyez ou cliquez pour supprimer le nom et la valeur des propriétés personnalisées.

   - **Réorganiser** : appuyez ou cliquez et faites glisser pour réorganiser l’ordre du nom et de la valeur des propriétés personnalisées.

### Onglet Formats {#formats-tab}

L’onglet Formats vous permet de définir des formats de date par défaut et personnalisés.

![Onglet Format.](/help/adaptive-forms/assets/datepicker_formatpolicy.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Articles connexes {#related-articles}

{{more-like-this}}

## Voir également {#see-also}

{{see-also}}


