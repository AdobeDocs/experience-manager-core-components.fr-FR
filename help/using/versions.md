---
title: Versions des composants principaux
seo-title: Versions des composants principaux
description: Les composants principaux sont publiés sous forme de versions qui peuvent contenir plusieurs versions des mêmes composants principaux. Ce document explique les versions et les versions et explique comment comprendre la compatibilité avec les composants principaux et AEM.
seo-description: Les composants principaux sont publiés sous forme de versions qui peuvent contenir plusieurs versions des mêmes composants principaux. Ce document explique les versions et les versions et explique comment comprendre la compatibilité avec les composants principaux et AEM.
uuid: a 916 a 923-8 c 5 e -456 a -84 b 5-b 52228 e 21434
contentOwner: Utilisateur
content-type: référence
topic-tags: introduction
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: a 3 a 98 b 2 f -65 bf -4493-82 ad -01717938 fdbc
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Versions des composants principaux{#core-components-versions}

La version actuelle des composants principaux est 2.4.0 et est compatible avec AEM 6.5. Il a été publié en mai 2019 comme une mise à jour mineure de la version 2.0.0. La version 2.0.0 introduit de nouveaux composants avec les mises à jour v 2 des composants existants.

Pour plus d&#39;informations, consultez la section [Historique des versions et compatibilité](#versions-and-releases) de ce document.

Vous pouvez également consulter la [bibliothèque](http://opensource.adobe.com/aem-core-wcm-components/library.html)de composants qui présente la version actuelle des composants principaux et fournit des exemples d&#39;utilisation.

## Versions et versions {#versions-and-releases}

Les composants principaux sont distribués via github. Cela permet à Adobe d&#39;ajouter plus rapidement des fonctionnalités aux composants et d&#39;autoriser la saisie de la communauté en dehors du cycle de publication AEM.

Les composants principaux sont disponibles avec les versions AEM définies avec lesquelles elles sont compatibles. Cela signifie qu&#39;une version AEM peut prendre en charge plusieurs versions ou versions des composants principaux. Plus de flexibilité que les anciens composants Foundation, qui étaient liés à une version spécifique d&#39;AEM.

### Versions {#versions}

Les **versions principales constituent l&#39;itération majeure des composants principaux**. Chaque composant possède une version. Les versions sont signalées avec **la valeur v** appended avec un entier positif non nul, comme v 1 et v 2. Les versions ne sont incrémentées que pour les modifications qui ne sont pas rétrocompatibles, ce qui est normalement le cas pour l&#39;introduction de nouvelles fonctionnalités et fonctionnalités.

Les développeurs et les administrateurs peuvent reconnaître les versions des composants principaux d&#39;un certain nombre dans leurs chemins de ressource et, dans le cas complet, les noms de classe Java qualifiés de leurs implémentations. Ce numéro de version représente une version majeure définie par [les directives de contrôle sémantique](https://semver.org/).

Pour plus d&#39;informations sur les versions de composants principaux, consultez la documentation [destinée aux développeurs des composants principaux](guidelines.md).

### Versions {#releases}

Les composants principaux sont disponibles via **les versions** et [représentent les artefacts publiés réels disponibles sur github](https://github.com/adobe/aem-core-wcm-components/releases). Les versions sont signalées par un nombre décimal du format X.Y.Z et rassemblent tous les composants principaux en tant que package livrable.

* **Les principales versions** peuvent introduire de nouvelles versions des composants existants avec des composants entièrement nouveaux ainsi que des correctifs standard. Elle est représentée par un incrément dans le composant X du nombre de version.

* **Les versions importantes** peuvent introduire de nouvelles fonctionnalités aux versions existantes des composants, ainsi que des correctifs. Elle est représentée par un incrément dans le composant Y du nombre de version.

* **Les versions mineures** contiennent uniquement des correctifs. Elle est représentée par un incrément dans le composant Z du nombre de version.

>[!NOTE]
>
>Les versions peuvent contenir plusieurs versions du même composant.
>
>La même version d&#39;un composant peut apparaître dans plusieurs versions.

## Historique des versions et compatibilité {#release-history-and-compatibility}

Les composants principaux ont d&#39;abord été publiés avec AEM 6.3 et sont conçus pour être flexibles et compatibles avec toutes les versions AEM prises en charge. C&#39;est pourquoi une version des composants peut contenir plusieurs versions du même composant.

Les tableaux ci-dessous illustrent la compatibilité des versions des composants principaux avec les versions des composants contenues dans les versions.

### Historique des versions et versions AEM prises en charge {#release-history-supported-aem-versions}

Le tableau suivant, dont le contenu est [disponible sur github avec les détails complets de la version](https://github.com/adobe/aem-core-wcm-components/releases), donne une vue d&#39;ensemble des versions des composants principaux et leur compatibilité avec les versions AEM et les versions Java.

| Mise à jour | Description | AEM 6.3 | AEM 6.4 | AEM 6.5 | Java |
|---|---|---|---|---|---|
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | Cette version a introduit le composant Liste de fragments de contenu | 6.3.3.0 | 6.4.2.0 | 6.5.0.0 | 1.8 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | Cette version concernait les améliorations apportées à la bibliothèque des composants, mais contient également quelques améliorations des fonctionnalités du composant Separator. | 6.3.3.0 | 6.4.2.0 | 6.5.0.0 | 1.8 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | Cette version se concentre sur la bibliothèque de composants et présente le nouveau composant Separator, mais contient également quelques améliorations des fonctionnalités du composant Image. | 6.3.3.0 | 6.4.2.0 | - | 1.8 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | Cette version concernait principalement les correctifs, mais contient également quelques améliorations des fonctionnalités du composant Carrousel. | 6.3.3.0 | 6.4.2.0 | - | 1.8 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | Composants Onglets et Carrousel introduits, améliorations apportées aux composants Image, Page et Titre et suivi amélioré | 6.3.3.0 | 6.4.2.0 | - | 1.8 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | Composant Teaser introduit, améliorations des composants d&#39;image et nombreux correctifs | 6.3.3.0 | 6.4.2.0 | 1.8 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | Version du correctif | 6.3.2.0 | 6.4.0.0 | - | 1.8 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | Améliorations supplémentaires, corrections de bogues et petites améliorations, notamment la prise en charge de la symétrie de l&#39;image. | 6.3.2.0 | 6.4.0.0 | - | 1.8 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | Améliorations principalement apportées à la persistance, à la résolution des bogues et à quelques améliorations mineures apportées aux composants Image, Page et Fragment de contenu | 6.3.2.0 | 6.4.0.0 | - | 1.8 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | Les composants Navigation, Navigation dans la langue et Recherche rapide ont été introduits. Système de style implémenté pour tous les composants. | 6.3.2.0 | 6.4.0.0 | - | 1.8 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Mise en œuvre de l&#39;exportation JSON sur tous les composants, introduction au composant Fragment de contenu | 6.3.1.0 | 6.4.0.0 | 1.8 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | Plusieurs correctifs pour le composant Image | 6.3.0.0 | 6.4.0.0 | - | 1.8 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | Correctifs du composant de page, composant d&#39;image, divers correctifs globaux et améliorations | 6.3.0.0 | 6.4.0.0 | - | 1.8 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | Correctifs des images GIF animées dans le composant Image | 6.3.0.0 | 6.4.0.0 | - | 1.7 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Version initiale des composants principaux | 6.3.0.0 | 6.4.0.0 | - | 1.7 |

>[!NOTE]
>
>Comme avec AEM, Adobe conseille aux développeurs d&#39;utiliser la [version la plus récente et les versions des composants](https://github.com/adobe/aem-core-wcm-components/releases/latest) principaux disponibles compatibles avec la version d&#39;AEM qu&#39;ils exécutent pour bénéficier des correctifs et fonctionnalités les plus récents.

### Versions et versions des composants {component-versions-and-release}

Le tableau suivant détaille les versions des composants contenant les versions des composants principaux.

|  | Version 1.0.0 - 1.0.6 | Version 1.1.0 | Version 2.0.0 - 2.0.8 | Version 2.1.0 | Version 2.2.-2.2.0 | 2.3.0 |
|---|---|---|---|---|---|---|
| **[Page](page.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Titre](title.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Image](image.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Liste](list.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Chemin de navigation](breadcrumb.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Partage sur les réseaux sociaux](sharing.md)** | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Formular-Container](form-container.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Texte du formulaire](form-text.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Options du formulaire](form-options.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Formulaire masqué](form-hidden.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Bouton de formulaire](form-button.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Fragment de contenu](content-fragment-component.md)** | Environnement de test | v1 | v1 | v1 | v1 |
| **[Navigation](navigation.md)** | v1 | v1 | v1 | v1 |
| **[Navigation par langue](language-navigation.md)** | v1 | v1 | v1 | v1 |
| **[Recherche rapide](quick-search.md)** | v1 | v1 | v1 | v1 |
| **[Teaser](teaser.md)** | v1 | v1 | v1 |
| **[Onglets](tabs.md)** | v1 | v1 |
| **[Carrousel](carousel.md)** | v1 | v1 |
| **[Séparateur](separator.md)** | v1 |

## Documentation {#documentation}

[La création avec des composants](authoring.md) principaux décrit l&#39;utilisation des composants principaux et les fonctionnalités présentées aux auteurs de contenu et aux auteurs de modèles. Chaque composant est documenté en détails.

[La bibliothèque](http://opensource.adobe.com/aem-core-wcm-components/library.html) de composants est une présentation de la version actuelle de la plupart des composants principaux, illustrant leur utilisation.

[Developing Core Components](developing.md) décrit les fonctionnalités techniques des composants principaux, comment les utiliser dans vos projets, comment personnaliser et les bonnes pratiques.

[Présentation des composants principaux présente](introduction.md) une présentation de la compatibilité des composants principaux dans les versions, les cas d&#39;utilisation et la prise en charge.
