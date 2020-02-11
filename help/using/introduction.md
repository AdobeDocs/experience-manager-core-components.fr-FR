---
title: Présentation des composants principaux
description: 'Les composants principaux ont été conçus pour offrir des composants de base solides et extensibles, reposant sur les dernières technologies et les bonnes pratiques. '
translation-type: tm+mt
source-git-commit: 5439f90faef28c72367419bb7429a3a880b65229

---


# Présentation des composants principaux{#core-components-introduction}

Dans Adobe Experience Manager, les composants sont des éléments structurels qui constituent le contenu des pages en cours de création. Les composants ont toujours été un élément fondamental de l’expérience AEM. Ils facilitent la création de pages pour l’auteur et le développement de composants flexibles et extensibles pour le développeur.

Les composants principaux ont été conçus pour offrir des composants de base solides et extensibles, reposant sur les dernières technologies et les bonnes pratiques et respectant les directives d’accessibilité. Ils sont en outre conformes aux normes WCAG 2.0 AA. Les composants principaux rendent la création de pages plus flexible et personnalisable. Ils offrent aux développeurs une fonctionnalité personnalisée.

## Essai des composants principaux

Si vous souhaitez commencer immédiatement à essayer les composants principaux, passez en revue la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library). La bibliothèque de composants est une présentation en ligne de la version actuelle de la plupart des composants principaux, ce qui permet d’interagir avec des variantes des composants, ainsi que des exemples de sortie HTML et JSON.

The [WKND tutorial](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html) also illustrates how the core components can be used.

## Composants principaux - Principales fonctionnalités {#core-components-core-features}

Les composants principaux sont :

|  |  |
|--- |--- |
| Préconfigurables | Les modèles peuvent définir comment les auteurs de pages peuvent les utiliser. |
| Polyvalents | Les auteurs peuvent créer la plupart du contenu avec eux. |
| Faciles à utiliser | Les auteurs peuvent créer et gérer du contenu avec efficacité. |
| Prêts pour la production | Utilisables prêts à l’emploi Ils sont robustes, bien testés et performants. |
| Accessibles | Ils sont conformes à la norme WCAG 2.0, fournissent des libellés ARIA et prennent en charge la navigation au clavier. |
| Faciles à styliser | Les composants implémentent le système de style et les annotations suivent l’attribution de noms BEM CSS. |
| Optimisation pour SEO | La sortie HTML est sémantique et fournit des annotations de microdonnées schema.org. |
| Prêts PWA/SPA/App | Leur sortie JSON rationalisée peut également être utilisée pour le rendu côté client. |
| Extensibles | Pour couvrir les besoins personnalisés mais sans partir de zéro, tout peut être étendu. |
| Open Source | Si quelque chose n’est pas comme il le devrait, apportez des améliorations sur GitHub (licence Apache). |
| Versionnés | Les composants principaux n’endommageront pas votre site lorsque vous apportez des améliorations susceptibles d’avoir un impact sur vous. |
| [Localisé](localization.md) | La résolution intelligente des références permet à certains composants de rechercher le contenu localisé correspondant et d’en effectuer automatiquement le rendu. |

## Composants disponibles {#available-components}

La version actuelle des composants principaux comporte les composants ci-après.

* [Accordéon](accordion.md)
* [Chemin de navigation](breadcrumb.md)
* [Bouton](button.md)
* [Conteneur](container.md)
* [Carrousel](carousel.md)
* [Fragment de contenu](content-fragment-component.md)
* [Liste de fragments de contenu](content-fragment-list.md)
* [Téléchargement](download.md)
* [Incorporer](embed.md)
* [Fragment d’expérience](experience-fragment.md)
* [Bouton de formulaire](form-button.md)
* [Conteneur de formulaires](form-container.md)
* [Formulaire masqué](form-hidden.md)
* [Options du formulaire](form-options.md)
* [Texte du formulaire](form-text.md)
* [Image](image.md)
* [Navigation par langue](language-navigation.md)
* [Liste](list.md)
* [Navigation](navigation.md)
* [Page](page.md)
* [Recherche rapide](quick-search.md)
* [Séparateur](separator.md)
* [Partage sur les réseaux sociaux](sharing.md)
* [Onglets](tabs.md)
* [Texte](text.md)
* [Titre](title.md)

>[!NOTE]
>
>Les auteurs ne peuvent pas disposer immédiatement de ces composants principaux. En effet, l’[équipe de développement doit d’abord les intégrer dans leur environnement](using.md). Une fois intégrés, ils peuvent être rendus disponibles et préconfigurés dans l’[éditeur de modèles](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!CAUTION]
>
>Certaines versions de composants principaux peuvent uniquement être compatibles avec certaines versions d’AEM.
>
>Pour plus d’informations, reportez-vous à la page d’aide (liée dans la liste précédente) pour le composant spécifique ou consultez le document [Versions des composants principaux](versions.md).

## Quand utiliser les composants principaux {#when-to-use-core-components}

Les composants principaux étant nouveaux et offrant plusieurs avantages, il est recommandé que les nouveaux projets AEM les utilisent. Pour les projets existants, une migration doit être envisagée dans le cadre d’un travail plus important, par exemple une création de nouvelle image ou une restructuration globale.

Pour des recommandations spécifiques, voir [Quand utiliser les composants principaux ?](developing.md) dans le document [Développement des composants principaux](developing.md).

## Présentation de la session Gems {#gems-session-overview}

Pour une présentation des composants principaux, des fonctionnalités qu’ils proposent et de leur utilisation dans AEM, consultez la session AEM Gems sur les [composants principaux AEM.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[Gems sur Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) est une série de séances approfondies sur des aspects techniques réalisées par des experts Adobe. Cette série complète la documentation du produit et de tous les autres canaux techniques, ce qui permet aux développeurs de communiquer entre eux et d’approfondir un sujet spécifique.

## Développement avec les composants principaux {#developing-core-components}

Les composants principaux fournissent des composants de base robustes et extensibles qui implémentent plusieurs modèles permettant une personnalisation facile, de la mise en forme simple à la réutilisation des fonctionnalités avancées. Pour en savoir plus, consultez la [documentation relative au développement des composants principaux](developing.md).

Get started developing AEM Sites with Core Components by following [the WKND tutorial.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

N’oubliez pas de démarrer votre propre projet AEM en exploitant l’[archétype de projet AEM](overview.md) dotés des tout derniers composants principaux intégrés.

## Prise en charge des composants principaux {#core-components-support}

Les composants principaux font partie intégrante d’AEM et sont pris en charge en l’état, selon les mêmes conditions que s’ils étaient fournis dans le cadre du Quickstart.

À l’instar des autres fonctionnalités du produit, la règle générale de fin de vie est la suivante :

* Les composants sont d’abord annoncés comme étant obsolètes avant d’être supprimés.
* Ils sont ensuite retirés au plus tôt de la version d’AEM après l’annonce.

Les clients disposent ainsi d’au moins un cycle de publication pour passer à la nouvelle version du composant avant la fin de la prise en charge.

La version de chaque composant indique clairement les versions d’AEM prises en charge. Lorsque la prise en charge d’une version d’AEM est interrompue, la prise en charge des composants principaux de cette version d’AEM est prise en charge.

Pour plus d’informations sur la prise en charge des personnalisations des composants, consultez la page [Personnalisation des composants principaux](customizing.md) de la version des composants principaux appropriée.

## Prise en charge des composants de base {#foundation-component-support}

Dans la mesure où les composants de base ont servi de fondation à une multitude de développement de projets sur de nombreuses versions, ils seront toujours pris en charge dans un futur prévisible.

Toutefois, Adobe met désormais l’accent sur les composants principaux et de nouvelles fonctionnalités leur seront ajoutées, alors que la [plupart des composants de base ont été abandonnés avec AEM 6.5](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) et seuls les correctifs leur seront dorénavant appliqués.
