---
title: Prise en charge d’AMP par les composants principaux
description: Les composants principaux prennent en charge les pages mobiles accélérées (AMP).
role: Architect, Developer, Admin
exl-id: 1fd9b6b5-0e4d-48c7-8faa-42e0d4a6bbd0
source-git-commit: 2ac16b15718128feefbe903e92f276b16fe96f69
workflow-type: ht
source-wordcount: '554'
ht-degree: 100%

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

Pour activer AMP pour une page, le **Mode AMP** doit être sélectionné dans la [Stratégie de page.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=fr#editing-a-template-page-policy-template-author-developer)

![Options de stratégie de page AMP](/help/assets/amp-policy.png)

* **Aucun AMP** : la page est diffusée en HTML standard uniquement.
* **AMP couplé** : la page est diffusée au format AMP ainsi qu’au format HTML.
* **AMP uniquement** : la page est diffusée uniquement au format AMP.

Les paramètres AMP d’une page peuvent également être remplacés dans les [Propriétés de page](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=fr) d’une page donnée.

![Propriétés de page AMP](/help/assets/amp-page-properties.png)

* **Hériter du modèle de page** : il s’agit de la valeur par défaut, qui permet d’utiliser le paramètre de la stratégie du modèle de page.
* **Aucun AMP** : la page est diffusée en HTML standard uniquement.
* **AMP couplé** : la page est diffusée au format AMP ainsi qu’au format HTML.
* **AMP uniquement** : la page est diffusée uniquement au format AMP.

### Exigences CSS {#css-requirements}

Lors de l’utilisation d’AMP avec les composants principaux, la principale différence réside dans le fait qu’AMP exige que tous les [éléments CSS soient insérés](including-clientlibs.md#inlining) dans l’élément `<head>` et optimisés.

Pour ce faire, un composant de page personnalisé est utilisé. Celui-ci charge uniquement la page CSS spécifique à AMP pour les composants présents sur la page.

>[!NOTE]
>
>En raison des limitations de conception d’AMP, Adobe ne prend pas en charge l’utilisation de la grille réactive avec la version AMP de votre page.

Pour plus d’informations sur les exigences et les détails techniques, consultez la [documentation destinée aux développeurs sur GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp).
