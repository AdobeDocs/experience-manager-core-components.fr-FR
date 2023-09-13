---
title: Composant principal des formulaires adaptatifs - Pièce jointe
description: Utilisation ou personnalisation du composant principal « Pièce jointe » des formulaires adaptatifs.
role: Architect, Developer, Admin, User
exl-id: 64a54fc6-db52-481f-bf5a-60c05122004d
source-git-commit: ad3e3bca5cb46f14e864e4704c90ac3b62779794
workflow-type: ht
source-wordcount: '1580'
ht-degree: 100%

---

# Pièce jointe {#file-attachment-adaptive-forms-core-component}

Un composant « Pièce jointe » dans un formulaire adaptatif permet aux utilisateurs et aux utilisatrices de sélectionner et de charger des fichiers à partir de leur ordinateur ou appareil local. Le composant « Pièce jointe » peut être configuré pour accepter des types de fichiers spécifiques, plusieurs pièces jointes, et définir des limites de taille.

**Exemple**

![](/help/adaptive-forms/assets/upload-image.png)


## Utilisation {#reasons-to-use-file-attachment}

Il existe plusieurs raisons d’inclure un composant « Pièce jointe » dans un formulaire adaptatif, notamment :

* **Collecter des informations supplémentaires** : un composant « Pièce jointe » permet aux utilisateurs et ux utilisatrices de charger des documents, des images, des vidéos ou d’autres types de fichiers dans le cadre de l’envoi du formulaire. Cela peut s’avérer utile pour collecter des informations supplémentaires, telles que des CV, des portfolios ou de la documentation d’aide.

* **Partage facile de fichiers volumineux** : le composant « Pièce jointe » permet aux utilisateurs et aux utilisatrices de partager facilement des fichiers volumineux, sans avoir à recourir à des services de partage de fichiers externes.

* **Convivialité** : le composant « Pièce jointe » permet aux utilisateurs et aux utilisatrices de charger des fichiers à partir de leur ordinateur local, sans avoir à quitter le formulaire ou utiliser d’autres outils.

* **Analyse des données** : le composant « Pièce jointe » peut être utilisé pour collecter des données provenant de diverses sources et les analyser ou les utiliser comme entrée pour un traitement ultérieur.

* **Expérience utilisateur** : le composant « Pièce jointe » peut être utilisé pour rendre le formulaire plus convivial en offrant une méthode claire et intuitive pour que les utilisateurs et les utilisatrices puissent joindre des fichiers.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Accordéon des formulaires adaptatifs a été publié en février 2023 au sein des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec la <br>[version 2.0.4](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible avec les<br>[versions 1.1.12](/help/adaptive-forms/version.md) à 2.0.0 exclue. |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Retrouvez les informations les plus récentes sur le composant principal « Pièce jointe » des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/fileinput/v1/fileinput). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience de pièce jointe pour les visiteurs et les visiteuses en utilisant la boîte de dialogue Configurer. Vous pouvez également définir facilement des options de pièce jointe pour une expérience utilisateur fluide.

### Onglet De base {#basic-tab}

![Onglet De base](/help/adaptive-forms/assets/fileattachement_basictab.png)

* **Nom** - Vous pouvez identifier facilement un composant de formulaire en lui attribuant un nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

* **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

* **Masquer le titre** - Sélectionnez cette option pour masquer le titre du composant.

* **Titre du bouton** - Cette option est utilisée pour définir le libellé du bouton affiché sur un formulaire adaptatif.

* **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.
* **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.
* **Désactiver le composant** - Sélectionnez cette option pour désactiver le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
* **Lecture seule** - Sélectionnez cette option pour rendre le composant non modifiable. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
* **Autoriser plusieurs pièces jointes** - Sélectionnez cette option pour accepter plusieurs pièces jointes à l’aide du bouton **Pièce jointe**.

### Onglet Validation {#validation-tab}

![Onglet Validation](/help/adaptive-forms/assets/fileattachment_validationtab.png)

* **Obligatoire** : Sélectionnez cette option si vous souhaitez afficher le composant dans un formulaire adaptatif. Vous ne pouvez pas sélectionner **Masquer le composant** ou **Désactiver le composant**  dans l’onglet **De base** lorsque cette option est sélectionnée.

* **Message d’erreur** - Cette option vous permet de saisir un message qui s’affiche si la case à cocher **Obligatoire** est cochée et que le champ n’est pas renseigné.

* **Message de validation de script** - Cette option permet de saisir un message à afficher en cas d’échec de la validation du script.

* **Message d’erreur sur le nombre de fichiers minimaux** - Cette option est utilisée pour saisir un message d’erreur qui s’affiche si vous téléchargez un nombre de fichiers inférieur au nombre minimum de fichiers spécifié.

* **Message d’erreur sur le nombre de fichiers maximum** - Cette option est utilisée pour saisir un message d’erreur qui s’affiche si vous téléchargez un nombre de fichiers supérieur au nombre maximum de fichiers spécifié.

* **Taille maximale du fichier (Mo)** - Cette option permet de spécifier une taille de fichier maximale. Les tailles de fichier sont spécifiées en Mo.

* **Message d’erreur sur la taille de fichier maximale** - Cette option est utilisée pour saisir un message d’erreur qui s’affiche si vous téléchargez des fichiers d’une taille supérieure à la taille de fichier spécifiée dans **Taille maximale du fichier (Mo)**.

* **Types de fichiers autorisés** - Les différents types de fichiers qui peuvent être chargés à l’aide du bouton **Pièce jointe** sont ajoutés ici. Cette option permet également d’ajouter un nouveau format de fichier en cliquant sur le bouton **Ajouter**. Les formats de fichiers pris en charge sont les suivants : audio, vidéo, image, texte ou PDF. Vous pouvez également supprimer ou réorganiser les types de fichiers autorisés à l’aide de :
   * **Supprimer** - Appuyez ou cliquez sur supprimer pour supprimer certains types de fichier.
   * **Réorganiser** - Appuyez ou faites glisser pour réorganiser l’ordre des types de fichier autorisés.

* **Message d’erreur sur le type de fichier** - Cette option vous permet de saisir un message d’erreur qui s’affiche lorsque vous téléchargez des formats de fichiers autres que ceux répertoriés dans les **Types de fichiers autorisés**.

### Onglet Contenu de l’aide {#help-content-tab}

![Onglet Contenu d’aide](/help/adaptive-forms/assets/fileattachement_helpcontenttab.png)

* **Description courte** : Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez l’option **Toujours afficher une description courte** pour l’afficher sous le composant.

* **Toujours afficher une description courte** - Activez l’option pour afficher la description courte sous le composant.

* **Texte d’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility-tab}


![Onglet Accessibilité](/help/adaptive-forms/assets/fileattachement_accessibilitytab.png)

* **Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.


## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS du composant « Pièce jointe ».

### Onglet Styles {#styles-tab}

Le composant principal « Pièce jointe » des formulaires adaptatifs prend en charge le [Système de style](/help/get-started/authoring.md#component-styling) d’AEM.

![Boîte de dialogue de conception de pièce jointe.](/help/adaptive-forms/assets/fileattachment_designdialog.png)

* **Classes CSS par défaut** : vous pouvez fournir une classe CSS par défaut pour le composant principal « Pièce jointe » des formulaires adaptatifs.

* **Styles autorisés** : vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé « texte en gras » et fournir la classe CSS « police d’épaisseur : gras ». Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de formulaires adaptatifs. Pour appliquer un style, sélectionnez le composant auquel vous souhaitez appliquer le style dans l’éditeur de formulaires adaptatifs, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans la liste déroulante **Styles**. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

## Article connexe {#related-article}

* [Création d’un formulaire adaptatif dans une page AEM Sites ou un fragment d’expérience](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=fr)

* [Création d’un formulaire adaptatif autonome](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=fr)


## Voir également {#see-also}

* [Accordéon](/help/adaptive-forms/components/accordion.md)
* [Bouton](/help/adaptive-forms/components/button.md)
* [Case à cocher Groupe](/help/adaptive-forms/components/checkbox-group.md)
* [Sélecteur de date](/help/adaptive-forms/components/date-picker.md)
* [Liste déroulante](/help/adaptive-forms/components/drop-down.md)
* [Entrée d’e-mail](/help/adaptive-forms/components/email-input.md)
* [Conteneur de formulaires](/help/adaptive-forms/components/form-container.md)
* [Pied de page](/help/adaptive-forms/components/footer.md)
* [En-tête](/help/adaptive-forms/components/header.md)
* [Onglets horizontaux](/help/adaptive-forms/components/horizontal-tabs.md)
* [Image](/help/adaptive-forms/components/image.md)
* [Entrée de nombre](/help/adaptive-forms/components/number-input.md)
* [Conteneur de panneau](/help/adaptive-forms/components/panel-container.md)
* [Bouton radio](/help/adaptive-forms/components/radio-button.md)
* [Bouton de réinitialisation](/help/adaptive-forms/components/reset-button.md)
* [Bouton Envoyer](/help/adaptive-forms/components/submit-button.md)
* [Entrée téléphonique](/help/adaptive-forms/components/telephone-input.md)
* [Entrée de texte](/help/adaptive-forms/components/text-input.md)
* [Texte](/help/adaptive-forms/components/text.md)
* [Titre](/help/adaptive-forms/components/title.md)
* [Assistant](/help/adaptive-forms/components/wizard.md)