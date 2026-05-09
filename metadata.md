---
product: adobe experience manager
solution: Experience Manager, Experience Manager Sites
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
landing-page-name: experience-manager
landing-page-breadcrumb-title: AEM
type: Documentation
description: Documentation des composants principaux Adobe Experience Manager
git-repo: https://github.com/AdobeDocs/experience-manager-core-components.fr-FR
index: true
recommendations: noDisplay
source-git-commit: 1525c048c6ab66e6b483e1110ea3dbfd926378be
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 1%

---


# Métadonnées à usage interne

Dans le système de création GitHub, les métadonnées sont hiérarchiques et définies selon les niveaux de précédent croissants suivants.

1. metadata.md
1. ToC
1. Article

Les métadonnées définies dans le fichier metadata.md s’appliquent à l’ensemble du référentiel, mais elles peuvent être remplacées au niveau de la table des matières et de l’article. Tout remplacement des métadonnées doit être effectué au niveau le plus bas possible.

Les métadonnées du référentiel experience-manager-core-components.en sont le minimum requis.

metadata.md

* `product`
* `git-repo`
* `index: true`
* `solution-title`
* `solution-hub-url`
* `getting-started-title`
* `getting-started-url`
* `tutorials-title`
* `tutorials-url`

ToCs

* `sub-product`
* `user-guide-title`

Article

* `title`
* `description`
* `index: false` (uniquement pour les versions précédentes des composants)

Vous trouverez des informations supplémentaires sur les métadonnées dans le [guide de création interne](https://experienceleague.adobe.com/docs/authoring-guide-exl/using/authoring/features/metadata.html#solution).
