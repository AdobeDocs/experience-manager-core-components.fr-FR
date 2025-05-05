---
title: Composant principal des formulaires adaptatifs - Assistant
description: Utilisation ou personnalisation du composant principal « Assistant » des formulaires adaptatifs.
role: Architect, Developer, Admin, User
exl-id: fd785cd2-5ed6-4efb-997f-ce9056ed113d
source-git-commit: 8bba79956a04020647d5d04f9fe6fa674affedf1
workflow-type: tm+mt
source-wordcount: '2186'
ht-degree: 100%

---

# Composant Assistant{#wizard-adaptive-forms-core-component}

La disposition « Assistant » d’un formulaire adaptatif fait référence à un formulaire divisé en plusieurs étapes ou pages, où l’utilisateur ou l’utilisatrice passe d’une étape à l’autre. Cette disposition est appelée « assistant », car elle présente un processus détaillé du formulaire à l’utilisateur ou l’utilisatrice.

Chaque étape de l’assistant contient généralement un groupe de champs de formulaire associés et un mécanisme de navigation, comme les boutons « Suivant » et « Retour », pour passer d’une étape à l’autre. L’utilisateur ou l’utilisatrice ne peut passer à l’étape suivante qu’une fois l’étape en cours terminée et lorque tous les champs requis ont été remplis.

La disposition « Assistant » s’avère utile pour les formulaires contenant de nombreux champs ou informations à collecter, dans la mesure où elle répartit le formulaire en blocs plus petits et plus faciles à gérer. Elle permet également aux utilisateurs et aux utilisatrices de se concentrer sur un ensemble de champs à la fois, ce qui peut rendre le processus de remplissage de formulaire moins contraignant.

Cependant, cela peut également accroître la complexité du formulaire, car l’utilisateur ou l’utilisatrice doit parcourir plusieurs pages pour remplir le formulaire. Il est donc nécessaire d’évaluer les exigences du formulaire et les besoins de l’utilisateur ou de l’utilisatrice avant de décider d’utiliser la disposition « Assistant ».
Vous pouvez utiliser le composant principal de disposition « Assistant » dans un formulaire adaptatif pour créer une disposition « Assistant ».

**Exemple**

![exemple](/help/adaptive-forms/assets/wizard.png)

## Utilisation {#reasons-to-use-wizard-in-an-adaptive-form}

Il existe plusieurs raisons d’utiliser la disposition « Assistant » dans un formulaire adaptatif :

- **Simplicité** : la répartition d’un formulaire en plusieurs étapes peut faciliter la compréhension et la saisie, car les utilisateurs et les utilisatrices peuvent se concentrer sur un ensemble de champs à la fois.

- **Organisation** : une disposition « Assistant » peut vous aider à organiser les formulaires par sujet ou objectif. Elle peut également regrouper les champs associés, ce qui peut rendre le processus de remplissage de formulaires plus logique et plus efficace.

- **Validation** : une disposition « Assistant » permet une validation étape par étape, qui peut aider les utilisateurs et les utilisatrices à identifier et corriger les erreurs au fur et à mesure, plutôt que d’attendre jusqu’à la fin du formulaire.

- **Indicateur de progression** : une disposition « Assistant » peut afficher la progression du formulaire, ce qui peut aider l’utilisateur ou l’utilisatrice à comprendre la partie du formulaire à remplir.

- **Formulaires longs** : si le formulaire comporte de nombreux champs, il peut être très difficile pour l’utilisateur ou l’utilisatrice de les voir tous en même temps. Par conséquent, le décomposer en blocs plus petits et plus faciles à gérer peut le rendre moins intimidant.

- **Éviter l’abandon** : une disposition Assistant peut également contribuer à réduire l’abandon de formulaire, car les utilisateurs et les utilisatrices sont plus susceptibles de remplir un formulaire s’ils ou elles peuvent voir la progression et comprendre ce qu’il reste à faire.

- **Expérience mobile** : une disposition « Assistant » peut également s’avérer bénéfique pour les formulaires accessibles sur les appareils mobiles, dans la mesure où elle permet d’afficher des pages plus petites qui se chargent plus rapidement et sont plus faciles à parcourir.

Dans l’ensemble, une disposition « Assistant » peut rendre le processus de remplissage du formulaire plus facile à gérer et plus efficace pour les utilisateurs et les utilisatrices, mais il est important de tenir compte de la complexité du formulaire et des besoins de l’utilisateur ou de l’utilisatrice avant de décider d’utiliser ce type de disposition.

## Version et compatibilité {#version-and-compatibility}

Le composant principal « Disposition Assistant » des formulaires adaptatifs a été publié en février 2023 dans le cadre de la version 2.0.4 des composants principaux. Voici un tableau présentant toutes les versions prises en charge, la compatibilité AEM et les liens vers la documentation correspondante :

|  |  |
|---|---|
| Version du composant | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatible avec la <br>[version 2.0.4](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible | Compatible |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_fr). -->

## Détails techniques {#technical-details}

Retrouvez les informations les plus récentes sur le composant principal « Titre » des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/wizard/v1/wizard). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience d’assistant pour les visiteurs et les visiteuses en utilisant la boîte de dialogue Configurer. Vous pouvez également définir facilement des options d’assistant pour une expérience utilisateur fluide.

### Onglet De base {#basic-tab}

![Onglet De base](/help/adaptive-forms/assets/wizard-basic.png)

- **Nom** - Vous pouvez identifier facilement un composant de formulaire en lui attribuant un nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

- **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant.

- **Masquer le titre** - Sélectionnez cette option pour masquer le titre du composant.

- **Associer les données des composants enfants lors de l’envoi du formulaire (encapsuler les données dans l’objet)** : lorsque l’option est sélectionnée, les données de ses composants enfants sont imbriquées dans l’objet JSON du composant parent. Cependant, si l’option n’est pas sélectionnée, les données JSON envoyées ont une structure plate, sans objet pour le composant parent. Par exemple :

   - Lorsque cette option est sélectionnée, les données des composants enfants (par exemple, Rue, Ville et Code postal) sont imbriquées dans le composant parent (Adresse) sous la forme d’un objet JSON. Cela crée une structure hiérarchique et les données sont organisées sous le composant parent.

     Structure des données envoyées :

     ```JSON
     { "Address":
     
     { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     
     }
     ```

   - Lorsque l’option n’est pas sélectionnée, les données JSON envoyées ont une structure plate sans objet pour le composant parent (Adresse). Toutes les données se trouvent au même niveau, sans organisation hiérarchique.


     Structure des données envoyées :

     ```JSON
        { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     ```

<!--   **Wrap data in an object** - Choose "Wrap data in an object" to put the field data from the Wizard inside a JSON object. If not chosen, the submit data JSON has a flat structure for the Wizard's fields.

-   **Layout** - You can have either a fixed layout (Simple) or a flexible layout (Responsive Grid) for your wizard. The Simple layout keeps everything fixed in the place, while the Responsive Grid allows you to adjust the position of components to suit your needs. For example, use Responsive Grid to align "First Name", "Middle Name" and "Last Name" in a form in a single row.  -->

- **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.

- **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.

- **Désactiver le composant** - Sélectionnez cette option pour désactiver le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

- **Lecture seule** - Sélectionnez cette option pour rendre le composant non modifiable. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

### Onglet Répéter l’assistant {#repeat-wizard-tab}

![Répéter l’assistant](/help/adaptive-forms/assets/wizard-repeat.png)

Vous pouvez utiliser les options de répétition pour dupliquer l’assistant et ses composants enfants, définir un nombre de répétitions minimal et maximal et faciliter la réplication de sections similaires dans un formulaire. Lors de l’interaction avec le composant Assistant et de l’accès à ses paramètres, les options suivantes s’affichent :

- **Rendre l’assistant répétable** : fonctionnalité de basculement qui permet aux utilisateurs et utilisatrices d’activer ou de désactiver la fonctionnalité de répétabilité.
- **Nombre minimal de répétitions** : définit le nombre minimal de répétitions possibles du panneau Assistant. La valeur zéro indique que le panneau Assistant n’est pas répété. La valeur par défaut est zéro.
- **Nombre maximal de répétitions** : définit le nombre maximal de répétitions possibles du panneau Assistant. Par défaut, cette valeur est illimitée.

Pour gérer efficacement les sections répétables dans l’assistant, procédez comme indiqué dans l’article [Création de formulaires avec des sections répétables](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html?lang=fr).

### Onglet Éléments {#items-tab}

![Onglet Éléments](/help/adaptive-forms/assets/wizard_itemstab.png)

Cette option vous permet d’ajouter des composants de formulaire adaptatif en cliquant sur le bouton Ajouter, qui s’affiche par défaut lorsque l’assistant est ajouté en mode d’édition.

### Onglet Aide {#help-tab}

![Onglet Aide](/help/adaptive-forms/assets/wizard_helptab.png)

- **Description courte** : Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez l’option **Toujours afficher une description courte** pour l’afficher sous le composant.

- **Toujours afficher une description courte** - Activez cette option pour afficher la description courte sous le composant.

- **Texte d’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.


### Onglet Accessibilité {#accessibility}

![Onglet Accessibilité](/help/adaptive-forms/assets/wizard_accessibiltytab.png)

- **Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.
   - **Texte personnalisé** : sélectionnez cette option pour utiliser le texte personnalisé pour les libellés d’accessibilité ARIA. Cette option affiche la boîte de dialogue Texte personnalisé. Vous pouvez ajouter des informations pertinentes dans la boîte de dialogue Texte personnalisé.
   - **Description** : sélectionnez cette option pour utiliser la description des libellés d’accessibilité ARIA.
   - **Titre** : sélectionnez cette option pour utiliser le titre pour les libellés d’accessibilité ARIA.
   - **Nom** : sélectionnez cette option pour utiliser le nom pour les libellés d’accessibilité ARIA.
   - **Aucun** : sélectionnez cette option si vous ne souhaitez pas l’ajouter pour les libellés d’accessibilité ARIA.

- **Rôle HTML à annoncer par le lecteur d’écran** - Le rôle HTML est un attribut utilisé pour spécifier l’objectif d’un élément HTML pour les technologies d’assistance telles que les lecteurs d’écran. L’attribut rôle est utilisé pour fournir un contexte et une signification sémantique supplémentaires à un élément, ce qui facilite l’interprétation et l’annonce du contenu à l’utilisateur ou à l’utilisatrice par les lecteurs d’écran. Par exemple, dans AEM Forms, le libellé d’un champ de formulaire peut avoir le rôle « libellé » et son champ de saisie peut avoir le rôle « zone de texte ». Cela permet au lecteur d’écran de comprendre la relation entre le libellé et le champ de saisie, et de les annoncer correctement à l’utilisateur ou à l’utilisatrice.


## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue Conception permet aux créateurs et aux créatrices de modèles de contrôler l’affichage des éléments par défaut. Pour le composant « Assistant » des formulaires adaptatifs, vous pouvez définir les éléments suivants :

- Composants principaux qu’un créateur ou une créatrice de formulaire peut ajouter à l’assistant dans l’éditeur de formulaires adaptatifs.
- Noms simples pour les styles (classes CSS) qui peuvent être appliqués dans la boîte de dialogue des propriétés du composant « Assistant » dans l’éditeur de formulaires adaptatifs.

Cela permet de rendre le processus de création et de personnalisation de formulaires plus simple et plus efficace.

### Onglet Composants autorisés {#allowed-components-tab}

![Onglet Composants autorisés](/help/adaptive-forms/assets/tabs-allowed-component.png)

L’onglet **Composants autorisés** permet à l’éditeur de modèles de définir les composants qui peuvent être ajoutés en tant qu’éléments aux panneaux dans le composant Assistant de l’éditeur de formulaires adaptatifs.

### Onglet Styles {#styles-tab}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS d’un composant. Le composant principal Assistant des formulaires adaptatifs prend en charge le [Système de style](/help/get-started/authoring.md#component-styling) d’AEM.

![Onglet Styles](/help/adaptive-forms/assets/tabs-styles-tab.png)

- **Classes CSS par défaut** : vous pouvez fournir une classe CSS par défaut pour le composant principal Assistant des formulaires adaptatifs.

- **Styles autorisés** : vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé « texte en gras » et fournir la classe CSS « police d’épaisseur : gras ». Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de formulaires adaptatifs. Pour appliquer un style, sélectionnez le composant auquel vous souhaitez appliquer le style dans l’éditeur de formulaires adaptatifs, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans la liste déroulante **Styles**. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

### Onglet Propriétés personnalisées

![Onglet Propriétés personnalisées](/help/adaptive-forms/assets/tabs-custom-properties.png)

Les propriétés personnalisées vous permettent d’associer des attributs personnalisés (paires clé-valeur) à un composant principal de formulaire adaptatif à l’aide du modèle de formulaire. Les propriétés personnalisées sont répercutées dans la section des propriétés du rendu déocuplé du composant. Cela permet de créer un comportement de formulaire dynamique qui s’adapte en fonction des valeurs d’attributs personnalisés. Par exemple, les développeurs et développeuses peuvent concevoir plusieurs rendus d’un composant de formulaires découplés pour des plateformes mobiles, de bureau ou web, ce qui améliore considérablement l’expérience client sur un large éventail d’appareils.

- **Nom du groupe** : vous pouvez fournir un nom pour identifier le groupe de propriétés personnalisées. Vous pouvez ajouter, supprimer ou réorganiser plusieurs groupes de propriétés personnalisées. Après avoir ajouté le groupe de propriétés personnalisées, vous pouvez voir les options suivantes :

   - **Paires clé-valeur** : vous pouvez ajouter plusieurs noms et valeurs de propriétés personnalisées en cliquant sur le bouton **Ajouter** pour chaque groupe de propriétés personnalisées.

   - **Supprimer** : appuyez ou cliquez pour supprimer le nom et la valeur des propriétés personnalisées.

   - **Réorganiser** : appuyez ou cliquez et faites glisser pour réorganiser l’ordre du nom et de la valeur des propriétés personnalisées.

## Articles connexes {#related-articles}

{{more-like-this}}

## Voir également {#see-also}

{{see-also}}