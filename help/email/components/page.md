---
title: Composant de page de courriel
description: Composant Page de courrier électronique
role: Architect, Developer, Admin, User
exl-id: 17fd0f5e-2b85-41a1-abaf-8ad190a5341a
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 40%

---


# Composant de page de courriel {#email-page-component}

Le composant Page de courrier électronique est un composant de page extensible conçu pour fonctionner avec [éditeur de modèles](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=fr) et permet l’assemblage de composants d’en-tête/de pied de page et de structure à l’aide de l’éditeur de modèles, adaptés à la création de contenu Adobe Campaign.

## Utilisation {#usage}

Le composant de page de courrier électronique constitue la base de toutes les pages conçues avec les composants principaux du courrier électronique et les modèles modifiables. En utilisant le composant Page de messagerie, les en-têtes, les pieds de page et la structure de la page peuvent être définis comme un modèle à l’aide des autres composants principaux de messagerie.

* En utilisant la variable [boîte de dialogue de conception,](#design-dialog) des bibliothèques côté client personnalisées peuvent être définies pour la page.
* Contrairement à d’autres composants dont la boîte de dialogue de modification est accessible directement à partir du composant, puisque le composant de page de courrier électronique est la page elle-même, la variable [Modifier la boîte de dialogue](#edit-dialog) Le composant Page de courrier électronique contient la fenêtre des propriétés de page.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de page d’e-mail est v1, qui a été introduite avec la version X des composants principaux d’e-mail en octobre 2022. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatible | Compatible |

Pour plus d’informations sur les versions et versions des composants principaux d’email, consultez le document . [Courrier électronique des versions des composants principaux](/help/email/versions.md)

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Page [se trouve sur GitHub.](https://adobe.com/go/aem_cmp_tech_email_page_v1)

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de modification {#edit-dialog}

Étant donné que le composant représente la page entière, les paramètres qui seraient normalement dans une boîte de dialogue de modification se trouvent dans la fenêtre [Propriétés de la page](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=fr).

### Onglet Cloud Services {#cloud-services}

Pour que les composants principaux d’email puissent récupérer les données et les variables de campagne, la page doit être liée à une configuration Adobe Campaign.

![Propriétés de la page Email](/help/email/assets/email-page-properties.png)

Sous **Configuration du Cloud Service** en-tête, dans la liste déroulante **Ajouter une configuration**.

Sous **Adobe Campaign** , sélectionnez la configuration de votre intégration à Adobe Campaign.

Voir le document [Utilisation des composants principaux de messagerie](/help/email/using.md) pour plus d’informations sur la configuration des composants principaux de messagerie.

### Onglet Email {#email-tab}

L’onglet Email définit les propriétés des emails envoyés via Adobe Campaign en fonction du contenu de cette page, tel que l’objet de l’email et le contenu en texte brut.

![Propriétés de la page Email](/help/email/assets/email-page-properties-email.png)

* **Objet** - Objet de l’e-mail envoyé par Adobe Campaign sur la base de cette page
   * Cliquez sur le bouton **Sélectionner la variable Adobe Campaign** pour ouvrir la [Sélectionner la variable Adobe Campaign](/help/email/campaign-variables.md) pour insérer du contenu dynamique depuis Adobe Campaign.
* **Pre-header**
   * Cliquez sur le bouton **Sélectionner la variable Adobe Campaign** pour ouvrir la [Sélectionner la variable Adobe Campaign](/help/email/campaign-variables.md) pour insérer du contenu dynamique depuis Adobe Campaign.
* **Texte brut** - Version en texte brut de l’email envoyé par Adobe Campaign
   * Cliquez sur le bouton **Sélectionner la variable Adobe Campaign** pour ouvrir la [Sélectionner la variable Adobe Campaign](/help/email/campaign-variables.md) pour insérer du contenu dynamique depuis Adobe Campaign.
* **Url De Référence**

## Boîte de dialogue de conception {#design-dialog}

Étant donné que le composant représente la page entière, la boîte de dialogue de conception est accessible via **Informations sur la page -> Stratégie de page** lors de la modification du modèle de page.

![Stratégie de page](/help/assets/page-policy.png)

### Onglet Propriétés {#properties-tab}

À l’aide de la fenêtre Conception de page, vous pouvez définir les bibliothèques clientes à charger ainsi que la bibliothèque de ressources web pour la page.

![Boîte de dialogue de conception du composant Page de messagerie](/help/email/assets/email-page-design.png)

* **Bibliothèques clientes** : cette option définit les catégories de bibliothèques clientes à charger. JavaScript est ajouté à la fin du corps et le CSS est ajouté à l’en-tête de la page.
* **En-tête de page JavaScript des bibliothèques clientes** - Définit les catégories de bibliothèques clientes JavaScript à charger dans l’en-tête de la page.
   * Les catégories définies ici et qui sont aussi présentes dans le champ **Bibliothèques clientes** ont le code JavaScript chargé dans l’en-tête de la page et non dans la fin du corps.
   * Aucun CSS ne sera chargé, sauf si la catégorie est également présente dans le champ **Bibliothèques clientes**.
* **Chargement asynchrone des bibliothèques JavaScript** - Si cette option est activée, les bibliothèques JavaScript personnalisées sont chargées de manière asynchrone.
* **Bibliothèque cliente des ressources web** : catégorie de bibliothèque cliente utilisée pour distribuer des ressources web telles que des favicons.
* **Passer au sélecteur d’élément de contenu principal** : utilisé comme fonction d’accessibilité pour passer directement au contenu principal de la page.

Les bibliothèques peuvent être configurées pour les champs **Bibliothèques clientes** et **En-tête de page JavaScript des bibliothèques clientes** de la manière suivante :

* Pour ajouter un nouveau champ, cliquez ou appuyez sur le bouton **Ajouter** sous les champs.
* Pour supprimer un champ, cliquez ou appuyez sur l’icône de corbeille en regard du champ à supprimer.
* Pour réorganiser l’ordre de chargement, cliquez ou appuyez et faites glisser la poignée à côté du champ à déplacer.

Pour plus d’informations sur l’utilisation des bibliothèques côté client, voir [Utilisation des bibliothèques côté client.](https://helpx.adobe.com/fr/experience-manager/6-5/sites/developing/using/clientlibs.html)

### Onglet Styles {#styles-tab}

Le composant Page prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.
