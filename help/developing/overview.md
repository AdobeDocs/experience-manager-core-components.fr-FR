---
title: Développement des composants principaux
description: Les composants principaux fournissent des composants de base robustes et extensibles qui offrent de riches fonctionnalités, une diffusion en continu, un contrôle de version des composants, une mise en œuvre moderne, un balisage Lean et une exportation JSON de contenu.
role: Architecte, développeur, administrateur
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '1445'
ht-degree: 99%

---


# Développement des composants principaux {#developing-core-components}

## Quand utiliser les composants principaux ? {#when-to-use-the-core-components}

Les composants principaux étant nouveaux et offrant plusieurs avantages, il est recommandé que les nouveaux projets AEM les utilisent. Pour les projets existants, une migration doit être envisagée dans le cadre d’un travail plus important, par exemple une création de nouvelle image ou une restructuration globale.

Par conséquent, Adobe donne les recommandations suivantes :

* **Nouveaux projets**
Les nouveaux projets doivent toujours tenter d’utiliser les composants principaux. Si les composants principaux ne peuvent pas être utilisés directement ou [étendus](customizing.md) pour répondre aux exigences du projet, créez un composant personnalisé d’après l’architecture du composant définie dans les composants principaux. Sauf si cela est impossible, évitez d’utiliser les [composants de base](/help/versions.md#foundation-component-support).
* **Projets existants**
Il est recommandé de continuer à utiliser les [composants de base](/help/versions.md#foundation-component-support), à moins qu’une restructuration de sites ou de composants ne soit planifiée.\
   Comme la plupart des projets existants les utilisent largement, les composants de base [continueront à être pris en charge](/help/versions.md#foundation-component-support).
* **Nouveaux composants personnalisés**
Vous pouvez évaluer si un [composant principal existant peut être personnalisé](customizing.md).\
   Dans le cas contraire, vous devez créer un nouveau composant personnalisé suivant les [instructions des composants](guidelines.md).
* **Composants personnalisés existants**
Si vos composants fonctionnent comme prévu, conservez-les tels quels.
\
   Dans le cas contraire, reportez-vous à la section « Nouveaux composants personnalisés » ci-dessus.

## Réussir avec les composants principaux {#how-to-succeed}

Les composants principaux sont puissants, flexibles et faciles à utiliser et personnaliser. [Suivez quelques instructions](success.md) pour vous assurer que votre projet utilisant les composants principaux soit une réussite.

## Migration vers les composants principaux

Tout nouveau projet doit être implémenté avec les composants principaux. Toutefois, les projets existants disposent généralement de mises en œuvre étendues des composants de base.

Un travail plus important sur un projet existant (par exemple une création de nouvelle image ou une restructuration globale) offre souvent une chance d’effectuer une migration vers les composants principaux. Pour faciliter cette migration, Adobe fournit un certain nombre d’outils de migration pour inciter l’adoption des composants principaux et de la dernière technologie AEM.

[Les outils de modernisation AEM](http://opensource.adobe.com/aem-modernize-tools/) permettent de convertir facilement :

* Les modèles statiques en modèles modifiables
* Les configurations de la conception en stratégies
* Les composants de base en composants principaux
* L’interface utilisateur classique en interface utilisateur tactile

Pour plus d’informations sur l’utilisation de ces outils, [voir leur documentation](http://opensource.adobe.com/aem-modernize-tools/).

>[!NOTE]
>
>Les outils de modernisation AEM ont été créés par la communauté et ne sont pas pris en charge ni garantis par Adobe.

## Prise en charge des composants principaux {#core-component-support}

Les composants principaux font partie intégrante d’AEM et sont pris en charge en l’état, selon les mêmes conditions que s’ils étaient fournis dans le cadre du Quickstart.

Comme pour les autres fonctionnalités du produit AEM, la règle générale est la suivante : les composants sont d’abord annoncés comme étant obsolètes, puis supprimés au plus tôt pour la version AEM suivante. Cela permet aux clients d’avoir au moins un cycle de publication pour passer à la nouvelle version du composant avant l’abandon de sa prise en charge.

La version de chaque composant indique clairement les versions d’AEM prises en charge. Lorsque la prise en charge d’une version d’AEM est interrompue, la prise en charge des composants principaux de cette version d’AEM est prise en charge.

Pour plus d’informations sur la prise en charge des personnalisations des composants, voir la page [Personnalisation des composants principaux](customizing.md).


## Fonctionnalités techniques {#technical-capabilities}

Le tableau ci-après présente les différences entre les composants principaux et les composants de base.

Pour plus d’informations sur leurs capacités de création et les options pour les préconfigurer, [reportez-vous à la page de création qui leur a été consacrée](/help/get-started/authoring.md).

| **Fonction** | **Composant principal** | **Composant de base** |
|-----|---|---|
| Logique d’implémentation | POJO Java avec les annotations de [modèles Sling](https://sling.apache.org/documentation/bundles/models.html). | Code JSP |
| Définition de balisage | [Syntaxe du modèle de langage HTML](https://docs.adobe.com/content/help/fr-FR/experience-manager-htl/using/overview.html) (HTL) | Code JSP |
| Assainissement XSS | Automatisée par HTL | Essentiellement manuelle |
| Nommage des classes CSS | Convention d’affectation de noms normalisée basée sur la notification [Block Element Modifier](https://getbem.com/) (BEM) (à partir de la version 2.0.0) | Modèles personnalisés |
| Définition de boîte de dialogue | [Coral 3](https://helpx.adobe.com/fr/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Interface utilisateur Coral 2 + Classique |
| Sortie JSON | [Exportateur de modèles Sling avec sérialisation Jackson](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | Servlet Sling par défaut |
| Contrôle de version | [Pour le modèle et le HTL](guidelines.md) | Aucun |
| Tests | Tests unitaires + tests d’intégration | Tests d’intégration |
| Diffusion | [Via le site GitHub public](https://github.com/adobe/aem-core-wcm-components) | Via Quickstart |
| Licence | [Licence Apache](https://www.apache.org/licenses/LICENSE-2.0) | Adobe propriétaire |
| Contribution | Via une demande d’extraction | Impossible |
| Accessibilité | Totalement conforme à la [norme WCAG 2.0 AA](https://docs.adobe.com/content/help/fr-FR/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html) | Partiellement conforme à la [norme WCAG 2.0 AA](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html) |

## Liste des composants {#component-list}

Le tableau ci-après répertorie les composants principaux disponibles, les liens vers leur API, et indique quels composants de base ils remplacent.

| Composant principal | Description | Composants de base remplacés |
|---|---|---|
| [Page](https://adobe.com/go/aem_cmp_tech_page_v2) | Page réactive fonctionnant avec l’éditeur de modèles | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [Chemin de navigation](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2) | Navigation dans la hiérarchie des pages | `/libs/foundation/components/breadcrumb` |
| [Titre](https://adobe.com/go/aem_cmp_tech_title_v2) | Titre H1-H6 | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [Texte](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | Texte enrichi | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [Image](https://adobe.com/go/aem_cmp_tech_image_v2) | Chargement intelligent et différé de la taille optimale du rendu | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [Liste](https://adobe.com/go/aem_cmp_tech_list_v2) | Liste des pages | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [Partage sur les réseaux sociaux](https://adobe.com/go/aem_cmp_tech_sharing_v1) | Widget de partage Facebook et Pinterest | `-` |
| [Conteneur de formulaires](https://adobe.com/go/aem_cmp_tech_form_container_v2) | Système de paragraphe de formulaire réactif | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [Texte du formulaire](https://adobe.com/go/aem_cmp_tech_form_text_v2) | Champ de saisie de texte | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [Options du formulaire](https://adobe.com/go/aem_cmp_tech_form_options_v2) | Champ de saisie d’options multiples | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [Formulaire masqué](https://adobe.com/go/aem_cmp_tech_form_hidden_v2) | Champ de saisie masqué | `/libs/foundation/components/form/hidden` |
| [Bouton de formulaire](https://adobe.com/go/aem_cmp_tech_form_button_v2) | Bouton Envoyer ou personnalisé | `/libs/foundation/components/form/submit` |
| [Navigation](https://adobe.com/go/aem_cmp_tech_navigation_v1) | Composant de navigation sur le site qui répertorie la hiérarchie de la page imbriquée | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [Navigation par langue](https://adobe.com/go/aem_cmp_tech_langnav_v1) | Sélecteur de langue et de pays qui répertorie la structure de langue globale | `-` |
| [Recherche rapide](https://adobe.com/go/aem_cmp_tech_search_v1) | Composant de recherche qui affiche les résultats sous forme de suggestions sur place dans un menu déroulant | `/libs/foundation/components/search` |
| [Teaser](https://adobe.com/go/aem_cmp_tech_teaser_v1) | Permet à l’auteur de contenu de créer facilement un teaser vers un contenu supplémentaire à l’aide d’une image, d’un titre ou d’un texte enrichi et de lier un contenu supplémentaire ou d’effectuer d’autres actions | `-` |
| [Onglets](https://adobe.com/go/aem_cmp_tech_tabs_v1) | Permet à l’auteur de contenu d’organiser le contenu de la page dans plusieurs onglets | `-` |
| [Carrousel](https://adobe.com/go/aem_cmp_tech_carousel_v1) | Permet à l’auteur de contenu d’organiser le contenu dans un carrousel de diapositives | `/libs/foundation/components/carousel` |
| [Fragment de contenu](https://adobe.com/go/aem_cmp_tech_cf_v1) | Permet l’affichage d’un fragment de contenu | `-` |
| [Liste de fragments de contenu](https://adobe.com/go/aem_cmp_tech_cflist_v1) | Permet l’affichage d’une liste de fragments de contenu | `-` |
| [Séparateur](https://adobe.com/go/aem_cmp_tech_separator_v1) | Sépare le contenu d’une page | `-` |
| [Accordéon](https://adobe.com/go/aem_cmp_tech_accordion_v1) | Organise les panneaux de contenu dans un accordéon réductible | `-` |
| [Conteneur](https://adobe.com/go/aem_cmp_tech_container_v1) | Organise les composants dans un conteneur | `-` |
| [Bouton](https://adobe.com/go/aem_cmp_tech_button_v1) | Crée un bouton sur une page | `-` |
| [Téléchargement](https://adobe.com/go/aem_cmp_tech_download_v1) | Ajoute une ressource téléchargeable à une page | `-` |
| [Fragment d’expérience](https://adobe.com/go/aem_cmp_tech_xf_v1) | Ajout d’un fragment d’expérience à une page | `/libs/cq/experience-fragments/editor/components/experiencefragment` |
| [Incorporer](https://adobe.com/go/aem_cmp_tech_embed_v1) | Incorporation d’une ressource externe dans une page | - |
| [Barre de progression](https://adobe.com/go/aem_cmp_tech_progress_v1) | Fournit une représentation visuelle de la progression par rapport à un objectif | - |
| [Visionneuse PDF](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1) | Présente un document PDF sur une page | - |

### Composants à venir {#upcoming-components}

Pour obtenir un aperçu de la feuille de route des composants principaux à venir, voir le [wiki du projet sur GitHub](https://github.com/adobe/aem-core-wcm-components/wiki/home).

## Mise à niveau des composants principaux {#upgrade-of-core-components}

L’un des avantages des composants versionnés est qu’ils permettent de séparer la migration vers une nouvelle version d’AEM de la migration vers les nouvelles versions des composants. En outre, si de nouvelles versions de composants sont disponibles, ils permettent la migration individuelle de chaque composant vers la nouvelle version.

Les migrations vers une nouvelle version d’AEM n’auront aucune incidence sur le fonctionnement des composants principaux, à condition que leurs versions prennent également en charge la nouvelle version d’AEM vers laquelle est effectuée la migration. Les personnalisations apportées aux composants principaux ne doivent pas être affectées tant qu’elles n’utilisent pas d’API [obsolètes ou supprimées](https://docs.adobe.com/content/help/fr-FR/experience-manager-cloud-service/release-notes/deprecated-removed-features.html).

Les migrations vers de nouvelles versions des composants principaux n’auront aucune incidence sur le fonctionnement du composant. De plus, de nouvelles fonctionnalités peuvent être ajoutées pour les auteurs de pages, ce qui peut nécessiter une configuration par un éditeur de modèles, au cas où le comportement par défaut ne serait pas souhaité. Il est toutefois possible que des personnalisations doivent être adaptées. Pour plus d’informations, voir la page [Personnalisation des composants principaux](customizing.md#upgrade-compatibility-of-customizations).
