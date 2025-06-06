---
title: Composant principal des formulaires adaptatifs - Pièce jointe
description: Utilisation ou personnalisation du composant principal « Pièce jointe » des formulaires adaptatifs.
role: Architect, Developer, Admin, User
exl-id: 64a54fc6-db52-481f-bf5a-60c05122004d
source-git-commit: b6ed89048065830171b70f105e755f2279dd7b01
workflow-type: tm+mt
source-wordcount: '2061'
ht-degree: 97%

---

# Composant Pièce jointe {#file-attachment-adaptive-forms-core-component}

<span class="preview"> La fonctionnalité **Type de données de la valeur envoyée** est disponible par le biais d’un programme d’adoption précoce. Vous pouvez écrire à aem-forms-ea@adobe.com à partir de votre identifiant e-mail officiel pour rejoindre le programme d’adoption précoce et demander l’accès à la fonctionnalité. </span>

Un composant « Pièce jointe » dans un formulaire adaptatif permet aux utilisateurs et aux utilisatrices de sélectionner et de charger des fichiers à partir de leur ordinateur ou appareil local. Le composant « Pièce jointe » peut être configuré pour accepter des types de fichiers spécifiques, plusieurs pièces jointes, et définir des limites de taille.

**Exemple**

![exemple](/help/adaptive-forms/assets/upload-image.png)


## Utilisation {#reasons-to-use-file-attachment}

Il existe plusieurs raisons d’inclure un composant « Pièce jointe » dans un formulaire adaptatif, notamment :

- **Collecter des informations supplémentaires** : un composant « Pièce jointe » permet aux utilisateurs et ux utilisatrices de charger des documents, des images, des vidéos ou d’autres types de fichiers dans le cadre de l’envoi du formulaire. Cela peut s’avérer utile pour collecter des informations supplémentaires, telles que des CV, des portfolios ou de la documentation d’aide.

- **Partage facile de fichiers volumineux** : le composant « Pièce jointe » permet aux utilisateurs et aux utilisatrices de partager facilement des fichiers volumineux, sans avoir à recourir à des services de partage de fichiers externes.

- **Convivialité** : le composant « Pièce jointe » permet aux utilisateurs et aux utilisatrices de charger des fichiers à partir de leur ordinateur local, sans avoir à quitter le formulaire ou utiliser d’autres outils.

- **Analyse des données** : le composant « Pièce jointe » peut être utilisé pour collecter des données provenant de diverses sources et les analyser ou les utiliser comme entrée pour un traitement ultérieur.

- **Expérience utilisateur** : le composant « Pièce jointe » peut être utilisé pour rendre le formulaire plus convivial en offrant une méthode claire et intuitive pour que les utilisateurs et les utilisatrices puissent joindre des fichiers.

## Version et compatibilité {#version-and-compatibility}

Le composant principal « Pièce jointe » des Forms adaptatives a été publié en février 2023 dans le cadre des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec la <br>[version 2.0.4](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible avec les<br>[versions 1.1.12](/help/adaptive-forms/version.md) à 2.0.0 exclue. |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_fr). -->

## Détails techniques {#technical-details}

Retrouvez les informations les plus récentes sur le composant principal « Pièce jointe » des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/fileinput/v1/fileinput). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience de pièce jointe pour les visiteurs et les visiteuses en utilisant la boîte de dialogue Configurer. Vous pouvez également définir facilement des options de pièce jointe pour une expérience utilisateur fluide.

### Onglet De base {#basic-tab}

![Onglet De base](/help/adaptive-forms/assets/fileattachement_basictab1.png)

- **Nom** - Vous pouvez identifier facilement un composant de formulaire en lui attribuant un nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

- **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.
- **Autoriser le texte enrichi pour le titre** - Cette fonctionnalité permet aux personnes de mettre en forme les titres en texte brut en y incorporant des fonctionnalités telles que le texte en gras, en italique et souligné, diverses polices, tailles de police et couleurs, et d’autres options pour améliorer la présentation visuelle et la personnalisation. Elle offre une plus grande flexibilité et un contrôle créatif pour faire ressortir les titres dans les documents, sites web ou applications.\
  Lorsque vous cochez la case **Autoriser le texte enrichi pour le titre**, les options de formatage deviennent visibles pour appliquer un style au titre du composant. Pour accéder à toutes les options de formatage disponibles, vous pouvez cliquer sur l’onglet ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Prise en charge de texte enrichi](/help/adaptive-forms/assets/richtext-support-title.png)

- **Masquer le titre** - Sélectionnez cette option pour masquer le titre du composant.

- **Titre du bouton** - Cette option est utilisée pour définir le libellé du bouton affiché sur un formulaire adaptatif.
- **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.
- **Marquer comme élément de formulaire non lié** : sélectionnez cette option pour configurer un champ de formulaire qui n’est lié à aucun schéma. Cette option vous permet d’enregistrer des données sans mettre à jour la source de données. Elle vous permet également de gérer les données de manière personnalisée, en les séparant de l’intégration de base de données standard.
- **Type de données de la valeur envoyée** : sélectionnez cette option pour déterminer comment la pièce jointe est envoyée au serveur. Pour envoyer la pièce jointe en tant que données binaires, sélectionnez l’option `File`. Pour envoyer la pièce jointe en tant que chaîne codée en Base64, sélectionnez l’option `String`. Si l’option `String` est sélectionnée, le fichier au format binaire est envoyé au serveur sous la forme d’une URL de données. Le serveur convertit automatiquement l’URL de données au format binaire, garantissant ainsi la compatibilité avec les actions existantes, telles que l’envoi d’e-mails et la génération du document d’enregistrement, sans nécessiter d’intervention de la part des utilisateurs et des utilisatrices. L’option `File` est sélectionnée par défaut.
- **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.
- **Désactiver le composant** - Sélectionnez cette option pour désactiver le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
- **Lecture seule** - Sélectionnez cette option pour rendre le composant non modifiable. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
- **Autoriser plusieurs pièces jointes** - Sélectionnez cette option pour accepter plusieurs pièces jointes à l’aide du bouton **Pièce jointe**.
- **Glisser-déposer le texte** - Il s’agit du texte affiché en haut du bouton **Joindre** pour inviter les utilisateurs et utilisatrices à joindre ou à faire glisser et déposer des fichiers. Vous avez la possibilité de personnaliser le texte affiché en haut du bouton **Joindre**. En outre, vous pouvez mettre en forme le texte à l’aide du menu de texte enrichi.

### Onglet Validation {#validation-tab}

![Onglet Validation](/help/adaptive-forms/assets/fileattachment_validationtab.png)

- **Obligatoire** : Sélectionnez cette option si vous souhaitez afficher le composant dans un formulaire adaptatif. Après avoir sélectionné cette option, vous devez ajouter des pièces jointes avant de poursuivre l’envoi du formulaire. Vous ne pouvez pas sélectionner **Masquer le composant** ou **Désactiver le composant**  dans l’onglet **De base** lorsque cette option est sélectionnée.
- **Message d’erreur** - Cette option vous permet de saisir un message qui s’affiche si la case à cocher **Obligatoire** est cochée et que le champ n’est pas renseigné.

- **Message de validation de script** - Cette option permet de saisir un message à afficher en cas d’échec de la validation du script.

<!--   **Minimum files error message** - This option is used to enter an error message that is displayed if you upload files lesser than the specified minimum number of files.-->

- **Taille maximale du fichier (Mo)** - Cette option permet de spécifier une taille de fichier maximale. Les tailles de fichier sont spécifiées en Mo.
  <!--   **Maximum files error message** - This option is used to enter an error message that is displayed if you upload files greater than the specified maximum number of files.-->

- **Message d’erreur sur la taille de fichier maximale** - Cette option est utilisée pour saisir un message d’erreur qui s’affiche si vous téléchargez des fichiers d’une taille supérieure à la taille de fichier spécifiée dans **Taille maximale du fichier (Mo)**.

- **Types de fichiers autorisés** - Les différents types de fichiers qui peuvent être chargés à l’aide du bouton **Pièce jointe** sont ajoutés ici. Cette option permet également d’ajouter un nouveau format de fichier en cliquant sur le bouton **Ajouter**. Les formats de fichiers pris en charge sont les suivants : audio, vidéo, image, texte ou PDF. Vous pouvez également supprimer ou réorganiser les types de fichiers autorisés à l’aide de :
   - **Supprimer** - Appuyez ou cliquez sur supprimer pour supprimer certains types de fichier.
   - **Réorganiser** - Appuyez ou faites glisser pour réorganiser l’ordre des types de fichier autorisés.

  L’envoi d’un fichier en modifiant son type sur un format de types de fichiers autorisé renvoie une erreur lors de l’envoi du formulaire.
- **Message d’erreur sur le type de fichier** - Cette option vous permet de saisir un message d’erreur qui s’affiche lorsque vous téléchargez des formats de fichiers autres que ceux répertoriés dans les **Types de fichiers autorisés**.

### Onglet Contenu de l’aide {#help-content-tab}

![Onglet Contenu d’aide](/help/adaptive-forms/assets/fileattachement_helpcontenttab.png)

- **Description courte** : Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez l’option **Toujours afficher une description courte** pour l’afficher sous le composant.

- **Toujours afficher une description courte** - Activez cette option pour afficher la description courte sous le composant.

- **Texte d’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility-tab}


![Onglet Accessibilité](/help/adaptive-forms/assets/fileattachement_accessibilitytab.png)

- **Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

   - **Texte personnalisé** : sélectionnez cette option pour utiliser le texte personnalisé pour les libellés d’accessibilité ARIA. Cette option affiche la boîte de dialogue Texte personnalisé. Vous pouvez ajouter des informations pertinentes dans la boîte de dialogue Texte personnalisé.
   - **Description** : sélectionnez cette option pour utiliser la description des libellés d’accessibilité ARIA.
   - **Titre** : sélectionnez cette option pour utiliser le titre pour les libellés d’accessibilité ARIA.
   - **Nom** : sélectionnez cette option pour utiliser le nom pour les libellés d’accessibilité ARIA.
   - **Aucun** : sélectionnez cette option si vous ne souhaitez pas ajouter de texte supplémentaire pour les libellés d’accessibilité ARIA.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS du composant « Pièce jointe ».

### Onglet Styles {#styles-tab}

Le composant principal « Pièce jointe » des formulaires adaptatifs prend en charge le [Système de style](/help/get-started/authoring.md#component-styling) d’AEM.

![Boîte de dialogue de conception](/help/adaptive-forms/assets/checkbox-style.png)

- **Classes CSS par défaut** : vous pouvez fournir une classe CSS par défaut pour le composant principal « Pièce jointe » des formulaires adaptatifs.

- **Styles autorisés** : vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé « texte en gras » et fournir la classe CSS « police d’épaisseur : gras ». Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de formulaires adaptatifs. Pour appliquer un style, sélectionnez le composant auquel vous souhaitez appliquer le style dans l’éditeur de formulaires adaptatifs, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans la liste déroulante **Styles**. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

### Propriétés personnalisées

![Boîte de dialogue Propriétés personnalisées](/help/adaptive-forms/assets/checkbox-customproperties.png)

Les propriétés personnalisées vous permettent d’associer des attributs personnalisés (paires clé-valeur) à un composant principal de formulaire adaptatif à l’aide du modèle de formulaire. Les propriétés personnalisées sont répercutées dans la section des propriétés du rendu déocuplé du composant. Cela permet de créer un comportement de formulaire dynamique qui s’adapte en fonction des valeurs d’attributs personnalisés. Par exemple, les développeurs et développeuses peuvent concevoir plusieurs rendus d’un composant de formulaires découplés pour des plateformes mobiles, de bureau ou web, ce qui améliore considérablement l’expérience client sur un large éventail d’appareils.

- **Nom du groupe** : vous pouvez fournir un nom pour identifier le groupe de propriétés personnalisées. Vous pouvez ajouter, supprimer ou réorganiser plusieurs groupes de propriétés personnalisées. Après avoir ajouté le groupe de propriétés personnalisées, vous pouvez voir les options suivantes :

   - **Paires clé-valeur** : vous pouvez ajouter plusieurs noms et valeurs de propriétés personnalisées en cliquant sur le bouton **Ajouter** pour chaque groupe de propriétés personnalisées.

   - **Supprimer** : appuyez ou cliquez pour supprimer le nom et la valeur des propriétés personnalisées.

   - **Réorganiser** : appuyez ou cliquez et faites glisser pour réorganiser l’ordre du nom et de la valeur des propriétés personnalisées.
<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=fr)

-->

## Articles connexes {#related-articles}

{{more-like-this}}

## Voir également {#see-also}

{{see-also}}
