---
title: Composant principal de formulaires adaptatifs - Conteneur de formulaires
description: Ajoutez un formulaire adaptatif à une page Web.
role: Architect, Developer, Admin, User
exl-id: 8df7f862-4d59-4c3f-88dd-f0c937081f4f
source-git-commit: ad3e3bca5cb46f14e864e4704c90ac3b62779794
workflow-type: ht
source-wordcount: '791'
ht-degree: 100%

---

# Conteneur de formulaires {#form-container-adaptive-forms-core-component}

Les formulaires permettent aux visiteurs et aux visiteuses d’un site Web d’interagir avec ce site en fournissant des informations précieuses, ce qui peut augmenter l’engagement et la satisfaction des utilisateurs et des utilisatrices. Un conteneur de formulaires adaptatifs dans Adobe Experience Manager (AEM) Sites permet aux propriétaires de sites Web d’ajouter facilement des formulaires à leurs pages. Cela facilite la communication entre les visiteurs et les visiteuses du site Web et le/la propriétaire ou l’organisation du site Web en permettant aux visiteurs et aux visiteuses de fournir des commentaires, de répondre à des questions et de terminer d’autres actions de manière simplifiée.

## Utilisation {#reasons-to-use-forms-container}

Plusieurs raisons peuvent expliquer l’ajout d’un formulaire à un site Web :

* **Collecte de données** : les formulaires peuvent être utilisés pour collecter des données auprès des visiteurs et visiteuses de sites Web à diverses fins, telles que des recherches sur le marché, une analyse du comportement des utilisateurs et des utilisatrices, etc.

* **Génération de piste** : un formulaire peut être utilisé pour recueillir des informations auprès de clients et clientes potentiels, tels que le nom et l’adresse électronique, afin de générer des pistes pour les efforts de vente et de marketing.

* **E-commerce** : les formulaires peuvent être utilisés pour les achats en ligne, ce qui permet aux clients et clientes de passer des commandes et d’effectuer des paiements sur le site Web.

* **Contact** : un formulaire de contact permet aux visiteurs et visiteuses du site Web d’accéder facilement au propriétaire ou à l’organisation du site Web.

* **Questionnaires et sondages** : les formulaires peuvent être utilisés pour recueillir les commentaires et les opinions des visiteurs et visiteuses du site par le biais d’enquêtes et de sondages.

* **Enregistrement d’événements** : les formulaires peuvent être utilisés pour l’enregistrement d’événements, ce qui permet aux visiteurs et visiteuses du site Web de s’inscrire à des événements ou à des webinaires.

* **Abonnements** : les formulaires peuvent être utilisés pour les abonnements à des sites Web, ce qui permet aux visiteurs et aux visiteuses de s’abonner à une newsletter ou à d’autres communications régulières.

* **Authentification de l’utilisateur** : les formulaires peuvent être utilisés pour l’authentification des utilisateurs et des utilisatrices, ce qui permet aux visiteurs et aux visiteuses du site Web de créer des comptes et de se connecter pour accéder à du contenu ou à des fonctionnalités exclusifs.

* **Augmentation du taux de conversion** : un formulaire bien conçu peut augmenter le taux de conversion en facilitant la réalisation de l’action souhaitée par les utilisateurs et les utilisatrices, comme l’achat d’un produit ou l’inscription à un service.


## Version et compatibilité {#version-and-compatibility}

Le composant principal Accordéon des formulaires adaptatifs a été publié en février 2023 au sein des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec la <br>[version 2.0.4](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible avec les<br>[versions 1.1.12](/help/adaptive-forms/version.md) à 2.0.0 exclue. |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).
<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Obtenez les dernières informations sur le composant principal de conteneur des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser votre expérience de conteneur de formulaires pour les visiteurs et les visiteuses avec la boîte de dialogue de configuration. Vous pouvez également définir facilement des options de conteneur de formulaires pour une expérience utilisateur transparente.

### Onglet De base {#basic-tab}

![Onglet De base](/help/adaptive-forms/assets/formcontainer_basictab.png)

* **Services de préremplissage** : cette option permet à l’utilisateur ou à l’utilisatrice de sélectionner un service de préremplissage pour récupérer les données lors de la génération du formulaire adaptatif. En savoir plus sur [comment créer et configurer un service de préremplissage](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=fr#aem-forms-custom-prefill-service).

* **Catégorie de bibliothèque cliente** - L’utilisateur ou l’utilisatrice peut configurer une bibliothèque JavaScript personnalisée par formulaire adaptatif. Il est recommandé de ne conserver que les fonctions réutilisables de la bibliothèque, qui dépendent des bibliothèques tierces jquery et underscore.js.

### Onglet Envoi {#submission-tab}

![Onglet Envoi](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

Les utilisateurs et les utilisatrices peuvent configurer différentes actions pour les envois de formulaires adaptatifs.

* **URL/chemin de redirection** - Cette option permet à l’utilisateur ou à l’utilisatrice de configurer une page pour chaque formulaire, vers laquelle les utilisateurs et utilisatrices du formulaire sont redirigés après l’envoi d’un formulaire adaptatif. Cliquez ici pour plus d’informations sur [la façon de configurer des pages de redirection](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html?lang=fr).

![Onglet Afficher le message](/help/adaptive-forms/assets/formconatiner_showmessage.png)

* **Afficher le message** - Cette option permet aux utilisateurs et utilisatrices d’ajouter un message qui s’affiche lorsque le formulaire adaptatif est envoyé avec succès. Le texte prédéfini est inclus dans la boîte de dialogue et peut être modifié par l’utilisateur ou l’utilisatrice. La boîte de dialogue Afficher le message prend en charge les outils de mise en forme de texte enrichi qui permettent aux utilisateurs et aux utilisatrices de mettre en forme le texte ajouté.

* **Action Envoyer** - Une action Envoyer est déclenchée lorsqu’un utilisateur ou une utilisatrice clique sur le bouton Envoyer d’un formulaire adaptatif. Les utilisateurs et les utilisatrices peuvent sélectionner les actions Envoyer dans la liste déroulante qui sont prises en charge par défaut. Découvrir comment [configurer une action Envoyer dans l’onglet Envoi](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html?lang=fr#supporting-custom-functions-in-validation-expressions-br).

## Article connexe {#related-article}

* [Création d’un formulaire adaptatif dans une page AEM Sites ou un fragment d’expérience](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=fr)

* [Création d’un formulaire adaptatif autonome](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=fr)


## Voir également {#see-also}

* [Accordéon](/help/adaptive-forms/components/accordion.md)
* [Bouton](/help/adaptive-forms/components/button.md)
* [Case à cocher Groupe](/help/adaptive-forms/components/checkbox-group.md)
* [Sélecteur de date](/help/adaptive-forms/components/date-picker.md)
* [Liste déroulante](/help/adaptive-forms/components/drop-down.md)
* [Entrée d’e-mail](/help/adaptive-forms/components/email-input.md)
* [Pièce jointe](/help/adaptive-forms/components/file-attachment.md)
* [Pied de page](/help/adaptive-forms/components/footer.md)
* [En-tête](/help/adaptive-forms/components/header.md)
* [Onglets horizontaux](/help/adaptive-forms/components/horizontal-tabs.md)
* [Image](/help/adaptive-forms/components/image.md)
* [Entrée de nombre](/help/adaptive-forms/components/number-input.md)
* [Conteneur de panneau](/help/adaptive-forms/components/panel-container.md)
* [Bouton radio](/help/adaptive-forms/components/radio-button.md)
* [Bouton de réinitialisation](/help/adaptive-forms/components/reset-button.md)
* [Bouton Envoyer](/help/adaptive-forms/components/submit-button.md)
* [Entrée téléphonique](/help/adaptive-forms/components/telephone-input.md)
* [Entrée de texte](/help/adaptive-forms/components/text-input.md)
* [Texte](/help/adaptive-forms/components/text.md)
* [Titre](/help/adaptive-forms/components/title.md)
* [Assistant](/help/adaptive-forms/components/wizard.md)