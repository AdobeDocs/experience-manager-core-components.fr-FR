---
title: Composant principal Formulaires adaptatifs - Bouton
description: Utilisation ou personnalisation du composant principal Bouton des formulaires adaptatifs.
role: Architect, Developer, Admin, User
exl-id: cb75929b-8c86-49d1-b51a-368f5b80b1a9
source-git-commit: e0ed415bd7f45fdca6fbbb8ba409604d9e82a647
workflow-type: tm+mt
source-wordcount: '1634'
ht-degree: 86%

---

# Composant Bouton {#button-component-adaptive-forms-core-component}

Le bouton d’un formulaire adaptatif est un élément de l’interface utilisateur qui permet aux utilisateurs et utilisatrices de déclencher une action lorsqu’ils ou elles cliquent dessus. L’élément bouton peut être utilisé pour envoyer un formulaire, le réinitialiser ou effectuer d’autres actions, comme accéder à une autre page ou déclencher un code personnalisé. Le bouton peut être créé à l’aide du composant principal Bouton.

L’éditeur de règles de formulaires adaptatifs permet aux utilisateurs et utilisatrices de définir différentes actions pour le composant Bouton. Par exemple, l’ouverture d’un site web, l’affichage ou le masquage de composants de formulaire, l’ajout d’une instance Panneau ou Composant, l’envoi ou la réinitialisation d’un formulaire, etc.

Les formulaires adaptatifs proposent des composants distincts pour le [Bouton Envoyer](/help/adaptive-forms/components/submit-button.md) et le [Bouton Réinitialiser](/help/adaptive-forms/components/reset-button.md), qui permettent d’envoyer ou de réinitialiser un formulaire en toute facilité. Le composant Bouton peut être configuré de manière flexible pour exécuter ces actions en fonction des besoins spécifiques.

Les utilisateurs et utilisatrices peuvent accéder à la liste complète des actions prises en charge par le composant Bouton à l’aide de l’éditeur de règles de formulaires adaptatifs. L’éditeur de règles permet de créer des règles qui sont déclenchées par divers événements, comme le clic sur un bouton, le chargement d’un formulaire ou la modification de la valeur d’un champ. Ces règles peuvent ensuite être utilisées pour effectuer différentes actions, telles que l’affichage ou le masquage de composants, la définition de valeurs de champ ou l’envoi du formulaire.

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

Le composant principal Accordéon des formulaires adaptatifs a été publié en février 2023 au sein des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

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

- **Nom** - Vous pouvez identifier facilement un composant de formulaire avec son nom unique aussi bien dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

- **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

- **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.

- **Référence Bind du document d’enregistrement** - Cette option vous permet d’associer un champ de formulaire adaptatif au champ « Document d’enregistrement ». Lorsque l’utilisateur ou l’utilisatrice saisit une valeur dans un champ lié d’un formulaire adaptatif, cette valeur apparaît également dans le champ lié du document d’enregistrement correspondant. Par exemple, une référence Bind de document d’enregistrement peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un document d’enregistrement, en fonction de l’identifiant saisi dans le formulaire. AEM Forms vous permet ainsi de générer un document d’enregistrement et offre une expérience utilisateur transparente pour la collecte et la gestion des données.

- **Marquer comme élément de formulaire non lié**: sélectionnez l’option de configuration d’un champ de formulaire non lié à un schéma. Cette option vous permet d’enregistrer des données sans mettre à jour la source de données. Il vous permet également de gérer les données de manière personnalisée, en les séparant de l’intégration de base de données standard.

- **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.
- **Désactiver le composant** - Sélectionnez cette option pour désactiver le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
- **Lecture seule** - Sélectionnez cette option pour rendre le composant non modifiable. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

### Onglet Contenu de l’aide {#help-content}

![Onglet Contenu d’aide](/help/adaptive-forms/assets/button_helptab.png)

- **Description courte** : Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez l’option **Toujours afficher une description courte** pour l’afficher sous le composant.

- **Toujours afficher une description courte** - Activez cette option pour afficher la description courte sous le composant.

- **Texte d’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Accessibilité {#accessibility}

![Onglet Accessibilité](/help/adaptive-forms/assets/button_accessibilitytab.png)


- **Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS du composant Bouton.

### Onglet Styles {#styles-tab}

Le composant principal Bouton des formulaires adaptatifs prend en charge le [Système de style](/help/get-started/authoring.md#component-styling) AEM.

![Boîte de dialogue de conception.](/help/adaptive-forms/assets/checkbox-style.png)

- **Classes CSS par défaut** : vous pouvez fournir une classe CSS par défaut pour le composant principal Bouton des formulaires adaptatifs.

- **Styles autorisés** : vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé « texte en gras » et fournir la classe CSS « police d’épaisseur : gras ». Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de formulaires adaptatifs. Pour appliquer un style, sélectionnez le composant auquel vous souhaitez appliquer le style dans l’éditeur de formulaires adaptatifs, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans la liste déroulante **Styles**. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

### Propriétés personnalisées

![Boîte de dialogue Propriétés personnalisées](/help/adaptive-forms/assets/checkbox-customproperties.png)

Les propriétés personnalisées vous permettent d’associer des attributs personnalisés (paires clé-valeur) à un composant de base de formulaire adaptatif à l’aide du modèle de formulaire. Les propriétés personnalisées sont répercutées dans la section des propriétés du rendu sans en-tête du composant. Il permet de créer un comportement de formulaire dynamique qui s’adapte en fonction des valeurs d’attributs personnalisés. Par exemple, les développeurs peuvent concevoir différents rendus d’un composant Forms sans affichage pour les plateformes mobiles, de bureau ou web, ce qui améliore considérablement l’expérience utilisateur sur un large éventail d’appareils.

- **Nom du groupe**: vous pouvez fournir un nom pour identifier le groupe de propriétés personnalisé. Vous pouvez ajouter, supprimer ou réorganiser plusieurs groupes de propriétés personnalisés. Après avoir ajouté le groupe de propriétés personnalisées, vous pouvez voir les options suivantes :

   - **Paires clé-valeur**: vous pouvez ajouter plusieurs noms de propriétés personnalisées et valeurs de propriétés personnalisées en cliquant sur le bouton **Ajouter** pour chaque groupe de propriétés personnalisé.

   - **Supprimer**: appuyez ou cliquez sur pour supprimer le nom de propriété personnalisée et la valeur de propriété personnalisée.

   - **Réorganiser**: appuyez ou cliquez dessus et faites glisser pour réorganiser l’ordre du nom de propriété personnalisée et de la valeur de propriété personnalisée.

## Articles connexes {#related-articles}

{{more-like-this}}

## Voir également {#see-also}

{{see-also}}

