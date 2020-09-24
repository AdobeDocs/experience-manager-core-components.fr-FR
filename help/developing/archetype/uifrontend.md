---
title: Version front-end de l’archétype de projet AEM
description: Modèle de projet pour les applications basées sur AEM
translation-type: tm+mt
source-git-commit: d8503d92c2d4948e54b2ad7d5407e4c7c98ebf83
workflow-type: tm+mt
source-wordcount: '1621'
ht-degree: 98%

---


# Module ui.frontend de l’archétype de projet AEM {#uifrontend-module}

L’archétype de projet AEM comprend un mécanisme de génération front-end dédié et facultatif basé sur Webpack. Ainsi, le module ui.frontend devient l’emplacement central de toutes les ressources front-end du projet, y compris les fichiers JavaScript et CSS. Pour tirer pleinement parti de cette fonctionnalité utile et flexible, il est essentiel de savoir comment le développement front-end s’intègre à un projet AEM.

## Projets AEM et développement front-end{#aem-and-front-end-development}

En termes beaucoup plus simples, les projets AEM peuvent être considérés comme comprenant deux parties distinctes, mais connexes :

* Développement principal générant la logique d’AEM et créant des bibliothèques Java, des services OSGi, etc.
* Développement front-end permettant de gérer la présentation et le comportement du site Web obtenu, et de créer des bibliothèques JavaScript et CSS

Ces deux processus de développement étant axés sur différentes parties du projet, les développements front-end et back-end peuvent être réalisés en parallèle.

![diagramme de workflow front-end](/help/assets/front-end-flow.png)

Toutefois, le projet obtenu doit utiliser les résultats de ces deux processus de développement, à savoir les développements front-end et back-end.

L’exécution de `npm run dev` permet de lancer le processus de génération front-end, qui rassemble les fichiers JavaScript et CSS stockés dans le module ui.frontend et qui crée deux bibliothèques clientes minifield, `clientlib-site` et `clientlib-dependencies`, et de les déposer dans le module ui.apps. Il est possible de déployer les bibliothèques clientes vers AEM. Ainsi, vous pouvez stocker votre code côté client dans le référentiel.

Si l’archétype complet de projet AEM est exécuté avec `mvn clean install -PautoInstallPackage` tous les artefacts de projet, y compris les bibliothèques clientes, sont ensuite transmis à l’instance AEM.

>[!TIP]
>
>Découvrez comment AEM gère les bibliothèques client dans la documentation [de développement](https://docs.adobe.com/content/help/en/experience-manager-65/developing/introduction/clientlibs.html)AEM, comment les [inclure](/help/developing/including-clientlibs.md)[ou comment le module ui.frontend les utilise.](#clientlib-generation)

## Présentation des bibliothèques clientes {#clientlibs}

Le module front-end est rendu disponible à l’aide d’une [bibliothèque cliente AEM](https://helpx.adobe.com/fr/experience-manager/6-5/sites/developing/using/clientlibs.html). Lors de l’exécution du script de génération NPM, l’application est créée et le package aem-clientlib-generator récupère le résultat de la génération et le transforme en une bibliothèque cliente de ce type.

Une bibliothèque cliente se compose des fichiers et répertoires suivants :

* `css/` : fichiers CSS pouvant être demandés dans le code HTML.
* `css.txt` : indique à AEM l’ordre et le nom des fichiers dans `css/` afin qu’ils puissent être fusionnés.
* `js/` : fichiers JavaScript pouvant être demandés dans le code HTML.
* `js.txt` : indique à AEM l’ordre et le nom des fichiers dans `js/` afin qu’ils puissent être fusionnés.
* `resources/` : cartes source, blocs de code autres que les points d’entrée (résultant du fractionnement de code), ressources statiques (par exemple, icônes), etc.

## Workflows front-end possibles {#possible-workflows}

Le module de génération front-end est un outil utile et très flexible, mais n&#39;impose aucun avis en particulier sur la manière dont il doit être utilisé. Vous trouverez ci-dessous deux exemples d’utilisation *possibles*, mais les besoins à satisfaire pour votre projet personnel peuvent exiger d’autres modèles d’utilisation.

### Utilisation du serveur de développement statique Webpack {#using-webpack}

Grâce à Webpack, vous pouvez mettre en forme et développer vos contenus selon les résultats statiques des pages Web AEM dans le module ui.frontend.

1. Aperçu de la page dans AEM à l’aide du mode d’aperçu de page ou transmission `wcmmode=disabled` de l’URL
1. Affichage de la source de la page et enregistrement au format HTML statique dans le module ui.frontend
1. [Lancez Webpack](#webpack-dev-server), puis commencez à mettre en forme et à générer les codes JavaScript et CSS requis.
1. Exécutez `npm run dev` pour générer les bibliothèques clientes.

Dans ce processus, un développeur AEM peut exécuter les première et deuxième étapes, puis transmettre le code HTML statique au développeur front-end qui se développe selon les résultats HTML AEM.

>[!TIP]
>
>Vous pouvez également tirer parti de la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library) pour obtenir des exemples de résultats de balisage de chaque composant pour travailler sur le composant au lieu de la page.

### Utilisation de Storybook {#using-storybook}

Avec [Storybook](https://storybook.js.org), vous pouvez effectuer un développement front-end plus important. Même s&#39;il ne fait pas partie de l’archétype de projet AEM, vous pouvez installer Storybook et stocker vos artefacts dans le module ui.frontend. Il est possible de les déployer en tant que bibliothèques clientes une fois prêts pour les tests dans AEM en exécutant `npm run dev`.

>[!NOTE]
>
>[Storybook](https://storybook.js.org) n’est pas fourni dans l’archétype de projet AEM. Si vous choisissez de l’utiliser, vous devez l’installer séparément.

### Définition du balisage {#determining-markup}

Quel que soit le workflow front-end que vous décidez de mettre en œuvre pour votre projet, les développeurs front-end et back-end doivent avant tout s’entendre sur le balisage. En règle générale, AEM définit le balisage que les principaux composants fournissent. [Vous pouvez toutefois le personnaliser, le cas échéant](/help/developing/customizing.md#customizing-the-markup).

## Le module ui.frontend {#ui-frontend-module}

L’archétype de projet AEM comprend un mécanisme de génération front-end dédié facultatif basé sur Webpack avec les fonctionnalités suivantes.

* Prise en charge complète de TypeScript, ES6 et ES5 (et des enveloppes Webpack applicables)
* Peluchage TypeScript et JavaScript à l’aide d&#39;un jeu de règles TSLint
* Sortie ES5 pour la prise en charge des navigateurs hérités
* Extension métacaractère
   * Inutile d&#39;ajouter des importations
   * Tous les fichiers JS et CSS peuvent désormais être ajoutés à chaque composant.
      * Les meilleures pratiques figurent sous `/clientlib/js`, `/clientlib/css` ou `/clientlib/scss`.
   * Aucun fichier `.content.xml` ou `js.txt`/`css.txt` n’est requis, car tous les éléments sont exécutés via Webpack.
   * Extraction de tous les fichiers JS par l’application globale sous le dossier `/component/`.
      * Webpack permet aux fichiers CSS/SCSS d’être liés via des fichiers JS.
      * Ces fichiers sont extraits via les deux points d&#39;entrée `sites.js` et `vendors.js`.
   * Les seuls fichiers consommés par AEM sont les fichiers de sortie `site.js` et `site.css` dans `/clientlib-site`, ainsi que `dependencies.js` et `dependencies.css` dans `/clientlib-dependencies`
* Blocs
   * Principal (js/css de site)
   * Fournisseurs (js/css de dépendances)
* Prise en charge complète de Sass/Scss (Sass est compilé dans CSS via Webpack)
* Serveur de développement Webpack statique avec proxy intégré utilisé pour une instance locale AEM

>[!NOTE]
>
>Pour plus d’informations d’ordre technique sur le module ui.frontend, consultez la [documentation sur GitHub](https://github.com/adobe/aem-project-archetype/blob/master/src/main/archetype/ui.frontend.general/README.md).

## Installation {#installation}

1. Installez globalement [NodeJS](https://nodejs.org/en/download/) (v10+). Cela installera également npm.
1. Accédez à ui.frontend dans votre projet et exécutez `npm install`.

>[!NOTE]
>
>Vous devez avoir [exécuté l’archétype](overview.md) avec l’option `-DoptionIncludeFrontendModule=y` pour renseigner le dossier ui.frontend.

## Utilisation {#usage}

Les scripts npm suivants orientent le workflow front-end :

* `npm run dev` : version complète avec optimisation JS désactivée (shaking d’arborescence, etc.), cartes source activées et optimisation CSS désactivée.
* `npm run prod` : version complète avec optimisation JS activée (shaking d’arborescence, etc.), cartes source désactivées et optimisation CSS activée.
* `npm run start` :- Démarre un serveur de développement Webpack statique à des fins de développement local et avec une dépendance minimale d’AEM.

## Sortie {#output}

Le module ui.frontend compile le code sous le dossier `ui.frontend/src` et génère les fichiers CSS et JS compilés, ainsi que les ressources sous un dossier dénommé `ui.frontend/dist`.

* **Site** : `site.js`, `site.css` et un dossier `resources/` correspondant aux images et polices dépendantes de la disposition sont créés dans un dossier `dist/`clientlib-site.
* **Dépendances ** : `dependencies.js` et `dependencies.css` sont créés dans un dossier `dist/clientlib-dependencies`.

### JavaScript {#javascript}

* Optimisation : pour les versions de production, tous les JS qui ne sont pas utilisés ou appelés sont supprimés.

### CSS {#css}

* Indexation automatique : toutes les feuilles de style CSS sont exécutées via un pré-indexeur et les propriétés nécessitant une pré-indexation sont automatiquement ajoutées dans les feuilles de style CSS.
* Optimisation : lors de la publication, toutes les feuilles de style CSS sont exécutées via un optimiseur (cssnano) qui les normalise selon les règles par défaut suivantes :
   * Réduit l’expression calc CSS chaque fois que possible, assurant à la fois la compatibilité du navigateur et la compression.
Convertit entre des valeurs équivalentes de longueur, de temps et d’angle. Notez que, par défaut, les valeurs de longueur ne sont pas converties.
   * Supprime les commentaires dans les règles, les sélecteurs et les déclarations et autour de ceux-ci.
   * Supprime les doublons de règles, de règles at et de déclarations.
      * Notez que cela ne fonctionne que pour les doublons exacts.
   * Supprime les règles vides, les requêtes multimédias et les règles ayant des sélecteurs vides, car elles n’affectent pas la sortie.
   * Fusionne les règles adjacentes par sélecteurs et paires propriété/valeur se chevauchant.
   * Garantit qu’un seul @charset est présent dans le fichier CSS et le déplace en haut du document.
   * Remplace le mot-clé initial CSS par la valeur réelle, lorsque la sortie obtenue est plus petite.
   * Compresse les définitions SVG en ligne avec SVGO.
* Nettoyage : comprend une tâche de nettoyage explicite pour effacer à la demande les fichiers CSS, JS et Map générés.
* Mappage de source : version de développement uniquement

>[!NOTE]
>
>L’option de version front-end utilise des fichiers de configuration Webpack uniquement destinés au développement et à la production qui partagent un fichier de configuration commun. Les paramètres de développement et de production peuvent ainsi être modifiés indépendamment.

### Génération de bibliothèques clientes {#clientlib-generation}

Le processus de génération du module ui.frontend tire parti du plug-in [aem-clientlib-generator](https://www.npmjs.com/package/aem-clientlib-generator) pour déplacer les fichiers CSS et JavaScript compilés, ainsi que les ressources utilisées dans le module ui.apps. La configuration aem-clientlib-generator est définie dans `clientlib.config.js`. Les bibliothèques clientes suivantes sont générées :

* **clientlib-site** - `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-site`
* **clientlib-dependencies** - `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-dependencies`

### Ajout de bibliothèques clientes aux pages {#clientlib-inclusion}

Les catégories `clientlib-site` et `clientlib-dependencies` sont ajoutées aux pages via la [configuration Règles de page](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/templates/page-templates-editable.html#template-definitions) dans le modèle par défaut. Pour afficher les règles, modifiez la ligne de commande **Modèle de page de contenu > Informations de page > Règles de page**.

L’ajout final de bibliothèques clientes à la page des sites se présente comme suit :

```
<HTML>
    <head>
        <link rel="stylesheet" href="clientlib-base.css" type="text/css">
        <script type="text/javascript" src="clientlib-dependencies.js"></script>
        <link rel="stylesheet" href="clientlib-dependencies.css" type="text/css">
        <link rel="stylesheet" href="clientlib-site.css" type="text/css">
    </head>
    <body>
        ....
        <script type="text/javascript" src="clientlib-site.js"></script>
        <script type="text/javascript" src="clientlib-base.js"></script>
    </body>
</HTML>
```

Vous pouvez naturellement modifier cet ajout en mettant à jour les règles de page ou en modifiant les catégories, et incorporer les propriétés des bibliothèques clientes concernées.

### Serveur de développement Webpack statique {#webpack-dev-server}

Le module ui.frontend comprend un serveur webpack-dev-server qui assure le rechargement en direct pour réaliser un développement front-end rapide en dehors d’AEM. La configuration tire parti du plug-in html-webpack-plugin pour intégrer automatiquement les fichiers CSS et JavaScript compilés à partir du module ui.frontend dans un modèle HTML statique.

#### Fichier important {#important-files}

* `ui.frontend/webpack.dev.js`
   * Contient la configuration utilisée pour webpack-dev-server et pointe vers le modèle HTML à employer.
   * Il comprend également une configuration proxy utilisée pour une instance AEM s’exécutant sur localhost:4502.
* `ui.frontend/src/main/webpack/static/index.html`
   * Il s’agit du code HTML statique sur lequel le serveur est exécuté.
   * Ainsi, les développeurs peuvent modifier les fichiers CSS et JavaScript, et voir ces modifications répercutées immédiatement dans le balisage.
   * On suppose que le balisage stocké dans ce fichier reproduit fidèlement le balisage généré par les composants AEM.
   * Le balisage de ce fichier n’est pas synchronisé automatiquement avec le balisage du composant AEM.
   * Ce fichier comporte également des références aux bibliothèques clientes stockées dans AEM, comme Core Component CSS et Responsive Grid CSS.
   * Le serveur de développement Webpack est configuré pour remplacer les fichiers CSS et JavaScript ajoutés depuis une instance locale AEM en cours d’exécution, selon la configuration disponible dans `ui.frontend/webpack.dev.js`.

#### Utilisation de {#using-webpack-server}

1. Exécutez la commande `mvn -PautoInstallSinglePackage clean install` depuis la racine du projet pour l’installer dans son intégralité sur une instance AEM s’exécutant sur `localhost:4502`.
1. Naviguez dans le dossier `ui.frontend`.
1. Exécutez la commande suivante `npm run start` pour démarrer le serveur de développement Webpack. Une page de navigateur (`localhost:8080` ou le port disponible suivant) doit s’ouvrir.

Vous pouvez désormais modifier les fichiers CSS, JS, SCSS et TS, et voir ces modifications répercutées immédiatement sur le serveur de développement Webpack.
