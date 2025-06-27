---
title: Composant principal des formulaires adaptatifs - Image
description: Utilisation ou personnalisation du composant principal « Image » des formulaires adaptatifs.
role: Architect, Developer, Admin, User
exl-id: 9ee42d5d-16e3-4973-8364-5bc512ebe72e
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '1056'
ht-degree: 100%

---


# Composant Image{#image-adaptive-forms-core-component}

Un composant « Image » dans un formulaire adaptatif permet d’inclure des images dans un formulaire. Ces images peuvent être utilisées pour améliorer la conception globale du formulaire, fournir des informations supplémentaires ou servir d’aide visuelle pour aider les utilisateurs et les utilisatrices à comprendre l’objectif du formulaire. Le composant « Image » peut être utilisé pour ajouter un logo, une photo ou un graphique dans le formulaire.

Pour l’accessibilité, il est important de spécifier le **Texte secondaire** de l’image afin de fournir un texte de remplacement court et descriptif qui décrit l’image aux utilisateurs et utilisatrices qui ne peuvent pas la voir.

{{traditional-aem}}

**Exemple**

![exemple](/help/adaptive-forms/assets/image.png)


## Utilisation {#reasons-to-use-image-in-a-form}

Il existe plusieurs raisons d’inclure un composant « Image » dans un formulaire adaptatif, notamment :

- **Image de marque** : une image peut être utilisée pour afficher le logo ou le nom de l’organisation qui a créé le formulaire, ce qui contribue à établir la reconnaissance et la crédibilité de la marque.

- **Supports visuels** : une image peut aider à fournir un niveau d’information supplémentaire aux utilisateurs et aux utilisatrices, en fournissant un support visuel pour aider les utilisateurs et utilisatrices à comprendre l’objectif du formulaire.

- **Décoration** : une image peut être utilisée pour améliorer la conception globale du formulaire et le rendre plus attrayant visuellement.

- **Expérience utilisateur** : une image peut être utilisée pour rendre le formulaire plus convivial en offrant une méthode claire et intuitive d’accès et de remplissage des champs de formulaire.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Image des formulaires adaptatifs a été publié en février 2023 au sein des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec la <br>[version 2.0.4](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible avec les<br>[versions 1.1.12](/help/adaptive-forms/version.md) à 2.0.0 exclue. |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_fr). -->

## Détails techniques {#technical-details}

Retrouvez les informations les plus récentes sur le composant principal « Image » des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/image/v1/image). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).


## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience d’image pour les visiteurs et les visiteuses à l’aide de la boîte de dialogue Configurer. Vous pouvez également définir facilement des options d’image pour une expérience utilisateur fluide.

![Onglet Propriétés](/help/adaptive-forms/assets/image_properties.png)

- **Nom** - Vous pouvez identifier facilement un composant de formulaire en lui attribuant un nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

- **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

- **Marquer comme élément de formulaire non lié** : sélectionnez cette option pour configurer un champ de formulaire qui n’est lié à aucun schéma. Cette option vous permet d’enregistrer des données sans mettre à jour la source de données. Elle vous permet également de gérer les données de manière personnalisée, en les séparant de l’intégration de base de données standard.

<!--   **Document of Record bind reference** - This option allows you to associate an Adaptive Form field with Document of Record field. When user enters any value in a linked field of an Adaptive Form that value also appears in the linked field of the corresponding Document of Record. For example, a Document of Record bind reference can be used to display a customer's name and address in a Document of Record, based on the customer's ID entered into the form. In this way, AEM Forms enable you to generate Document of Record and offers a seamless user experience for collecting and managing data.-->

- **Description** - Une description est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’une image spécifique.

- **Déposez une ressource ici ou recherchez un fichier à télécharger** - Cette option permet de déposer une ressource telle qu’une image par glisser-déposer de la souris. Vous pouvez également télécharger un fichier à partir d’un système de fichiers local à l’aide du bouton **Parcourir**. Après avoir ajouté une image, trois boutons s’affichent au bas de l’image :
   - **Modifier** - Appuyez ou cliquez sur **Modifier** pour gérer les rendus de la ressource dans l’éditeur de ressources.
   - **Effacer** - Appuyez ou cliquez sur **Effacer** pour désélectionner l’image actuellement sélectionnée.
   - **Sélection** - Appuyez ou cliquez sur **Sélection** pour sélectionner une autre image dans le dossier Ressources.

- **Texte secondaire** - Cette option est utilisée pour saisir un texte de remplacement court et descriptif qui décrit l’image aux personnes malvoyantes.

- **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.

<!--   **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.
-->

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS du composant « Image ».

### Onglet Styles {#styles-tab}

Cet onglet vous permet de définir et de gérer les styles CSS d’un composant. Le composant principal « Image » des formulaires adaptatifs prend en charge le [Système de style](/help/get-started/authoring.md#component-styling) d’AEM.

![Boîte de dialogue de conception.](/help/adaptive-forms/assets/checkbox-style.png)

- **Classes CSS par défaut** : vous pouvez fournir une classe CSS par défaut pour le composant principal « Image » des formulaires adaptatifs.

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