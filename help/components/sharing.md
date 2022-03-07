---
title: 'Composant Partage sur les réseaux sociaux '
description: Le composant Partage sur les réseaux sociaux des composants principaux est un widget permettant de partager des contenus sur Facebook et Pinterest.
role: Architect, Developer, Admin, User
exl-id: 8bd53c76-da91-479b-b416-f978682a3d43
source-git-commit: 9767a3a10cb9a77f385edc0ac3fb00096c0087af
workflow-type: ht
source-wordcount: '423'
ht-degree: 100%

---

# Composant Partage sur les réseaux sociaux {#social-sharing-component}

Le composant Partage sur les réseaux sociaux des composants principaux est un widget permettant de partager des contenus sur Facebook et Pinterest.

## Utilisation {#usage}

Le composant Partage sur les réseaux sociaux ajoute des liens de partage Facebook et Pinterest à la page. Il est souvent inclus dans les en-têtes ou les pieds de page.

Contrairement à d’autres composants, les paramètres du composant Partage sur les réseaux sociaux sont définis par l’auteur du modèle par le biais [des propriétés de la page initiale](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=fr) et par l’auteur du contenu via [les propriétés de la page](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=fr).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Partage sur les réseaux sociaux est v1, qui a été introduite avec la version 1.0.0 des composants principaux. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant et les versions AEM avec lesquelles les versions du composant sont compatibles.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatible avec la <br>[version 2.17.4](/help/versions.md) et versions antérieures. | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant Partage sur les réseaux sociaux et voir des exemples d’options de configuration et de sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_sharing_fr).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant de partage [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_sharing_v1_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de modification {#edit-dialog}

![Boîte de dialogue de modification du composant Partage](/help/assets/sharing-edit.png)

* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

Étant donné que le partage nécessite des en-têtes de page spéciaux, tout partage doit être activé au niveau de la page. Par conséquent, pour l’auteur du contenu, des options de modification supplémentaires du composant Partage sont disponibles via l’onglet de partage dans les [propriétés de la page](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=fr).

## Boîte de dialogue de conception {#design-dialog}

Étant donné que le partage nécessite des en-têtes de page spéciaux, tout partage doit être activé au niveau de la page. Par conséquent, pour l’auteur du modèle, les options de conception du composant Partage sont disponibles via les [propriétés de la page initiale](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=fr).
