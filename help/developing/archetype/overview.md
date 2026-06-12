---
title: Archétype de projet AEM
description: Découvrez l’archétype de projet AEM qui sert de modèle pour les applications basées sur AEM.
feature: Core Components, AEM Project Archetype
role: Developer, Admin
exl-id: 58994726-9b65-4035-9d45-60b745d577bb
TQID: https://experienceleague.adobe.com/snvIzunCCWegShAzgcg9Zpof00Wq-tAYkaoGvq4RwEk
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
subfeature_v2:
  - id: f86a5563-8f73-4ec0-be7d-a1782604870a
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: ce44533e-8ec8-4e11-a9e9-78b0fe561832
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 705
ht-degree: 100%

---

# Archétype de projet AEM {#aem-project-archetype}

L’archétype de projet AEM est un modèle Maven qui crée un projet Adobe Experience Manager (AEM) minimal qui s’appuie sur des bonnes pratiques pour démarrer votre site web. Cette documentation présente une vue d’ensemble des avantages de l’archétype et de l’utilisation générale. Vous trouverez des instructions techniques détaillées et de la documentation dans le référentiel GitHub de l’archétype.

>[!TIP]
>
>Le dernier archétype de projet AEM, ainsi que la documentation technique complète, [sont disponibles sur GitHub](https://github.com/adobe/aem-project-archetype).

{{traditional-aem}}

## Pourquoi utiliser l’archétype {#why-use-the-archetype}

L’utilisation de l’archétype de projet AEM vous permet de vous orienter vers la création d’un projet AEM basé sur des bonnes pratiques, et ce, en un tour de main. Avec l’archétype, toutes les pièces sont déjà en place afin que, même avec un résultat de projet très simple, celui-ci implémente déjà toutes les [fonctionnalités clés](/help/developing/archetype/using.md#what-you-get) d’AEM. Tout ce que vous aurez alors à faire est de vous appuyer sur ce projet de base et de le développer.

De nombreux éléments entrent bien sûr en compte dans la [réussite d’un projet AEM](/help/developing/success.md), mais l’utilisation de l’archétype de projet AEM constitue une base solide et est vivement recommandée pour la création de tout projet AEM.

## Fonctions {#features}

* **Bonne pratique :** démarrez votre site en suivant toutes les dernières pratiques recommandées par Adobe.
* **Peu de code requis :** modifiez vos modèles, créez du contenu, déployez votre feuille de style CSS et votre site est prêt à être publié.
* **Prêt pour le cloud :** si vous le souhaitez, utilisez [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=fr) pour publier votre site en quelques jours seulement, ainsi que pour faciliter l’évolutivité et la maintenance.
* **Dispatcher :** un projet ne sera complet qu’avec une [configuration du Dispatcher](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/dispatcher.html?lang=fr) qui assure vitesse et sécurité.
* **Multi-site :** si nécessaire, l’archétype génère la structure de contenu pour une [configuration multilingue et multi-région](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/msm/overview.html?lang=fr).
* **Composants principaux :** les auteurs peuvent créer pratiquement n’importe quelle disposition grâce à notre [ensemble polyvalent de composants standardisés](/help/introduction.md).
* **Modèles modifiables :** assemblez pratiquement n’importe quel [modèle sans code](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html?lang=fr) et définissez ce que les auteurs sont autorisés à modifier.
* **Disposition en responsive design :** sur les modèles ou les pages individuelles, [définissez la manière dont les éléments se redistribuent](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html?lang=fr) pour les points d’arrêt définis.
* **En-tête et pied de page :** assemblez-les et localisez-les sans code, à l’aide des [fonctionnalités de localisation des composants](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html?lang=fr).
* **Système de style :** évitez de devoir créer des composants personnalisés en permettant aux auteurs de leur [appliquer différents styles](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/project-archetype/style-system.html?lang=fr).
* **Création front-end :** les développeurs et développeuses front-end peuvent [concevoir des maquettes de pages AEM et créer des bibliothèques clientes](front-end.md) avec Webpack, TypeScript et SASS.
* **Prêt pour WebApp :** pour les sites qui utilisent React ou Angular, utilisez le [SDK SPA](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/hybrid/developing.html?lang=fr) afin de conserver la [création en contexte au sein de l’application](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=fr).
* **Compatible Commerce :** pour les projets qui souhaitent intégrer [AEM Commerce](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/home.html?lang=fr) à des solutions de commerce comme [Magento](https://magento.com/fr) à l’aide des composants [principaux](https://github.com/adobe/aem-core-cif-components) Commerce.
* **Exemple de code :** vous pouvez extraire le composant HelloWorld, ainsi que les exemples de modèles, servlets, filtres et planificateurs.
* **Open source :** si quelque chose ne va pas, [contribuez](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) en apportant vos améliorations.

## Informations complémentaires {#further-reading}

* **[GitHub de l’archétype de projet AEM](https://github.com/adobe/aem-project-archetype)** : pour une utilisation complète et des détails techniques de l’archétype.
* **[Utilisation de l’archétype](using.md)** : présentation de l’utilisation de l’archétype dans votre projet et des modules générés.
* **[Développement front-end avec l’archétype de projet AEM](front-end.md)** : utilisation du module front-end de l’archétype
* **Les tutoriels suivants sont basés sur cet archétype :**
   * **[Site WKND](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=fr)** : apprenez à créer un site web attrayant.
   * **[Application d’une seule page WKND :](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=fr)** découvrez comment concevoir une application web React ou Angular offrant des fonctions de création complètes dans AEM.
