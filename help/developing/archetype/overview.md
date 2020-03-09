---
title: Archétype de projet AEM
description: Modèle de projet pour les applications basées sur AEM
translation-type: tm+mt
source-git-commit: 6be0028c45ce9f8b36ea278f8e569f3d6a626ae2

---


# Archétype de projet AEM {#aem-project-archetype}

L’archétype de projet AEM crée un projet Adobe Experience Manager minimal qui s&#39;appuie sur des bonnes pratiques pour que vous puissiez démarrer vos propres projets AEM sur des bases saines. Les propriétés à fournir lors de l&#39;utilisation de cet archétype vous permettent de spécifier les noms de toutes les parties de ce projet et de contrôler certaines fonctionnalités facultatives.

>[!TIP]
>
>Le dernier archétype de projet AEM [est disponible sur GitHub](https://github.com/adobe/aem-project-archetype).

## Fonctionnalités {#features}

L’archétype comporte plusieurs fonctionnalités destinées à offrir un point de départ pratique pour les nouveaux projets AEM :

* Pages en anglais et en français avec un exemple de contenu
* Un modèle de contenu basé sur la fonction de modèle modifiable avec un exemple de stratégie de contenu
* Composant de page basé sur le [composant principal de page AEM](/help/components/page.md)
* Exemples de composants de contenu implémentés avec le modèle de proxy recommandé et un exemple de composant personnalisé helloworld tous basés sur les [composants principaux AEM](/help/introduction.md).
* Exemples de [composants de formulaire](/help/components/forms/form-container.md)
* Configurations des émulateurs de terminal, configuration par glisser-déposer et internationalisation
* Bibliothèques clientes observant les conventions de dénomination BEM et styles spécifiques aux composants
* Exemples de lots incluant des exemples de modèles, des serveurs, des  et des
* Tests d’unité, d’intégration et côté client
* Exemples d’implémentations SPA dans Réaction ou Angulaire (facultatif)

## Pourquoi utiliser l&#39;archétype {#why-use-the-archetype}

L’utilisation de l’archétype de projet AEM vous permet de vous orienter vers la création d’un projet AEM basé sur des bonnes pratiques, et ce, en un tour de main. Avec l’archétype, toutes les pièces sont déjà en place afin que, même avec un résultat de projet très simple, celui-ci implémente déjà toutes les [fonctionnalités clés](#features) d’AEM. Tout ce que vous aurez alors à faire est de vous appuyer sur ce projet de base et de le développer.

De nombreux éléments entrent bien sûr en compte dans la réussite d&#39;un projet AEM, mais l’utilisation de l’archétype de projet AEM constitue une base solide et est vivement recommandée pour la création de tout projet AEM.

## Prise en main {#getting-started}

L’archétype du projet facilite la prise en main du développement sur AEM. Vous pouvez faire vos premiers pas de plusieurs manières.

* Didacticiel WKND - Pour une excellente introduction au développement sur AEM, y compris sur la manière de tirer parti de l’archétype, reportez-vous au didacticiel [Prise en main des sites AEM - WKND](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) pour obtenir un exemple pratique qui vous guide tout au long de l’utilisation de l’archétype pour mettre en oeuvre un projet simple.
* Didacticiel sur les  WKND - Si vous êtes particulièrement intéressé par le développement d’applications d’une seule page (SPA) sur AEM, n’oubliez pas de consulter le didacticiel [sur les](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html)WKND dédiés.
* Téléchargez et vous-même ! - Vous pouvez facilement télécharger l&#39;archétype de projet actuel disponible sur GitHub et créer votre premier projet en [suivant les étapes simples ci-dessous](#how-to-use-the-archetype).

## Avantages de l&#39;utilisation de l&#39;archétype {#what-you-get}

L’archétype AEM est constitué de modules :

* **[principaux](core.md)** : un lot Java contenant toutes les fonctionnalités de base, telles que les services OSGi, les écouteurs et les planificateurs, ainsi que le code Java associé aux composants, tel que les servlets et les filtres de requête.
* **[ui.apps](uiapps.md)** : avec les éléments`/apps`et`/etc`du projet, c’est-à-dire les bibliothèques clients JS et CSS, les composants, les modèles, les configurations spécifiques au mode d’exécution, ainsi que les tests Hobbes.
* **[ui.content](uicontent.md)** : avec un exemple de contenu utilisant des composants du module ui.apps.
* **[ui.tests](uitests.md)** : lot Java contenant des tests JUnit exécutés côté serveur. Ce lot ne doit pas être déployé en production.
* **ui.launcher** : avec le code-glue qui déploie le lot ui.tests (et les lots dépendants) vers le serveur et déclenche l’exécution de JUnit distante.
* **[ui.frontend.general](uifrontend.md)**:**(facultatif)**contient les artefacts requis pour utiliser le module de génération frontale basé sur Webpack général.
* **[ui.frontend.response](uifrontend-react.md)**:**(facultatif)**contient les artefacts requis lors de l’utilisation de l’archétype pour créer des projets SPA basés sur React.
* **[ui.frontend.angular](uifrontend-angular.md)**:**(facultatif)**contient les artefacts requis lors de l’utilisation de l’archétype pour créer des projets SPA basés sur Angular.

![](/help/assets/archetype-structure.png)

Les modules de l’archétype AEM représentés dans Maven sont déployés vers AEM en tant que packages de contenu représentant l’application, le contenu et les lots OSGi nécessaires.

## Conditions {#requirements}

La version actuelle de l’archétype requiert les éléments suivants :

* Adobe Experience Manager 6.3.3.0 ou version ultérieure (6.4.2 ou version ultérieure lors de la génération d’un projet avec les options de génération frontale Angular ou React) ou [AEM en tant que service Cloud](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)
* Apache Maven (3.3.9 ou version ultérieure)
* Référentiel Adobe Public Maven dans vos paramètres Maven. Consultez cet [article de la Base de connaissances pour plus de détails](https://helpx.adobe.com/experience-manager/kb/SetUpTheAdobeMavenRepository.html).

Pour obtenir la liste des versions AEM prises en charge pour les versions précédentes de l’archétype, reportez-vous à l’[historique des versions AEM prises en charge](https://github.com/adobe/aem-project-archetype/blob/master/VERSIONS.md).

## Utilisation de l&#39;archétype {#how-to-use-the-archetype}

Pour utiliser l&#39;archétype, vous devez d&#39;abord créer un projet qui génère les modules dans une structure de fichiers locale comme [décrit précédemment](#what-you-get). Dans le cadre de la génération du projet, plusieurs propriétés de votre projet peuvent être définies, telles que le nom du projet, la version, etc.

La création du projet avec Maven crée les artefacts (packages et lots OSGi) qui peuvent être déployés vers AEM. Des commandes et des profils Maven supplémentaires peuvent être utilisés pour déployer les artefacts du projet vers une instance AEM.

### Création d’un projet {#create-project}

Pour commencer, il vous suffit d’utiliser l&#39;[extension Eclipse AEM](https://docs.adobe.com/content/help/en/experience-manager-65/developing/devtools/aem-eclipse.html), de suivre l’assistant Nouveau projet et de choisir **AEM Sample Multi-Module Project** pour utiliser une version publiée de l’archétype.

Bien sûr, vous pouvez également appeler Maven directement.

```
mvn archetype:generate \
 -DarchetypeGroupId=com.adobe.granite.archetypes \
 -DarchetypeArtifactId=aem-project-archetype \
 -DarchetypeVersion=XX
```

Où `XX` est le [numéro de la dernière version](https://github.com/adobe/aem-project-archetype/blob/master/VERSIONS.md) de l&#39;archétype de projet AEM.

>[!NOTE]
>
>Il est recommandé d’ajouter le profil `adobe-public` à votre fichier `settings.xml` Maven afin d’ajouter automatiquement repo.adobe.com au processus de création Maven.
>
>Un exemple de fichier POM [est disponible ici](https://helpx.adobe.com/experience-manager/kb/SetUpTheAdobeMavenRepository.html).

### Propriétés {#properties}

Les propriétés suivantes sont disponibles lors de la création d’un projet à l’aide de l’archétype.

| Nom | Default | Description |
----------------------------|---------|--------------------
| `groupId` |  | `groupId` Maven de base |
| `artifactId` |  | ID d’artefact Maven de base |
| `version` |  | Version |
| `package` |  | Package source Java |
| `appID` |  |  utilisé pour les dossiers de composants, de configuration et de contenu et les ID CSS |
| `appTitle` |  | Titre de l’application utilisé pour le titre du site Web et les groupes de composants |
| `aemVersion` | 6.5.0 | Version cible d’AEM |
| `sdkVersion` |  |
| `languageCountry` | en_us | Code de langue et de pays pour créer la structure de contenu localisée (ex. `en_us`) |
| `includeExamples` | y | Inclure un exemple de site de bibliothèque de composants |
| `includeErrorHandler` | n | Inclure une page de réponse 404 personnalisée |
| `frontendModule` | none | Inclure un module frontal dédié (l&#39;un des `none`, [`general`](uifrontend.md), [`angular`](uifrontend-angular.md), [`react`](uifrontend-react.md)) |
| `singleCountry` | y | Création d’une structure de langue principale dans un exemple de contenu |
| `includeDispatcherConfig` | n | Définit si une configuration de répartiteur est générée pour le projet <br> défini sur [`cloud`](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.cloud) lors de la création d’un projet pour [AEM en tant que service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) Cloud défini sur <br> [`ams`](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) lors de la création d’un projet pour Adobe Managed Services |

>[!NOTE]
> Si l’archétype est exécuté en mode interactif la première fois, les propriétés ayant des valeurs par défaut ne peuvent pas être modifiées (voir [ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) pour plus de détails). La valeur peut être modifiée lorsque la confirmation de propriété finale est refusée et que le questionnaire est répété, ou en transmettant le paramètre dans la ligne de commande (par ex., `-DoptionIncludeExamples=n`).

>[!NOTE]
>Lorsque vous exécutez Windows et générez la configuration du répartiteur, vous devez être exécuté dans une invite de commande élevée ou dans le sous-système Windows pour Linux (voir [la publication 329](https://github.com/adobe/aem-project-archetype/issues/329)).

### Profils {#profiles}

Le projet Maven généré prend en charge différents profils de déploiement lors de l’exécution de `mvn install`.

| ID de profil | Description |
--------------------------|------------------------------
| `autoInstallBundle` | Installez le lot principal avec le maven-sling-plugin dans la console felix. |
| `autoInstallPackage` | Installez le package de contenu ui.content et ui.apps avec le plug-in content-package-maven-plugin dans le gestionnaire de packages afin d’installer l’instance d’auteur par défaut sur localhost, port 4502. Hostname and port can be changed with the `aem.host` and `aem.port` user defined properties. |
| `autoInstallPackagePublish` | Installe le package de contenu ui.content et ui.apps avec le plug-in content-package-maven-plugin dans le gestionnaire de packages dans l’instance de publication par défaut sur l’hôte local, le port 4503. Hostname and port can be changed with the `aem.host` and `aem.port` user defined properties. |
| `autoInstallSinglePackage` | Install the `all` content package with the content-package-maven-plugin to the package manager to default author instance on localhost, port 4502. Hostname and port can be changed with the `aem.host` and `aem.port` user defined properties. |
| `autoInstallSinglePackagePublish` | Install the `all` content package with the content-package-maven-plugin to the package manager to default publish instance on localhost, port 4503. Hostname and port can be changed with the `aem.host` and `aem.port` user defined properties. |
| `integrationTests` | Exécute les tests d’intégration fournis sur l’instance AEM (uniquement pour la phase `verify`). |

### Création et installation {#building-and-installing}

Pour créer tous les modules exécutés dans le répertoire racine du projet, utilisez la commande Maven suivante.

```
mvn clean install
```

Si vous disposez d’une instance AEM en cours d’exécution, vous pouvez créer et assembler l’ensemble du projet et le déployer vers AEM avec la commande Maven suivante.

```
mvn clean install -PautoInstallPackage
```

Pour déployer le projet vers une instance de publication, exécutez cette commande.

```
mvn clean install -PautoInstallPackagePublish
```

Vous pouvez également exécuter cette commande pour effectuer un déploiement vers une instance de publication.

```
mvn clean install -PautoInstallPackage -Daem.port=4503
```

Ou pour déployer uniquement le lot vers l’auteur, exécutez cette commande.

```
mvn clean install -PautoInstallBundle
```

## Fichier POM parent {#parent-pom}

Le fichier `pom.xml` racine du projet (`<src-directory>/<project>/pom.xml`) est connu sous le nom de fichier POM parent et oriente la structure du projet et gère les dépendances ainsi que certaines propriétés globales du projet.

### Propriétés globales du projet {#global-properties}

La section `<properties>` du fichier POM parent définit plusieurs propriétés globales importantes pour le déploiement de votre projet vers une instance AEM, telles que le nom d’utilisateur/mot de passe, le nom d’hôte/port, etc.

Ces propriétés sont configurées pour être déployées vers une instance AEM locale, car il s’agit du scénario de création le plus courant pour les développeurs. Notez qu’il existe des propriétés à déployer vers une instance de création et une instance de publication. Il s&#39;agit également de l’endroit où les informations d’identification sont définies pour s’authentifier auprès de l’instance AEM. Les informations d’identification admin:admin utilisées sont celles par défaut.

Ces propriétés sont configurées de manière à pouvoir être remplacées lors d&#39;un déploiement vers des environnements de niveau supérieur. De cette manière, les fichiers POM n’ont pas à changer, mais des variables comme `aem.host` et `sling.password` peuvent être remplacées via des arguments de ligne de commande :

````
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
````

### Structure du module {#module-structure}

La section `<modules>` du fichier POM parent définit les modules que le projet va créer. Par défaut, le projet crée [les modules standard précédemment définis](#what-you-get) : core, ui.apps, ui.content, ui.tests et it.launcher. D&#39;autres modules peuvent toujours être ajoutés à mesure qu&#39;un projet évolue.

### Dépendances {#dependencies}

La section `<dependencyManagement>` du fichier POM parent définit toutes les dépendances et versions des API utilisées dans le projet. Les versions doivent être gérées dans le fichier POM parent. Les sous-modules tels que core et ui.apps ne doivent inclure aucune information de version.

#### Uber Jar {#uber-jar}

L’une des dépendances clés est [AEM Uber Jar](https://docs.adobe.com/content/help/en/experience-manager-65/developing/devtools/ht-projects-maven.html#ExperienceManagerAPIDependencies). Celui-ci inclut toutes les API AEM ayant une seule entrée de dépendance pour la version d’AEM.

>[!NOTE]
>
>Il est recommandé de mettre à jour la version d&#39;Uber Jar pour qu’elle corresponde à la version cible d’AEM. Par exemple, si vous prévoyez de procéder au déploiement vers AEM 6.4, vous devez mettre à jour la version d&#39;Uber Jar vers la 6.4.0.

#### Composants principaux {#core-components}

L’archétype de projet AEM tire bien sûr parti des composants principaux.

Les composants principaux sont installés automatiquement dans AEM dans le mode d’exécution par défaut et utilisés par l’exemple de site Web.Retail. Dans un [mode d’exécution de production](https://docs.adobe.com/content/help/en/experience-manager-65/administering/security/production-ready.html) (`nosamplecontent`), les composants principaux ne sont pas disponibles.

Par conséquent, pour tirer parti des composants principaux dans tous les déploiements, il est recommandé de les inclure dans le projet Maven.

>[!NOTE]
>
>Chaque version des composants principaux est généralement suivie d’une version de l’archétype de projet AEM, de sorte que l’archétype le plus récent utilise la dernière version des composants principaux.
>
>Cependant, une nouvelle version de l&#39;archétype peut ne pas suivre directement une nouvelle version des composants principaux. Vous pouvez donc mettre à jour la dépendance envers les composants principaux vers la dernière version.

>[!NOTE]
>
>Le fichier core.wcm.components.example est un ensemble d’exemples de pages qui illustrent des exemples de composants principaux. Les bonnes pratiques recommandent que, lors du déploiement d’un projet destiné à la production, vous supprimiez cette dépendance et cette inclusion de sous-package.

## Tests {#testing}

Il existe trois niveaux de tests contenus dans le projet et, parce qu&#39;il s&#39;agit de différents types de tests, ils sont exécutés de différentes manières ou à différents endroits.

* Test unitaire dans le noyau : celui-ci comprend les tests unitaires classiques du code contenu dans le lot. Pour lancer ce test, exécutez :
   * `mvn clean test`
* Tests d’intégration côté serveur : ces tests exécutent des tests de type unitaire dans l’environnement AEM, c’est-à-dire sur le serveur AEM. Pour lancer ce test, exécutez :
   * `mvn clean verify -PintegrationTests`
* Tests Hobbes.js côté client : il s’agit de tests JavaScript côté navigateur qui vérifient le comportement côté navigateur. Pour tester :
   1. Chargez AEM dans votre navigateur comme vous le feriez pour créer une page.
   1. Ouvrez la page en [mode développeur](https://docs.adobe.com/content/help/en/experience-manager-65/developing/components/developer-mode.html).
   1. Ouvrez le panneau de gauche et basculez sur l’onglet **Tests**.
   1. Recherchez les **Tests MonNom** générés et exécutez-les.

## Étapes suivantes {#next-steps}

Vous avez ainsi créé et installé l’archétype de projet AEM. Et maintenant ? L’archétype est petit mais comprend de nombreux exemples de puissantes fonctionnalités AEM configurées selon les recommandations des bonnes pratiques. Utilisez ces exemples pour vous guider sur la meilleure manière de tirer parti de ces fonctionnalités dans votre projet. Pour tout projet, il vous faudra probablement :

* [Personnaliser les composants en étendant les composants principaux existants](/help/developing/customizing.md)
* [Ajouter des modèles supplémentaires](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)
* [Adapter la structure de localisation](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/tc-prep.html)
* [En savoir plus sur le module de génération front-end](uifrontend.md)
