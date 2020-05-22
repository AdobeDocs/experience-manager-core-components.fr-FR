---
title: Présentation des composants principaux
description: 'Les composants principaux ont été conçus pour offrir des composants de base solides et extensibles, reposant sur les dernières technologies et les bonnes pratiques. '
translation-type: ht
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
| Prêts pour la production | Les composants principaux sont 27 composants robustes, bien testés, largement utilisés et performants. |
| Prêts pour le cloud | Ils fonctionnent aussi bien sur [AEM as a Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) que sur [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) ou On-Premise. |
| Polyvalents | Les composants représentent des concepts génériques avec lesquels les auteurs peuvent assembler pratiquement n’importe quelle disposition. |
| Configurables | Des [stratégies de contenu](https://docs.adobe.com/content/help/fr-FR/experience-manager-65/developing/platform/templates/page-templates-editable.html#content-policies) au niveau du modèle définissent les fonctionnalités que les auteurs de pages peuvent ou non utiliser. |
| Accessibles | Ils sont conformes à la [norme WCAG 2.1](https://www.w3.org/TR/WCAG21/), fournissent des libellés ARIA et prennent en charge la navigation au clavier ([problèmes connus](https://github.com/adobe/aem-core-wcm-components/issues?utf8=✓&amp;q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle)). |
| Optimisation du référencement | La sortie HTML est sémantique et fournit des annotations de microdonnées [schema.org](https://schema.org). |
| Prêts pour WebApp | La [sortie JSON rationalisée](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/develop-sling-model-exporter.html) permet le rendu côté client, avec la possibilité d’une [modification contextuelle](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html). |
| Kit de conception | Un [kit d’interface utilisateur pour Adobe XD](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_Wireframe.xd) permet aux concepteurs de créer des maquettes qu’ils peuvent ensuite [mettre en forme selon leurs besoins](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_WKND.xd). |
| Possibilité d’appliquer des thèmes | Les composants implémentent le [système de style](https://docs.adobe.com/content/help/fr-FR/experience-manager-65/developing/components/style-system.html) et le balisage suit les [conventions CSS BEM](http://getbem.com/). |
| Personnalisables | Plusieurs modèles permettent une [personnalisation facile](developing/customizing.md), depuis l’ajustement du code HTML jusqu’à la réutilisation des fonctionnalités avancées. |
| Contrôle de version | La [politique de contrôle de version](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) garantit que les composants principaux ne rendent pas votre site inopérable lorsqu’ils améliorent des éléments susceptibles de vous affecter. |
| Localisables | La résolution intelligente des références permet à certains composants de rechercher le contenu localisé correspondant et d’en [effectuer automatiquement le rendu](get-started/localization.md). |
| Open source | Si quelque chose ne va pas, [contribuez en apportant vos améliorations.](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) |

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
