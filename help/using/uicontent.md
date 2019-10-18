---
title: module ui.content de l’archétype du projet AEM
seo-title: module ui.content de l’archétype du projet AEM
description: module ui.content de l’archétype du projet AEM
seo-description: module ui.content de l’archétype du projet AEM
contentOwner: bohnert
content-type: référence
topic-tags: core-components
translation-type: tm+mt
source-git-commit: 3c37b57eb72d1d662cdbd41ca54cdc592919203c

---


# module ui.content de l’archétype du projet AEM {#uicontent-module}

Le module ui.content maven (`<src-directory>/<project>/ui.content`) comprend le contenu de ligne de base et des configurations sous `/content` et `/conf`. ui.content est compilé dans un package AEM, tout comme ui.apps. La principale différence est que les noeuds stockés dans ui.content peuvent être modifiés directement sur l’instance AEM. Cela inclut les pages, les ressources DAM et les modèles modifiables. Le module ui.content peut être utilisé pour stocker un exemple de contenu pour une instance propre et/ou pour créer des configurations de base à gérer dans le contrôle de code source.

## filter.xml {#filter}

Le `filter.xml` fichier du module ui.content se trouve à `<src>/<project>/ui.content/src/main/content/META-INF/vault/filter.xml` et contient les chemins qui seront inclus et installés avec le package ui.content. Notez qu’un `mode="merge"` attribut est ajouté au chemin d’accès. Cela permet de s’assurer que les configurations déployées avec un déploiement de code ne remplacent pas automatiquement le contenu ou les configurations qui ont été créées directement sur l’instance AEM.

## ui.content/pom.xml

Le module ui.content, tout comme le module ui.apps, utilise le module FileVault Package. Cependant, le module ui.content (`<src>/<project>/ui.content/pom.xml`) comprend une propriété de configuration supplémentaire appelée `acHandling`, définie sur `merge_preserve`. Ceci est inclus car le module ui.content inclut des listes de contrôle d’accès (ACL) qui sont des autorisations, qui déterminent qui peut modifier les modèles. Pour que ces listes ACL soient importées dans AEM, la `acHandling` propriété est nécessaire.
