---
title: Archétype de projet AEM
description: Modèle de projet pour les applications basées sur AEM
translation-type: tm+mt
source-git-commit: 1e95666ee58c63fc5dc98821e6424be6acfe4e04
workflow-type: tm+mt
source-wordcount: '989'
ht-degree: 95%

---


# Archétype de projet AEM {#aem-project-archetype}

L’archétype de projet AEM est un modèle Maven qui crée un projet Adobe Experience Manager (AEM) minimal qui s’appuie sur des bonnes pratiques pour démarrer votre site web.

>[!TIP]
>
>Le dernier archétype de projet AEM [est disponible sur GitHub](https://github.com/adobe/aem-project-archetype).

## Ressources {#resources}

* **Documentation de l’archétype (ce document) :** présentation de l’architecture de l’archétype et de ses différents modules.
   * **[Utilisation de l’archétype :](using.md)** détails supplémentaires sur l’utilisation de l’archétype et des modules disponibles.
   * **[ui.frontend :](uifrontend.md)** utilisation du module de création front-end.
* Les tutoriels suivants reposent sur cet archétype :
   * **[Site WKND :](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** apprenez à créer un site web attrayant.
   * **[Application monopage WKND :](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html)** découvrez comment concevoir une application web React ou Angular offrant des fonctions de création complètes dans AEM.

## Fonctionnalités {#features}

* **Bonne pratique :** démarrez votre site en suivant toutes les dernières pratiques recommandées par Adobe.
* **Peu de code requis :** modifiez vos modèles, créez du contenu, déployez votre feuille de style CSS et votre site est prêt à être publié.
* **Prêt pour le cloud :** si vous le souhaitez, utilisez [AEM as a Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) pour publier votre site en quelques jours seulement, ainsi que pour faciliter l’évolutivité et la maintenance.
* **Dispatcher :** un projet ne sera complet qu’avec une [configuration du Dispatcher](https://docs.adobe.com/content/help/fr-FR/experience-manager-dispatcher/using/dispatcher.html) qui assure vitesse et sécurité.
* **Multi-site :** si nécessaire, l’archétype génère la structure de contenu pour une [configuration multilingue et multi-région](https://docs.adobe.com/content/help/fr-FR/experience-manager-65/administering/introduction/msm.html).
* **Composants principaux :** les auteurs peuvent créer pratiquement n’importe quelle disposition grâce à notre [ensemble polyvalent de composants standardisés](/help/introduction.md).
* **Modèles modifiables :** assemblez pratiquement n’importe quel [modèle sans code](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html) et définissez ce que les auteurs sont autorisés à modifier.
* **Disposition en responsive design :** sur les modèles ou les pages individuelles, [définissez la manière dont les éléments se redistribuent](https://docs.adobe.com/content/help/fr-FR/experience-manager-65/authoring/siteandpage/responsive-layout.html) pour les points d’arrêt définis.
* **En-tête et pied de page :** assemblez-les et localisez-les sans code, à l’aide des [fonctionnalités de localisation des composants](https://docs.adobe.com/content/help/fr-FR/experience-manager-core-components/using/get-started/localization.html).
* **Système de style :** évitez de devoir créer des composants personnalisés en permettant aux auteurs de leur [appliquer différents styles](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/style-system.html).
* **Création front-end :** les développeurs front-end peuvent [concevoir des maquettes de pages AEM](uifrontend.md#webpack-dev-server) et [créer des bibliothèques clientes](uifrontend.md) avec Webpack, TypeScript et SASS.
* **Prêt pour WebApp :** pour les sites qui utilisent [React](uifrontend-react.md) ou [Angular](uifrontend-angular.md), utilisez le [SDK SPA](https://docs.adobe.com/content/help/fr-FR/experience-manager-64/developing/headless/spas/spa-architecture.html) afin de conserver la [création en contexte au sein de l’application](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html).
* **Exemple de code :** découvrez le composant HelloWorld, ainsi que les exemples de modèles, servlets, filtres et planificateurs.
* **Open source :** si quelque chose ne va pas, [contribuez](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) en apportant vos améliorations.

## Utilisation

Pour générer un projet, ajustez la ligne de commande suivante en fonction de vos besoins :

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

* Définissez `aemVersion=cloud` pour [AEM as a Cloud Service](https://docs.adobe.com/content/help/fr-FR/experience-manager-cloud-service/landing/home.html).\
   Définissez `aemVersion=6.5.0` pour [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) ou On-Premise.
La dépendance des composants principaux n’est ajoutée que pour les versions d’AEM hors du cloud, car ils sont fournis prêts à l’emploi pour AEM as a Cloud Service.
* Ajustez `appTitle="My Site"` de façon à définir le titre du site web et les groupes de composants.
* Ajustez `appId="mysite"` afin de définir l’artifactId Maven, les noms des dossiers de composants, de configurations et de contenu, ainsi que les noms des bibliothèques clientes.
* Ajustez `groupId="com.mysite"` pour définir le groupId Maven et le package source Java.
* Parcourez la liste des propriétés disponibles pour déterminer si d’autres doivent être modifiées.

## Propriétés disponibles

| Nom | Valeur par défaut | Description |
--------------------------|----------------|--------------------
| `appTitle` |  | Titre de l’application qui sera utilisé comme titre du site web et des groupes de composants (par exemple, `"My Site"`). |
| `appId` |  | Nom technique qui sera utilisé pour les noms des dossiers de composants, de configurations et de contenu, ainsi que pour les noms des bibliothèques clientes (par exemple, `"mysite"`). |
| `artifactId` | *`${appId}`* | ID d’artefact Maven de base (par exemple, `"mysite"`). |
| `groupId` |  | ID de groupe Maven de base (par exemple, `"com.mysite"`). |
| `package` | *`${groupId}`* | Package source Java (par exemple, `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | Version du projet (par exemple, `1.0-SNAPSHOT`). |
| `aemVersion` | `6.5.0` |  Version d’AEM cible (par exemple, `cloud` pour [AEM as a Cloud Service](https://docs.adobe.com/content/help/fr-FR/experience-manager-cloud-service/landing/home.html) ; ou `6.5.0`, `6.4.4` ou `6.3.3` pour [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) ou On-Premise). |
| `sdkVersion` | `latest` | Lorsque `aemVersion=cloud`, une version de [SDK](https://docs.adobe.com/content/help/fr-FR/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) peut être spécifiée (par exemple, `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Inclut une configuration du Dispatcher pour le cloud ou pour AMS/On-Premise, selon la valeur de `aemVersion` (par exemple, `y` ou `n`). |
| `frontendModule` | `none` | Comprend un module de création front-end Webpack qui génère les bibliothèques clientes (par exemple, `general` ou `none` pour les sites standard ; ou `angular` ou `react` pour une application monopage qui implémente l’[éditeur d’application monopage](https://docs.adobe.com/content/help/fr-FR/experience-manager-65/developing/headless/spas/spa-overview.html)). |
| `languageCountry` | `en_us` | Code de langue et de pays utilisé pour créer la structure de contenu (par exemple, `en_us`). |
| `singleCountry` | `y` | Inclut une structure de contenu servant de gabarit de langue (par exemple, `y` ou `n`). |
| `includeExamples` | `y` | Inclut un exemple de site de [bibliothèque de composants](https://www.aemcomponents.dev/) (par exemple, `y` ou `n`). |
| `includeErrorHandler` | `n` | Inclut une page de réponse personnalisée 404 qui sera globale pour l’ensemble de l’instance (par exemple, `y` ou `n`). |
| `includeCommerce` | `n` | Inclut des dépendances [CIF Core Components](https://github.com/adobe/aem-core-cif-components) et génère des artefacts correspondants. |
| `commerceEndpoint` |  | Requis pour CIF uniquement. Point de terminaison facultatif du service GraphQL du système de commerce à utiliser (ex. `https://hostname.com/grapql`). |
| `datalayer` | `y` | Activez l’intégration avec la couche [de données du client](/help/developing/data-layer/overview.md)d’Adobe. |
| `amp` | `n` | Activez la prise en charge [AMP](/help/developing/amp.md) pour les modèles de projet générés. |

## Configuration requise

| Archétype | AEM as a Cloud Service | AEM 6.5 | AEM 6.4 | Java SE | Maven |
|---------|---------|---------|---------|---------|---------|
| [24](https://github.com/adobe/aem-project-archetype/releases/tag/aem-project-archetype-24) | Suite | 6.5.5.0+ | 6.4.8.1+ | 8, 11 | 3.3.9+ |

Configurez votre environnement de développement local pour le [SDK AEM as a Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) ou pour les [versions antérieures d’AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).

### Problèmes connus

Lorsque vous exécutez Windows et générez la configuration du Dispatcher, vous devez utiliser une invite de commande avec élévation de privilèges ou le sous-système Windows pour Linux (voir le [problème 329](https://github.com/adobe/aem-project-archetype/issues/329)).

Lors de l’exécution de l’archétype en mode interactif (sans le paramètre `-B`), les propriétés avec des valeurs par défaut ne peuvent pas être modifiées, sauf si la confirmation finale est rejetée, ce qui répète les questions en incluant les propriétés avec des valeurs par défaut (voir [ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) pour plus de détails).

## Informations complémentaires {#further-reading}

Pour plus d’informations sur l’utilisation de l’archétype, notamment ses avantages, ses options et le fonctionnement de ses modules, consultez le [document Utilisation de l’archétype](using.md).
