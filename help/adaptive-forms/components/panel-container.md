---
title: Composant principal de formulaires adaptatifs - Conteneur de panneau
description: Utilisation ou personnalisation du composant principal Conteneur de panneau de formulaires adaptatifs.
role: Architect, Developer, Admin, User
exl-id: 104836fe-8325-47de-978d-1ff2d6a9dd15
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: ht
source-wordcount: '1696'
ht-degree: 100%

---

# Conteneur de panneau {#panel-container-adaptive-forms-core-component}

Dans un formulaire adaptatif, un panneau est un élément de conteneur qui peut être utilisé pour regrouper les éléments de formulaire associés. Il vous permet de regrouper et d’organiser différents éléments de formulaire de manière logique et significative. Cela peut contribuer à améliorer la structure et la lisibilité globale du formulaire, ce qui facilite la compréhension et la navigation des utilisateurs et utilisatrices.

Les panneaux peuvent être utilisés pour créer des sections réductibles, ce qui peut s’avérer utile pour masquer les champs de formulaire complexes ou moins fréquemment utilisés, et donc faciliter et simplifier l’utilisation du formulaire. Ils vous permettent également d’inclure d’autres composants tels que du texte, des cases à cocher, ou des boutons.

Ils peuvent également être utilisés pour définir différentes actions basées sur des règles, telles qu’envoyer un formulaire, ouvrir un site web, afficher ou masquer des composants ou ajouter une instance d’un panneau.

**Exemple**

![](/help/adaptive-forms/assets/panel-container.png)

## Utilisation {#reasons-to-use-panel-container}

Il existe plusieurs raisons d’utiliser un panneau dans un formulaire, notamment :

* **Organisation des éléments de formulaire** : un panneau peut être utilisé pour regrouper des éléments de formulaire associés, ce qui facilite la compréhension et la navigation des utilisateurs et utilisatrices dans le formulaire.

* **Amélioration de la structure des formulaires** : en regroupant les éléments de formulaire dans des panneaux, vous pouvez améliorer la structure et la lisibilité globale du formulaire, ce qui facilite sa compréhension.

* **Création de sections réductibles** : les panneaux peuvent être utilisés pour créer des sections réductibles, ce qui peut s’avérer utile pour masquer les champs de formulaire complexes ou moins fréquemment utilisés, et donc faciliter et simplifier l’utilisation du formulaire.

* **Améliorations apportées à l’utilisation** : en utilisant des panneaux pour organiser les éléments de formulaire, le formulaire est plus convivial et plus facile à utiliser, ce qui peut aboutir à des taux de remplissage plus élevés.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Accordéon des formulaires adaptatifs a été publié en février 2023 au sein des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec la <br>[version 2.0.4](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible avec les<br>[versions 1.1.12](/help/adaptive-forms/version.md) à 2.0.0 exclue. |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Obtenez les dernières informations sur le composant principal Conteneur de panneau des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/panelcontainer/v1/panelcontainer). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience de votre conteneur de panneau pour les visiteurs et visiteuses qui utilisent la boîte de dialogue Configurer. Vous pouvez également définir facilement des options de conteneur de panneau pour une expérience client harmonieuse.

### Onglet De base {#basic-tab}

![Onglet De base](/help/adaptive-forms/assets/panelcontainer_basictab.png)

* **Nom** : Vous pouvez identifier facilement un composant de formulaire en lui attribuant un nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

* **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

* **Masquer le titre** - Sélectionnez cette option pour masquer le titre du composant.

* **Inclure des données dans l’objet** - Sélectionnez « Inclure des données dans l’objet » pour placer les données de champ de l’assistant dans un objet JSON. Si cette option n’est pas sélectionnée, le fichier JSON des données d’envoi présente une structure plate pour les champs de l’assistant.

* **Disposition** - Vous pouvez utiliser une disposition fixe (simple) ou une disposition flexible (grille réactive) pour votre assistant. La disposition simple conserve tout ce qui est fixe, tandis que la grille réactive vous permet d’ajuster la position des composants en fonction de vos besoins. Par exemple, utilisez la grille réactive pour aligner « Prénom », « Deuxième prénom » et « Nom » dans un formulaire sur une seule ligne.

* **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.
* **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.
* **Désactiver le composant** - Sélectionnez cette option pour désactiver le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

### Onglet Contenu de l’aide {#help-content}

![Onglet Contenu d’aide](/help/adaptive-forms/assets/panelcontainer_helptab.png)

* **Description courte** - Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez l’option **Toujours afficher une description courte** pour l’afficher sous le composant.

* **Toujours afficher une description courte** - Activez cette option pour afficher la description courte sous le composant.

* **Texte d’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility}

![Onglet Accessibilité](/help/adaptive-forms/assets/panelcontainer_accessibilitytab.png)

* **Texte pour les lecteurs d’écran** : Il s’agit d’un texte supplémentaire conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

* **Rôle HTML à annoncer par le lecteur d’écran** - Le rôle HTML est un attribut utilisé pour spécifier l’objectif d’un élément HTML pour les technologies d’assistance telles que les lecteurs d’écran. L’attribut rôle est utilisé pour fournir un contexte et une signification sémantique supplémentaires à un élément, ce qui facilite l’interprétation et l’annonce du contenu à l’utilisateur ou à l’utilisatrice par les lecteurs d’écran. Par exemple, dans AEM Forms, le libellé d’un champ de formulaire peut avoir le rôle « libellé » et son champ de saisie peut avoir le rôle « zone de texte ». Cela permet au lecteur d’écran de comprendre la relation entre le libellé et le champ de saisie, et de les annoncer correctement à l’utilisateur ou à l’utilisatrice.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS pour le composant Conteneur de panneau.

### Onglet Composants autorisés {#allowed-components-tab}

![Onglets Composants autorisés.](/help/adaptive-forms/assets/panel_allowedcomponent.png)

L’onglet **Composants autorisés** permet à l’éditeur de modèles de définir les composants qui peuvent être ajoutés en tant qu’éléments aux panneaux dans le composant Conteneur de panneau de l’éditeur de formulaires adaptatifs.

### Onglet Composants par défaut {#default-component-tab}

Cet onglet permet à l’éditeur de modèles de mapper les composants qui peuvent être ajoutés en tant qu’éléments aux panneaux dans le composant Conteneur de panneau de l’éditeur de formulaires adaptatifs.

![Composant par défaut du panneau.](/help/adaptive-forms/assets/panel_defaultcomponent.png)

### Paramètres réactifs {#responsive-settings}

Cet onglet permet à l’éditeur de modèles de définir le nombre de colonnes à afficher dans la grille réactive.

![Grille réactive.](/help/adaptive-forms/assets/panel_responsivesettings.png)

### Onglet Paramètres de conteneur {#container-setting-tab}

L’onglet Paramètres du conteneur permet de définir la position des composants dans l’éditeur de formulaires adaptatifs.

![Paramètres de conteneur.](/help/adaptive-forms/assets/panel_settings.png)

* **Disposition** : la disposition simple conserve tout ce qui est fixe, tandis que la grille réactive vous permet de modifier la position des composants en fonction de vos besoins.
* **Désactiver la disposition** : vous pouvez également désactiver la disposition dans la boîte de dialogue de modification en activant la case **Désactiver la disposition**.
* **Activer l’image d’arrière-plan** : cet onglet permet de définir l’image et la couleur d’arrière-plan dans l’éditeur de modèles.
* **Activer la couleur d’arrière-plan** : cet onglet permet de définir la couleur d’arrière-plan dans l’éditeur de modèles.

### Onglet Styles {#styles-tab}

Cet onglet vous permet de définir et de gérer les styles CSS d’un composant. Le composant principal Conteneur de panneau des formulaires adaptatifs prend en charge le [Système de style](/help/get-started/authoring.md#component-styling) d’AEM.

![Onglet Styles.](/help/adaptive-forms/assets/panel_style.png)

* **Classes CSS par défaut** : vous pouvez fournir une classe CSS par défaut pour le composant principal des formulaires adaptatifs.

* **Styles autorisés** : vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé « texte en gras » et fournir la classe CSS « police d’épaisseur : gras ». Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans les formulaires adaptatifs. Pour appliquer un style, sélectionnez le composant auquel vous souhaitez appliquer le style dans l’éditeur de formulaires adaptatifs, accédez à la boîte de dialogue des propriétés, puis sélectionnez le style de votre choix dans la liste déroulante **Styles**. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

* **Rôle HTML à annoncer par le lecteur d’écran** - Le rôle HTML est un attribut utilisé pour spécifier l’objectif d’un élément HTML pour les technologies d’assistance telles que les lecteurs d’écran. L’attribut rôle est utilisé pour fournir un contexte et une signification sémantique supplémentaires à un élément, ce qui facilite l’interprétation et l’annonce du contenu à l’utilisateur ou à l’utilisatrice par les lecteurs d’écran. Par exemple, dans AEM Forms, le libellé d’un champ de formulaire peut avoir le rôle « libellé » et son champ de saisie peut avoir le rôle « zone de texte ». Cela permet au lecteur d’écran de comprendre la relation entre le libellé et le champ de saisie, et de les annoncer correctement à l’utilisateur ou à l’utilisatrice.

