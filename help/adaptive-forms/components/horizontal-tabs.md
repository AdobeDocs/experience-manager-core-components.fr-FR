---
title: Composant principal des formulaires adaptatifs - Onglets horizontaux
description: Utilisation ou personnalisation du composant principal des onglets horizontaux des formulaires adaptatifs.
role: Architect, Developer, Admin, User
exl-id: fbdf330b-3b85-4f94-9dab-eea8465fba67
source-git-commit: 7888cfa0f1358ce8018fc1e3cc3b19eb66a82b9d
workflow-type: ht
source-wordcount: '1769'
ht-degree: 100%

---

# Onglets horizontaux {#horizontal-tabs-adaptive-forms-core-component}

Les onglets horizontaux d’un formulaire adaptatif font référence à un modèle de conception dans lequel plusieurs sections d’un formulaire sont regroupées et affichées sous la forme d’onglets distincts, alignés horizontalement. L’utilisateur ou l’utilisatrice peut basculer entre les onglets pour accéder aux différentes sections du formulaire. Chaque onglet sert de déclencheur pour afficher et masquer le contenu du formulaire associé. Les onglets horizontaux permettent d’organiser les formulaires longs en sections gérables et d’améliorer l’expérience client. Les onglets peuvent vous aider à rendre un formulaire plus accessible aux personnes présentant un handicap, car elles peuvent permuter entre les sections à l’aide de la navigation à l’aide du clavier.

Les onglets sont généralement créés sous la forme d’une série de liens ou de boutons, chaque lien ou bouton correspondant à une section du formulaire. Lorsqu’un utilisateur ou une utilisatrice clique sur un onglet, le contenu du formulaire est mis à jour de manière dynamique afin d’afficher la section correspondante.

## Utilisation {#reasons-to-use-horizontal-tabs}

Les raisons courantes d’utiliser les onglets horizontaux dans un formulaire adaptatif sont les suivantes :

* **Utilisation améliorée** : les onglets horizontaux permettent aux utilisateurs ou aux utilisatrices de parcourir plus facilement le formulaire, en particulier s’il comporte plusieurs sections ou un grand nombre de champs.

* **Gestion de l’espace** : les onglets horizontaux permettent de préserver l’espace de l’écran en regroupant les sections de formulaire associées en onglets et en n’affichant qu’une seule section à la fois.

* **Meilleure organisation** : les onglets offrent une structure claire et organisée pour un formulaire, ce qui permet aux utilisateurs et aux utilisatrices de comprendre et de remplir plus facilement le formulaire.

* **Interactions des utilisateurs renforcée** : les onglets horizontaux peuvent rendre un formulaire plus intéressant et attrayant visuellement pour les utilisateurs et les utilisatrices, ce qui peut améliorer le taux d’achèvement du formulaire.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Onglets horizontaux des formulaires adaptatif a été publié en février 2023 dans le cadre de la version 2.0.4 des composants principaux. Voici un tableau présentant toutes les versions prises en charge, la compatibilité AEM et les liens vers la documentation correspondante :

|  |  |
|---|---|
| Version du composant | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatible avec la <br>[version 2.0.4](/help/versions.md) et les versions ultérieures | Compatible | Compatible |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/versions.md).


<!-- ## Sample Component Output {#sample-component-output}

To experience the Horizontal-tabs  Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_Horizontal-tabs ). -->


## Détails techniques {#technical-details}

Obtenez les dernières informations sur le composant principal des onglets horizontaux des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageHorizontal tabs/v1/pageHorizontal tabs). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser votre expérience en matière d’onglets horizontaux pour les visiteurs et les visiteuses qui utilisent la boîte de dialogue de configuration. Vous pouvez également définir facilement des options d’onglets horizontaux pour une expérience utilisateur fluide.

### Onglet De base {#basic-tab}

![Onglet De base](/help/adaptive-forms/assets/tabs-on-top-basic.png)

* **Nom** - Vous pouvez identifier facilement un composant de formulaire en lui attribuant un nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

* **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

* **Masquer le titre** - Sélectionnez cette option pour masquer le titre du composant.

* **Inclure des données dans l’objet** - Sélectionnez « Inclure des données dans l’objet » pour placer les données de champ de l’assistant dans un objet JSON. Si cette option n’est pas sélectionnée, le fichier JSON des données d’envoi présente une structure plate pour les champs de l’assistant.

* **Disposition** - Vous pouvez utiliser une disposition fixe (simple) ou une disposition flexible (grille réactive) pour votre assistant. La disposition simple conserve tout ce qui est fixe, tandis que la grille réactive vous permet d’ajuster la position des composants en fonction de vos besoins. Par exemple, utilisez la grille réactive pour aligner « Prénom », « Deuxième prénom » et « Nom » dans un formulaire sur une seule ligne.

* **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.
* **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.
* **Désactiver le composant** - Sélectionnez cette option pour désactiver le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

### Répéter les onglets supérieurs {#repeat-tabs-on-top}

![Onglet Accessibilité](/help/adaptive-forms/assets/repeat-tabsontop.png)

Vous pouvez utiliser les options de répétition pour dupliquer le composant Onglets horizontaux et ses composants enfants, définir un nombre de répétitions minimal et maximal et faciliter la réplication de sections similaires dans un formulaire. Lors de l’interaction avec le composant Onglets horizontaux et de l’accès à ses paramètres, les options suivantes s’affichent :

* **Rendre les onglets horizontaux répétables** : fonctionnalité de basculement qui permet aux utilisateurs et utilisatrices d’activer ou de désactiver la fonctionnalité de répétabilité.
* **Nombre minimal de répétitions** : définit le nombre minimal de répétitions possibles du composant Onglets horizontaux. La valeur zéro indique que le composant Onglets horizontaux n’est pas répété. La valeur par défaut est zéro.
* **Nombre maximal de répétitions** : définit le nombre maximal de répétitions possibles du composant Onglets horizontaux. Par défaut, cette valeur est illimitée.

Pour gérer efficacement les sections répétables dans les Onglets horizontaux, procédez comme indiqué dans l’article [Création de formulaires avec des sections répétables](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html?lang=fr).

### Onglet Éléments {#items-tab}

![Onglet Éléments](/help/adaptive-forms/assets/items-tabs-on-top.png)

Le bouton **Ajouter** vous permet de sélectionner un composant à ajouter en tant que panneau à partir de la fenêtre de sélection de composant. Après avoir ajouté le composant, vous pouvez voir les options suivantes :

* **Icône** : L’icône identifie le composant du panneau dans la liste. Pointez sur l’icône pour afficher le nom complet du composant sous forme d’info-bulle.
* **Description** : Description utilisée comme texte du panneau. Par défaut, le nom du composant sélectionné pour le panneau.
* **Supprimer** : Appuyez ou cliquez sur cette option pour supprimer le panneau du composant Onglets horizontaux.
* **Réorganiser** : Appuyez ou cliquez et faites glisser pour réorganiser l’ordre des panneaux.

### Onglet Contenu de l’aide {#help-content}

![Onglet Contenu d’aide](/help/adaptive-forms/assets/helpcontent-tabs-on-top.png)

* **Description courte** : Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez l’option **Toujours afficher une description courte** pour l’afficher sous le composant.

* **Toujours afficher une description courte** - Activez cette option pour afficher la description courte sous le composant.

* **Texte d’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility}

![Onglet Accessibilité](/help/adaptive-forms/assets/accessibilty-tabs-on-top.png)

* **Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

* **Rôle HTML à annoncer par le lecteur d’écran** - Le rôle HTML est un attribut utilisé pour spécifier l’objectif d’un élément HTML pour les technologies d’assistance telles que les lecteurs d’écran. L’attribut rôle est utilisé pour fournir un contexte et une signification sémantique supplémentaires à un élément, ce qui facilite l’interprétation et l’annonce du contenu à l’utilisateur ou à l’utilisatrice par les lecteurs d’écran. Par exemple, dans AEM Forms, le libellé d’un champ de formulaire peut avoir le rôle « libellé » et son champ de saisie peut avoir le rôle « zone de texte ». Cela permet au lecteur d’écran de comprendre la relation entre le libellé et le champ de saisie, et de les annoncer correctement à l’utilisateur ou à l’utilisatrice.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue Conception permet aux créateurs et aux créatrices de modèles de contrôler l’affichage des éléments par défaut. Pour le composant Onglets horizontaux des formulaires adaptatifs, vous pouvez définir les éléments suivants :

* Composants principaux qu’un créateur ou une créatrice de formulaire peut ajouter aux Onglets horizontaux dans l’éditeur de formulaires adaptatifs.
* Noms simples pour les styles (classes CSS) qui peuvent être appliqués dans la boîte de dialogue des propriétés du composant Onglets horizontaux dans l’éditeur de formulaires adaptatifs.

Cela permet de rendre le processus de création et de personnalisation de formulaires plus simple et plus efficace.

### Onglet Composants autorisés {#allowed-components-tab}

L’onglet **Composants autorisés** permet à l’éditeur de modèles de définir les composants qui peuvent être ajoutés en tant qu’éléments aux panneaux dans le composant « Onglets horizontaux » de l’éditeur de formulaires adaptatifs.

### Onglet Styles {#styles-tab}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS d’un composant. Le composant principal « Onglets horizontaux » des formulaires adaptatifs prend en charge le [Système de style](/help/get-started/authoring.md#component-styling) d’AEM.

**Classes CSS par défaut** : vous pouvez fournir une classe CSS par défaut pour le composant principal « Onglets horizontaux » des formulaires adaptatifs.

* **Styles autorisés** : vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé « texte en gras » et fournir la classe CSS « police d’épaisseur : gras ». Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de formulaires adaptatifs. Pour appliquer un style, sélectionnez le composant auquel vous souhaitez appliquer le style dans l’éditeur de formulaires adaptatifs, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans la liste déroulante **Styles**. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

## Article connexe {#related-article}

* [Création d’un formulaire adaptatif dans une page AEM Sites ou un fragment d’expérience](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=fr)

* [Création d’un formulaire adaptatif autonome](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=fr)
