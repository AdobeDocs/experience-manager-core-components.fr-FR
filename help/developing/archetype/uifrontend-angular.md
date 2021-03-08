---
title: Génération front-end pour les applications monopage Angular
description: Description du processus de génération front-end pour les projets d’application monopage Angular
translation-type: ht
source-git-commit: 9d737b31efc8c346775ea5296f7599295af07cf1
workflow-type: ht
source-wordcount: '404'
ht-degree: 100%

---


# Génération front-end pour les applications monopage Angular {#frontend-angular}

Ce document explique les détails du projet créé lors de l’utilisation de l’archétype pour créer une application monopage (SPA) basée sur l’infrastructure Angular, c’est-à-dire, lorsque vous définissez l’option `frontendModule` sur `angular`.

## Présentation {#overview}

Ce projet a été démarré avec l’[interface de ligne de commande Angular](https://github.com/angular/angular-cli).

Cette application est créée pour consommer le modèle AEM d’un site. Elle génère automatiquement la mise en page à l’aide des composants de l’application d’assistance à partir du package [@adobe/cq-angular-editable-components](https://www.npmjs.com/package/@adobe/cq-angular-editable-components).

## Scripts {#scripts}

Dans le répertoire du projet, vous pouvez exécuter les commandes ci-après.

### npm start {#npm-start}

```
npm start
```

Cette commande exécute l’application en mode de développement en transmettant un proxy au modèle JSON à partir d’une instance AEM locale s’exécutant sur http://localhost:4502. Cela suppose que le projet entier a été déployé sur AEM au moins une fois (`mvn clean install -PautoInstallPackage` à la racine du projet).

Une fois que vous avez exécuté npm start dans le répertoire ui.frontend, votre application s’ouvre automatiquement dans votre navigateur (à l’adresse http://localhost:4200/content/${appId}/${country}/${language}/home.html). Si vous effectuez des modifications, la page se recharge.

Si des erreurs liées à CORS s’affiche, vous souhaiterez peut-être configurer AEM comme suit :

1. Accédez au gestionnaire de configuration (http://localhost:4502/system/console/configMgr).
1. Ouvrez la configuration pour « Adobe Granite Cross-Origin Resource Sharing Policy ».
1. Créez une configuration avec les valeurs supplémentaires suivantes :
   * Origines autorisées : http://localhost:4200
   * En-têtes pris en charge : Autorisation
   * Méthodes autorisées : OPTIONS

### test npm {#npm-test}

```shell
npm test
```

Cette commande lance l’exécuteur de test Karma. Pour plus d’informations, consultez la [documentation Angular sur l’exécution des tests](https://angular.io/guide/testing).

### npm run test:debug {#npm-run-test-debug}

```shell
npm run test:debug
```

Cette commande lance l’exécuteur de test Karma en mode espion interactif.

### npm run build {#npm-run-build}

```shell
npm run build
```

Cette commande crée l’application pour production dans le dossier de génération. Elle place Angular en mode de production et optimise la génération pour des performances optimales. Pour plus d’informations, consultez la [documentation Angular sur le déploiement](https://angular.io/guide/deployment).

De plus, une bibliothèque cliente AEM est générée à partir de l’application à l’aide du package [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator).

Pour plus d’informations sur l’utilisation des bibliothèques clientes AEM par l’archétype du projet, consultez la [documentation générale du module ui.frontend](uifrontend.md#clientlibs).

## Prise en charge des navigateurs {#browser-support}

Par défaut, ce projet utilise l’option par défaut [Browserslist](https://github.com/browserslist/browserslist) pour identifier les navigateurs cible. De plus, il inclut des polyfills pour les fonctionnalités de langage moderne afin de prendre en charge les navigateurs plus anciens (par exemple, Internet Explorer 11). Si la prise en charge de ces navigateurs n’est pas obligatoire, les dépendances de polyfills et les importations peuvent être supprimées.
