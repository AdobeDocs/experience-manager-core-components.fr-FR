---
title: Module ui.apps de l’archétype de projet AEM
seo-title: Module ui.apps de l’archétype de projet AEM
description: Module ui.apps de l’archétype de projet AEM
seo-description: Module ui.apps de l’archétype de projet AEM
contentOwner: bohnert
content-type: référence
topic-tags: core-components
translation-type: tm+mt
source-git-commit: 3c37b57eb72d1d662cdbd41ca54cdc592919203c

---


# Module ui.apps de l’archétype de projet AEM {#uiapps-module}

Le module expert ui.apps (`<src-directory>/<project>/ui.apps`) comprend tout le code de rendu nécessaire pour le site situé sous `/apps`. Cela inclut CSS/JS qui sera stocké dans un format AEM appelé clientlibs. Cela inclut également les scripts HTML pour le rendu du code HTML dynamique. Vous pouvez considérer le module ui.apps comme une carte de la structure dans le JCR, mais dans un format qui peut être stocké sur un système de fichiers et engagé dans le contrôle de code source.

Le module Apache Jackrabbit FileVault Package est utilisé pour compiler le contenu du module ui.apps dans un package AEM qui peut être déployé dans AEM. Les configurations globales du module externe sont définies dans le fichier pom.xml parent.

## POM parent {#parent-pom}

[Le POM](archetype.md#parent-pom) parent (`<src>/<project>/pom.xml`) comprend `<plugin>` des sections qui définissent différentes configurations pour les modules externes utilisés dans le projet. Ceci inclut une configuration pour le `filterSource` module externe Jackrabbit FileVault Package. Il `filterSource` pointe vers l’emplacement du `filter.xml` fichier utilisé pour définir les chemins d’accès jcr inclus dans le package.

Outre le module Jackrabbit FileVault Package Plugin est une définition du module Content Package Plugin qui est utilisé pour envoyer le module dans AEM. Notez que les variables pour `aem.host`, `aem.port`, `vault.user`et `vault.password` sont utilisées qui correspondent aux propriétés globales définies dans le même POM parent.

## ui.apps/pom.xml {#uiapps-pom}

Le pom ui.apps (`<src>/<project>/ui.apps/pom.xml`) fournit les `embedded` balises pour le `filevault-package-maven-plugin`. Les `embedded` balises incluent le lot de base compilé dans le package ui.apps et son emplacement d’installation.

Notez que les packages core.wcm.components.all et core.wcm.components.example sont inclus en tant que sous-package. Le pack des composants principaux est ainsi déployé chaque fois avec le code WKND.

Les exemples core.wcm.components.all et core.wcm.components.example sont inclus en tant que dépendances dans la liste des dépendances. Toutefois, il est recommandé d’omettre les versions des dépendances ici et de les gérer dans le fichier [pom](archetype.md#core-components)parent.

## filter.xml {#filter}

Le `filter.xml` fichier du module ui.apps se trouve à l’adresse `<src>/<project>/ui.apps/src/main/content/META-INF/vault/filter.xml` et contient les chemins d’accès qui seront inclus et installés avec le package ui.apps.
