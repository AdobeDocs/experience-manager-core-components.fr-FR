---
title: Composant Liste (v3)
description: Le composant principal « Liste » (v3) permet de créer facilement des listes dynamiques et statiques.
role: Architect, Developer, Admin, User
exl-id: 4aefce2e-9c22-4c6d-869e-aaa8c246b073
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Composant Liste (v3) {#list-component}

Le composant principal « Liste » (v3) permet de créer facilement des listes dynamiques et statiques.

## Utilisation {#usage}

Le composant « Liste » (v3) peut servir à créer, par exemple, une liste dynamique de pages enfants ou une liste statique d’éléments définis de manière arbitraire. Le type de liste disponible et les options de mise en forme peuvent être définis par l’auteur du modèle dans la [boîte de dialogue de conception](#design-dialog). L’éditeur de contenu peut sélectionner les types de liste disponibles et mettre en forme les éléments de liste dans la [boîte de dialogue de modification](#edit-dialog).

## Version et compatibilité {#version-and-compatibility}

Ce document décrit la version v3 du composant « Liste », qui a été introduite avec la version 2.18.0 des composants principaux en février 2022.

>[!CAUTION]
>
>Ce document décrit la version v3 du composant Liste.
>
>Pour plus d’informations sur la version actuelle du composant Liste, voir le document [Composant Liste](/help/components/list.md).

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| [v4](/help/components/list.md) | - | Compatible | Compatible |
| v3 | - | Compatible | Compatible |
| [v2](/help/components/v2/list.md) | Compatible | Compatible | Compatible |
| [v1](/help/components/v1/list-v1.md) | Compatible | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Redirections dans les listes {#redirects}

Lorsqu’une page a une cible de redirection (et ce, qu’elle pointe vers une URL externe ou vers une autre page AEM), une liste contenant des liens vers cette cible pointe directement vers l’URL de la cible de redirection.

### Exemple {#redirect-example}

* Créez une page A qui redirige vers la page B.
* Créez une page C qui redirige vers `https://aemcomponents.dev`
* Sur une page D, insérez un composant de liste contenant les pages A et C
* Les liens respectifs générés pointent alors directement vers la page B et `https://aemcomponents.dev`

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant de liste et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_list_fr).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant de liste [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_list_v3_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de modification {#edit-dialog}

La boîte de dialogue de modification permet à l’auteur du contenu de configurer la liste et les éléments de la liste.

### Onglet Paramètres de liste {#list-settings-tab}

La liste peut être générée de différentes manières.

* [Pages enfants](#child-pages)
* [Liste fixe](#fixed-list)
* [Rechercher](#search-options)
* [Balises](#tags)

Quelle que soit la façon dont la liste est créée, il existe des [options de tri et d’ID](#sort-options) qui peuvent toujours être configurées.

![Boîte de dialogue de modification du composant Liste](/help/assets/v3/list-edit.png)

Selon la manière dont l’auteur du contenu choisit de construire la liste, les options de configuration supplémentaires changent.

#### Pages enfants {#child-pages}

La liste peut être créée à partir des pages enfants de la page active ou d’une autre page.

![Options de page enfant](/help/assets/v3/list-edit-child-pages.png)

* **Page parente**
   * Page dont les pages enfants doivent faire la liste.
   * Laissez vide pour utiliser la page active.

* **Profondeur-enfant**
Combien de niveaux dans la hiérarchie doivent être utilisés.

#### Liste fixe {#fixed-list}

La liste peut être créée à l’aide d’une liste fixe d’éléments.

![Options de liste fixe](/help/assets/v3/list-edit-fixed.png)

Appuyez ou cliquez sur le bouton **Ajouter** pour insérer un nouvel élément dans la liste.

* Entrez le texte de l’élément dans la liste ou utilisez la **boîte de dialogue Sélection** pour choisir un élément dans AEM.
* Utilisez la poignée de glisser-déplacer pour réorganiser les éléments de la liste.
* Utilisez l’icône de corbeille pour supprimer les éléments de la liste.

#### Rechercher {#search-options}

La liste peut être créée à l’aide des résultats d’une recherche de contenu AEM.

![Options de liste de recherche](/help/assets/v3/list-edit-search.png)

* **Requête de recherche**
Chaîne pour laquelle une recherche de texte intégral est exécutée afin de générer les éléments de la liste.
* **Recherche dans**
L’emplacement où la recherche doit être exécutée.
   * Utilisez la **boîte de dialogue Sélection** pour choisir l’emplacement dans AEM.
   * Utilisez la page active si laissée vide.

#### Balises {#tags}

La liste peut être créée à l’aide de pages qui correspondent à certaines balises sous un emplacement particulier.

![Options de liste de balises](/help/assets/v3/list-edit-tags.png)

* **Page parente**
Où la correspondance des balises doit commencer.
   * Utilisez la **boîte de dialogue Sélection** pour choisir l’emplacement dans AEM.
   * Utilisez la page active si laissée vide.
* **Balises**
Les balises qui doivent correspondre.
   * Utilisez la boîte de dialogue **Parcourir** pour sélectionner les balises.
* **Correspondance**
Définit quel type de correspondance doit qualifier une page à inclure dans la liste.
   * **n’importe quelle balise**
   * **toutes les balises**

#### Options de tri {#sort-options}

Quelle que soit la manière dont vous choisissez de créer la liste, certaines options de tri peuvent toujours être définies.

![Options de tri](/help/assets/v3/list-edit-sort-options.png)

* **Classer par**
Comment les éléments doivent être triés.
   * **Titre**
   * **Date de dernière modification**
* **Ordre de tri**
Ordre dans lequel les éléments doivent être triés.
   * **croissant**
   * **décroissant**
* **Nombre maximal d’éléments**
Nombre maximal d’éléments affichés dans la liste.
   * Laissez vide pour renvoyer tous les éléments.
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

### Onglet Paramètres d’élément {#item-settings-tab}

À l’aide de l’onglet Paramètres d’élément, la mise en forme des éléments de liste peut être configurée.

![Paramètres d’élément](/help/assets/v3/list-edit-items.png)

* **Lier des éléments** : liez des éléments à la page correspondante.
* **Afficher la description** : affichez les descriptions de l’élément de lien.
* **Afficher la date** : permet d’afficher la date de modification de l’élément de lien.
* **Afficher en tant que teaser** : lorsque cette option est cochée, l’élément est affiché comme un teaser.

### Onglet Styles {#styles-tab-edit}

Le composant Liste prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

Utilisez la liste déroulante pour sélectionner les styles à appliquer au composant. Les sélections effectuées dans la boîte de dialogue de modification ou dans la barre d’outils du composant ont le même effet.

Pour que le menu déroulant soit disponible, les styles doivent être configurés pour ce composant dans la [boîte de dialogue de conception](#design-dialog).

![Onglet Styles de la boîte de dialogue de modification du composant Liste](/help/assets/v3/list-edit-styles.png)

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les types de listes à autoriser aux auteurs de contenu ainsi que les paramètres d’éléments disponibles.

### Paramètres de liste {#list-settings}

Dans l’onglet **Paramètres de liste**, le format de date peut être défini et le type de liste doit être disponible dans le composant pour les auteurs de contenu.

![Paramètre de liste de la boîte de dialogue de conception du composant Liste](/help/assets/v3/list-design-list-settings.png)

* **Format de la date**
Format à utiliser pour l’affichage de la date de la dernière modification.
* **Désactiver les enfants**
Désactive le type de liste enfant dans le composant.
* **Désactiver statique**
Désactive le type de liste statique dans le composant.
* **Désactiver la recherche**
Désactive le type de liste de recherche dans le composant.
* **Désactiver les balises**
Désactive le type de liste de balises dans le composant.

### Paramètres d’élément {#item-settings}

Dans l’onglet **Paramètres d’élément**, les options de mise en forme des éléments de liste individuels qui doivent être disponibles dans le composant pour les auteurs de contenu peuvent être définies.

![Paramètre d’élément de la boîte de dialogue de conception du composant Liste](/help/assets/v3/list-design-item-settings.png)

* **Lier des éléments**
Activez l’option Lier des éléments dans la [boîte de dialogue de modification](#edit-dialog).
* **Afficher la description**
Activez l’option Afficher les descriptions dans la [boîte de dialogue de modification](#edit-dialog).
* **Afficher la date**
Activez l’option Afficher la date dans la [boîte de dialogue de modification](#edit-dialog).

### Onglet Styles {#styles-tab}

Le composant d’image prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

## Couche de données client Adobe {#data-layer}

Le composant Liste prend en charge la [couche de données client Adobe](/help/developing/data-layer/overview.md).
