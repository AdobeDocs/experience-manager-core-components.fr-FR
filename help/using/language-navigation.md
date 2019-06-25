---
title: Composant Navigation par langue
seo-title: Composant Navigation par langue
description: 'null'
seo-description: Le composant Navigation par langue fournit une navigation par langue/pays pour un site, de sorte que les visiteurs puissent accéder à la même page dans un autre paramètre régional.
uuid: ce736458-9cdf-4bc2-b90f-9c5a62fe1ca0
content-type: référence
topic-tags: création
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 8f232eb0-65d5-4075-8668-75f1366882c8
disttype: dist5
gnavtheme: light
groupsectionnavitems: non
hidemerchandisingbar: inherit
hidepromocomponent: inherit
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c58826c133eb112b305fa4facbe2a81e577eb896

---


# Composant Navigation par langue {#language-navigation-component}

Le composant Navigation par langue fournit une navigation par langue/pays pour un site, de sorte que les visiteurs puissent accéder à la même page dans un autre paramètre régional.

## Utilisation {#usage}

Souvent, les sites Web sont diffusés en plusieurs langues pour différentes régions. Le composant Navigation par langue permet à un visiteur d’afficher la même page dans différents langues/dialectes.

La [boîte de dialogue Modifier](#edit-dialog) permet la définition de la racine de navigation globale ainsi que la profondeur de la structure de navigation. A l’aide de [la boîte de dialogue Conception](#design-dialog), l’auteur du modèle peut définir les valeurs par défaut des mêmes options.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Navigation par langue est v1, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018 et est décrite dans ce document.

Le tableau suivant détaille toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Composant Version | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Compatible | Compatible | Compatible |


Pour plus d’informations sur les versions et les mises à jour des composants principaux, consultez le document sur les [versions des composants principaux](versions.md).

## Exemple de sortie de composant {#sample-component-output}

To experience the Language Navigation Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/languagenavigation.html).

## Détails techniques {#technical-details}

The latest technical documentation about the Language Navigation Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/languagenavigation/v1/languagenavigation).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](developing.md).

## Boîte de dialogue Modifier {#edit-dialog}

La boîte de dialogue Modifier permet la définition de la racine de navigation globale ainsi que la profondeur de la structure de navigation.

![](assets/screen_shot_2018-01-12at133353.png)

* **Racine de navigation**
Définit la page racine de la structure de navigation.
   * Utilisez le bouton **Ouvrir la boîte de dialogue Sélection** pour parcourir facilement la structure de contenu et sélectionner la racine.
* **Profondeur de la structure de langue**
Profondeur de la structure de langue globale par rapport à la racine de navigation.

## Boîte de dialogue Conception {#design-dialog}

A l’aide de la boîte de dialogue Conception, l’auteur du modèle peut définir les valeurs par défaut des mêmes options disponibles dans la boîte de dialogue Modifier.

### Onglet Propriétés {#properties-tab}

![](assets/screen_shot_2018-01-12at133642.png)

* **Racine de navigation**
Valeur par défaut de la racine de navigation lorsqu’un auteur de contenu place le composant Sélecteur de langue sur une page de contenu.
* **Profondeur de la structure de langue**
Valeur par défaut de la profondeur de la structure de langue lorsqu’un auteur de contenu place le composant Sélecteur de langue sur une page de contenu.

### Onglet Styles {#styles-tab}

Le composant Navigation par langue prend en charge le [système de style](authoring.md#component-styling) AEM.