---
title: Composant Fragment de contenu
description: Le composant de fragment de contenu des composants principaux permet l’affichage d’un fragment de contenu.
role: Developer, Admin, User
exl-id: 551ff2a1-f8db-490c-84a3-4255b364fc83
TQID: https://experienceleague.adobe.com/0DtXdVGWrkNjQrgW9Vye-g21IlySz4fjYpZLQ5twQrM
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 693
ht-degree: 100%

---

# Composant Fragment de contenu{#content-fragment-component}

Le composant Fragment de contenu des composants principaux permet l’affichage d’un [fragment de contenu](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=fr).

>[!NOTE]
>
>Avant la version 2.4.0 des composants principaux, le composant de fragment de contenu était disponible en tant qu’extension aux composants principaux et devait être téléchargé séparément et explicitement activé.

{{traditional-aem}}

## Utilisation {#usage}

Le composant de fragment de contenu des composants principaux permet d’inclure un [fragment de contenu](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=fr) sur une page.

* Le fragment et ses propriétés peuvent être sélectionnés dans la [boîte de dialogue de configuration](#configure-dialog).
* Les types de ressources qui permettent de gérer certaines images et grilles peuvent être définis dans la [boîte de dialogue de conception](#design-dialog).
* L’option d’édition ouvre le fragment sélectionné dans l’[éditeur de fragments de contenu](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments-variations.html?lang=fr).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de fragment de contenu est v1, qui a été introduite avec la version 1.1.0 des composants principaux d’octobre 2017. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |---|---|---|
| v1 | Compatible avec la <br>[version 2.17.4](/help/versions.md) et versions antérieures | Compatible | Compatible | Compatible |

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

Pour tester le composant de fragment de contenu et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_cf_fr).

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Fragment de contenu [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_cf_v1_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation relative au développement des composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de définir le fragment de contenu et les éléments de ce fragment à inclure.

### Onglet Propriétés {#properties-tab}

![Composant Fragment de contenu](/help/assets/content-fragment-edit-properties.png)

* **Fragment de contenu**

   * Chemin d’accès au fragment de contenu souhaité
   * Vous pouvez utiliser la **boîte de dialogue de sélection** pour localiser le fragment.

* **Mode d’affichage**
   * **Un seul élément texte** : permet la sélection d’un élément de texte multiligne et active les options de contrôle des paragraphes.
   * **Plusieurs éléments** : permet la sélection d’un ou de plusieurs éléments du fragment de contenu sélectionné.
* **Élément** : élément ou éléments du fragment de contenu à inclure.
* **Variation** : variante du fragment de contenu à utiliser (par défaut, **Gabarit**).

* **Paragraphes**

   * **Tout** : permet d’afficher tous les paragraphes.
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

Le composant Fragment de contenu prend en charge la [couche de données client Adobe](/help/developing/data-layer/overview.md).
