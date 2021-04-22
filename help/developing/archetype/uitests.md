---
title: Module ui.tests de l’archétype de projet AEM
description: Utilisation des tests d’interface utilisateur de l’archétype de projet AEM
feature: Composants principaux, archétype de projet AEM
role: Architect, Developer, Administrator
exl-id: eb3c9b34-f10e-410f-bcf3-34f94f124c7c
translation-type: ht
source-git-commit: 8ff36ca143af9496f988b1ca65475497181def1d
workflow-type: ht
source-wordcount: '117'
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
