---
title: Version frontale pour les applications monopages
description: Description du processus de génération frontale pour les projets SPA basés sur la réaction
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Version frontale pour les applications monopages {#frontend-react}

Ce document explique les détails du projet créé lors de l’utilisation de l’archétype pour créer une application d’une seule page (SPA) basée sur la structure Réagir. Par exemple, lorsque vous définissez l’ `frontendModule` option sur `react`.

## Présentation {#overview}

Ce projet a été lancé avec [create-response-app](https://github.com/facebook/create-react-app).

Cette application est créée pour consommer le modèle AEM d’un site. Il génère automatiquement la mise en page à l’aide des composants de l’aide à partir du package [@adobe/cq-response-editable-components](https://www.npmjs.com/package/@adobe/cq-react-editable-components) .

## Scripts {#scripts}

Dans le répertoire du projet, vous pouvez exécuter les commandes suivantes :

### démarrage de npm {#npm-start}

```
npm start
```

Cette commande exécute l’application en mode de développement en proxy du modèle JSON à partir d’une instance locale AEM s’exécutant sur http://localhost:4502. Cela suppose que l’ensemble du projet a été déployé sur AEM au moins une fois (`mvn clean install -PautoInstallPackage` dans la racine du projet).

Une fois l’application exécutée `npm start` dans le répertoire [ui.frontend](uifrontend.md) , elle s’ouvre automatiquement dans votre navigateur (à l’emplacement `http://localhost:3000/content/<appId>/<country>/<language>/home.html`). Si vous effectuez des modifications, la page se recharge.

Si vous recevez des erreurs liées à CORS, vous pouvez configurer AEM comme suit :

1. Accédez à Configuration Manager (http://localhost:4502/system/console/configMgr)
1. Ouvrez la configuration pour &quot;Adobe Granite Cross-Origin Resource Sharing Policy&quot;.
1. Créez une configuration avec les valeurs supplémentaires suivantes :
   * Origines autorisées : http://localhost:3000
   * En-têtes pris en charge : Autorisation
   * Méthodes autorisées : OPTIONS

### test npm {#npm-test}

```
npm test
```

Cette commande lance le programme d’exécution du test en mode de contrôle interactif. Pour plus d’informations, consultez la documentation [Réagir sur l’exécution des tests](https://facebook.github.io/create-react-app/docs/running-tests) .

### npm run build {#npm-run-build}

```
npm run build
```

Cette commande crée l’application en vue de sa production dans le dossier de création. Les lots Réagissent en mode de production et optimisent la génération pour des performances optimales. Pour plus d’informations, consultez la documentation [Réagir sur le déploiement](https://facebook.github.io/create-react-app/docs/deployment) .

De plus, une bibliothèque cliente AEM est générée à partir de l’application à l’aide du package [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator) .

## Prise en charge des navigateurs {#browser-support}

Par défaut, ce projet utilise l’option par défaut de [Browserslist](https://github.com/browserslist/browserslist)pour identifier les navigateurs cibles. De plus, il inclut des remplissages polyvalents pour les fonctionnalités de langue moderne afin de prendre en charge les anciens navigateurs (par exemple, Internet Explorer 11). Si la prise en charge de ces navigateurs n’est pas obligatoire, les dépendances de polyremplissage et les importations peuvent être supprimées.

## Fractionnement du code {#code-splitting}

L’application Réagir est configurée pour utiliser le fractionnement [du](https://webpack.js.org/guides/code-splitting) code par défaut. Lors de la création de l’application pour production, le code est généré en plusieurs blocs :

```
$ ls build/static/js
2.5b77f553.chunk.js
2.5b77f553.chunk.js.map
main.cff1a559.chunk.js
main.cff1a559.chunk.js.map
runtime~main.a8a9905a.js
runtime~main.a8a9905a.js.map
```

Le chargement des blocs uniquement lorsqu’ils sont requis peut améliorer considérablement les performances de l’application.

Pour que cette fonctionnalité fonctionne avec AEM, l’application doit être en mesure d’identifier les fichiers JS et CSS à demander au code HTML généré par AEM. Pour ce faire, vous pouvez utiliser la clé &quot;entrypoints&quot; dans le fichier asset-manifest.json. Le fichier est analysé dans clientlib.config.js et seuls les fichiers d’entrée sont regroupés dans ClientLib. Les fichiers restants sont placés dans le répertoire des ressources de ClientLib et seront demandés dynamiquement. Ils ne seront donc chargés que lorsqu’ils sont réellement nécessaires.

Pour plus d’informations sur la manière dont AEM ClientLibs est utilisé par l’archétype du projet, consultez la documentation [générale du module](uifrontend.md#clientlibs) ui.frontend.
