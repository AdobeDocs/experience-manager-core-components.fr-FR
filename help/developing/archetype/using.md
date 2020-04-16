---
title: Utilisation de l’archétype du projet AEM
description: Instructions d’utilisation détaillées pour l’archétype de projet AEM
translation-type: tm+mt
source-git-commit: 477a1774a856725f52b9db7a978c534de4700661

---


# Archétype de projet AEM {#aem-project-archetype}

L’archétype de projet AEM crée un projet Adobe Experience Manager minimal qui s&#39;appuie sur des bonnes pratiques pour que vous puissiez démarrer vos propres projets AEM sur des bases saines. Les propriétés à fournir lors de l&#39;utilisation de cet archétype vous permettent de spécifier les noms de toutes les parties de ce projet et de contrôler certaines fonctionnalités facultatives.

## Pourquoi utiliser l&#39;archétype {#why-use-the-archetype}

L’utilisation de l’archétype de projet AEM vous permet de vous orienter vers la création d’un projet AEM basé sur des bonnes pratiques, et ce, en un tour de main. Avec l’archétype, toutes les pièces sont déjà en place afin que, même avec un résultat de projet très simple, celui-ci implémente déjà toutes les [fonctionnalités clés](#features) d’AEM. Tout ce que vous aurez alors à faire est de vous appuyer sur ce projet de base et de le développer.

De nombreux éléments entrent bien sûr en compte dans la réussite d&#39;un projet AEM, mais l’utilisation de l’archétype de projet AEM constitue une base solide et est vivement recommandée pour la création de tout projet AEM.

## Prise en main {#getting-started}

L’archétype de projet permet de commencer facilement à développer dans AEM. Vous pouvez débuter de plusieurs manières.

* Tutoriel WKND - Pour une excellente introduction au développement dans AEM, notamment des informations sur l’utilisation de l’archétype, reportez-vous à [Prise en main d’AEM Sites - tutoriel WKND](https://docs.adobe.com/content/help/fr/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) afin d’obtenir un exemple pratique vous guidant tout au long de l’utilisation de l’archétype pour mettre en œuvre un projet simple.
* Tutoriel sur WKND Events - Si vous êtes particulièrement intéressé par le développement d’applications monopage (SPA) dans AEM, consultez notre [tutoriel WKND Events](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html) dédié.
* Téléchargez et commencez votre premier projet. - Vous pouvez facilement télécharger l’archétype de projet actuel disponible sur GitHub et créer votre premier projet en [suivant les étapes simples ci-dessous](#how-to-use-the-archetype).

## Avantages de l&#39;utilisation de l&#39;archétype {#what-you-get}

L’archétype AEM est constitué de modules :

* **[principaux](core.md)** : un lot Java contenant toutes les fonctionnalités de base, telles que les services OSGi, les écouteurs et les planificateurs, ainsi que le code Java associé aux composants, tel que les servlets et les filtres de requête.
* **[ui.apps](uiapps.md)** : contient les éléments`/apps`et`/etc`du projet, c’est-à-dire les bibliothèques clientes JS et CSS, les composants, les modèles, les configurations spécifiques au mode d’exécution, ainsi que les tests Hobbes.
* **[ui.content](uicontent.md)** : avec un exemple de contenu utilisant des composants du module ui.apps.
* **[ui.tests](uitests.md)** : lot Java contenant des tests JUnit exécutés côté serveur. Ce lot ne doit pas être déployé en production.
* **ui.launcher** : avec le code-glue qui déploie le lot ui.tests (et les lots dépendants) vers le serveur et déclenche l’exécution de JUnit distante.
* **[ui.frontend.general](uifrontend.md)** :**(facultatif)**contient les artefacts requis pour utiliser le module de génération front-end basé sur Webpack général.
* **[ui.frontend.react](uifrontend-react.md)** :**(facultatif)**contient les artefacts requis lors de l’utilisation de l’archétype pour créer des projets SPA basés sur React.
* **[ui.frontend.angular](uifrontend-angular.md)** :**(facultatif)**contient les artefacts requis lors de l’utilisation de l’archétype pour créer des projets SPA basés sur Angular.

![](/help/assets/archetype-structure.png)

Les modules de l’archétype AEM représentés dans Maven sont déployés vers AEM en tant que packages de contenu représentant l’application, le contenu et les lots OSGi nécessaires.

## Utilisation de l&#39;archétype {#how-to-use-the-archetype}

Pour utiliser l&#39;archétype, vous devez d&#39;abord créer un projet qui génère les modules dans une structure de fichiers locale comme [décrit précédemment](#what-you-get). Dans le cadre de la génération du projet, plusieurs propriétés de votre projet peuvent être définies, telles que le nom du projet, la version, etc.

La création du projet avec Maven crée les artefacts (packages et lots OSGi) qui peuvent être déployés vers AEM. Des commandes et des profils Maven supplémentaires peuvent être utilisés pour déployer les artefacts du projet vers une instance AEM.

### Création d’un projet {#create-project}

Pour commencer, il vous suffit d’utiliser l&#39;[extension Eclipse AEM](https://docs.adobe.com/content/help/en/experience-manager-65/developing/devtools/aem-eclipse.html), de suivre l’assistant Nouveau projet et de choisir **AEM Sample Multi-Module Project** pour utiliser une version publiée de l’archétype.

Bien sûr, vous pouvez également appeler Maven directement.

```
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.granite.archetypes \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=XX \
 -D aemVersion=cloud \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
 -D frontendModule=general \
 -D includeExamples=n
```

* Set `XX` to the [version number](https://github.com/adobe/aem-project-archetype/blob/master/VERSIONS.md) of the latest AEM Project Archetype.
* Défini `aemVersion=cloud` pour [AEM en tant que service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)Cloud ;\
   Défini `aemVersion=6.5.0` pour [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)ou sur site.
La dépendance des composants principaux n’est ajoutée que pour les versions d’Aem non cloud, car les composants principaux sont fournis avec une optimisation d’AEM en tant que CloudService.
* Ajustez `appTitle="My Site"` pour définir le titre du site Web et les groupes de composants.
* Ajustez `appId="mysite"` la variable pour définir le paramètre Maven artifactId, le composant, les noms de dossier de configuration et de contenu, ainsi que les noms de bibliothèque cliente.
* Définissez `groupId="com.mysite"` le groupId Maven et le package source Java.
* Recherchez le  des propriétés disponibles pour savoir s’il y a plus à ajuster.

>[!NOTE]
>
>Il est recommandé d’ajouter le profil `adobe-public` à votre fichier `settings.xml` Maven afin d’ajouter automatiquement repo.adobe.com au processus de création Maven.
>
>Un exemple de fichier POM [est disponible ici](https://helpx.adobe.com/experience-manager/kb/SetUpTheAdobeMavenRepository.html).

### Propriétés {#properties}

Les propriétés suivantes sont disponibles lors de la création d’un projet à l’aide de l’archétype.

| Nom | Default | Description |
--------------------------|----------------|--------------------
| `appTitle` |  | Le titre de la demande sera utilisé pour le titre du site Web et les groupes de composants (p. ex. `"My Site"`). |
| `appId` |  | Le nom technique sera utilisé pour les noms de composants, de configurations et de dossiers de contenu, ainsi que pour les noms de bibliothèques client (ex. `"mysite"`). |
| `artifactId` | *`${appId}`* | Base Maven artifact ID (e.g. `"mysite"`). |
| `groupId` |  | Base Maven group ID (e.g. `"com.mysite"`). |
| `package` | *`${groupId}`* | Package source Java (ex. `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | Version du projet (ex. `1.0-SNAPSHOT`). |
| `aemVersion` | `6.5.0` |  version d’AEM (peut être `cloud` pour [AEM en tant que service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)Cloud ; ou `6.5.0`, `6.4.4`ou `6.3.3` Adobe Managed Services [](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) ou on-premise). |
| `sdkVersion` | `latest` | Lorsqu’ `aemVersion=cloud` une version du [SDK](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) peut être spécifiée (p. ex. `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Inclut une configuration de répartiteur pour le cloud ou pour AMS/sur site, selon la valeur de `aemVersion` (peut être `y` ou `n`). |
| `frontendModule` | `none` | Comprend un module de génération frontale Webpack qui génère les bibliothèques client (peut être `general` ou `none` pour les sites standard ; peut être `angular` ou `react` pour une application d’une seule page qui implémente l’éditeur [d’](https://docs.adobe.com/content/help/en/experience-manager-65/developing/headless/spas/spa-overview.html)application d’une seule page). |
| `languageCountry` | `en_us` | Language and country code to create the content structure from (e.g. `en_us`). |
| `singleCountry` | `y` | Inclut une structure de contenu maître de langue (peut être `y`ou `n`). |
| `includeExamples` | `y` | Inclut un exemple de site de bibliothèque [de](https://www.aemcomponents.dev/) composants (peut être `y`ou `n`). |
| `includeErrorHandler` | `n` | Inclut une page de réponse personnalisée 404 qui sera globale pour l’instance entière (peut être `y` ou `n`). |

>[!NOTE]
> Si l’archétype est exécuté en mode interactif la première fois, les propriétés ayant des valeurs par défaut ne peuvent pas être modifiées (voir [ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) pour plus de détails). La valeur peut être modifiée lorsque la confirmation de propriété finale est refusée et que le questionnaire est répété, ou en transmettant le paramètre dans la ligne de commande (par ex., `-DoptionIncludeExamples=n`).

>[!NOTE]
>Lorsque vous exécutez Windows et générez la configuration du Dispatcher, vous devez utiliser une invite de commandes avec élévation de privilèges ou le sous-système Windows pour Linux (voir le [problème 329](https://github.com/adobe/aem-project-archetype/issues/329)).

### Profils {#profiles}

Le projet Maven généré prend en charge différents profils de déploiement lors de l’exécution de `mvn install`.

| ID de profil | Description |
--------------------------|------------------------------
| `autoInstallBundle` | Installez le lot principal avec le plug-in maven-sling-plugin sur la console felix. |
| `autoInstallPackage` | Installez le package de contenu ui.content et ui.apps avec le plug-in content-package-maven-plugin dans le gestionnaire de packages sur l’instance de création par défaut sur l’hôte local, port 4502. Le nom d’hôte et le port peuvent être modifiés à l’aide des propriétés `aem.host` et `aem.port` définies par l’utilisateur. |
| `autoInstallPackagePublish` | Installez le package de contenu ui.content et ui.apps avec le plug-in content-package-maven-plugin dans le gestionnaire de packages sur l’instance de publication par défaut sur l’hôte local, port 4503. Le nom d’hôte et le port peuvent être modifiés à l’aide des propriétés `aem.host` et `aem.port` définies par l’utilisateur. |
| `autoInstallSinglePackage` | Installez le package de contenu `all` avec le plug-in content-package-maven-plugin dans le gestionnaire de packages sur l’instance de création par défaut sur l’hôte local, port 4502. Le nom d’hôte et le port peuvent être modifiés à l’aide des propriétés `aem.host` et `aem.port` définies par l’utilisateur. |
| `autoInstallSinglePackagePublish` | Installez le package de contenu `all` avec le plug-in content-package-maven-plugin dans le gestionnaire de packages sur l’instance de publication par défaut sur l’hôte local, port 4503. Le nom d’hôte et le port peuvent être modifiés à l’aide des propriétés `aem.host` et `aem.port` définies par l’utilisateur. |
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