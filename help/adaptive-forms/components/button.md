---
title: Composant principal Formulaires adaptatifs - Bouton
description: Utilisation ou personnalisation du composant principal Bouton des formulaires adaptatifs.
role: Architect, Developer, Admin, User
exl-id: cb75929b-8c86-49d1-b51a-368f5b80b1a9
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '1658'
ht-degree: 98%

---


# Composant Bouton {#button-component-adaptive-forms-core-component}

Le bouton d’un formulaire adaptatif est un élément de l’interface utilisateur qui permet aux utilisateurs et utilisatrices de déclencher une action lorsqu’ils ou elles cliquent dessus. L’élément bouton peut être utilisé pour envoyer un formulaire, le réinitialiser ou effectuer d’autres actions, comme accéder à une autre page ou déclencher un code personnalisé. Le bouton peut être créé à l’aide du composant principal Bouton.

L’éditeur de règles de formulaires adaptatifs permet aux utilisateurs et utilisatrices de définir différentes actions pour le composant Bouton. Par exemple, l’ouverture d’un site web, l’affichage ou le masquage de composants de formulaire, l’ajout d’une instance Panneau ou Composant, l’envoi ou la réinitialisation d’un formulaire, etc.

Les formulaires adaptatifs proposent des composants distincts pour le [Bouton Envoyer](/help/adaptive-forms/components/submit-button.md) et le [Bouton Réinitialiser](/help/adaptive-forms/components/reset-button.md), qui permettent d’envoyer ou de réinitialiser un formulaire en toute facilité. Le composant Bouton peut être configuré de manière flexible pour exécuter ces actions en fonction des besoins spécifiques.

Les utilisateurs et utilisatrices peuvent accéder à la liste complète des actions prises en charge par le composant Bouton à l’aide de l’éditeur de règles de formulaires adaptatifs. L’éditeur de règles permet de créer des règles qui sont déclenchées par divers événements, comme le clic sur un bouton, le chargement d’un formulaire ou la modification de la valeur d’un champ. Ces règles peuvent ensuite être utilisées pour effectuer différentes actions, telles que l’affichage ou le masquage de composants, la définition de valeurs de champ ou l’envoi du formulaire.

{{traditional-aem}}

**Exemple**

![Exemple de bouton](/help/adaptive-forms/assets/example-button.png)

## Utilisation {#reasons-to-use-button}

L’emploi du bouton dans un formulaire offre les avantages suivants :

- **Envoi de formulaire** : un bouton est généralement utilisé pour envoyer un formulaire, ce qui permet aux utilisateurs et utilisatrices d’envoyer les données qu’ils ou elles ont saisies au serveur en vue de leur traitement.

- **Réinitialisation du formulaire** : vous pouvez également utiliser des boutons pour réinitialiser un formulaire et effacer toutes les données saisies par l’utilisateur ou l’utilisatrice.

- **Navigation** : utilisez les boutons pour accéder aux différentes sections d’un formulaire ou aux différentes pages d’un site web.

- **Gestion des événements** : utilisez les boutons pour déclencher différents événements, tels que l’ouverture d’un site web, l’affichage ou le masquage d’un composant, ainsi que l’ajout d’une instance Panneau ou Composant au bouton.

- **Interactivité** : les boutons permettent de créer des formulaires interactifs. Par exemple, un bouton peut être utilisé pour ouvrir une boîte de dialogue modale ou pour activer ou non une section du formulaire (bouton bascule).

## Version et compatibilité {#version-and-compatibility}

Le composant principal Bouton du Forms adaptatif a été publié en février 2023 dans le cadre des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec la <br>[version 2.0.4](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible avec les<br>[versions 1.1.12](/help/adaptive-forms/version.md) à 2.0.0 exclue. |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Pour obtenir les informations les plus récentes sur le composant principal Bouton des formulaires adaptatifs, consultez la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/button/v1/button). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience visiteur du bouton à l’aide de la boîte de dialogue de configuration. Vous pouvez également définir facilement les propriétés du bouton pour une expérience utilisateur transparente.

### Onglet de base {#basic-tab}

![Onglet De base](/help/adaptive-forms/assets/button_basictab.png)

- **Nom** - Vous pouvez identifier facilement un composant de formulaire en lui attribuant un nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

- **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

- **Autoriser le texte enrichi pour le titre** - Cette fonctionnalité permet aux personnes de mettre en forme les titres en texte brut en y incorporant des fonctionnalités telles que le texte en gras, en italique et souligné, diverses polices, tailles de police et couleurs, et d’autres options pour améliorer la présentation visuelle et la personnalisation. Elle offre une plus grande flexibilité et un contrôle créatif pour faire ressortir les titres dans les documents, sites web ou applications.\
  Lorsque vous cochez la case **Autoriser le texte enrichi pour le titre**, les options de formatage deviennent visibles pour appliquer un style au titre du composant. Pour accéder à toutes les options de formatage disponibles, vous pouvez cliquer sur l’onglet ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Prise en charge de texte enrichi](/help/adaptive-forms/assets/richtext-support-title.png)

- **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.

<!--   **Document of Record bind reference** - This option allows you to associate an Adaptive Form field with Document of Record field. When user enters any value in a linked field of an Adaptive Form that value also appears in the linked field of the corresponding Document of Record. For example, a Document of Record bind reference can be used to display a customer's name and address in a Document of Record, based on the customer's ID entered into the form. In this way, AEM Forms enables you to generate Document of Record and offers a seamless user experience for collecting and managing data.-->

- **Marquer comme élément de formulaire non lié** : sélectionnez cette option pour configurer un champ de formulaire qui n’est lié à aucun schéma. Cette option vous permet d’enregistrer des données sans mettre à jour la source de données. Elle vous permet également de gérer les données de manière personnalisée, en les séparant de l’intégration de base de données standard.
- **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.
- **Désactiver le composant** - Sélectionnez cette option pour désactiver le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

<!--   **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.-->

### Onglet Contenu de l’aide {#help-content}

![Onglet Contenu d’aide](/help/adaptive-forms/assets/button_helptab.png)

- **Description courte** : Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez l’option **Toujours afficher une description courte** pour l’afficher sous le composant.

- **Toujours afficher une description courte** - Activez cette option pour afficher la description courte sous le composant.

- **Texte d’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Accessibilité {#accessibility}

![Onglet Accessibilité](/help/adaptive-forms/assets/button_accessibilitytab.png)


- **Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.
   - **Texte personnalisé** : sélectionnez cette option pour utiliser le texte personnalisé pour les libellés d’accessibilité ARIA. Cette option affiche la boîte de dialogue Texte personnalisé. Vous pouvez ajouter des informations pertinentes dans la boîte de dialogue Texte personnalisé.
   - **Description** : sélectionnez cette option pour utiliser la description des libellés d’accessibilité ARIA.
   - **Titre** : sélectionnez cette option pour utiliser le titre pour les libellés d’accessibilité ARIA.
   - **Nom** : sélectionnez cette option pour utiliser le nom pour les libellés d’accessibilité ARIA.
   - **Aucun** : sélectionnez cette option si vous ne souhaitez pas ajouter de texte supplémentaire pour les libellés d’accessibilité ARIA.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS du composant Bouton.

### Onglet Styles {#styles-tab}

Le composant principal Bouton des formulaires adaptatifs prend en charge le [Système de style](/help/get-started/authoring.md#component-styling) AEM.

![Boîte de dialogue de conception](/help/adaptive-forms/assets/checkbox-style.png)

- **Classes CSS par défaut** : vous pouvez fournir une classe CSS par défaut pour le composant principal Bouton des formulaires adaptatifs.

- **Styles autorisés** : vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé « texte en gras » et fournir la classe CSS « police d’épaisseur : gras ». Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de formulaires adaptatifs. Pour appliquer un style, sélectionnez le composant auquel vous souhaitez appliquer le style dans l’éditeur de formulaires adaptatifs, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans la liste déroulante **Styles**. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

### Propriétés personnalisées

![Boîte de dialogue Propriétés personnalisées](/help/adaptive-forms/assets/checkbox-customproperties.png)

Les propriétés personnalisées vous permettent d’associer des attributs personnalisés (paires clé-valeur) à un composant principal de formulaire adaptatif à l’aide du modèle de formulaire. Les propriétés personnalisées sont répercutées dans la section des propriétés du rendu déocuplé du composant. Cela permet de créer un comportement de formulaire dynamique qui s’adapte en fonction des valeurs d’attributs personnalisés. Par exemple, les développeurs et développeuses peuvent concevoir plusieurs rendus d’un composant de formulaires découplés pour des plateformes mobiles, de bureau ou web, ce qui améliore considérablement l’expérience client sur un large éventail d’appareils.

- **Nom du groupe** : vous pouvez fournir un nom pour identifier le groupe de propriétés personnalisées. Vous pouvez ajouter, supprimer ou réorganiser plusieurs groupes de propriétés personnalisées. Après avoir ajouté le groupe de propriétés personnalisées, vous pouvez voir les options suivantes :

   - **Paires clé-valeur** : vous pouvez ajouter plusieurs noms et valeurs de propriétés personnalisées en cliquant sur le bouton **Ajouter** pour chaque groupe de propriétés personnalisées.

   - **Supprimer** : appuyez ou cliquez pour supprimer le nom et la valeur des propriétés personnalisées.

   - **Réorganiser** : appuyez ou cliquez et faites glisser pour réorganiser l’ordre du nom et de la valeur des propriétés personnalisées.

## Articles connexes {#related-articles}

{{more-like-this}}

## Voir également {#see-also}

{{see-also}}

