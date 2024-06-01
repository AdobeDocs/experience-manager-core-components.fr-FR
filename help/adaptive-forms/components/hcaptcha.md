---
title: Captcha dans AEM Forms adaptatif
description: Améliorez la sécurité des formulaires grâce à Captcha&reg ; sans effort. Guide pas à pas à l'intérieur !
feature-set: Experience Manager Sites, Experience Manager Forms
feature: Adaptive Forms, Core Components
role: Architect, Developer, Admin, User
source-git-commit: ddfd55259f84443e6add3ced09fd319bcd9c1677
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 12%

---

# Composant Captcha{#hCaptcha-component-adaptive-forms-core-component}

<span class="preview"> Cette fonctionnalité s’inscrit dans le cadre du Programme des Adopteurs Anticipés. Vous pouvez écrire à aem-forms-ea@adobe.com à partir de votre ID de courrier électronique officiel pour rejoindre le programme des premiers adopteurs et demander l’accès à la fonctionnalité. </span>

Le service Captcha® protège vos formulaires contre les robots, les spams et les abus automatisés. Il pose un problème de widget de case à cocher et évalue la réponse de l’utilisateur pour déterminer s’il s’agit d’un humain ou d’un robot interagissant avec le formulaire. Elle empêche l’utilisateur de procéder si le test échoue et permet de sécuriser les transactions en ligne en empêchant les robots de publier du spam ou des activités malveillantes.

![Captcha®](/help/adaptive-forms/assets/hCaptcha-challenge.png)

## Utilisation {#usage}

Il existe plusieurs raisons pour lesquelles il est bénéfique d’inclure un défi de tcha dans un processus d’envoi de formulaire, à savoir :

- **Prévention des robots**: permet de s’assurer que le formulaire est envoyé par un humain, ce qui réduit les spams et les envois automatisés.

- **Sécurité**: ajoute une couche supplémentaire de sécurité, en vérifiant la légitimité de chaque envoi de formulaire et en protégeant contre les attaques malveillantes.

- **Intégrité des données**: en empêchant les envois multiples ou frauduleux, il contribue à préserver l’intégrité et la précision des données collectées par le biais du formulaire.

- **Vérification de l’utilisateur**: vérifie l’identité de l’utilisateur qui envoie le formulaire, en veillant à ce que seuls les utilisateurs authentifiés puissent effectuer des transactions sensibles.

- **Chargement de la gestion**: permet de gérer la charge du serveur en contrôlant le taux d’envoi des formulaires, empêchant la surcharge du système pendant les périodes à trafic élevé.

## Détails techniques {#technical-details}

Obtenez les dernières informations sur le composant Captcha dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/hCaptcha/v1/hCaptcha/README.md). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

Spécifiez les propriétés du composant Captcha à l’aide du [boîte de dialogue de configuration](#configure-dialog). La boîte de dialogue de configuration fait partie des composants principaux conçus pour faciliter la création des formulaires et offrir un moyen efficace de créer des formulaires complexes.

## Version et compatibilité {#version-and-compatibility}


Le composant Captcha de Forms adaptatif a été publié en mai 2024 dans le cadre du [Composants principaux 3.0.20](https://github.com/adobe/aem-core-forms-components/commit/a4cb97131ffad47137a8f5f173401128a1cf3491). Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

|  |  |
|---|---|
| Version du composant | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatible avec la <br>[version 2.0.4](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible | Compatible |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser les propriétés de votre composant Captcha à l’aide de sa boîte de dialogue Configurer qui s’accompagne de l’onglet Simple et de l’onglet Validation pour personnaliser différentes propriétés.

### Onglet De base {#basic-tab}

- **[!UICONTROL Nom]:** Indiquez le nom de votre composant Captcha. Vous pouvez identifier facilement un composant de formulaire avec son nom unique dans le formulaire et dans l’éditeur de règles.
- **[!UICONTROL Titre]:** Indiquez le titre de votre composant Captcha.
- **[!UICONTROL Paramètres de configuration]:** Sélectionnez une configuration de cloud configurée pour Captcha®.
- **Taille du captcha :** Vous pouvez sélectionner la taille d&#39;affichage de la boîte de dialogue de défi Captcha®. Utilisez la variable **[!UICONTROL Compact]** pour afficher une petite taille et la variable **[!UICONTROL Normal]** pour afficher une boîte de dialogue de défi Captcha® de taille relativement grande.<!-- or **[!UICONTROL Invisible]** to validate hCaptcha&reg; without explicitly rendering the checkbox widget on the user interface. -->

  ![Onglet Captcha de base](/help/adaptive-forms/assets/hcaptcha-basic.png)

### Onglet Validation {#validation-tab}

- **[!UICONTROL Message de validation]:** Fournissez un message de validation pour votre validation Captcha lors de l’envoi du formulaire.
- **[!UICONTROL Message de validation de script]** - Utilisez cette option pour saisir un message rapide en cas d’échec de la validation du script.

  ![Onglet Validation de captcha](/help/adaptive-forms/assets/hcaptcha-validation-tab.png)

**Captcha® est une marque déposée de Intuition Machines, Inc.**

**En savoir plus** about **Composants Captcha** et leurs services, tels que :

- [Utilisation du captcha dans un formulaire adaptatif pour les composants principaux](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/integrate-adaptive-forms-hCaptcha-core-components)

- [Utilisation du captcha dans un formulaire adaptatif pour les composants de base](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-hcaptcha)

- [Utilisation de Turnstile CAPTCHA dans un formulaire adaptatif pour les composants de base](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile)

- [Utilisation de Google reCAPTCHA dans un formulaire adaptatif pour les composants de base](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components)

## Articles connexes {#related-articles}

{{more-like-this}}

## Voir également {#see-also}

{{see-also}}
