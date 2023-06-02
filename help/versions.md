---
title: Versions des composants principaux
description: Les composants principaux sont publiés sous forme de versions qui peuvent contenir plusieurs versions des mêmes composants principaux. Ce document explique les versions et les mises à jour ainsi que comment comprendre la compatibilité avec les composants principaux et AEM.
role: Architect, Developer, Admin, User
exl-id: 7d4dbe46-4013-4217-b815-cdb1462072c6
source-git-commit: b7b06b5760e233756a0e8906251fa3b8ab401908
workflow-type: tm+mt
source-wordcount: '3006'
ht-degree: 99%

---

# Versions des composants principaux {#core-components-versions}

La version actuelle des composants principaux est la version 2.22.12. Elle est compatible avec les installations [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=fr) et [AEM On-Premise](https://experienceleague.adobe.com/docs/experience-manager-65/user-guide/home.html?lang=fr).

## Historique des versions et compatibilité {#release-history-and-compatibility}

Les composants principaux sont conçus pour être flexibles et compatibles avec toutes les versions d’AEM prises en charge. C’est pourquoi une mise à jour des composants peut contenir plusieurs versions du même composant.

Les tableaux ci-dessous illustrent la compatibilité des mises à jour des composants principaux avec les versions des composants contenues dans les mises à jour.

### Historique des versions et configuration requise {#release-history-requirements}

Le tableau suivant, dont le contenu est [disponible sur GitHub avec les détails complets de la mise à jour](https://github.com/adobe/aem-core-wcm-components/releases), donne une vue d’ensemble des versions des composants principaux et de leur compatibilité avec les versions AEM et les versions Java.

| Mise à jour | Description | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service | Java | Date de publication |
|---|---|---|---|---|---|---|
| [2.22.12](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.12) | Cette version de correctif corrige deux problèmes. | - | 6.5.14.0+ * | En continu | 8, 11 | 25 mai 2023 |
| [2.22.10](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.10) | Cette version de correctif corrige deux régressions. | - | 6.5.14.0+ * | En continu | 8, 11 | 11 mai 2023 |
| [2.22.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.8) | Cette version de correctif réintroduit les fonctionnalités qui ont été supprimées accidentellement dans la version précédente. | - | 6.5.14.0+ * | En continu | 8, 11 | 9 mai 2023 |
| [2.22.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.6) | Cette version de correctif corrige une régression dans le [composant Conteneur.](/help/components/container.md) | - | 6.5.14.0+ * | En continu | 8, 11 | 21 avril 2023 |
| [2.22.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.4) | Il s’agit d’une version de correctif qui corrige un problème dans le [composant Liste de fragments de contenu.](/help/components/content-fragment-list.md) | - | 6.5.14.0+ * | En continu | 8, 11 | 5 avril 2023 |
| [2.22.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.2) | Il s’agit d’une version de maintenance qui résout deux problèmes introduits dans la version 2.22.0. | - | 6.5.14.0+ * | En continu | 8, 11 | 31 mars 2023 |
| [2.22.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.0) | Cette version introduit une nouvelle version du [composant Liste](/help/components/list.md) ainsi que des améliorations de la fonction [Teaser](/help/components/teaser.md) et une mise à jour de la [Visionneuse PDF](/help/components/pdf-viewer.md) et du [Carrousel](/help/components/carousel.md). | - | 6.5.14.0+ * | En continu | 8, 11 | 9 février 2023 |
| [2.21.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.21.2) | Il s’agit d’une version de correctif qui corrige un problème lié aux [composants du teaser](/help/components/teaser.md) des versions v1 et v2. | - | 6.5.13.0+ * | En continu | 8, 11 | 12 septembre 2022 |
| [2.21.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.21.0) | Cette version comprend plusieurs améliorations, notamment la publication de l’API LinkHandler, des améliorations du [composant Image](/help/components/image.md) et de la [couche de données,](/help/developing/data-layer/overview.md) ainsi que des améliorations des composants à plusieurs panneaux. | - | 6.5.13.0+ * | En continu | 8, 11 | 12 septembre 2022 |
| [2.20.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.8) | Cette version corrige un problème lié à la diffusion des images SVG via l’AdaptiveImageServlet. | - | 6.5.13.0+ * | En continu | 8, 11 | 4 août 2022 |
| [2.20.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.6) | Cette version de correctif corrige un problème lié au nouveau [composant Table des matières.](/help/components/tableofcontents.md) | - | 6.5.13.0+ * | En continu | 8, 11 | 7 juillet 2022 |
| [2.20.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.4) | Cette version de correctif corrige un problème lié au nouveau [composant Table des matières.](/help/components/tableofcontents.md) | - | 6.5.13.0+ * | En continu | 8, 11 | 29 juin 2022 |
| [2.20.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.2) | Il s’agit d’une version de correctif qui corrige un problème dans le nouveau [service de diffusion de ressources optimisées pour le web](/help/developing/web-optimized-image-delivery.md) d’AEMaaCS. | - | 6.5.13.0+ * | En continu | 8, 11 | 20 juin 2022 |
| [2.20.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.0) | Cette version comprend un nouveau [composant Table des matières](/help/components/tableofcontents.md), prend en charge le [service de diffusion de ressources optimisées pour le web](/help/developing/web-optimized-image-delivery.md) d’AEMaaCS et comprend des correctifs. | - | 6.5.13.0+ * | En continu | 8, 11 | 9 juin 2022 |
| [2.19.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.19.0) | Cette version ajoute une nouvelle version au [Composant de recherche](/help/components/quick-search.md) et des fonctionnalités à la fonction [Composant de bouton](/help/components/button.md) ainsi que de nombreuses améliorations de l’accessibilité et correctifs de bogues. | - | 6.5.10.0+ * | En continu | 8, 11 | 7 avril 2022 |
| [2.18.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.18.8) | Cette version corrige un problème pour AEMaaCS. | - | 6.5.10.0+ * | En continu | 8, 11 | 17 mars 2022 |
| [2.18.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.18.6) | Il s’agit d’une version de correctif. | - | 6.5.10.0+ * | En continu | 8, 11 | 3 mars 2022 |
| [2.18.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.18.0) | Cette version majeure des composants principaux contient les améliorations suivantes : introduction d’un nouveau gestionnaire de liens dans les nouvelles versions de plusieurs composants, nombreuses améliorations en matière dʼaccessibilité et correctifs de bugs. | - | 6.5.10.0+ * | En continu | 8, 11 | 16 février 2022 |
| [2.17.14](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.12) | Il s’agit d’une version de correctif. | 6.4.8.4+ * | 6.5.6.0+ * | En continu | 8, 11 | 13 décembre 2021 |
| [2.17.12](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.12) | Il s’agit d’une version de correctif qui corrige une régression introduite dans la version précédente. | 6.4.8.4+ * | 6.5.6.0+ * | En continu | 8, 11 | 1 octobre 2021 |
| [2.17.10](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.10) | Ce correctif améliore les composants [Liste](/help/components/list.md) et [Navigation](/help/components/navigation.md) pour afficher l’URL externe pour les cibles de redirection, active l’héritage des images de page pour la version v2 à venir du composant [Teaser](/help/components/teaser.md) et contient des correctifs supplémentaires. | 6.4.8.4+ * | 6.5.6.0+ * | En continu | 8, 11 | 31 août 2021 |
| [2.17.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.8) | Cette version de correctif Il s’agit d’une version de correctif permettant de corriger une modification rétrocompatible introduite précédemment. | 6.4.8.4+ * | 6.5.6.0+ * | En continu | 8, 11 | 2 août 2021 |
| [2.17.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.6) | Cette version de correctif prend en charge les cartes du site pour des pages et comprend différentes améliorations d’accessibilité. | 6.4.8.4+ * | 6.5.6.0+ * | En continu | 8, 11 | 29 juillet 2021 |
| [2.17.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.2) | Cette version de correctif vient corriger la [couche de données](/help/developing/data-layer/overview.md) qui ne fonctionne pas avec AEMaaCS. | 6.4.8.4+ * | 6.5.6.0+ * | En continu | 8, 11 | 8 juillet 2021 |
| [2.17.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.0) | Cette version comprend des aperçus techniques de nombreuses nouvelles versions de composants prenant en charge les fonctionnalités de gestionnaire de liens, ainsi qu’un aperçu technique d’une fonctionnalité d’image présentée pour le [composant de page.](/help/components/page.md) Plusieurs correctifs sont également inclus. | 6.4.8.4+ * | 6.5.6.0+ * | En continu | 8, 11 | 16 juin 2021 |
| [2.16.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.4) | Il s’agit d’une version de correctif permettant de résoudre un problème lié au nouveau gestionnaire de liens. | 6.4.8.1+ * | 6.5.5.0+ * | En continu | 8, 11 | 19 mai 2021 |
| [2.16.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.2) | Il s’agissait d’une version de correctif qui corrigeait principalement un problème avec le nouveau gestionnaire de liens et ajoutait une amélioration pour la prise en charge des applications de plusieurs pages pour [PWA](/help/components/page.md#pwa-support). | 6.4.8.1+ * | 6.5.5.0+ * | En continu | 8, 11 | 15 mai 2021 |
| [2.16.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.0) | Cette version s’est concentrée sur les améliorations de l’accessibilité et sur l’introduction d’un nouveau gestionnaire de liens dans les composants existants. | 6.4.8.1+ * | 6.5.5.0+ * | En continu | 8, 11 | 22 avril 2021 |
| [2.15.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.15.2) | Cette version de correctif corrigeait principalement des problèmes de compatibilité ascendante [de la couche de données](/help/developing/data-layer/overview.md) et de tests informatiques qui échouaient dans certaines situations. | 6.4.8.1+ * | 6.5.5.0+ * | En continu | 8, 11 | 16 mars 2021 |
| [2.15.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.15.0) | Cette version comprend la prise en charge des [applications web progressives dans le composant Page](/help/components/page.md#pwa-support) ainsi que la version 2.0.0 de la [couche de données Adobe.](/help/developing/data-layer/overview.md) | 6.4.8.1+ * | 6.5.5.0+ * | En continu | 8, 11 | 23 février 2021 |
| [2.14.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.14.0) | Cette version comprend de nouvelles options pour le [composant Incorporer](/help/components/embed.md), introduit le slug de marque au niveau de la [page](/help/components/page.md), et corrige de nombreux problèmes. | 6.4.8.1+ * | 6.5.5.0+ * | En continu | 8, 11 | 9 février 2021 |
| [2.13.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.2) | Il s’agissait d’une version de correctif destinée à corriger un problème lié au RTE, utilisé sur AEMaaCS. | 6.4.8.1+ * | 6.5.5.0+ * | En continu | 8, 11 | 16 décembre 2020 |
| [2.13.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.0) | Cette version contient de nouvelles fonctionnalités Dynamic Media pour le [composant d’image](/help/components/image.md). | 6.4.8.1+ * | 6.5.5.0+ * | En continu | 8, 11 | 4 décembre 2020 |
| [2.12.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.2) | Il s’agissait d’une version de correctif pour la version 2.12.0 contenant des corrections mineures. | 6.4.8.1+ * | 6.5.5.0+ * | En continu | 8, 11 | 11 novembre 2020 |
| [2.12.1](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.1) | Il s’agissait d’une version de correctif pour la version 2.12.0 servant à corriger un bogue majeur dans le [composant d’image](/help/components/image.md). | 6.4.8.1+ * | 6.5.5.0+ * | En continu | 8, 11 | 5 novembre 2020 |
| [2.12.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.0) | Cette version a introduit [un nouveau gestionnaire de formulaires POST ;](/help/components/forms/form-container.md#post-data) la possibilité d’inclure des [balises CSS, JavaScript et de métadonnées personnalisées via une configuration contextuelle ;](/help/developing/including-clientlibs.md#context-aware-loading) et un utilitaire `DataLayerBuilder` destiné à [simplifier l’intégration de la couche de données aux composants personnalisés.](/help/developing/data-layer/integrations.md#enabling-custom-components) | 6.4.8.1+ * | 6.5.5.0+ * | En continu | 8, 11 | 29 octobre 2020 |
| [2.11.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.11.0) | Cette version a introduit la [prise en charge d’AMP.](/help/developing/amp.md) | 6.4.8.1+ * | 6.5.5.0+ * | En continu | 8, 11 | 20 juillet 2020 |
| [2.10.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.10.0) | Cette version a introduit le [composant Visionneuse PDF.](/help/components/pdf-viewer.md) | 6.4.8.1+ | 6.5.5.0+ | En continu | 8, 11 | 17 juin 2020 |
| [2.9.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.9.0) | Cette version a permis l’intégration à la [couche de données client Adobe](/help/developing/data-layer/overview.md) et introduit le [composant Barre de progression](/help/components/progress-bar.md). | 6.4.8.0+ | 6.5.4.0+ | En continu | 8, 11 | 29 mai 2020 |
| [2.8.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0) | Cette version comprend principalement des correctifs ainsi que de petites améliorations. | 6.4.4.0+ | 6.5.0.0+ | En continu | 8, 11 | 5 décembre 2019 |
| [2.7.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0) | Cette version a introduit le nouveau [composant Incorporer](/help/components/embed.md). | 6.4.4.0+ | 6.5.0.0+ | En continu | 8, 11 | 25 septembre 2019 |
| [2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | Cette version a introduit le nouveau [composant Fragment d’expérience](/help/components/experience-fragment.md). | 6.4.4.0+ | 6.5.0.0+ | En continu | 8, 11 | 6 septembre 2019 |
| [2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | Les nouveaux composants [Accordéon,](/help/components/accordion.md) [Bouton,](/help/components/button.md) [Conteneur](/help/components/container.md) et [Téléchargement](/help/components/download.md) ont été introduits dans cette version. | 6.4.2.0+ | 6.5.0.0+ | En continu | 8, 11 | 25 juin 2019 |
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | Cette version a introduit le [composant Liste de fragments de contenu](/help/components/content-fragment-list.md). | 6.4.2.0+ | 6.5.0.0+ | En continu | 8, 11 | 7 mai 2019 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | Cette version était axée sur l’amélioration de la [bibliothèque de composants](https://aemcomponents.dev), mais contenait également quelques améliorations des fonctionnalités du [composant Séparateur](/help/components/separator.md). | 6.4.2.0+ | 6.5.0.0+ | En continu | 8 | 14 mars 2019 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | Cette version était axée sur la [bibliothèque de composants](https://aemcomponents.dev) et introduisait le nouveau [composant Séparateur](/help/components/separator.md), mais elle contenait également quelques améliorations des fonctionnalités du [composant Image.](/help/components/image.md) | 6.4.2.0+ | - | - | 8 | 11 février 2019 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | Cette version concernait principalement les correctifs, mais contenait également quelques améliorations des fonctionnalités du [composant Carrousel.](/help/components/carousel.md) | 6.4.2.0+ | - | - | 8 | 27 novembre 2018 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | Cette version a introduit le [composant Onglets](/help/components/tabs.md) et le [composant Carrousel](/help/components/carousel.md), ainsi que des améliorations du [composant Image,](/help/components/image.md) du [composant Page](/help/components/page.md) et du [Composant Titre](/help/components/title.md). Elle a également amélioré le suivi. | 6.4.2.0+ | - | - | 8 | 16 octobre 2018 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | Cette version a introduit le [composant Teaser](/help/components/teaser.md), ainsi que des améliorations du [composant Image](/help/components/image.md) et de nombreux correctifs. | 6.4.2.0+ | - | - | 8 | 13 juillet 2018 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | Il s’agissait d’une version de correctif. | 6.4.0.0+ | - | - | 8 | 12 juin 2018 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | Cette version a apporté des améliorations au niveau du code, des correctifs de bogues et de petites améliorations, notamment la possibilité de retourner les images dans le [composant Image.](/help/components/image.md) | 6.4.0.0+ | - | - | 8 | 11 avril 2018 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | Cette version était principalement axée sur les améliorations au niveau du code, les correctifs de bogues, ainsi que quelques améliorations mineures apportées au [composant Image,](/help/components/image.md) au [composant Page](/help/components/page.md) et au [composant Fragment de contenu.](/help/components/content-fragment-component.md) | 6.4.0.0+ | - | - | 8 | 7 mars 2018 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | Cette version a introduit le [composant Navigation,](/help/components/navigation.md) le [composant Navigation linguistique,](/help/components/language-navigation.md) ainsi que le [composant Recherche rapide](/help/components/quick-search.md), et a mis en œuvre le [Système de style](/help/get-started/authoring.md#component-styling) pour tous les composants. | 6.4.0.0+ | - | - | 8 | 16 janvier 2018 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Cette version a mis en œuvre l’exportation JSON sur tous les composants et introduit le [composant Fragment de contenu.](/help/components/content-fragment-component.md) | 6.4.0.0+ | - | - | 8 | 10 octobre 2017 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | Cette version a ajouté plusieurs correctifs pour le [composant Image.](/help/components/image.md) | 6.4.0.0+ | - | - | 8 | 4 août 2017 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | Cette version a ajouté des correctifs pour le [composant de page,](/help/components/page.md) le [composant Image,](/help/components/image.md) ainsi que divers correctifs et améliorations globaux. | 6.4.0.0+ | - | - | 8 | 26 avril 2017 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | Cette version a ajouté des correctifs pour les images GIF animées dans le [composant Image.](/help/components/image.md) | 6.4.0.0+ | - | - | 7 | 22 mars 2017 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Version initiale des composants principaux. | 6.4.0.0+ | - | - | 7 | 20 mars 2017 |

>[!NOTE]
>
>(*) Depuis la version 2.11.0, `org.apache.sling.models.impl` version 1.4.12 ou ultérieure est nécessaire (en raison de [SLING-8781](https://issues.apache.org/jira/browse/SLING-8781)). Elle sera fournie pour AEM 6.4 et 6.5 dans un futur Service Pack. Dans l’intervalle, le lot Sling Models est inclus dans le package `core.wcm.components.all`.

>[!TIP]
>
>Comme avec AEM, Adobe conseille aux développeurs d’utiliser la [mise à jour et les versions les plus récentes disponibles des composants principaux](https://github.com/adobe/aem-core-wcm-components/releases/latest), compatibles avec la version d’AEM qu’ils exécutent pour bénéficier des correctifs et fonctionnalités les plus récents.

### Versions et versions des composants {#component-versions-and-releases}

Le tableau suivant répertorie les versions des composants contenus dans les versions des composants principaux.

|  | Version 1.0.0 - 1.0.6 | Version 1.1.0 | Version 2.0.0 - 2.0.8 | Version 2.1.0 | Version 2.2.0 - 2.2.0 | Version 2.3.0 - 2.3.2 | Version 2.4.0 | Version 2.5.0 | Version 2.6.0 | Version 2.7.0 - 2.8.0 | Version 2.9.0-2.17.14 | Version 2.18.0 | Version 2.19.0 | Version 2.20.0-2.21.2 | Version 2.22.0+ |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| **[Page](components/page.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 |
| **[Titre](components/title.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 |
| **[Image](components/image.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 |
| **[Liste](components/list.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3, v4 |
| **[Chemin de navigation](components/breadcrumb.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 |
| **[Partage sur les médias sociaux](components/sharing.md)** | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, obsolète | v1, obsolète | v1, obsolète | v1, obsolète |
| **[Conteneur de formulaires](components/forms/form-container.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Texte du formulaire](components/forms/form-text.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Options du formulaire](components/forms/form-options.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formulaire masqué](components/forms/form-hidden.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Bouton de formulaire](components/forms/form-button.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Fragment de contenu](components/content-fragment-component.md)** |  | Sandbox | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Navigation](components/navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Navigation par langue](components/language-navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Recherche rapide](components/quick-search.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 |
| **[Teaser](components/teaser.md)** |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Onglets](components/tabs.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Carrousel](components/carousel.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Séparateur](components/separator.md)** |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Liste de fragments de contenu](components/content-fragment-list.md)** |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Accordéon](components/accordion.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Bouton](components/button.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Conteneur](components/container.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Téléchargement](components/download.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Fragment d’expérience](components/experience-fragment.md)** |  |  |  |  |  |  |  |  | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Incorporer](components/embed.md)** |  |  |  |  |  |  |  |  |  | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Barre de progression](components/progress-bar.md)** |  |  |  |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 |
| **[Visionneuse PDF](components/pdf-viewer.md)** |  |  |  |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 |
| **[Table des matières](components/tableofcontents.md)** |  |  |  |  |  |  |  |  |  |  |  |  |  | v1 | v1 |

## Versions et mises à jour {#versions-and-releases}

Les composants principaux sont distribués via GitHub. Cela permet à Adobe d’ajouter plus rapidement des fonctionnalités aux composants et d’autoriser la saisie de la communauté en dehors du cycle de publication AEM.

Les composants principaux sont disponibles avec les versions AEM définies avec lesquelles ils sont compatibles. Cela signifie qu’une version AEM peut prendre en charge plusieurs versions ou mises à jour des composants principaux.

### Versions {#versions}

Les **versions** principales constituent l’itération majeure des composants principaux. Chaque composant possède une version. Les versions sont signalées avec la valeur **v** inscrite avec un entier positif non nul, comme v1 et v2. Les versions ne sont incrémentées que pour les modifications qui ne sont pas rétrocompatibles, ce qui est normalement le cas pour l’introduction de nouvelles fonctionnalités et fonctions.

Les développeurs et les administrateurs peuvent reconnaître les versions des composants principaux par un numéro figurant dans leurs chemins d’accès aux types de ressources et dans les noms de classe Java pleinement qualifiés de leurs implémentations. Ce numéro de version représente une version majeure définie par [les directives de contrôle de version sémantique](https://semver.org/).

Pour plus d’informations sur les versions des composants principaux, voir la [documentation destinée aux développeurs des composants principaux](developing/guidelines.md).

### Mises à jour {#releases}

Les composants principaux sont disponibles par l’intermédiaire des **mises à jour** et [représentent les artefacts publiés réels disponibles sur GitHub.](https://github.com/adobe/aem-core-wcm-components/releases) Les versions sont signalées par un nombre décimal au format `X.Y.Z` et rassemblent tous les composants principaux en tant que package livrable.

* Les **versions majeures** contiennent les éléments suivants : introduction de composants entièrement nouveaux, améliorations apportées aux versions existantes des composants et correctifs standard. Elles sont représentées par un incrément dans le composant `X` du numéro de version.
* Les **versions mineures** contiennent les éléments suivants : introduction de nouveaux composants, ajout de nouvelles fonctionnalités aux versions existantes des composants et divers correctifs. Elles sont représentées par un incrément dans le composant `Y` du numéro de version.
* Les **versions de correctif** contiennent uniquement des correctifs. Elles sont représentées par un incrément dans le composant `Z` du numéro de version.

>[!NOTE]
>
>Les versions peuvent contenir plusieurs versions du même composant.
>
>La même version d’un composant peut apparaître dans plusieurs versions.

## Prise en charge des composants principaux {#core-components-support}

Les composants principaux font partie intégrante d’AEM et sont pris en charge selon les mêmes conditions que s’ils étaient fournis dans le cadre du Quickstart.

À l’instar des autres fonctionnalités du produit, la règle générale de fin de vie est la suivante :

* Les composants sont d’abord annoncés comme étant obsolètes avant d’être supprimés.
* Ils sont ensuite retirés au plus tôt de la version d’AEM après l’annonce.

Les clients disposent ainsi d’au moins un cycle de publication pour passer à la nouvelle version du composant avant la fin de la prise en charge.

La version de chaque composant indique clairement les versions d’AEM prises en charge. Lorsque la prise en charge d’une version d’AEM est interrompue, la prise en charge des composants principaux de cette version d’AEM est prise en charge.

Pour plus d’informations sur la prise en charge des personnalisations des composants, consultez la page [Personnalisation des composants principaux](developing/customizing.md) de la version des composants principaux appropriée.

## Prise en charge des composants de base {#foundation-component-support}

Concernant le développement, Adobe met l’accent sur les composants principaux et de nouvelles fonctionnalités continueront d’être ajoutées.

[Presque tous les composants de base ont été abandonnés avec AEM 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/siteandpage/default-components-foundation.html?lang=fr) et seuls les correctifs majeurs seront pris en compte à l’avenir pour ces composants.
