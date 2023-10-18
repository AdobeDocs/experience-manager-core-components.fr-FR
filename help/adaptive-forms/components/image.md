---
title: Composant principal des formulaires adaptatifs - Image
description: Utilisation ou personnalisation du composant principal « Image » des formulaires adaptatifs.
role: Architect, Developer, Admin, User
exl-id: 9ee42d5d-16e3-4973-8364-5bc512ebe72e
source-git-commit: 0bebc248ee2b708f7677950d90356abd5bc70a98
workflow-type: tm+mt
source-wordcount: '1051'
ht-degree: 100%

---

# Image {#image-adaptive-forms-core-component}

Un composant « Image » dans un formulaire adaptatif permet d’inclure des images dans un formulaire. Ces images peuvent être utilisées pour améliorer la conception globale du formulaire, fournir des informations supplémentaires ou servir d’aide visuelle pour aider les utilisateurs et les utilisatrices à comprendre l’objectif du formulaire. Le composant « Image » peut être utilisé pour ajouter un logo, une photo ou un graphique dans le formulaire.

Pour l’accessibilité, il est important de spécifier le **Texte secondaire** de l’image afin de fournir un texte de remplacement court et descriptif qui décrit l’image aux utilisateurs et utilisatrices qui ne peuvent pas la voir.


**Exemple**

![](/help/adaptive-forms/assets/image.png)


## Utilisation {#reasons-to-use-image-in-a-form}

Il existe plusieurs raisons d’inclure un composant « Image » dans un formulaire adaptatif, notamment :

* **Image de marque** : une image peut être utilisée pour afficher le logo ou le nom de l’organisation qui a créé le formulaire, ce qui contribue à établir la reconnaissance et la crédibilité de la marque.

* **Supports visuels** : une image peut aider à fournir un niveau d’information supplémentaire aux utilisateurs et aux utilisatrices, en fournissant un support visuel pour aider les utilisateurs et utilisatrices à comprendre l’objectif du formulaire.

* **Décoration** : une image peut être utilisée pour améliorer la conception globale du formulaire et le rendre plus attrayant visuellement.

* **Expérience utilisateur** : une image peut être utilisée pour rendre le formulaire plus convivial en offrant une méthode claire et intuitive d’accès et de remplissage des champs de formulaire.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Accordéon des formulaires adaptatifs a été publié en février 2023 au sein des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec la <br>[version 2.0.4](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible avec les<br>[versions 1.1.12](/help/adaptive-forms/version.md) à 2.0.0 exclue. |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Retrouvez les informations les plus récentes sur le composant principal « Image » des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/image/v1/image). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).


## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience d’image pour les visiteurs et les visiteuses à l’aide de la boîte de dialogue Configurer. Vous pouvez également définir facilement des options d’image pour une expérience utilisateur fluide.

![Onglet Propriétés](/help/adaptive-forms/assets/image_properties.png)

* **Nom** - Vous pouvez identifier facilement un composant de formulaire avec son nom unique à la fois dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

* **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

* **Référence Bind du document d’enregistrement** - Cette option vous permet d’associer un champ de formulaire adaptatif au champ « Document d’enregistrement ». Lorsque l’utilisateur ou l’utilisatrice saisit une valeur dans un champ lié d’un formulaire adaptatif, cette valeur apparaît également dans le champ lié du document d’enregistrement correspondant. Par exemple, une référence Bind de document d’enregistrement peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un document d’enregistrement, en fonction de l’identifiant saisi dans le formulaire. Ainsi, AEM Forms vous permet de générer un document d’enregistrement et offre une expérience utilisateur fluide pour la collecte et la gestion des données.

* **Description** - Une description est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’une image spécifique.

* **Déposez une ressource ici ou recherchez un fichier à télécharger** - Cette option permet de déposer une ressource telle qu’une image par glisser-déposer de la souris. Vous pouvez également télécharger un fichier à partir d’un système de fichiers local à l’aide du bouton **Parcourir**. Après avoir ajouté une image, trois boutons s’affichent au bas de l’image :
   * **Modifier** - Appuyez ou cliquez sur **Modifier** pour gérer les rendus de la ressource dans l’éditeur de ressources.
   * **Effacer** - Appuyez ou cliquez sur **Effacer** pour désélectionner l’image actuellement sélectionnée.
   * **Sélection** - Appuyez ou cliquez sur **Sélection** pour sélectionner une autre image dans le dossier Ressources.

* **Texte secondaire** - Cette option est utilisée pour saisir un texte de remplacement court et descriptif qui décrit l’image aux personnes malvoyantes.

* **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.

* **Lecture seule** - Sélectionnez cette option pour rendre le composant non modifiable. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS du composant « Image ».

### Onglet Styles {#styles-tab}

Cet onglet vous permet de définir et de gérer les styles CSS d’un composant. Le composant principal « Image » des formulaires adaptatifs prend en charge le [Système de style](/help/get-started/authoring.md#component-styling) d’AEM.

![Boîte de dialogue de conception.](/help/adaptive-forms/assets/image_designdialog.png)

**Classes CSS par défaut** : vous pouvez fournir une classe CSS par défaut pour le composant principal « Image » des formulaires adaptatifs.

**Styles autorisés** : vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé « texte en gras » et fournir la classe CSS « police d’épaisseur : gras ». Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de formulaires adaptatifs. Pour appliquer un style, sélectionnez le composant auquel vous souhaitez appliquer le style dans l’éditeur de formulaires adaptatifs, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans la liste déroulante **Styles**. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

## Article connexe {#related-article}

* [Création d’un formulaire adaptatif dans une page AEM Sites ou un fragment d’expérience](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=fr)

* [Création d’un formulaire adaptatif autonome](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=fr)


>[!MORELIKETHIS]
>
>* [Accordéon](/help/adaptive-forms/components/accordion.md)
>* [Bouton](/help/adaptive-forms/components/button.md)
>* [Groupe de cases à cocher](/help/adaptive-forms/components/checkbox-group.md)
>* [Sélecteur de date](/help/adaptive-forms/components/date-picker.md)
>* [Liste déroulante](/help/adaptive-forms/components/drop-down.md)
>* [Entrée d’e-mail](/help/adaptive-forms/components/email-input.md)
>* [Conteneur de formulaires](/help/adaptive-forms/components/form-container.md)
>* [Pièce jointe](/help/adaptive-forms/components/file-attachment.md)
>* [Pied de page](/help/adaptive-forms/components/footer.md)
>* [En-tête](/help/adaptive-forms/components/header.md)
>* [Onglets horizontaux](/help/adaptive-forms/components/horizontal-tabs.md)
>* [Entrée de nombre](/help/adaptive-forms/components/number-input.md)
>* [Conteneur de panneau](/help/adaptive-forms/components/panel-container.md)
>* [Bouton radio](/help/adaptive-forms/components/radio-button.md)
>* [Bouton de réinitialisation](/help/adaptive-forms/components/reset-button.md)
>* [Bouton Envoyer](/help/adaptive-forms/components/submit-button.md)
>* [Entrée téléphonique](/help/adaptive-forms/components/telephone-input.md)
>* [Entrée de texte](/help/adaptive-forms/components/text-input.md)
>* [Texte](/help/adaptive-forms/components/text.md)
>* [Titre](/help/adaptive-forms/components/title.md)
>* [Assistant](/help/adaptive-forms/components/wizard.md)

## Voir également {#see-also}

{{see-also}}