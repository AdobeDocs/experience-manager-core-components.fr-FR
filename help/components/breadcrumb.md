---
title: Composant de chemin de navigation
description: Le composant de chemin de navigation des composants principaux est un composant de navigation qui crée un chemin de navigation des liens en fonction de l’emplacement de la page dans la hiérarchie du contenu.
translation-type: ht
source-git-commit: d3ebcea5fa1523c1a986841cd3d1a64e16e85f6d
workflow-type: ht
source-wordcount: '722'
ht-degree: 100%

---


# Composant de chemin de navigation {#breadcrumb-component}

Le composant de chemin de navigation des composants principaux est un composant de navigation qui crée un chemin de navigation des liens en fonction de l’emplacement de la page dans la hiérarchie du contenu.

## Utilisation {#usage}

Le composant de chemin de navigation affiche la position de la page actuelle dans la hiérarchie du site, ce qui permet aux visiteurs de la page de parcourir la hiérarchie de celle-ci à partir de leur emplacement actuel. Cela est souvent intégré dans les en-têtes ou pieds de page.

Les options disponibles, telles que le niveau de navigation par défaut et la possibilité d’afficher la ou les pages masquées, peuvent être définies par l’auteur du modèle dans la [boîte de dialogue de conception](#design-dialog). L’éditeur de contenu peut ensuite choisir si les pages masquées doivent être affichées ou non et le niveau de navigation actuel du composant dans la [boîte de dialogue de modification](#edit-dialog).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de chemin de navigation est v2, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- | --- |--- |---|
| v2 | Compatible | Compatible | Compatible |
| [v1](v1/breadcrumb-v1.md) | Compatible | Compatible | - |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant de chemin de navigation et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_breadcrumb_fr).

>[!NOTE]
>
>À compter de la version 2.1.0 des composants principaux, le composant de chemin de navigation prend en charge les [microdonnées schema.org](https://schema.org/BreadcrumbList).

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant de chemin de navigation [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de modification {#edit-dialog}

La boîte de dialogue de modification permet à l’auteur de contenu de supprimer les pages masquées et actives dans les chemins de navigation ainsi que la profondeur de la hiérarchie qu’elle doit afficher.

![Boîte de dialogue de modification du composant Chemin de navigation](/help/assets/breadcrumb-edit.png)

* **Niveau de départ de la navigation** : à quel niveau dans la hiérarchie le composant de chemin de navigation doit commencer à descendre jusqu’à la page actuelle. Par exemple :

   * 0 commence à `/content`
   * 1 commence à `/content/<yourSite>`
   * 2 commence à `/content/<yourSite>/<country>`

* **Afficher les éléments de navigation masqués** : affichez les pages marquées comme étant masquées dans le chemin de navigation (elles ne sont pas affichées par défaut).
* **Masquer la page active** : supprime la page actuelle dans le chemin de navigation (par défaut, elle s’affiche).
* **Désactiver l’effet d’ombre portée** : si la page de la hiérarchie est une redirection, le nom de la page de redirection s’affiche à la place de la cible. Pour plus d’informations, consultez [Prise en charge de la structure de site fantôme](navigation.md#shadow-structure) du composant Navigation.
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les valeurs par défaut des options de suppression des pages masquées et actives dans les chemins de navigation, ainsi que la profondeur de la hiérarchie qu’elle doit afficher.

### Onglet principal {#main-tab}

![](/help/assets/breadcrumb-design.png)

* **Niveau de départ de la navigation** définit la valeur par défaut à partir de laquelle le composant de chemin de navigation doit commencer à se déplacer jusqu’à la page actuelle lorsqu’il est ajouté à une page.
* **Afficher les éléments de navigation masqués** : définit la valeur par défaut de l’option **Afficher les éléments de navigation masqués** lorsque le composant de chemin de navigation est ajouté à une page.

   * Cela n’active ou ne désactive pas l’option de l’auteur. Cela définit uniquement la valeur par défaut.

* **Masquer la page active** : définit la valeur par défaut de l’option **Masquer la page active** lorsque le composant de chemin de navigation est ajouté à une page.

   * Cela n’active ou ne désactive pas l’option de l’auteur. Cela définit uniquement la valeur par défaut.

* **Désactiver l’effet d’ombre portée** : définit la valeur par défaut de l’option **Désactiver l’effet d’ombre portée** lorsque le composant Chemin de navigation est ajouté à une page.

### Onglet Styles {#styles-tab}

Le composant de chemin de navigation prend en charge le [système de style AEM](/help/get-started/authoring.md#component-styling).

## Couche de données client Adobe {#data-layer}

Le composant Chemin de navigation prend en charge la [couche de données client Adobe](/help/developing/data-layer/overview.md).
