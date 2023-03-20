---
title: Composant principal Adaptive Forms - Titre
description: Utilisation ou personnalisation du composant principal Titre du Forms adaptatif .
role: Architect, Developer, Admin, User
exl-id: 33eac885-8d66-4a5c-9a32-0ba11e6de293
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '862'
ht-degree: 13%

---

# Titre {#title-input-adaptive-forms-core-component}

Dans un formulaire adaptatif, un &quot;titre&quot; fait référence au texte qui s’affiche en haut du formulaire, généralement sous l’en-tête . Le titre est spécifié à l’aide du composant Titre . Ce composant peut être ajouté à la disposition du formulaire et son texte peut être modifié pour correspondre à l’objectif ou au sujet du formulaire. Le titre sert de libellé ou de brève description du formulaire pour l’utilisateur et permet de distinguer le formulaire des autres.

**Exemple**

![](/help/adaptive-forms/assets/title.png)

## Utilisation {#reasons-to-use-title-in-an-adaptive-form}

Il existe plusieurs raisons pour lesquelles il est recommandé d’utiliser un titre dans un formulaire :

* **Clarité**: Un titre identifie clairement l’objectif du formulaire, ce qui permet aux utilisateurs de comprendre les informations qu’ils doivent fournir.

* **Organisation**: Un titre peut vous aider à organiser les formulaires par sujet ou objectif, ce qui facilite la recherche du formulaire dont les utilisateurs ont besoin.

* **Accessibilité**: Un titre est un élément clé pour les utilisateurs ayant des besoins d’accessibilité, car il est lu à haute voix par les lecteurs d’écran, ce qui permet aux utilisateurs de comprendre le contexte du formulaire.

* **Marques**: Un titre peut également être utilisé pour afficher le nom d’une entreprise ou d’une organisation, ce qui contribue à créer un sentiment de confiance et de familiarité avec l’utilisateur.

* **Navigation**: Un titre peut également s’avérer utile pour parcourir le formulaire, en particulier s’il est long ou complexe.

* **Optimisation du moteur de recherche (SEO)**: Le fait d’avoir un titre sur le formulaire permet également d’effectuer des opérations d’optimisation pour les moteurs de recherche, car ce dernier permet de déterminer la pertinence d’une page web pour une requête.

Dans l’ensemble, le titre d’un formulaire est un aspect important de l’expérience utilisateur. Il doit être utilisé pour fournir un libellé clair et concis pour le formulaire, qui aide les utilisateurs à comprendre le contexte et l’objectif du formulaire.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Accordéon de Forms adaptatif a été publié en février 2023 dans le cadre des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Voici un tableau de toutes les versions prises en charge, de la compatibilité AEM et des liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec<br>[version 2.0.4](/help/adaptive-forms/version.md) et plus tard | Compatible avec<br>[version 1.1.12](/help/adaptive-forms/version.md) et plus tard, mais moins de 2.0.0. |

Pour plus d’informations sur les versions et versions des composants principaux, reportez-vous à la section [Versions des composants principaux](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Détails techniques {#technical-details}

Découvrez les informations les plus récentes sur le composant principal du titre de Forms adaptatif dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/title/v1/title). Pour plus d’informations sur le développement des composants principaux, consultez la section [Documentation destinée aux développeurs sur les composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser votre expérience de titre pour les visiteurs qui utilisent la boîte de dialogue Configurer . Vous pouvez également définir facilement des options de titre pour une expérience utilisateur transparente.

![Onglet Simple](/help/adaptive-forms/assets/title_properties.png)

La boîte de dialogue de modification permet à l’auteur de contenu de définir le texte du titre et de sélectionner le niveau de titre.

* **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.
* **Type /Size** - Définit le niveau d’en-tête du titre.
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la couche de données.
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

## Boîte de dialogue de conception {#design-dialog}

Cet onglet permet de définir et de gérer les styles CSS du composant Sélecteur de date.

### Titre

L’onglet Titre permet aux auteurs de modèles de définir des éléments d’en-tête de HTML par défaut et autorisés pour les auteurs de formulaires :

![Onglet Titre de la boîte de dialogue de conception](/help/adaptive-forms/assets/title_heading.png)

* **Éléments d’en-tête autorisés**: Une liste comportant plusieurs options permettant à l’auteur du modèle de choisir les en-têtes que l’auteur peut utiliser pour le titre.

* **Elément d’en-tête par défaut**: Liste déroulante qui définit l’élément Titre par défaut pour le composant Titre.

### Onglet Styles {#styles-tab}

L’onglet permet de définir et de gérer les styles CSS d’un composant. Le composant principal Sélecteur de date de Forms adaptatif prend en charge l’AEM [Système de style](/help/get-started/authoring.md#component-styling).

![Onglet Titre de la boîte de dialogue de conception](/help/adaptive-forms/assets/title_styles.png)

* **Classes CSS par défaut**: Vous pouvez fournir une classe CSS par défaut pour le composant principal Sélecteur de date du Forms adaptatif .

* **Styles autorisés**: Vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé &quot;bold text&quot; et fournir la classe CSS &quot;font-weight: bold&quot;. Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de Forms adaptatif. Pour appliquer un style, dans l’éditeur de Forms adaptatif, sélectionnez le composant auquel vous souhaitez appliquer le style, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans le **Styles** liste déroulante. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

### Onglet Formats {#format-tab}

L’onglet Formats vous permet de définir des formats de date par défaut et personnalisés.

![Onglet Format](/help/adaptive-forms/assets/title_styles.png)


