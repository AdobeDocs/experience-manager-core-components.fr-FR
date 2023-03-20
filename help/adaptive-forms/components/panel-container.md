---
title: Composant principal Forms adaptatif - Conteneur de panneau
description: Utilisation ou personnalisation du composant principal du conteneur de panneau Forms adaptatif .
role: Architect, Developer, Admin, User
exl-id: 104836fe-8325-47de-978d-1ff2d6a9dd15
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '1696'
ht-degree: 2%

---

# Conteneur de panneau {#panel-container-adaptive-forms-core-component}

Dans un formulaire adaptatif, un panneau est un élément de conteneur qui peut être utilisé pour regrouper les éléments de formulaire associés. Il vous permet de regrouper et d’organiser différents éléments de formulaire de manière logique et significative. Cela peut contribuer à améliorer la structure globale et la lisibilité du formulaire, ce qui facilite la compréhension et la navigation des utilisateurs.

Les panneaux peuvent être utilisés pour créer des sections réductibles, ce qui peut s’avérer utile pour masquer les champs de formulaire complexes ou moins fréquemment utilisés, ce qui rend le formulaire simple et facile à utiliser. Il vous permet également d’inclure d’autres composants tels que du texte, une case à cocher ou un bouton.

Il peut également être utilisé pour définir différentes actions basées sur des règles, telles que l’envoi d’un formulaire, l’ouverture d’un site web, l’affichage/le masquage de composants ou l’ajout d’une instance d’un panneau.

**Exemple**

![](/help/adaptive-forms/assets/panel-container.png)

## Utilisation {#reasons-to-use-panel-container}

Il existe plusieurs raisons d’utiliser un panneau dans un formulaire, notamment :

* **Organisation des éléments de formulaire**: Un panneau peut être utilisé pour regrouper des éléments de formulaire associés, ce qui facilite la compréhension et la navigation des utilisateurs dans le formulaire.

* **Amélioration de la structure des formulaires**: En regroupant les éléments de formulaire dans des panneaux, vous pouvez améliorer la structure globale et la lisibilité du formulaire, ce qui facilite sa compréhension.

* **Création de sections réductibles**: Les panneaux peuvent être utilisés pour créer des sections réductibles, ce qui peut s’avérer utile pour masquer les champs de formulaire complexes ou moins fréquemment utilisés, ce qui rend le formulaire simple et facile à utiliser.

* **Amélioration de la convivialité**: En utilisant des panneaux pour organiser les éléments de formulaire, vous pouvez rendre le formulaire plus convivial et plus facile à utiliser, ce qui peut entraîner des taux d’achèvement plus élevés.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Accordéon de Forms adaptatif a été publié en février 2023 dans le cadre des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Voici un tableau de toutes les versions prises en charge, de la compatibilité AEM et des liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec<br>[version 2.0.4](/help/adaptive-forms/version.md) et plus tard | Compatible avec<br>[version 1.1.12](/help/adaptive-forms/version.md) et plus tard, mais moins de 2.0.0. |

Pour plus d’informations sur les versions et versions des composants principaux, reportez-vous à la section [Versions des composants principaux](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Obtenez les dernières informations sur le composant principal Conteneur de panneau de Forms adaptatif dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/panelcontainer/v1/panelcontainer). Pour plus d’informations sur le développement des composants principaux, consultez la section [Documentation destinée aux développeurs sur les composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience du conteneur de panneaux pour les visiteurs qui utilisent la boîte de dialogue Configurer . Vous pouvez également définir facilement des options de conteneur de panneaux pour une expérience utilisateur transparente.

### Onglet De base {#basic-tab}

![Onglet Simple](/help/adaptive-forms/assets/panelcontainer_basictab.png)

* **Nom** - Vous pouvez identifier facilement un composant de formulaire avec son nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

* **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

* **Masquer le titre** - Sélectionnez l’option pour masquer le titre du composant.

* **Encapsuler des données dans l’objet** - Sélectionnez &quot;Placer les données dans un objet&quot; pour placer les données de champ de l’assistant dans un objet JSON. Si cette option n’est pas sélectionnée, le fichier JSON des données d’envoi présente une structure plate pour les champs de l’assistant.

* **Disposition** - Vous pouvez disposer d’une mise en page fixe (simple) ou d’une mise en page flexible (grille réactive) pour votre assistant. La mise en page simple conserve tout ce qui est fixe, tandis que la grille réactive vous permet d’ajuster la position des composants en fonction de vos besoins. Par exemple, utilisez la grille réactive pour aligner &quot;Prénom&quot;, &quot;Nom intermédiaire&quot; et &quot;Nom&quot; dans un formulaire sur une seule ligne.

* **Référence de liaison** - Une référence de liaison est une référence à un élément de données stocké dans une source de données externe et utilisé dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client dans un formulaire, en fonction de l’identifiant du client saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur transparente pour la collecte et la gestion des données.
* **Masquer le composant** - Sélectionnez l’option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par l’utilisateur.
* **Désactiver le composant** - Sélectionnez l’option pour désactiver le composant. Le composant désactivé n’est pas principal ni modifiable par l’utilisateur final. L’utilisateur peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

### Onglet Contenu de l’aide {#help-content}

![Onglet Contenu de l’aide](/help/adaptive-forms/assets/panelcontainer_helptab.png)

* **Description courte** - Une brève description est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez la variable **Toujours afficher une description courte** pour l’afficher sous le composant.

* **Toujours afficher une description courte** - Activez l’option pour afficher la description courte sous le composant.

* **Texte de l’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur clique sur l’icône d’aide (i) placée en regard du composant. Le texte d’aide fournit des informations plus détaillées que le texte d’étiquette ou d’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility}

![Onglet Accessibilité](/help/adaptive-forms/assets/panelcontainer_accessibilitytab.png)

* **Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire destiné à être lu par les technologies d’assistance, telles que les lecteurs d’écran, utilisés par les malvoyants. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom et tout message pertinent du champ (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs, y compris ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

* **Rôle de HTML à annoncer pour le lecteur d’écran** - Le rôle de HTML est un attribut utilisé pour spécifier l’objectif d’un élément de HTML pour les technologies d’assistance telles que les lecteurs d’écran. L’attribut role est utilisé pour fournir un contexte et une signification sémantique supplémentaires à un élément, ce qui facilite l’interprétation et l’annonce du contenu à l’utilisateur par les lecteurs d’écran. Par exemple, dans AEM Forms, le libellé d’un champ de formulaire peut avoir le rôle &quot;libellé&quot; et son champ de saisie peut avoir le rôle &quot;textbox&quot;. Cela permet au lecteur d’écran de comprendre la relation entre le libellé et le champ de saisie, et de les annoncer correctement à l’utilisateur.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS du composant de conteneur Panneau.

### Onglet Composants autorisés {#allowed-components-tab}

![Onglets Composants autorisés](/help/adaptive-forms/assets/panel_allowedcomponent.png)

Le **Composants autorisés** Cet onglet permet à l’éditeur de modèles de définir les composants qui peuvent être ajoutés en tant qu’éléments aux panneaux dans le composant Conteneur de panneau de l’éditeur Forms adaptatif.

### Onglet Composants par défaut {#default-component-tab}

Cet onglet permet à l’éditeur de modèles de mapper les composants qui peuvent être ajoutés en tant qu’éléments aux panneaux dans le composant de conteneur Panneau dans l’éditeur Forms adaptatif.

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

L’onglet permet de définir et de gérer les styles CSS d’un composant. Le composant principal du panneau Forms adaptatif prend en charge l’AEM [Système de style](/help/get-started/authoring.md#component-styling).

![Onglet Style](/help/adaptive-forms/assets/panel_style.png)

* **Classes CSS par défaut**: Vous pouvez fournir une classe CSS par défaut pour le composant principal Forms adaptatif.

* **Styles autorisés**: Vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé &quot;bold text&quot; et fournir la classe CSS &quot;font-weight: bold&quot;. Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans Forms adaptatif . Pour appliquer un style, dans l’éditeur de Forms adaptatif, sélectionnez le composant auquel vous souhaitez appliquer l’éditeur, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans la **Styles** liste déroulante. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

* **Rôle de HTML à annoncer pour le lecteur d’écran** - Le rôle de HTML est un attribut utilisé pour spécifier l’objectif d’un élément de HTML pour les technologies d’assistance telles que les lecteurs d’écran. L’attribut role est utilisé pour fournir un contexte et une signification sémantique supplémentaires à un élément, ce qui facilite l’interprétation et l’annonce du contenu à l’utilisateur par les lecteurs d’écran. Par exemple, dans AEM Forms, le libellé d’un champ de formulaire peut avoir le rôle &quot;libellé&quot; et son champ de saisie peut avoir le rôle &quot;textbox&quot;. Cela permet au lecteur d’écran de comprendre la relation entre le libellé et le champ de saisie, et de les annoncer correctement à l’utilisateur.

