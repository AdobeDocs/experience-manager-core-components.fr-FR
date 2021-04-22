---
title: Module ui.content de l’archétype de projet AEM
description: Module ui.content de l’archétype de projet AEM
feature: Composants principaux, archétype de projet AEM
role: Architect, Developer, Administrator
exl-id: af019cd8-c733-4b53-bb57-321dd9451178
translation-type: ht
source-git-commit: 8ff36ca143af9496f988b1ca65475497181def1d
workflow-type: ht
source-wordcount: '223'
ht-degree: 100%

---

# Module ui.content de l’archétype de projet AEM {#uicontent-module}

Le module Maven ui.content (`<src-directory>/<project>/ui.content`) comprend le contenu de ligne de base et des configurations sous `/content` et `/conf`. ui.content est compilé dans un package AEM, de manière très similaire à ui.apps. La principale différence est que les nœuds stockés dans ui.content peuvent être modifiés directement sur l’instance AEM. Cela comprend les pages, les ressources DAM et les modèles modifiables. Le module ui.content peut être utilisé pour stocker un exemple de contenu pour une instance propre ou pour créer des configurations de ligne de base à gérer dans le contrôle source.

## filter.xml {#filter}

Le fichier `filter.xml` du module ui.content se trouve sous `<src>/<project>/ui.content/src/main/content/META-INF/vault/filter.xml` et contient les chemins qui seront inclus et installés avec le package ui.content. Notez qu’un attribut `mode="merge"` est ajouté au chemin d’accès. Cela permet de s’assurer que les configurations déployées avec un déploiement de code ne remplacent pas automatiquement le contenu ou les configurations qui ont été créés directement sur l’instance AEM.

## ui.content/pom.xml

Le module ui.content, tout comme le module ui.apps, utilise le plug-in FileVault Package. Cependant, le fichier POM ui.content (`<src>/<project>/ui.content/pom.xml`) comprend une propriété de configuration supplémentaire appelée `acHandling`, définie sur `merge_preserve`. Cette propriété est incluse car le module ui.content comprend des listes de contrôle d’accès (ACL) qui sont des autorisations, qui déterminent qui peut modifier les modèles. Pour que ces listes ACL soient importées dans AEM, la propriété `acHandling` est nécessaire.
