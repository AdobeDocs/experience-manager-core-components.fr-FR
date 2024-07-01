---
title: Configurations basées sur le contexte Sling et composants principaux
description: Les composants principaux tirent parti des configurations basées sur le contexte Sling pour certaines fonctionnalités
role: Architect, Developer, Admin
exl-id: d35210f7-a65d-4768-ab9e-f12ec406da2d
source-git-commit: b72defe1bbe6cb286730ac3f508f7d6c14b3fc33
workflow-type: ht
source-wordcount: '174'
ht-degree: 100%

---

# Configurations basées sur le contexte Sling et composants principaux {#sling-context-aware-configurations}

Les configurations tenant compte du contexte sont une [fonctionnalité de Sling](https://sling.apache.org/documentation/bundles/context-aware-configuration/context-aware-configuration.html). Il s’agit de configurations liées à une ressource de contenu, ou à une arborescence de ressources, qui sont exploitées par les composants principaux pour permettre les configurations à l’échelle du site.

## Configurations basées sur le contexte Sling {#context-aware-configurations}

Votre site peut nécessiter différentes configurations pour différentes régions de sites, par exemple lorsque certains paramètres peuvent être partagés et nécessitent l’héritage pour les contextes imbriqués et les valeurs de secours globales. AEM exploite les configurations compatibles avec le contexte Sling, ce qui permet cette possibilité.

Pour plus d’informations sur les configurations dans AEM, [consultez la documentation sur les configurations et le navigateur de configuration.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/configurations.html?lang=fr)

## Utilisation dans les composants principaux {#core-components}

Un certain nombre de composants principaux exploitent les configurations basées sur le contexte. Toutes ces configurations se trouvent sous le nœud suivant :

* `/conf/<my-site>/sling:configs/<my-configuration>`

Les configurations individuelles dépendent du composant ou de la fonctionnalité spécifique. Les fonctionnalités des composants principaux qui utilisent les configurations basées sur le contexte incluent ce qui suit :

* Le [composant de page](https://github.com/adobe/aem-core-wcm-components/tree/main/content/src/content/jcr_root/apps/core/wcm/components/page/v3/page#loading-of-context-aware-cssjs) repose sur une configuration basée sur le contexte lors du rendu des balises `link`, `script` et `meta`.
* [Composant Visionneuse PDF](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)
* [Couche de données client Adobe](/help/developing/data-layer/overview.md#installation-activation)
* [Prise en charge d’AMP](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
