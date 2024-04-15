---
title: Composant principal des formulaires adaptatifs - Entrée de nombre
description: Utilisation ou personnalisation du composant principal « Entrée de nombre » dans les formulaires adaptatifs.
role: Architect, Developer, Admin, User
exl-id: 75604ecf-1ec5-4e97-b934-d6ed49726147
source-git-commit: e843ccf5c030cd4f1015e3290347b5799828537a
workflow-type: tm+mt
source-wordcount: '2103'
ht-degree: 94%

---

# Entrée de nombre {#number-input-adaptive-forms-core-component}

<span class="preview"> Cet article contient du contenu sur la variable **Autoriser le texte enrichi pour le titre** fonctionnalité , une fonctionnalité de version préliminaire. La fonctionnalité de version préliminaire n’est accessible que par le biais de notre [canal de version préliminaire](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html#new-features).</span>

Dans un formulaire adaptatif, un composant « entrée de nombre » est un type de champ de formulaire qui permet aux utilisateurs et utilisatrices de saisir des valeurs numériques. Le composant est généralement représenté par un champ de texte avec une flèche vers le haut et vers le bas pour incrémenter et décrémenter le nombre.

Il peut également être utilisé avec des attributs tels que min, max, étape, valeur, etc. Ces attributs peuvent être utilisés pour définir les valeurs minimale et maximale autorisées dans le champ, l’intervalle d’étape pour incrémenter ou décrémenter le nombre et la valeur par défaut du champ.

Ce composant peut être utilisé pour collecter des données numériques telles que l’âge, la quantité, etc. Il peut également être utilisé pour effectuer des opérations mathématiques, comme l’addition et la soustraction. Ce composant peut également être utilisé pour valider les données numériques saisies par l’utilisateur ou l’utilisatrice.

Pour l’accessibilité, il est important de spécifier un « libellé » qui décrit l’objectif du champ d’entrée de nombre et le type d’entrée attendu.

**Exemple**

![exemple](/help/adaptive-forms/assets/numeric-stepper.png)

## Utilisation {#reasons-to-use-number-input-numeric-stepper}

Il existe plusieurs raisons d’inclure un composant « Entrée de nombre » dans un formulaire adaptatif, notamment :

- **Opérations mathématiques** : les champs numériques peuvent être utilisés pour effectuer des opérations mathématiques telles que l’addition, la soustraction, la multiplication et la division.

- **Plage de données** : les champs numériques peuvent être utilisés pour définir une plage de valeurs valides à l’aide des attributs min, max et étape.

- **Contenu dynamique** : un composant numérique peut être utilisé pour afficher des données dynamiques en fonction des champs du formulaire.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Accordéon des formulaires adaptatifs a été publié en février 2023 au sein des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec la <br>[version 2.0.4](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible avec les<br>[versions 1.1.12](/help/adaptive-forms/version.md) à 2.0.0 exclue. |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Retrouvez les informations les plus récentes sur le composant principal « Entrée de nombre » des formulaires adaptatif dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/numberinput/v1/numberinput). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience d’entrée de nombre pour les visiteurs à l’aide de la boîte de dialogue Configurer. Vous pouvez également définir facilement des options d’entrée de nombre pour une expérience utilisateur fluide.

### Onglet De base {#basic-tab}

![Onglet De base](/help/adaptive-forms/assets/numberinput_basictab.png)

- **Nom** - Vous pouvez identifier facilement un composant de formulaire avec son nom unique aussi bien dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

- **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.
- **Autoriser le texte enrichi pour le titre** - Cette fonctionnalité permet aux utilisateurs de mettre en forme les titres en texte brut en y incorporant des fonctionnalités telles que le gras, l’italique, le texte souligné, diverses polices, la taille des polices, les couleurs et d’autres options pour améliorer la présentation visuelle et la personnalisation. Il offre une plus grande flexibilité et un contrôle créatif pour faire ressortir les titres dans les documents, sites web ou applications.\
  Lorsque vous cochez la case pour **Autoriser le texte enrichi pour le titre** , les options de mise en forme deviennent visibles pour appliquer un style au titre du composant. Pour accéder à toutes les options de formatage disponibles, vous pouvez cliquer sur le ![Icône Plein écran](/help/adaptive-forms/assets/fullscreen-icon.png) .

  ![Prise en charge du texte enrichi](/help/adaptive-forms/assets/richtext-support-title.png)

- **Masquer le titre** - Sélectionnez cette option pour masquer le titre du composant.
- **Texte d’espace réservé** - Le texte d’espace réservé dans un composant de formulaire fait référence à un libellé court ou à une invite qui apparaît dans un champ de saisie comme conseil à l’utilisateur ou à l’utilisatrice sur le type d’information à saisir dans ce champ. Le texte d’espace réservé disparaît lorsque l’utilisateur ou l’utilisatrice commence à saisir du texte dans le champ et réapparaît si le champ est vide. Il fournit un indice visuel à l’utilisateur ou à l’utilisatrice, mais n’agit pas comme une valeur ou un libellé permanent pour le champ.
- **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.
- **Marquer comme élément de formulaire non lié** : sélectionnez cette option pour configurer un champ de formulaire qui n’est lié à aucun schéma. Cette option vous permet d’enregistrer des données sans mettre à jour la source de données. Elle vous permet également de gérer les données de manière personnalisée, en les séparant de l’intégration de base de données standard.
- **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.
- **Désactiver le composant** - Sélectionnez cette option pour désactiver le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
- **Lecture seule** - Sélectionnez cette option pour rendre le composant non modifiable. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas le modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
- **Type de nombre** - Cette option permet de sélectionner le type de valeurs numériques autorisé dans le champ du formulaire. Vous pouvez sélectionner les types Décimal ou Entier dans le menu déroulant.
- **Valeur par défaut** - Cette option vous permet d’ajouter une valeur par défaut dans un champ de formulaire. Si **Composant désactivé** ou **Composant en lecture seule** est sélectionné, la valeur par défaut s’affiche à l’écran. Si aucune valeur n’est saisie par l’utilisateur ou l’utilisatrice dans le champ de formulaire, cette valeur est envoyée au moment de l’envoi du formulaire.

### Onglet Validation {#validation-tab}

![Onglet Validation](/help/adaptive-forms/assets/numberinput_validationtab.png)

- **Obligatoire** : Sélectionnez cette option si vous souhaitez afficher le composant dans un formulaire adaptatif. Après avoir sélectionné cette option, vous devez saisir une valeur avant de poursuivre l’envoi du formulaire. Vous ne pouvez pas sélectionner **Masquer le composant** ou **Désactiver le composant**  dans l’onglet **De base** lorsque cette option est sélectionnée.

- **Message d’erreur** - Cette option vous permet de saisir un message qui s’affiche si la case à cocher **Obligatoire** est cochée et que le champ n’est pas renseigné.

- **Message de validation de script** - Cette option permet de saisir un message à afficher en cas d’échec de la validation du script.

- **Nombre le plus bas/Nombre le plus petit** - Utilisez cette option pour sélectionner le nombre minimum autorisé pouvant être renseigné dans le champ de formulaire. Si une valeur inférieure au nombre spécifié dans **Nombre le plus bas/Nombre le plus petit** est saisie dans le champ de formulaire, le message d’erreur s’affiche.

- **Message d’erreur minimum** - Cette option vous permet de saisir un message d’erreur qui s’affiche lorsque l’utilisateur ou l’utilisatrice saisit une valeur inférieure à celle spécifiée dans l’option **Nombre minimum**.

- **Exclure la valeur minimum** - Cochez cette case si vous ne souhaitez pas que la valeur minimum indiquée dans l’option **Nombre le plus bas/Nombre le plus petit** soit incluse dans la plage de valeurs à renseigner dans le champ du formulaire.

- **Nombre le plus élevé/Nombre le plus grand** - Utilisez cette option pour sélectionner le nombre maximal autorisé pouvant être renseigné dans le champ de formulaire. Si un nombre supérieur au nombre spécifié dans **Nombre le plus élevé/Nombre le plus grand** est saisi dans le champ de formulaire, le message d’erreur s’affiche.

- **Message d’erreur maximum** - Cette option vous permet de saisir un message d’erreur qui s’affiche lorsque l’utilisateur ou l’utilisatrice saisit une valeur supérieure à celle spécifiée dans l’option **Nombre le plus élevé/Nombre le plus grand**.

- **Exclure la valeur maximale** - Cochez cette case si vous ne souhaitez pas que la valeur maximale indiquée dans l’option **Nombre le plus élevé/Nombre le plus grand** soit incluse dans la plage de valeurs à renseigner dans le champ du formulaire.

### Onglet Contenu de l’aide {#help-content}

![Onglet Contenu d’aide](/help/adaptive-forms/assets/numberinput_helptab.png)

- **Description courte** : Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez l’option **Toujours afficher une description courte** pour l’afficher sous le composant.

- **Toujours afficher une description courte** - Activez cette option pour afficher la description courte sous le composant.

- **Texte d’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility}

![Onglet Accessibilité](/help/adaptive-forms/assets/numberinput_accessibility.png)

**Texte pour les lecteurs d’écran** : le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

### Onglet Formats {#formats-configure-tab}

![Onglet Accessibilité](/help/adaptive-forms/assets/numberinput_formattab.png)

- **Format d’affichage** : Cette option permet de sélectionner un format de type entier-numérique pour l’affichage. Lorsque l’utilisateur ou l’utilisatrice sélectionne une option dans le menu déroulant **Type**, l’option **Format** apparaît dans le panneau. Vous pouvez choisir un format spécifique dans lequel les nombres s’affichent pour l’utilisateur ou l’utilisatrice.

<!--   **Number of digits before the decimal separator (1234.000)** - Use this option to specify the number of digits to display before the decimal point. 

- **Number of digits after the decimal separator (1234.000)** - Use this option to specify the number of digits to display after the decimal point. -->

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS pour le composant Entrée de nombre.

### Onglet Styles {#styles-tab}

Cet onglet vous permet de définir et de gérer les styles CSS d’un composant. Le composant principal « Entrée de nombre » des formulaires adaptatifs prend en charge le [Système de style](/help/get-started/authoring.md#component-styling) d’AEM.

![Onglet Styles.](/help/adaptive-forms/assets/datepicker_styletab.png)

- **Classes CSS par défaut** : vous pouvez fournir une classe CSS par défaut pour le composant principal Entrée de nombre des formulaires adaptatifs.

- **Styles autorisés** : vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé « texte en gras » et fournir la classe CSS « police d’épaisseur : gras ». Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de formulaires adaptatifs. Pour appliquer un style, sélectionnez le composant auquel vous souhaitez appliquer le style dans l’éditeur de formulaires adaptatifs, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans la liste déroulante **Styles**. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

### Propriétés personnalisées

![Boîte de dialogue Propriétés personnalisées](/help/adaptive-forms/assets/datepicker_customproperties.png)

Les propriétés personnalisées vous permettent d’associer des attributs personnalisés (paires clé-valeur) à un composant principal de formulaire adaptatif à l’aide du modèle de formulaire. Les propriétés personnalisées sont répercutées dans la section des propriétés du rendu déocuplé du composant. Cela permet de créer un comportement de formulaire dynamique qui s’adapte en fonction des valeurs d’attributs personnalisés. Par exemple, les développeurs et développeuses peuvent concevoir plusieurs rendus d’un composant de formulaires découplés pour des plateformes mobiles, de bureau ou web, ce qui améliore considérablement l’expérience client sur un large éventail d’appareils.

- **Nom du groupe** : vous pouvez fournir un nom pour identifier le groupe de propriétés personnalisées. Vous pouvez ajouter, supprimer ou réorganiser plusieurs groupes de propriétés personnalisées. Après avoir ajouté le groupe de propriétés personnalisées, vous pouvez voir les options suivantes :

   - **Paires clé-valeur** : vous pouvez ajouter plusieurs noms et valeurs de propriétés personnalisées en cliquant sur le bouton **Ajouter** pour chaque groupe de propriétés personnalisées.

   - **Supprimer** : appuyez ou cliquez pour supprimer le nom et la valeur des propriétés personnalisées.

   - **Réorganiser** : appuyez ou cliquez et faites glisser pour réorganiser l’ordre du nom et de la valeur des propriétés personnalisées.

### Onglet Formats {#formats-tab}

L’onglet Formats vous permet de définir des formats de date par défaut et personnalisés.

![Onglet Format.](/help/adaptive-forms/assets/emailinput_formattab.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Articles connexes {#related-articles}

{{more-like-this}}

## Voir également {#see-also}

{{see-also}}
