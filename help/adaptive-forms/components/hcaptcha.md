---
title: hCaptcha dans les formulaires adaptatifs AEM
description: Améliorez sans effort la sécurité des formulaires grâce au service hCaptcha®. Guide détaillé inclus.
feature-set: Experience Manager Sites, Experience Manager Forms
feature: Adaptive Forms, Core Components
role: Architect, Developer, Admin, User
exl-id: eecb38d5-711e-4dc5-bc19-498e003f37e7
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Composant hCaptcha{#hCaptcha-component-adaptive-forms-core-component}

<span class="preview"> Cette fonctionnalité s’inscrit dans le cadre du programme d’adoption précoce. Vous pouvez écrire à aem-forms-ea@adobe.com à partir de votre adresse e-mail officielle pour rejoindre le programme d’adoption précoce et demander l’accès à la fonctionnalité. </span>

Le service hCaptcha® protège vos formulaires des robots, spams et violations automatisées. Il propose un test sous forme de widget de case à cocher et évalue la réponse de l’utilisateur ou de l’utilisatrice pour déterminer s’il s’agit d’une personne humaine ou d’un robot qui interagit avec le formulaire. Cela empêche l’utilisateur ou l’utilisatrice de continuer si le test échoue et permet de sécuriser les transactions en ligne en empêchant les robots d’envoyer du spam ou des activités malveillantes.

![hCaptcha®](/help/adaptive-forms/assets/hCaptcha-challenge.png)

{{traditional-aem}}

## Utilisation {#usage}

Il existe plusieurs raisons pour lesquelles il est intéressant d’inclure un test hCaptcha dans un processus d’envoi de formulaire. En voici quelques-unes :

- **Prévention des robots** : permet de s’assurer que le formulaire est envoyé par une personne humaine, ce qui réduit les spams et les envois automatisés.

- **Sécurité** : ajoute une couche supplémentaire de sécurité, en vérifiant la légitimité de chaque envoi de formulaire et en protégeant contre les attaques malveillantes.

- **Intégrité des données** : contribue à préserver l’intégrité et la précision des données collectées par le biais du formulaire, en empêchant les envois multiples ou frauduleux.

- **Vérification de l’utilisateur ou de l’utilisatrice** : vérifie l’identité de la personne qui envoie le formulaire, en veillant à ce que seules les personnes authentifiées puissent effectuer des transactions sensibles.

- **Gestion de la charge** : permet de gérer la charge du serveur en contrôlant le taux d’envoi des formulaires et empêcher ainsi la surcharge du système pendant les périodes de trafic élevé.

## Détails techniques {#technical-details}

Retrouvez les dernières informations sur le composant hCaptcha dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/hCaptcha/v1/hCaptcha/README.md). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

Spécifiez les propriétés du composant hCaptcha à l’aide de la [boîte de dialogue de configuration](#configure-dialog). La boîte de dialogue de configuration fait partie des composants principaux conçus pour faciliter la création des formulaires et fournir un moyen efficace de créer des formulaires complexes.

## Version et compatibilité {#version-and-compatibility}


Le composant Captcha du formulaire adaptatif a été publié en mai 2024 dans le cadre des [Composants principaux 3.0.20](https://github.com/adobe/aem-core-forms-components/commit/a4cb97131ffad47137a8f5f173401128a1cf3491). Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

|  |  |
|---|---|
| Version du composant | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatible avec la <br>[version 2.0.4](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible | Compatible |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser les propriétés de votre composant Captcha à l’aide de sa boîte de dialogue de configuration qui s’accompagne de l’onglet De base et de l’onglet Validation pour la personnalisation de différentes propriétés.

### Onglet De base {#basic-tab}

- **[!UICONTROL Nom] :** indiquez le nom de votre composant hCaptcha. Vous pouvez identifier facilement un composant de formulaire par son nom unique dans le formulaire et dans l’éditeur de règles.
- **[!UICONTROL Titre] :** indiquez le titre de votre composant hCaptcha.
- **[!UICONTROL Paramètres de configuration] :** sélectionnez une configuration de cloud configurée pour hCaptcha®.
- **Taille de Captcha :** vous pouvez sélectionner la taille d’affichage de la boîte de dialogue du test Captcha®. Utilisez l’option **[!UICONTROL Compact]** pour afficher une boîte de dialogue de test Captcha® de petite taille et l’option **[!UICONTROL Normal]** pour afficher une taille relativement grande.<!-- or **[!UICONTROL Invisible]** to validate hCaptcha&reg; without explicitly rendering the checkbox widget on the user interface. -->

  ![Onglet De base de hCaptcha](/help/adaptive-forms/assets/hcaptcha-basic.png)

### Onglet Validation {#validation-tab}

- **[!UICONTROL Message de validation] :** fournissez un message de validation pour votre validation Captcha lors de l’envoi du formulaire.
- **[!UICONTROL Message de validation de script]** : utilisez cette option pour saisir un message rapide en cas d’échec de la validation du script.

  ![Onglet Validation de hCaptcha](/help/adaptive-forms/assets/hcaptcha-validation-tab.png)

**hCaptcha® est une marque déposée d’Intuition Machines, Inc.**

**En savoir plus** sur d’autres **composants Captcha** et leurs services, tels que les suivants :

- [Utiliser hCaptcha dans un formulaire adaptatif pour les composants principaux](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/integrate-adaptive-forms-hcaptcha-core-components)

- [Utiliser hCaptcha dans un formulaire adaptatif pour les composants de base](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-hcaptcha)

- [Utiliser Turnstile CAPTCHA dans un formulaire adaptatif pour les composants de base](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile)

- [Utiliser Google reCAPTCHA dans un formulaire adaptatif pour les composants de base](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components)

## Articles connexes {#related-articles}

{{more-like-this}}

## Voir également {#see-also}

{{see-also}}
