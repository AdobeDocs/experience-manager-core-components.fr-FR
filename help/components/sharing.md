---
title: Composant Partage sur les réseaux sociaux
description: Le composant Partage sur les réseaux sociaux des composants principaux est un widget permettant de partager des contenus sur Facebook et Pinterest.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 77%

---


# Composant Partage sur les réseaux sociaux{#social-sharing-component}

Le composant Partage sur les réseaux sociaux des composants principaux est un widget permettant de partager des contenus sur Facebook et Pinterest.

## Utilisation {#usage}

Le composant Partage sur les réseaux sociaux ajoute des liens de partage Facebook et Pinterest à la page. Il est souvent inclus dans les en-têtes ou les pieds de page.

Contrairement à d’autres composants, les paramètres du composant Partage sur les réseaux sociaux sont définis par l’auteur du modèle par le biais [des propriétés de la page initiale](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) et par l’auteur du contenu via [les propriétés de la page](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Partage sur les réseaux sociaux est v1, qui a été introduite avec la version 1.0.0 des composants principaux avec AEM 6.3. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant et les versions AEM avec lesquelles les versions du composant sont compatibles.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant Partage sur les réseaux sociaux et voir des exemples d&#39;options de configuration et de sorties HTML et JSON, consultez [la bibliothèque de composants](https://adobe.com/go/aem_cmp_library_sharing).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant de partage [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_sharing_v1).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de modification{#edit-dialog}

![Boîte de dialogue de modification du composant Partage](/help/assets/sharing-edit.png)

* **ID** : cette option permet de contrôler l&#39;identifiant unique du composant dans le code HTML et dans la couche [de](/help/developing/data-layer/overview.md)données.
   * Si rien n’est indiqué, un identifiant unique est automatiquement généré et peut être trouvé en examinant la page qui en résulte.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

Étant donné que le partage nécessite des en-têtes de page spéciaux, tout partage doit être activé au niveau de la page. Therefore, for the content author additional edit options for the sharing component are available through the sharing tab the [page properties](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html).

## Boîte de dialogue de conception {#design-dialog}

Étant donné que le partage nécessite des en-têtes de page spéciaux, tout partage doit être activé au niveau de la page. Par conséquent, pour l’auteur du modèle, les options de conception du composant Partage sont disponibles via les [propriétés de la page initiale](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).
