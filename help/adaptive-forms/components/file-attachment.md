---
title: Composant principal Adaptive Forms - Pièce jointe
description: Utilisation ou personnalisation du composant principal de pièce jointe de fichier Forms adaptatif .
role: Architect, Developer, Admin, User
source-git-commit: 1e6460d318f4f9a5dfdcbb81723da01b51b72f3f
workflow-type: tm+mt
source-wordcount: '1482'
ht-degree: 1%

---


# Pièce jointe {#file-attachment-adaptive-forms-core-component}

Un composant de pièce jointe de fichier dans un formulaire adaptatif permet aux utilisateurs de sélectionner et de charger des fichiers à partir de leur ordinateur ou appareil local. Le composant de pièce jointe peut être configuré pour autoriser des types de fichiers spécifiques, des limites de taille et plusieurs pièces jointes.

**Exemple**

![](/help/adaptive-forms/assets/upload-image.png)


## Utilisation {#reasons-to-use-file-attachment}

Il existe plusieurs raisons pour lesquelles il est bénéfique d’inclure un composant de pièce jointe dans un formulaire adaptatif, notamment :

* **Collecter les informations supplémentaires**: Un composant de pièce jointe permet aux utilisateurs de télécharger des documents, des images, des vidéos ou d’autres types de fichiers dans le cadre de l’envoi du formulaire. Cela peut s’avérer utile pour collecter des informations supplémentaires, telles que des reprise, des portefeuilles ou de la documentation de prise en charge.

* **Partage aisé de fichiers volumineux**: Le composant Pièce jointe permet aux utilisateurs de partager facilement des fichiers volumineux, sans avoir à recourir à des services de partage de fichiers externes.

* **Convivialité**: Le composant de pièce jointe permet aux utilisateurs de charger des fichiers à partir de leur ordinateur local, sans avoir à quitter le formulaire ou utiliser d’autres outils.

* **Analyse des données**: Le composant Pièce jointe peut être utilisé pour collecter des données provenant de diverses sources et les analyser ou les utiliser comme entrée pour un traitement ultérieur.

* **Expérience utilisateur**: Le composant de pièce jointe peut être utilisé pour rendre le formulaire plus convivial en offrant une méthode claire et intuitive pour que les utilisateurs puissent télécharger des fichiers.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Pièce jointe Adaptive Forms a été publié en février 2023 dans le cadre de la version 2.0.4 des composants principaux. Voici un tableau présentant toutes les versions prises en charge, la compatibilité AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible avec<br>[version 2.0.4](/help/versions.md) et plus tard | Compatible | Compatible |

Pour plus d’informations sur les versions et versions des composants principaux, reportez-vous à la section [Versions des composants principaux](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Découvrez les informations les plus récentes sur le composant principal Pièce jointe du Forms adaptatif dans la documentation technique de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/fileinput/v1/fileinput). Pour plus d’informations sur le développement des composants principaux, consultez la section [Documentation destinée aux développeurs sur les composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser votre expérience de pièce jointe pour les visiteurs qui utilisent la boîte de dialogue Configurer . Vous pouvez également définir facilement des options de pièce jointe pour une expérience utilisateur fluide.

### Onglet De base {#basic-tab}

![Onglet Simple](/help/adaptive-forms/assets/fileattachement_basictab.png)

* **Nom** - Vous pouvez identifier facilement un composant de formulaire avec son nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

* **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

* **Masquer le titre** - Sélectionnez l’option pour masquer le titre du composant.

* **Titre du bouton** - Cette option est utilisée pour définir le libellé du bouton affiché sur un formulaire adaptatif.

* **Référence de liaison** - Une référence de liaison est une référence à un élément de données stocké dans une source de données externe et utilisé dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client dans un formulaire, en fonction de l’identifiant du client saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur transparente pour la collecte et la gestion des données.
* **Masquer le composant** - Sélectionnez l’option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par l’utilisateur.
* **Désactiver le composant** - Sélectionnez l’option pour désactiver le composant. Le composant désactivé n’est pas principal ni modifiable par l’utilisateur final. L’utilisateur peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
* **Lecture seule** - Sélectionnez l’option pour rendre le composant non modifiable. L’utilisateur peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
* **Autoriser plusieurs pièces jointes** - Sélectionnez cette option pour charger plusieurs pièces jointes à l’aide de la variable **Pièce jointe** bouton .

### Onglet Validation {#validation-tab}

![Onglet Validation](/help/adaptive-forms/assets/fileattachment_validationtab.png)

* **Obligatoire** - Sélectionnez cette option si vous souhaitez afficher le composant dans un formulaire adaptatif. Vous ne pouvez pas sélectionner la variable **Masquer le composant** ou **Désactiver le composant**  dans le **De base** lorsque cette option est sélectionnée.

* **Message d’erreur** - Cette option vous permet de saisir un message qui s’affiche si la variable **Obligatoire** est cochée et le champ n’est pas renseigné.

* **Message de validation de script** - Cette option permet de saisir un message à afficher en cas d’échec de la validation du script.

* **Message d’erreur des fichiers minimaux** - Cette option est utilisée pour saisir un message d’erreur qui s’affiche si vous téléchargez des fichiers inférieurs au nombre minimum de fichiers spécifié.

* **Message d’erreur de fichiers maximum** - Cette option est utilisée pour saisir un message d’erreur qui s’affiche si vous téléchargez des fichiers dont le nombre maximal de fichiers est supérieur à celui spécifié.

* **Taille maximale du fichier (Mo)** - Cette option permet de spécifier une taille de fichier maximale. Les tailles de fichier sont spécifiées en Mo.

* **Message d’erreur de taille de fichier maximale** - Cette option est utilisée pour saisir un message d’erreur qui s’affiche si vous téléchargez des fichiers d’une taille supérieure à la taille de fichier spécifiée dans **Taille maximale du fichier (Mo)** .

* **Types de fichiers autorisés** - Les différents types de fichiers qui peuvent être chargés à l’aide de la variable **Pièce jointe** sont ajoutés ici. Il permet également d’ajouter un nouveau format de fichier en cliquant sur le **Ajouter** bouton . Les formats de fichiers pris en charge sont les suivants : audio, vidéo, image, texte ou PDF. Vous pouvez également supprimer ou réorganiser les types de fichiers autorisés à l’aide de :
   * **Supprimer** - Appuyez ou cliquez sur pour supprimer des types de fichiers spécifiques.
   * **Réorganiser** - Appuyez ou cliquez dessus et faites glisser pour réorganiser l’ordre des types de fichiers autorisés.

* **Message d’erreur de type de fichier** - Cette option vous permet de saisir un message d’erreur qui s’affiche lorsque vous téléchargez des formats de fichiers autres que ceux répertoriés dans la **Types de fichiers autorisés** .

### Onglet Contenu de l’aide {#help-content-tab}

![Onglet Contenu de l’aide](/help/adaptive-forms/assets/fileattachement_helpcontenttab.png)

* **Description courte** - Une brève description est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez la variable **Toujours afficher une description courte** pour l’afficher sous le composant.

* **Toujours afficher une description courte** - Activez l’option pour afficher la description courte sous le composant.

* **Texte de l’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur clique sur l’icône d’aide (i) placée en regard du composant. Le texte d’aide fournit des informations plus détaillées que le texte d’étiquette ou d’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

![Onglet Accessibilité](/help/adaptive-forms/assets/fileattachement_accessibilitytab.png)

* **Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisé par les malvoyants. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom et tout message pertinent du champ (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs, y compris ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.


## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS du composant Pièce jointe.

### Onglet Styles {#styles-tab}

Le composant principal de pièce jointe de fichier Forms adaptatif prend en charge l’AEM [Système de style](/help/get-started/authoring.md#component-styling).

**Classes CSS par défaut**: Vous pouvez fournir une classe CSS par défaut pour le composant principal Pièce jointe du Forms adaptatif.

**Styles autorisés**: Vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé &quot;bold text&quot; et fournir la classe CSS &quot;font-weight: bold&quot;. Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de Forms adaptatif. Pour appliquer un style, dans l’éditeur de Forms adaptatif, sélectionnez le composant auquel vous souhaitez appliquer le style, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans le **Styles** liste déroulante. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.
