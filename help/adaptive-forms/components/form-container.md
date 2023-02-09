---
title: Composant principal Forms adaptatif - Conteneur de formulaires
description: Ajouter un formulaire adaptatif à une page web.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 3%

---


# Conteneur de formulaires {#form-container-adaptive-forms-core-component}

Forms permet aux visiteurs du site web d’interagir avec le site en fournissant des informations précieuses, ce qui peut augmenter l’engagement et la satisfaction des utilisateurs. Un conteneur de formulaires adaptatifs dans Adobe Experience Manager (AEM) Sites permet aux propriétaires de sites web d’ajouter facilement des formulaires à leurs pages. Cela facilite la communication entre les visiteurs du site web et le propriétaire ou l’organisation du site web en permettant aux visiteurs de fournir des commentaires, de répondre à des questions et de terminer d’autres actions de manière simplifiée.

## Utilisation {#reasons-to-use-forms-container}

Plusieurs raisons peuvent expliquer l’ajout d’un formulaire à un site web :

* **Collecte de données**: Forms peut être utilisé pour collecter des données auprès des visiteurs de sites web à diverses fins, telles que des recherches sur le marché, une analyse du comportement des utilisateurs, etc.

* **Génération de pistes**: Un formulaire peut être utilisé pour recueillir des informations auprès de clients potentiels, tels que le nom et l’adresse électronique, afin de générer des pistes pour les efforts de vente et de marketing.

* **Commerce électronique**: Forms peut être utilisé pour les achats en ligne, ce qui permet aux clients de passer des commandes et d’effectuer des paiements sur le site web.

* **Contact**: Un formulaire de contact permet aux visiteurs du site Web d’accéder facilement au propriétaire ou à l’organisation du site Web.

* **Questionnaires et sondages**: Forms peut être utilisé pour recueillir les commentaires et les opinions des visiteurs du site par le biais d&#39;enquêtes et de sondages.

* **Enregistrement d’événement**: Forms peut être utilisé pour l’enregistrement des événements, ce qui permet aux visiteurs du site web de s’inscrire à des événements ou à des webinaires.

* **Abonnements**: Forms peut être utilisé pour les abonnements à des sites web, ce qui permet aux visiteurs de s’inscrire à une newsletter ou à d’autres communications régulières.

* **Authentification de l’utilisateur**: Forms peut être utilisé pour l’authentification des utilisateurs, ce qui permet aux visiteurs du site web de créer des comptes et de se connecter pour accéder à du contenu ou à des fonctionnalités exclusifs.

* **Augmentation du taux de conversion**: Un formulaire bien conçu peut augmenter le taux de conversion en facilitant la réalisation de l’action souhaitée par les utilisateurs, comme l’achat d’un produit ou l’inscription à un service.


## Version et compatibilité {#version-and-compatibility}

Le composant principal de conteneur de Forms adaptatif a été publié en février 2023 dans le cadre des composants principaux 2.0.4. Voici un tableau présentant toutes les versions prises en charge, la compatibilité AEM et les liens vers la documentation correspondante :

|  |  |
|---|---|
| Version du composant | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatible avec<br>[version 2.0.4](/help/versions.md) et plus tard | Compatible | Compatible |

Pour plus d’informations sur les versions et versions des composants principaux, reportez-vous à la section [Versions des composants principaux](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Obtenez les dernières informations sur le composant principal de conteneur de Forms adaptatif dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container). Pour plus d’informations sur le développement des composants principaux, consultez la section [Documentation destinée aux développeurs sur les composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser votre expérience de conteneur de formulaires pour les visiteurs qui utilisent la boîte de dialogue Configurer . Vous pouvez également définir facilement des options de conteneur de formulaires pour une expérience utilisateur transparente.

### Onglet De base {#basic-tab}

![Onglet Simple](/help/adaptive-forms/assets/formcontainer_basictab.png)

* **Services de préremplissage** - Cette option permet à l’utilisateur de sélectionner un service de préremplissage pour récupérer les données lors de la génération du formulaire adaptatif. En savoir plus sur [comment créer et configurer un service de préremplissage](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=en#aem-forms-custom-prefill-service).

* **Catégorie de bibliothèque cliente** - L’utilisateur peut configurer une bibliothèque JavaScript personnalisée par formulaire adaptatif. Il est recommandé de ne conserver que les fonctions réutilisables de la bibliothèque, qui dépendent des bibliothèques tierces jquery et underscore.js.

### Onglet Envoi {#submission-tab}

![Onglet Envoi](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

Les utilisateurs peuvent configurer différentes actions pour les envois de formulaire adaptatif.

* **URL/chemin de redirection** - Cette option permet à l’utilisateur de configurer une page pour chaque formulaire, vers laquelle les utilisateurs du formulaire sont redirigés après l’envoi d’un formulaire adaptatif. Cliquez ici pour plus d’informations sur [configuration des pages de redirection](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html).

![Afficher le message, onglet](/help/adaptive-forms/assets/formconatiner_showmessage.png)

* **Afficher le message** - Cette option permet aux utilisateurs d’ajouter un message qui s’affiche lorsque le formulaire adaptatif est envoyé avec succès. Le texte prédéfini est inclus dans la boîte de dialogue et peut être modifié par l’utilisateur. La boîte de dialogue Afficher le message prend en charge les outils de mise en forme de texte enrichi qui permettent aux utilisateurs de mettre en forme le texte ajouté.

* **Action Envoyer** - Une action Envoyer est déclenchée lorsqu’un utilisateur clique sur le bouton Envoyer d’un formulaire adaptatif. Les utilisateurs peuvent sélectionner Actions Envoyer dans la liste déroulante qui sont prises en charge par défaut. Découvrez comment [configuration d’une action Envoyer dans l’onglet Envoi](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#supporting-custom-functions-in-validation-expressions-br).




