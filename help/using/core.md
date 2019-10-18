---
title: Module principal de l’archétype du projet AEM
seo-title: Module principal de l’archétype du projet AEM
description: Module principal de l’archétype du projet AEM
seo-description: Module principal de l’archétype du projet AEM
contentOwner: bohnert
content-type: référence
topic-tags: core-components
translation-type: tm+mt
source-git-commit: 683b4f4705c226275439a408423cbf1b23bea66f

---


# Module principal de l’archétype du projet AEM {#core-module}

Le module principal Maven (`<src-directory>/<project>/core`) comprend tout le code Java nécessaire à l’implémentation. Le module compresse l’ensemble du code Java et le déploie sur l’instance AEM en tant que lot OSGi.

Le module externe Maven Bundle défini dans le `<src-directory>/<project>/core/pom.xml` est responsable de la compilation du code Java dans un lot OSGi qui peut être reconnu par le conteneur OSGi d’AEM. Notez que c’est là que l’emplacement des modèles Sling est défini.

Bien qu’il soit rare que le lot principal doive être déployé indépendamment du module ui.apps dans les environnements de niveau supérieur, le déploiement direct du lot principal est utile lors du développement/test local. Le module externe Maven Sling permet au lot principal d’être déployé dans AEM en exploitant directement le `autoInstallBundle` profil défini dans le POM [](overview.md#parent-pom)parent.

```
mvn -PautoInstallBundle clean install
```

Une fois l’exécution terminée, vous devriez pouvoir voir la console des offres groupées à l’adresse `http://<host>:<port>/system/console/bundles`.
