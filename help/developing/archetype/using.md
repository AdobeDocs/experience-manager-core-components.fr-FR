---
title: Utilisation de l’archétype de projet AEM
description: Découvrez comment utiliser l’ archétype de projet AEM pour créer un projet Adobe Experience Manager minimal basé sur les bonnes pratiques comme point de départ de vos propres projets AEM.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: a3978d8b-4904-42aa-9ee2-9c1f884327bb
source-git-commit: bd92a5d1884056ca7b44ea28e5817d8bde10a4d9
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 33%

---


# Utilisation de l’archétype de projet AEM {#using-the-archetype}

Ce document explique comment utiliser l’ archétype de projet AEM pour créer un projet Adobe Experience Manager minimal basé sur les bonnes pratiques comme point de départ de vos propres projets AEM.

Il se concentre sur les schémas d’utilisation généraux et sur ce que l’archétype fait pour vous. Pour obtenir des instructions techniques et des options de génération détaillées, consultez la documentation du référentiel GitHub de l’archétype.

>[!TIP]
>
>Dernier AEM archétype de projet et documentation technique associée [est disponible sur GitHub.](https://github.com/adobe/aem-project-archetype)

## Prise en main {#getting-started}

L’archétype de projet permet de commencer facilement à développer dans AEM. Vous pouvez réaliser vos premiers pas avec l’archétype de plusieurs façons.

* **Tutoriel WKND** - Pour une excellente introduction au développement sur AEM, y compris sur la manière d’exploiter l’archétype, voir la section [Prise en main d’AEM Sites - Tutoriel WKND](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=fr) pour un exemple pratique qui vous guide tout au long de l’utilisation de l’archétype pour mettre en oeuvre un projet simple.
* **Tutoriel sur WKND Events** - Si vous êtes particulièrement intéressé par le développement d’applications d’une seule page (SPA) sur AEM, veillez à consulter dédié. [Tutoriel sur WKND Events.](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=fr)
* **Commence par toi-même !** - Vous pouvez facilement télécharger le fichier [archétype de projet actuel disponible sur GitHub](https://github.com/adobe/aem-project-archetype) et créez votre premier projet par vous-même.

## Utilisation de l’archétype {#how-to-use-the-archetype}

La première étape à l’aide de l’archétype consiste à créer un projet qui génère [les modules ;](#what-you-get) dans une structure de fichiers locale. Dans le cadre de la génération du projet, plusieurs propriétés de votre projet peuvent être définies, telles que le nom, la version, l’activation de diverses options, etc.

>[!TIP]
>
>Chaque fois que vous créez l’archétype, il génère également une série de lisibles, vous fournissant les détails techniques et l’utilisation de chaque module en tant que [lien ci-dessous.](#what-you-get)

La création du projet avec Maven crée les artefacts (packages et lots OSGi) qui peuvent être déployés vers AEM. Des commandes et des profils Maven supplémentaires peuvent être utilisés pour déployer les artefacts du projet vers une instance AEM.

## Avantages de l’utilisation de l’archétype {#what-you-get}

L’archétype est constitué de modules qui sont tous créés automatiquement lors de l’utilisation de l’archétype.

* **[core](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/core)** est un lot Java contenant toutes les fonctionnalités de base telles que les services OSGi, les écouteurs et les planificateurs, ainsi que le code Java associé aux composants tels que les servlets et les filtres de requête.
* **[it.tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/it.tests)** sont des tests d’intégration Java.
* **[ui.apps](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.apps)** contient la variable `/apps` et `/etc` des parties du projet, c’est-à-dire des bibliothèques clientes JS et CSS, des composants et des modèles.
* **[ui.content](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.content)** contient des exemples de contenu utilisant les composants du module ui.apps.
* **[ui.config](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.config)** contient des configurations OSGi spécifiques au mode d’exécution pour le projet.
* **[ui.frontend.general](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.general)** contient les artefacts requis pour utiliser le module de génération front-end général basé sur Webpack (facultatif).
* **[ui.frontend.response](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.react)** **(facultatif)** contient les artefacts requis lors de l’utilisation de l’archétype pour créer SPA projets basés sur React (facultatif, dépend des paramètres de génération).
* **[ui.frontend.angular](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.angular)** **(facultatif)** contient les artefacts requis lors de l’utilisation de l’archétype pour créer SPA projets basés sur l’Angular (facultatif, dépend des paramètres de génération).
* **[ui.tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.tests)** contient des tests d’IU basés sur Selenium.
* **[all](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/all)** est un module de contenu unique qui incorpore tous les modules compilés (bundles et packages de contenu), y compris toutes les dépendances des fournisseurs.
* **[dispatcher.ams](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/dispatcher.ams)** contient les configurations de Dispatcher de base pour les projets AMS/On-prem (facultatif, dépend des paramètres de génération).
* **[dispatcher.cloud](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/dispatcher.cloud)** contient les configurations de Dispatcher de base pour les projets AEMaaCS (facultatif, dépend des paramètres de génération).

![Organisation du package de contenu](/help/assets/content-package-organization.png)

Les modules de l’archétype représentés dans Maven sont déployés vers AEM en tant que packages de contenu représentant l’application, le contenu et les lots OSGi nécessaires.

## Fichier POM parent {#parent-pom}

Le fichier `pom.xml` racine du projet (`<src-directory>/<project>/pom.xml`) est connu sous le nom de fichier POM parent et oriente la structure du projet et gère les dépendances ainsi que certaines propriétés globales du projet.

### Propriétés globales du projet {#global-properties}

La section `<properties>` du fichier POM parent définit plusieurs propriétés globales importantes pour le déploiement de votre projet vers une instance AEM, telles que le nom d’utilisateur/mot de passe, le nom d’hôte/port, etc.

Ces propriétés sont configurées pour être déployées vers une instance AEM locale, car il s’agit du scénario de création le plus courant pour les développeurs. Notez qu’il existe des propriétés à déployer vers une instance de création et une instance de publication. Il s’agit également de l’endroit où les informations d’identification sont définies pour s’authentifier auprès de l’instance AEM. Par défaut `admin:admin` les informations d’identification sont utilisées.

Ces propriétés sont configurées de manière à pouvoir être remplacées lors d’un déploiement vers des environnements de niveau supérieur. De cette manière, les fichiers POM n’ont pas à changer, mais des variables comme `aem.host` et `sling.password` peuvent être remplacées via des arguments de ligne de commande :

```shell
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
```

### Structure du module {#module-structure}

La section `<modules>` du fichier POM parent définit les modules que le projet va créer. Par défaut, les versions du projet [les modules standard précédemment définis.](#what-you-get) D’autres modules peuvent toujours être ajoutés à mesure qu’un projet évolue.

### Dépendances {#dependencies}

La section `<dependencyManagement>` du fichier POM parent définit toutes les dépendances et versions des API utilisées dans le projet. Les versions doivent être gérées dans le fichier POM parent. Les sous-modules ne doivent inclure aucune information de version.

#### Uber Jar {#uber-jar}

L’une des dépendances clés est la [AEM Java API Jar.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html?lang=fr) Cela inclut toutes les API AEM avec une seule entrée de dépendance pour la version d’AEM.

>[!NOTE]
>
>Il est recommandé de mettre à jour la version d’Uber Jar pour qu’elle corresponde à la version cible d’AEM. Par exemple, si vous prévoyez de déployer vers AEM 6.5, vous devez mettre à jour la version d’uber-jar vers la version 6.5.X, où `X` est le dernier Service Pack.

#### Composants principaux {#core-components}

L’archétype tire bien sûr parti de la méthode [Composants principaux.](/help/introduction.md) Par conséquent, pour tirer parti des composants principaux dans tous les déploiements, il est recommandé de les inclure dans le projet Maven.

Le fichier core.wcm.components.example est un ensemble d’exemples de pages qui illustrent des exemples de composants principaux. Les bonnes pratiques recommandent que, lors du déploiement d’un projet destiné à la production, vous supprimiez cette dépendance et cette inclusion de sous-package.

>[!NOTE]
>
>Les composants principaux et l’archétype sont conservés en tant que projets GitHub distincts et leurs versions diffèrent donc.
>
>Chaque version de l’archétype utilisera la dernière version des composants principaux disponibles au moment de la publication. Cependant, vous pouvez mettre à jour manuellement la dépendance sur les composants principaux.

## Tests {#testing}

Il existe trois niveaux de tests contenus dans le projet et, parce qu’il s’agit de différents types de tests, ils sont exécutés de différentes manières ou à différents endroits.

* **[Test unitaire](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/core)** - Test unitaire classique du code contenu dans le lot
* **[Tests d’intégration](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/it.tests)** - Tests d’intégration côté serveur qui exécutent des tests de type unitaire dans l’environnement AEM, c’est-à-dire sur le serveur AEM
* **[Tests de l’interface utilisateur](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.tests)** - Tests Selenium côté navigateur qui vérifient le comportement côté navigateur
