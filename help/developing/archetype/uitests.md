---
title: module ui.tests de l’archétype du projet AEM
description: Utilisation des tests JUnit de l’archétype de projet AEM
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# ui.tests Module of the AEM Project Archetype {#uitests-module}

Le projet comporte trois niveaux de tests :

## Tests unitaires {#unit-tests}

The unit test in the [core module](core.md) showcases classic unit testing of the code contained in the bundle. Pour lancer ce test, exécutez :

```
mvn clean test
```

## Tests d’intégration {#integration-tests}

Les tests d’intégration côté serveur permettent d’exécuter des tests de type unité dans l’environnement AEM, c’est-à-dire sur le serveur AEM. Pour lancer ce test, exécutez :

```
mvn clean verify -PintegrationTests
```

## Tests côté client {#client-side-tests}

Les `client-side Hobbes.js` tests sont des tests JavaScript côté navigateur qui vérifient le comportement côté navigateur.

Pour tester, lorsque vous affichez une page AEM que vous souhaitez tester dans le navigateur, ouvrez la page en mode **** Développeur en ouvrant le panneau de gauche et passez à l’onglet **Tests** et recherchez les tests **** Monnom générés et exécutez-les.
