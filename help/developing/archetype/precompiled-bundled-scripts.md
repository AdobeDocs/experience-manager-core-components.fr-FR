---
title: Scripts groupés précompilés
description: Découvrez comment déployer vos scripts de composant à l’aide de lots OSGi vers Adobe Experience Manager Cloud Service.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 3edc388f-01b2-45cc-bd56-f22e5a5a8624
source-git-commit: 554be9539428cd75462a38fc45f1bece04baf066
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 53%

---


# Scripts groupés précompilés {#precompiled-bundled-scripts}

AEM as a Cloud Service prend en charge le déploiement des scripts de composant [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=fr#code-packages-%2F-osgi-bundles) en tant que scripts groupés précompilés. Cela permet aux développeurs de précompiler leurs scripts au moment de la création et de les compresser en tant que lots OSGi.

## Avantages du déploiement de scripts précompilés via des lots OSGi {#advantages}

Le déploiement de vos scripts en tant que scripts groupés précompilés présente les avantages suivants :

+ La compilation de scripts au moment de la création permet aux développeurs de détecter des erreurs tôt dans le processus de développement.
+ Les dépendances des scripts d’API Java sont explicitement définies via la variable `Import-Package` et `Export-Package` en-têtes de lot.
+ Héritage (via `sling:resourceSuperType`) et la délégation à d’autres types de ressources (via HTL `data-sly-resource` élément block ou via `sling:include` La balise JSP, par exemple) peut être mappée via les métadonnées du lot.
+ Le contrôle de version du type de ressource peut être appliqué de la même manière que les API Java.

## Précompilation et importation de modules {#precompilation}

[`htl-maven-plugin`](https://sling.apache.org/components/htl-maven-plugin/index.html) peut valider la syntaxe des scripts HTL, mais il peut également être utilisé pour transférer les scripts HTL dans des classes Java. Ils sont ensuite ajoutés au dossier `generated-sources` de votre projet Maven et récupérés par le `maven-compiler-plugin`.

Vous pouvez ajouter [`bnd-maven-plugin`](https://github.com/bndtools/bnd/tree/master/maven/bnd-maven-plugin) afin de générer les métadonnées du lot OSGi pour les importations d’API Java.

## Héritage et délégation {#inheritance-delegation}

La structure OSGi offre un moyen puissant de définir [exigences et fonctionnalités](https://docs.osgi.org/specification/osgi.core/7.0.0/framework.module.html#framework.module.dependencies) pour exprimer des contrats entre différents composants. Elles sont décrites au moyen de métadonnées et appliquées au moment de l’exécution. Les scripts groupés utilisent ce mécanisme pour exprimer à la fois leurs relations d’héritage (`sling:resourceSuperType`), ainsi que la délégation (y compris d’autres types de ressources dans le processus de rendu).

La variable `bnd` du module externe [scriptingbundle-maven-plugin](https://sling.apache.org/components/scriptingbundle-maven-plugin/bnd.html) Vous pouvez utiliser ce projet pour extraire les exigences et fonctionnalités correspondant aux scripts fournis par le [`ui.apps`.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=fr#code-packages-%2F-osgi-bundles) package de contenu

## Prise en charge de l’archétype de projet AEM {#support}

À partir de la version 31, la variable [AEM Archétype de projet](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html?lang=fr) peut être utilisé pour configurer correctement un projet as a Cloud Service AEM afin d’utiliser des scripts groupés précompilés.

En outre, l’archétype de projet AEM configure le [plug-in Maven Build Analyzer du SDK as a Cloud Service](/help/developing/archetype/build-analyzer-maven-plugin.md) pour valider les dépendances au niveau du package Java et du script.
