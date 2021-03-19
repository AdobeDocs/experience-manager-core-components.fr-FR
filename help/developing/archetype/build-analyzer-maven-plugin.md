---
title: Plug-in Maven Build Analyzer du SDK AEM as a Cloud Service
description: Documentation du plug-in local Maven Build Analyzer
feature: Composants principaux, AEM Archétype de projet
role: Architecte, développeur, administrateur
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 98%

---


# Plug-in Maven Build Analyzer du SDK AEM as a Cloud Service {#maven-analyzer-plugin}

Le plug-in Maven Build Analyzer du SDK AEM as a Cloud Service analyse la structure des différents projets de packages de contenu.

Consultez la [documentation du plug-in Maven](https://github.com/adobe/aemanalyser-maven-plugin/blob/main/aemanalyser-maven-plugin/README.md) pour savoir comment l’inclure dans un projet Maven AEM.

>[!NOTE]
>
>Il est recommandé de mettre à jour votre projet Maven pour référencer la dernière version du plug-in du référentiel central Maven, à cet emplacement : https://repo1.maven.org/maven2/com/adobe/aem/aemanalyser-maven-plugin/

Vous trouverez ci-dessous un tableau décrivant les analyseurs exécutés au cours de cette étape. <!-- Note that some are executed in the local SDK, while others are only executed during the Cloud Manager pipeline deployment. -->

| Module | Fonction, exemple et dépannage | SDK local | Cloud Manager |
|---|---|---|---|
| `api-regions-exportsimports` | Vérifie si les déclarations Import-Package de tous les lots OSGI sont satisfaites par la déclaration Export-package d’autres lots inclus dans le projet Maven. Une erreur se présenterait comme suit : <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is importing package(s) org.acme.foo in start level 20 but no bundle is exporting these for that start level.`<p> </p>Pour résoudre les problèmes, vérifiez si le lot contenant le package est inclus dans le déploiement ou examinez le manifeste du lot que vous prévoyez d’exporter pour déterminer si un nom incorrect ou une version erronée a été utilisé. | Oui | Oui |
| `requirements-capabilities` | Vérifie si toutes les déclarations d’exigences faites dans les lots OSGI sont satisfaites par les déclarations de capacités d’autres lots inclus dans le projet Maven. Une erreur se présenterait comme suit : <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Artifact org.acme:mybundle:0.0.1-SNAPSHOT requires org.foo.bar in start level 20 but no artifact is providing a matching capability in this start level.`<p> </p> Pour résoudre les problèmes, vérifiez le manifeste du lot censé contenir une déclaration de capacité afin de déterminer pourquoi elle n’y figure pas ou examinez le manifeste du lot requis pour vérifier que l’exigence qu’il contient est correcte. | Oui | Oui |
| `bundle-content` | Émet un avertissement si un lot contient le contenu initial spécifié avec Sling-Initial-Content, ce qui pose problème dans l’environnement organisé en grappes d’AEM as a Cloud Service. L’avertissement ressemble à ceci : <p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found initial content : [/]` <p> </p>Pour résoudre les problèmes de conversion du contenu initial en instructions repoinit, voir la documentation relative à la fonction RepoInit. | Oui | Oui |
| `bundle-resources` | Émet un avertissement si un lot contient des ressources spécifiées avec l’en-tête Sling-Bundle-Resources, ce qui pose problème dans l’environnement organisé en grappes d’AEM as a Cloud Service. L’avertissement ressemble à ceci :<p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found bundle resources : [/libs/sling/explorer!/resources/explorer]`<p> </p> Pour résoudre les problèmes de conversion des ressources en instructions repoinit, voir la [Documentation RepoInit](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=fr#repo-init). | Oui | Oui |
| `api-regions`<p> </p>`api-regions-check-order`<p> </p>`api-regions-dependencies`<p> </p>`api-regions-duplicates` | Ces analyseurs vérifient certains détails relatifs au [processus de conversion de package de contenu en modèle de fonctionnalité](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=fr#deploying) qui crée des artefacts conformes au modèle de fonctionnalité Sling. Toute erreur doit être signalée au service clientèle d’Adobe. | Oui | Oui |
| `api-regions-crossfeature-dups` | Vérifie que les lots OSGI des clients ne comportent pas de déclarations Export-package qui remplacent l’API publique d’AEM as a Cloud Service<p> </p>`[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Package overlap found between region global and bundle org.acme:mybundle:0.0.1.SNAPSHOT which comes from feature: [org.acme:myproject.analyse:slingosgifeature:0.0.1-SNAPSHOT]. Both export package: com.day.util`<p> </p>Pour résoudre ce problème, arrêtez l’exportation d’un package faisant partie de l’API publique d’AEM. | Oui | Oui |
| `repoinit` | Vérifiez la syntaxe de toutes les sections de redirection. | Oui | Oui |
| `bundle-nativecode` | Vérifie que les lots OSGI n’installent pas de code natif. | Oui | Oui |