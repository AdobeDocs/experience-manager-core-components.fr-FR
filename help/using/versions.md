---
title: Versions des composants principaux
description: Les composants principaux sont publiés sous forme de versions qui peuvent contenir plusieurs versions des mêmes composants principaux. Ce document explique les versions et les mises à jour ainsi que comment comprendre la compatibilité avec les composants principaux et AEM.
translation-type: tm+mt
source-git-commit: 080f53582cfa758aa99ec491f261af7cde1f5ea7

---


# Versions des composants principaux {#core-components-versions}

La version actuelle des composants principaux est la version 2.8.0 et est compatible avec [AEM en tant que service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) cloud et avec les installations AEM [](https://docs.adobe.com/content/help/en/experience-manager-65/user-guide/home.html) sur site. Il a été publié en décembre 2019 comme une mise à jour importante de la version 2.0.0. La version 2.0.0 introduit de nouveaux composants ainsi que des mises à jour v2 des composants existants.

Pour plus d’informations, voir la section [Historique des versions et compatibilité](#versions-and-releases) de ce document.

Vous pouvez également consulter la [Bibliothèque de composants](https://adobe.com/go/aem_cmp_library), qui présente la version actuelle des composants principaux et fournit des exemples d’utilisation.

## Versions et mises à jour {#versions-and-releases}

Les composants principaux sont distribués via GitHub. Cela permet à Adobe d’ajouter plus rapidement des fonctionnalités aux composants et d’autoriser la saisie de la communauté en dehors du cycle de publication AEM.

Les composants principaux sont disponibles avec les versions AEM définies avec lesquelles ils sont compatibles. Cela signifie qu’une version AEM peut prendre en charge plusieurs versions ou mises à jour des composants principaux. Cela donne plus de flexibilité par rapport aux anciens composants de base, qui étaient liés à une version spécifique d’AEM.

### Versions {#versions}

Les **versions** principales constituent l’itération majeure des composants principaux. Chaque composant possède une version. Les versions sont signalées avec la valeur **v** inscrite avec un entier positif non nul, comme v1 et v2. Les versions ne sont incrémentées que pour les modifications qui ne sont pas rétrocompatibles, ce qui est normalement le cas pour l’introduction de nouvelles fonctionnalités et fonctions.

Les développeurs et les administrateurs peuvent reconnaître les versions des composants principaux par un numéro figurant dans leurs chemins d’accès aux types de ressources et dans les noms de classe Java pleinement qualifiés de leurs implémentations. Ce numéro de version représente une version majeure définie par [les directives de contrôle de version sémantique](https://semver.org/).

Pour plus d’informations sur les versions des composants principaux, voir la [documentation destinée aux développeurs des composants principaux](guidelines.md).

### Mises à jour {#releases}

Les composants principaux sont disponibles par l’intermédiaire des **mises à jour** et [représentent les artefacts publiés réels disponibles sur GitHub](https://github.com/adobe/aem-core-wcm-components/releases). Les versions sont signalées par un nombre décimal du format X.Y.Z et rassemblent tous les composants principaux en tant que package livrable.

* **Les mises à jour majeures** peuvent introduire de nouvelles versions des composants existants avec des composants entièrement nouveaux ainsi que des correctifs standards. Elles sont représentées par un incrément dans le composant X du numéro de version.
* **Les mises à jour importantes** peuvent introduire de nouvelles fonctionnalités aux versions existantes des composants, ainsi que des correctifs. Elles sont représentées par un incrément dans le composant Y du numéro de version.
* **Les mises à jour mineures** contiennent uniquement des correctifs. Elles sont représentées par un incrément dans le composant Z du numéro de version.

>[!NOTE]
>
>Les versions peuvent contenir plusieurs versions du même composant.
>
>La même version d’un composant peut apparaître dans plusieurs versions.

## Historique des versions et compatibilité {#release-history-and-compatibility}

Les composants principaux ont d’abord été publiés avec AEM 6.3 et sont conçus pour être flexibles et compatibles avec toutes les versions AEM prises en charge. C’est pourquoi une mise à jour des composants peut contenir plusieurs versions du même composant.

Les tableaux ci-dessous illustrent la compatibilité des mises à jour des composants principaux avec les versions des composants contenues dans les mises à jour.

### Historique des versions et mises à jour AEM prises en charge {#release-history-supported-aem-versions}

Le tableau suivant, dont le contenu est [disponible sur GitHub avec les détails complets de la mise à jour](https://github.com/adobe/aem-core-wcm-components/releases), donne une vue d’ensemble des versions des composants principaux et de leur compatibilité avec les versions AEM et les versions Java.

| Mise à jour | Description | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM en tant que service cloud | Java | Date de publication |
|---|---|---|---|---|---|---|---|
| [2.8.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0) | Cette version comprend principalement des correctifs ainsi que de petites améliorations. | 6.3.3.4+ | 6.4.4.0+ | 6.5.0.0+ | Continu | 8, 11 | 5 décembre 2019 |
| [2.7.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0) | Cette version a introduit le nouveau composant Incorporer. | 6.3.3.4+ | 6.4.4.0+ | 6.5.0.0+ | Continu | 8, 11 | 25 septembre 2019 |
| [2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | Cette version a introduit le nouveau composant de fragment d’expérience. | 6.3.3.4+ | 6.4.4.0+ | 6.5.0.0+ | Continu | 8, 11 | 6 septembre 2019 |
| [2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | Les nouveaux composants Accordéon, Bouton, Conteneur et Téléchargement ont été ajoutés dans cette version. | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | Continu | 8, 11 | 25 juin 2019 |
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | Cette version a introduit le composant Liste de fragments de contenu. | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | Continu | 8, 11 | 7 mai 2019 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | Cette version concernait les améliorations apportées à la bibliothèque de composants, mais contient également quelques améliorations des fonctionnalités du composant Séparateur. | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | Continu | 8 | 14 mars 2019 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | Cette version se concentre sur la bibliothèque de composants et présente le nouveau composant Séparateur, mais contient également quelques améliorations des fonctionnalités du composant Image. | 6.3.3.0+ | 6.4.2.0+ | - | - | 8 | 11 février 2019 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | Cette version concerne principalement les correctifs, mais contient également quelques améliorations des fonctionnalités du composant Carrousel. | 6.3.3.0+ | 6.4.2.0+ | - | - | 8 | 27 novembre 2018 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | Les composants Onglets et Carrousel sont introduits et des améliorations sont apportées aux composants Image, Page et Titre avec un suivi amélioré. | 6.3.3.0+ | 6.4.2.0+ | - | - | 8 | 16 octobre 2018 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | Le composant Teaser est introduit et des améliorations du composant Image et de nombreux correctifs sont apportés. | 6.3.3.0+ | 6.4.2.0+ | - | - | 8 | 13 juillet 2018 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | Version du correctif | 6.3.2.0+ | 6.4.0.0+ | - | - | 8 | 12 juin 2018 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | Améliorations supplémentaires, corrections de bogues et petites améliorations, notamment la prise en charge de la symétrie de l’image. | 6.3.2.0+ | 6.4.0.0+ | - | - | 8 | 11 avril 2018 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | Améliorations principalement apportées à la persistance, à la résolution des bogues et à quelques améliorations mineures apportées aux composants Image, Page et Fragment de contenu. | 6.3.2.0+ | 6.4.0.0+ | - | - | 8 | 7 mars 2018 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | Les composants Navigation, Langue de Navigation et Recherche rapide ont été introduits. Système de style implémenté pour tous les composants. | 6.3.2.0+ | 6.4.0.0+ | - | - | 8 | 16 janvier 2018 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Mise en œuvre de l’exportation JSON sur tous les composants, introduction au composant Fragment de contenu. | 6.3.1.0 | 6.4.0.0+ | - | - | 8 | 10 octobre 2017 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | Plusieurs correctifs pour le composant Image. | 6.3.0.0+ | 6.4.0.0+ | - | - | 8 | 4 août 2017 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | Correctifs du composant Page, composant Image, divers correctifs globaux et améliorations. | 6.3.0.0+ | 6.4.0.0+ | - | - | 8 | 26 avril 2017 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | Correctifs des images GIF animées dans le composant Image. | 6.3.0.0+ | 6.4.0.0+ | - | - | 7 | 22 mars 2017 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Version initiale des composants principaux. | 6.3.0.0+ | 6.4.0.0+ | - | - | 7 | 20 mars 2017 |

>[!NOTE]
>
>Comme avec AEM, Adobe conseille aux développeurs d’utiliser la [mise à jour et les versions les plus récentes disponibles des composants principaux](https://github.com/adobe/aem-core-wcm-components/releases/latest), compatibles avec la version d’AEM qu’ils exécutent pour bénéficier des correctifs et fonctionnalités les plus récents.

### Versions et versions des composants {#component-versions-and-releases}

Le tableau suivant répertorie les versions des composants contenus dans les versions des composants principaux.

|  | Version 1.0.0 - 1.0.6 | Version 1.1.0 | Version 2.0.0 - 2.0.8 | Version 2.1.0 | Version 2.2.0 - 2.2.0 | Version 2.3.0 - 2.3.2 | Version 2.4.0 | Version 2.5.0 | Version 2.6.0 | Version 2.7.0+ |
|---|---|---|---|---|---|---|---|---|---|---|
| **[Page](page.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Titre](title.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Image](image.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Liste](list.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Chemin de navigation](breadcrumb.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Partage sur les réseaux sociaux](sharing.md)** | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Conteneur de formulaires](form-container.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Texte du formulaire](form-text.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Options du formulaire](form-options.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formulaire masqué](form-hidden.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Bouton de formulaire](form-button.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Fragment de contenu](content-fragment-component.md)** |  | Environnement de test | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Navigation](navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Navigation par langue](language-navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Recherche rapide](quick-search.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Teaser](teaser.md)** |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Onglets](tabs.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Carrousel](carousel.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Séparateur](separator.md)** |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 |
| **[Liste de fragments de contenu](content-fragment-list.md)** |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Accordéon](accordion.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Bouton](button.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Conteneur](separator.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Téléchargement](separator.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Fragment d’expérience](separator.md)** |  |  |  |  |  |  |  |  | v1 | v1 |
| **[Incorporer](separator.md)** |  |  |  |  |  |  |  |  |  | v1 |

## Documentation {#documentation}

[La création avec des composants](authoring.md) principaux décrit l’utilisation des composants principaux et les fonctionnalités présentées aux auteurs de contenu et aux auteurs de modèles. Chaque composant est documenté en détail.

La [bibliothèque de composants](https://adobe.com/go/aem_cmp_library) est une présentation de la version actuelle de la plupart des composants principaux, illustrant leur utilisation.

[Le développement des composants principaux](developing.md) décrit les fonctionnalités techniques des composants principaux, comment les utiliser dans vos projets, comment personnaliser et les bonnes pratiques.

[Présentation des composants principaux](introduction.md) donne un aperçu de la compatibilité des composants principaux dans les versions, les cas d’utilisation et la prise en charge.

Le [tutoriel WKND](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) est une excellente introduction au développement pour AEM, notamment à l’utilisation des composants principaux.
