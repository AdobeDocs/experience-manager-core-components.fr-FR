---
title: Composant Page (v2)
description: Le composant Page est un composant de page extensible, conçu pour fonctionner avec l’éditeur de modèles et autoriser l’assemblage de composants d’en-tête/de pied de page et de structure à l’aide de l’éditeur de modèles.
role: Architect, Developer, Admin, User
exl-id: e85fe4db-6de4-4a84-a54c-bd07a67efed3
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: ht
source-wordcount: '618'
ht-degree: 100%

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

La version 2.15.0 des composants principaux a introduit la prise en charge d’AEM as a Cloud Service de façon intégrée dans les fonctionnalités des [applications web progressives (PWA).](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/enable-pwa.html?lang=fr) Grâce à cette simple configuration au niveau du site, transformez votre expérience AEM en PWA !

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Page [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_page_v2_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de modification {#edit-dialog}

Étant donné que le composant représente la page entière, les paramètres qui seraient normalement dans une boîte de dialogue de modification se trouvent dans la fenêtre [Propriétés de la page](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=fr).

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
