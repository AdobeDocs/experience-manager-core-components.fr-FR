---
title: Composant Formulaire masqué
description: Le composant Formulaire masqué des composants principaux permet l’affichage d’un champ masqué.
role: Developer, Admin, User
exl-id: 0364cd3b-3c09-46db-9392-a67e3f9ea7a5
TQID: https://experienceleague.adobe.com/4A6TDfa-zTap73hcgFA-fbjbKqd3dF11Zgs-eEypE0Y
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 432
ht-degree: 100%

---

# Composant Formulaire masqué{#form-hidden-component}

Le composant Formulaire masqué des composants principaux permet l’affichage d’un champ masqué.

## Utilisation {#usage}

Le composant Formulaire masqué des composants principaux permet la création de champs masqués pour transmettre des informations sur la page actuelle à AEM. Il est destiné à être utilisé avec le [composant de conteneur de formulaires](form-container.md).

Les propriétés de champ peuvent être définies par l’éditeur de contenu dans la [boîte de dialogue de configuration](form-hidden.md).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Masqué du formulaire est v2, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v2 | Compatible avec la <br>[version 2.17.4](/help/versions.md) et versions antérieures | Compatible | Compatible | Compatible |
| [v1](/help/components/v1/form-hidden-v1.md) | Compatible | Compatible | - | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant Formulaire masqué et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_form_hidden_fr).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Formulaire masqué [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_form_hidden_v2_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation relative au développement des composants principaux](/help/developing/overview.md).

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
