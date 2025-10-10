---
title: Présentation des composants principaux
description: Obtenez des solutions aux problèmes grâce aux composants principaux et permettez à d’autres personnes de créer des éléments dans AEM.
role: Architect, Developer, Admin, User
exl-id: d294db22-4cb0-48a4-9366-03fda5b8bb8e
source-git-commit: b6b850237bdab1cb59a81c3162182e5b25fbdb68
workflow-type: ht
source-wordcount: '836'
ht-degree: 100%

---


# Présentation des composants principaux{#core-components-introduction}

{{traditional-aem}}

Dans Adobe Experience Manager, les composants sont des éléments structurels qui constituent le contenu des pages en cours de création. Les composants ont toujours été un élément fondamental de l’expérience AEM. Ils facilitent la création de pages pour l’auteur et le développement de composants flexibles et extensibles pour le développeur.

Les composants principaux sont un ensemble de composants WCM (Web Content Management, gestion de contenu web) normalisés pour AEM dont l’objectif est d’accélérer le développement et de réduire les coûts de maintenance de vos sites web.

## Ressources {#resources}

* **[Bibliothèque de composants :](https://www.adobe.com/go/aem_cmp_library_fr)** ensemble d’exemples permettant d’afficher les composants dans leurs différentes configurations.
* **Documentation des composants (le présent document) :** pour les développeurs et les auteurs, avec des détails sur chaque composant.
* **[Référentiel GitHub des composants principaux :](https://github.com/adobe/aem-core-wcm-components)** pour les développeurs, avec des informations détaillées sur chaque téléchargement de composant et de projet.
* Prise en main :
   * **[Réussir avec les composants principaux :](/help/developing/success.md)** lignes directrices à prendre en compte avant de débuter tout projet qui fera appel aux composants principaux.
   * **[Tutoriel WKND :](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=fr)** tutoriel de deux jours pour créer un site.
   * **[Tutoriel Summit :](https://expleague.azureedge.net/labs/L767/index.html)** tutoriel de deux heures pour créer un site (issu d’un atelier de l’Adobe US Summit 2019).
   * **[Webinaire Gems :](https://helpx.adobe.com/fr/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)** visite guidée des composants principaux (enregistrée en décembre 2018).

## Fonctions {#features}

|  |  |
|---|---|
| Prêts pour la production | Les composants principaux sont 30 composants de gestion de contenu web robustes, bien testés, largement utilisés et performants. |
| Prêts pour le cloud | Ils fonctionnent aussi bien sur [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=fr) que sur [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) ou On-Premise. |
| Polyvalents | Les composants représentent des concepts génériques avec lesquels les auteurs peuvent assembler pratiquement n’importe quelle disposition. |
| Configurables | Des [politiques de contenu](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html?lang=fr#content-policies) au niveau du modèle définissent les fonctionnalités que les auteurs de pages peuvent ou non utiliser. |
| [Réactif](responsive.md) | Tous les composants principaux sont conçus pour être entièrement réactifs, ce qui garantit une expérience transparente sur tous les appareils. |
| Permettent un suivi | L’[intégration de la couche de données client Adobe](/help/developing/data-layer/overview.md) permet le suivi de tous les aspects de l’expérience du visiteur. |
| Accessibles | Ils sont conformes à la [norme WCAG 2.1](https://www.w3.org/TR/WCAG21/), fournissent des étiquettes ARIA et prennent en charge la navigation au clavier ([problèmes connus](https://github.com/adobe/aem-core-wcm-components/issues?utf8=✓&q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle)). |
| Optimisation du référencement | La sortie HTML est sémantique et fournit des annotations de microdonnées [schema.org](https://schema.org). |
| Prêts pour WebApp | La [sortie JSON rationalisée](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/develop-sling-model-exporter.html?lang=fr) permet le rendu côté client, avec la possibilité d’une [modification contextuelle](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=fr). |
| Prise en charge d’AMP | Les composants intègrent la [prise en charge de la norme AMP](/help/developing/amp.md), ce qui accélère vos expériences mobiles. |
| Kit de conception | Un [kit d’interface utilisateur pour Adobe XD](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/AEM-CoreComponents-UI-Kit.xd?lang=fr) permet aux concepteurs de créer des maquettes qu’ils peuvent ensuite [mettre en forme selon leurs besoins](https://github.com/adobe/aem-guides-wknd/releases/download/aem-guides-wknd-0.0.2/AEM_UI-kit-WKND.xd). |
| Possibilité d’appliquer des thèmes | Les composants implémentent le [système de style](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=fr) et le balisage suit les [conventions CSS BEM](https://getbem.com/). |
| Personnalisables | Plusieurs modèles permettent une [personnalisation facile](developing/customizing.md), depuis l’ajustement du code HTML jusqu’à la réutilisation des fonctionnalités avancées. |
| Contrôle de version | La [politique de contrôle de version](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) garantit que les composants principaux ne rendent pas votre site inopérable lorsqu’ils améliorent des éléments susceptibles de vous affecter. |
| Localisables | La résolution intelligente des références permet à certains composants de rechercher le contenu localisé correspondant et d’en [effectuer automatiquement le rendu](get-started/localization.md). |
| Open source | Si quelque chose ne va pas, [contribuez en apportant vos améliorations.](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) |


## Composants de gestion de contenu web {#the-wcm-components}

La version actuelle des composants principaux comporte les composants ci-après :

### Composants de modèle {#template-components}

* [Page](components/page.md)
* [Navigation](components/navigation.md)
* [Navigation par langue](components/language-navigation.md)
* [Chemin de navigation](components/breadcrumb.md)
* [Recherche rapide](components/quick-search.md)
* [Table des matières](components/tableofcontents.md)

### Composants de création de page {#page-authoring-components}

* [Titre](components/title.md)
* [Texte](components/text.md)
* [Image](components/image.md)
* [Bouton](components/button.md)
* [Teaser](components/teaser.md)
* [Télécharger](components/download.md)
* [Liste](components/list.md)
* [Fragment d’expérience](components/experience-fragment.md)
* [Fragment de contenu](components/content-fragment-component.md)
* [Liste de fragments de contenu](components/content-fragment-list.md)
* [Incorporer](components/embed.md)
* [Partage sur les médias sociaux](components/sharing.md) (obsolète)
* [Séparateur](components/separator.md)
* [Barre de progression](components/progress-bar.md)
* [Visionneuse PDF](components/pdf-viewer.md)

### Composants de conteneur {#container-components}

* [Conteneur](components/container.md)
* [Carrousel](components/carousel.md)
* [Onglets](components/tabs.md)
* [Accordéon](components/accordion.md)

### Composants de formulaire {#form-components}

* [Conteneur de formulaires](components/forms/form-container.md)
* [Texte du formulaire](components/forms/form-text.md)
* [Options du formulaire](components/forms/form-options.md)
* [Formulaire masqué](components/forms/form-hidden.md)
* [Bouton de formulaire](components/forms/form-button.md)

>[!NOTE]
>
>Les auteurs ne peuvent pas disposer immédiatement de ces composants principaux. En effet, l’[équipe de développement doit d’abord les intégrer dans leur environnement](get-started/using.md). Une fois intégrés, ils peuvent être rendus disponibles et préconfigurés dans l’[éditeur de modèles](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=fr).

>[!NOTE]
>
>Certaines versions de composants principaux peuvent uniquement être compatibles avec certaines versions d’AEM.
>
>Pour plus d’informations, reportez-vous à la page d’aide (liée dans la liste précédente) pour le composant spécifique ou consultez le document [Versions des composants principaux](versions.md).

## Configuration requise {#system-requirements}

| Version des composants principaux | AEM as a Cloud Service | AEM 6.5 LTS | AEM 6.5 | Version de Java SE | Version de Maven |
|---|---|---|---|---|---|
| [2.30.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.30.0) | En continu | 6.5 LTS (disponibilité générale) | 6.5.21.0+ | 8, 11 | 3.3.9+ |

Pour connaître les exigences des versions précédentes des composants principaux, voir [Versions des composants principaux](versions.md).

Les composants principaux nécessitent l’utilisation de [modèles modifiables](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html?lang=fr) et ne prennent pas en charge l’interface utilisateur classique ni les modèles statiques. Si nécessaire, consultez les [outils de modernisation d’AEM](https://opensource.adobe.com/aem-modernize-tools/) pour mettre à jour votre projet avec ces fonctionnalités modernes d’AEM.

Pour configurer votre environnement de développement local, consultez [cet aperçu du SDK d’AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html?lang=fr) ou ce document [pour les versions plus anciennes d’AEM](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html?lang=fr).

>[!TIP]
>
>Les composants principaux sont automatiquement intégrés à AEM as a Cloud Service et vous disposez toujours de la dernière version.
>
>Consultez le document [Utilisation des composants principaux](/help/get-started/using.md) pour obtenir plus d’informations sur la façon d’utiliser les composants principaux dans AEM as a Cloud Service et On-Premise.

## Autres composants {#other-components}

D’autres composants basés sur les composants principaux sont disponibles pour les auteurs AEM.

* [Composants principaux d’e-mail](/help/email/introduction.md) - Découvrez les composants conçus sur les composants principaux spécifiquement destinés à être utilisés avec Adobe Campaign.
* [Composants principaux des formulaires adaptatifs](/help/adaptive-forms/introduction.md) : à l’aide des composants principaux des formulaires adaptatifs dans Adobe Experience Manager, vous pouvez créer des expériences d’inscription attrayantes.
