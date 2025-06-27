---
title: Composant principal des formulaires adaptatifs - Pied de page
description: Utilisation ou personnalisation du composant principal Pied de page des formulaires adaptatifs.
role: Architect, Developer, Admin, User
exl-id: c8e7d3fe-4b82-4a80-8da2-19f6cff1e3e9
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '767'
ht-degree: 100%

---


# Pied de page {#footer-adaptive-forms-core-component}

Un composant Pied de page d’un formulaire adaptatif est une zone qui s’affiche généralement au bas du formulaire et qui contient des informations telles qu’un avis de copyright, des liens vers des ressources connexes ou des coordonnées. Un pied de page peut fournir des informations supplémentaires, telles que la date de la dernière mise à jour, ce qui peut être bénéfique pour les utilisateurs ou les utilisatrices ayant des besoins en matière d’accessibilité.

{{traditional-aem}}

**Exemple**

![exemple](/help/adaptive-forms/assets/footer.png)

## Utilisation {#reasons-to-use-footer}

Il existe plusieurs raisons pour lesquelles il est bénéfique d’inclure un composant Pied de page dans un formulaire, notamment :

- **Exigences juridiques** : il peut être requis pour certains formulaires d’inclure une clause de non-responsabilité, un avis de copyright ou d’autres informations juridiques. Un pied de page est un endroit pratique pour inclure ces informations.

- **Navigation** : un pied de page peut fournir des liens vers d’autres pages importantes du site Web, telles qu’une politique de confidentialité, les conditions d’utilisation ou une page de contact.

- **Image de marque** : un pied de page peut être utilisé pour inclure un logo ou d’autres éléments d’image de marque, ce qui contribue à renforcer l’identité de l’organisation ou du site Web.

- **Cohérence** : un pied de page est cohérent au niveau de la conception et de la mise en page du formulaire, ce qui rend la navigation plus intuitive et plus facile pour les utilisateurs et les utilisatrices.

- **Contexte supplémentaire** : un pied de page peut fournir un contexte supplémentaire au formulaire, tel qu’un texte décrivant le formulaire ou un lien vers des ressources associées, ce qui le rend plus informatif et convivial.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Pied de page des formulaires adaptatifs a été publié en février 2023 au sein des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec la <br>[version 2.0.4](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible avec les<br>[versions 1.1.12](/help/adaptive-forms/version.md) à 2.0.0 exclue. |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Découvrez les informations les plus récentes sur le composant principal Pied de page des formulaires adaptatifs dans la documentation technique de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/footer/v1/footer). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).


## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser votre expérience de pied de page pour les visiteurs et les visiteuses qui utilisent la boîte de dialogue de configuration. Vous pouvez également définir facilement des options de pied de page pour une expérience utilisateur fluide.

![Onglet Propriétés](/help/adaptive-forms/assets/footer_propertiestab.png)

- **Boîte de dialogue Modifier**
La boîte de dialogue de modification fournit des outils de mise en forme de texte enrichi standard qui permettent à l’utilisateur ou à l’utilisatrice de créer du texte pour le pied de page.

- **Gras** - Cette option est utilisée pour appliquer le format Gras au texte sélectionné ou au texte saisi après le curseur. `Ctrl+B` est un raccourci clavier.

- **Italique** - Cette option applique une mise en forme en italique au texte sélectionné ou au texte saisi après le curseur. `Ctrl+I` est un raccourci clavier.

![Options de puces](/help/adaptive-forms/assets/footer_bullet.png)


- **Puce**

   - **Icône Puces** - Utilisée pour formater le texte sélectionné sous forme d’une liste à puces ou commencer l’insertion d’une liste à puces après le curseur. Pour mettre fin à une liste à puces, appuyez ou cliquez de nouveau sur le bouton Puces ou saisissez deux retours chariot.

   - **Icône Liste numérotée** - Utilisée pour mettre en forme le texte sélectionné sous forme de liste numérotée ou commencer l’insertion d’une liste numérotée après le curseur. Pour mettre fin à une liste numérotée, appuyez ou cliquez de nouveau sur le bouton Numérotée ou saisissez deux retours chariot.

   - **Icône Ajouter un retrait négatif** : Ajoute un retrait négatif au texte ou du texte saisi après le curseur. Uniquement actif si le texte ou la position sélectionnés du curseur est déjà mis en retrait.

   - **Icône Mettre en retrait** - Met en retrait le texte ou le texte sélectionné après le curseur.

![Options d’hyperlien](/help/adaptive-forms/assets/footer_link.png)

- **Lien hypertexte**

   - **Chemin** - Saisir le chemin
      1. Utilisation de la boîte de dialogue Ouvrir la sélection pour choisir un chemin dans AEM.
      1. Si le lien ne se trouve pas dans AEM, saisissez l’URL absolue.
      1. Les chemins non absolus sont interprétés comme relatifs à AEM.

   - **Texte secondaire** - Saisir un autre texte descriptif pour le lien.

   - **Cible** - Sélectionner le comportement du lien
      - Cible
      - Même onglet
      - Nouvel onglet
      - Cadre parent
      - Cadre supérieur

   - **Icône Dissocier** - Cette option supprime un lien déjà appliqué au texte sélectionné. Cette option est uniquement active lorsqu’un lien est déjà sélectionné.

   - **Icône Format de paragraphe** - Cette option vous permet d’appliquer une mise en forme de paragraphe au texte sélectionné. Elle permet également de mettre en forme le texte inséré après le curseur. Définit le niveau d’en-tête du titre.

- **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la couche de données.

   - Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   - Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   - La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Articles connexes {#related-articles}

{{more-like-this}}

## Voir également {#see-also}

{{see-also}}
