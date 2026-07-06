---
title: Composant principal de formulaires adaptatifs - Conteneur de formulaires
description: Ajoutez un formulaire adaptatif à une page Web.
role: Developer, Admin, User
exl-id: 03c4cf7c-51d6-4850-a566-1c0514d52dab
TQID: https://experienceleague.adobe.com/kMG6SKHisAUmKhOh9AFLI8NG6w0vH7tP4XimBKAMo-I
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 0af65c80f9cc58c4ba48d5b3dc7a026820bd2833
workflow-type: tm+mt
source-wordcount: 2555
ht-degree: 64%

---

# Conteneur de formulaire {#form-container-adaptive-forms-core-component}

<span class="preview"> Cet article traite des fonctionnalités **Drafts** et **Hamburger Menu Support**, qui sont des fonctionnalités de version préliminaire. La fonctionnalité de version préliminaire n’est accessible que par le biais de notre [canal de version préliminaire](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=fr#new-features).</span>

Les formulaires permettent aux visiteurs et aux visiteuses d’un site Web d’interagir avec ce site en fournissant des informations précieuses, ce qui peut augmenter l’engagement et la satisfaction des utilisateurs et des utilisatrices. Un conteneur de formulaires adaptatifs dans Adobe Experience Manager (AEM) Sites permet aux propriétaires de sites Web d’ajouter facilement des formulaires à leurs pages. Cela facilite la communication entre les visiteurs et les visiteuses du site Web et le/la propriétaire ou l’organisation du site Web en permettant aux visiteurs et aux visiteuses de fournir des commentaires, de répondre à des questions et de terminer d’autres actions de manière simplifiée

{{traditional-aem}}

## Utilisation {#reasons-to-use-forms-container}

Plusieurs raisons peuvent expliquer l’ajout d’un formulaire à un site Web :
- **Collecte de données** : les formulaires peuvent être utilisés pour collecter des données auprès des visiteurs et visiteuses de sites Web à diverses fins, telles que des recherches sur le marché, une analyse du comportement des utilisateurs et des utilisatrices, etc.

- **Génération de piste** : un formulaire peut être utilisé pour recueillir des informations auprès de clients et clientes potentiels, tels que le nom et l’adresse électronique, afin de générer des pistes pour les efforts de vente et de marketing.

- **E-commerce** : les formulaires peuvent être utilisés pour les achats en ligne, ce qui permet aux clients et clientes de passer des commandes et d’effectuer des paiements sur le site Web.

- **Contact** : un formulaire de contact permet aux visiteurs et visiteuses du site Web d’accéder facilement au propriétaire ou à l’organisation du site Web.

- **Questionnaires et sondages** : les formulaires peuvent être utilisés pour recueillir les commentaires et les opinions des visiteurs et visiteuses du site par le biais d’enquêtes et de sondages.

- **Enregistrement d’événements** : les formulaires peuvent être utilisés pour l’enregistrement d’événements, ce qui permet aux visiteurs et visiteuses du site Web de s’inscrire à des événements ou à des webinaires.

- **Abonnements** : les formulaires peuvent être utilisés pour les abonnements à des sites Web, ce qui permet aux visiteurs et aux visiteuses de s’abonner à une newsletter ou à d’autres communications régulières.

- **Authentification de l’utilisateur** : les formulaires peuvent être utilisés pour l’authentification des utilisateurs et des utilisatrices, ce qui permet aux visiteurs et aux visiteuses du site Web de créer des comptes et de se connecter pour accéder à du contenu ou à des fonctionnalités exclusifs.

- **Augmentation du taux de conversion** : un formulaire bien conçu peut augmenter le taux de conversion en facilitant la réalisation de l’action souhaitée par les utilisateurs et les utilisatrices, comme l’achat d’un produit ou l’inscription à un service.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Accordéon des formulaires adaptatifs a été publié en février 2023 au sein des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec la <br>[version 2.0.4](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible avec les<br>[versions 1.1.12](/help/adaptive-forms/version.md) à 2.0.0 exclue. |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).
<!--
## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_fr). 
-->

## Détails techniques {#technical-details}

Obtenez les dernières informations sur le composant principal de conteneur des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation relative au développement des composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser votre expérience de conteneur de formulaires pour les visiteurs et les visiteuses avec la boîte de dialogue de configuration. Vous pouvez également définir facilement des options de conteneur de formulaires pour une expérience utilisateur transparente.

### Onglet De base {#basic-tab}

![Onglet De base](/help/adaptive-forms/assets/formcontainer_basictab1.png)

- **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

- **Services de préremplissage** : cette option permet à l’utilisateur ou à l’utilisatrice de sélectionner un service de préremplissage pour récupérer les données lors de la génération du formulaire adaptatif. En savoir plus sur [comment créer et configurer un service de préremplissage](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=fr#aem-forms-custom-prefill-service).

- **Rôle** : le rôle est un attribut HTML utilisé pour spécifier l’objectif d’un élément HTML pour les technologies d’assistance telles que les lecteurs d’écran. L’attribut rôle est utilisé pour fournir un contexte et une signification sémantique supplémentaires à un élément, ce qui facilite l’interprétation et l’annonce du contenu à l’utilisateur ou à l’utilisatrice par les lecteurs d’écran. Par exemple, dans AEM Forms, le libellé d’un champ de formulaire peut avoir le rôle « libellé » et son champ de saisie peut avoir le rôle « zone de texte ». Cela permet au lecteur d’écran de comprendre la relation entre le libellé et le champ de saisie, et de les annoncer correctement à l’utilisateur ou à l’utilisatrice.

- **Catégorie de bibliothèque cliente** : l’utilisateur ou l’utilisatrice peut configurer une bibliothèque JavaScript personnalisée par formulaire adaptatif. Il est recommandé de ne conserver que les fonctions réutilisables de la bibliothèque, qui dépendent des bibliothèques tierces jquery et underscore.js.Parfois, en cas de **règles de validation complexes**, le script de validation exact réside dans des fonctions personnalisées que l’utilisateur ou l’utilisatrice doit appeler à partir de l’expression du champ de validation. Pour rendre cette bibliothèque de fonctions personnalisées visible et disponible lors des validations côté serveur, l’utilisateur ou l’utilisatrice de formulaires peut configurer le nom de la bibliothèque cliente AEM sous l’onglet **[!UICONTROL Réglages de base]** des propriétés du conteneur de formulaires adaptatifs.L’utilisateur ou l’utilisatrice peut configurer la bibliothèque personnalisée JavaScript pour chaque formulaire adaptatif. Dans la bibliothèque, conservez uniquement les fonctions réutilisables ayant une dépendance sur les bibliothèques tierces jquery et underscore.js.

- **Activer le menu hamburger pour la vue mobile** - Cochez la case pour intégrer un menu hamburger dans votre formulaire pour la vue mobile. Représenté par trois lignes horizontales empilées verticalement, ce menu offre un affichage clair et épuré pour les panneaux sur les appareils plus petits, en particulier sur les appareils mobiles. Pour plus d’informations sur le menu hamburger, reportez-vous à la section [En savoir plus sur le menu hamburger](#learn-more-about-the-hamburger-menu).


### Onglet Modèle de données {#data-model-tab}

![Onglet Modèle de données](/help/adaptive-forms/assets/formcontainer_fdmtab.png)

Vous pouvez utiliser le modèle de données de formulaire pour connecter un formulaire à une source de données afin d’envoyer et de recevoir des données en fonction des actions de l’utilisateur ou de l’utilisatrice. Vous pouvez également connecter un formulaire à un schéma JSON pour recevoir les données envoyées dans un format prédéfini. Selon les besoins, connectez votre formulaire à un schéma JSON ou à un modèle de données de formulaire :
- **Aucun** - N’associez pas le formulaire à un modèle de données.
- **Schéma** - Connectez le formulaire à un schéma JSON chargé dans votre environnement.
- **Modèle de données de formulaire** - Connectez le formulaire à un modèle de données de formulaire à intégrer à des sources de données externes.
- **Connecteur** - Connectez le formulaire à une source de données basée sur un connecteur.
- **Modèles de formulaire** - Associez le formulaire à un modèle de formulaire.

### Onglet Brouillons {#drafts-tab}

![Onglet Brouillons](/help/adaptive-forms/assets/formcontainer_autosavetab.png)

- **Enregistrer automatiquement les brouillons** : cochez la case **Enregistrer automatiquement les brouillons** pour activer l’enregistrement des formulaires en tant que brouillons.
- **Préférence d’enregistrement** : configurez la **préférence d’enregistrement** sur **Enregistrer des brouillons à intervalles réguliers** pour enregistrer automatiquement le formulaire après un intervalle de temps spécifique.
  **Fréquence d’intervalle d’enregistrement (en secondes)** : spécifiez l’intervalle de temps (en secondes) pour déterminer la durée qui déclenche l’enregistrement automatique du formulaire selon l’intervalle configuré.

### Onglet Envoi {#submission-tab}

Les utilisateurs et les utilisatrices peuvent configurer différentes actions pour les envois de formulaires adaptatifs.

- **Lors de l’envoi** - Sélectionnez **Rediriger vers l’URL** pour envoyer les utilisateurs du formulaire vers une page configurée après l’envoi, ou **Afficher le message** pour afficher un message de confirmation sur le formulaire.

- **URL/chemin de redirection** - Cette option permet à l’utilisateur ou à l’utilisatrice de configurer une page pour chaque formulaire, vers laquelle les utilisateurs et utilisatrices du formulaire sont redirigés après l’envoi d’un formulaire adaptatif. Cliquez ici pour plus d’informations sur [la façon de configurer des pages de redirection](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html?lang=fr).

![Onglet Envoi](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

- **Afficher le message** - Cette option permet aux utilisateurs et utilisatrices d’ajouter un message qui s’affiche lorsque le formulaire adaptatif est envoyé avec succès. Le texte prédéfini est inclus dans la boîte de dialogue et peut être modifié par l’utilisateur ou l’utilisatrice. La boîte de dialogue Afficher le message prend en charge les outils de mise en forme de texte enrichi qui permettent aux utilisateurs et aux utilisatrices de mettre en forme le texte ajouté.

![Onglet Afficher le message](/help/adaptive-forms/assets/formconatiner_showmessage.png)

- **Action Envoyer** - Une action Envoyer est déclenchée lorsqu’un utilisateur ou une utilisatrice clique sur le bouton Envoyer d’un formulaire adaptatif. Les utilisateurs et les utilisatrices peuvent sélectionner les actions Envoyer dans la liste déroulante qui sont prises en charge par défaut. Découvrir comment [configurer une action Envoyer dans l’onglet Envoi](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html?lang=fr#supporting-custom-functions-in-validation-expressions-br).

- **Configuration de l’action** - Configurez les mappages pour la transmission des valeurs de champ en tant que paramètres de requête de page de remerciement.

- **Activer la requête POST** - Sélectionnez cette option pour envoyer les données de formulaire à l’aide d’une requête HTTP POST.

### Onglet Document d’enregistrement {#document-of-record-tab}

![Onglet Document d’enregistrement](/help/adaptive-forms/assets/formcontainer_dortab.png)

Un [&#x200B; document d’enregistrement (DE)](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/generate-document-of-record-core-components) est une représentation formelle et imprimable des données envoyées via le formulaire. Utilisez l’onglet **Document d’enregistrement** pour configurer la manière dont un document d’enregistrement est généré lorsqu’un utilisateur envoie le formulaire :

- **Aucun** - Ne générez pas de document d’enregistrement pour le formulaire.
- **Associer le modèle de formulaire en tant que modèle de document d’enregistrement** - Utilisez un modèle de formulaire existant en tant que modèle de document d’enregistrement.
- **Générer un document d’enregistrement** - Génère automatiquement un document d’enregistrement en fonction des données de formulaire envoyées.
- **Exclure les pièces jointes du document d’enregistrement** - Sélectionnez cette option pour omettre les pièces jointes du document d’enregistrement généré.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS pour le composant Conteneur de formulaire.

### Onglet Composants autorisés {#allowed-components-tab}

![Onglet Composant autorisé de la boîte de dialogue de conception](/help/adaptive-forms/assets/formcontainer-allowedcomponents.png)

L’onglet **Composants autorisés** permet à l’éditeur de modèles de définir les composants qui peuvent être ajoutés en tant qu’éléments aux panneaux dans le composant de l’éditeur de formulaires adaptatifs.

### Onglet Composants par défaut {#default-components-tab}

![Onglet Composant par défaut de la boîte de dialogue de conception](/help/adaptive-forms/assets/formcontainer-defaultcomponents.png)

L’onglet **Composants par défaut** permet à l’éditeur de modèles de spécifier les composants visibles par défaut en tant qu’éléments dans le composant Conteneur de formulaire dans l’éditeur de formulaires adaptatifs.

### Onglet Paramètres réactifs {#responsive-tab}

![Onglet Paramètres réactifs de la boîte de dialogue de conception](/help/adaptive-forms/assets/formcontainer-responsivestyle.png)

L’onglet **Paramètres réactifs** permet à l’éditeur de modèles de spécifier le nombre de colonnes dans la grille à l’intérieur du composant Conteneur de formulaire de l’éditeur de formulaires adaptatifs.

### Onglet Styles {#styles-tab}

Le composant principal « Pièce jointe » des formulaires adaptatifs prend en charge le [Système de style](/help/get-started/authoring.md#component-styling) d’AEM.

![Boîte de dialogue de conception.](/help/adaptive-forms/assets/formcontainer-styletab.png)

- **Classes CSS par défaut** : vous pouvez fournir une classe CSS par défaut pour le composant principal Conteneur de formulaire des formulaires adaptatifs.

- **Styles autorisés** : vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé « texte en gras » et fournir la classe CSS « police d’épaisseur : gras ». Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de formulaires adaptatifs. Pour appliquer un style, sélectionnez le composant auquel vous souhaitez appliquer le style dans l’éditeur de formulaires adaptatifs, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans la liste déroulante **Styles**. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

### Onglet Propriétés personnalisées

![Boîte de dialogue Propriétés personnalisées](/help/adaptive-forms/assets/formcontainer-custompropertiestab.png)

Les propriétés personnalisées vous permettent d’associer des attributs personnalisés (paires clé-valeur) à un composant principal de formulaire adaptatif à l’aide du modèle de formulaire. Les propriétés personnalisées sont répercutées dans la section des propriétés du rendu déocuplé du composant. Cela permet de créer un comportement de formulaire dynamique qui s’adapte en fonction des valeurs d’attributs personnalisés. Par exemple, les développeurs et développeuses peuvent concevoir plusieurs rendus d’un composant de formulaires découplés pour des plateformes mobiles, de bureau ou web, ce qui améliore considérablement l’expérience client sur un large éventail d’appareils.

- **Nom du groupe** : vous pouvez fournir un nom pour identifier le groupe de propriétés personnalisées. Vous pouvez ajouter, supprimer ou réorganiser plusieurs groupes de propriétés personnalisées. Après avoir ajouté le groupe de propriétés personnalisées, vous pouvez voir les options suivantes :

   - **Paires clé-valeur** : vous pouvez ajouter plusieurs noms et valeurs de propriétés personnalisées en cliquant sur le bouton **Ajouter** pour chaque groupe de propriétés personnalisées.

   - **Supprimer** : appuyez ou cliquez pour supprimer le nom et la valeur des propriétés personnalisées.

   - **Réorganiser** : appuyez ou cliquez et faites glisser pour réorganiser l’ordre du nom et de la valeur des propriétés personnalisées.

## En savoir plus sur le menu hamburger {#learn-more-about-the-hamburger-menu}

Un menu hamburger, souvent appelé menu mobile ou tiroir de navigation, est un élément de conception populaire dans les interfaces utilisateur mobiles. Il comporte trois lignes horizontales empilées verticalement, ressemblant à un hamburger. La conception permet de conserver efficacement l’espace de l’écran en masquant les options de navigation secondaires jusqu’à ce qu’elles soient nécessaires, en particulier sur les appareils plus petits tels que les appareils mobiles. Les formulaires AEM peuvent être efficacement organisés dans le menu hamburger, ce qui permet aux utilisateurs d’accéder à divers panneaux au sein d’un formulaire sans surcharger l’interface principale.

Supposons qu’une institution financière propose un formulaire de demande de prêt en ligne qui oblige les utilisateurs à fournir des informations détaillées sur plusieurs panneaux, telles que des détails personnels, des informations financières, des préférences de prêt et des documents annexes. Le formulaire comprend plusieurs panneaux et options qui peuvent encombrer l’interface, en particulier sur les appareils mobiles. Les utilisateurs ont besoin d’une manière organisée de naviguer dans ces panneaux sans se sentir dépassés. Le menu hamburger est implémenté pour améliorer l’expérience utilisateur sur les appareils mobiles.

### Composants du menu hamburger

![Menu Hamburger &#x200B;](/help/adaptive-forms/assets/hamburger-menu.png){width=50%, align=center}

**A. Menu hamburger** : le menu hamburger comporte un panneau de navigation qui glisse ou s’abaisse lorsque l’on clique ou que l’on appuie sur l’icône hamburger. Le menu affiche les en-têtes du panneau et la sélection d’un panneau déplace le focus vers ce panneau. Il permet aux utilisateurs de naviguer facilement entre les différents panneaux.

![Menu Hamburger &#x200B;](/help/adaptive-forms/assets/hamburger-menu-icon.png){width=50%}

**B. Chemin de navigation** : les chemins de navigation indiquent l’emplacement actuel de l’utilisateur dans le formulaire. Ils offrent un suivi hiérarchique qui montre le chemin de navigation de l’utilisateur et l’aide à comprendre sa position dans le formulaire.

**C. Panneau actif** le panneau actif fait référence à la section ou à la partie du formulaire en cours d’affichage. Lorsqu’un utilisateur sélectionne une option dans le menu hamburger , le panneau correspondant devient le panneau actif, affichant les champs et informations pertinents pour cette section.

### Points à prendre en compte lorsque vous utilisez le menu hamburger

- Le menu hamburger affiche uniquement les noms des panneaux. Voici différents scénarios illustrant la manière dont le nom du panneau apparaît dans le volet de navigation du menu hamburger en fonction des propriétés de configuration du panneau :

   - Si vous définissez les propriétés du panneau sur masqué, le nom du panneau n’apparaît pas dans le volet de navigation du menu hamburger. Par exemple, si vous configurez les propriétés du panneau `Financial Information` comme `hidden`, le nom du panneau n’apparaît pas dans le volet de navigation du menu hamburger.

     ![&#x200B; Panneau masqué &#x200B;](/help/adaptive-forms/assets/hidden-panel.png){width=50%}

   - Si vous définissez les propriétés du panneau sur `disabled`, son nom apparaît dans le volet de navigation du menu hamburger, mais vous ne pouvez pas le sélectionner ni le modifier. Par exemple, si vous configurez les propriétés du panneau `Financial Information` comme `disabled`, le nom du panneau s’affiche dans le volet de navigation, mais il ne peut pas être sélectionné ni modifié.

     ![Panneau désactivé](/help/adaptive-forms/assets/disabled-panel.png){width=50%}

   - Si vous masquez le titre du panneau, il n’apparaît pas dans le volet de navigation du menu hamburger. Un espace vierge s’affiche à la place de cette sélection, mais vous pouvez accéder aux champs du panneau en cliquant dessus. Par exemple, si vous masquez le titre du panneau `Financial Information`, l’espace vide s’affiche à sa place dans le volet de navigation du menu hamburger. Vous pouvez accéder aux champs du panneau en cliquant sur l’espace vide.

     ![Panneau de titre masqué](/help/adaptive-forms/assets/hidden-title-panel.png){width=50%}

- Par défaut, le volet de navigation du composant de chemin de navigation prend en charge jusqu’à trois niveaux de navigation. Cependant, avec le composant personnalisé, vous pouvez configurer l’arborescence de navigation pour accueillir autant de niveaux que nécessaire.
- Lorsque vous utilisez le menu hamburger, l’utilisateur peut naviguer entre les panneaux à l’aide de flèches. Cependant, une fois qu’un panneau est sélectionné, le menu se ferme automatiquement et le focus se déplace vers les champs du panneau sélectionné.

<!--
### Advantages to use hamburger menu

- **Space efficiency**: By hiding form navigation options until needed, the hamburger menu maximizes screen space, which is especially beneficial on smaller devices.

- **Clutter reduction**: It minimizes visual clutter by consolidating various form navigation links into a single, collapsible menu.

- **Improved focus**: With fewer visible navigation elements, users can concentrate on the main content of the form without being distracted by secondary options.

- **Simplified design**: It creates a more streamlined user interface, resulting in a cleaner and more organized form layout.

- **Enhanced mobile experience**: On mobile devices, where screen space is limited, the hamburger menu offers an efficient way to access all form navigation options without overwhelming the user.

### How to enable hamburger menu for your form?

To enable hamburger menu for form, perform the following steps:

1. Open form in an edit mode.
1. Open the Content browser, and select the **[!UICONTROL Guide Container]** component of your Adaptive Form. 
1. Click the Guide Container properties ![Guide properties](/help/adaptive-forms/assets/configure_icon.png) icon. The Adaptive Form Container dialog box opens. 
1. Click the  **[!UICONTROL Basic]** tab. 
1. Select the **[!UICONTROL Add hamburger menu support]** checkbox.
1. Click **[!UICONTROL Done]**.

![Basic tab](/help/adaptive-forms/assets/formcontainer_basictab1.png)
-->

## Articles connexes {#related-articles}

{{more-like-this}}

## Voir également {#see-also}

{{see-also}}