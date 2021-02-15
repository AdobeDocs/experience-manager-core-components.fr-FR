---
title: Module principal de l’archétype de projet AEM
description: Module principal de l’archétype de projet AEM
translation-type: tm+mt
source-git-commit: 9d737b31efc8c346775ea5296f7599295af07cf1
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 100%

---


# Module principal de l’archétype de projet AEM {#core-module}

Le module Maven principal (`<src-directory>/<project>/core`) comprend tout le code Java nécessaire à l’implémentation. Le module compresse l’ensemble du code Java et le déploie vers l’instance AEM en tant que lot OSGi.

Le plug-in Maven Bundle défini dans le fichier `<src-directory>/<project>/core/pom.xml` a pour tâche de compiler le code Java dans un lot OSGi pouvant être reconnu par le conteneur OSGi d’AEM. Notez qu’il s’agit de l’endroit où l’emplacement des modèles Sling est défini.

Bien qu’il soit rare que le lot principal doive être déployé indépendamment du module ui.apps dans les environnements de niveau supérieur, le déploiement direct du lot principal est utile lors du développement/test local. Le plug-in Maven Sling permet au lot principal d’être déployé vers AEM en exploitant directement le profil `autoInstallBundle` tel que défini dans le [fichier POM parent](/help/developing/archetype/using.md#parent-pom).

```shell
mvn -PautoInstallBundle clean install
```

Une fois l’exécution terminée, vous devriez pouvoir visualiser la console des lots à l’adresse `http://<host>:<port>/system/console/bundles`.

##  Tests unitaires {#unit-tests}

Le test unitaire dans le module principal comprend les tests unitaires classiques du code contenu dans le lot. Pour lancer ce test, exécutez :

```shell
mvn clean test
```
