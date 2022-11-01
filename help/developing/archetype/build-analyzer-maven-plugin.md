---
title: Plug-in Maven Build Analyzer du SDK AEM as a Cloud Service
description: Documentation du plug-in local Maven Build Analyzer
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: de26b310-a294-42d6-a0db-91f6036a328c
source-git-commit: 60ec9c1643abce0ee75da5368269928476390440
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 92%

---

# Plug-in Maven Build Analyzer du SDK AEM as a Cloud Service {#maven-analyzer-plugin}

Le plug-in Maven Build Analyzer du SDK AEM as a Cloud Service analyse la structure des différents projets de packages de contenu.

Consultez la [documentation du plug-in Maven](https://github.com/adobe/aemanalyser-maven-plugin/blob/main/aemanalyser-maven-plugin/README.md) pour savoir comment l’inclure dans un projet Maven AEM.

>[!NOTE]
>
>Il est recommandé de mettre à jour votre projet Maven pour référencer la dernière version du plug-in du référentiel central Maven, à cet emplacement : https://repo1.maven.org/maven2/com/adobe/aem/aemanalyser-maven-plugin/

Le plug-in utilise le dernier SDK disponible plutôt que celui configuré dans le projet.

Vous trouverez ci-dessous un tableau décrivant les analyseurs exécutés au cours de cette étape. <!-- Note that some are executed in the local SDK, while others are only executed during the Cloud Manager pipeline deployment. -->

| Module | Fonction, exemple et dépannage | SDK local | Cloud Manager |
|---|---|---|---|
| `api-regions-exportsimports` | Vérifie si les déclarations Import-Package de tous les lots OSGI sont satisfaites par la déclaration Export-package d’autres lots inclus dans le projet Maven. Une erreur se présenterait comme suit : <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is importing package(s) org.acme.foo in start level 20 but no bundle is exporting these for that start level.`<p> </p>Pour résoudre les problèmes, vérifiez si le lot contenant le package est inclus dans le déploiement ou examinez le manifeste du lot que vous prévoyez d’exporter pour déterminer si un nom incorrect ou une version erronée a été utilisé. | Oui | Oui |
| `bundle-unversioned-packages` | Vérifie si les lots OSGi spécifient une version avec une déclaration Export-Package et une plage de versions avec une déclaration Import-Package. Une erreur se présenterait comme suit : <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is exporting package org.acme.foo without a version.`<p> </p>Pour résoudre le problème, veillez à ajouter une `package-info.java` à ce package spécifiant la version à exporter. | Oui | Oui |
| `requirements-capabilities` | Vérifie si toutes les déclarations d’exigences faites dans les lots OSGI sont satisfaites par les déclarations de capacités d’autres lots inclus dans le projet Maven. Une erreur se présenterait comme suit : <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Artifact org.acme:mybundle:0.0.1-SNAPSHOT requires org.foo.bar in start level 20 but no artifact is providing a matching capability in this start level.`<p> </p> Pour résoudre les problèmes, vérifiez le manifeste du lot censé contenir une déclaration de capacité afin de déterminer pourquoi elle n’y figure pas ou examinez le manifeste du lot requis pour vérifier que l’exigence qu’il contient est correcte. | Oui | Oui |
| `bundle-content` | Émet un avertissement si un lot contient le contenu initial spécifié avec Sling-Initial-Content, ce qui pose problème dans l’environnement organisé en grappes d’AEM as a Cloud Service. L’avertissement ressemble à ceci : <p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found initial content : [/]` <p> </p>Pour résoudre les problèmes de conversion du contenu initial en instructions repoinit, voir la documentation relative à la fonction RepoInit. | Oui | Oui |
| `bundle-resources` | Émet un avertissement si un lot contient des ressources spécifiées avec l’en-tête Sling-Bundle-Resources, ce qui pose problème dans l’environnement organisé en grappes d’AEM as a Cloud Service. L’avertissement ressemble à ceci :<p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found bundle resources : [/libs/sling/explorer!/resources/explorer]`<p> </p> Pour résoudre les problèmes de conversion des ressources en instructions repoinit, voir la [Documentation RepoInit](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=fr#repo-init). | Oui | Oui |
| `api-regions`<p> </p>`api-regions-check-order`<p> </p>`api-regions-dependencies`<p> </p>`api-regions-duplicates` | Ces analyseurs vérifient certains détails relatifs au [processus de conversion de package de contenu en modèle de fonctionnalité](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=fr#deploying) qui crée des artefacts conformes au modèle de fonctionnalité Sling. Toute erreur doit être signalée au service clientèle d’Adobe. | Oui | Oui |
| `api-regions-crossfeature-dups` | Vérifie que les lots OSGI des clients ne comportent pas de déclarations Export-package qui remplacent l’API publique d’AEM as a Cloud Service<p> </p>`[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Package overlap found between region global and bundle org.acme:mybundle:0.0.1.SNAPSHOT which comes from feature: [org.acme:myproject.analyse:slingosgifeature:0.0.1-SNAPSHOT]. Both export package: com.day.util`<p> </p>Pour résoudre ce problème, arrêtez l’exportation d’un package faisant partie de l’API publique d’AEM. | Oui | Oui |
| `repoinit` | Vérifiez la syntaxe de toutes les sections de redirection. | Oui | Oui |
| `bundle-nativecode` | Vérifie que les lots OSGI n’installent pas de code natif. | Oui | Oui |
| `configuration-api` | Valide les configurations OSGi importantes. <p> </p> `Configuration org.apache.felix.webconsole.internal.servlet.OsgiManager: Configuration is not allowed (com.mysite:mysite.all:1.0.0-SNAPSHOT\|com.mysite:mysite.ui.config:1.0.0-SNAPSHOT)` | Oui | Oui |
| `region-deprecated-api` | Vérifie si une [API obsolète](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-apis.html?lang=fr) est utilisée. <p> </p>`[WARNING] com.mysite:mysite.core:1.0.0-SNAPSHOT: Usage of deprecated package found : org.apache.sling.settings : Avoid these features at runtime: run modes, file system access (com.mysite:mysite.all:1.0.0-SNAPSHOT)` | Oui | Oui |
| `artifact-rules` | Valide les dépendances comme les lots et les packages de contenu pour éviter les problèmes connus dans les artefacts.<p> </p>`[WARNING] [artifact-rules] com.adobe.acs:acs-aem-commons-bundle:5.0.4: Use at least version 5.0.10 (com.mysite:mysite.all:1.0.0-SNAPSHOT)` | Oui | Oui |
| `aem-env-var` | Vérifie l’utilisation des variables d’environnement en fonction de la variable [guide de dénomination de variable](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#variable-naming)<p> </p>`[ERROR] Configuration org.apache.felix.webconsole.internal.servlet.OsgiManager: Value for property 'port' must not use env vars prefixed with INTERNAL_ or ADOBE_ (com.mysite1:my-site-1.all:1.0.0-SNAPSHOT\|com.mysite1:my-site-1.ui.config:1.0.0-SNAPSHOT)` | Oui | Oui |
| `content-package-validation` | Exécute les validateurs filevault. Par défaut, jackrabbit-docviewparser est activé, pour vérifier la syntaxe de contenu bien formée du xml dans les modules qui seront installés pendant le déploiement.<p> </p>`[main] WARN org.apache.sling.feature.analyser.task.impl.CheckContentPackages - ValidationViolation: "jackrabbit-docviewparser: Invalid XML found: The reference to entity "se" must end with the ';' delimiter.", filePath=jcr_root/apps/somename/configs/com.adobe.test.Invalid.xml, nodePath=/apps/somename/configs/com.adobe.test.Invalid`<p> </p>Pour résoudre cette difficulté, vérifiez les problèmes xml dans le fichier nommé par l’analyseur. | Oui | Oui |

{style=&quot;table-layout:auto&quot;}

## Problèmes connus

Vous trouverez, ci-dessous, une liste de problèmes connus dans le cadre de l’utilisation du plug-in Maven Build Analyzer.

### Échec de l’exécution du plug-in Maven Build Analyzer dans le SDK local

Lorsque vous utilisez le SDK local avec une version du plug-in Maven Build Analyzer inférieure à `1.1.2`, l’exécution du plug-in peut entraîner l’erreur ci-dessous. Dans ce cas, mettez à jour votre projet vers la dernière version du plug-in.

```txt
[ERROR] Failed to execute goal com.adobe.aem:aemanalyser-maven-plugin:1.1.0:analyse (default-analyse) on project mysite.analyse: Execution default-analyse of goal com.adobe.aem:aemanalyser-maven-plugin:1.1.0:analyse failed: arraycopy: source index -1 out of bounds for char[65536] -> [Help 1]
```

Si vous avez utilisé l’archétype de projet AEM pour configurer votre projet, veillez à configurer la propriété dans le fichier `pom.xml` Maven racine comme indiqué ci-dessous.

```xml
   ...
   <properties>
      ...
      <aemanalyser.version>1.1.2</aemanalyser.version> <!-- Make sure to use the latest release -->
      ...
   </properties>
```
