---
title: Configurations adaptées au contexte Sling et composants principaux
description: Les composants principaux tirent parti des configurations Sling tenant compte du contexte pour certaines fonctionnalités
translation-type: tm+mt
source-git-commit: 24a810ff634f8846881dfa0095e879476d0f16f0
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 12%

---


# Configurations adaptées au contexte Sling et composants principaux {#sling-context-aware-configurations}

Les configurations contextuelles sont une fonctionnalité de Sling et sont des configurations liées à une ressource de contenu ou à une arborescence de ressources et exploitées par les composants principaux pour autoriser les configurations à l’échelle du site.

## Configurations adaptées au contexte Sling {#context-aware-configurations}

Votre site peut nécessiter différentes configurations pour différentes régions de sites, par exemple lorsque certains paramètres peuvent être partagés et nécessitent l&#39;héritage pour les contextes imbriqués et les valeurs de secours globales. Les configurations prenant en compte le contexte Sling activent cette fonction.

Pour obtenir des détails complets sur les configurations prenant en compte le contexte Sling, [consultez la documentation Apache.](https://sling.apache.org/documentation/bundles/context-aware-configuration/context-aware-configuration.html)

## Use in the Core Components {#core-components}

Un certain nombre de composants principaux exploitent des configurations contextuelles. Toutes ces configurations se trouvent sous le noeud suivant :

* `/conf/<my-site>/sling:configs/<my-configuration>`

Les configurations individuelles dépendent du composant ou de la fonctionnalité spécifique. Les fonctionnalités des composants principaux qui utilisent des configurations adaptées au contexte sont les suivantes :

* [Composant Visionneuse PDF](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)
* [Couche de données client Adobe](/help/developing/data-layer/overview.md#installation-activation)
* [Prise en charge d’AMP](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
