---
title: Composant principal Adaptive Forms - Pied de page
description: Utilisation ou personnalisation du composant principal Pied de page de Forms adaptatif .
role: Architect, Developer, Admin, User
source-git-commit: b378fbd5695f82b8fc9de3a2d53a8387099ae33b
workflow-type: tm+mt
source-wordcount: '749'
ht-degree: 16%

---


# Pied de page {#footer-adaptive-forms-core-component}

Un composant de pied de page d’un formulaire adaptatif est une zone qui s’affiche généralement au bas du formulaire et qui contient des informations telles qu’un avis de copyright, des liens vers des ressources connexes ou des coordonnées. Un pied de page peut fournir des informations supplémentaires, telles que la date de la dernière mise à jour, ce qui peut être bénéfique pour les utilisateurs ayant des besoins d’accessibilité.

**Exemple**

![](/help/adaptive-forms/assets/footer.png)

## Utilisation {#reasons-to-use-footer}

Il existe plusieurs raisons pour lesquelles il est bénéfique d’inclure un composant de pied de page dans un formulaire, notamment :

* **Exigences juridiques**: Certains formulaires peuvent être requis pour inclure une clause de non-responsabilité, un avis de copyright ou d’autres informations juridiques. Un pied de page est un endroit pratique pour inclure ces informations.

* **Navigation**: Un pied de page peut fournir des liens vers d’autres pages importantes du site Web, telles qu’une politique de confidentialité, les conditions d’utilisation ou une page de contact.

* **Marques**: Un pied de page peut être utilisé pour inclure un logo ou d’autres éléments d’identité graphique, ce qui contribue à renforcer l’identité de l’organisation ou du site web.

* **Cohérence**: Un pied de page est cohérent au niveau de la conception et de la mise en page du formulaire, ce qui rend la navigation plus intuitive et plus facile pour les utilisateurs.

* **Contexte supplémentaire**: Un pied de page peut fournir un contexte supplémentaire au formulaire, tel qu’un texte décrivant le formulaire ou un lien vers des ressources associées, ce qui le rend plus informatif et convivial.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Pied de page de Forms adaptatif a été publié en février 2023 dans le cadre de la version 2.0.4 des composants principaux. Voici un tableau présentant toutes les versions prises en charge, la compatibilité AEM et les liens vers la documentation correspondante :

|  |  |
|---|---|
| Version du composant | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatible avec<br>[version 2.0.4](/help/versions.md) et plus tard | Compatible | Compatible |

Pour plus d’informations sur les versions et versions des composants principaux, reportez-vous à la section [Versions des composants principaux](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Découvrez les informations les plus récentes sur le composant principal Pied de page de Forms adaptatif dans la documentation technique de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/footer/v1/footer). Pour plus d’informations sur le développement des composants principaux, consultez la section [Documentation destinée aux développeurs sur les composants principaux](/help/developing/overview.md).


## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser votre expérience de pied de page pour les visiteurs qui utilisent la boîte de dialogue Configurer . Vous pouvez également définir facilement des options de pied de page pour une expérience utilisateur fluide.

![Onglet Propriétés](/help/adaptive-forms/assets/footer_propertiestab.png)

* **Boîte de dialogue Modifier**
La boîte de dialogue de modification fournit des outils de mise en forme de texte enrichi standard qui permettent à l’utilisateur de créer du texte pour le pied de page.

* **Gras** - Cette option applique une mise en forme gras au texte sélectionné ou au texte gras saisi après le curseur. `Ctrl+B` est un raccourci clavier.

* **Italique** - Cette option applique une mise en forme en italique au texte sélectionné ou en italique au texte saisi après le curseur. `Ctrl+I` est un raccourci clavier.

![Options de puces](/help/adaptive-forms/assets/footer_bullet.png)


* **Puce**

   * **Icône Puce** - Le texte sélectionné est alors mis en forme sous forme de liste à puces ou commence l’insertion d’une liste à puces après le curseur. Pour mettre fin à une liste à puces, appuyez ou cliquez de nouveau sur le bouton Puces ou saisissez deux retours chariot.

   * **Icône Liste numérotée** - Le texte sélectionné est alors mis en forme sous forme de liste numérotée ou commence l’insertion d’une liste numérotée après le curseur. Pour mettre fin à une liste numérotée, appuyez ou cliquez de nouveau sur le bouton Numérotée ou saisissez deux retours chariot.

   * **Icône Retrait négatif** : réduit le niveau de mise en retrait du texte ou du texte sélectionné après le curseur. Uniquement actif si le texte ou la position sélectionnés du curseur est déjà mis en retrait.

   * **Icône Retrait** - Cela augmente le niveau de mise en retrait du texte ou du texte sélectionné après le curseur.

![Options d’hyperlien](/help/adaptive-forms/assets/footer_link.png)

* **Lien hypertexte**

   * **Chemin** - Entrez le chemin
      1. Utilisation de la boîte de dialogue Ouvrir la sélection pour choisir un chemin dans AEM.
      1. Si le lien ne se trouve pas dans AEM, saisissez l’URL absolue.
      1. Les chemins non absolus sont interprétés comme relatifs par rapport aux AEM.
   * **Texte de remplacement** - Entrez un texte descriptif alternatif pour le lien.

   * **Cible** - Sélectionner le comportement du lien
      * Cible
      * Même onglet
      * Nouvel onglet
      * Cadre parent
      * Cadre supérieur
   * **Icône Dissocier** - Cette option supprime un lien déjà appliqué au texte sélectionné. Cette option n’est principale que si le lien est déjà sélectionné.

   * **Icône Format de paragraphe** - Cette option vous permet d’appliquer une mise en forme de paragraphe au texte sélectionné. Il permet également de mettre en forme le texte inséré après le curseur. Il définit le niveau d’en-tête du titre.



* **ID**: Cette option permet de contrôler l’identifiant unique du composant dans le HTML et dans la couche de données.

   * Si rien n’est indiqué, un identifiant unique est automatiquement * généré et peut être trouvé en examinant la page qui en résulte.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.


