---
title: Composant principal des formulaires adaptatifs - Assistant
description: Utilisation ou personnalisation du composant principal « Assistant » des formulaires adaptatifs.
role: Architect, Developer, Admin, User
exl-id: fd785cd2-5ed6-4efb-997f-ce9056ed113d
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '1847'
ht-degree: 90%

---

# Assistant {#wizard-adaptive-forms-core-component}

La disposition « Assistant » d’un formulaire adaptatif fait référence à un formulaire divisé en plusieurs étapes ou pages, où l’utilisateur ou l’utilisatrice passe d’une étape à l’autre. Cette disposition est appelée « assistant », car elle présente un processus détaillé du formulaire à l’utilisateur ou l’utilisatrice.

Chaque étape de l’assistant contient généralement un groupe de champs de formulaire associés et un mécanisme de navigation, comme les boutons « Suivant » et « Retour », pour passer d’une étape à l’autre. L’utilisateur ou l’utilisatrice ne peut passer à l’étape suivante qu’une fois l’étape en cours terminée et lorque tous les champs requis ont été remplis.

La disposition « Assistant » s’avère utile pour les formulaires contenant de nombreux champs ou informations à collecter, dans la mesure où elle répartit le formulaire en blocs plus petits et plus faciles à gérer. Elle permet également aux utilisateurs et aux utilisatrices de se concentrer sur un ensemble de champs à la fois, ce qui peut rendre le processus de remplissage de formulaire moins contraignant.

Cependant, cela peut également accroître la complexité du formulaire, car l’utilisateur ou l’utilisatrice doit parcourir plusieurs pages pour remplir le formulaire. Il est donc nécessaire d’évaluer les exigences du formulaire et les besoins de l’utilisateur ou de l’utilisatrice avant de décider d’utiliser la disposition « Assistant ».

Vous pouvez utiliser le composant principal de disposition « Assistant » dans un formulaire adaptatif pour créer une disposition « Assistant ».


**Exemple**

![](/help/adaptive-forms/assets/wizard.png)

## Utilisation {#reasons-to-use-wizard-in-an-adaptive-form}

Il existe plusieurs raisons d’utiliser la disposition « Assistant » dans un formulaire adaptatif :

* **Simplicité** : la répartition d’un formulaire en plusieurs étapes peut faciliter la compréhension et la saisie, car les utilisateurs et les utilisatrices peuvent se concentrer sur un ensemble de champs à la fois.

* **Organisation** : une disposition « Assistant » peut vous aider à organiser les formulaires par sujet ou objectif. Elle peut également regrouper les champs associés, ce qui peut rendre le processus de remplissage de formulaires plus logique et plus efficace.

* **Validation** : une disposition « Assistant » permet une validation étape par étape, qui peut aider les utilisateurs et les utilisatrices à identifier et corriger les erreurs au fur et à mesure, plutôt que d’attendre jusqu’à la fin du formulaire.

* **Indicateur de progression** : une disposition « Assistant » peut afficher la progression du formulaire, ce qui peut aider l’utilisateur ou l’utilisatrice à comprendre la partie du formulaire à remplir.

* **Formulaires longs** : si le formulaire comporte de nombreux champs, il peut être très difficile pour l’utilisateur ou l’utilisatrice de les voir tous en même temps. Par conséquent, le décomposer en blocs plus petits et plus faciles à gérer peut le rendre moins intimidant.

* **Éviter l’abandon** : une disposition Assistant peut également contribuer à réduire l’abandon de formulaire, car les utilisateurs et les utilisatrices sont plus susceptibles de remplir un formulaire s’ils ou elles peuvent voir la progression et comprendre ce qu’il reste à faire.

* **Expérience mobile** : une disposition « Assistant » peut également s’avérer bénéfique pour les formulaires accessibles sur les appareils mobiles, dans la mesure où elle permet d’afficher des pages plus petites qui se chargent plus rapidement et sont plus faciles à parcourir.

Dans l’ensemble, une disposition « Assistant » peut rendre le processus de remplissage du formulaire plus facile à gérer et plus efficace pour les utilisateurs et les utilisatrices, mais il est important de tenir compte de la complexité du formulaire et des besoins de l’utilisateur ou de l’utilisatrice avant de décider d’utiliser ce type de disposition.

## Version et compatibilité {#version-and-compatibility}

Le composant principal « Disposition Assistant » des formulaires adaptatifs a été publié en février 2023 dans le cadre de la version 2.0.4 des composants principaux. Voici un tableau présentant toutes les versions prises en charge, la compatibilité AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec la <br>[version 2.0.4](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible avec<br>[version 1.1.12](/help/adaptive-forms/version.md) et plus tard, mais moins de 2.0.0. |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Retrouvez les informations les plus récentes sur le composant principal « Titre » des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/wizard/v1/wizard). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience d’assistant pour les visiteurs et les visiteuses en utilisant la boîte de dialogue Configurer. Vous pouvez également définir facilement des options d’assistant pour une expérience utilisateur fluide.

### Onglet De base {#basic-tab}

![Onglet De base](/help/adaptive-forms/assets/wizard_basictab.png)

* **Nom** - Vous pouvez identifier facilement un composant de formulaire avec son nom unique à la fois dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

* **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant.

* **Masquer le titre** - Sélectionnez cette option pour masquer le titre du composant.

* **Inclure des données dans l’objet** - Sélectionnez « Inclure des données dans l’objet » pour placer les données de champ de l’assistant dans un objet JSON. Si cette option n’est pas sélectionnée, le fichier JSON des données d’envoi présente une structure plate pour les champs de l’assistant.

* **Disposition** - Vous pouvez utiliser une disposition fixe (simple) ou une disposition flexible (grille réactive) pour votre assistant. La disposition simple conserve tout ce qui est fixe, tandis que la grille réactive vous permet d’ajuster la position des composants en fonction de vos besoins. Par exemple, utilisez la grille réactive pour aligner « Prénom », « Deuxième prénom » et « Nom » dans un formulaire sur une seule ligne.

* **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.

* **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.

* **Désactiver le composant** - Sélectionnez cette option pour désactiver le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

### Onglet Aide {#help-tab}

![Onglet Aide](/help/adaptive-forms/assets/wizard_helptab.png)

* **Description courte** - Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez l’option **Toujours afficher une description courte** pour l’afficher sous le composant.

* **Toujours afficher une description courte** - Activez cette option pour afficher la description courte sous le composant.

* **Texte d’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.


### Onglet Accessibilité {#accessibility}

![Onglet De base](/help/adaptive-forms/assets/wizard_accessibiltytab.png)

* **Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

* **Rôle HTML à annoncer par le lecteur d’écran** - Le rôle HTML est un attribut utilisé pour spécifier l’objectif d’un élément HTML pour les technologies d’assistance telles que les lecteurs d’écran. L’attribut rôle est utilisé pour fournir un contexte et une signification sémantique supplémentaires à un élément, ce qui facilite l’interprétation et l’annonce du contenu à l’utilisateur ou à l’utilisatrice par les lecteurs d’écran. Par exemple, dans AEM Forms, le libellé d’un champ de formulaire peut avoir le rôle « libellé » et son champ de saisie peut avoir le rôle « zone de texte ». Cela permet au lecteur d’écran de comprendre la relation entre le libellé et le champ de saisie, et de les annoncer correctement à l’utilisateur ou à l’utilisatrice.


## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue Conception permet aux créateurs et aux créatrices de modèles de contrôler l’affichage des éléments par défaut. Pour le composant « Assistant » des formulaires adaptatifs, vous pouvez définir les éléments suivants :

* Composants principaux qu’un créateur ou une créatrice de formulaire peut ajouter à l’assistant dans l’éditeur de formulaires adaptatifs
* Noms simples pour les styles (classes CSS) qui peuvent être appliqués dans la boîte de dialogue des propriétés du composant « Assistant » dans l’éditeur de formulaires adaptatifs.

Cela permet de rendre le processus de création et de personnalisation de formulaires plus simple et plus efficace.

### Onglet Composants autorisés {#allowed-components-tab}

L’onglet **Composants autorisés** permet à l’éditeur de modèles de définir les composants qui peuvent être ajoutés en tant qu’éléments aux panneaux dans le composant « Assistant » de l’éditeur de formulaires adaptatifs.

![Onglets Composants autorisés](/help/adaptive-forms/assets/panel_allowedcomponent.png)

### Onglet Composants par défaut {#default-component-tab}

Cet onglet permet à l’éditeur de modèles de mapper les composants qui peuvent être ajoutés en tant qu’éléments aux panneaux dans le composant de l’assistant dans l’éditeur de Forms adaptatif.

![Composant par défaut du panneau](/help/adaptive-forms/assets/panel_defaultcomponent.png)

### Paramètres réactifs {#responsive-settings}

Cet onglet permet à l’éditeur de modèles de définir le nombre de colonnes à afficher dans la grille réactive.

![Grille réactive](/help/adaptive-forms/assets/panel_responsivesettings.png)

### Onglet Paramètres de conteneur {#container-setting-tab}

L’onglet Paramètres du conteneur permet de définir la position des composants dans l’éditeur de Forms adaptatif.

![Paramètres du conteneur](/help/adaptive-forms/assets/panel_settings.png)

* **Disposition**: La mise en page simple conserve tout ce qui est fixe, tandis que la grille réactive vous permet de modifier la position des composants en fonction de vos besoins.
* **Désactiver la mise en page**: Vous pouvez également désactiver la sélection de mise en page dans la boîte de dialogue de modification en sélectionnant **Désactiver la mise en page** .
* **Activer l’image d’arrière-plan**: Cet onglet permet de définir l’image d’arrière-plan et la couleur dans l’éditeur de modèles.
* **Activer la couleur d’arrière-plan**: Cet onglet permet de définir la couleur d’arrière-plan dans l’éditeur de modèles.

### Onglet Styles {#styles-tab}

L’onglet permet de définir et de gérer les styles CSS d’un composant. Le composant principal « Assistant » des formulaires adaptatifs prend en charge le [Système de style](/help/get-started/authoring.md#component-styling) d’AEM.

![Onglet Style](/help/adaptive-forms/assets/panel_style.png)

* **Classes CSS par défaut** : vous pouvez fournir une classe CSS par défaut pour le composant « Assistant ».

* **Styles autorisés** : vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé « texte en gras » et fournir la classe CSS « police d’épaisseur : gras ». Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de formulaires adaptatifs. Pour appliquer un style, sélectionnez le composant auquel vous souhaitez appliquer le style dans l’éditeur de formulaires adaptatifs, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans la liste déroulante **Styles**. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

