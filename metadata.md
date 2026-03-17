---
product: adobe experience manager
solution: Experience Manager, Experience Manager Sites
type: Documentation
description: Documentation des composants principaux Adobe Experience Manager
git-repo: https://github.com/AdobeDocs/experience-manager-core-components.en
index: true
recommendations: noDisplay
source-git-commit: 7ba1374bd64686c2e7ac44398d77fb187ff60949
workflow-type: tm+mt
source-wordcount: '120'
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
