---
title: Module it.tests de l’archétype de projet AEM
description: Utilisation des tests d’intégration de l’archétype de projet AEM
feature: Composants principaux, archétype de projet AEM
role: Architect, Developer, Admin
exl-id: 0abc0265-3a3f-4323-97e6-3af0c62299ef
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 100%

---

# Module it.tests de l’archétype de projet AEM {#ittests-module}

Le projet comporte trois niveaux de tests :

* [Tests unitaires](core.md#unit-tests)
* Tests d’intégration
* [Tests de l’interface utilisateur](uitests.md)

Cet article décrit les tests d’intégration disponibles dans le module it.tests.

## Exécution des tests d’intégration {#running-tests}

Les tests d’intégration côté serveur permettent d’exécuter des tests de type unitaire dans l’environnement AEM, c’est-à-dire sur le serveur AEM. Pour lancer ce test, exécutez :

```
mvn clean verify -PintegrationTests
```
