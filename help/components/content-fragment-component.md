---
title: Composant de fragment de contenu
description: Le composant de fragment de contenu des composants principaux permet l’affichage d’un fragment de contenu.
translation-type: tm+mt
source-git-commit: d3ebcea5fa1523c1a986841cd3d1a64e16e85f6d
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 98%

---


# Composant de fragment de contenu{#content-fragment-component}

Le composant de fragment de contenu des composants principaux permet l’affichage d’un [fragment de contenu](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html).

>[!NOTE]
>
>Avant la version 2.4.0 des composants principaux, le composant de fragment de contenu était disponible en tant qu’extension aux composants principaux et devait être téléchargé séparément et explicitement activé.

## Utilisation {#usage}

Le composant de fragment de contenu des composants principaux permet d’inclure un [fragment de contenu](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) sur une page.

* Le fragment et ses propriétés peuvent être sélectionnés dans la [boîte de dialogue de configuration](#configure-dialog).
* Les types de ressources qui permettent de gérer certaines images et grilles peuvent être définis dans la [boîte de dialogue de conception](#design-dialog).
* L’option d’édition ouvre le fragment sélectionné dans l’[éditeur de fragments de contenu](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments-variations.html).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de fragment de contenu est v1, qui a été introduite avec la version 1.1.0 des composants principaux d’octobre 2017. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible | Compatible | Compatible |

>[!NOTE]
>
>Avant la version 2.4.0, le composant de fragment de contenu se trouvait dans le dossier des extensions.
>
> `apps/core/wcm/extension/components/contentfragment/v1/contentfragment`
> 
>À partir de la version 2.4.0, il a été déplacé à l’emplacement ci-après.
>
>`apps/core/wcm/components/contentfragment/v1/contentfragment`
>
>Bien que la version de tous les deux soit v1, tout composant de fragment de contenu ayant été utilisé à partir du dossier des extensions nécessite la migration de ses composants proxy associés pour utiliser le nouveau type de ressource lors de la mise à niveau vers la version 2.4.0 ou ultérieure des composants principaux.

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant de fragment de contenu et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_cf).

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Fragment de contenu [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_cf_v1).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de définir le fragment de contenu et les éléments de ce fragment à inclure.

### Onglet Propriétés {#properties-tab}

![Composant Fragment de contenu](/help/assets/content-fragment-edit-properties.png)

* **Fragment de contenu**

   * Chemin d’accès au fragment de contenu souhaité
   * Vous pouvez utiliser la **boîte de dialogue de sélection** pour localiser le fragment.

* **Mode d’affichage**
   * **Un seul élément de texte** : permet la sélection d’un élément de texte multiligne et active les options de contrôle des paragraphes.
   * **Plusieurs éléments** : permet la sélection d’un ou de plusieurs éléments du fragment de contenu sélectionné.
* **Élément** : élément ou éléments du fragment de contenu à inclure.
* **Variation** : variante du fragment de contenu à utiliser (par défaut, **Gabarit**).

* **Paragraphes**

   * **Tous** : permet d’afficher tous les paragraphes.
   * **Étendue**

      * Spécifiez les plages de paragraphes à afficher, séparées par un point-virgule.
      * Par exemple, `1;3-5;7;9-*` pour inclure les paragraphes 1, 3 à 5, 7 et 9 aux paragraphes finaux.
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

### Onglet Contrôle de paragraphe {#paragraph-control-tab}

Cet onglet n’est pas disponible lorsque le mode **Plusieurs éléments** est sélectionné.

![Composant Fragment de contenu](/help/assets/content-fragment-edit-paragraph.png)

* **Paragraphes** : permet la sélection de tous les paragraphes ou d’une plage.
* **Gérer les en-têtes comme leurs propres paragraphes**

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les types de ressources utilisés pour traiter les images de supports variés et les grilles adaptées.

![Boîte de dialogue de conception du composant Fragment de contenu](/help/assets/content-fragment-design.png)

* **Grille réactive interne**

   * Type de ressource Sling utilisé pour la grille réactive interne

## Couche de données client Adobe {#data-layer}

Le composant Fragment de contenu prend en charge la couche de données client [Adobe.](/help/developing/data-layer/overview.md)
