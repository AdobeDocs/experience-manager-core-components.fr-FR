---
title: Composant Liste (v2)
description: Le composant Liste des composants principaux permet de créer facilement des listes dynamiques et statiques.
role: Developer, Admin, User
exl-id: fa34be64-b345-45cd-baf3-571973414852
index: false
TQID: https://experienceleague.adobe.com/9zz16bJ7tDpOSntRTbPDUJQIabSAmIfvRPCD067tQXc
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 1020
ht-degree: 100%

---

# Composant Liste (v2) {#list-component}

Le composant principal Liste permet de créer facilement des listes dynamiques et statiques.

## Utilisation {#usage}

Le composant Liste peut servir à créer, par exemple, une liste dynamique de pages enfants ou une liste statique d’éléments définis de manière arbitraire. Le type de liste disponible et les options de mise en forme peuvent être définis par l’auteur du modèle dans la [boîte de dialogue de conception](#design-dialog). L’éditeur de contenu peut sélectionner les types de liste disponibles et mettre en forme les éléments de liste dans la [boîte de dialogue de modification](#edit-dialog).

## Version et compatibilité {#version-and-compatibility}

Ce document décrit la version v1 du composant Liste, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018.

>[!CAUTION]
>
>Ce document décrit la version v2 du composant Liste.
>
>Pour plus d’informations sur la version actuelle du composant Liste, voir le document [Composant Liste](/help/components/list.md).

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

La documentation technique la plus récente sur le composant de liste [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_list_v2_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation relative au développement des composants principaux](/help/developing/overview.md).

## Boîte de dialogue de modification {#edit-dialog}

La boîte de dialogue de modification permet à l’auteur du contenu de configurer la liste et les éléments de la liste.

### Onglet Paramètres de liste {#list-settings-tab}

La liste peut être générée de différentes manières.

* [Pages enfants](#child-pages)
* [Liste fixe](#fixed-list)
* [Rechercher](#search-options)
* [Balises](#tags)

Quelle que soit la façon dont la liste est créée, il existe des [options de tri et d’ID](#sort-options) qui peuvent toujours être configurées.

![Boîte de dialogue de modification du composant Liste](/help/assets/v2/list-edit.png)

Selon la manière dont l’auteur du contenu choisit de construire la liste, les options de configuration supplémentaires changent.

#### Pages enfants {#child-pages}

La liste peut être créée à partir des pages enfants de la page active ou d’une autre page.

![Options de page enfant](/help/assets/v2/list-edit-child-pages.png)

* **Page parente**
   * Page dont les pages enfants doivent faire la liste.
   * Laissez vide pour utiliser la page active.

* **Profondeur enfant**
Nombre de niveaux vers le bas dans la hiérarchie.

#### Liste fixe {#fixed-list}

La liste peut être créée à l’aide d’une liste fixe d’éléments.

![Options de liste fixe](/help/assets/v2/list-edit-fixed-list.png)

Appuyez ou cliquez sur le bouton **Ajouter** pour insérer un nouvel élément dans la liste.

* Entrez le texte de l’élément dans la liste ou utilisez la **boîte de dialogue Sélection** pour choisir un élément dans AEM.
* Utilisez la poignée de glisser-déplacer pour réorganiser les éléments de la liste.
* Utilisez l’icône de corbeille pour supprimer les éléments de la liste.

#### Rechercher {#search-options}

La liste peut être créée à l’aide des résultats d’une recherche de contenu AEM.

![Options de liste de recherche](/help/assets/v2/list-edit-search.png)

* **Requête de recherche**
Chaîne pour laquelle une recherche de texte intégral est exécutée pour générer les éléments de la liste.
* **Rechercher dans**
Emplacement où la recherche doit être exécutée.
   * Utilisez la **boîte de dialogue Sélection** pour choisir l’emplacement dans AEM.
   * Utilisez la page active si laissée vide.

#### Balises {#tags}

La liste peut être créée à l’aide de pages qui correspondent à certaines balises sous un emplacement particulier.

![Options de liste de balises](/help/assets/v2/list-edit-tags.png)

* **Page parente**
Emplacement où la correspondance des balises doit commencer.
   * Utilisez la **boîte de dialogue Sélection** pour choisir l’emplacement dans AEM.
   * Utilisez la page active si laissée vide.
* **Balises**
Quelles balises doivent correspondre.
   * Utilisez la boîte de dialogue **Parcourir** pour sélectionner les balises.
* **Correspondance**
Définissez le type de correspondance à associer à une page à inclure dans la liste.
   * **n’importe quelle balise**
   * **toutes les balises**

#### Options de tri {#sort-options}

Quelle que soit la manière dont vous choisissez de créer la liste, certaines options de tri peuvent toujours être définies.

![Options de tri](/help/assets/v2/list-edit-sort-options.png)

* **Classer par**
Comment les éléments doivent être triés.
   * **Titre**
   * **Date de dernière modification**
* **Ordre de tri**
Ordre dans lequel les éléments doivent être triés.
   * **croissant**
   * **décroissant**
* **Nombre max. d’éléments**
Nombre maximal d’éléments affichés dans la liste.
   * Laissez vide pour renvoyer tous les éléments.
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

### Onglet Paramètres d’élément {#item-settings-tab}

À l’aide de l’onglet Paramètres d’élément, la mise en forme des éléments de liste peut être configurée.

![Paramètres d’élément](/help/assets/v2/list-edit-item-settings.png)

* **Lier les éléments**
Éléments de lien vers la page correspondante.
* **Afficher la description**
Permet d’afficher les descriptions de l’élément de lien.
* **Afficher la date**
Permet d’afficher la date de modification de l’élément de lien.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les types de listes à autoriser aux auteurs de contenu ainsi que les paramètres d’éléments disponibles.

### Paramètres de liste {#list-settings}

Dans l’onglet **Paramètres de liste**, le format de date peut être défini et le type de liste doit être disponible dans le composant pour les auteurs de contenu.

![Paramètre de liste de la boîte de dialogue de conception du composant Liste](/help/assets/v2/list-design-list-settings.png)

* **Format de date**
Format à utiliser pour l’affichage de la date de la dernière modification
* **Désactiver les enfants**
Désactivez le type de liste enfants dans le composant.
* **Désactiver statique**
Désactivez le type de liste statique dans le composant.
* **Désactiver la recherche**
Désactivez le type de liste de recherche dans le composant.
* **Désactiver les balises**
Désactivez le type de liste des balises dans le composant.

### Paramètres d’élément {#item-settings}

Dans l’onglet **Paramètres d’élément**, les options de mise en forme des éléments de liste individuels qui doivent être disponibles dans le composant pour les auteurs de contenu peuvent être définies.

![Paramètre d’élément de la boîte de dialogue de conception du composant Liste](/help/assets/v2/list-design-item-settings.png)

* **Lier les éléments**
Activez l’option Éléments de lien dans la [boîte de dialogue de modification](#edit-dialog).
* **Afficher les descriptions**
Activez l’option Afficher les descriptions dans la [boîte de dialogue de modification](#edit-dialog).
* **Afficher la date**
Activez l’option Afficher la date dans la [boîte de dialogue de modification](#edit-dialog).

### Onglet Styles {#styles-tab}

Le composant d’image prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

## Couche de données client Adobe {#data-layer}

Le composant Liste prend en charge la [couche de données client Adobe](/help/developing/data-layer/overview.md).
