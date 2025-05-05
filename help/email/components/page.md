---
title: Composant Page d’e-mail
description: Composant Page d’e-mail
role: Architect, Developer, Admin, User
exl-id: 17fd0f5e-2b85-41a1-abaf-8ad190a5341a
source-git-commit: 91969e4956bef1a511b8d588d5290a7999bf86ec
workflow-type: ht
source-wordcount: '780'
ht-degree: 100%

---


# Composant Page d’e-mail {#email-page-component}

Le composant Page d’e-mail est un composant de page extensible conçu pour fonctionner avec l’[éditeur de modèles](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=fr). Il permet d’assembler des composants d’en-tête/de pied de page et de structure avec l’éditeur de modèles, le tout adapté à la création de contenu Adobe Campaign.

## Utilisation {#usage}

Le composant Page d’e-mail constitute la base de toutes les pages conçues avec les composants principaux d’e-mail ainsi que les modèles modifiables. Grâce au composant Page d’e-mail, les en-têtes, les pieds de page et la structure de la page peuvent être définis dans un modèle à l’aide des autres composants principaux d’e-mail.

* Grâce à la [boîte de dialogue de conception](#design-dialog), les bibliothèques côté client personnalisées peuvent être définies pour la page.
* Contrairement aux autres composants dont la boîte de dialogue de modification est accessible directement à partir de ceux-ci, puisque le composant Page d’e-mail est la page elle-même, la [boîte de dialogue de modification](#edit-dialog) du composant Page d’e-mail est la fenêtre Propriétés de la page.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Page d’e-mail est v1. Celle-ci a été introduite avec la version X des composants principaux d’e-mail en octobre 2022. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatible | - | - |

Pour plus d’informations sur les versions et les publications des composants principaux d’e-mail, voir le document sur les [versions des composants principaux d’e-mail](/help/email/versions.md).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Page [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_email_page_v1).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de modification {#edit-dialog}

Étant donné que le composant représente la page entière, les paramètres qui seraient normalement dans une boîte de dialogue de modification se trouvent dans la fenêtre [Propriétés de la page](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=fr).

### Onglet Services cloud {#cloud-services}

Afin que les composants principaux d’e-mail puissent récupérer les données et les variables de campagne, la page doit être liée à une configuration Adobe Campaign.

![Propriétés de la page d’e-mail](/help/email/assets/email-page-properties.png)

Sous l’en-tête **Configuration du service Cloud**, dans la liste déroulante, sélectionnez **Ajouter la configuration**.

Sous l’en-tête **Adobe Campaign**, sélectionnez la configuration de votre intégration à Adobe Campaign.

Pour plus d’informations sur la configuration des composants principaux d’e-mail, voir le document [Utilisation des composants principaux d’e-mail](/help/email/using.md).

### Onglet E-mail {#email-tab}

L’onglet E-mail définit les propriétés des e-mails envoyés via Adobe Campaign en fonction du contenu de cette page, tel que l’objet du message et le contenu en texte brut.

![Propriétés de la page d’e-mail](/help/email/assets/email-page-properties-email.png)

* **Objet** : objet de l’e-mail envoyé par Adobe Campaign sur la base de cette page.
   * Cliquez sur l’icône **Sélectionner la variable Adobe Campaign** pour ouvrir la boîte de dialogue [Sélectionner la variable Adobe Campaign](/help/email/campaign-variables.md) et insérer du contenu dynamique depuis Adobe Campaign.
* **Pré-en-tête**
   * Cliquez sur l’icône **Sélectionner la variable Adobe Campaign** pour ouvrir la boîte de dialogue [Sélectionner la variable Adobe Campaign](/help/email/campaign-variables.md) et insérer du contenu dynamique depuis Adobe Campaign.
* **Texte brut** : la version en texte brut de l’e-mail envoyé par Adobe Campaign.
   * Cliquez sur l’icône **Sélectionner la variable Adobe Campaign** pour ouvrir la boîte de dialogue [Sélectionner la variable Adobe Campaign](/help/email/campaign-variables.md) et insérer du contenu dynamique depuis Adobe Campaign.
* **URL de référence**

## Boîte de dialogue de conception {#design-dialog}

Étant donné que le composant représente la page entière, la boîte de dialogue de conception est accessible via **Informations sur la page -> Politique de page** lors de la modification du modèle de page.

![Politique de page](/help/assets/page-policy.png)

### Onglet Propriétés {#properties-tab}

À l’aide de la fenêtre Conception de page, vous pouvez définir les bibliothèques clientes à charger ainsi que la bibliothèque de ressources web pour la page.

![Boîte de dialogue de conception du composant Page d’e-mail](/help/email/assets/email-page-design.png)

* **Bibliothèques clientes** : cette option définit les catégories de bibliothèques clientes à charger. JavaScript est ajouté à la fin du corps et le CSS est ajouté à l’en-tête de la page.
* **En-tête de page JavaScript des bibliothèques clientes** : cette option définit les catégories de bibliothèques clientes JavaScript à charger dans l’en-tête de la page.
   * Les catégories définies ici et qui sont aussi présentes dans le champ **Bibliothèques clientes** ont le code JavaScript chargé dans l’en-tête de la page et non dans la fin du corps.
   * Aucun CSS ne sera chargé, sauf si la catégorie est également présente dans le champ **Bibliothèques clientes**.
* **Chargement asynchrone des bibliothèques JavaScript** : si cette option est activée, les bibliothèques JavaScript personnalisées sont chargées de manière asynchrone.
* **Bibliothèque cliente des ressources web** : catégorie de bibliothèque cliente utilisée pour distribuer des ressources web telles que des favicons.
* **Passer au sélecteur d’élément de contenu principal** : utilisé comme fonction d’accessibilité pour passer directement au contenu principal de la page.

Les bibliothèques peuvent être configurées pour les champs **Bibliothèques clientes** et **En-tête de page JavaScript des bibliothèques clientes** de la manière suivante :

* Pour ajouter un nouveau champ, appuyez ou cliquez sur le bouton **Ajouter** sous les champs.
* Pour supprimer un champ, appuyez ou cliquez sur l’icône de corbeille située en regard du champ à supprimer.
* Pour réorganiser l’ordre de chargement, cliquez ou appuyez sur la poignée située en regard du champ à déplacer et faites-la glisser.

Pour plus d’informations sur l’utilisation des bibliothèques côté client, voir [Utilisation de bibliothèques côté client](https://helpx.adobe.com/fr/experience-manager/6-5/sites/developing/using/clientlibs.html).

### Onglet Styles {#styles-tab}

Le composant Page prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.
