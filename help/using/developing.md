---
title: Développement des composants principaux
seo-title: Développement des composants principaux
description: Les composants principaux fournissent des composants de base robustes et extensibles qui offrent des capacités riches en fonctionnalités, une diffusion continue, un contrôle de version des composants, une mise en œuvre moderne, des balises Lean et une exportation JSON de contenu.
seo-description: Les composants principaux fournissent des composants de base robustes et extensibles qui offrent des capacités riches en fonctionnalités, une diffusion continue, un contrôle de version des composants, une mise en œuvre moderne, des balises Lean et une exportation JSON de contenu.
uuid: 68569da2-9bc8-4e20-9a71-e5816ace51ce
contentOwner: Utilisateur
content-type: référence
topic-tags: développement
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 157a2ec3-9fca-4fad-977a-d93013eeb218
translation-type: tm+mt
source-git-commit: bea783936100abe899f9b60e4a09522514755db2

---


# Développement des composants principaux{#developing-core-components}

## Présentation {#overview}

Les composants principaux fournissent des composants de base robustes et extensibles dont les points forts sont les suivants :

* Riches fonctionnalités
   * [Options de configuration souples](authoring.md) pour répondre à de nombreux cas d’utilisation.
   * [Pré-configurables](authoring.md#pre-configuring-core-components) afin de définir les fonctionnalités accessibles aux auteurs de pages.
* Disponibilité continue
   * Améliorations fréquentes des fonctionnalités incrémentielles.
   * Disponibilité du [code source sur GitHub](https://github.com/adobe/aem-core-wcm-components) pour permettre à la communauté des développeurs de fournir des commentaires et de contribuer.
   * Installation through a [separately released content package](https://github.com/adobe/aem-core-wcm-components/releases) for component upgrades to be done independently from AEM upgrades
* [Contrôle de version des composants](guidelines.md#component-versioning)
   * [Permettent d’assurer la compatibilité dans une version](#upgrade-of-core-components), tout en permettant aux composants d’évoluer.
   * Autoriser plusieurs versions d’un composant à coexister sur le même environnement.
* Implémentation moderne
   * Markup defined in [HTML Template Language](https://helpx.adobe.com/experience-manager/htl/using/overview.html) (HTL)
   * Content model logic implemented with [Sling Models](https://sling.apache.org/documentation/bundles/models.html)
* Balisage Lean
   * Following [Block Element Modifier](https://getbem.com/) (BEM) notation as of Release 2.0.0
      * Prior release follow [Bootstrap](https://getbootstrap.com/css/) naming conventions
   * Built around [accessibility guidelines](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)
   * Capacité à être utilisés pour les sites réactifs et mobiles.
* Possibilité de sérialiser en JSON le modèle de contenu pour les cas d’utilisation d’un CMS sans interface.
* Accessibles
   * Compliant with the [WCAG 2.0 AA standard](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)

>[!CAUTION]
>
>Core Components require AEM 6.3 or later and Java 8 and and require the use of [editable templates](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)
>
>Les composants principaux ne fonctionnent pas avec l’interface utilisateur classique ni avec les modèles statiques.

## Présentation de la session Gems {#gems-session-overview}

Pour une présentation des composants principaux, des fonctionnalités qu’ils proposent et de leur exploitation dans AEM, consultez la session AEM Gems sur les [composants principaux AEM.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[Astuces pour Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) est une série d&#39;épisodes d&#39;épisodes techniques profonds fournis par des experts Adobe. Cette série complète la documentation du produit et de tous les autres canaux techniques, ce qui permet aux développeurs de prendre contact avec eux et d’accéder à une rubrique spécifique.

## Didacticiel du développeur WKND {#wknd-developer-tutorial}

Commencez à développer AEM Sites avec des composants principaux en suivant [ce didacticiel détaillé.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

## Diffusé sur github {#delivered-over-github}

Les composants principaux sont développés et distribués via GitHub.

CODE SUR GITHUB

Vous pouvez trouver le code de cette page sur GitHub.

* [Ouvrez le projet aem-core-wcm-components sur github](https://github.com/adobe/aem-core-wcm-components)
* Download the project as [a ZIP file](https://github.com/adobe/aem-core-wcm-components/archive/master.zip)

Reportez-vous à la documentation sur l’[Utilisation des composants principaux](using.md) pour savoir comment commencer à les utiliser dans votre projet.

L’utilisation des composants principaux sur GitHub permet d’effectuer des mises à jour fréquentes et d’écouter les commentaires de la communauté des développeurs AEM. En outre, cela devrait permettre aux clients et aux partenaires de suivre des modèles similaires lors de la création de composants personnalisés.

>[!NOTE]
>
>Pour connaître les dernières modifications apportées aux composants principaux, vous pouvez consulter le [Référentiels des composants principaux](https://github.com/adobe/aem-core-wcm-components) sur GitHub.

## Bibliothèque de composants

Consultez la [Bibliothèque des composants](http://opensource.adobe.com/aem-core-wcm-components/library.html), qui présente la version actuelle des composants principaux et fournit des exemples d’utilisation.

### Exemple de contenu en mode exécution {#sample-content-run-mode}

The Core Components are visible in the Quickstart when the sample content is present, because the [We.Retail reference site](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) uses them. Toutefois, lors de l’exécution en production (en `nosamplecontent` mode exécution, sans exemple de contenu activé), les composants principaux ne sont plus présents et doivent être installés sur les instances AEM par l’équipe de développement et/ou d’exploitation.

>[!NOTE]
>
>Dans les environnements de production, exécutez toujours Quickstart en `nosamplecontent` mode exécution. Pour utiliser les composants principaux en `nosamplecontent` mode exécution, suivez les instructions de la page de documentation sur l’[la page Utilisation des composants principaux](using.md).

## Fonctionnalités techniques {#technical-capabilities}

Le tableau suivant présente les différences entre les composants principaux et les composants de base.

Pour plus d’informations sur leurs capacités de création et les options pour les préconfigurer, [reportez-vous à la page de création qui leur a été consacrée](authoring.md).

| **Fonction** | **Composant de base** | **Composant de base** |
|-----|---|---|
| Logique d’implémentation | Java POJOs with [Sling Models](https://sling.apache.org/documentation/bundles/models.html) annotations | Code JSP |
| Définition d’annotation | [Syntaxe HTML (](https://helpx.adobe.com/experience-manager/htl/user-guide.html) HTML Template Language) | Code JSP |
| Assainissement XSS | Automatisée par HTL | Essentiellement manuelle |
| Nommage des classes CSS | Standardized naming convention based on [Block Element Modifier](https://getbem.com/) (BEM) notation (as of release 2.0.0) | Modèles personnalisés |
| Définition de dialogue | [Coral 3](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Interface utilisateur Coral 2 + Classique |
| Sortie JSON | [Sling Models Exporter avec la sérialisation de Jackson](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | Servlet Sling par défaut |
| Création de versions | [Pour le modèle et le HTL](guidelines.md) | Aucun |
| Tests | Tests d’unité + Tests d’intégration | Tests d’intégration |
| Diffusion | [Via github public](https://github.com/adobe/aem-core-wcm-components) | Via Quickstart |
| Licence | [Licence Apache](https://www.apache.org/licenses/LICENSE-2.0) | Adobe propriétaire |
| Contribution | Via une requête d’extraction | Impossible |
| Accessibilité | Fully compliant with the [WCAG 2.0 AA standard](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html) | Only partially compliant with the [WCAG 2.0 AA standard](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html) |

## Liste des composants {#component-list}

Le tableau suivant répertorie les composants principaux disponibles, les liens vers leur API, et indique quels composants de base ils remplacent.

| Composant de base | Description | Composants de base remplacés |
|---|---|---|
| [Page](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page) | Page réactive travaillant avec l’éditeur de modèles | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [Chemin de navigation](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb) | Navigation dans la hiérarchie des pages | `/libs/foundation/components/breadcrumb` |
| [Titre](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v2/title) | Titre H1-H6 | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [Texte](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | Texte enrichi | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [Image](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/image/v2/image) | Chargement intelligent et différé de la taille optimale du rendu | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [Liste](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v2/list) | Liste des pages | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [Partage sur les réseaux sociaux](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/sharing/v1/sharing) | Widget de partage Facebook et Pinterest | `-` |
| [Formular-Container](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v2/container) | Système de paragraphe de formulaire réactif | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [Texte du formulaire](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v2/text) | Champ de saisie de texte | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [Options du formulaire](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v2/options) | Champ de saisie d’options multiples | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [Formulaire masqué](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v2/hidden) | Champ de saisie masqué | `/libs/foundation/components/form/hidden` |
| [Bouton de formulaire](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v2/button) | Bouton Envoyer ou personnalisé | `/libs/foundation/components/form/submit` |
| [Navigation](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/navigation/v1/navigation) | Composant de navigation sur le site qui répertorie la hiérarchie de la page imbriquée. | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [Navigation par langue](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/languagenavigation/v1/languagenavigation) | Sélecteur de langue et de pays qui répertorie la structure de langue globale. | `-` |
| [Recherche rapide](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/search/v1/search) | Un composant de recherche qui affiche les résultats sous forme de suggestions sur place dans un menu déroulant. | `/libs/foundation/components/search` |
| [Teaser](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/teaser/v1/teaser) | Permet à l’auteur de contenu de créer facilement un teaser vers un contenu supplémentaire à l’aide d’une image, d’un titre ou d’un texte enrichi et de lier un contenu supplémentaire ou d’autres actions. | `-` |
| [Onglets](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/tabs/v1/tabs) | Permet à l’auteur de contenu d’organiser le contenu de la page dans plusieurs onglets. | `-` |
| [Carrousel](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/carousel/v1/carousel) | Permet à l’auteur de contenu d’organiser le contenu dans un carrousel de diapositives. | `/libs/foundation/components/carousel` |
| [Frayer de contenu](https://github.com/adobe/aem-core-wcm-components/tree/master/extension/contentfragment/content/src/content/jcr_root/apps/core/wcm/extension/components/contentfragment/v1/contentfragment) | Autorise l’affichage d’un fragment de contenu. | `-` |
| [Liste des fractions de contenu](https://github.com/adobe/aem-core-wcm-components/tree/master/extension/contentfragment/content/src/content/jcr_root/apps/core/wcm/extension/components/contentfragmentlist/v1/contentfragmentlist) | Autorise l’affichage d’une liste de fragments de contenu. | `-` |
| [Séparateur](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/separator/v1/separator) | Sépare le contenu d’une page. | `-` |
| [Accordéon](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/accordion/v1/accordion) | Organisation des panneaux de contenu dans un accordéon réductible | `-` |
| [Conteneur](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/container/v1/container) | Organiser les composants dans un conteneur | `-` |
| [Bouton](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/button/v1/button) | Création d&#39;un bouton sur une page | `-` |
| [Télécharger](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/download/v1/download) | Ajout d&#39;un fichier téléchargeable à une page | `-` |

### Composants à venir {#upcoming-components}

Les composants principaux suivants font l’objet d’un travail intensif. They haven&#39;t been released yet, but can be previewed in the [development branch](https://github.com/adobe/aem-core-wcm-components/tree/development):

* Incorporer
* Modal

## Mise à niveau des composants principaux {#upgrade-of-core-components}

L’un des avantages des composants versionnés est qu’ils permettent de séparer la migration vers une nouvelle version AEM de la migration vers les nouvelles versions des composants. En outre, si de nouvelles versions de composants sont disponibles, elles permettent la migration individuelle de chaque composant vers la nouvelle version.

Les migrations vers une nouvelle version AEM n’affecteront pas le fonctionnement des composants principaux, à condition que leurs versions prennent également en charge la nouvelle version AEM qui est migrée. Les personnalisations apportées aux composants principaux ne devraient pas être affectées aussi longtemps qu’elles n’utilisent pas d’API [obsolètes ou supprimées](https://helpx.adobe.com/experience-manager/6-5/release-notes/deprecated-removed-features.html).

Les migrations vers de nouvelles versions des composants principaux n’auront aucune incidence sur le fonctionnement du composant. De plus, de nouvelles fonctionnalités peuvent être introduites aux auteurs de pages, ce qui peut nécessiter une configuration par un éditeur de modèle, au cas où le comportement par défaut ne serait pas souhaité. Toutefois, il est possible que des personnalisations doivent être adaptées. Pour plus d’informations, voir la page [Personnalisation des composants principaux](customizing.md#upgrade-compatibility-of-customizations).

## Quand utiliser les composants principaux ? {#when-to-use-the-core-components}

Les composants principaux étant nouveaux et offrant plusieurs avantages, il est recommandé que les nouveaux projets AEM les utilisent. Pour les projets existants, une migration doit faire partie d’un effort de projet plus volumineux, par exemple une recomposition ou une restructuration globale.

Par conséquent, Adobe propose les recommandations suivantes :

* **Nouveaux projets**
Les nouveaux projets doivent toujours tenter d’utiliser les composants principaux. Si les composants principaux ne peuvent pas être utilisés directement ou [étendus](customizing.md) pour répondre aux exigences du projet, créez un composant personnalisé d’après l’architecture du composant définie dans les composants principaux. Sauf si cela est impossible, évitez d’utiliser les [composants de base](developing.md).
* **Projets existants**
Il est recommandé de continuer à utiliser les [composants de base](developing.md), à moins qu’un site ou une restructuration de composants ne soit planifié.\
   Comme la plupart des projets existants les utilisent largement, les composants de base [continueront à être pris en charge](developing.md).
* **Nouveaux composants personnalisés**
Vous pouvez évaluer si un [composant principal existant peut être personnalisé](customizing.md).\
   Dans le cas contraire, vous devez créer un nouveau composant personnalisé suivant les [instructions des composants](guidelines.md).
* **Composants personnalisés existants**
Si vos composants fonctionnent comme prévu, conservez-les comme ils le sont.\
   Dans le cas contraire, reportez-vous à la section « Nouveaux composants personnalisés » ci-dessus.

## Migration vers les composants principaux

Tout nouveau projet doit être implémenté avec les composants principaux. Toutefois, les projets existants disposent généralement de mises en œuvre étendues des composants de base.

Un effort plus important d’un projet existant (par exemple une recomposition ou une restructuration globale) offre souvent une chance de migrer vers les composants principaux. Pour faciliter cette migration, Adobe fournit un certain nombre d’outils de migration pour encourager l’adoption des composants principaux et de la dernière technologie AEM.

[Les outils de modernisation AEM](http://opensource.adobe.com/aem-modernize-tools/) permettent de convertir facilement les éléments suivants :

* Les modèles statiques en modèles modifiables.
* La configuration de la conception en stratégies.
* Les composants de base en composants principaux.
* L’interface utilisateur classique en interface utilisateur tactile.

For further information about the usage of these tools, [see their documentation](http://opensource.adobe.com/aem-modernize-tools/).

>[!NOTE]
>
>Les outils de modernisation d&#39;AEM sont un effort communautaire et ne sont pas pris en charge ou warranciés par Adobe.

## Prise en charge des composants principaux {#core-component-support}

Les composants principaux font partie intégrante d’AEM et pris en charge en l’état, selon les mêmes conditions que s’ils étaient fournis dans le cadre de Quickstart.

Comme pour les autres fonctionnalités du produit AEM, la règle générale est la suivante : les composants sont d’abord déclarés obsolètes, puis supprimés au plus tôt pour la version AEM suivante. Cela permet aux clients d’avoir au moins un cycle de publication pour passer à la nouvelle version du composant avant l’abandon de sa prise en charge.

La version de chaque composant indique clairement les versions AEM prises en charge. Lorsque la prise en charge d’une version d’AEM est interrompue, la prise en charge des composants principaux de cette version d’AEM est prise en charge.

Pour plus d’informations sur la prise en charge des personnalisations des composants, voir la page [Personnalisation des composants principaux](customizing.md).

## Prise en charge des composants de base {#foundation-component-support}

Dans la mesure où les composants de base ont servi de fondation à une multitude de développement de projets sur de nombreuses versions d’AEM, ils seront toujours pris en charge dans un futur prévisible.

Toutefois, l’accent mis sur le développement d’Adobe a été déplacé vers les composants principaux et de nouvelles fonctionnalités leur seront ajoutées, alors que [la plupart des composants de base ont été abandonnés avec AEM 6.5](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-foundation.html) et seuls les correctifs leur seront dorénavant apportés.

**À lire aussi :**

* [Utilisation des composants principaux](using.md) - Soyez opérationnel avec les composants principaux de votre propre projet.
* [Instructions sur les composants](guidelines.md) - Pour connaître les schémas d’implémentation des composants principaux.
