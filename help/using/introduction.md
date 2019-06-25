---
title: Présentation des composants principaux
seo-title: Présentation des composants principaux
description: 'Les composants principaux ont été introduits afin de fournir des composants de base solides et extensibles, reposant sur les dernières technologies et les meilleures pratiques. '
seo-description: 'Les composants principaux ont été introduits afin de fournir des composants de base solides et extensibles, reposant sur les dernières technologies et les meilleures pratiques. '
uuid: b815c7d1-fbb0-4480-bd23-42606ff8b1eb
contentOwner: Utilisateur
content-type: référence
topic-tags: introduction
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: c44bb0d7-5d91-4659-878e-a0658fe29aa2
translation-type: tm+mt
source-git-commit: 7130f4ae8add8c8dc3cdfcc4addd0621722b89f7

---


# Présentation des composants principaux{#core-components-introduction}

Dans Adobe Experience Manager, les composants sont des éléments structurels qui constituent le contenu des pages en cours de création. Les composants ont toujours été un élément fondamental de l’expérience AEM, ce qui rend la création de pages simple mais puissante pour l’auteur et le développement de composants flexibles et extensibles pour le développeur.

Les composants principaux ont été introduits pour fournir des composants de base solides et extensibles, reposant sur les dernières technologies et pratiques recommandées et respecter les directives d’accessibilité et sont conformes aux normes WCAG 2.0 AA. Les composants principaux rendent la création de pages plus flexible et personnalisable, et offrent une fonctionnalité personnalisée à un développeur.

## Essayez les principaux composants.

Si vous souhaitez commencer immédiatement à essayer les composants principaux, passez en revue la [Bibliothèque de composants](http://opensource.adobe.com/aem-core-wcm-components/library.html). La bibliothèque de composants est une présentation en ligne de la version actuelle de la plupart des composants principaux, ce qui vous permet d’interagir avec des variations des composants ainsi que des exemples de sortie HTML et JSON.

The [We.Retail reference site](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html) also illustrates how the core components can be used.

## Composants principaux - Principales fonctionnalités {#core-components-core-features}

Les composants principaux sont :

|  |  |
|--- |--- |
| Préconfigurables | Les modèles peuvent définir comment les auteurs de pages peuvent les utiliser. |
| Polyvalents | Les auteurs peuvent créer la plupart du contenu avec eux. |
| Faciles à utiliser | Les auteurs peuvent créer et gérer du contenu avec efficacité. |
| Prêts pour la production | Utilisables prêts à l&#39;emploi ! Ils sont robustes, bien testés et performants. |
| Accessibles | Ils respectent la norme WCAG 2.0, fournissent des libellés ARIA et prennent en charge la navigation au clavier. |
| Faciles à styliser | Les composants implémentent le système de style et les annotations suivent le nommage BEM CSS. |
| Optimisation pour SEO | La sortie HTML est sémantique et fournit schema.org des annotations de microdonnées. |
| Prêts PWA/SPA/App | Leur sortie JSON rationalisée peut également être utilisée pour le rendu côté client. |
| Extensible | Pour couvrir les besoins personnalisés mais sans partir de zéro, tout peut être étendu. |
| Open Source | Si ce n’est pas le cas, apportez les améliorations à GitHub (licence Apache). |
| Versionnés | Les composants principaux ne scinderont pas votre site lorsque vous améliorez des éléments susceptibles d’avoir un impact sur vous. |

## Composants disponibles {#available-components}

La version actuelle des composants principaux comporte les composants suivants.

* [Accordéon](accordion.md)
* [Chemin de navigation](breadcrumb.md)
* [Bouton](button.md)
* [Conteneur](container.md)
* [Carrousel](carousel.md)
* [Fragment de contenu](content-fragment-component.md)
* [Liste des fragments de contenu](content-fragment-list.md)
* [Télécharger](download.md)
* [Bouton de formulaire](form-button.md)
* [Formular-Container](form-container.md)
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
>Les auteurs ne peuvent pas disposer immédiatement de ces composants principaux. L’[équipe de développement doit d’abord les intégrer dans leur environnement](using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) or in [design mode](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-designmode.html).

>[!CAUTION]
>
>Certaines versions de composants principaux individuels peuvent uniquement être compatibles avec certaines versions d’AEM.
>
>Pour plus d’informations, reportez-vous à la page d’aide individuelle (liée à dans la liste précédente) pour le composant spécifique ou consultez le document [Versions des composants principaux](versions.md).

## Quand utiliser les composants principaux {#when-to-use-core-components}

Les composants principaux étant nouveaux et offrant plusieurs avantages, il est recommandé que les nouveaux projets AEM les utilisent. Pour les projets existants, une migration doit faire partie d’un effort de projet plus volumineux, par exemple une recomposition ou une restructuration globale.

Pour des recommandations spécifiques, voir [Quand utiliser les composants principaux ?](developing.md) dans le document [Développement des composants principaux](developing.md).

## Présentation de la session Gems {#gems-session-overview}

Pour une présentation des composants principaux, des fonctionnalités qu’ils proposent et de leur exploitation dans AEM, consultez la session AEM Gems sur les [composants principaux AEM.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[Astuces pour Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) est une série d&#39;épisodes d&#39;épisodes techniques profonds fournis par des experts Adobe. Cette série complète la documentation du produit et de tous les autres canaux techniques, ce qui permet aux développeurs de prendre contact avec eux et d’accéder à une rubrique spécifique.

## Didacticiel du développeur WKND {#wknd-developer-tutorial}

Commencez à développer AEM Sites avec des composants principaux en suivant [ce didacticiel pas à pas.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

## Prise en charge des composants principaux {#core-components-support}

Les composants principaux font partie intégrante d’AEM et pris en charge en l’état, selon les mêmes conditions que s’ils étaient fournis dans le cadre de Quickstart.

À l’instar des autres fonctionnalités du produit, la règle générale de fin de vie est :

* Les composants sont d’abord déclarés obsolètes avant d’être supprimés.
* Ils sont ensuite retirés au plus tôt de la version d’AEM après l’annonce.

Cela donne aux clients au moins un cycle de publication pour passer à la nouvelle version du composant avant la fin de la prise en charge.

La version de chaque composant indique clairement les versions AEM prises en charge. Lorsque la prise en charge d’une version d’AEM est interrompue, la prise en charge des composants principaux de cette version d’AEM est prise en charge.

Pour plus d’informations sur la prise en charge des personnalisations des composants, consultez la page [Personnalisation des composants principaux](customizing.md) de la version des composants principaux appropriée.

## Prise en charge des composants de base {#foundation-component-support}

Dans la mesure où les composants de base ont servi de fondation à une multitude de développement de projets sur de nombreuses versions, ils seront toujours pris en charge dans un futur prévisible.

Toutefois, l’accent mis sur le développement d’Adobe a été déplacé vers les composants principaux et de nouvelles fonctionnalités leur seront ajoutées, alors que [la plupart des composants de base ont été abandonnés avec AEM 6.5](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-foundation.html) et seuls les correctifs leur seront dorénavant apportés.
