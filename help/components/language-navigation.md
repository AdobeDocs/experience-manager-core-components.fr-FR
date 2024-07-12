---
title: Composant de navigation par langue
description: Le composant Navigation par langue fournit une navigation par langue/pays pour un site, de sorte que les visiteurs puissent accéder à la même page dans un autre paramètre régional.
role: Architect, Developer, Admin, User
exl-id: 10b218b4-c439-4a0f-a46f-0b15d78b0360
source-git-commit: 327c239b02e0aecee878784c918bfa98d960530e
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 100%

---

# Composant de navigation par langue {#language-navigation-component}

Le composant Navigation par langue fournit une navigation par langue/pays pour un site, de sorte que les visiteurs puissent accéder à la même page dans un autre paramètre régional.

## Utilisation {#usage}

Souvent, les sites web sont proposés en plusieurs langues pour différentes zones géographiques. Le composant de navigation par langue permet à un visiteur d’afficher la même page dans différentes langues/différents paramètres régionaux. Ainsi, si vous consultez la version suisse allemande du site web, vous pouvez facilement passer à la version en anglais (États-Unis) de la même page. Le composant Navigation par langue gère la compréhension de la structure linguistique du site et recherche automatiquement la page correspondante.

* Pour un exemple du fonctionnement de la fonction de localisation du composant de navigation linguistique, reportez-vous à [la section ci-dessous](#example).
* Pour un exemple de la façon dont les fonctions de localisation des autres composants principaux fonctionnent ensemble, reportez-vous à la page [Fonctions de localisation de la page Composants principaux](/help/get-started/localization.md).

La [boîte de dialogue de modification](#edit-dialog) permet de définir la racine de navigation globale d’un site ainsi que la profondeur de la structure de navigation. À l’aide de [la boîte de dialogue de conception](#design-dialog), l’auteur du modèle peut définir les valeurs par défaut des mêmes options.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Navigation par langue est v2, qui a été introduite avec la version 2.18.0 des composants principaux en février 2022. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | - | Compatible | Compatible |
| [v1](v1/language-navigation.md) | Compatible | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant Navigation par langue et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_langnav_fr).

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Navigation par langue [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_langnav_v2_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir la racine de navigation globale d’un site ainsi que la profondeur de la structure de navigation.

En règle générale, ces configurations doivent être effectuées uniquement au niveau du modèle de page. Toutefois, elles peuvent être modifiées au niveau de la page dans la [boîte de dialogue de modification](#edit-dialog).

### Onglet Propriétés {#properties-tab}

![Boîte de dialogue de conception du composant Navigation par langue](/help/assets/language-navigation-design.png)

* **Racine de navigation**
   * C’est là que doit commencer la navigation par langue du site.
   * La structure linguistique du site commence au niveau suivant sous cette racine.
* **Profondeur de la structure de langue**
   * Il s’agit du nombre de niveaux de l’arborescence de contenu sous la **racine de navigation** qui représentent la structure linguistique du site. Exemples :
      * `1` signifie généralement que vous avez le choix de la langue.
      * `2` signifie généralement que vous avez le choix de la langue et du pays.
      * `3` signifie généralement que vous avez le choix de la langue, du pays et de la région.

#### Exemple {#example}

Imaginons que votre contenu ressemble à ceci :

```
/content
+-- wknd
   +-- language-masters
   +-- us
      +-- en
      \-- es
   \-- ch
      +-- de
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

Pour le site WKND, il est probable que vous souhaitiez placer le composant Navigation par langue sur un modèle de page dans le cadre de l’en-tête. Une fois qu’il fait partie du modèle, vous pouvez définir la **racine de navigation** du composant sur `/content/wknd` puisque c’est là où commence le contenu localisé de ce site. Vous souhaiteriez également définir la **Profondeur de la structure de langue** sur `2` puisqu’il s’agit d’une structure à deux niveaux (pays puis langue).

Avec la valeur **Racine de navigation**, le composant Langue sait que la navigation commence après `/content/wknd` et il peut générer des options de navigation par langue en reconnaissant les deux niveaux suivants dans l’arborescence de contenu en tant que structure de navigation de langue du site (comme défini par la valeur **Profondeur de la structure de langue**).

Quelle que soit la page consultée par un utilisateur, le composant Navigation par langue trouve la page correspondante dans une autre langue, en connaissant l’emplacement de la page actuelle et en remontant à la racine, puis en transmettant la page correspondante.

### Onglet Styles {#styles-tab}

Le composant Navigation par langue prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

## Boîte de dialogue de modification {#edit-dialog}

### Onglet Propriétés {#properties-tab-edit}

En règle générale, le composant Navigation par langue doit uniquement être ajouté et configuré sur les modèles de page d’un site. Cependant, si le composant Navigation par langue doit être ajouté à une page de contenu, la boîte de dialogue de modification permet à un auteur de contenu de configurer les mêmes valeurs, comme décrit dans la [boîte de dialogue de conception](#design-dialog)

De plus, vous pouvez définir un **ID**. Cette option permet de contrôler l’identifiant unique du composant dans le code HTML et dans la [couche de données](/help/developing/data-layer/overview.md).

* Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
* Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
* La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

![Boîte de dialogue de modification du composant Navigation par langue](/help/assets/language-navigation-edit.png)

### Onglet Accessibilité {#accessibility-tab}

* **Libeller** : cette option doit être définie si la page contient plusieurs langues de navigation afin de définir l’attribut Libellé ARIA du composant.

![Onglet Accessibilité du composant Navigation par langue](/help/assets/language-navigation-edit-accessibility.png)

### Onglet Styles {#styles-tab-edit}

Le composant Navigation par langue prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

Utilisez la liste déroulante pour sélectionner les styles à appliquer au composant. Les sélections effectuées dans la boîte de dialogue de modification ou dans la barre d’outils du composant ont le même effet.

Pour que le menu déroulant soit disponible, les styles doivent être configurés pour ce composant dans la [boîte de dialogue de conception](#design-dialog).

![Onglet Styles de la boîte de dialogue de modification du composant Navigation par langue](/help/assets/language-navigation-edit-styles.png)

## Couche de données client Adobe {#data-layer}

Le composant Navigation linguistique prend en charge la [couche de données client Adobe](/help/developing/data-layer/overview.md).
