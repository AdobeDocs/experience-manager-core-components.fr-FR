---
title: Scripts groupés précompilés
description: Découvrez comment déployer vos scripts de composant via des lots OSGi vers Adobe Experience Manager Cloud Service.
source-git-commit: 56464decc8d6ae3cef68d62bfe459bceda0539ef
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---

# Scripts groupés précompilés

AEM as a Cloud Service prend en charge le déploiement des scripts de composant [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#code-packages-%2F-osgi-bundles) en tant que scripts groupés précompilés. Cela permet aux développeurs de précompiler leurs scripts au moment de la création et de les compresser en tant que lots OSGi.

## Avantages du déploiement de scripts précompilés via des lots OSGi

Le déploiement de vos scripts en tant que scripts groupés précompilés présente les avantages suivants :

+ la compilation de scripts au moment de la création permet aux développeurs de découvrir des erreurs tôt dans le processus de développement.
+ Les dépendances de script API Java sont explicitement définies via les en-têtes de bundle `Import-Package` et `Export-Package`
+ L’héritage (via `sling:resourceSuperType`) et la délégation à d’autres types de ressources (via l’élément de bloc `data-sly-resource` de HTL ou via la balise `sling:include` JSP, par exemple) peuvent être mappés via les métadonnées du lot.
+ le contrôle de version du type de ressource peut être appliqué de la même manière que les API Java.

## Précompilation et imports de package

[`htl-maven-plugin`](https://sling.apache.org/components/htl-maven-plugin/index.html) peut valider la syntaxe des scripts HTL, mais il peut également être utilisé pour transférer les scripts HTL dans des classes Java. Ils sont ensuite ajoutés au dossier `generated-sources` de votre projet Maven et récupérés par le `maven-compiler-plugin`.

Vous pouvez ajouter [`bnd-maven-plugin`](https://github.com/bndtools/bnd/tree/master/maven/bnd-maven-plugin) pour générer les métadonnées du lot OSGi pour les importations d’API Java.

## Héritage et délégation

La structure OSGi offre un moyen puissant de définir les [exigences et fonctionnalités](https://docs.osgi.org/specification/osgi.core/7.0.0/framework.module.html#framework.module.dependencies) pour exprimer les contrats entre les différents composants. Elles sont décrites au moyen de métadonnées et appliquées au moment de l’exécution. Les scripts groupés utilisent ce mécanisme pour exprimer à la fois leurs relations d’héritage (`sling:resourceSuperType`), ainsi que la délégation (y compris d’autres types de ressources dans le processus de rendu).

Le module `bnd` du projet [scriptingbundle-maven-plugin](https://sling.apache.org/components/scriptingbundle-maven-plugin/bnd.html) peut être utilisé pour extraire les exigences et fonctionnalités correspondant aux scripts fournis par le module de contenu [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#code-packages-%2F-osgi-bundles).

## Prise en charge AEM’archétype de projet

À partir de la version 31, l’[archétype de projet AEM](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html) peut être utilisé pour configurer correctement un AEM en tant que projet de Cloud Service afin d’utiliser des scripts groupés précompilés. En outre, l’archétype de projet AEM configure l’[AEM en tant que module externe Maven Build Analyzer du SDK Cloud Service](/help/developing/archetype/build-analyzer-maven-plugin.md) pour valider les dépendances au niveau du package Java ainsi que les dépendances au niveau du script.
