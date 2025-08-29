---
title: Composant principal de Forms adaptatif - Signature tactile
description: Utilisation ou personnalisation du composant principal de signature tactile du Forms adaptatif.
role: Architect, Developer, Admin, User
source-git-commit: 4218af42d947e19a65efe8839ccd4eb102fe2f21
workflow-type: tm+mt
source-wordcount: '1732'
ht-degree: 80%

---


# Composant Signature tactile

Un composant Signature tactile dans un formulaire adaptatif est un élément de l’interface utilisateur qui permet aux utilisateurs et aux utilisatrices de tracer leur **signature** directement dans le formulaire à l’aide d’une souris, d’un stylet ou d’un écran tactile. Elle garantit la capture précise du consentement écrit à la main, des approbations ou de la vérification dans les workflows numériques.

**Exemple**

![exemple](/help/adaptive-forms/assets/scribble-signature.png){width=50%,align-center}

**Diverses options disponibles dans la fenêtre de signature**

- **A :** cliquez sur l’icône **Dessiner** pour tracer votre signature sur la zone de travail.
- **B :** cliquez sur l’icône **Effacer** pour effacer la signature sur la zone de travail.
- **C :** cliquez sur l’icône **Géolocalisation** pour ajouter une géolocalisation avec la signature.
- **D :** cliquez sur l’icône **Clavier** pour saisir votre nom sur la zone de travail.

Une fois que vous avez sélectionné l’icône **Enregistrer** dans la fenêtre de signature tactile, vous ne pouvez plus modifier la signature. Si vous souhaitez modifier la signature, vous devez ignorer la signature actuelle et la signer à nouveau à l’aide de l’option Pinceau/Clavier ci-dessus.

>[!NOTE]
>
> Les signatures sont toujours enregistrées au format PNG.

## Utilisation {#reasons-to-use-scribble-signature}

Il existe plusieurs raisons d’inclure un champ de signature tactile dans un formulaire, notamment :

- **Consentement numérique** : permet aux utilisateurs de fournir électroniquement des signatures légalement valides.
- **Expérience utilisateur améliorée** : permet de se connecter directement et naturellement aux appareils sans analyser ni charger.
- **Workflows sans papier** : élimine le besoin d’imprimer, de signer et de numériser à nouveau des documents.
- **Authentification** : agit comme une couche supplémentaire de confirmation et d’approbation.
- **Précision des données** : garantit la capture correcte de l’entrée manuscrite du signataire sous forme numérique.

## Version et compatibilité {#version-and-compatibility}

Le composant principal de signature tactile Forms adaptative a été publié en **août 2025** dans le cadre de **composants principaux 2.24.6** pour Cloud Service et versions ultérieures.

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec la <br>[version 2.24.6](/help/adaptive-forms/version.md) et les versions ultérieures | |

Pour plus d’informations sur les versions, voir [Versions des composants principaux](/help/adaptive-forms/version.md).

## Détails techniques {#technical-details}

Obtenez les derniers détails techniques sur le composant principal de la signature tactile du Forms adaptatif sur [GitHub](https://github.com/adobe/aem-core-forms-components). Pour plus d’informations sur le développement des composants principaux, voir [Documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet de personnaliser le composant Signature tactile.

### Onglet De base {#basic-tab}

![Onglet De base](/help/adaptive-forms/assets/scribble-signature-basictab.png)

- **Nom** - Le nom identifie de manière unique le composant dans l’éditeur de règles. Les caractères spéciaux et les espaces ne sont pas autorisés dans les chaînes de nom.

- **Titre** - Le titre est une chaîne qui s’affiche en haut d’un composant dans un formulaire adaptatif. Le titre identifie de manière unique le composant dans l’arborescence d’un formulaire adaptatif. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.
- **Autoriser le texte enrichi pour le titre** - Cette fonctionnalité permet aux personnes de mettre en forme les titres en texte brut en y incorporant des fonctionnalités telles que le texte en gras, en italique et souligné, diverses polices, tailles de police et couleurs, et d’autres options pour améliorer la présentation visuelle et la personnalisation. Elle offre une plus grande flexibilité et un contrôle créatif pour faire ressortir les titres dans les documents, sites web ou applications.\
  Lorsque vous cochez la case **Autoriser le texte enrichi pour le titre**, les options de formatage deviennent visibles pour appliquer un style au titre du composant. Pour accéder à toutes les options de formatage disponibles, vous pouvez cliquer sur l’onglet ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Prise en charge de texte enrichi](/help/adaptive-forms/assets/richtext-support-title.png)

- **Masquer le titre** - Sélectionnez cette option pour masquer le titre du type de composant dans un formulaire adaptatif.
- **Texte d’espace réservé** - Le texte d’espace réservé dans un composant de formulaire fait référence à un libellé court ou à un prompt qui apparaît dans un champ de saisie comme conseil à l’utilisateur ou à l’utilisatrice sur le type d’information à saisir dans ce champ. Le texte d’espace réservé disparaît lorsque l’utilisateur ou l’utilisatrice commence à saisir du texte dans le champ et réapparaît si le champ est vide. Il fournit un indice visuel à l’utilisateur ou à l’utilisatrice, mais n’agit pas comme une valeur ou un libellé permanent pour le champ.

- **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.

- **Marquer comme élément de formulaire non lié** : sélectionnez cette option pour configurer un champ de formulaire qui n’est lié à aucun schéma. Cette option vous permet d’enregistrer des données sans mettre à jour la source de données. Elle vous permet également de gérer les données de manière personnalisée, en les séparant de l’intégration de base de données standard.

- **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.
- **Désactiver le composant** - Sélectionnez cette option pour désactiver le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

- **Titre de la boîte de dialogue de signature** : le titre de la boîte de dialogue de signature définit le texte affiché en haut de la boîte de dialogue de capture de signature. Il sert d’invite ou d’instruction à l’utilisateur lorsqu’il est tenu de fournir une signature. Le texte guide l’utilisateur tout au long du processus de signature, rendant l’interaction claire et intuitive.

### Onglet Validation

![onglet validation](/help/adaptive-forms/assets/scribble-signature-validation.png)

- **Obligatoire** : Sélectionnez cette option si vous souhaitez afficher le composant dans un formulaire adaptatif. Après avoir sélectionné cette option, vous devez effectuer une sélection avant de poursuivre l’envoi du formulaire. Vous ne pouvez pas sélectionner **Masquer le composant** ou **Désactiver le composant** sous l’onglet **De base** lorsque cette option est sélectionnée.

- **Message d’erreur** : cette option vous permet de rédiger un message qui s’affiche si la case à cocher **Obligatoire** est activée et le champ de formulaire reste vide.

- **Message de validation de script** : cette option permet de saisir un message à afficher en cas d’échec de la validation du script.

### Onglet Contenu de l’aide {#help-content-tab}

![Onglet Contenu d’aide](/help/adaptive-forms/assets/scribble-signature-helptab.png)

- **Description courte** : Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Sélectionnez l’option **Toujours afficher la description courte** pour l’afficher sous le composant.

- **Toujours afficher la description courte** : sélectionnez cette option pour afficher la description courte sous le composant.

- **Texte de l’aide** : le texte d’aide prodigue des informations supplémentaires ou des conseils à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility-tab}

![Onglet Accessibilité](/help/adaptive-forms/assets/scribble-signature-accessibilitytab.png)

- **Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.
   - **Texte personnalisé** : sélectionnez cette option pour utiliser le texte personnalisé pour les libellés d’accessibilité ARIA. Cette option affiche la boîte de dialogue Texte personnalisé. Vous pouvez ajouter des informations pertinentes dans la boîte de dialogue Texte personnalisé.
   - **Description** : sélectionnez cette option pour utiliser la description des libellés d’accessibilité ARIA.
   - **Titre** : sélectionnez cette option pour utiliser le titre pour les libellés d’accessibilité ARIA.
   - **Nom** : sélectionnez cette option pour utiliser le nom pour les libellés d’accessibilité ARIA.
   - **Aucun** : sélectionnez cette option si vous ne souhaitez pas ajouter de texte supplémentaire pour les libellés d’accessibilité ARIA.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS du composant Signature tactile.

### Onglet Styles {#styles-tab}

Cet onglet vous permet de définir et de gérer les styles CSS d’un composant. Le composant principal de signature tactile Forms adaptative prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

![Boîte de dialogue de conception](/help/adaptive-forms/assets/checkbox-style.png)

- **Classes CSS par défaut** : vous pouvez fournir une classe CSS par défaut pour le composant principal de la signature tactile du Forms adaptatif.

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
