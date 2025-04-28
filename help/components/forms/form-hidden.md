---
title: Composant Formulaire masqué
description: Le composant Formulaire masqué des composants principaux permet l’affichage d’un champ masqué.
role: Architect, Developer, Admin, User
exl-id: 0364cd3b-3c09-46db-9392-a67e3f9ea7a5
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: ht
source-wordcount: '429'
ht-degree: 100%

---

# Composant Formulaire masqué {#form-hidden-component}

Le composant Formulaire masqué des composants principaux permet l’affichage d’un champ masqué.

## Utilisation {#usage}

Le composant Formulaire masqué des composants principaux permet la création de champs masqués pour transmettre des informations sur la page actuelle à AEM. Il est destiné à être utilisé avec le [composant de conteneur de formulaires](form-container.md).

Les propriétés de champ peuvent être définies par l’éditeur de contenu dans la [boîte de dialogue de configuration](form-hidden.md).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Formulaire masqué est v2, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v2 | Compatible avec la <br>[version 2.17.4](/help/versions.md) et versions antérieures. | Compatible | Compatible | Compatible |
| [v1](/help/components/v1/form-hidden-v1.md) | Compatible | Compatible | - | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant Formulaire masqué et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_form_hidden_fr).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Formulaire masqué [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_form_hidden_v2_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de définir les paramètres du champ masqué.

![Boîte de dialogue de modification de formulaire maqué](/help/assets/form-hidden-edit.png)

* **Nom** : nom du champ qui est envoyé avec les données de formulaire.
* **Valeur** : valeur du champ qui est envoyée avec les données de formulaire.
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

Étant donné que le composant Formulaire masqué ne comporte normalement aucun attribut visible, l’espace réservé du composant dans l’éditeur affiche les valeurs des champs **Nom** et **Valeur** si elles sont affectées pour aider l’auteur à identifier le composant Formulaire masqué approprié.

![Exemple de composant Formulaire masqué](/help/assets/form-hidden-example.png)

## Boîte de dialogue de conception {#design-dialog}

### Onglet Styles {#styles-tab}

Le composant Formulaire masqué prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.
