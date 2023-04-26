---
title: Formulaire adaptatif - Accordéon
description: Utilisez l’accordéon pour organiser et simplifier un formulaire long ou complexe en le divisant en sections plus petites et plus faciles à gérer.
role: Architect, Developer, Admin, User
exl-id: 0ed38eee-fc22-4708-82eb-3fb1839b1ff2
source-git-commit: 0cfdc56fe5508e156eee2ae818be311748af7247
workflow-type: ht
source-wordcount: '1677'
ht-degree: 100%

---

# Composant Accordéon {#accordion-component-adaptive-forms-core-component}

Le composant principal « Accordéon » permet aux utilisateurs et aux utilisatrices de créer des sections extensibles et réductibles dans un formulaire adaptatif. Il est souvent utilisé pour organiser et simplifier des formulaires longs ou complexes en les divisant en sections plus petites et plus faciles à gérer. Chaque section d’un accordéon est généralement représentée par un en-tête sur lequel l’utilisateur ou l’utilisatrice peut cliquer pour développer ou réduire le contenu correspondant. Le contenu peut être n’importe quel composant principal.

## Utilisation {#usage}

Il existe plusieurs raisons d’inclure un accordéon dans un formulaire adaptatif, notamment :

* **Gain de place** : un accordéon permet aux utilisateurs et aux utilisatrices de modifier la taille des sections d’un formulaire, et d’avoir besoijn de moins de place pour afficher tous les champs du formulaire en même temps.

* **Navigation** : un accordéon peut être utilisé pour créer une structure de navigation hiérarchique, ce qui facilite la recherche des champs de formulaire dont les utilisateurs et les utilisatrices ont besoin.

* **Expérience utilisateur** : l’accordéon peut être utilisé pour rendre le formulaire plus convivial en offrant une méthode claire et intuitive d’accès et de remplissage des champs de formulaire.

* **Formulaires longs** : l’accordéon est un composant idéal pour gérer les formulaires longs, car il permet aux utilisateurs et aux utilisatrices de se concentrer sur une section à la fois, plutôt que d’essayer de traiter de nombreuses informations en même temps.

Vous pouvez utiliser :

* La [boîte de dialogue de configuration](#configure-dialog) pour spécifier les propriétés du composant Accordéon.

* La [fenêtre contextuelle Sélectionner un panneau](#select-panel-popover) pour définir l’ordre des panneaux de l’accordéon. Cela permet au créateur ou à la créatrice d’organiser les panneaux dans l’ordre dans lequel ils doivent apparaître.

* Options permettant à un créateur ou à une créatrice de formulaires d’activer ou de désactiver certaines fonctions dans la [boîte de dialogue de conception](#design-dialog). Par exemple, un créateur ou une créatrice peut choisir de désactiver certains champs ou sections d’un formulaire. Ces options permettent au créateur ou à la créatrice de mieux contrôler la conception et les fonctionnalités du formulaire, ce qui facilite la création de formulaires adaptés aux besoins spécifiques de l’entreprise.

La boîte de dialogue de configuration, la fenêtre contextuelle de sélection et la boîte de dialogue de conception font toutes partie des composants principaux conçus pour faciliter la création des formulaires et fournir un moyen efficace de créer des formulaires complexes.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Accordéon des formulaires adaptatifs a été publié en février 2023 au sein des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec la <br>[version 2.0.4](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible avec les<br>[versions 1.1.12](/help/adaptive-forms/version.md) à 2.0.0 exclue. |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Retrouvez les informations les plus récentes sur le composant « Accordéon » dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/accordion/v1/accordion). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience d’accordéon pour les visiteurs et les visiteuses en utilisant la boîte de dialogue Configurer. Vous pouvez également définir facilement des éléments d’accordéon, des panneaux, un comportement et une apparence pour une expérience utilisateur fluide.

### Onglet De base {#basic-tab}

![Onglet De base](/help/adaptive-forms/assets/accordion_basictab.png)

* **Nom** : vous pouvez identifier facilement un composant de formulaire en lui attribuant un nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

* **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

* **Masquer le titre** - Sélectionnez cette option pour masquer le titre du composant.

* **Inclure des données dans l’objet** - Sélectionnez « Inclure des données dans l’objet » pour placer les données de champ de l’assistant dans un objet JSON. Si cette option n’est pas sélectionnée, le fichier JSON des données d’envoi présente une structure plate pour les champs de l’assistant.

* **Disposition** - Vous pouvez utiliser une disposition fixe (simple) ou une disposition flexible (grille réactive) pour votre assistant. La disposition simple conserve tout ce qui est fixe, tandis que la grille réactive vous permet d’ajuster la position des composants en fonction de vos besoins. Par exemple, utilisez la grille réactive pour aligner « Prénom », « Deuxième prénom » et « Nom » dans un formulaire sur une seule ligne.

* **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.
* **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.
* **Désactiver le composant** - Sélectionnez cette option pour désactiver le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

### Onglet Éléments {#items-tab}

![Onglet Éléments](/help/adaptive-forms/assets/accordion_itemstab.png)

Le bouton Ajouter vous permet de sélectionner un composant à ajouter sous forme de panneau à partir de la fenêtre de sélection des composants. Après avoir ajouté le composant, vous pouvez voir les options suivantes :

* **Icône** - L’icône identifie le composant du panneau dans la liste. Pointez sur l’icône pour afficher le nom complet du composant sous forme d’info-bulle.
* **Description** - Description utilisée comme texte du panneau. Par défaut, le nom du composant est sélectionné pour le panneau.
* **Supprimer** : appuyez ou cliquez sur cette option pour supprimer le panneau du composant d’accordéon.
* **Réorganiser** : appuyez ou cliquez dessus et faites glisser pour réorganiser l’ordre des panneaux.

### Onglet Contenu de l’aide {#help-content}

![Onglet Contenu d’aide](/help/adaptive-forms/assets/accordion_helpcontent.png)

* **Description courte** - Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez l’option **Toujours afficher une description courte** pour l’afficher sous le composant.

* **Toujours afficher une description courte** - Activez cette option pour afficher la description courte sous le composant.

* **Texte d’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility}

![Onglet Accessibilité](/help/adaptive-forms/assets/accordion_accessibility.png)

**Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue Conception permet aux créateurs et aux créatrices de modèles de contrôler l’affichage des éléments par défaut. Pour le composant « Accordéon » des formulaires adaptatifs, vous pouvez définir les éléments suivants :

* Le type des éléments d’en-tête HTML autorisés et définis comme valeur par défaut (tels que H1, H2, H3, etc.)
* Les composants principaux qu’un créateur ou une créatrice de formulaire peut ajouter à l’accordéon dans l’éditeur de formulaires adaptatifs
* Les noms simples pour les styles (classes CSS) qui peuvent être appliqués dans la boîte de dialogue des propriétés du composant « Accordéon » dans l’éditeur de formulaires adaptatifs.

Cela permet de rendre le processus de création et de personnalisation de formulaires plus simple et plus efficace.

### Onglet Propriétés {#properties-tab-design}

L’onglet Propriétés permet aux créateurs et aux créatrices de modèles de définir et d’autoriser des éléments d’en-tête HTML par défaut pour les créateurs et créatrices de formulaires :

![Onglet Propriétés de la boîte de dialogue de conception](/help/assets/accordion-design-properties.png)

* **Éléments d’en-tête autorisés** : une liste déroulante comportant plusieurs options permettant au créateur ou à la créatrice du modèle de choisir les en-têtes quu peuvent être utilisés pour l’accordéon.

* **Élément d’en-tête par défaut** : une liste déroulante qui définit l’élément d’en-tête par défaut pour le composant « Accordéon ».

### Onglet Composants autorisés {#allowed-components-tab}

L’onglet **Composants autorisés** permet à l’éditeur de modèles de définir les composants qui peuvent être ajoutés en tant qu’éléments aux panneaux dans le composant « Accordéon » de l’éditeur de formulaires adaptatifs.

![Onglet Composants autorisés.](/help/adaptive-forms/assets/accordion_allowedcomponents.png)

### Onglet Styles {#styles-tab}

Cet onglet vous permet de définir et de gérer les styles CSS d’un composant. Le composant principal « Accordéon » des formulaires adaptatifs prend en charge le [Système de style](/help/get-started/authoring.md#component-styling) d’AEM.

![Onglet Styles.](/help/adaptive-forms/assets/accordion_style.png)

* **Classes CSS par défaut** : vous pouvez fournir une classe CSS par défaut pour le composant « Accordéon ».

* **Styles autorisés** : vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé « texte en gras » et fournir la classe CSS « police d’épaisseur : gras ». Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de formulaires adaptatifs. Pour appliquer un style, sélectionnez le composant auquel vous souhaitez appliquer le style dans l’éditeur de formulaires adaptatifs, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans la liste déroulante **Styles**. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

