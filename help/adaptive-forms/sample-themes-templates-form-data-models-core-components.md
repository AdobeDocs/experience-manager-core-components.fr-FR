---
title: Comment obtenir des exemples de thèmes et de modèles pour AEM Forms ?
description: Les composants principaux d’AEM Forms fournissent des exemples de thèmes, de modèles et de modèles de données de formulaire pour les formulaires adaptatifs.
solution: Experience Manager Forms
topic: Administration
role: Admin, User
hide: true
hidefromtoc: true
level: Intermediate
source-git-commit: ebbe3471164341076fe085bbef9c93fcb1fe382a
workflow-type: ht
source-wordcount: '1259'
ht-degree: 100%

---


# Exemples de thèmes, modèles et modèles de données de formulaire {#sample-themes-templates-and-data-models}

Les composants principaux [!DNL AEM Forms] fournissent des exemples de thèmes, de modèles et de modèles de données de formulaire prêts à l’emploi pour créer rapidement des formulaires adaptatifs polyvalents. Ils aident également les auteurs et autrices de formulaires à comprendre l’extensibilité, l’adaptabilité et la réactivité des [composants principaux d’AEM Forms](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=fr) pour créer facilement des formulaires simples en un rien de temps, ainsi que des formulaires complexes lors d’une connexion transparente à la base de données.

Les exemples de thèmes, modèles et modèles de données de formulaire inclus dans le package de contenu de référence sont les suivants :

| Modèles | Thèmes | Modèle de données de formulaire |
---------|----------|---------
| [De base](#Basic) | [Canevas](#Canvas) | Microsoft® Dynamics 365 |
| [Vide](#Blank) | [WKND](#WKND) | Salesforce |
| [Nous contacter](#Contact-Us) | [Chevalet](#Easel) |  |
| [Mise à jour des détails du contact](#Contact-Details-Update) |   |   |
| [Formulaire de consentement](#Consent-Form) | |  |
| [Consigner la demande de service](#Log-Service-Request) |  |  |
| [Envoyer des commentaires](#Give-Feedback) |  |  |
| [Souscription aux prestations](#Benefits-Enrollment) |  |   |
| [Résumé des prestations souscrites par les employé(e)s](#Employee-Benefits-Summary) |   |   |
| [Demande de relevé de compte](#Request-for-Account-Statement) |   |   |
| [Formulaire d’inspection de la sécurité](#Safety-Inspection) |   |   |
| [Inspection du contrôle qualité](#Quality-Control-Inspection) |   |   |
| [Demande d’achat](#Purchase-Request) |  |  |

## Exemples de thèmes {#Sample-Themes}

Les exemples de thèmes de référence aident les auteurs et autrices à définir et personnaliser le style des formulaires. Les personnes qui ne possèdent que de simples connaissances de base du code CSS peuvent aussi personnaliser le thème selon leurs besoins.

**Comment obtenir ces thèmes ?**
* Pour activer ces thèmes sur l’environnement **Forms as a Cloud Service**, [activez les composants principaux des formulaires adaptatifs](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html?lang=fr) et utilisez la fonction [pipeline front-end](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html?lang=fr) pour les déployer.
* Pour obtenir ces thèmes dans un environnement **AEM 6.5 Forms**, [activez les composants principaux de formulaires adaptatifs](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/enable-adaptive-forms-core-components.html?lang=fr) et utilisez le [gestionnaire de modules](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/create-or-customize-themes-for-adaptive-forms-core-components.?lang=fr) pour les déployer.

Les thèmes **prêts à l’emploi** des [composants principaux des formulaires adaptatifs](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=fr) sont les suivants :

![Thèmes prêts à l’emploi](/help/adaptive-forms/assets/OOTB-themes.png)

### Canevas {#Canvas}

Canevas est le thème par défaut des formulaires. Il souligne l’utilisation des couleurs de base, de la transparence et des icônes aplaties. Dans la capture d’écran ci-dessous, vous pouvez voir à quoi ressemble le thème Canevas.

![Thème Canevas](/help/adaptive-forms/assets/Safety-Inspection-Theme-Canvas.png)

### WKND {#WKND}

Le thème WKND incarne un design vivant, imaginatif et attrayant pour donner un aspect stylisé à vos formulaires. Le thème est basé sur l’aspect et le style du [site WKND](https://wknd.site/fr/fr.html), un site Web de voyage et d’aventures utilisant les [composants principaux d’Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=fr).

![Thème WKND](/help/adaptive-forms/assets/Safety-Inspection-Form-Theme.png)


### Chevalet {#Easel}

Le thème Chevalet permet de créer une apparence de formulaire attrayante et facile à configurer. Il est personnalisé pour plus de simplicité et de convivialité. Le thème Chevalet reprend le concept du support portable utilisé par les artistes pour poser leur toile pendant qu’ils travaillent.

![Thème Chevalet](/help/adaptive-forms/assets/Safety-Inspection-Theme-Easel.png)

## Exemples de modèles {#Sample-templates}

Les modèles définissent la structure, le contenu et les actions du formulaire initial à répliquer dans votre propre formulaire. Ils utilisent une structure de modèle similaire à votre formulaire, comme le formulaire de consentement, le formulaire de souscription aux prestations, et bien d’autres encore.

**Comment obtenir ces modèles ?**
Vous pouvez obtenir les modèles en déployant un [projet basé sur AEM Archetype 43 ou version ultérieure](https://github.com/adobe/aem-project-archetype) dans votre environnement de formulaires **AEM Forms as a Cloud Service** ou **AEM 6.5**.

Les modèles **prêts à l’emploi** des [composants principaux des formulaires adaptatifs](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=fr) sont les suivants :

![Modèles de référence](/help/adaptive-forms/assets/reference-templates-core-components.png)

### De base {#Basic}

Le modèle de base permet de créer rapidement un formulaire d’expérience. Vous pouvez également l’utiliser pour prévisualiser les fonctionnalités des [composants de base des formulaires adaptatifs](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=fr). Il fournit une disposition d’assistant pour la présentation section par section des données.

![Modèle de base](/help/adaptive-forms/assets/Basic-template-desktop-view.png)

### Vide {#Blank}

Le modèle Canevas vierge permet de créer entièrement une structure de formulaire adaptatif, avec du contenu et des règles. Aucun composant de formulaire n’est préincorporé dans le modèle vierge.

![Modèle vierge](/help/adaptive-forms/assets/Blank-temp-desktop-view.png)

### Nous contacter {#Contact-Us}

Le modèle de formulaire Nous contacter est utilisé pour créer un formulaire afin de faciliter la communication entre les personnes qui visitent le site Web et les personnes qui administrent des formulaires. Les personnes utilisatrices peuvent envoyer des requêtes, des commentaires ou des demandes d’assistance par le biais du formulaire.

![Modèle Nous contacter](/help/adaptive-forms/assets/Contact-us-desktop-view.png)

### Mise à jour des détails du contact {#Contact-Details-Update}

Le modèle Mise à jour des détails du contact aident les auteurs et autrices à créer un formulaire pour la mise à jour des informations d’adresse et de contact des clients et clientes. Ce formulaire aide également les clients et clientes à mettre à jour leurs informations personnelles relatives aux abonnements ou aux prestations, afin d’assurer une communication transparente et un accès ininterrompu à ces derniers.

![Contact-details-update](/help/adaptive-forms/assets/Contact-details-update.png)

### Formulaire de consentement {#Consent-Form}

Le modèle Formulaire de consentement permet de créer un formulaire d’obtention d’un document juridique auprès des personnes participant à une activité spécifique, une étude de recherche ou une procédure médicale, etc. Il concerne également les personnes dont les informations personnelles ou les droits sont impliqués. Ce formulaire garantit la transparence, protège les droits des personnes participantes et établit une compréhension claire de ce que la personne accepte.

![Formulaire de consentement](/help/adaptive-forms/assets/Consent-form-desktop-view.png)

### Demande de service de consignation {#Log-Service-Request}

Le modèle Demande de service de consignation permet de créer un formulaire qui demande des services de consignation spécifiques à un prestataire de services. Ce formulaire sert de demande formelle de création d’un ticket pour des événements, des activités ou des données enregistrées à des fins de surveillance ou de suivi de leur statut.

![Modèle Demande de service de consignation](/help/adaptive-forms/assets/Log-service-request-desktop-view.png)


### Envoyer des commentaires {#Give-Feedback}

Le modèle de formulaire Envoyer des commentaires permet de créer un formulaire fournissant des informations constructives à une autre personne ou équipe. Le formulaire permet de s’assurer que les commentaires sont clairs, spécifiques et exploitables, ce qui favorise une communication ouverte et l’amélioration des situations.

![Modèle Envoyer des commentaires](/help/adaptive-forms/assets/Give-feedback-desktop-view.png)


### Souscription aux prestations {#Benefits-Enrollment}

Le modèle de formulaire Souscription aux prestations sert à créer un formulaire recueillant des informations essentielles sur les prestations et les options de couverture préférées des employé(e)s. Il accompagne généralement la période de souscription annuelle aux prestations.

![Modèle Souscription aux prestations](/help/adaptive-forms/assets/Benefits-enrollment-form-template.png)


### Résumé des prestations souscrites par les employé(e)s {#Employee-Benefits-Summary}

Le modèle de formulaire Résumé des prestations souscrites par les employé(e)s permet de créer un formulaire afin de recueillir des détails essentiels sur les prestations souscrites par une personne. Il permet d’évaluer rapidement et précisément chaque couverture, offrant ainsi une vue d’ensemble complète pour une assistance et un soutien efficaces.
![Résumé des prestations souscrites par les employé(e)s](/help/adaptive-forms/assets/Employee-benefits-summary.png)


### Demande de relevé de compte {#Request-for-Account-Statement}

Le modèle Demande de relevé de compte permet de créer un formulaire qui initie le processus d’obtention d’un relevé de compte précis et actualisé. Le relevé fournit un enregistrement détaillé des transactions financières, des activités ou d’autres informations pertinentes concernant les client(e)s qui utilisent ce formulaire.

![Request-for-account-statment](/help/adaptive-forms/assets/Request-for-account-statment.png)

### Inspection de la sécurité {#Safety-Inspection}

Le modèle de formulaire Inspection de sécurité permet de créer un formulaire de saisie des détails pour un environnement de travail sécurisé. En procédant à des inspections régulières à partir de ce formulaire, les dangers potentiels peuvent être identifiés. Ce formulaire couvre divers aspects tels que les sorties de secours, la sécurité incendie, la sécurité électrique, les matières dangereuses, les équipements de protection personnelle, l’ergonomie du poste de travail pour la sécurité, ou encore le bien-être des employé(e)s, des visiteurs/visiteuses et des client(e)s.

![Formulaire d’inspection de la sécurité](/help/adaptive-forms/assets/Safety-inspection-form.png)

### Inspection du contrôle qualité {#Quality-Control-Inspection}

Le modèle de formulaire Inspection du contrôle qualité permet de créer un formulaire pour évaluer et faire état de l’aspect visuel, des dimensions, de la fonctionnalité, de la documentation, des résultats de test et de la qualité globale d’un produit ou d’un article. Il permet d’identifier les défauts, les non-conformités et les actions correctives nécessaires pour garantir le respect des normes de qualité.

![Inspection du contrôle qualité](/help/adaptive-forms/assets/Quality-Control-Inspection.png)


### Demande d’achat {#Purchase-Request}

Le modèle de formulaire Demande d’achat permet de créer un formulaire pour lancer la procédure d’achat et permettre aux employé(e)s de formellement demander l’achat de biens ou de services nécessaires à leur travail. Ce formulaire capture les détails essentiels tels que la description de l’article, la quantité, le fournisseur préféré (le cas échéant), l’allocation du budget, la justification de l’achat, les informations de diffusion et les validations requises.

![purchase-request-form](/help/adaptive-forms/assets/Purchase-request-form.png)

## Modèles de données de formulaire de référence {#reference-models}

Après avoir créé un formulaire adaptatif basé sur un [composant principal](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=fr), vous pouvez connecter votre formulaire à la base de données Microsoft® Dynamics 365 et aux serveurs Salesforce pour activer les workflows métier. Par exemple :

* Écrire des données sur Microsoft Dynamics 365 et Salesforce sur les envois de formulaires adaptatifs.
* Écrire des données dans Microsoft Dynamics 365 et Salesforce via des entités personnalisées définies dans le modèle de données de formulaire et vice versa.
* Demander des données aux serveurs Microsoft Dynamics 365 et Salesforce et préremplir des formulaires adaptatifs.
* Lire des données à partir des serveurs Microsoft Dynamics 365 et Salesforce.

Vous pouvez obtenir les modèles de données de formulaire suivants en installant le [package de contenu de référence](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-forms-reference-content.ui.content-2.1.0.zip) :

* Microsoft® Dynamics 365
* Salesforce

Pour plus d’informations sur l’utilisation de ces modèles, consultez [Configurer les services cloud Microsoft Dynamics 365 et Salesforce](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/configure-msdynamics-salesforce.html?lang=fr#configure-dynamics-cloud-service).
