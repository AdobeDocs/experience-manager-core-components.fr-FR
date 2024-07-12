---
title: Utilisation de l’archétype de projet AEM
description: Découvrez comment l’archétype de projet AEM crée un projet Adobe Experience Manager minimal qui s’appuie sur des bonnes pratiques pour que vous puissiez démarrer vos propres projets AEM sur des bases saines.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: a3978d8b-4904-42aa-9ee2-9c1f884327bb
source-git-commit: bd92a5d1884056ca7b44ea28e5817d8bde10a4d9
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 100%

---


# Utilisation de l’archétype de projet AEM {#using-the-archetype}

Ce document explique comment vous pouvez utiliser l’archétype de projet AEM pour créer un projet Adobe Experience Manager minimal qui s’appuie sur des bonnes pratiques pour que vous puissiez démarrer vos propres projets AEM sur des bases saines.

Il se concentre sur les schémas d’utilisation généraux et sur ce que l’archétype fait pour vous. Pour obtenir des instructions techniques et des options de génération détaillées, consultez la documentation du référentiel GitHub de l’archétype.

>[!TIP]
>
>Le dernier archétype de projet AEM, ainsi que la documentation technique complète, [sont disponibles sur GitHub](https://github.com/adobe/aem-project-archetype).

## Prise en main {#getting-started}

L’archétype de projet permet de commencer facilement à développer dans AEM. Vous pouvez commencer à travailler avec l’archétype de plusieurs manières.

* **Tutoriel WKND** : pour une excellente introduction au développement dans AEM, notamment des informations sur l’utilisation de l’archétype, reportez-vous à [Prise en main d’AEM Sites - Tutoriel WKND](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=fr) afin d’obtenir un exemple pratique vous guidant tout au long de l’utilisation de l’archétype pour mettre en œuvre un projet simple.
* **Tutoriel sur WKND Events** : si le développement d’applications d’une seule page (SPA) dans AEM vous intéresse particulièrement, consultez notre [tutoriel WKND Events](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=fr) dédié.
* **C’est à vous de jouer !** : vous pouvez facilement télécharger l’archétype de [projet actuel disponible sur GitHub](https://github.com/adobe/aem-project-archetype) et créer votre premier projet en suivant les étapes simples ci-dessous.

## Utilisation de l’archétype {#how-to-use-the-archetype}

La première étape d’utilisation de l’archétype consiste à créer un projet qui génère [les modules](#what-you-get) dans une structure de fichiers locale. Dans le cadre de la génération du projet, plusieurs propriétés de votre projet peuvent être définies, telles que le nom du projet, la version, l’activation de certaines options, etc.

>[!TIP]
>
>Chaque fois que vous créez l’archétype, il génère également une série de fichiers LisezMoi, vous fournissant les détails techniques et l’utilisation de chaque module, comme [ci-dessous](#what-you-get).

La création du projet avec Maven crée les artefacts (packages et lots OSGi) qui peuvent être déployés vers AEM. Des commandes et des profils Maven supplémentaires peuvent être utilisés pour déployer les artefacts du projet vers une instance AEM.

## Avantages de l’utilisation de l’archétype {#what-you-get}

L’archétype est constitué de modules qui sont tous créés automatiquement lors de l’utilisation de l’archétype.

* **[core](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/core)** est un lot Java contenant toutes les fonctionnalités de base, telles que les services, les listeners et les planificateurs OSGi, ainsi que le code Java associé aux composants, tel que les servlets et les filtres de requête.
* **[it.tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/it.tests)** sont des tests d’intégration basés sur Java.
* **[ui.apps](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.apps)** contient les parties du projet `/apps` et `/etc`, c’est-à-dire les bibliothèques clientes, les composants et les modèles JS et CSS.
* **[ui.content](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.content)** contient un exemple de contenu utilisant des composants du module ui.apps.
* **[ui.config](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.config)** contient des configurations OSGi spécifiques au projet.
* **[ui.frontend.general](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.general)** contient les artefacts requis pour utiliser le module de génération front-end basé sur Webpack général (facultatif).
* **[ui.frontend.react](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.react)** **(facultatif)** contient les artefacts requis lors de l’utilisation de l’archétype pour créer des projets SPA basés sur React (facultatif, dépend des paramètres de version).
* **[ui.frontend.angular](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.angular)****(facultatif)** contient les artefacts requis lors de l’utilisation de l’archétype pour créer des projets SPA basés sur Angular (facultatif, dépend des paramètres de version).
* **[ui.tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.tests)** contient des tests d’interface utilisateur basés sur Selenium.
* **[al](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/all)** est un package de contenu unique qui intègre tous les modules compilés (lots et packages de contenu), y compris les dépendances des fournisseurs.
* **[dispatcher.ams](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/dispatcher.ams)** contient les configurations de Dispatcher de base pour les projets AMS/On-Prem (facultatif, dépend des paramètres de version).
* **[dispatcher.cloud](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/dispatcher.cloud)** contient les configurations de Dispatcher de base pour les projets AEMaaCS (facultatif, dépend des paramètres de version).

![Organisation du package de contenu](/help/assets/content-package-organization.png)

Les modules de l’archétype AEM représentés dans Maven sont déployés vers AEM en tant que packages de contenu représentant l’application, le contenu et les lots OSGi nécessaires.

## Fichier POM parent {#parent-pom}

Le fichier `pom.xml` racine du projet (`<src-directory>/<project>/pom.xml`) est connu sous le nom de fichier POM parent et oriente la structure du projet et gère les dépendances ainsi que certaines propriétés globales du projet.

### Propriétés globales du projet {#global-properties}

La section `<properties>` du fichier POM parent définit plusieurs propriétés globales importantes pour le déploiement de votre projet vers une instance AEM, telles que le nom d’utilisateur/mot de passe, le nom d’hôte/port, etc.

Ces propriétés sont configurées pour être déployées vers une instance AEM locale, car il s’agit du scénario de création le plus courant pour les développeurs. Notez qu’il existe des propriétés à déployer vers une instance de création et une instance de publication. Il s’agit également de l’endroit où les informations d’identification sont définies pour s’authentifier auprès de l’instance AEM. Les informations d’identification par défaut sont `admin:admin`.

Ces propriétés sont configurées de manière à pouvoir être remplacées lors d’un déploiement vers des environnements de niveau supérieur. De cette manière, les fichiers POM n’ont pas à changer, mais des variables comme `aem.host` et `sling.password` peuvent être remplacées via des arguments de ligne de commande :

```shell
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
```

### Structure du module {#module-structure}

La section `<modules>` du fichier POM parent définit les modules que le projet va créer. Par défaut, le projet crée [les modules standard précédemment définis.](#what-you-get) D’autres modules peuvent toujours être ajoutés à mesure qu’un projet évolue.

### Dépendances {#dependencies}

La section `<dependencyManagement>` du fichier POM parent définit toutes les dépendances et versions des API utilisées dans le projet. Les versions doivent être gérées dans le fichier POM parent. Les sous-modules ne doivent inclure aucune information de version.

#### Uber Jar {#uber-jar}

L’une des dépendances clés est le [Jar d’API Java AEM.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html?lang=fr) Celui-ci inclut toutes les API AEM ayant une seule entrée de dépendance pour la version d’AEM.

>[!NOTE]
>
>Il est recommandé de mettre à jour la version d’Uber Jar pour qu’elle corresponde à la version cible d’AEM. Par exemple, si vous prévoyez de procéder au déploiement vers AEM 6.5, vous devez mettre à jour la version d’Uber Jar vers 6.5.X, où `X` est le dernier pack de services.

#### Composants principaux {#core-components}

L’archétype tire bien sûr parti des [composants principaux.](/help/introduction.md)Par conséquent, pour tirer parti des composants principaux dans tous les déploiements, il est recommandé de les inclure dans le projet Maven.

Le fichier core.wcm.components.example est un ensemble d’exemples de pages qui illustrent des exemples de composants principaux. Les bonnes pratiques recommandent que, lors du déploiement d’un projet destiné à la production, vous supprimiez cette dépendance et cette inclusion de sous-package.

>[!NOTE]
>
>Les composants principaux et l’archétype sont conservés en tant que projets GitHub distincts et leurs versions diffèrent donc.
>
>Chaque version de l’archétype utilisera la dernière version des composants principaux disponibles au moment de la publication. Cependant, vous pouvez mettre à jour manuellement la dépendance sur les composants principaux.

## Tests {#testing}

Il existe trois niveaux de tests contenus dans le projet et, parce qu’il s’agit de différents types de tests, ils sont exécutés de différentes manières ou à différents endroits.

* **[Test unitaire](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/core)** - : test unitaire classique du code contenu dans le lot
* **[Tests d’intégration](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/it.tests)** : tests d’intégration côté serveur s’exécutant comme des tests de type unitaire dans l’environnement AEM, c’est-à-dire sur le serveur AEM
* **[Tests de l’interface utilisateur](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.tests)** : tests côté navigateur basés sur Selenium qui vérifient le comportement côté navigateur
