---
title: Composant principal des formulaires adaptatifs - Titre
description: Utilisation ou personnalisation du composant principal « Titre » dans les formulaires adaptatifs.
role: Architect, Developer, Admin, User
exl-id: 33eac885-8d66-4a5c-9a32-0ba11e6de293
source-git-commit: 59cd9d65bf4c1be6ab2eaf15bbb747b532863fdd
workflow-type: ht
source-wordcount: '899'
ht-degree: 100%

---

# Titre {#title-input-adaptive-forms-core-component}

Dans un formulaire adaptatif, un « titre » fait référence au texte qui s’affiche en haut du formulaire, généralement sous l’en-tête. Le titre est spécifié à l’aide du composant Titre. Ce composant peut être ajouté à la disposition du formulaire et son texte peut être modifié pour correspondre à l’objectif ou au sujet du formulaire. Le titre sert de libellé ou de brève description du formulaire pour l’utilisateur ou l’utilisatrice et permet de distinguer le formulaire des autres.

**Exemple**

![](/help/adaptive-forms/assets/title.png)

## Utilisation {#reasons-to-use-title-in-an-adaptive-form}

Il est recommandé d’utiliser un titre dans un formulaire pour plusieurs raisons :

* **Clarté** : un titre identifie clairement l’objectif du formulaire, ce qui permet aux utilisateurs et aux utilisatrices de comprendre les informations qu’ils ou elles doivent fournir.

* **Organisation** : un titre peut vous aider à organiser les formulaires par sujet ou objectif, ce qui facilite la recherche du formulaire dont les utilisateurs et utilisatrices ont besoin.

* **Accessibilité** : un titre est un élément clé pour les utilisateurs ou les utilisatrices ayant des besoins en matière d’accessibilité, car il est lu à haute voix par les lecteurs d’écran, ce qui permet aux utilisateurs et aux utilisatrices de comprendre le contexte du formulaire.

* **Image de marque** : un titre peut également être utilisé pour afficher le nom d’une entreprise ou d’une organisation, ce qui contribue à créer un sentiment de confiance et de familiarité chez l’utilisateur ou l’utilisatrice.

* **Navigation** : un titre peut également s’avérer utile pour parcourir le formulaire, en particulier s’il est long ou complexe.

* **Optimisation du moteur de recherche (SEO)** : le fait d’avoir un titre sur le formulaire permet également d’effectuer des opérations d’optimisation des moteurs de recherche, car ce dernier permet de déterminer la pertinence d’une page Web pour une requête.

Dans l’ensemble, le titre d’un formulaire est un aspect important de l’expérience client. Il doit être utilisé pour fournir un libellé clair et concis pour le formulaire, qui aide les utilisateurs et les utilisatrices à comprendre le contexte et l’objectif du formulaire.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Accordéon des formulaires adaptatifs a été publié en février 2023 au sein des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec la <br>[version 2.0.4](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible avec les<br>[versions 1.1.12](/help/adaptive-forms/version.md) à 2.0.0 exclue. |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Détails techniques {#technical-details}

Retrouvez les informations les plus récentes sur le composant principal « Titre » des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/title/v1/title). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience de titre pour les visiteurs et les visiteuses à l’aide de la boîte de dialogue Configurer. Vous pouvez également définir facilement des options de titre pour une expérience utilisateur fluide.

![Onglet De base](/help/adaptive-forms/assets/title_properties.png)

La boîte de dialogue de modification permet au créateur ou à la créatrice de contenu de définir le texte du titre et de sélectionner le niveau de titre.

* **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.
* **Type/Taille** - Définit le niveau d’en-tête du titre.
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la couche de données.
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

## Boîte de dialogue de conception {#design-dialog}

L’onglet Conception permet de définir et de gérer les styles CSS du composant Sélecteur de date.

### Titre

L’onglet Titre permet aux créateurs et créatrices de modèles de définir et d’autoriser des éléments d’en-tête HTML pour les créateurs et créatrices de formulaires :

![Onglet Titre de la boîte de dialogue de conception](/help/adaptive-forms/assets/title_heading.png)

* **Éléments d’en-tête autorisés** : une liste comportant plusieurs options permettant au créateur ou à la créatrice du modèle de choisir les en-têtes qui peuvent être utilisés pour le titre.

* **Élément d’en-tête par défaut** : liste déroulante qui définit l’élément En-tête par défaut pour le composant Titre.

### Onglet Styles {#styles-tab}

Cet onglet vous permet de définir et de gérer les styles CSS d’un composant. Le composant principal Sélecteur de date des formulaires adaptatifs prend en charge le [Système de style](/help/get-started/authoring.md#component-styling) d’AEM.

![Onglet Titre de la boîte de dialogue de conception.](/help/adaptive-forms/assets/title_styles.png)

* **Classes CSS par défaut** : vous pouvez indiquer une classe CSS par défaut pour le composant principal Sélecteur de date des formulaires adaptatifs.

* **Styles autorisés** : vous pouvez appliquer des styles en indiquant un nom et la classe CSS du style. Par exemple, vous pouvez créer un style nommé « texte en gras » et fournir la classe CSS « police d’épaisseur : gras ». Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de formulaires adaptatifs. Pour appliquer un style, sélectionnez le composant auquel vous souhaitez appliquer le style dans l’éditeur de formulaires adaptatifs, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans la liste déroulante **Styles**. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

### Onglet Formats {#format-tab}

L’onglet Formats vous permet de définir des formats de date par défaut et personnalisés.

![Onglet Format.](/help/adaptive-forms/assets/title_styles.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->


>[!MORELIKETHIS]
>
>* [Accordéon](/help/adaptive-forms/components/accordion.md)
>* [Bouton](/help/adaptive-forms/components/button.md)
>* [Groupe de cases à cocher](/help/adaptive-forms/components/checkbox-group.md)
>* [Sélecteur de date](/help/adaptive-forms/components/date-picker.md)
>* [Liste déroulante](/help/adaptive-forms/components/drop-down.md)
>* [Entrée d’e-mail](/help/adaptive-forms/components/email-input.md)
>* [Conteneur de formulaires](/help/adaptive-forms/components/form-container.md)
>* [Pièce jointe](/help/adaptive-forms/components/file-attachment.md)
>* [Pied de page](/help/adaptive-forms/components/footer.md)
>* [En-tête](/help/adaptive-forms/components/header.md)
>* [Onglets horizontaux](/help/adaptive-forms/components/horizontal-tabs.md)
>* [Image](/help/adaptive-forms/components/image.md)
>* [Entrée de nombre](/help/adaptive-forms/components/number-input.md)
>* [Conteneur de panneau](/help/adaptive-forms/components/panel-container.md)
>* [Bouton radio](/help/adaptive-forms/components/radio-button.md)
>* [Bouton de réinitialisation](/help/adaptive-forms/components/reset-button.md)
>* [Bouton Envoyer](/help/adaptive-forms/components/submit-button.md)
>* [Entrée téléphonique](/help/adaptive-forms/components/telephone-input.md)
>* [Entrée de texte](/help/adaptive-forms/components/text-input.md)
>* [Texte](/help/adaptive-forms/components/text.md)
>* [Assistant](/help/adaptive-forms/components/wizard.md)

## Voir également {#see-also}

{{see-also}}