---
title: Prise en charge d’AMP par les composants principaux
description: Les composants principaux prennent en charge les pages mobiles accélérées (AMP).
translation-type: tm+mt
source-git-commit: 2926c51c2ab97b50b9ec4942cd5415c15a1411b6
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 93%

---


# Prise en charge d’AMP par les composants principaux {#amp-support}

Depuis la [version 2.11.0](/help/versions.md) des composants principaux, la fonctionnalité [AMP de pages mobiles accélérées](https://developers.google.com/amp) est entièrement pris en charge.

Ce document donne un aperçu de la prise en charge d’AMP et explique comment l’activer pour vos sites. Pour obtenir des détails techniques complets, consultez la [documentation destinée aux développeurs sur GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp).

## Qu’est-ce qu’AMP ? {#what-is-amp}

AMP (Accelerated Mobile Pages) est un framework open source conçu à l’origine par Google en vue d’optimiser les pages pour la navigation mobile. En règle générale, les pages AMP se chargent beaucoup plus rapidement que les pages web standard, offrant ainsi de meilleures expériences mobiles.

## AMP dans les composants principaux {#amp-in-core-components}

La prise en charge d’AMP dans les composants principaux est [entièrement configurable.](#enabling-amp) Les versions AMP des pages peuvent être diffusées seules, avec les versions HTML standard, ou ne pas être diffusées du tout.

Les composants principaux utilisent `amp` comme sélecteur Sling pour le rendu d’une page AMP. Par exemple, `example.html` affiche la page normale et `example.amp.html` la version AMP.

Les projets individuels peuvent décider de tirer ou non parti d’AMP. En fait, étant donné que les pages AMP et HTML standard peuvent être diffusées en parallèle, un projet peut choisir d’utiliser AMP uniquement sur certaines pages.

## Prise en main de la prise en charge AMP dans votre projet {#getting-started}

La prise en charge AMP offre avec une grande flexibilité et quelques étapes simples suffisent pour une prise en main rapide :

1. Installez l’extension de prise en charge AMP si nécessaire.
   * Pour les projets AEM as a Cloud Service, l’extension est disponible automatiquement avec les composants principaux et aucune installation n’est nécessaire.
   * Pour les projets On-Premise et AMS, l’extension doit être installée explicitement lors de l’installation des composants principaux.
1. Une fois l’extension AMP installée, l’auteur du composant doit simplement pointer les supertypes de composant vers ceux de l’extension.
1. [Activez la prise en charge AMP](#enabling-amp) au niveau du modèle ou sur vos pages individuelles.
1. [Déployez une page CSS intégrée](#css-requirements) selon les besoins.

### Activation d’AMP pour les pages {#enabling-amp}

Pour activer AMP pour une page, le **Mode AMP** doit être sélectionné dans la [Stratégie de page.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-page-policy-template-author-developer)

![Options de stratégie de page AMP](/help/assets/amp-policy.png)

* **Aucun AMP** : la page est diffusée en HTML standard uniquement.
* **AMP couplé** : la page est diffusée au format AMP ainsi qu’au format HTML.
* **AMP uniquement** : la page est diffusée uniquement au format AMP.

Les paramètres AMP d’une page peuvent également être remplacés dans les [Propriétés de page](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html) d’une page donnée.

![Propriétés de page AMP](/help/assets/amp-page-properties.png)

* **Hériter du modèle de page** : il s’agit de la valeur par défaut, qui permet d’utiliser le paramètre de la stratégie du modèle de page.
* **Aucun AMP** : la page est diffusée en HTML standard uniquement.
* **AMP couplé** : la page est diffusée au format AMP ainsi qu’au format HTML.
* **AMP uniquement** : la page est diffusée uniquement au format AMP.

### Exigences CSS {#css-requirements}

When using AMP with the Core Components, the main difference is that AMP requires all [CSS to be inlined](including-clientlibs.md#inlining) in the `<head>` element as well as optimized.

Pour ce faire, un composant de page personnalisé est utilisé. Celui-ci charge uniquement la page CSS spécifique à AMP pour les composants présents sur la page.

Pour plus d’informations sur les exigences et les détails techniques, consultez la [documentation destinée aux développeurs sur GitHub.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
