---
title: Fonctions de localisation des composants principaux
description: Fonctions de localisation des composants principaux
role: Architect, Developer, Admin, User
exl-id: 9140b65a-6dd7-4ec9-9095-6e8243ec8424
source-git-commit: 888719359f9a1d1c9dccff97fb639b332f2be54c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Fonctions de localisation des composants principaux {#localization-features-of-the-core-components}

De nombreux sites web exigent que le contenu soit diffusé dans un format localisé dans plusieurs langues et géographies. Les composants principaux sélectionnés disposent d’une résolution intelligente des références afin de faciliter la création d’un modèle unifié pour l’ensemble du contenu localisé qui s’adapte automatiquement en fonction de la structure de votre site localisé.

## Exemple - Page localisée avec navigation et pieds de page {#example}

La plupart des sites nécessitent qu’un pied de page soit présent sur toutes les pages. Ces pieds de page sont généralement cohérents dans tout le contenu de la page. Toutefois, pour une page de contenu localisée, une version localisée de cet en-tête ou pied de page doit être affichée.

De même, un composant de navigation doit généralement être affiché sur toutes les pages. Toutefois, il devra également refléter le contenu des pages localisées.

En utilisant les fonctionnalités de localisation du [composant principal de navigation](/help/components/navigation.md) et du [composant principal de fragment d’expérience](/help/components/experience-fragment.md), ainsi que les [modèles modifiables d’AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=fr), cela devient facile à réaliser. L’exemple pourrait être étendu à l’utilisation du [composant Navigation linguistique](/help/components/language-navigation.md).

## La structure du contenu {#content-structure}

Toutes les fonctionnalités de localisation d’AEM et de ses composants principaux reposent sur une structure de contenu claire et logique pour votre contenu localisé.

Supposons que votre site soit simplement appelé `my-site` et se trouve ici :

```
/content/my-site
```

Disons aussi que vous créez votre site en anglais et que vous le proposez aussi en français. Ainsi, si vous avez une page simple appelée `my-page`, elle se trouve dans deux branches de localisation dans l’arborescence de contenu de votre site :

```
/content
\-- my-site
   +-- en
       \-- my-page
   \-- fr
       \-- my-page
```

C’est sous ces branches de localisation que vous allez créer des pages de sites supplémentaires.

Les pieds de page sont généralement créés à l’aide de fragments d’expérience. Vous aurez donc besoin d’une version en anglais et en français, tout comme vos pages. Toutefois, les fragments d’expérience ne sont pas des pages, mais des parties de pages qui peuvent être réutilisées sur plusieurs pages. Ils ne résident donc pas directement sous `/content` le reste de vos pages. Au lieu de cela, ils résident sous leur propre dossier, mais comme ils doivent également être localisés, leur structure doit refléter la structure de localisation de votre site.

```
/content
+-- experience-fragments
   +-- en
      \-- footer
   \-- fr
      \-- footer
\-- my-site
   +-- en
      \-- my-page
   \-- fr
      \-- my-page
```

C’est grâce à la structure de localisation en miroir que les composants principaux peuvent trouver le contenu localisé nécessaire pour une page correspondante.

## Pied de page - Fragment d’expérience {#xf-footer}

Le composant Fragment d’expérience est très flexible et convient parfaitement à un en-tête ou un pied de page.

Comme notre site Web hypothétique est offert en anglais et en français, nous devrons créer deux fragments d’expérience, tous deux appelés `footer` [dans les emplacements que nous avons décrits précédemment.](#content-structure)

![](/help/assets/screen-shot-2019-09-09-11.08.28.png)

## Modèle de page {#template}

Comme le pied de page s’affiche sur chaque page, nous devrons ajouter le fragment d’expérience à notre modèle de page standard.

Notre modèle est simplement appelé `my-template` et se trouve avec nos autres modèles :

```
/conf/my-site/settings/wcm/templates/my-template
```

Nous ajouterons à ce modèle les composants de base sur lesquels nous voulons que nos pages soient basées.

* [Composant Navigation](/help/components/navigation.md)
   * Le composant de navigation apparaît en haut de chaque page.
   * Dans le composant de navigation, nous définissons la racine de navigation, indiquant au composant où commence la structure de navigation du site.
   * En fonction de la racine de navigation, le composant peut rechercher automatiquement le contenu localisé correspondant.
* [Composant de conteneur](/help/components/container.md)
   * Chaque page contient un composant de conteneur modifiable afin que les auteurs puissent placer du contenu supplémentaire sur la page.
* [Fragment d’expérience](/help/components/experience-fragment.md)
   * Nous pointons le composant de fragment d’expérience vers le chemin du fragment dans notre langage de création du fragment qui représente le pied de page.
   * En fonction du chemin d’accès de ce fragment et de la structure des fragments d’expérience qui reflètent la structure de page localisée, le composant peut rechercher automatiquement le contenu localisé correspondant.

   ![](/help/assets/screen-shot-2019-09-09-11.20.10.png)

## Pages {#pages}

En effectuant le travail acharné de configuration de la structure et du modèle du site, l’auteur du contenu doit simplement ajouter le contenu nécessaire aux pages. Grâce aux modèles et à la logique de localisation des composants, la navigation et les pieds de page seront automatiquement ajoutés à la page et localisés.

Par exemple, l’auteur n’aurait besoin que d’ajouter du contenu tel qu’un composant de texte aux pages en anglais et en français (représenté en bleu ci-dessous).

Le composant de navigation et le composant de fragment d’expérience proviennent du modèle de page et savent afficher automatiquement le contenu correct en fonction de la structure de localisation et de l’emplacement de la page elle-même (représenté en blanc ci-dessous).

![](/help/assets/screen-shot-2019-09-09-11.22.14.png)

## Ajuster tout ensemble {#fitting-it-all-together}

Voici une image complète de la manière dont ces éléments simples, mais puissants, opèrent ensemble pour fournir des pages localisées aux auteurs de contenu.

![](/help/assets/screen-shot-2019-09-09-11.27.58.png)
