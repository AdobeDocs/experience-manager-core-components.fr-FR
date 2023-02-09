---
title: Composant principal Adaptive Forms - Image
description: Utilisation ou personnalisation du composant principal Image Forms adaptative.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 2%

---


# Image {#image-adaptive-forms-core-component}

Un composant Image d’un formulaire adaptatif est un moyen d’inclure des images dans un formulaire. Ces images peuvent être utilisées pour améliorer la conception globale du formulaire, fournir des informations supplémentaires ou servir d’aide visuelle pour aider les utilisateurs à comprendre l’objectif du formulaire. Le composant d’image peut être utilisé pour ajouter un logo, une photo ou un graphique dans le formulaire.

Pour l’accessibilité, il est important de spécifier **Texte secondaire** à l’image afin de fournir un texte de remplacement court et descriptif pour l’image, qui décrit l’image aux utilisateurs qui ne peuvent pas la voir.


**Exemple**

![](/help/adaptive-forms/assets/image.png)


## Utilisation {#reasons-to-use-image-in-a-form}

Il existe plusieurs raisons pour lesquelles il est bénéfique d’inclure un composant Image dans un formulaire adaptatif, notamment :

* **Marques**: Une image peut être utilisée pour afficher le logo ou le nom de l’organisation qui a créé le formulaire, ce qui contribue à établir la reconnaissance et la crédibilité de la marque.

* **Accessoires visuels**: Une image peut aider à fournir un niveau d’information supplémentaire aux utilisateurs, en fournissant une aide visuelle pour aider les utilisateurs à comprendre l’objectif du formulaire.

* **Décoration**: Une image peut être utilisée pour améliorer la conception globale du formulaire et le rendre plus attrayant visuellement.

* **Expérience utilisateur**: Une image peut être utilisée pour rendre le formulaire plus convivial en offrant une méthode claire et intuitive d’accès et de remplissage des champs de formulaire.

## Version et compatibilité {#version-and-compatibility}

Le composant principal d’image Adaptive Forms a été publié en février 2023 dans le cadre de la version 2.0.4 des composants principaux. Voici un tableau présentant toutes les versions prises en charge, la compatibilité AEM et les liens vers la documentation correspondante :

|  |  |
|---|---|
| Version du composant | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatible avec<br>[version 2.0.4](/help/versions.md) et plus tard | Compatible | Compatible |

Pour plus d’informations sur les versions et versions des composants principaux, reportez-vous à la section [Versions des composants principaux](/help/versions.md) document.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Découvrez les informations les plus récentes sur le composant principal Image de Forms adaptative dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/image/v1/image). Pour plus d’informations sur le développement des composants principaux, consultez la section [Documentation destinée aux développeurs sur les composants principaux](/help/developing/overview.md).


## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser votre expérience d’image pour les visiteurs qui utilisent la boîte de dialogue Configurer . Vous pouvez également définir facilement des options d’image pour une expérience utilisateur transparente.

![Onglet Propriétés](/help/adaptive-forms/assets/image_properties.png)

* **Nom** - Vous pouvez identifier facilement un composant de formulaire avec son nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

* **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

* **Référence de liaison de document d’enregistrement** - Cette option vous permet d’associer un champ Formulaire adaptatif au champ Document d’enregistrement. Lorsque l’utilisateur saisit une valeur dans un champ lié d’un formulaire adaptatif, cette valeur apparaît également dans le champ lié du document d’enregistrement correspondant. Par exemple, une référence de liaison de document d’enregistrement peut être utilisée pour afficher le nom et l’adresse d’un client dans un document d’enregistrement, en fonction de l’identifiant du client saisi dans le formulaire. Ainsi, AEM Forms vous permet de générer un document d’enregistrement et offre une expérience utilisateur transparente pour la collecte et la gestion des données.

* **Description** - Une description est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’une image spécifique.

* **Déposez une ressource ici ou recherchez un fichier à charger.** - Cette option permet de déposer une ressource telle qu’une image par glisser-déposer de la souris. Vous pouvez également télécharger un fichier à partir d’un système de fichiers local à l’aide de la fonction **Parcourir** bouton . Après l’ajout d’une image, trois boutons s’affichent au bas de l’image :
   * **Modifier** - Appuyez ou cliquez sur **Modifier** pour gérer les rendus de la ressource dans l’éditeur de ressources.
   * **Effacer** - Appuyez ou cliquez sur **Effacer** pour désélectionner l’image actuellement sélectionnée.
   * **Pick** - Appuyez ou cliquez sur **Pick**  pour sélectionner une autre image dans le dossier Ressources.

* **Texte secondaire** - Cette option est utilisée pour saisir le texte qui fournit un texte de remplacement court et descriptif pour l’image, qui décrit l’image aux utilisateurs malvoyants.

* **Masquer le composant** - Sélectionnez l’option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par l’utilisateur.

* **Lecture seule** - Sélectionnez l’option pour rendre le composant non modifiable. L’utilisateur peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS du composant Image.

### Onglet Styles {#styles-tab}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS d’un composant. Le composant principal Image Forms adaptative prend en charge l’AEM [Système de style](/help/get-started/authoring.md#component-styling).

**Classes CSS par défaut**: Vous pouvez fournir une classe CSS par défaut pour le composant principal Image Forms adaptative.

**Styles autorisés**: Vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé &quot;bold text&quot; et fournir la classe CSS &quot;font-weight: bold&quot;. Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de Forms adaptatif. Pour appliquer un style, dans l’éditeur de Forms adaptatif, sélectionnez le composant auquel vous souhaitez appliquer le style, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans le **Styles** liste déroulante. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.
