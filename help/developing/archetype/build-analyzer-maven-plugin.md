---
title: aem en tant que module externe expert du kit SDK Cloud Service
description: Documentation du module externe Maven build analyzer local
translation-type: tm+mt
source-git-commit: e32521f35f33897cd72892de393073b01ad963f1
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 3%

---


# aem en tant que module externe expert du kit SDK Cloud Service {#maven-analyzer-plugin}

Le module externe Maven de l’analyseur AEM analyse la structure des différents projets de packages de contenu.

Pour plus d’informations sur la façon de l’inclure dans un projet d’expert AEM, consultez la documentation [du module externe](https://github.com/adobe/aemanalyser-maven-plugin/blob/main/aemanalyser-maven-plugin/README.md) Analyzer Maven. Le module externe est inclus dans l&#39;archétype AEM Maven version 25 et ultérieure.

Vous trouverez ci-dessous un tableau décrivant les analyseurs exécutés dans le cadre de cette étape. Notez que certains sont exécutés dans le SDK local, tandis que d’autres ne le sont que pendant le déploiement du pipeline de Cloud Manager.

| Module | Fonction, exemple et dépannage | SDK local | Cloud Manager |
|---|---|---|---|
| `api-regions-exportsimports` | Vérifie si les déclarations d&#39;importation-package de tous les lots OSGI sont satisfaites par la déclaration d&#39;exportation-package d&#39;autres lots inclus dans le projet Maven. Une erreur se présenterait comme suit : <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is importing package(s) org.acme.foo in start level 20 but no bundle is exporting these for that start level.`<p> </p>Pour résoudre les problèmes, vérifiez si l’offre groupée fournissant le pack est incluse dans le déploiement ou regardez le manifeste de l’offre groupée que vous prévoyez d’exporter afin de déterminer si un nom incorrect ou une version incorrecte a été utilisé. | Oui | Oui |
| `requirements-capabilities` | Vérifie si toutes les déclarations d&#39;exigences faites dans les lots OSGI sont satisfaites par les déclarations de capacités d&#39;autres lots inclus dans le projet Maven. Une erreur se présenterait comme suit : <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Artifact org.acme:mybundle:0.0.1-SNAPSHOT requires org.foo.bar in start level 20 but no artifact is providing a matching capability in this start level.`<p> </p> Pour résoudre les problèmes, regardez le manifeste du lot que vous vous attendiez à déclarer une capacité pour déterminer pourquoi il est manquant ou vérifiez le manifeste du lot requis pour vous assurer que l&#39;exigence y est correcte. | Oui | Oui |
| `bundle-content` | Indique un avertissement si un lot contient le contenu initial spécifié avec Sling-Initial-Content, ce qui pose problème dans l’AEM en tant qu’environnement organisé en grappes de Cloud Service. L&#39;avertissement ressemble à ceci : <p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found initial content : [/]` <p> </p>Pour résoudre les problèmes de conversion du contenu initial en instructions de repointage, voir Documentation de repointage. | Oui | Oui |
| `bundle-resources` | Indique un avertissement si un lot contient des ressources spécifiées avec l’en-tête Sling-Bundle-Resources, ce qui pose problème dans l’AEM en tant qu’environnement en grappe Cloud Service. L&#39;avertissement ressemble à ceci :<p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found bundle resources : [/libs/sling/explorer!/resources/explorer]`<p> </p> Pour résoudre les problèmes de conversion des ressources en instructions repointé, voir Documentation [](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=en#repo-init)repointé. | Oui | Oui |
| `api-regions`<p> </p>`api-regions-check-order`<p> </p>`api-regions-dependencies`<p> </p>`api-regions-duplicates` | Ces analyseurs vérifient quelques détails sur la configuration des régions API dans les fonctionnalités. Pour les clients, la configuration Régions de l’API est générée et n’est pas directement spécifiée par eux, ces analyseurs sont activés car ils sont également activés dans AEMaaCS. Cependant, un échec produit par l&#39;une de ces méthodes indique un bogue dans le package de contenu pour inclure le processus de conversion du modèle. | Oui | Oui |
| `api-regions-crossfeature-dups` | Vérifie que les lots OSGI des clients ne comportent pas de déclarations de package d’exportation qui remplacent AEM en tant qu’API publique Cloud Service<p> </p>`[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Package overlap found between region global and bundle org.acme:mybundle:0.0.1.SNAPSHOT which comes from feature: [org.acme:myproject.analyse:slingosgifeature:0.0.1-SNAPSHOT]. Both export package: com.day.util`<p> </p>Pour résoudre ce problème, arrêtez d’exporter un package qui fait partie de l’API publique AEM. | Oui | Oui |