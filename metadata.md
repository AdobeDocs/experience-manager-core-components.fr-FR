---
product: adobe experience manager
solution: Experience Manager, Experience Manager Sites
type: Documentation
description: Documentation relative aux composants principaux Adobe Experience Manager
git-repo: https://git.corp.adobe.com/AdobeDocs/experience-manager-core-components.fr-FR
index: y
source-git-commit: 3897e37ed1e24c4a045b7f6cc716b5cabdd7cf9f
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 100%

---


# Métadonnées pour utilisation interne

Les métadonnées figurant dans le système de création GitHub sont hiérarchisées et définies selon les niveaux de précédents croissants suivants.

1. metadata.md
1. Table des matières
1. Article

Les métadonnées définies dans le fichier metadata.md s’appliquent à l’intégralité du référentiel, mais peuvent être remplacées aux niveaux de la table des matières et de l’article. Tout remplacement des métadonnées doit être effectué au niveau le plus bas possible.

Les métadonnées figurant dans le référentiel experience-manager-core-components.en sont le minimum requis.

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

Tables des matières

* `sub-product`
* `user-guide-title`

Article

* `title`
* `description`
* `index: n` (uniquement pour les versions précédentes des composants)

Vous trouverez des informations supplémentaires sur les métadonnées dans le [guide de création interne.](https://docs.adobe.com/help/fr-FR/collaborative-doc-instructions/collaboration-guide/markdown/metadata.html#solution-metadata)
