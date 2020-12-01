---
title: Module ui.tests de l’archétype de projet AEM
description: Utilisation des tests JUnit de l’archétype de projet AEM
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 100%

---


# Module ui.tests de l’archétype de projet AEM {#uitests-module}

Le projet comporte trois niveaux de tests :

## Tests unitaires {#unit-tests}

Le test unitaire dans le [module principal](core.md) comprend les tests unitaires classiques du code contenu dans le lot. Pour lancer ce test, exécutez :

```
mvn clean test
```

## Tests d’intégration {#integration-tests}

Les tests d’intégration côté serveur permettent d&#39;exécuter des tests de type unitaire dans l’environnement AEM, c’est-à-dire sur le serveur AEM. Pour lancer ce test, exécutez :

```
mvn clean verify -PintegrationTests
```

## Tests côté client {#client-side-tests}

Les tests `client-side Hobbes.js` sont des tests JavaScript côté navigateur qui vérifient le comportement côté navigateur.

Pour effectuer les tests, lorsque vous affichez une page AEM que vous souhaitez tester dans le navigateur, ouvrez la page en **mode développeur** en ouvrant le panneau de gauche, passez à l’onglet **Tests**, recherchez les **tests MonNom** générés et exécutez-les.
