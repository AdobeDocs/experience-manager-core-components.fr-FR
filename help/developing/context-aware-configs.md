---
title: Configurations basées sur le contexte Sling et composants principaux
description: Les composants principaux tirent parti des configurations basées sur le contexte Sling pour certaines fonctionnalités
translation-type: ht
source-git-commit: 24a810ff634f8846881dfa0095e879476d0f16f0
workflow-type: ht
source-wordcount: '185'
ht-degree: 100%

---


# Configurations basées sur le contexte Sling et composants principaux {#sling-context-aware-configurations}

Les configurations basées sur le contexte sont une fonctionnalité de Sling. Il s’agit de configurations liées à une ressource de contenu, ou à une arborescence de ressources, qui sont exploitées par les composants principaux pour permettre les configurations à l’échelle du site.

## Configurations basées sur le contexte Sling {#context-aware-configurations}

Votre site peut nécessiter différentes configurations pour différentes régions de sites, par exemple lorsque certains paramètres peuvent être partagés et nécessitent l’héritage pour les contextes imbriqués et les valeurs de secours globales. Les configurations basées sur le contexte Sling rendent cela possible.

Pour des détails complets sur les configurations basées sur le contexte Sling, [consultez la documentation Apache.](https://sling.apache.org/documentation/bundles/context-aware-configuration/context-aware-configuration.html)

## Utilisation dans les composants principaux {#core-components}

Un certain nombre de composants principaux exploitent les configurations basées sur le contexte. Toutes ces configurations se trouvent sous le nœud suivant :

* `/conf/<my-site>/sling:configs/<my-configuration>`

Les configurations individuelles dépendent du composant ou de la fonctionnalité spécifique. Les fonctionnalités des composants principaux qui utilisent les configurations basées sur le contexte sont les suivantes :

* [Composant Visionneuse PDF](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)
* [Couche de données client Adobe](/help/developing/data-layer/overview.md#installation-activation)
* [Prise en charge d’AMP](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
