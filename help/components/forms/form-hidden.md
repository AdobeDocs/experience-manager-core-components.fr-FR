---
title: Composant Masqué du formulaire
description: Le composant Masqué du formulaire des composants principaux permet l’affichage d’un champ masqué.
translation-type: tm+mt
source-git-commit: 95c0621f5423bfa515fe5e8b693e127ea56b4ae0

---


# Composant Masqué du formulaire{#form-hidden-component}

Le composant Masqué du formulaire des composants principaux permet l’affichage d’un champ masqué.

## Utilisation {#usage}

Le composant Masqué du formulaire des composants principaux permet la création de champs masqués pour transmettre des informations sur la page actuelle à AEM. Il est destiné à être utilisé avec le [composant de conteneur de formulaires](form-container.md).

Les propriétés de champ peuvent être définies par l’éditeur de contenu dans la [boîte de dialogue de configuration](form-hidden.md).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Masqué du formulaire est v2, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Compatible | Compatible | Compatible | Compatible |
| [v1](/help/components/v1/form-hidden-v1.md) | Compatible | Compatible | Compatible | - |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

To experience the Form Hidden Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_form_hidden).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Masqué du formulaire [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_form_hidden_v2).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de définir les paramètres du champ masqué.

![](/help/assets/chlimage_1-26.png)

* **Nom**
Nom du champ qui est envoyé avec les données de formulaire.
* **Valeur**
Valeur du champ qui est envoyée avec les données de formulaire.
* **Identifiant**
L’identifiant doit être unique sur la page et peut être utilisé pour lier les scripts à ce champ de formulaire.

Étant donné que le composant Masqué du formulaire ne comporte normalement aucun attribut visible, l’espace réservé du composant dans l’éditeur affiche les valeurs des champs **Nom** et **Valeur** si elles sont affectées pour aider l’auteur à identifier le composant Masqué du formulaire approprié.

![](/help/assets/screenshot_2018-10-19at094927.png)

## Boîte de dialogue de conception {#design-dialog}

Il n’existe pas de boîte de dialogue de conception pour le composant Masqué du formulaire.
