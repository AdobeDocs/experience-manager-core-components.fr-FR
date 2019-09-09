---
title: Fonctionnalités de localisation des composants principaux
seo-title: Fonctionnalités de localisation des composants principaux
description: Fonctionnalités de localisation des composants principaux
seo-description: Fonctionnalités de localisation des composants principaux
content-type: référence
topic-tags: core-components
index: y
internal: n
translation-type: tm+mt
source-git-commit: 4af4873edf290f93733b0997b0e7a19c6c9e26f2

---


# Fonctionnalités de localisation des composants principaux {#localization-features-of-the-core-components}

De nombreux sites Web exigent que le contenu soit livré dans un format localisé dans plusieurs langues et régions. Les composants principaux de la fonctionnalité de référence intelligente permettent de créer facilement un modèle unifié pour l'ensemble de votre contenu localisé qui s'adapte automatiquement à la structure localisée de votre site.

## Exemple - Page localisée avec navigation et pied de page {#example}

La plupart des sites nécessitent un pied de page pour être présents sur toutes les pages. Ces pieds de page sont généralement cohérents sur l'ensemble du contenu de la page. Toutefois, pour une page de contenu localisée, une version localisée de cet en-tête ou du pied de page doit être affichée.

De même, un composant de navigation doit généralement s'afficher sur toutes les pages. Toutefois, il doit également refléter le contenu des pages localisées.

Utilisation des fonctions de localisation du composant noyau [de navigation](navigation.md) et [du composant](experience-fragment.md) principal Fragment d'expérience avec les [modèles modifiables d'AEM](https://docs.adobe.com/content/help/en/experience-manager-64/authoring/siteandpage/templates.html).

## Structure de contenu {#content-structure}

Toutes les fonctionnalités de localisation d'AEM et de ses composants principaux reposent sur une structure de contenu claire et logique pour votre contenu localisé.

Supposons que votre site soit simplement appelé `my-site` et qu'il se trouve ici :

```
/content/my-site
```

Imaginons également que vous conceviez votre site en anglais et l'offre également en français. Ainsi, si une page simple est appelée `my-page` , elle serait trouvée dans deux branches de localisation dans l'arborescence de contenu de votre site :

```
/content
\-- my-site
   +-- en
       \-- my-page
   \-- fr
       \-- my-page
```

Il se trouve sous ces branches de localisation dans lesquelles vous allez créer d'autres pages de sites.

En règle générale, les pieds de page sont créés à l'aide de Fragments d'expérience afin que vous ayez besoin d'une version anglaise et française comme vos pages. Toutefois, les fragments d'expérience ne sont pas des pages, mais sont des parties de pages qui peuvent être réutilisées. Elles ne sont donc pas directement sous `/content` comme reste de vos pages. Elles vivent dans leur propre dossier mais, comme elles doivent également être localisées, leur structure doit refléter la structure de localisation de votre site.

```
/content
+-- experience-fragments
   +-- en
      +-- footer
   \-- fr
      +-- footer
\-- my-site
   +-- en
      \-- my-page
   \-- fr
      \-- my-page
```

C'est grâce à la structure de localisation miroir que les composants principaux peuvent trouver le contenu localisé nécessaire pour une page correspondante.

## Pied de page - Fragment d'expérience {#footer}

Le composant Fragment d'expérience est très souple et est adapté à l'en-tête ou au pied de page d'une page.

Notre site Web hypothétique étant proposé en anglais et en français, nous devons créer deux fragments d'expérience, appelés tous deux `footer`[à l'emplacement décrit précédemment.](#content-structure)

![](assets/screen-shot-2019-09-09-11.08.28.png)

## Modèle de page {#template}

Comme le pied de page apparaîtra sur chaque page, nous devons ajouter le fragment d'expérience à notre modèle de page standard.

Notre modèle est simplement appelé `my-template` et se trouve avec nos autres modèles :

```
/conf/my-site/settings/wcm/templates/my-template
```

À ce modèle, nous ajouterons les composants de base que nous voulons utiliser pour les pages.

* [Composant Navigation](navigation.md)
   * Le composant de navigation s'affiche en haut de chaque page.
   * Dans le composant de navigation, nous définissons la racine de navigation, indiquant au composant où commence la structure de navigation du site.
   * Selon la racine de navigation, le composant trouve automatiquement le contenu localisé correspondant.
* Conteneur de mises en page
   * Chaque page contient un composant Conteneur de dispositions modifiable afin que les auteurs puissent placer du contenu supplémentaire sur la page.
* [Fragment d’expérience](experience-fragment.md)
   * Nous pointons le composant Expert Inece sur le chemin du fragment dans la langue de création du fragment qui représente le pied de page.
   * Selon le chemin d'accès de ce fragment et la structure des fragments d'expérience reflétant la structure localisée de la page, le composant trouve automatiquement le contenu localisé correspondant.
   ![](assets/screen-shot-2019-09-09-11.20.10.png)

## Pages {#pages}

En travaillant dur dans la définition de la structure et du modèle du site, l'auteur doit simplement ajouter le contenu nécessaire aux pages. En raison de la logique de localisation des composants, la navigation et les pieds de page sont automatiquement localisés.

Par exemple, l'auteur doit uniquement ajouter un composant de texte aux pages anglaise et française (représenté en bleu ci-dessous).

Le composant de navigation et le composant Fragment d'expérience savent afficher automatiquement le contenu correct en fonction de la structure de localisation et de l'emplacement de la page elle-même (représentée en blanc ci-dessous).

![](assets/screen-shot-2019-09-09-11.22.14.png)

## Ajustement complet {#fitting-it-all-together}

Vous trouverez ci-dessous une illustration complète de la manière dont ces éléments simples mais performants collaborent pour diffuser des pages localisées pour les auteurs de contenu.

![](assets/screen-shot-2019-09-09-11.27.58.png)
