---
title: Composant principal de formulaires adaptatifs - Conteneur de formulaires
description: Ajoutez un formulaire adaptatif à une page Web.
role: Architect, Developer, Admin, User
hide: true
hidefromtoc: true
exl-id: 1e413ef3-7a6f-41fc-825d-dbe09ebaffe9
source-git-commit: 37ac7d3a9ae8c88d4c9be8129cfbd1eb4a7cccd1
workflow-type: tm+mt
source-wordcount: '1048'
ht-degree: 73%

---

# Google reCAPTCHA {#google-recaptcha}

CAPTCHA (Completely Automated Public Turing test to tell Computers and Humans Apart, Test public de Turing complètement automatisé ayant pour but de différencier les personnes humaines des ordinateurs) est un programme couramment utilisé dans les transactions en ligne pour différencier les personnes humaines des programmes automatisés ou des robots. Il présente un test et évalue la réponse de l’utilisateur ou de l’utilisatrice pour déterminer s’il s’agit d’une personne humaine ou d’un robot qui interagit avec le site. Cela empêche l’utilisateur ou l’utilisatrice de continuer si le test échoue et permet de sécuriser les transactions en ligne en empêchant les robots d’envoyer du spam ou des éléments malveillants.

AEM Forms as a Cloud Service prend en charge Google reCAPTCHA v2 dans les formulaires adaptatifs. Vous pouvez l’utiliser pour présenter un défi Captcha lors de l’envoi du formulaire.

## Utilisation {#reasons-to-use-google-recaptcha}


- **Prévention contre le spam et les robots** : l’une des principales raisons d’utiliser reCAPTCHA est d’empêcher les envois de spam et l’afflux de robots malveillants dans votre formulaire. Les algorithmes avancés de reCAPTCHA peuvent détecter les tentatives automatisées d’envoi du formulaire, assurant ainsi que seuls les utilisateurs et utilisatrices légitimes peuvent interagir avec celui-ci.

- **Sécurité renforcée** : en implémentant reCAPTCHA, vous ajoutez une couche supplémentaire de sécurité à votre formulaire adaptatif. Cela permet de protéger les informations sensibles et d’empêcher les utilisateurs et utilisatrices malveillants d’exploiter les vulnérabilités.

- **Expérience client** : bien que les Captcha puissent parfois être considérés comme un inconvénient, l’approche adaptative de reCAPTCHA signifie que la plupart des utilisateurs et utilisatrices se voient présenter une expérience rationalisée et conviviale qui nécessite une interaction minimale. Cela peut aider à maintenir une expérience client positive tout en dissuadant les robots.

- **Adaptabilité** : le mécanisme adaptatif de reCAPTCHA analyse le comportement et les interactions des utilisateurs et utilisatrices pour déterminer s’ils sont humains ou non. Cela signifie que le niveau de défi présenté à la personne utilisatrice peut varier en fonction de la probabilité qu’elle soit un robot. Cette adaptabilité réduit la friction pour les utilisateurs et utilisatrices authentiques tout en maintenant une sécurité renforcée.

- **Modération manuelle réduite** : en réduisant de manière significative le nombre d’envois de spam et le contenu généré par les robots, reCAPTCHA peut faire économiser du temps et des ressources qui seraient autrement utilisés pour la modération manuelle et le nettoyage.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Google reCAPTCHA du formulaire adaptatif a été publié en août 2023 dans le cadre de la « version » des composants principaux. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

|  |  |
|---|---|
| Version du composant | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatible avec la <br>[version 2.0.4](/help/versions.md) et les versions ultérieures | Compatible | Compatible |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/versions.md).

## Détails techniques {#technical-details}

Retrouvez les informations les plus récentes sur le composant principal Google reCAPTCHA des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/recaptcha/v1/recaptcha). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser votre expérience Google reCAPTCHA pour les visiteurs et les visiteuses à l’aide de la boîte de dialogue de configuration. Vous pouvez également définir facilement des options de Google reCAPTCHA pour une expérience client fluide.

### Onglet De base {#basic-tab}

- **Nom** - Vous pouvez identifier facilement un composant de formulaire en lui attribuant un nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

- **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

- **Masquer le titre** - Sélectionnez cette option pour masquer le titre du composant.

- **Configuration** -

- **Type** -

- **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.

- **Désactiver le composant** - Sélectionnez cette option pour désactiver le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. Les données du composant désactivé ne sont pas envoyées. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

- **Lecture seule** - Sélectionnez cette option pour rendre le composant non modifiable. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

### Onglet Validation {#validation-tab}

- **Message d’erreur** : cette option vous permet de saisir un message qui s’affiche si la case à cocher **Obligatoire** est cochée et que le champ de formulaire reste vide.

## Voir également {#see-also}

- [Création d’un formulaire adaptatif AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=fr)
- [Ajout d’un formulaire adaptatif AEM à une page AEM Sites](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html)
- [Application de thèmes à un formulaire adaptatif AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html?lang=fr)
- [Ajout de composants à un formulaire adaptatif AEM](/help/adaptive-forms/introduction.md#adaptive-forms-core-components-components)
- [Utiliser reCAPTCHA dans un formulaire adaptatif AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/captcha-adaptive-forms.html)
- [Générer une version de PDF (DE) d’un formulaire adaptatif AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/generate-document-of-record-core-components.html)
- [Traduire un formulaire adaptatif AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-aem-translation-workflow-to-localize-adaptive-forms-core-components.html)
- [Activation d’Adobe Analytics pour un formulaire adaptatif pour effectuer le suivi de l’utilisation des formulaires](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/integrate/services/enable-adobe-analytics-adaptive-form-using-experience-cloud-setup-automation.html)
- [Connexion d’un formulaire adaptatif à Microsoft SharePoint](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#create-sharepoint-configuration)
- [Connexion d’un formulaire adaptatif à Microsoft Power Automate](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#microsoft-power-automate)
- [Connexion d’un formulaire adaptatif à Microsoft OneDrive](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#submit-to-onedrive)
- [Connexion d’un formulaire adaptatif au stockage Azure Blob de Microsoft](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#submit-to-azure-blob-storage)
- [Connexion d’un formulaire adaptatif à Salesforce](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/oauth2-client-credentials-flow-for-server-to-server-integration.html)
- [Utilisation d’Adobe Sign dans un formulaire adaptatif AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/use-adobe-sign/working-with-adobe-sign.html)
- [Ajouter un nouveau paramètre régional pour un formulaire adaptatif](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/supporting-new-language-localization-core-components.html)
- [Envoi de données de formulaire adaptatif à une base de données](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/data-integration.html?lang=fr)
- [Envoi de données de formulaire adaptatif à un point de terminaison REST](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#submit-to-rest-endpoint)
- [Envoi de données de formulaire adaptatif au processus AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#invoke-an-aem-workflow)
- [Utilisation de Forms Portal pour répertorier AEM Forms adaptatif sur un site web AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-forms-portal.html)

