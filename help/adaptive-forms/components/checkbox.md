---
title: Composant principal Adaptive Forms - Case à cocher
description: Utilisation ou personnalisation du composant principal de case à cocher Forms adaptatif.
role: Architect, Developer, Admin, User
hide: true
hidefromtoc: true
source-git-commit: ecc6ba79ba5e90bd6e759353d15ca85ce404d769
workflow-type: tm+mt
source-wordcount: '1708'
ht-degree: 53%

---


# Case à cocher {#checkbox-component}

Une case à cocher est un élément d’interface utilisateur graphique généralement utilisé dans les applications logicielles et les formulaires pour permettre aux utilisateurs d’effectuer un choix binaire entre deux options : cochée (sélectionnée) ou non cochée (désélectionnée).

Une case à cocher est généralement représentée sous la forme d’un petit carré qui peut être activé ou désactivé en cliquant ou en appuyant dessus. Lorsqu’une case est cochée, une coche s’affiche pour indiquer que l’option ou la fonction associée est active ou activée.

**Exemple**

![groupe de cases à cocher](/help/adaptive-forms/assets/checkbox-example.png)

## Utilisation {#reasons-to-use-checkbox}

Les raisons courantes d’utiliser la case à cocher dans un formulaire adaptatif sont les suivantes :

- **Facilité d’utilisation**: les cases à cocher sont visuellement claires et fournissent une méthode simple pour effectuer des choix binaires. Ils sont intuitifs et faciles à comprendre, ce qui les rend conviviaux.

- **Consentement et accord**: des cases à cocher sont utilisées pour obtenir le consentement de l’utilisateur à diverses fins, par exemple pour accepter les conditions générales, s’abonner à des newsletters ou confirmer la vérification de l’âge. Ils indiquent clairement que l’utilisateur accepte activement quelque chose.

- **Confirmation visuelle**: les cases à cocher activées fournissent une confirmation visuelle pour les utilisateurs que leur sélection a été enregistrée. Ces commentaires permettent d’éviter les erreurs des utilisateurs et de s’assurer qu’ils savent que leurs choix ont été enregistrés.

- **Prévention des erreurs**: les cases à cocher réduisent la probabilité des erreurs en permettant aux utilisateurs de vérifier et de confirmer les choix avant l’envoi du formulaire.

## Version et compatibilité {#version-and-compatibility}

Le composant principal de case à cocher Adaptive Forms a été publié en février 2023 dans le cadre des composants principaux 2.0.4. Voici un tableau de toutes les versions prises en charge, de la compatibilité AEM et des liens vers la documentation correspondante :

|  |  |
|---|---|
| Version du composant | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatible avec la <br>[version 2.0.4](/help/versions.md) et les versions ultérieures | Compatible | Compatible |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/versions.md).

## Détails techniques {#technical-details}

Obtenez les dernières informations sur le composant principal de case à cocher Adaptive Forms dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkbox/v1/checkbox). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser votre expérience de case à cocher pour les visiteurs qui utilisent la boîte de dialogue Configurer . Vous pouvez également définir facilement les options de case à cocher pour une expérience utilisateur fluide.

![Onglet De base](/help/adaptive-forms/assets/checkbox-basic.png)

- **Nom** - Vous pouvez identifier facilement un composant de formulaire en lui attribuant un nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

- **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre apparaît à côté du composant. Si vous n’ajoutez pas de titre, le composant ne s’affiche pas.

- **Masquer le titre** - Sélectionnez cette option pour masquer le titre du composant.

- **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.

- **Marquer comme élément de formulaire non lié**: sélectionnez l’option de configuration d’un champ de formulaire non lié à un schéma. Cette option vous permet d’enregistrer des données sans mettre à jour la source de données. Il vous permet également de gérer les données de manière personnalisée, en les séparant de l’intégration de base de données standard.

- **Type de données de la valeur envoyée**: cette option spécifie le type de données de la valeur envoyée lorsqu’une option est sélectionnée. Si le **type de données de la valeur envoyée** est défini sur `Number` et que vous ajoutez des données de chaîne à la **Valeur des données** dans l’onglet **Options**, l’écran affiche un message d’erreur `Value type mismatch`.

- **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.

- **Désactiver le composant** - Sélectionnez l’option pour désactiver ou verrouiller le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
- **Lecture seule** - Sélectionnez cette option pour rendre le composant non modifiable. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
- **Lorsqu’elle est cochée, la valeur renvoyée** -Sélectionnez cette option pour spécifier la valeur à associer à la case à cocher lorsqu’elle est cochée ou sélectionnée. Il s’agit de l’action qui se produit lorsqu’un utilisateur coche ou marque la case.
- **Activez l’option Décocher.**- Sélectionnez l’option permettant d’activer ou de désactiver la possibilité de décocher une case précédemment cochée.
   - If **Enable Uncheck** est activée ou définie sur true, cela signifie que l’utilisateur peut cocher et décocher la case à cocher à sa discrétion. Ils peuvent activer et désactiver la case à cocher si nécessaire.

   - If **Enable Uncheck** est désactivé ou défini sur false, cela signifie qu’une fois la case à cocher cochée, l’utilisateur n’est pas autorisé à la décocher.
- **Lorsque la case est décochée, la valeur renvoyée** - L’option vous permet de spécifier la valeur à associer à la case à cocher lorsqu’elle est dans un état non coché ou désélectionné.

- **Valeur par défaut**: cette option permet d’ajouter une valeur par défaut dans un champ de formulaire. Si **Composant désactivé** ou **Composant en lecture seule** est sélectionné, la valeur par défaut s’affiche à l’écran. Si aucune valeur n’est saisie par l’utilisateur dans le champ de formulaire, cette valeur est envoyée au moment de l’envoi du formulaire.

### Onglet Validation {#validation-tab}

![Onglet Validation](/help/adaptive-forms/assets/checkbox-validation.png)

- **Obligatoire** : Sélectionnez cette option si vous souhaitez afficher le composant dans un formulaire adaptatif. Après avoir sélectionné cette option, vous devez effectuer une sélection avant de poursuivre l’envoi du formulaire. Vous ne pouvez pas sélectionner **Masquer le composant** ou **Désactiver le composant**  dans l’onglet **De base** lorsque cette option est sélectionnée.

- **Message d’erreur** : Cette option vous permet de saisir un message qui s’affiche si la case à cocher **Obligatoire** est cochée et que le champ de formulaire reste vide.

- **Message de validation de script** : cette option permet de saisir un message à afficher en cas d’échec de la validation du script.

### Onglet Contenu de l’aide {#helpcontent-tab}

![Onglet Contenu d’aide](/help/adaptive-forms/assets/checkbox-help.png)

- **Description courte** : Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez l’option **Toujours afficher une description courte** pour l’afficher sous le composant.

- **Toujours afficher une description courte** - Activez cette option pour afficher la description courte sous le composant.

- **Texte d’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility-tab}

![Onglet Accessibilité](/help/adaptive-forms/assets/checkbox-accessibility.png)

**Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS du composant Case à cocher.

### Onglet Styles {#styles-tab}

Le composant principal de case à cocher Adaptive Forms prend en charge l’AEM [Système de style](/help/get-started/authoring.md#component-styling).

![Boîte de dialogue de conception.](/help/adaptive-forms/assets/checkbox-style.png)

- **Classes CSS par défaut** : vous pouvez fournir une classe CSS par défaut pour le composant principal du groupe de cases à cocher des formulaires adaptatifs.

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


