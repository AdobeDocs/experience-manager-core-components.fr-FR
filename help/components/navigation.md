---
title: Composant Navigation
description: Le composant Navigation permet aux utilisateurs de parcourir facilement une structure de site globalisée.
translation-type: ht
source-git-commit: d3ebcea5fa1523c1a986841cd3d1a64e16e85f6d
workflow-type: ht
source-wordcount: '1382'
ht-degree: 100%

---


# Composant Navigation {#navigation-component}

Le composant Navigation permet aux utilisateurs de parcourir facilement une structure de site globalisée.

## Utilisation {#usage}

Les listes de composants de navigation répertorient une arborescence de pages afin que les utilisateurs d’un site puissent facilement naviguer dans la structure du site.

Le composant de navigation peut détecter automatiquement la structure de site globalisée de votre site et [s’adapter automatiquement à une page localisée.](#localized-site-structure) En outre, elle peut prendre en charge toute structure arbitraire de site en utilisant [des pages de redirection fantômes](#shadow-structure) pour représenter une structure autre que la structure de contenu principale.

La boîte de dialogue de [modification](#edit-dialog) permet à l’auteur de contenu de définir la page racine de navigation ainsi que la profondeur de navigation. La boîte de dialogue de [conception](#design-dialog) permet à l’auteur du modèle de définir les valeurs par défaut de la racine de navigation et de la profondeur.

## Prise en charge de la structure de site localisée {#localized-site-structure}

Souvent, les sites web sont proposés en plusieurs langues pour différentes zones géographiques. En règle générale, chaque page localisée contient un élément de navigation qui est inclus dans le modèle de page. Le composant de navigation permet de le placer une fois sur un modèle pour toutes les pages du site. Il s’adapte ensuite automatiquement aux pages localisées individuelles en fonction de la structure de site globalisée.

* Pour un exemple du fonctionnement de la fonction de localisation du composant de navigation, reportez-vous à [la section ci-dessous](#example-localization).
* Pour un exemple de la façon dont les fonctions de localisation des composants principaux fonctionnent ensemble, reportez-vous à la page [Fonctions de localisation de la page Composants principaux](/help/get-started/localization.md).

### Exemple {#example-localization}

Imaginons que votre contenu ressemble à ceci :

```
/content
+-- wknd
   +-- language-masters
      +-- de
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- en
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- es
      +-- fr
      \-- it
   +-- us
      +-- en
         \-- experience
            \-- arctic-surfing-in-lofoten
      \-- es
   \-- ch
      +-- de
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

Pour le site WKND, il est probable que vous souhaitiez placer le composant Navigation dans un modèle de page incorporé à l’en-tête. Une fois qu’il fait partie du modèle, vous pouvez définir la **racine de navigation** du composant sur `/content/wknd/language-masters/en` puisque c’est là où commence le contenu principal de ce site. Il peut également être judicieux de définir **la profondeur de la structure de navigation** sur `2` puisque vous ne souhaitez probablement pas que l’intégralité de l’arborescence de contenu soit affichée par le composant, mais plutôt les deux premiers niveaux afin de servir d’aperçu.

Avec **la valeur racine de navigation**, le composant de navigation sait que la `/content/wknd/language-masters/en`navigation démarre et qu’elle peut générer des options de navigation en effectuant une récurrence de la structure du site deux niveaux vers le bas (comme défini par la valeur de **profondeur de la structure de navigation**).

Quelle que soit la page localisée consultée par un utilisateur, le composant de navigation par langue est capable de trouver la page localisée correspondante en connaissant l’emplacement de la page actuelle et en remontant à la racine, puis en revenant à la page correspondante.

Ainsi, si un visiteur consulte `/content/ch/de/experience/arctic-surfing-in-lofoten`, le composant sait comment générer la structure de navigation sur la base de `/content/wknd/language-masters/de`. De même, si le visiteur consulte `/content/us/en/experience/arctic-surfing-in-lofoten`, le composant sait comment générer la structure de navigation en fonction de `/content/wknd/language-masters/en`.

## Prise en charge de la structure de site fantôme {#shadow-structure}

Parfois, il est nécessaire de créer un menu de navigation pour le visiteur différent de la structure réelle du site. Par exemple, une promotion peut mettre en surbrillance certains contenus du menu en réorganisant la liste du contenu. En utilisant des pages fantômes qui redirigent simplement vers d’autres pages de contenu, le composant de navigation peut générer n’importe quelle structure de navigation arbitraire nécessaire.

Pour ce faire, vous devez :

1. Créer des pages fantômes en tant que pages vides représentant la structure désirée du site. On parle généralement de structure de site fantôme.
1. Définir les valeurs de **redirection** dans les propriétés de page sur ces pages pour qu’elles pointent vers les pages de contenu.
1. Définir l’option **Masquer dans la navigation** dans les propriétés de page des pages fantômes.
1. Définir la valeur de **racine de navigation** du composant de navigation pour qu’elle pointe vers la racine de la nouvelle structure du site fantôme.

Le composant de navigation affichera alors le menu en fonction de la structure du site fantôme. Les liens rendus par le composant correspondent aux pages de contenu réelles vers lesquelles les pages fantômes redirigent et non les pages fantômes elles-mêmes. En outre, le composant affiche les noms des pages réelles et met correctement en surbrillance la page active, même lorsque la navigation est basée sur des pages fantômes. Le composant de navigation rend les pages fantômes complètement transparentes pour le visiteur.

>[!NOTE]
>Les pages fantômes rendent vos options de navigation beaucoup plus flexibles, mais gardez à l’esprit que la maintenance de cette structure est ensuite totalement manuelle. Si vous réorganisez le contenu réel du site ou ajoutez/supprimez du contenu, vous devrez mettre à jour manuellement la structure fantôme si nécessaire.

>[!NOTE]
>Lors du rendu d’une structure de site fantôme, seules les pages fantômes sont répétées par la logique de navigation. La logique ne répète pas la structure des destinations de redirection.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de navigation est v1, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018 et est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant de navigation et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [Bibliothèque de composants](https://adobe.com/go/aem_cmp_library_navigation_fr).

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant de navigation [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_navigation_v1).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

>[!NOTE]
>
>À compter de la version 2.1.0 des composants principaux, le composant de navigation prend en charge [les microdonnées schema.org](https://schema.org).

## Boîte de dialogue de modification {#edit-dialog}

Dans la boîte de dialogue de modification, l’auteur du contenu peut définir la page racine pour la navigation et la profondeur de la structure de navigation.

### Onglet Propriétés {#properties-tab}

![Onglet Propriétés de la boîte de dialogue de modification du composant Navigation](/help/assets/navigation-edit-properties.png)

* **Racine de navigation** : page racine qui sera utilisée pour générer l’arborescence de navigation.
* **Exclure les niveaux racine** : il arrive souvent que la racine ne doive pas être incluse dans la navigation. Cette option vous permet de spécifier le nombre de niveaux que vous souhaitez exclure à partir de la racine. Par exemple :
   * 0 = afficher le niveau racine
   * 1 = exclure le niveau racine
   * 2 = exclure la racine et 1 niveau supérieur
   * etc.
* **Collecter toutes les pages enfants** : collecte toutes les pages qui sont des descendants de la racine de navigation.
* **Profondeur de la structure de navigation** : définit le nombre de niveaux vers le bas de l’arborescence de navigation que le composant doit afficher par rapport à la racine de navigation (disponible uniquement si **Collecter toutes les pages enfants** n’est pas sélectionné).
* **Désactiver l’effet d’ombre portée** : si la page de la hiérarchie est une redirection, le nom de la page de redirection s’affiche à la place de la cible. Pour plus d’informations, consultez [Prise en charge de la structure de site fantôme](#shadow-structure).
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

### Onglet Accessibilité {#accessibility-tab}

![Onglet Accessibilité de la boîte de dialogue de modification du composant Navigation](/help/assets/navigation-edit-accessibility.png)

Dans l’onglet **Accessibilité**, les valeurs peuvent être définies pour les étiquettes d’[accessibilité ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) du composant.

* **Étiquette** : Valeur d’un attribut de étiquette ARIA pour le composant

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les valeurs par défaut de la page racine de navigation et de la profondeur de navigation présentée aux auteurs de contenu.

### Onglet Propriétés {#properties-tab-design}

![Boîte de dialogue de conception du composant Navigation](/help/assets/navigation-design.png)

* **Racine de navigation** : valeur par défaut de la page racine de la structure de navigation, qui sera utilisée pour générer l’arborescence de navigation. La valeur par défaut est définie lorsque l’auteur du contenu ajoute le composant à la page.
* **Exclure les niveaux racine** : il arrive souvent que la racine ne doive pas être incluse dans la navigation. Cette option vous permet de spécifier la valeur par défaut du nombre de niveaux que vous souhaitez exclure à partir de la racine. Par exemple :
   * 0 = afficher le niveau racine
   * 1 = exclure le niveau racine
   * 2 = exclure la racine et 1 niveau supérieur
   * etc.
* **Collecter toutes les pages enfants** : valeur par défaut de la collecte de toutes les pages qui sont des descendants de la racine de navigation.
* **Profondeur de la structure de navigation** : valeur par défaut de la profondeur de la structure de navigation.
* **Désactiver l’effet d’ombre portée** : valeur par défaut de l’option indiquant si la fonction fantôme doit être désactivée lors de l’ajout d’un composant Navigation

### Onglet Styles {#styles-tab}

Le composant de navigation prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

## Couche de données client Adobe {#data-layer}

Le composant Navigation prend en charge la [couche de données client Adobe](/help/developing/data-layer/overview.md).
