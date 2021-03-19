---
title: Composant de texte de formulaire
description: Le composant de texte de formulaire des composants principaux permet l’entrée de texte de formulaire pour envoi.
role: Architecte, Développeur, Administrateur, Professionnel
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 99%

---


# Composant de texte de formulaire{#form-text-component}

Le composant de texte de formulaire des composants principaux permet l’entrée de texte de formulaire pour envoi.

## Utilisation {#usage}

Le composant de texte de formulaire permet l’envoi de différents types de texte et est conçu pour être utilisé avec le [composant de conteneur de formulaires](form-container.md). Le type de validation de texte, d’étiquettes et de messages d’aide peut être défini par l’éditeur de contenu dans la [boîte de dialogue de configuration](#configure-dialog).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de texte de formulaire est v2, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatible | Compatible | Compatible |
| [v1](/help/components/v1/form-text-v1.md) | Compatible | Compatible | - |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant de texte de formulaire et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_form_text).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant de texte de formulaire [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_form_text_v2).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de définir le type de texte à saisir, ainsi que les valeurs et étiquettes par défaut.

### Onglet Propriétés {#properties-tab}

![Onglet Propriétés](/help/assets/form-text-edit-properties.png)

* **Contrainte** : type de texte à saisir et par rapport auquel il sera validé.
   * **Texte**
   * **Zone de texte**
   * **Courriel**
   * **Téléphone**
   * **Date**
   * **Nombre**
   * **Mot de passe**
* **Lignes de texte** : nombre de lignes à afficher dans la zone de texte (affiché uniquement lorsque la **contrainte** est définie sur **Zone de texte**).
* **Étiquette** : libellé qui s’affiche pour le champ.
* **Masquer l’étiquette** : nécessaire si l’étiquette est requise uniquement à des fins d’accessibilité et ne transmet aucune information visuelle supplémentaire sur le champ.
* **Nom de l’élément** : nom du champ qui est envoyé avec les données de formulaire.
* **Valeur** : valeur par défaut prérenseignée dans le champ.
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

### Onglet À propos {#about-tab}

![Onglet À propos](/help/assets/form-text-edit-about.png)

* **Message d’aide** : conseil à l’intention de l’utilisateur sur ce qui peut être entré dans le champ.
* **Afficher le message d’aide comme espace réservé** : indique s’il convient d’afficher le message d’aide dans l’entrée de formulaire lorsqu’elle est vide et désactivée.

### Onglet Contraintes {#constraints-tab}

![Onglet Contraintes](/help/assets/form-text-edit-constraints.png)

* **Message de contrainte**
   * Message affiché sous forme d’info-bulle lors de l’envoi du formulaire si la valeur ne valide pas le type sélectionné
   * Non affiché pour les types de contraintes **Texte** et **Zone de texte**.
* **Requis** : indique si l’utilisateur doit renseigner une valeur avant d’envoyer le formulaire.
   * **Message obligatoire** : message affiché sous forme d’info-bulle si le champ est vide.
* **Rendre en lecture seule** : si cette option est sélectionnée, l’utilisateur ne peut pas modifier la valeur du champ.

## Boîte de dialogue de conception {#design-dialog}

### Onglet Styles {#styles-tab}

Le composant Texte de formulaire prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.
