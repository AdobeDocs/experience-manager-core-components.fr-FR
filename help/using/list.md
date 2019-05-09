---
title: Liste des composants
seo-title: Liste des composants
description: 'null'
seo-description: Le composant Liste des composants principaux permet de créer facilement des listes dynamiques et statiques.
uuid: 50 a 572 e 8-b 444-4 f 7 d -82 bc -5 a 93 ebb 4 be 95
contentOwner: Utilisateur
content-type: référence
topic-tags: création
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 89053323-6221-46 ed -896 a -31 a -31 a 42 c 55282
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
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Liste des composants{#list-component}

Le composant Liste des composants principaux permet de créer facilement des listes dynamiques et statiques.

## Utilisation {#usage}

Le composant Liste peut servir à créer, par exemple, une liste dynamique de pages enfants ou une liste statique d&#39;éléments définis de manière arbitraire. Le type de liste disponible et les options de formatage peuvent être définies par l&#39;auteur du modèle dans la boîte de dialogue [de conception](#design-dialog). L&#39;éditeur de contenu peut sélectionner les types de liste disponibles et formater les éléments de liste dans la boîte de dialogue [Modifier](#edit-dialog).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant List est v 2, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018 et est décrite dans ce document.

Le tableau suivant détaille toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatible | Compatible | Compatible |
| [v1](list-v1.md) | Compatible | Compatible | Compatible |

Pour plus d&#39;informations sur les versions et les versions des composants principaux, consultez les versions des composants de Document [principaux](versions.md).

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple tiré de [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Capture d’écran {#screenshot}

![](assets/screen_shot_2018-01-12at105924.png)

### Bibliothèque de composants

Pour tester le composant Liste ainsi que des exemples d&#39;options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque Composant](http://opensource.adobe.com/aem-core-wcm-components/library/list.html).

### Détails techniques {#technical-details}

Vous trouverez la documentation technique la plus récente sur le composant [de liste sur github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/list/v2/list).

Vous trouverez plus d&#39;informations sur le développement des composants principaux dans la documentation destinée aux développeurs de composants [principaux](developing.md).

## Modifier le dialogue {#edit-dialog}

Le dialogue Modifier permet à l&#39;auteur du contenu de configurer la liste et les éléments de la liste.

### Onglet Paramètres de liste {#list-settings-tab}

La liste peut être générée de différentes manières.

* [Pages enfants](#child-pages)
* [Liste fixe](#fixed-list)
* [Rechercher](#search-options)
* [Balises](#tags)

Quelle que soit la création de la liste, il existe des options [de tri](#sort-options) qui peuvent toujours être configurées.

![](assets/chlimage_1-38.png)

Selon la manière dont l&#39;auteur du contenu choisit de construire la liste, les options de configuration supplémentaires changent.

#### Pages enfants {#child-pages}

La liste peut être créée des pages enfants de la page active ou d&#39;une autre page.

![](assets/chlimage_1-39.png)

* **Page parente**
   * Page dont les pages enfants doivent faire la liste
   * Laisser vide pour utiliser la page active

* **Profondeur de l&#39;enfant**
combien de niveaux dans la hiérarchie doivent être utilisés

#### Liste fixe {#fixed-list}

La liste peut être créée à l&#39;aide d&#39;une liste fixe d&#39;éléments.

![](assets/chlimage_1-40.png)

Appuyez ou cliquez sur le **bouton Ajouter** pour insérer un nouvel élément dans la liste.

* Entrez le texte de l&#39;élément dans la liste ou utilisez le dialogue **de sélection** pour choisir un élément dans AEM.
* Utilisez la poignée de glisser-déplacer pour réorganiser les éléments de la liste.
* Utilisez l&#39;icône de corbeille pour supprimer les éléments de la liste.

#### Recherche {#search-options}

La liste peut être créée à l&#39;aide des résultats d&#39;une recherche de contenu AEM.

![](assets/chlimage_1-41.png)

* **Requête**
de recherche Chaîne pour laquelle une recherche de texte intégral est exécutée pour générer les éléments de la liste
* **Recherche dans**
l&#39;emplacement où la recherche doit être exécutée
   * Utilisation de **la boîte de dialogue** de sélection pour choisir l&#39;emplacement dans AEM
   * Utiliser la page active si laissée vide

#### Balises {#tags}

La liste peut être créée à l&#39;aide de pages qui correspondent à certaines balises sous un emplacement particulier.

![](assets/chlimage_1-42.png)

* **Page
parente** où la correspondance des balises doit commencer
   * Utilisation de **la boîte de dialogue** de sélection pour choisir l&#39;emplacement dans AEM
   * Utiliser la page active si laissée vide
* **Balises**
pour lesquelles les balises doivent correspondre
   * Utilisez le dialogue **Parcourir** pour sélectionner les balises.
* **Correspondance**
Définit le type de correspondance doit qualifier une page à inclure dans la liste
   * **n’importe quelle balise**
   * **toutes les balises**

#### Options de tri {#sort-options}

Quelle que soit la manière dont vous choisissez de créer la liste, certaines options de tri peuvent toujours être définies.

![](assets/chlimage_1-43.png)

* **Ordre de**
tri des éléments
   * **Titre**
   * **Date de dernière modification**
* **Ordre**
de tri Ordre dans lequel les éléments doivent être triés
   * **croissant**
   * **décroissant**
* **Nombre max. d&#39;éléments**
Nombre maximal d&#39;éléments affichés dans la liste.
   * Laisser vide pour renvoyer tous les éléments.

### Onglet Paramètres d&#39;élément {#item-settings-tab}

A l&#39;aide de l&#39;onglet Paramètres d&#39;élément, la mise en forme des éléments de liste peut être configurée.

![](assets/chlimage_1-44.png)

* **Lien Éléments**
de lien vers la page correspondante
* **Afficher Description**
Afficher les descriptions de l&#39;élément de lien
* **Afficher la date de modification de la date**
de modification de l&#39;élément de lien

## Créer un dialogue {#design-dialog}

Le dialogue de conception permet à l&#39;auteur du modèle de définir les types de listes à autoriser aux auteurs de contenu ainsi que les paramètres d&#39;éléments disponibles.

### Paramètres de liste {#list-settings}

Dans **l&#39;onglet Paramètres** de liste, le format de date peut être défini et le type de liste doit être disponible dans le composant aux auteurs de contenu.

![](assets/chlimage_1-45.png)

* **Format de format**
de date à utiliser pour l&#39;affichage de la date de dernière modification
* **Désactivation des enfants**
Désactive le type de liste des enfants dans le composant
* **Désactiver**la désactivation du
type de liste statique dans le composant
* **Désactiver la recherche**
Désactive le type de liste de recherche dans le composant
* **Désactiver les balises**
Désactive le type de liste des balises dans le composant

### Paramètres d’élément {#item-settings}

Dans **l&#39;onglet Paramètres** d&#39;élément, les options de formatage des éléments de liste individuels qui doivent être disponibles dans le composant pour les auteurs de contenu peuvent être définies.

![](assets/chlimage_1-46.png)

* **Option**d&#39;activation des
éléments de lien activée dans la boîte de dialogue [Modifier](#edit-dialog)
* **Afficher les descriptions**
Activez l&#39;option Afficher les descriptions dans le [dialogue Modifier](#edit-dialog)
* **Afficher la date**
Activer l&#39;option Afficher la date dans le [dialogue Modifier](#edit-dialog)

### Onglet Styles {#styles-tab}

Le composant Image prend en charge le système [de style AEM](authoring.md#component-styling).