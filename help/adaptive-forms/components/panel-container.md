---
title: Composant principal de formulaires adaptatifs - Conteneur de panneau
description: Utilisation ou personnalisation du composant principal Conteneur de panneau de formulaires adaptatifs.
role: Architect, Developer, Admin, User
exl-id: 104836fe-8325-47de-978d-1ff2d6a9dd15
source-git-commit: e0ed415bd7f45fdca6fbbb8ba409604d9e82a647
workflow-type: ht
source-wordcount: '2036'
ht-degree: 100%

---

# Conteneur de panneau {#panel-container-adaptive-forms-core-component}

Dans un formulaire adaptatif, un panneau est un élément de conteneur qui peut être utilisé pour regrouper les éléments de formulaire associés. Il vous permet de regrouper et d’organiser différents éléments de formulaire de manière logique et significative. Cela peut contribuer à améliorer la structure et la lisibilité globale du formulaire, ce qui facilite la compréhension et la navigation des utilisateurs et utilisatrices.

Les panneaux peuvent également être utilisés pour créer des sections réductibles, ce qui peut s’avérer utile pour masquer les champs de formulaire complexes ou moins fréquemment utilisés, et donc faciliter et simplifier l’utilisation du formulaire. Ils vous permettent également d’inclure d’autres composants tels que du texte, des cases à cocher, des boutons, etc.

Ils peuvent également être utilisés pour définir différentes actions basées sur des règles, telles qu’envoyer un formulaire, ouvrir un site Web, afficher ou masquer des composants ou ajouter une instance d’un panneau.

**Exemple**

![exemple](/help/adaptive-forms/assets/panel-container.png)

## Utilisation {#reasons-to-use-panel-container}

Il existe plusieurs raisons d’utiliser un panneau dans un formulaire, notamment :

- **Organisation des éléments de formulaire** : un panneau peut être utilisé pour regrouper des éléments de formulaire associés, ce qui facilite la compréhension et la navigation des utilisateurs et utilisatrices dans le formulaire.

- **Amélioration de la structure des formulaires** : en regroupant les éléments de formulaire dans des panneaux, vous pouvez améliorer la structure et la lisibilité globale du formulaire, ce qui facilite sa compréhension.

- **Création de sections réductibles** : les panneaux peuvent être utilisés pour créer des sections réductibles, ce qui peut s’avérer utile pour masquer les champs de formulaire complexes ou moins fréquemment utilisés, et donc faciliter et simplifier l’utilisation du formulaire.

- **Améliorations apportées à l’utilisation** : en utilisant des panneaux pour organiser les éléments de formulaire, le formulaire est plus convivial et plus facile à utiliser, ce qui peut aboutir à des taux de remplissage plus élevés.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Conteneur de panneau des formulaires adaptatifs a été publié en février 2023 dans le cadre de la version 2.0.4 des composants principaux. Voici un tableau présentant toutes les versions prises en charge, la compatibilité AEM et les liens vers la documentation correspondante :

|  |  |
|---|---|
| Version du composant | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatible avec la <br>[version 2.0.4](/help/versions.md) et les versions ultérieures | Compatible | Compatible |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/versions.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Obtenez les dernières informations sur le composant principal Conteneur de panneau des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/panelcontainer/v1/panelcontainer). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience de votre conteneur de panneau pour les visiteurs et visiteuses qui utilisent la boîte de dialogue Configurer. Vous pouvez également définir facilement des options de conteneur de panneau pour une expérience client harmonieuse.

### Onglet De base {#basic-tab}

![Onglet De base](/help/adaptive-forms/assets/basic-panel.png)

- **Nom** - Vous pouvez identifier facilement un composant de formulaire en lui attribuant un nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

- **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

- **Masquer le titre** - Sélectionnez cette option pour masquer le titre du composant.

- **Associer les données des composants enfants lors de l’envoi du formulaire (encapsuler les données dans l’objet)** : lorsque l’option est sélectionnée, les données de ses composants enfants sont imbriquées dans l’objet JSON du composant parent. Cependant, si l’option n’est pas sélectionnée, les données JSON envoyées ont une structure plate, sans objet pour le composant parent. Par exemple :

   - Lorsque cette option est sélectionnée, les données des composants enfants (par exemple, Rue, Ville et Code postal) sont imbriquées dans le composant parent (Adresse) sous la forme d’un objet JSON. Cela crée une structure hiérarchique et les données sont organisées sous le composant parent.

     Structure des données envoyées :

     ```JSON
     { "Address":
     
     { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     
     }
     ```

   - Lorsque l’option n’est pas sélectionnée, les données JSON envoyées ont une structure plate sans objet pour le composant parent (Adresse). Toutes les données se trouvent au même niveau, sans organisation hiérarchique.


     Structure des données envoyées :

     ```JSON
        { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     ```

- **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.
- **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.
- **Désactiver le composant** - Sélectionnez cette option pour désactiver le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

### Onglet Répéter le panneau {#repeat-panel}

![onglet répéter](/help/adaptive-forms/assets/repeat-panel.png)

Vous pouvez utiliser les options de répétition pour dupliquer le conteneur du panneau et ses composants enfants, définir un nombre de répétitions minimal et maximal et faciliter la réplication de sections similaires dans un formulaire. Lors de l’interaction avec le composant de conteneur du panneau et de l’accès à ses paramètres, les options suivantes s’affichent :

- **Rendre l’assistant répétable** : fonctionnalité de basculement qui permet aux utilisateurs et utilisatrices d’activer ou de désactiver la fonctionnalité de répétabilité.
- **Nombre minimal de répétitions** : définit le nombre minimal de répétitions possibles du conteneur du panneau. La valeur zéro indique que le panneau Assistant n’est pas répété. La valeur par défaut est zéro.
- **Nombre maximal de répétitions** : définit le nombre maximal de répétitions possibles du conteneur du panneau. Par défaut, cette valeur est illimitée.

Pour gérer efficacement les sections répétables dans le conteneur du panneau, procédez comme indiqué dans l’article [Création de formulaires avec des sections répétables](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html?lang=fr).

### Onglet Contenu de l’aide {#help-content}

![Onglet Contenu d’aide](/help/adaptive-forms/assets/helpcontent-panel.png)


- **Description courte** : Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez l’option **Toujours afficher une description courte** pour l’afficher sous le composant.

- **Toujours afficher une description courte** - Activez cette option pour afficher la description courte sous le composant.

- **Texte d’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility}

![Onglet Accessibilité](/help/adaptive-forms/assets/accessibilty-panel.png)


- **Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

- **Rôle HTML à annoncer par le lecteur d’écran** - Le rôle HTML est un attribut utilisé pour spécifier l’objectif d’un élément HTML pour les technologies d’assistance telles que les lecteurs d’écran. L’attribut rôle est utilisé pour fournir un contexte et une signification sémantique supplémentaires à un élément, ce qui facilite l’interprétation et l’annonce du contenu à l’utilisateur ou à l’utilisatrice par les lecteurs d’écran. Par exemple, dans AEM Forms, le libellé d’un champ de formulaire peut avoir le rôle « libellé » et son champ de saisie peut avoir le rôle « zone de texte ». Cela permet au lecteur d’écran de comprendre la relation entre le libellé et le champ de saisie, et de les annoncer correctement à l’utilisateur ou à l’utilisatrice.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS pour le composant Conteneur de formulaire.

### Onglet Composants autorisés {#allowed-components-tab}

![Onglet Composants autorisés de la boîte de dialogue de conception](/help/adaptive-forms/assets/panel-container-allowed-component.png)

L’onglet **Composants autorisés** permet à l’éditeur de modèles de définir les composants qui peuvent être ajoutés en tant qu’éléments aux panneaux dans le composant de l’éditeur de formulaires adaptatifs.

### Onglet Composants par défaut {#default-components-tab}

![Onglet Composants par défaut de la boîte de dialogue de conception](/help/adaptive-forms/assets/panel-container-default-component.png)

L’onglet **Composants par défaut** permet à l’éditeur de modèles de spécifier les composants visibles par défaut en tant qu’éléments dans le composant Conteneur de formulaire dans l’éditeur de formulaires adaptatifs.

### Onglet Paramètres réactifs {#responsive-tab}

![Onglet Paramètres réactifs de la boîte de dialogue de conception](/help/adaptive-forms/assets/panel-container-responsive-style-tab.png)

L’onglet **Paramètres réactifs** permet à l’éditeur de modèles de spécifier le nombre de colonnes dans la grille à l’intérieur du composant Conteneur de formulaire de l’éditeur de formulaires adaptatifs.

### Onglet Paramètres de conteneur

![Onglet Paramètres de conteneur](/help/adaptive-forms/assets/panel-container-container-settings.png)

- **Disposition** - Vous pouvez utiliser une disposition fixe (simple) ou une disposition flexible (grille réactive) pour votre assistant. La disposition simple conserve tout ce qui est fixe, tandis que la grille réactive vous permet d’ajuster la position des composants en fonction de vos besoins. Par exemple, utilisez la grille réactive pour aligner « Prénom », « Deuxième prénom » et « Nom » dans un formulaire sur une seule ligne.

- **Désactiver la disposition** : sélectionnez cette option pour désactiver la sélection de la disposition dans la boîte de dialogue de modification d’un composant.

- **Activer l’image d’arrière-plan** : cette option permet à la personne de configurer les paramètres du panneau pour inclure un arrière-plan visuel afin d’améliorer l’attrait visuel.

- **Activer la couleur d’arrière-plan** : cette option vous permet de définir ou de modifier la couleur d’arrière-plan du panneau. Cette fonctionnalité est généralement utilisée dans la conception de l’interface utilisateur pour personnaliser l’apparence des panneaux dans une interface plus grande. Lorsque vous sélectionnez l’option **Activer la couleur d’arrière-plan**, l’option **Nuanciers uniquement** s’affiche. L’option **Nuanciers uniquement** vous permet de spécifier ou de sélectionner des couleurs pour l’arrière-plan, le texte ou d’autres éléments visuels du panneau à l’aide du bouton **Ajouter**.

### Onglet Styles {#styles-tab}

Le composant principal « Pièce jointe » des formulaires adaptatifs prend en charge le [Système de style](/help/get-started/authoring.md#component-styling) d’AEM.

![Boîte de dialogue de conception.](/help/adaptive-forms/assets/panel-container-styles-tab.png)

- **Classes CSS par défaut** : vous pouvez fournir une classe CSS par défaut pour le composant principal du groupe de cases à cocher des formulaires adaptatifs.

- **Styles autorisés** : vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé « texte en gras » et fournir la classe CSS « police d’épaisseur : gras ». Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de formulaires adaptatifs. Pour appliquer un style, sélectionnez le composant auquel vous souhaitez appliquer le style dans l’éditeur de formulaires adaptatifs, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans la liste déroulante **Styles**. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

### Onglet Propriétés personnalisées

![Boîte de dialogue Propriétés personnalisées](/help/adaptive-forms/assets/panel-container-custom-properties.png)

Les propriétés personnalisées vous permettent d’associer des attributs personnalisés (paires clé-valeur) à un composant principal de formulaire adaptatif à l’aide du modèle de formulaire. Les propriétés personnalisées sont répercutées dans la section des propriétés du rendu déocuplé du composant. Cela permet de créer un comportement de formulaire dynamique qui s’adapte en fonction des valeurs d’attributs personnalisés. Par exemple, les développeurs et développeuses peuvent concevoir plusieurs rendus d’un composant de formulaires découplés pour des plateformes mobiles, de bureau ou web, ce qui améliore considérablement l’expérience client sur un large éventail d’appareils.

- **Nom du groupe** : vous pouvez fournir un nom pour identifier le groupe de propriétés personnalisées. Vous pouvez ajouter, supprimer ou réorganiser plusieurs groupes de propriétés personnalisées. Après avoir ajouté le groupe de propriétés personnalisées, vous pouvez voir les options suivantes :

   - **Paires clé-valeur** : vous pouvez ajouter plusieurs noms ou valeurs de propriétés personnalisées en cliquant sur le bouton **Ajouter** pour chaque groupe de propriétés personnalisées.

   - **Supprimer** : appuyez ou cliquez pour supprimer le nom ou la valeur des propriétés personnalisées.

   - **Réorganiser** : appuyez ou cliquez et faites glisser pour réorganiser l’ordre du nom ou de la valeur des propriétés personnalisées.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Articles connexes {#related-articles}

{{more-like-this}}

## Voir également {#see-also}

{{see-also}}