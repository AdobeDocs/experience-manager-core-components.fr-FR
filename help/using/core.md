---
title: Module principal de l’archétype de projet AEM
seo-title: Module principal de l’archétype de projet AEM
description: Module principal de l’archétype de projet AEM
seo-description: Module principal de l’archétype de projet AEM
contentOwner: bohnert
content-type: référence
topic-tags: core-components
translation-type: ht
source-git-commit: 683b4f4705c226275439a408423cbf1b23bea66f

---


# Module principal de l’archétype de projet AEM {#core-module}

Le module Maven principal (`<src-directory>/<project>/core`) comprend tout le code Java nécessaire à l’implémentation. Le module compresse l’ensemble du code Java et le déploie vers l’instance AEM en tant que lot OSGi.

Le plug-in Maven Bundle défini dans le fichier `<src-directory>/<project>/core/pom.xml` a pour tâche de compiler le code Java dans un lot OSGi pouvant être reconnu par le conteneur OSGi d’AEM. Notez qu’il s’agit de l’endroit où l’emplacement des modèles Sling est défini.

Bien qu’il soit rare que le lot principal doive être déployé indépendamment du module ui.apps dans les environnements de niveau supérieur, le déploiement direct du lot principal est utile lors du développement/test local. Le plug-in Maven Sling permet au lot principal d’être déployé vers AEM en exploitant directement le profil `autoInstallBundle` tel que défini dans le [fichier POM parent](overview.md#parent-pom).

```
mvn -PautoInstallBundle clean install
```

Une fois l’exécution terminée, vous devriez pouvoir voir la console des lots à l’adresse `http://<host>:<port>/system/console/bundles`.
