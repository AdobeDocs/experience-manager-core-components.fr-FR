---
title: Composant de navigation par langue
seo-title: Composant de navigation par langue
description: 'null'
seo-description: Le composant de navigation par langue fournit une navigation par langue/pays pour un site, de sorte que les visiteurs puissent accéder à la même page dans un autre paramètre régional.
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
source-git-commit: 8a34ecc432e489b8dc025aeda29d8eba9c788861

---


# Composant de navigation par langue {#language-navigation-component}

Le composant de navigation par langue fournit une navigation par langue/pays pour un site, de sorte que les visiteurs puissent accéder à la même page dans un autre paramètre régional.

## Utilisation {#usage}

Les sites Web sont souvent fournis en plusieurs langues pour différentes régions. Le composant de navigation par langue permet à un visiteur d’afficher la même page dans différentes langues/différents paramètres régionaux. Ainsi, si vous êtes un lecteur sur la version allemande du site web, vous pouvez facilement passer à la version anglais américaine de la même page. Le composant Navigation de langue gère la présentation de la structure de la langue du site et recherche la page correspondante automatiquement.

La [boîte de dialogue de modification](#edit-dialog) permet la définition de la racine de navigation globale d’un site ainsi que la profondeur de la structure de navigation. À l’aide de [la boîte de dialogue de conception](#design-dialog), l’auteur du modèle peut définir les valeurs par défaut des mêmes options.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de navigation par langue est v1, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Compatible | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](versions.md).

## Exemple de sortie de composant {#sample-component-output}

To experience the Language Navigation Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/language-navigation/language-structure/us/en/language-navigation.html).

## Détails techniques {#technical-details}

Vous trouverez la documentation technique la plus récente sur le composant [de navigation dans la langue sur github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/languagenavigation/v1/languagenavigation).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](developing.md).

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de modification permet la définition de la racine de navigation globale d’un site ainsi que la profondeur de la structure de navigation.

En règle générale, ces configurations ne doivent être effectuées qu'au niveau du modèle de page. Toutefois, ils peuvent être modifiés au niveau de la page via la boîte de dialogue [Modifier](#edit-dialog).

### Onglet Propriétés {#properties-tab}

![](assets/screen_shot_2018-01-12at133642.png)

* **Racine de navigation**
   * C'est là que la navigation du site doit commencer.
   * La structure linguistique du site commence au niveau suivant sous cette racine.
* **Profondeur de la structure de langue**
   * Il s'agit du nombre de niveaux de l'arborescence de contenu sous la racine **de navigation** qui représentent la structure linguistique du site. Exemples:
      * `1` signifie généralement que vous avez le choix de la langue.
      * `2` signifie que vous avez le choix entre la langue et le pays.
      * `3` signifie généralement que vous avez le choix entre le langage, le pays et la région.

#### Exemple {#example}

Imaginons que votre contenu ressemble à ceci :

```
/content
+-- we-retail
   +-- language-masters
   +-- us
      +-- en
      \-- es
   +-- ch
      +-- de
      +-- fr
      +-- it
+-- wknd-events
\-- wknd-shop
```

Pour le site We. Retail, il est probable que vous souhaitiez placer le composant Navigation de langue sur un modèle de page dans le cadre de l'en-tête. Une fois la partie du modèle définie, vous pouvez définir la racine **de navigation** du composant comme `/content/we-retail` étant à partir de là où le contenu localisé de ce site commence. Vous souhaitez également définir **la Profondeur** de la structure de langue `2` puisque la structure est de deux niveaux (pays puis langue).

Avec la valeur **Racine** de navigation, le composant Langue sait que la `/content/we-retail` navigation commence et qu'elle peut générer des options de navigation de langue en reconnaissant les deux niveaux suivants dans l'arborescence de contenu en tant que structure de navigation de langue du site (comme défini par la valeur **Profondeur** de la structure de langue).

Quelle que soit la page consultée par un utilisateur, le composant Navigation de langue trouve la page correspondante dans une autre langue en connaissant l'emplacement de la page actuelle et en travaillant en arrière à la racine, puis en transmettant la page correspondante.

### Onglet Styles {#styles-tab}

Le composant Navigation par langue prend en charge le [système de style](authoring.md#component-styling) AEM.

## Boîte de dialogue de modification {#edit-dialog}

En règle générale, le composant de navigation de Langauge doit uniquement être ajouté et configuré sur les modèles de page d'un site. Cependant, si le composant Navigation de langue doit être ajouté à une page de contenu individuelle, la boîte de dialogue Modifier permet à un auteur de contenu de configurer les mêmes valeurs comme décrit dans la boîte de dialogue [de conception](#design-dialog).

![](assets/screen_shot_2018-01-12at133353.png)
