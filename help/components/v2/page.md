---
title: Composant Page (v2)
description: Le composant Page est un composant de page extensible, conçu pour fonctionner avec l’éditeur de modèles et autoriser l’assemblage de composants d’en-tête/de pied de page et de structure à l’aide de l’éditeur de modèles.
role: Developer, Admin, User
exl-id: e85fe4db-6de4-4a84-a54c-bd07a67efed3
index: false
TQID: https://experienceleague.adobe.com/p1V-3XLpA6H-rC-zWIYFqbPkd6HW7bBLWFXaj8aeNAs
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
subfeature_v2:
  - id: f86a5563-8f73-4ec0-be7d-a1782604870a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 2a9a69dd7eeade8cdc2f681a354350c4370d5d1b
workflow-type: tm+mt
source-wordcount: 753
ht-degree: 90%

---

# Composant Page (v2) {#page-component}

Le composant Page est un composant de page extensible conçu pour fonctionner avec l’[éditeur de modèles](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=fr) et permet l’assemblage de composants d’en-tête/de pied de page et de structure à l’aide de l’éditeur de modèles.

## Utilisation {#usage}

Le composant Page sert de base à toutes les pages conçues avec les composants principaux ainsi que les modèles modifiables. En utilisant le composant Page, les en-têtes, les pieds de page et la structure de la page peuvent être définis dans un modèle à l’aide des autres composants principaux.

Grâce à la [boîte de dialogue de conception](#design-dialog), les bibliothèques côté client personnalisées peuvent être définies pour la page. Contrairement aux autres composants dont la boîte de dialogue de modification est accessible directement à partir de ceux-ci, puisque le composant est la page elle-même, la [boîte de dialogue de modification](#edit-dialog) du composant de page est la fenêtre des propriétés de la page.

## Version et compatibilité {#version-and-compatibility}

Ce document décrit la version v2 du composant Page, introduite à l’origine avec la version 2.0.0 des composants principaux en janvier 2018.

>[!CAUTION]
>
>Ce document décrit la version v2 du composant Page.
>
>Pour plus d’informations sur la version actuelle du composant Page, voir le document [Composant Page](/help/components/page.md).

## Prise en charge des applications web progressives {#pwa-support}

La version 2.15.0 des composants principaux a introduit la prise en charge d’AEM as a Cloud Service de façon intégrée dans les fonctionnalités des [applications web progressives (PWA).](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/enable-pwa.html?lang=fr) Grâce à cette simple configuration au niveau du site, transformez votre expérience AEM en PWA !

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Page [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_page_v2_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation relative au développement des composants principaux](/help/developing/overview.md).

## Boîte de dialogue de modification {#edit-dialog}

Étant donné que le composant représente la page entière, les paramètres qui seraient normalement dans une boîte de dialogue de modification se trouvent dans la fenêtre [Propriétés de la page](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=fr).

### Prise en charge des données structurées {#structured-data}

La [version 2.31.0](/help/versions.md) des composants principaux a introduit la prise en charge des données structurées au niveau de la page (JSON-LD) des types [schema.org](https://schema.org) dans toutes les versions du composant de page.  AEM effectue le rendu de ces blocs côté serveur dans l’en-tête de la page.

La version [2026.6.0 d’AEM as a Cloud Service](https://experienceleague.adobe.com/fr/docs/experience-manager-release-information/aem-release-updates/update-releases-roadmap) permet désormais aux auteurs d’utiliser la fenêtre Propriétés de la page pour ajouter un ou plusieurs blocs JSON-LD à une page dans la section **SEO** de l’onglet **Avancé**.

## Boîte de dialogue de conception {#design-dialog}

Étant donné que le composant représente la page entière, la boîte de dialogue de conception est accessible via **Informations sur la page -> Politique de page** lors de la modification du modèle de page.

![Politique de page](/help/assets/page-policy.png)

>[!NOTE]
>
>Dans les versions précédentes d’AEM, la **Politique de page** était appelée **Conception de page**.

### Onglet Propriétés {#properties-tab}

À l’aide de la fenêtre Conception de page, vous pouvez définir les bibliothèques clientes à charger ainsi que la bibliothèque de ressources web pour la page.

* **Bibliothèques clientes** : cette option définit les catégories de bibliothèques clientes à charger. JavaScript est ajouté à la fin du corps et le CSS est ajouté à l’en-tête de la page.
* **En-tête de page JavaScript des bibliothèques clientes** : cette option définit les catégories de bibliothèques clientes JavaScript à charger dans l’en-tête de la page.
   * Les catégories définies ici et qui sont aussi présentes dans le champ **Bibliothèques clientes** ont le code JavaScript chargé dans l’en-tête de la page et non dans la fin du corps.
   * Aucun CSS ne sera chargé, sauf si la catégorie est également présente dans le champ **Bibliothèques clientes**.

* **Bibliothèque cliente des ressources web** : catégorie de bibliothèque cliente utilisée pour distribuer des ressources web telles que des favicons.

* **Passer au sélecteur d’élément de contenu principal** : utilisé comme fonction d’accessibilité pour passer directement au contenu principal de la page.

![Boîte de dialogue de conception du composant Page](/help/assets/page-design.png)

Les bibliothèques peuvent être configurées pour les champs **Bibliothèques clientes** et **En-tête de page JavaScript des bibliothèques clientes** de la manière suivante :

* Pour ajouter un nouveau champ, appuyez ou cliquez sur le bouton **Ajouter** sous les champs.
* Pour supprimer un champ, cliquez ou appuyez sur l’icône de corbeille à côté du champ à supprimer.
* Pour réorganiser l’ordre de chargement, cliquez ou appuyez et faites glisser la poignée à côté du champ à déplacer.

Pour plus d’informations sur l’utilisation des bibliothèques côté client, voir [Utilisation des bibliothèques côté client](https://helpx.adobe.com/fr/experience-manager/6-5/sites/developing/using/clientlibs.html).

>[!CAUTION]
>
>La possibilité de définir séparément les bibliothèques clientes pour l’en-tête de page a été introduite avec la version 2.2.0 des composants principaux.

### Onglet Styles {#styles-tab}

Le composant Page prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

## Couche de données client Adobe {#data-layer}

Le composant Page prend en charge la [couche de données client Adobe](/help/developing/data-layer/overview.md).
