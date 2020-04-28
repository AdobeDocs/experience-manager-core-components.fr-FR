---
title: Présentation des composants principaux
description: 'Les composants principaux ont été conçus pour offrir des composants de base solides et extensibles, reposant sur les dernières technologies et les bonnes pratiques. '
translation-type: tm+mt
source-git-commit: 1c6e27c163f72fd66336e8db883144dc4dd60510

---


# Présentation des composants principaux{#core-components-introduction}

Dans Adobe Experience Manager, les composants sont des éléments structurels qui constituent le contenu des pages en cours de création. Les composants ont toujours été un élément fondamental de l’expérience AEM. Ils facilitent la création de pages pour l’auteur et le développement de composants flexibles et extensibles pour le développeur.

Les composants principaux sont un ensemble de composants WCM (Web Content Management, gestion de contenu web) normalisés pour AEM dont l’objectif est d’accélérer le développement et de réduire les coûts de maintenance de vos sites web.

## Ressources {#resources}

* **[Bibliothèque de composants :](https://www.adobe.com/go/aem_cmp_library)**ensemble d’exemples permettant d’afficher les composants dans leurs différentes configurations.
* **Documentation des composants (le présent document) :** pour les développeurs et les auteurs, avec des détails sur chaque composant.
* Prise en main :
   * **[Réussir avec les composants principaux :](/help/developing/success.md)**lignes directrices à prendre en compte avant de débuter tout projet qui fera appel aux composants principaux.
   * **[Tutoriel WKND :](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)**tutoriel de deux jours pour créer un site.
   * **[Tutoriel Summit :](https://expleague.azureedge.net/labs/L767/index.html)**tutoriel de deux heures pour créer un site (issu d’un atelier de l’Adobe US Summit 2019).
   * **[Webinaire Gems :](https://helpx.adobe.com/fr/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)**visite guidée des composants principaux (enregistrée en décembre 2018).

## Fonctionnalités {#features}

|  |  |
|---|---|
| Prêts pour la production | Les composants principaux sont 27 composants robustes qui sont bien testés, largement utilisés et qui fonctionnent bien. |
| Cloud-Ready | Whether on [AEM as a Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html), on [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams), or on-premise, they just work. |
| Polyvalents | Les composants représentent des concepts génériques avec lesquels les auteurs peuvent assembler pratiquement n’importe quelle mise en page. |
| Configurable | Template-level [content policies](https://docs.adobe.com/content/help/fr-FR/experience-manager-65/developing/platform/templates/page-templates-editable.html#content-policies) define which features the page authors are allowed to use or not use. |
| Accessibles | They comply [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), provide ARIA labels, and support keyboard navigation ([known issues](https://github.com/adobe/aem-core-wcm-components/issues?utf8=✓&amp;q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle)). |
| Optimisation du référencement | The HTML output is semantic and provides [schema.org](https://schema.org) microdata annotations. |
| WebApp-Ready | The [streamlined JSON output](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/develop-sling-model-exporter.html) allows client-side rendering, still with a possibility of [in-context editing](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html). |
| Kit de conception | A [UI kit for Adobe XD](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_Wireframe.xd) allows designers to create wireframes that they can then [style as needed](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_WKND.xd). |
| Themeable | The components implement the [Style System](https://docs.adobe.com/content/help/fr-FR/experience-manager-65/developing/components/style-system.html), and the markup follows [BEM CSS conventions](http://getbem.com/). |
| Personnalisable | Several patterns allow [easy customization](developing/customizing.md), from adjusting the HTML to advanced functionality reuse. |
| Création de versions | The [versioning policy](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) ensures that the Core Components won&#39;t break your site when improving things that might impact you. |
| Localisable | Smart reference resolution allows certain components to find and [render corresponding localized content automatically](get-started/localization.md). |
| Ouvrir source | If something is not as it should, [contribute your improvements!](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) |

## Composants {#the-components}

La version actuelle des composants principaux comporte les composants ci-après.

### Composants de modèle {#template-components}

* [Page](components/page.md)
* [Navigation](components/navigation.md)
* [Navigation par langue](components/language-navigation.md)
* [Chemin de navigation](components/breadcrumb.md)
* [Recherche rapide](components/quick-search.md)

### Composants de création de page {#page-authoring-components}

* [Titre](components/title.md)
* [Texte](components/text.md)
* [Image](components/image.md)
* [Bouton](components/button.md)
* [Teaser](components/teaser.md)
* [Téléchargement](components/download.md)
* [Liste](components/list.md)
* [Fragment d’expérience](components/experience-fragment.md)
* [Fragment de contenu](components/content-fragment-component.md)
* [Liste de fragments de contenu](components/content-fragment-list.md)
* [Incorporer](components/embed.md)
* [Partage sur les réseaux sociaux](components/sharing.md)
* [Séparateur](components/separator.md)

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
>Les auteurs ne peuvent pas disposer immédiatement de ces composants principaux. En effet, l’[équipe de développement doit d’abord les intégrer dans leur environnement](get-started/using.md). Une fois intégrés, ils peuvent être rendus disponibles et préconfigurés dans l’[éditeur de modèles](https://docs.adobe.com/content/help/fr-FR/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!NOTE]
>
>Certaines versions de composants principaux peuvent uniquement être compatibles avec certaines versions d’AEM.
>
>Pour plus d’informations, reportez-vous à la page d’aide (liée dans la liste précédente) pour le composant spécifique ou consultez le document [Versions des composants principaux](versions.md).

## Configuration requise {#system-requirements}

| Composants principaux | AEM as a Cloud Service | AEM 6.5 | AEM 6.4 | AEM 6.3 | Java SE | Maven |
---------|---------|---------|---------|---------|---------|---------
| [2.8.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0) | Suite | 6.5.0.0+ | 6.4.4.0+ | 6.3.3.4+ | 8, 11 | 3.3.9+ |

Pour connaître les exigences des versions précédentes des composants principaux, voir [Versions des composants principaux](versions.md).

Les composants principaux nécessitent l’utilisation de [modèles modifiables](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html) et ne prennent pas en charge l’interface utilisateur classique ni les modèles statiques. Si nécessaire, consultez les [outils de modernisation d’AEM](https://opensource.adobe.com/aem-modernize-tools/pages/tools.html) pour mettre à jour votre projet avec ces fonctionnalités modernes d’AEM.

Pour configurer votre environnement de développement local, consultez [cet aperçu du SDK AEM as a Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) ou ce document [pour les versions plus anciennes d’AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).
