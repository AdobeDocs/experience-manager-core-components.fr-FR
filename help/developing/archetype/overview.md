---
title: Archétype de projet AEM
description: Modèle de projet pour les applications basées sur AEM
translation-type: tm+mt
source-git-commit: 2faa092a075ab0512e9bd5654884534936c0ad53

---


# Archétype de projet AEM {#aem-project-archetype}

L’archétype de projet AEM est un modèle expert qui crée un projet Adobe Experience Manager (AEM) minimal basé sur les bonnes pratiques comme point de départ pour votre site Web.

>[!TIP]
>
>Le dernier archétype de projet AEM [est disponible sur GitHub](https://github.com/adobe/aem-project-archetype).

## Ressources {#resources}

* **Documentation d&#39;archétype (ce ) :** Présentation de l&#39;architecture archétype et de ses différents modules.
   * **[Utilisation de l&#39;archétype :](using.md)**plus de détails sur l&#39;utilisation de l&#39;archétype et des modules disponibles
   * **[ui.frontend :](uifrontend.md)**Utilisation du module de génération frontal
* Les didacticiels suivants reposent sur cet archétype :
   * **[Site WKND :](https://docs.adobe.com/content/help/fr/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)**Apprenez à  un nouveau site Web.
   * **[Application WKND mono-page :](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html)**Découvrez comment créer une application Web React ou Angular qui soit totalement autorisée dans AEM.

## Fonctionnalités {#features}

* **Meilleure pratique :** Démarrez votre site à l’aide de toutes les dernières pratiques recommandées par Adobe.
* **Code faible :** Modifiez vos modèles, créez du contenu, déployez votre page CSS et votre site est prêt pour la mise en service.
* **Prêt pour le cloud :** Si vous le souhaitez, utilisez [AEM en tant que service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) Cloud pour vivre en quelques jours et faciliter l’évolutivité et la maintenance.
* **Répartiteur :** Un projet est terminé uniquement avec une configuration [du](https://docs.adobe.com/content/help/fr-FR/experience-manager-dispatcher/using/dispatcher.html) répartiteur qui assure la vitesse et la sécurité.
* **Multi-site :** Si nécessaire, l’archétype génère la structure de contenu pour une configuration [](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/msm.html)multilingue et multi-région.
* **Composants principaux :** Les auteurs peuvent créer pratiquement n’importe quelle mise en page avec notre [ensemble polyvalent de composants](/help/introduction.md)standardisés.
* **Modèles modifiables :** Assemblez pratiquement n’importe quel [modèle sans code](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html)et définissez ce que les auteurs sont autorisés à modifier.
* **Disposition réactive :** Sur les modèles ou les pages individuelles, [définissez la manière dont les éléments se répartissent](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/responsive-layout.html) pour les points d’arrêt définis.
* **En-tête et pied de page :** Assemblez-les et localisez-les sans code, à l’aide des fonctionnalités de  [des composants](https://docs.adobe.com/content/help/fr-FR/experience-manager-core-components/using/get-started/localization.html).
* **Système de style :** Evitez de créer des composants personnalisés en permettant aux auteurs d’ [appliquer différents styles](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/style-system.html) .
* **Version frontale :** Les périphériques frontaux peuvent [simuler des pages](uifrontend.md#webpack-dev-server) AEM et [créer des bibliothèques](uifrontend.md) clientes avec Webpack, TypeScript et SASS.
* **Prêt pour WebApp :** Pour les sites qui utilisent [React](uifrontend-react.md) ou [Angular](uifrontend-angular.md), utilisez le SDK [](https://docs.adobe.com/content/help/en/experience-manager-64/developing/headless/spas/spa-architecture.html) SPA pour conserver la création [en contexte de l’application.](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)
* **Exemple de code :** Extrayez le composant HelloWorld et les exemples de modèles, de serveurs, de  et de.
* **Ouvrir source :** Si quelque chose n&#39;est pas ce qu&#39;il devrait, [contribuez](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) à vos améliorations !

## Utilisation

Pour générer un projet, ajustez la ligne de commande suivante en fonction de vos besoins :

```
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.granite.archetypes \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=23 \
 -D aemVersion=cloud \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
 -D frontendModule=general \
 -D includeExamples=n
```

* Défini `aemVersion=cloud` pour [AEM en tant que service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)Cloud ;\
   Défini `aemVersion=6.5.0` pour [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)ou sur site.
La dépendance des composants principaux n’est ajoutée que pour les versions d’Aem non cloud, car les composants principaux sont fournis avec une optimisation d’AEM en tant que CloudService.
* Ajustez `appTitle="My Site"` pour définir le titre du site Web et les groupes de composants.
* Ajustez `appId="mysite"` la variable pour définir le paramètre Maven artifactId, le composant, les noms de dossier de configuration et de contenu, ainsi que les noms de bibliothèque cliente.
* Définissez `groupId="com.mysite"` le groupId Maven et le package source Java.
* Recherchez le  des propriétés disponibles pour savoir s’il y a plus à ajuster.

## Propriétés disponibles

| Nom | Default | Description |
--------------------------|----------------|--------------------
| `appTitle` |  | Le titre de la demande sera utilisé pour le titre du site Web et les groupes de composants (p. ex. `"My Site"`). |
| `appId` |  | Le nom technique sera utilisé pour les noms de composants, de configurations et de dossiers de contenu, ainsi que pour les noms de bibliothèques client (ex. `"mysite"`). |
| `artifactId` | *`${appId}`* | Base Maven artifact ID (e.g. `"mysite"`). |
| `groupId` |  | Base Maven group ID (e.g. `"com.mysite"`). |
| `package` | *`${groupId}`* | Package source Java (ex. `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | Version du projet (ex. `1.0-SNAPSHOT`). |
| `aemVersion` | `6.5.0` |  version d’AEM (peut être `cloud` pour [AEM en tant que service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)Cloud ; ou `6.5.0`, `6.4.4`ou `6.3.3` Adobe Managed Services [](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) ou on-premise). |
| `sdkVersion` | `latest` | Lorsqu’ `aemVersion=cloud` une version du [SDK](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) peut être spécifiée (p. ex. `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Inclut une configuration de répartiteur pour le cloud ou pour AMS/sur site, selon la valeur de `aemVersion` (peut être `y` ou `n`). |
| `frontendModule` | `none` | Comprend un module de génération frontale Webpack qui génère les bibliothèques client (peut être `general` ou `none` pour les sites standard ; peut être `angular` ou `react` pour une application d’une seule page qui implémente l’éditeur [d’](https://docs.adobe.com/content/help/en/experience-manager-65/developing/headless/spas/spa-overview.html)application d’une seule page). |
| `languageCountry` | `en_us` | Language and country code to create the content structure from (e.g. `en_us`). |
| `singleCountry` | `y` | Inclut une structure de contenu maître de langue (peut être `y`ou `n`). |
| `includeExamples` | `y` | Inclut un exemple de site de bibliothèque [de](https://www.aemcomponents.dev/) composants (peut être `y`ou `n`). |
| `includeErrorHandler` | `n` | Inclut une page de réponse personnalisée 404 qui sera globale pour l’instance entière (peut être `y` ou `n`). |

## Configuration requise

| Archétype | AEM as a Cloud Service | AEM 6.5 | AEM 6.4 | AEM 6.3 | Java SE | Maven |
---------|---------|---------|---------|---------|---------|---------
| [23](https://github.com/adobe/aem-project-archetype/releases/tag/aem-project-archetype-23) | Suite | 6.5.0.0+ | 6.4.4.0+ | 6.3.3.4+ | 8, 11 | 3.3.9+ |

Configurez votre  de développement local  pour [AEM en tant que SDK](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) de service cloud ou pour les versions [antérieures d’AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).

### Problèmes connus

When running on Windows and generating the dispatcher configuration, you should be running in an elevated command prompt or the Windows Subsystem for Linux (see [#329](https://github.com/adobe/aem-project-archetype/issues/329)).

Lors de l’exécution de l’archétype en mode interactif (sans le `-B` paramètre), les propriétés avec des valeurs par défaut ne peuvent pas être modifiées, sauf si la confirmation finale est rejetée, ce qui répète les questions en incluant les propriétés avec des valeurs par défaut dans les questions (voir[ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) pour plus de détails).

## Informations complémentaires {#further-reading}

Pour plus d&#39;informations sur l&#39;utilisation de l&#39;archétype, y compris ses avantages, ses options et le fonctionnement de ses modules, consultez la  [Utilisation de l&#39;archétype.](using.md)