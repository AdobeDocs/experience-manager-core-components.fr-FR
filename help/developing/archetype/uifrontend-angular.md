---
title: Version frontale pour les applications monopages angulaires
description: Description du processus de génération frontale pour les projets d’application d’une seule page
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Version frontale pour les applications monopages angulaires {#frontend-angular}

Ce document explique les détails du projet créé lors de l’utilisation de l’archétype pour créer une application d’une seule page (SPA) basée sur la structure angulaire. Par exemple, lorsque vous définissez l’ `frontendModule` option sur `angular`.

## Présentation {#overview}

Ce projet a été lancé avec l&#39;interface de ligne de commande [angulaire](https://github.com/angular/angular-cli).

Cette application est créée pour consommer le modèle AEM d’un site. Il génère automatiquement la mise en page à l’aide des composants de l’aide à partir du package [@adobe/cq-angular-editable-components](https://www.npmjs.com/package/@adobe/cq-angular-editable-components) .

## Scripts {#scripts}

Dans le répertoire du projet, vous pouvez exécuter les commandes suivantes.

### démarrage de npm {#npm-start}

```
npm start
```

Cette commande exécute l’application en mode de développement en proxy du modèle JSON à partir d’une instance locale AEM s’exécutant sur http://localhost:4502. Cela suppose que l’ensemble du projet a été déployé sur AEM au moins une fois (`mvn clean install -PautoInstallPackage` dans la racine du projet).

Après avoir exécuté npm start dans le répertoire ui.frontend, votre application s’ouvre automatiquement dans votre navigateur (à l’adresse http://localhost:4200/content/${appId}/${country}/${language}/home.html). Si vous effectuez des modifications, la page se recharge.

Si vous recevez des erreurs liées à CORS, vous pouvez configurer AEM comme suit :

1. Accédez à Configuration Manager (http://localhost:4502/system/console/configMgr)
1. Ouvrez la configuration pour &quot;Adobe Granite Cross-Origin Resource Sharing Policy&quot;.
1. Créez une configuration avec les valeurs supplémentaires suivantes :
   * Origines autorisées : http://localhost:4200
   * En-têtes pris en charge : Autorisation
   * Méthodes autorisées : OPTIONS

### test npm {#npm-test}

```
npm test
```

Cette commande lance le pilote de test Karma. Pour plus d’informations, consultez la documentation [Angular sur l’exécution des tests](https://angular.io/guide/testing) .

### test d’exécution npm:débogage {#npm-run-test-debug}

```
npm run test:debug
```

Cette commande lance le pilote de test Karma en mode de contrôle interactif.

### npm run build {#npm-run-build}

```
npm run build
```

Cette commande crée l’application en vue de sa production dans le dossier de création. Il regroupe Angular en mode de production et optimise la génération pour obtenir de meilleures performances. Pour plus d’informations, consultez la documentation [Angular sur le déploiement](https://angular.io/guide/deployment) .

De plus, une bibliothèque cliente AEM est générée à partir de l’application à l’aide du package [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator) .

Pour plus d’informations sur la manière dont AEM ClientLibs est utilisé par l’archétype du projet, consultez la documentation [générale du module](uifrontend.md#clientlibs) ui.frontend.

## Prise en charge des navigateurs {#browser-support}

Par défaut, ce projet utilise l’option par défaut de [Browserslist](https://github.com/browserslist/browserslist)pour identifier les navigateurs cibles. De plus, il inclut des remplissages polyvalents pour les fonctionnalités de langue moderne afin de prendre en charge les anciens navigateurs (par exemple, Internet Explorer 11). Si la prise en charge de ces navigateurs n’est pas obligatoire, les dépendances de polyremplissage et les importations peuvent être supprimées.
