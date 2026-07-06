---
title: Composant Principal De Forms Adaptatif - Choix D’Images
description: Utilisation du composant principal Choix d’image.
role: Developer, Admin, User
hide: true
source-git-commit: 0af65c80f9cc58c4ba48d5b3dc7a026820bd2833
workflow-type: tm+mt
source-wordcount: '1318'
ht-degree: 58%

---

# Champ ImageChoice de formulaire adaptatif {#image-choice}

Le composant Choix d’image d’un formulaire permet aux utilisateurs et aux utilisatrices d’effectuer des sélections en fonction de représentations visuelles, telles que des images, plutôt que des options textuelles. Il présente une série d&#39;images représentant chacune un choix distinct. Les utilisateurs peuvent sélectionner une ou plusieurs images, et des commentaires visuels indiquent leur sélection. Ce composant est utile pour des options telles que les variantes de produit, les réponses à un questionnaire ou les images de profil. Il améliore l’interaction et la clarté des utilisateurs et utilisatrices en offrant une méthode de sélection intuitive et attrayante visuellement.

## Utilisation

Le composant Choix d’image comporte plusieurs fonctionnalités clés, notamment :

- **Représentation de l’image :** les utilisateurs voient des images au lieu des libellés de texte ou des boutons radio traditionnels. Chaque image correspond à un choix qu’ils peuvent sélectionner, fournissant une représentation visuelle des options disponibles.

- **Images cliquables :** les utilisateurs peuvent sélectionner une option en cliquant directement sur l’image. L’image sélectionnée est souvent mise en surbrillance pour indiquer qu’elle a été choisie.

- **Sélections uniques ou multiples :** selon la conception du composant, les utilisateurs peuvent sélectionner une ou plusieurs images.

## Version et compatibilité {#version-and-compatibility}

Le composant Choix d’image d’Adaptive Forms a été publié dans le cadre de la version 2.0.64 des composants principaux. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service |
|---|---|
| v1 | Compatible avec la <br>[version 2.0.64](/help/adaptive-forms/version.md) et les versions ultérieures |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).

## Détails techniques {#technical-details}

Retrouvez les informations les plus récentes sur le composant principal « Choix d’image » d’Adaptive Forms dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation relative au développement des composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience de votre composant Choix d’image pour les visiteurs et les visiteuses en utilisant la boîte de dialogue Configurer.


### Onglet De base {#basic-tab}

![Choix d’image de l’onglet De base](basic-tab-imagechoice.png)

- **Nom** - Vous pouvez identifier facilement un composant de formulaire en lui attribuant un nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

- **Titre** - Avec son titre, vous pouvez facilement identifier un type de composant dans un formulaire adaptatif. Par défaut, le titre s’affiche en regard du composant.

- **Masquer le titre** - Vous pouvez masquer le titre en cochant la case Masquer le titre .

- **Options** - Permet d’ajouter une ou plusieurs images et de personnaliser les propriétés de choix de l’image. Les propriétés de choix de l’image incluent la valeur des données, la ressource de référence de l’image et le texte de remplacement pour chacune des images.

- **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données.

  Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.

- **Marquer comme élément de formulaire non lié** : sélectionnez cette option pour configurer un champ de formulaire qui n’est lié à aucun schéma. Cette option vous permet d’enregistrer des données sans mettre à jour la source de données. Elle vous permet également de gérer les données de manière personnalisée, en les séparant de l’intégration de base de données standard.

- **Type de données de la valeur envoyée** : cette option spécifie le type de données de la valeur envoyée lorsqu’une option est sélectionnée. Si le **type de données de la valeur envoyée** est défini sur `Number` et que vous ajoutez des données de chaîne à **Valeur des données** dans l’onglet **Options**, l’écran affiche un message d’erreur `Value type mismatch`.

- **Options d’affichage** : permet d’afficher le champ de votre choix d’image horizontalement ou verticalement.

- **Valeur par défaut** : cette option vous permet d’ajouter une valeur par défaut (valeur des données) dans un champ de formulaire. Si un **Composant désactivé** ou **Composant en lecture seule** est sélectionné, la valeur par défaut s’affiche à l’écran. Si aucune valeur n’est saisie par l’utilisateur ou l’utilisatrice dans le champ de formulaire, cette valeur est envoyée au moment de l’envoi du formulaire.

- **Masquer le composant** : sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.

- **Désactiver le composant** : sélectionnez cette option pour désactiver ou verrouiller le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

- **Lecture seule** : cette option permet d’ajouter une valeur par défaut (valeur de données) dans un champ de formulaire. Si un **Composant désactivé** ou **Composant en lecture seule** est sélectionné, la valeur par défaut s’affiche à l’écran. Si aucune valeur n’est saisie par l’utilisateur ou l’utilisatrice dans le champ de formulaire, cette valeur est envoyée au moment de l’envoi du formulaire.

- **Type de sélection** : cette option permet aux utilisateurs de sélectionner des sélections uniques ou multiples de champs de choix d’image.

### Onglet Validation {#validation-tab}

![Choix de l’image de l’onglet Validation](validation-tab-image-choice.png)

- **Obligatoire** : Sélectionnez cette option si vous souhaitez afficher le composant dans un formulaire adaptatif. Après avoir sélectionné cette option, vous devez effectuer une sélection avant de poursuivre l’envoi du formulaire. Lorsque cette option est sélectionnée, vous ne pouvez pas sélectionner les options **Masquer le composant** ou **Désactiver le composant** sous l’onglet ** De base.

- **Message d’erreur** - Cette option vous permet de saisir un message qui s’affiche si la case **Obligatoire** est cochée et que le champ de choix de l’image n’est pas sélectionné.

- **Message de validation de script** : cette option permet de saisir un message à afficher en cas d’échec de la validation du script.

### Onglet Contenu de l’aide {#helpcontent-tab}

![Choix de l’image du contenu d’aide](help-content-imagechoice.png)

- **Description courte** : Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez l’option **Toujours afficher une description courte** pour l’afficher sous le composant.

- **Toujours afficher une description courte** - Activez cette option pour afficher la description courte sous le composant.

- **Texte d’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.



### Onglet Accessibilité {#accessibility-tab}

![Choix des images d’accessibilité](accessibility-imagechoice.png)

- **Texte pour les lecteurs d’écran** : le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.
   - **Texte personnalisé** : sélectionnez cette option pour utiliser le texte personnalisé pour les libellés d’accessibilité ARIA. Cette option affiche la boîte de dialogue Texte personnalisé. Vous pouvez ajouter des informations pertinentes dans la boîte de dialogue Texte personnalisé.
   - **Titre** : sélectionnez cette option pour utiliser le titre pour les libellés d’accessibilité ARIA.

## Articles connexes {#related-articles}

{{more-like-this}}

## Voir également {#see-also}

{{see-also}}


