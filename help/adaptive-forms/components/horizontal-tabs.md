---
title: Composant principal Forms adaptatif - Onglets horizontaux
description: Utilisation ou personnalisation des onglets horizontaux de Forms adaptatif du composant principal.
role: Architect, Developer, Admin, User
source-git-commit: 1e6460d318f4f9a5dfdcbb81723da01b51b72f3f
workflow-type: tm+mt
source-wordcount: '1584'
ht-degree: 3%

---


# Onglets horizontaux {#horizontal-tabs-adaptive-forms-core-component}

Les onglets horizontaux d’un formulaire adaptatif font référence à un modèle de conception dans lequel plusieurs sections d’un formulaire sont regroupées et affichées sous la forme d’onglets distincts, alignés horizontalement. L’utilisateur peut basculer entre les onglets pour accéder aux différentes sections du formulaire. Chaque onglet sert de déclencheur pour afficher et masquer le contenu du formulaire associé. Les onglets horizontaux permettent d’organiser les formulaires longs en sections gérables et d’améliorer l’expérience utilisateur. Les onglets peuvent vous aider à rendre un formulaire plus accessible aux utilisateurs présentant un handicap, car ils peuvent permuter entre les sections à l’aide de la navigation à l’aide du clavier.

Les onglets sont généralement créés sous la forme d’une série de liens ou de boutons, chaque lien ou bouton correspondant à une section du formulaire. Lorsqu’un utilisateur clique sur un onglet, le contenu du formulaire est mis à jour de manière dynamique afin d’afficher la section correspondante.

## Utilisation {#reasons-to-use-horizontal-tabs}

Les raisons courantes d’utiliser les onglets horizontaux dans un formulaire adaptatif sont les suivantes :

* **Utilisation améliorée**: Les onglets horizontaux permettent aux utilisateurs de parcourir plus facilement le formulaire, en particulier s’il comporte plusieurs sections ou un grand nombre de champs.

* **Gestion de l’espace**: Les onglets horizontaux permettent de préserver l’espace de l’écran en regroupant les sections de formulaire associées en onglets et en n’affichant qu’une seule section à la fois.

* **Meilleure organisation**: Les onglets offrent une structure claire et organisée pour un formulaire, ce qui permet aux utilisateurs de comprendre et de remplir plus facilement le formulaire.

* **Engagement accru des utilisateurs**: Les onglets horizontaux peuvent rendre un formulaire plus attrayant et attrayant visuellement pour les utilisateurs, ce qui peut améliorer le taux d’achèvement du formulaire.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Onglets horizontaux de Forms adaptatif a été publié en février 2023 dans le cadre de la version 2.0.4 des composants principaux. Voici un tableau présentant toutes les versions prises en charge, la compatibilité AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible avec<br>[version 2.0.4](/help/versions.md) et plus tard | Compatible | Compatible |

Pour plus d’informations sur les versions et versions des composants principaux, reportez-vous à la section [Versions des composants principaux](/help/versions.md) document.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Détails techniques {#technical-details}

Obtenez les dernières informations sur le composant principal des onglets Horizontaux de Forms adaptatif dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageHorizontal onglets/v1/pageHorizontal). Pour plus d’informations sur le développement des composants principaux, consultez la section [Documentation destinée aux développeurs sur les composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser votre expérience d’onglets horizontaux pour les visiteurs qui utilisent la boîte de dialogue Configurer . Vous pouvez également définir facilement des options d’onglets horizontaux pour une expérience utilisateur fluide.

### Onglet De base {#basic-tab}

![Onglet Simple](/help/adaptive-forms/assets/tabsontop_basictab.png)

* **Nom** - Vous pouvez identifier facilement un composant de formulaire avec son nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

* **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

* **Masquer le titre** - Sélectionnez l’option pour masquer le titre du composant.

* **Encapsuler des données dans l’objet** - Sélectionnez &quot;Placer les données dans un objet&quot; pour placer les données de champ de l’assistant dans un objet JSON. Si cette option n’est pas sélectionnée, le fichier JSON des données d’envoi présente une structure plate pour les champs de l’assistant.

* **Disposition** - Vous pouvez disposer d’une mise en page fixe (simple) ou d’une mise en page flexible (grille réactive) pour votre assistant. La mise en page simple conserve tout ce qui est fixe, tandis que la grille réactive vous permet d’ajuster la position des composants en fonction de vos besoins. Par exemple, utilisez la grille réactive pour aligner &quot;Prénom&quot;, &quot;Nom intermédiaire&quot; et &quot;Nom&quot; dans un formulaire sur une seule ligne.

* **Référence de liaison** - Une référence de liaison est une référence à un élément de données stocké dans une source de données externe et utilisé dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client dans un formulaire, en fonction de l’identifiant du client saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur transparente pour la collecte et la gestion des données.
* **Masquer le composant** - Sélectionnez l’option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par l’utilisateur.
* **Désactiver le composant** - Sélectionnez l’option pour désactiver le composant. Le composant désactivé n’est pas principal ni modifiable par l’utilisateur final. L’utilisateur peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

### Onglet Éléments {#items-tab}

![Onglet Éléments](/help/adaptive-forms/assets/tabsontop_itemstab.png)

Le **Ajouter** vous permet de sélectionner un composant à ajouter en tant que panneau à partir de la fenêtre de sélection de composant. Après avoir ajouté le composant, vous pouvez voir les options suivantes :

* **Icône** - L’icône identifie le composant du panneau dans la liste. Pointez sur l’icône pour afficher le nom complet du composant sous forme d’info-bulle.
* **Description** - Description utilisée comme texte du panneau. Par défaut, nom du composant sélectionné pour le panneau.
* **Supprimer** : appuyez ou cliquez sur cette option pour supprimer le panneau du composant d’accordéon.
* **Réorganiser** : appuyez ou cliquez dessus et faites glisser pour réorganiser l’ordre des panneaux.

### Onglet Contenu de l’aide {#help-content}

![Onglet Contenu de l’aide](/help/adaptive-forms/assets/tabsontop_helptab.png)

* **Description courte** - Une brève description est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez la variable **Toujours afficher une description courte** pour l’afficher sous le composant.

* **Toujours afficher une description courte** - Activez l’option pour afficher la description courte sous le composant.

* **Texte de l’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur clique sur l’icône d’aide (i) placée en regard du composant. Le texte d’aide fournit des informations plus détaillées que le texte d’étiquette ou d’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility}

![Onglet Accessibilité](/help/adaptive-forms/assets/tabsontop_accessibilitytab.png)

* **Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisé par les malvoyants. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom et tout message pertinent du champ (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs, y compris ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

* **Rôle de HTML à annoncer pour le lecteur d’écran** - Le rôle de HTML est un attribut utilisé pour spécifier l’objectif d’un élément de HTML pour les technologies d’assistance telles que les lecteurs d’écran. L’attribut role est utilisé pour fournir un contexte et une signification sémantique supplémentaires à un élément, ce qui facilite l’interprétation et l’annonce du contenu à l’utilisateur par les lecteurs d’écran. Par exemple, dans AEM Forms, le libellé d’un champ de formulaire peut avoir le rôle &quot;libellé&quot; et son champ de saisie peut avoir le rôle &quot;textbox&quot;. Cela permet au lecteur d’écran de comprendre la relation entre le libellé et le champ de saisie, et de les annoncer correctement à l’utilisateur.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue Conception permet aux créateurs de modèles de contrôler l’affichage des éléments par défaut. Pour le composant d’accordéon Forms adaptatif, vous pouvez définir les éléments suivants :

* Composants principaux qu’un créateur de formulaire peut ajouter à l’accordéon dans l’éditeur de Forms adaptatif
* Noms simples pour les styles (classes CSS) qui peuvent être appliqués dans la boîte de dialogue des propriétés du composant d’accordéon dans l’éditeur de Forms adaptatif.

Cela permet de rendre le processus de création et de personnalisation de formulaires plus simple et plus efficace.

### Onglet Composants autorisés {#allowed-components-tab}

Le **Composants autorisés** Cet onglet permet à l’éditeur de modèles de définir les composants qui peuvent être ajoutés en tant qu’éléments aux panneaux dans le composant Onglets horizontaux de l’éditeur Forms adaptatif.

### Onglet Styles {#styles-tab}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS d’un composant. Le composant principal Onglets horizontaux de Forms adaptatif prend en charge l’AEM [Système de style](/help/get-started/authoring.md#component-styling).

**Classes CSS par défaut**: Vous pouvez fournir une classe CSS par défaut pour le composant principal Onglets horizontaux de Forms adaptative.

**Styles autorisés**: Vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé &quot;bold text&quot; et fournir la classe CSS &quot;font-weight: bold&quot;. Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de Forms adaptatif. Pour appliquer un style, dans l’éditeur de Forms adaptatif, sélectionnez le composant auquel vous souhaitez appliquer le style, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans le **Styles** liste déroulante. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.
