---
title: it.tests Module de l'archétype de projet AEM
description: Utilisation des tests d'intégration de l'archétype de projet AEM
translation-type: tm+mt
source-git-commit: 9d737b31efc8c346775ea5296f7599295af07cf1
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 46%

---


# Module it.tests de l&#39;archétype de projet AEM {#ittests-module}

Le projet comporte trois niveaux de tests :

* [Tests unitaires](core.md#unit-tests)
* Tests d’intégration
* [Tests de l’interface utilisateur](uitests.md)

Cet article décrit les tests d’intégration disponibles dans le module it.tests.

## Exécution de tests d&#39;intégration {#running-tests}

Les tests d’intégration côté serveur permettent d&#39;exécuter des tests de type unitaire dans l’environnement AEM, c’est-à-dire sur le serveur AEM. Pour lancer ce test, exécutez :

```
mvn clean verify -PintegrationTests
```