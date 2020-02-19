---
title: Composant de fragment de contenu
description: Le composant de fragment de contenu des composants principaux permet l’affichage d’un fragment de contenu.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Composant de fragment de contenu{#content-fragment-component}

The Core Component Content Fragment component allows for the display of a [content fragment](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html).

>[!NOTE]
>
>Avant la version 2.4.0 des composants principaux, le composant de fragment de contenu était disponible en tant qu’extension aux composants principaux et devait être téléchargé séparément et explicitement activé.

## Utilisation {#usage}

The Core Component Content Fragment Component allows for the inclusion of a [content fragment](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) on a page.

* Le fragment et ses propriétés peuvent être sélectionnés dans la [boîte de dialogue de configuration](#configure-dialog).
* Les types de ressources qui permettent de gérer certaines images et grilles peuvent être définis dans la [boîte de dialogue de conception](#design-dialog).
* The edit option will open the selected fragment within the [content fragment editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments-variations.html).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de fragment de contenu est v1, qui a été introduite avec la version 1.1.0 des composants principaux d’octobre 2017. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.3 | AEM 6.4 | AEM 6.5 |  d’AEM en tant que Cloud Service |
|--- |--- |--- |---|---|
| v1 | Compatible | Compatible | Compatible | Compatible |

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

Pour tester le composant de fragment de contenu, des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_cf).

## Détails techniques {#technical-details}

The latest technical documentation about the Content Fragment Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_cf_v1).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de définir le fragment de contenu et les éléments de ce fragment à inclure.

![](/help/assets/chlimage_1-87.png)

* **Fragment de contenu**

   * Chemin d’accès au fragment de contenu souhaité
   * Vous pouvez utiliser la **boîte de dialogue de sélection** pour localiser le fragment.

* **Élément** : élément du fragment de contenu à inclure.
* **Variation** : variante du fragment de contenu à utiliser (par défaut, **Gabarit**).

* **Paragraphes**

   * **Tous** : permet d’afficher tous les paragraphes.
   * **Étendue**

      * Spécifiez les plages de paragraphes à afficher, séparées par un point-virgule.
      * Par exemple, `1;3-5;7;9-*` pour inclure les paragraphes 1, 3 à 5, 7 et 9 aux paragraphes finaux.

* **Gérer les en-têtes comme leurs propres paragraphes**

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les types de ressources utilisés pour traiter les images de supports variés et les grilles adaptées.

![](/help/assets/chlimage_1-88.png)

* **Type d’image de supports variés**

   * Type de ressource Sling utilisé pour le rendu des images de supports variés

* **Grille réactive interne**

   * Type de ressource Sling utilisé pour la grille réactive interne
