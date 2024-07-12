---
title: Composant principal des formulaires adaptatifs – Composant de commutateur
description: Utilisation ou personnalisation du composant principal Commutateur des formulaires adaptatifs.
role: Architect, Developer, Admin, User
exl-id: 6ff2ca76-1514-42eb-bde3-60259af2d187
source-git-commit: 4c510b8fe59f4be6e1b329ee4257ab1b780fbf22
workflow-type: tm+mt
source-wordcount: '1922'
ht-degree: 100%

---

# Composant Commutateur du formulaire adaptatif{#switch-adaptive-forms-core-component}

Le composant de commutateur est une interface utilisateur graphique utilisée dans les formulaires qui permet aux utilisateurs et utilisatrices de choisir entre deux options. Il s’agit généralement d’un bouton (bascule) à deux états qui permet aux utilisateurs et aux utilisatrices de choisir entre deux états, permettant d’activer ou de désactiver une fonction, un paramètre ou une fonctionnalité. Le composant de commutateur est conçu pour représenter visuellement l’état actuel et indiquer si une fonction particulière est activée ou désactivée.

Le composant de commutateur est un élément de contrôle booléen qui définit la valeur sur vrai (true) ou faux (false). Par exemple, il est utilisé pour activer ou désactiver une fonction, comme couper ou activer le son, ou activer ou désactiver le Bluetooth ou le Wi-Fi.

![Exemple de composant de commutateur.](/help/adaptive-forms/assets/switch-example.png)

## Utilisation {#reasons-to-use-switch}

Les raisons courantes d’utiliser un commutateur dans un formulaire adaptatif sont les suivantes :

- **Interaction des utilisateurs et utilisatrices** : les utilisateurs et utilisatrices peuvent interagir avec le composant de commutateur en cliquant ou en appuyant dessus.

- **États** : le composant de commutateur a deux états : activé et désactivé. L’état initial du composant de commutateur dépend du paramètre par défaut ou du statut actuel de la fonction qu’il contrôle.

- **Représentation visuelle** : le composant de commutateur reflète visuellement son état actuel en changeant de couleur ou de position.

- **Fonctionnalité de contrôle** : le composant de commutateur est utilisé pour activer ou désactiver des fonctionnalités spécifiques dans un formulaire AEM. Par exemple, il permet aux utilisateurs et utilisatrices d’activer ou de désactiver une fonction.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Commutateur des formulaires adaptatifs a été publié dans le cadre de la version 2.0.64 des composants principaux. Voici un tableau présentant toutes les versions prises en charge, la compatibilité AEM et les liens vers la documentation correspondante :

|  |  |
|---|---|
| Version du composant | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatible avec la <br>[version 2.0.64](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible | Compatible |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).

## Détails techniques {#technical-details}

Retrouvez les dernières informations sur le composant principal Commutateur des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/switch/v1/switch). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience du composant Commutateur pour les visiteurs et les visiteuses à l’aide de la boîte de dialogue Configurer. Vous pouvez également définir facilement des options de composant Commutateur pour une expérience client fluide.

### Onglet De base

![Onglet De base](/help/adaptive-forms/assets/switch-basic.png)

- **Nom** - Vous pouvez identifier facilement un composant de formulaire en lui attribuant un nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

- **Titre** – Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche à côté du composant. Si vous n’ajoutez pas de titre, le composant ne s’affiche pas.
- **Autoriser le texte enrichi pour le titre** - Cette fonctionnalité permet aux personnes de mettre en forme les titres en texte brut en y incorporant des fonctionnalités telles que le texte en gras, en italique et souligné, diverses polices, tailles de police et couleurs, et d’autres options pour améliorer la présentation visuelle et la personnalisation. Elle offre une plus grande flexibilité et un contrôle créatif pour faire ressortir les titres dans les documents, sites web ou applications.\
  Lorsque vous cochez la case **Autoriser le texte enrichi pour le titre**, les options de formatage deviennent visibles pour appliquer un style au titre du composant. Pour accéder à toutes les options de formatage disponibles, vous pouvez cliquer sur l’onglet ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Prise en charge de texte enrichi](/help/adaptive-forms/assets/richtext-support-title.png)

- **Masquer le titre** - Sélectionnez cette option pour masquer le titre du composant.

- **Conserver la valeur de l’état décochée** – La sélection de cette option vous permet de spécifier la valeur à renvoyer lorsque le composant de commutateur n’est pas sélectionné.
- **Options** – Spécifiez la valeur des données et le texte d’affichage pour chaque option.
   - **Valeur des données activée** – Spécifiez la valeur à envoyer lorsque le commutateur est activé dans un formulaire adaptatif.
   - **Texte d’affichage activé** – Spécifiez le texte à afficher en tant que libellé lorsque le commutateur est activé dans un formulaire adaptatif.
   - **Valeur des données désactivée** – Spécifiez la valeur à envoyer lorsque le commutateur n’est pas activé dans un formulaire adaptatif. Cette option n’est visible que si le commutateur **Conserver la valeur de l’état décochée** est activé.
   - **Texte d’affichage désactivé** – Spécifiez le texte à afficher en tant que libellé lorsque le commutateur n’est pas activé dans un formulaire adaptatif. Cette option n’est visible que si le commutateur **Conserver la valeur de l’état décochée** est activé.

  Vous pouvez également mettre en forme les options du composant de commutateur à l’aide de **Autoriser le texte enrichi pour les options**.

  ![Prise en charge du texte enrichi pour les options](/help/adaptive-forms/assets/switch-optipn-rich-text.png)

  Une fois que vous avez coché la case **Autoriser le texte enrichi pour les options** les options de formatage deviennent visibles pour appliquer un style aux options du composant. Pour accéder à toutes les options de formatage disponibles, vous pouvez cliquer sur l’onglet `Fullscreen` ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Prise en charge du texte enrichi pour les options](/help/adaptive-forms/assets/switch-richtext-for-display.png)

- **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.
- **Marquer comme élément de formulaire non lié** : sélectionnez cette option pour configurer un champ de formulaire qui n’est lié à aucun schéma. Cette option vous permet d’enregistrer des données sans mettre à jour la source de données. Elle vous permet également de gérer les données de manière personnalisée, en les séparant de l’intégration de base de données standard.

- **Type de données de la valeur envoyée** : cette option spécifie le type de données de la valeur envoyée lorsqu’une option est sélectionnée. Si le **type de données de la valeur envoyée** est défini sur `Number` et que vous ajoutez des données de chaîne à la **Valeur des données** dans l’onglet **Options**, l’écran affiche un message d’erreur `Value type mismatch`.
- **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.

- **Désactiver le composant** – Sélectionnez cette option pour désactiver le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

- **Valeur par défaut** – Cette option vous permet d’ajouter une valeur par défaut dans un champ de formulaire. Si **Composant désactivé** ou **Composant en lecture seule** est sélectionné, la valeur par défaut s’affiche à l’écran. Si aucune valeur n’est saisie par l’utilisateur ou l’utilisatrice dans le champ de formulaire, cette valeur est envoyée au moment de l’envoi du formulaire.

### Onglet Validation {#validation-tab}

![Onglet Validation](/help/adaptive-forms/assets/switch-validation.png)

- **Obligatoire** : Sélectionnez cette option si vous souhaitez afficher le composant dans un formulaire adaptatif. Après avoir sélectionné cette option, vous devez effectuer une sélection avant de poursuivre l’envoi du formulaire. Vous ne pouvez pas sélectionner **Masquer le composant** ou **Désactiver le composant**  dans l’onglet **De base** lorsque cette option est sélectionnée.

- **Message d’erreur** : cette option vous permet de rédiger un message qui s’affiche si la case à cocher **Obligatoire** est activée et le champ de formulaire reste vide.

- **Message de validation de script** : cette option permet de saisir un message à afficher en cas d’échec de la validation du script.

### Onglet Contenu de l’aide {#helpcontent-tab}

![Onglet Contenu d’aide](/help/adaptive-forms/assets/switch-help.png)

- **Description courte** : Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez l’option **Toujours afficher une description courte** pour l’afficher sous le composant.

- **Toujours afficher une description courte** - Activez cette option pour afficher la description courte sous le composant.

- **Texte d’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility-tab}

![Onglet Accessibilité](/help/adaptive-forms/assets/switch-accessibility.png)

- **Texte pour les lecteurs d’écran** : le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.
   - **Texte personnalisé** : sélectionnez cette option pour utiliser le texte personnalisé pour les libellés d’accessibilité ARIA. Cette option affiche la boîte de dialogue Texte personnalisé. Vous pouvez ajouter des informations pertinentes dans la boîte de dialogue Texte personnalisé.
   - **Description** : sélectionnez cette option pour utiliser la description des libellés d’accessibilité ARIA.
   - **Titre** : sélectionnez cette option pour utiliser le titre pour les libellés d’accessibilité ARIA.
   - **Nom** : sélectionnez cette option pour utiliser le nom pour les libellés d’accessibilité ARIA.
   - **Aucun** : sélectionnez cette option si vous ne souhaitez pas l’ajouter pour les libellés d’accessibilité ARIA.

### Onglet Styles {#styles-tab}

![Onglet Styles](/help/adaptive-forms/assets/switch-styles.png)

- **Masquer les libellés** – Sélectionnez cette option pour masquer les libellés du composant de commutateur.

- **Afficher les libellés** – Sélectionnez cette option pour afficher les libellés du composant de commutateur.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS du composant Commutateur.

### Onglet Styles {#styles-design-tab}

Le composant principal Commutateur des formulaires adaptatifs prend en charge le [Système de style](/help/get-started/authoring.md#component-styling) d’AEM.

![Boîte de dialogue de conception.](/help/adaptive-forms/assets/checkbox-style.png)

- **Classes CSS par défaut** : vous pouvez fournir une classe CSS par défaut pour le composant principal Commutateur des formulaires adaptatifs.

- **Styles autorisés** : vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé « texte en gras » et fournir la classe CSS « police d’épaisseur : gras ». Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de formulaires adaptatifs. Pour appliquer un style, sélectionnez le composant auquel vous souhaitez appliquer le style dans l’éditeur de formulaires adaptatifs, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans la liste déroulante **Styles**. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

### Propriétés personnalisées

![Boîte de dialogue Propriétés personnalisées](/help/adaptive-forms/assets/checkbox-customproperties.png)

Les propriétés personnalisées vous permettent d’associer des attributs personnalisés (paires clé-valeur) à un composant principal de formulaire adaptatif à l’aide du modèle de formulaire. Les propriétés personnalisées sont répercutées dans la section des propriétés du rendu déocuplé du composant. Cela permet de créer un comportement de formulaire dynamique qui s’adapte en fonction des valeurs d’attributs personnalisés. Par exemple, les développeurs et développeuses peuvent concevoir plusieurs rendus d’un composant de formulaires découplés pour des plateformes mobiles, de bureau ou web, ce qui améliore considérablement l’expérience client sur un large éventail d’appareils.
- **Nom du groupe** : vous pouvez fournir un nom pour identifier le groupe de propriétés personnalisées. Vous pouvez ajouter, supprimer ou réorganiser plusieurs groupes de propriétés personnalisées. Après avoir ajouté le groupe de propriétés personnalisées, vous pouvez voir les options suivantes :

   - **Paires clé-valeur** : vous pouvez ajouter plusieurs noms et valeurs de propriétés personnalisées en cliquant sur le bouton **Ajouter** pour chaque groupe de propriétés personnalisées.

   - **Supprimer** : appuyez ou cliquez pour supprimer le nom et la valeur des propriétés personnalisées.

   - **Réorganiser** : appuyez ou cliquez et faites glisser pour réorganiser le nom et la valeur des propriétés personnalisées.

## Articles connexes {#related-articles}

{{more-like-this}}

## Voir également {#see-also}

{{see-also}}
