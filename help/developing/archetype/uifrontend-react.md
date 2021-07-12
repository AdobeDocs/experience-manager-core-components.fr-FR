---
title: Génération front-end pour les applications monopage React
description: Description du processus de génération front-end pour les projets d’application monopage React
feature: Composants principaux, archétype de projet AEM
role: Architect, Developer, Admin
exl-id: dd8ef13a-9686-47a9-b6af-e486ff10c4d8
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 100%

---

# Génération front-end pour les applications monopage React {#frontend-react}

Ce document explique les détails du projet créé lors de l’utilisation de l’archétype pour créer une application monopage (SPA) basée sur l’infrastructure React, c’est-à-dire, lorsque vous définissez l’option `frontendModule` sur `react`.

## Présentation {#overview}

Ce projet a été démarré avec [create-response-app](https://github.com/facebook/create-react-app).

Cette application est créée pour consommer le modèle AEM d’un site. Elle génère automatiquement la mise en page à l’aide des composants de l’application d’assistance à partir du package [@adobe/cq-response-editable-components](https://www.npmjs.com/package/@adobe/cq-react-editable-components).

## Scripts {#scripts}

Dans le répertoire du projet, vous pouvez exécuter les commandes suivantes :

### npm start {#npm-start}

```shell
npm start
```

Cette commande exécute l’application en mode de développement en transmettant un proxy au modèle JSON à partir d’une instance AEM locale s’exécutant sur http://localhost:4502. Cela suppose que le projet entier a été déployé sur AEM au moins une fois (`mvn clean install -PautoInstallPackage` à la racine du projet).

Après l’exécution de `npm start` dans le répertoire [ui.frontend](uifrontend.md), votre application s’ouvre automatiquement dans votre navigateur (au chemin d’accès `http://localhost:3000/content/<appId>/<country>/<language>/home.html`). Si vous effectuez des modifications, la page se recharge.

Si des erreurs liées à CORS s’affiche, vous souhaiterez peut-être configurer AEM comme suit :

1. Accédez au gestionnaire de configuration (http://localhost:4502/system/console/configMgr).
1. Ouvrez la configuration pour « Adobe Granite Cross-Origin Resource Sharing Policy ».
1. Créez une configuration avec les valeurs supplémentaires suivantes :
   * Origines autorisées : http://localhost:3000
   * En-têtes pris en charge : Autorisation
   * Méthodes autorisées : OPTIONS

### test npm {#npm-test}

```shell
npm test
```

Cette commande lance le programme d’exécution du test en mode d’espion interactif. Pour plus d’informations, consultez la [documentation React sur l’exécution des tests](https://facebook.github.io/create-react-app/docs/running-tests).

### npm run build {#npm-run-build}

```shell
npm run build
```

Cette commande crée l’application pour production dans le dossier de génération. Elle place React en mode de production et optimise la génération pour des performances optimales. Pour plus d’informations, consultez la [documentation React sur le déploiement](https://facebook.github.io/create-react-app/docs/deployment).

De plus, une bibliothèque cliente AEM est générée à partir de l’application à l’aide du package [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator).

## Prise en charge des navigateurs {#browser-support}

Par défaut, ce projet utilise l’option par défaut [Browserslist](https://github.com/browserslist/browserslist) pour identifier les navigateurs cible. De plus, il inclut des polyfills pour les fonctionnalités de langage moderne afin de prendre en charge les navigateurs plus anciens (par exemple, Internet Explorer 11). Si la prise en charge de ces navigateurs n’est pas obligatoire, les dépendances de polyfills et les importations peuvent être supprimées.

## Fractionnement de code {#code-splitting}

L’application React est configurée pour utiliser le [fractionnement de code](https://webpack.js.org/guides/code-splitting) par défaut. Lors de la création de l’application pour production, le code est généré en plusieurs blocs :

```shell
$ ls build/static/js
2.5b77f553.chunk.js
2.5b77f553.chunk.js.map
main.cff1a559.chunk.js
main.cff1a559.chunk.js.map
runtime~main.a8a9905a.js
runtime~main.a8a9905a.js.map
```

Charger les blocs uniquement lorsqu’ils sont requis peut améliorer considérablement les performances de l’application.

Pour que cette fonctionnalité fonctionne avec AEM, l’application doit être en mesure d’identifier les fichiers JS et CSS à demander au code HTML généré par AEM. Pour ce faire, vous pouvez utiliser la clé « entrypoints » dans le fichier asset-manifest.json. Le fichier est analysé dans clientlib.config.js et seuls les fichiers de point d’entrée sont regroupés dans la bibliothèque cliente. Les fichiers restants sont placés dans le répertoire des ressources de la bibliothèque cliente et seront demandés dynamiquement. Ils ne seront donc chargés que lorsqu’ils seront réellement nécessaires.

Pour plus d’informations sur l’utilisation des bibliothèques clientes AEM par l’archétype du projet, consultez la [documentation générale du module ui.frontend](uifrontend.md#clientlibs).
