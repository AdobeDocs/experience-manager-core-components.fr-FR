---
product: Adobe Experience Manager
git-repo: https://github.com/AdobeDocs/experience-manager-core-components.fr
index: y
solution-title: Formation et support pour AEM
solution-hub-url: https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/home.html
getting-started-title: Prise en main du développement pour AEM
getting-started-url: https://docs.adobe.com/content/help/en/experience-manager-cloud-service/core-concepts/home.html
tutorials-title: Tutoriels AEM
tutorials-url: https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/overview.html
translation-type: tm+mt
source-git-commit: a3085d266baf32649fda528a7f4703e133d03ab7

---


# Métadonnées pour utilisation interne

Les métadonnées dans le système de création GitHub sont hiérarchisées et sont définies comme les niveaux de précédents croissants suivants.

1. metadata.md
1. ToC
1. Article

Les métadonnées définies dans le fichier metadata.md s’appliquent à l’intégralité du référentiel, mais peuvent être remplacées aux niveaux de la table des matières et de l’article. Tout remplacement des métadonnées doit être effectué au niveau le plus bas possible.

Les métadonnées dans le référentiel experience-manager-core-components.en sont le minimum requis.

metadata.md

* `product`
* `git-repo`
* `index: y`
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
* `index: n` (uniquement pour les versions précédentes des composants)

Vous trouverez des informations supplémentaires sur les métadonnées dans le guide de création [interne.](https://docs.adobe.com/help/en/collaborative-doc-instructions/collaboration-guide/markdown/metadata.html#solution-metadata)
