---
title: Composant principal Adaptive Forms - Termes et conditions
description: Utilisation ou personnalisation du composant principal Termes et conditions de Forms adaptatif .
role: Architect, Developer, Admin, User
exl-id: c607d554-ad2d-4434-856d-91e174ef3149
source-git-commit: a567b5ad937d426abe16c34e039e19cd0b1af5b0
workflow-type: tm+mt
source-wordcount: '2639'
ht-degree: 66%

---

# Composant Termes et conditions

A **Termes et conditions** fait référence à une section d’un formulaire qui décrit les conditions, règles et conditions auxquelles les utilisateurs doivent accepter ou se conformer lors de l’utilisation d’un service ou de l’accès à un contenu.

La variable **Termes et conditions** Le composant est un composant composite constitué de composants Texte, Case à cocher et Lien. Le composant de texte contient un titre ainsi qu’un bref aperçu de l’objectif et de la portée des termes et conditions. Elle comprend également une case à cocher permettant d’obtenir le consentement explicite de l’utilisateur. Vous pouvez également remplacer un texte de consentement par des liens.

**Exemple**

![conditions générales](/help/adaptive-forms/assets/terms-and-conditions.png)

Voir [Sous-composants du composant Termes et conditions](#sub-component) pour en savoir plus sur les différents composants du composant Termes et conditions .

## Utilisation {#reasons-to-use-termsandconditions}

- **Contrat utilisateur**: le composant sert de contrat entre le fournisseur de services et l’utilisateur. Les utilisateurs doivent accepter les conditions avant d’accéder au service ou au contenu.

- **Conformité juridique**: garantit la conformité juridique et la protection du prestataire en exposant les droits, les responsabilités et les responsabilités des deux parties.

- **Processus d’enregistrement**: les formulaires d’inscription ou d’inscription incluent la variable **Termes et conditions** , ce qui nécessite que les utilisateurs acceptent explicitement les conditions avant de créer un compte ou d’utiliser un service.

- **Transactions de commerce électronique**: les sites Web en ligne incluent la variable **Termes et conditions** afin que les utilisateurs soient invités à accepter les conditions générales dans le cadre du processus de paiement avant d’effectuer des achats en ligne.

- **Accords de sécurité et de confidentialité**: la variable **Termes et conditions** Le composant comprend des détails sur la manière dont les données utilisateur sont collectées, stockées et utilisées, souvent complétées par une politique de confidentialité distincte.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Accordéon des formulaires adaptatifs a été publié en février 2023 au sein des composants principaux 2.0.62 pour Cloud Service et des composants principaux 1.1.28 pour AEM 6.5.16.0 Forms ou version ultérieure. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec la <br>[version 2.0.62](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible avec les<br>[versions 1.1.28](/help/adaptive-forms/version.md) à 2.0.0 exclue. |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).

## Détails techniques {#technical-details}

Retrouvez les dernières informations sur le composant principal « Groupe de cases à cocher » des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkboxgroup/v1/checkboxgroup). Pour plus d’informations sur le développement des composants principaux, consultez la [Documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience de votre composant Conditions générales pour les visiteurs utilisant la boîte de dialogue Configurer . Vous pouvez également définir facilement des conditions générales pour une expérience utilisateur fluide.

### Onglet De base

![Onglet De base](/help/adaptive-forms/assets/terms-and-conditions-basic-tab.png)

- **Nom** - Le nom identifie de manière unique le composant dans l’éditeur de règles. Les caractères spéciaux et les espaces ne sont pas autorisés dans les chaînes de nom.

- **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

- **Afficher l’option d’approbation** - Sélectionnez l’option permettant d’afficher la case à cocher du consentement utilisé pour obtenir le consentement explicite de l’utilisateur.

- **Afficher sous forme de fenêtre contextuelle** - Sélectionnez l’option permettant d’afficher le composant Conditions générales dans une fenêtre contextuelle.

- **Remplacer le texte de consentement par un ou plusieurs liens Web**: sélectionnez l’option pour remplacer un texte de consentement par un lien web.  Si cette option est décochée, le texte du consentement s’affiche par défaut.

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

- **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.

- **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.
- **Désactiver le composant** - Sélectionnez cette option pour désactiver le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
- **Lecture seule** - Sélectionnez cette option pour rendre le composant non modifiable. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

### Onglet Contenu de l’aide {#help-content-tab}

![Onglet Contenu d’aide](/help/adaptive-forms/assets/terms-and-conditions-help-tab.png)

- **Description courte** : Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez l’option **Toujours afficher une description courte** pour l’afficher sous le composant.

- **Toujours afficher une description courte** - Activez cette option pour afficher la description courte sous le composant.

- **Texte d’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité

![Onglet Accessibilité](/help/adaptive-forms/assets/terms-and-conditions-accessibility-tab.png)

**Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS pour le composant Termes et conditions .


### Onglet Styles {#styles-tab}

Cet onglet vous permet de définir et de gérer les styles CSS d’un composant. Le composant principal Termes et conditions de Forms adaptatif prend en charge AEM [Système de style](/help/get-started/authoring.md#component-styling).

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

## Sous-composants du composant Termes et conditions {#sub-component}

**Termes et conditions** Un composant est un composant composite qui comprend les sous-composants suivants :
- [Composant Lien](#link)
- [Composant textuel](#text)
- [Composant de case à cocher](#checkbox)

### Composant Lien{#link}

Ce composant remplace un texte de consentement par un ou plusieurs liens web. Il est utilisé dans un scénario où l’utilisateur souhaite proposer des références à des sections spécifiques, des informations supplémentaires ou des documents externes. Vous pouvez facilement personnaliser la variable **Lien** pour les visiteurs qui utilisent la boîte de dialogue Configurer.

#### Onglet De base

![Onglet De base](/help/adaptive-forms/assets/link-basic-tab.png)

- **Nom** - Le nom identifie de manière unique le composant dans l’éditeur de règles. Les caractères spéciaux et les espaces ne sont pas autorisés dans les chaînes de nom.

- **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

- **Masquer le titre** - Sélectionnez cette option pour masquer le titre du composant.

- **Liens** - Indiquez le lien et le texte d’affichage correspondant utilisés à la place du texte de consentement. Vous pouvez ajouter plusieurs liens en cliquant sur le bouton **Ajouter** bouton .

- **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.

- **Marquer comme élément de formulaire non lié**: sélectionnez l’option de configuration d’un champ de formulaire non lié à un schéma. Cette option vous permet d’enregistrer des données sans mettre à jour la source de données. Il vous permet également de gérer les données de manière personnalisée, en les séparant de l’intégration de base de données standard.

- **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.

- **Désactiver le composant** - Sélectionnez l’option pour désactiver ou verrouiller le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
- **Lecture seule** - Sélectionnez cette option pour rendre le composant non modifiable. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

#### Onglet Validation

![Onglet Validation](/help/adaptive-forms/assets/link-validation-tab.png)

- **Obligatoire** : Sélectionnez cette option si vous souhaitez afficher le composant dans un formulaire adaptatif. Après avoir sélectionné cette option, vous devez effectuer une sélection avant de poursuivre l’envoi du formulaire. Vous ne pouvez pas sélectionner **Masquer le composant** ou **Désactiver le composant**  dans l’onglet **De base** lorsque cette option est sélectionnée.

- **Message d’erreur** : Cette option vous permet de saisir un message qui s’affiche si la case à cocher **Obligatoire** est cochée et que le champ de formulaire reste vide.

- **Message de validation de script** : cette option permet de saisir un message à afficher en cas d’échec de la validation du script.

### Onglet Contenu de l’aide {#helpcontent-tab}

![Onglet Contenu d’aide](/help/adaptive-forms/assets/link-help-tab.png)

- **Description courte** : Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez l’option **Toujours afficher une description courte** pour l’afficher sous le composant.

- **Toujours afficher une description courte** - Activez cette option pour afficher la description courte sous le composant.

- **Texte d’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité

![Onglet Accessibilité](/help/adaptive-forms/assets/link-accessibilty-tab.png)

**Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

### Composant textuel {#text}

**Texte** affiche le contenu textuel qui fournit des informations aux utilisateurs. Ce composant comprend les conditions générales, la langue juridique ou toute autre information textuelle pertinente.

Vous pouvez facilement personnaliser la variable [Composant textuel](/help/adaptive-forms/components/text.md) individuellement pour les visiteurs qui utilisent la boîte de dialogue Configurer . Pour définir facilement des options de texte pour une expérience utilisateur transparente, utilisez la méthode [configurer la boîte de dialogue du composant Texte](/help/adaptive-forms/components/text.md#configure-dialog).


### Composant de case à cocher {#checkbox}

Une case à cocher permet d’obtenir le consentement ou l’accusé de réception de l’utilisateur. Il sert d’indicateur visuel que l’utilisateur a lu et accepté les termes décrits. Il est obligatoire de cocher la case pour indiquer le consentement de l’utilisateur.

Vous pouvez facilement personnaliser la variable [Composant de case à cocher](/help/adaptive-forms/components/checkbox.md) individuellement pour les visiteurs qui utilisent la boîte de dialogue Configurer . Pour définir les propriétés d’une case à cocher pour une expérience utilisateur transparente, utilisez la méthode [Configuration de la boîte de dialogue du composant de case à cocher](/help/adaptive-forms/components/checkbox.md#configure-dialog).


## Articles connexes {#related-articles}

{{more-like-this}}

## Voir également {#see-also}

{{see-also}}
