---
title: Présentation des composants principaux
description: 'Les composants principaux ont été conçus pour offrir des composants de base solides et extensibles, reposant sur les dernières technologies et les bonnes pratiques. '
translation-type: tm+mt
source-git-commit: 71c1cca664dde91968df16848650df9f0f0a5218

---


# Présentation des composants principaux{#core-components-introduction}

Dans Adobe Experience Manager, les composants sont des éléments structurels qui constituent le contenu des pages en cours de création. Les composants ont toujours été un élément fondamental de l’expérience AEM. Ils facilitent la création de pages pour l’auteur et le développement de composants flexibles et extensibles pour le développeur.

Les composants principaux sont un ensemble de composants WCM (Web) normalisés pour AEM afin d’accélérer le temps de développement et de réduire les coûts de maintenance de vos sites Web.

## Ressources {#resources}

* **[Bibliothèque de composants :](https://www.adobe.com/go/aem_cmp_library)**Ensemble d’exemples permettant de  les composants dans leurs différentes configurations.
* **Documentation du composant (ce ) :** Pour les développeurs et les auteurs, avec des détails sur chaque composant.
* Prise en main:
   * **[Succès avec les composants principaux :](/help/developing/success.md)**Lignes directrices à prendre en considération bien avant la  de tout projet qui utilisera les composants principaux.
   * **[Didacticiel WKND :](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)**Didacticiel de deux jours pour la création d’un nouveau site.
   * **[Didacticiel du sommet :](https://expleague.azureedge.net/labs/L767/index.html)**Un tutoriel de deux heures pour construire un nouveau site (d&#39;un laboratoire au Sommet des Etats-Unis 2019).
   * **[Gems Webinaire :](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)**Une visite guidée des composants principaux (enregistrée en décembre 2018).

## Fonctionnalités {#features}

||||—|—||Production-Ready| Les composants principaux sont 27 composants robustes, bien testés, largement utilisés et performants.||Cloud-Ready| Que ce soit sur [AEM en tant que service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)Cloud, sur les services [gérés](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)Adobe ou sur site, ils fonctionnent simplement.||Versatile| Les composants représentent des concepts génériques avec lesquels les auteurs peuvent assembler pratiquement n&#39;importe quelle mise en page.||Configurable| Les stratégies [de](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/templates/page-templates-editable.html#content-policies) contenu au niveau du modèle définissent les fonctionnalités que les auteurs de pages peuvent utiliser ou non.|
|Accessible| They comply [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), provide ARIA labels, and support keyboard navigation ([known issues](https://github.com/adobe/aem-core-wcm-components/issues?utf8= Scene&amp;q=is%3Aissue+is%3Aopen+Accessibilité+in%3Atitle)).|
|SEO-Friendly| The HTML output is semantic and provides [schema.org](https://schema.org) microdata annotations.||WebApp-Ready| La sortie [JSON](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/develop-sling-model-exporter.html) rationalisée permet le rendu côté client, avec la possibilité d&#39;une modification [](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)contextuelle.||Design Kit| Un kit [d’interface utilisateur pour Adobe XD](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_Wireframe.xd) permet aux concepteurs de créer des structures filaires qu’ils peuvent ensuite [mettre en forme selon les besoins](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_WKND.xd).|
|Themeable| The components implement the [Style System](https://docs.adobe.com/content/help/en/experience-manager-65/developing/components/style-system.html), and the markup follows [BEM CSS conventions](http://getbem.com/).||Personnalisable| Plusieurs modèles permettent une personnalisation [](developing/customizing.md)facile, de l&#39;ajustement du code HTML à la réutilisation des fonctionnalités avancées.||Versioning| La politique [de](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) gestion des versions garantit que les composants principaux ne rompent pas votre site lorsque vous améliorez des éléments susceptibles de vous affecter.|
|Localizable|Smart reference resolution allows certain components to find and [render corresponding localized content automatically](get-started/localization.md).||Ouvrir source| Si quelque chose n&#39;est pas comme il se doit, [apportez vos améliorations!](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md)|

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

### Composants {#container-components}

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
>Les auteurs ne peuvent pas disposer immédiatement de ces composants principaux. En effet, l’[équipe de développement doit d’abord les intégrer dans leur environnement](get-started/using.md). Une fois intégrés, ils peuvent être rendus disponibles et préconfigurés dans l’[éditeur de modèles](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!NOTE]
>
>Certaines versions de composants principaux peuvent uniquement être compatibles avec certaines versions d’AEM.
>
>Pour plus d’informations, reportez-vous à la page d’aide (liée dans la liste précédente) pour le composant spécifique ou consultez le document [Versions des composants principaux](versions.md).

## Configuration requise {#system-requirements}

| Composants principaux | AEM as a Cloud Service | AEM 6.5 | AEM 6.4 | AEM 6.3 | Java SE | Maven |
---------|---------|---------|---------|---------|---------|---------
| [2.8.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0) | Suite | 6.5.0.0+ | 6.4.4.0+ | 6.3.3.4+ | 8, 11 | 3.3.9+ |

Pour connaître les exigences des versions précédentes des composants principaux, voir Versions [des composants](versions.md)principaux.

Les composants principaux nécessitent l’utilisation de modèles [](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html) modifiables et ne prennent pas en charge l’interface utilisateur classique ni les modèles statiques. Si nécessaire, consultez les outils [de modernisation d’](https://opensource.adobe.com/aem-modernize-tools/pages/tools.html) AEM pour mettre à jour votre projet avec ces fonctionnalités modernes d’AEM.

Pour configurer votre  de développement local , consultez [cet aperçu pour AEM en tant que SDK](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) de service cloud ou ce  pour les versions plus anciennes d’AEM [](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).
