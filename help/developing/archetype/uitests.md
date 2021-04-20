---
title: Module ui.tests de l’archétype de projet AEM
description: Utilisation des tests d’interface utilisateur de l’archétype de projet AEM
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Administrator
translation-type: ht
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: ht
source-wordcount: '120'
ht-degree: 100%

---


# Module ui.tests de l’archétype de projet AEM {#uitests-module}

Le projet comporte trois niveaux de tests :

* [Tests unitaires](core.md#unit-tests)
* [Tests d’intégration](ittests.md)
* Tests de l’interface utilisateur

Cet article décrit les tests de l’interface utilisateur disponibles dans le module ui.tests.

## Exécution des tests d’interface utilisateur {#running-tests}

Pour lancer ce test, exécutez :

```shell
mvn verify -Pui-tests-local-execution
```

Après exécution, les rapports et les journaux sont disponibles dans le dossier `target/reports`.

## Options supplémentaires {#additional-options}

Les tests de l’interface utilisateur peuvent être exécutés avec de nombreuses options différentes, notamment pour les tests découplés sur un navigateur local et en tant qu’image Docker. Consultez le [fichier README.md du module ui.tests](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/ui.tests) pour plus d’informations.
