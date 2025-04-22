---
title: Composant du séparateur
description: Le composant du séparateur crée un saut entre les composants d’une page.
role: Architect, Developer, Admin, User
exl-id: 79f19368-67fa-4864-93f7-2aa801d13fdb
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 99%

---

# Composant du séparateur {#separator-component}

Le composant du séparateur des composants principaux affiche une règle horizontale pour la séparation de contenu.

## Utilisation {#usage}

Le composant du séparateur permet à l’auteur de contenu de créer facilement une règle horizontale comme saut entre le contenu afin de mieux organiser les informations sur une page.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant du séparateur est v1, qui a été introduite avec la version 2.3.0 des composants principaux en février 2019. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| v1 | Compatible avec la <br>[version 2.17.4](/help/versions.md) et versions antérieures | Compatible | Compatible | Compatible |

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant du séparateur et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_separator_fr).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant du séparateur [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_separator_v1_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

![Boîte de dialogue de modification du composant Séparateur](/help/assets/separator-edit.png)

* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les styles appliqués au composant Séparateur.

### Onglet Styles {#styles-tab}

Le composant du séparateur prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.
