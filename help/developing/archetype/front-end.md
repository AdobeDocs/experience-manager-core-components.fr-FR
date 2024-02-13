---
title: Développement front-end avec l’archétype de projet AEM
description: Découvrez le mécanisme de génération front-end facultatif et dédié de l’archétype de projet AEM basé sur Webpack.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 99132b49-bd06-4ac2-9348-12c0dfdfe8b2
source-git-commit: bd92a5d1884056ca7b44ea28e5817d8bde10a4d9
workflow-type: ht
source-wordcount: '654'
ht-degree: 100%

---


# Développement front-end avec l’archétype de projet AEM {#front-end}

L’archétype de projet AEM comprend un mécanisme de génération front-end dédié et facultatif basé sur Webpack. Ainsi, le module ui.frontend devient l’emplacement central de toutes les ressources front-end du projet, y compris les fichiers JavaScript et CSS. Pour tirer pleinement parti de cette fonctionnalité utile et flexible, il est essentiel de savoir comment le développement front-end s’intègre à un projet AEM.

Ce document se concentre sur les schémas d’utilisation généraux du module de génération front-end et sur ce qu’il fait pour vous. Pour obtenir des instructions techniques et des options de génération détaillées, consultez la documentation du référentiel GitHub de l’archétype.

>[!TIP]
>
>Le dernier archétype de projet AEM, ainsi que la documentation technique complète, [sont disponibles sur GitHub](https://github.com/adobe/aem-project-archetype).

## Développement front-end et back-end d’AEM {#front-end-back-end}

En termes beaucoup plus simples, les projets AEM peuvent être considérés comme comprenant deux parties distinctes, mais connexes :

* Développement principal générant la logique d’AEM et créant des bibliothèques Java, des services OSGi, etc.
* Développement front-end permettant de gérer la présentation et le comportement du site Web obtenu, et de créer des bibliothèques JavaScript et CSS

Ces deux processus de développement étant axés sur différentes parties du projet, les développements front-end et back-end peuvent être réalisés en parallèle.

![diagramme de workflow front-end](/help/assets/front-end-flow.png)

Toutefois, le projet obtenu doit utiliser les résultats de ces deux processus de développement, à savoir les développements front-end et back-end.

## Définition du balisage {#determining-markup}

Quel que soit le workflow front-end que vous décidez de mettre en œuvre pour votre projet, les développeurs front-end et back-end doivent avant tout s’entendre sur le balisage. En règle générale, AEM définit le balisage que les principaux composants fournissent. [Vous pouvez toutefois le personnaliser, le cas échéant](/help/developing/customizing.md#customizing-the-markup).

## Workflows front-end possibles {#possible-workflows}

Le module de génération front-end est un outil utile et très flexible, mais n’impose aucun avis en particulier sur la manière dont il doit être utilisé. Vous trouverez ci-dessous deux exemples d’utilisation *possibles*, mais les besoins à satisfaire pour votre projet personnel peuvent exiger d’autres modèles d’utilisation.

### Utilisation du serveur de développement statique Webpack {#using-webpack}

Grâce à Webpack, vous pouvez mettre en forme et développer vos contenus selon les résultats statiques des pages Web AEM dans le module ui.frontend.

1. Aperçu de la page dans AEM à l’aide du mode d’aperçu de page ou transmission `wcmmode=disabled` de l’URL
1. Affichage de la source de la page et enregistrement au format HTML statique dans le module ui.frontend
1. [Lancez Webpack](#webpack-dev-server), puis commencez à mettre en forme et à générer les codes JavaScript et CSS requis.
1. Exécutez `npm run dev` pour générer les bibliothèques client.

Dans ce processus, un développeur AEM peut exécuter les première et deuxième étapes, puis transmettre le code HTML statique au développeur front-end qui se développe selon les résultats HTML AEM.

>[!TIP]
>
>Vous pouvez également tirer parti de la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_fr) pour obtenir des exemples de résultats de balisage de chaque composant pour travailler sur le composant au lieu de la page.

### Utilisation de Storybook {#using-storybook}

Avec [Storybook](https://storybook.js.org), vous pouvez effectuer un développement front-end plus important. Même s&#39;il ne fait pas partie de l’archétype de projet AEM, vous pouvez installer Storybook et stocker vos artefacts dans le module ui.frontend. Il est possible de les déployer en tant que bibliothèques client une fois prêts pour les tests dans AEM en exécutant `npm run dev`.

>[!NOTE]
>
>[Storybook](https://storybook.js.org) n’est pas fourni dans l’archétype de projet AEM. Si vous choisissez de l’utiliser, vous devez l’installer séparément.

## Vue d’ensemble des bibliothèques clientes {#clientlibs}

Le module front-end est rendu disponible à l’aide d’une [bibliothèque cliente AEM.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html?lang=fr-FR). Lors de l’exécution du script de génération NPM, l’application est créée et le package `aem-clientlib-generator` récupère le résultat de la génération pour le transformer en une bibliothèque cliente de ce type.

Une bibliothèque cliente se compose des fichiers et répertoires suivants :

* `css/` : fichiers CSS pouvant être demandés dans le code HTML.
* `css.txt` : indique à AEM l’ordre et le nom des fichiers dans `css/` afin qu’ils puissent être fusionnés.
* `js/` : fichiers JavaScript pouvant être demandés dans le code HTML.
* `js.txt` : indique à AEM l’ordre et le nom des fichiers dans `js/` afin qu’ils puissent être fusionnés.
* `resources/` : cartes source, blocs de code autres que les points d’entrée (résultant du fractionnement de code), ressources statiques (par exemple, icônes), etc.

>[!TIP]
>
>En savoir plus sur la manière dont AEM gère les bibliothèques clientes dans la section [Documentation sur le développement d’AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html?lang=fr-FR) et sur la manière de les inclure dans la [Documentation sur les composants principaux](/help/developing/including-clientlibs.md).
