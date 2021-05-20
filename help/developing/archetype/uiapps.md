---
title: Module ui.apps de l’archétype de projet AEM
description: Module ui.apps de l’archétype de projet AEM
feature: Composants principaux, archétype de projet AEM
role: Architect, Developer, Administrator
exl-id: fc63a19a-3253-44ee-96e2-bb5544c2235b
source-git-commit: 8ff36ca143af9496f988b1ca65475497181def1d
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 100%

---

# Module ui.apps de l’archétype de projet AEM {#uiapps-module}

Le module Maven ui.apps (`<src-directory>/<project>/ui.apps`) comprend tout le code de rendu nécessaire pour le site situé sous `/apps`. Ce module comprend les éléments CSS/JS qui seront stockés dans un format AEM appelé [clientlibs.](uifrontend.md#clientlibs) Cela inclut également les scripts HTL pour le rendu du code HTML dynamique. Vous pouvez vous représenter le module ui.apps sous la forme d’une carte de la structure dans le JCR, mais dans un format pouvant être stocké sur un système de fichiers et validé dans le contrôle source.

Le plug-in Apache Jackrabbit FileVault Package est utilisé pour compiler le contenu du module ui.apps dans un package AEM pouvant être déployé vers AEM. Les configurations globales du plug-in sont définies dans le fichier pom.xml parent.

## Fichier POM parent {#parent-pom}

[Le fichier POM parent](/help/developing/archetype/using.md#parent-pom) (`<src>/<project>/pom.xml`) comprend des sections `<plugin>` qui définissent différentes configurations pour les plug-ins utilisés dans le projet. Il comprend la configuration pour le `filterSource` du plug-in Jackrabbit FileVault Package. Le `filterSource` pointe vers l’emplacement du fichier `filter.xml` utilisé pour définir les chemins d’accès jcr inclus dans le package.

Outre le plug-in Jackrabbit FileVault Package, il existe une définition du plug-in Content Package utilisée pour envoyer le package dans AEM. Notez que les variables de `aem.host`, `aem.port`, `vault.user` et `vault.password` qui sont utilisées correspondent aux propriétés globales définies dans le même fichier POM parent.

## ui.apps/pom.xml {#uiapps-pom}

Le fichier POM ui.apps (`<src>/<project>/ui.apps/pom.xml`) fournit les balises `embedded` pour le `filevault-package-maven-plugin`. Les balises `embedded` incluent le lot principal compilé comme partie intégrante du package ui.apps et son emplacement d’installation.

Notez que les packages core.wcm.components.all et core.wcm.components.examples sont inclus en tant que sous-package. Celui-ci déploie à chaque fois le package de composants principaux avec le code WKND.

Les packages core.wcm.components.all et core.wcm.components.examples sont inclus en tant que dépendances dans la liste des dépendances. Toutefois, les bonnes pratiques demandent que les versions des dépendances soient ici ignorées et gérées dans le [fichier POM parent](/help/developing/archetype/using.md#core-components).

## filter.xml {#filter}

Le fichier `filter.xml` du module ui.apps se trouve à l’adresse `<src>/<project>/ui.apps/src/main/content/META-INF/vault/filter.xml` et contient les chemins d’accès qui sont inclus et installés avec le package ui.apps.
