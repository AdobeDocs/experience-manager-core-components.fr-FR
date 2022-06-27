---
title: Composant de bouton de formulaire
description: Le composant Formulaire masqué des composants principaux permet l’inclusion d’un champ masqué dans un formulaire.
role: Architect, Developer, Admin, User
exl-id: 1e5cff43-57db-4bfc-b2d2-23307eaf5eb3
source-git-commit: 16930ccaa281f9d9c4ddbb890d4222e128557580
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 100%

---

# Composant de bouton de formulaire {#form-button-component}

Le composant de bouton de formulaire des composants principaux permet l’inclusion d’un bouton pour déclencher une action sur une page.

## Utilisation {#usage}

Le composant de bouton de formulaire des composants principaux permet la création de champs de bouton, souvent pour déclencher l’envoi du formulaire et est destiné à être utilisé avec le [composant de conteneur de formulaires](form-container.md).

Les propriétés de bouton peuvent être définies par l’éditeur de contenu dans la [boîte de dialogue de configuration](#configure-dialog).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de bouton de formulaire est v2, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatible avec la <br>[version 2.17.4](/help/versions.md) et versions antérieures. | Compatible | Compatible |
| [v1](/help/components/v1/form-button-v1.md) | Compatible | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant de bouton de formulaire et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_form_button_fr).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant de bouton de formulaire [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_form_button_v2_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de définir les paramètres du bouton.

### Onglet Propriétés {#properties-tab}

![Boîte de dialogue de modification du composant Bouton de formulaire](/help/assets/form-button-edit.png)

* **Type**

   * **Bouton**
   * **Envoyer**

* **Titre** : texte affiché sur le bouton.

   * Si aucun titre n’est défini, le type de bouton est utilisé par défaut.

* **Nom** : nom du bouton qui est envoyé avec les données de formulaire.
* **Valeur** : valeur du bouton qui est envoyée avec les données de formulaire.

* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

## Boîte de dialogue de conception {#design-dialog}

### Onglet Styles {#styles-tab}

Le composant de bouton de formulaire prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.
