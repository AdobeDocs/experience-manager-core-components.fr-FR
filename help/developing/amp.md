---
title: Prise en charge AMP des composants principaux
description: Les composants principaux prennent en charge AMP - Pages mobiles accélérées
translation-type: tm+mt
source-git-commit: 905096d909d4fbf624152ba3b5cbc1d80637245f
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---


# Prise en charge AMP des composants principaux {#amp-support}

Depuis la [version 2.11.0](/help/versions.md) des composants principaux, [AMP - Accelerated Mobile Pages](https://developers.google.com/amp) - est entièrement pris en charge.

Ce document donne un aperçu de la prise en charge d’AMP et explique comment l’activer pour vos sites. Toutefois, pour obtenir des détails techniques complets, consultez la documentation du développeur [GitHub.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

## Qu’est-ce que l’AMP ? {#what-is-amp}

Accelerated Mobile Pages ou AMP est une structure open-source conçue à l&#39;origine par Google pour optimiser les pages pour la navigation mobile. En règle générale, les pages AMP se chargent beaucoup plus rapidement que les pages Web standard, offrant ainsi de meilleures expériences mobiles.

## AMP dans les composants principaux {#amp-in-core-components}

La prise en charge d’AMP dans les composants principaux est [entièrement configurable.](#enabling-amp) Les versions AMP des pages peuvent être diffusées exclusivement, avec les versions HTML standard, ou pas du tout.

Les composants principaux sont utilisés `amp` comme sélecteur Sling pour générer une page AMP. Par exemple, `example.html` rendrait la page normale et `example.amp.html` serait la version AMP.

### Conditions requises {#requirements}

Lors de l’utilisation d’AMP avec les composants principaux, la principale différence réside dans le fait qu’AMP exige que toutes les feuilles de style CSS soient insérées dans l’ `<head>` élément et optimisées.

Pour ce faire, un composant de page personnalisé est utilisé, qui charge uniquement la page CSS spécifique à AMP pour les composants présents sur la page.

Pour plus d&#39;informations sur les exigences et les détails techniques, consultez la documentation destinée aux développeurs [GitHub.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

### Utilisation d’AMP dans les composants principaux {#using-amp}

Les projets individuels peuvent décider s&#39;ils doivent ou non tirer parti de l&#39;AMP. En fait, étant donné que les pages AMP et HTML standard peuvent être diffusées en parallèle, un projet peut choisir d’utiliser AMP sur certaines pages seulement du projet.

### Installation de la prise en charge AMP {#installing-amp}

Comme AMP est facultatif, il est fourni en tant qu’extension aux composants principaux.

* Pour AEM en tant que projets Cloud Service, l’extension est automatiquement disponible.
* Pour les projets sur site et AMS, l&#39;extension doit être explicitement installée lors de l&#39;installation des composants principaux.

Une fois l&#39;extension installée, l&#39;auteur du composant doit simplement pointer les supertypes de composant vers ceux de l&#39;extension.

### Activation d’AMP pour les pages {#enabling-amp}

Pour activer AMP pour une page, le mode **** AMP doit être sélectionné dans la stratégie de [page.](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/templates.html#editingatemplatepagepolicies)

![Options Stratégie de page AMP](/help/assets/amp-policy.png)

* **Pas de fichier AMP** : la page est diffusée en HTML standard uniquement.
* **AMP** appariée : la page est diffusée au format AMP ainsi qu’au format HTML.
* **AMP uniquement** : la page est diffusée en tant que AMP uniquement.

Les paramètres AMP d’une page peuvent également être remplacés dans les Propriétés [de](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/authoring/editing-page-properties.html) page d’une page donnée.

![Propriétés de page AMP](/help/assets/amp-page-properties.png)

* **Hériter du modèle** de page : il s&#39;agit de la valeur par défaut, qui permet de retirer le paramètre de la stratégie du modèle de page.
* **Pas de fichier AMP** : la page est diffusée en HTML standard uniquement.
* **AMP** appariée : la page est diffusée au format AMP ainsi qu’au format HTML.
* **AMP uniquement** : la page est diffusée en tant que AMP uniquement.
