---
title: Composant principal de formulaires adaptatifs - Conteneur de formulaires
description: Ajoutez un formulaire adaptatif à une page Web.
role: Architect, Developer, Admin, User
exl-id: 03c4cf7c-51d6-4850-a566-1c0514d52dab
source-git-commit: 86a30bc396d89340106177deb08323bfc5640e0e
workflow-type: tm+mt
source-wordcount: '1526'
ht-degree: 91%

---

# Conteneur de formulaire {#form-container-adaptive-forms-core-component}

<span class="preview"> Cet article traite de la fonctionnalité **Brouillons** <!--and **Hamburger Menu Support** -->, qui est une fonctionnalité de version préliminaire. La fonctionnalité de version préliminaire n’est accessible que par le biais de notre [canal de version préliminaire](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/release-notes/prerelease#new-features).</span>

Les formulaires permettent aux visiteurs et aux visiteuses d’un site Web d’interagir avec ce site en fournissant des informations précieuses, ce qui peut augmenter l’engagement et la satisfaction des utilisateurs et des utilisatrices. Un conteneur de formulaires adaptatifs dans Adobe Experience Manager (AEM) Sites permet aux propriétaires de sites Web d’ajouter facilement des formulaires à leurs pages. Cela facilite la communication entre les visiteurs et les visiteuses du site Web et le/la propriétaire ou l’organisation du site Web en permettant aux visiteurs et aux visiteuses de fournir des commentaires, de répondre à des questions et de terminer d’autres actions de manière simplifiée

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

![Onglet De base](/help/adaptive-forms/assets/formcontainer_basictab1.png)

- **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

- **Services de préremplissage** : cette option permet à l’utilisateur ou à l’utilisatrice de sélectionner un service de préremplissage pour récupérer les données lors de la génération du formulaire adaptatif. En savoir plus sur [comment créer et configurer un service de préremplissage](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=fr#aem-forms-custom-prefill-service).

- **Rôle** : le rôle est un attribut d’HTML utilisé pour spécifier l’objectif d’un élément d’HTML pour les technologies d’assistance telles que les lecteurs d’écran. L’attribut rôle est utilisé pour fournir un contexte et une signification sémantique supplémentaires à un élément, ce qui facilite l’interprétation et l’annonce du contenu à l’utilisateur ou à l’utilisatrice par les lecteurs d’écran. Par exemple, dans AEM Forms, le libellé d’un champ de formulaire peut avoir le rôle « libellé » et son champ de saisie peut avoir le rôle « zone de texte ». Cela permet au lecteur d’écran de comprendre la relation entre le libellé et le champ de saisie, et de les annoncer correctement à l’utilisateur ou à l’utilisatrice.

- **Catégorie de bibliothèque cliente** - L’utilisateur ou l’utilisatrice peut configurer une bibliothèque JavaScript personnalisée par formulaire adaptatif. Il est recommandé de ne conserver que les fonctions réutilisables de la bibliothèque, qui dépendent des bibliothèques tierces jquery et underscore.js.
Parfois, en cas de **règles de validation complexes**, le script de validation exact réside dans des fonctions personnalisées que l’utilisateur ou l’utilisatrice doit appeler à partir de l’expression du champ de validation. Pour rendre cette bibliothèque de fonctions personnalisées visible et disponible lors des validations côté serveur, l’utilisateur du formulaire peut configurer le nom de la bibliothèque cliente AEM sous l’onglet **[!UICONTROL De base]** des propriétés du conteneur de formulaires adaptatifs.
L’utilisateur ou l’utilisatrice peut configurer la bibliothèque personnalisée JavaScript pour chaque formulaire adaptatif. Dans la bibliothèque, conservez uniquement les fonctions réutilisables ayant une dépendance sur les bibliothèques tierces jquery et underscore.js.

<!--
- **Enable the hamburger menu for mobile view** - Select the checkbox to integrate a hamburger menu into your form for mobile view. Represented by three horizontal lines stacked vertically, this menu provides a clear and uncluttered display for panels on smaller devices, especially on mobile devices. For more information about the hamburger menu, refer to the [Learn more about the hamburger menu](#learn-more-about-the-hamburger-menu) section. -->


### Onglet Modèle de données {#data-model-tab}

![Onglet Envoi](/help/adaptive-forms/assets/formcontainer_fdmtab.png)

Vous pouvez utiliser le modèle de données de formulaire pour connecter un formulaire à une source de données afin d’envoyer et de recevoir des données en fonction des actions de l’utilisateur ou de l’utilisatrice. Vous pouvez également connecter un formulaire à un schéma JSON pour recevoir les données envoyées dans un format prédéfini. Selon les besoins, connectez votre formulaire à un schéma JSON ou à un modèle de données de formulaire :
- Créer un schéma JSON et le charger dans votre environnement
- Créer un modèle de données de formulaire

### Brouillons

![Onglet Envoi](/help/adaptive-forms/assets/formcontainer_autosavetab.png)

- **Enregistrement automatique des brouillons** : cochez la case **Enregistrement automatique des brouillons** pour activer l’enregistrement des formulaires en tant que brouillons.
- **Save Preference** : configurez **Save Preference** en tant que **Enregistrer les brouillons à intervalles réguliers**, pour enregistrer automatiquement le formulaire après un intervalle de temps spécifique.
  **Périodicité de l’intervalle de sauvegarde (secondes)** : spécifiez l’intervalle de temps (en secondes) pour définir la durée qui déclenche l’enregistrement automatique du formulaire à l’intervalle défini.

### Onglet Envoi {#submission-tab}

Les utilisateurs et les utilisatrices peuvent configurer différentes actions pour les envois de formulaires adaptatifs.

- **URL/chemin de redirection** - Cette option permet à l’utilisateur ou à l’utilisatrice de configurer une page pour chaque formulaire, vers laquelle les utilisateurs et utilisatrices du formulaire sont redirigés après l’envoi d’un formulaire adaptatif. Cliquez ici pour plus d’informations sur [la façon de configurer des pages de redirection](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html?lang=fr).

![Onglet Envoi](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

- **Afficher le message** - Cette option permet aux utilisateurs et utilisatrices d’ajouter un message qui s’affiche lorsque le formulaire adaptatif est envoyé avec succès. Le texte prédéfini est inclus dans la boîte de dialogue et peut être modifié par l’utilisateur ou l’utilisatrice. La boîte de dialogue Afficher le message prend en charge les outils de mise en forme de texte enrichi qui permettent aux utilisateurs et aux utilisatrices de mettre en forme le texte ajouté.

![Onglet Afficher le message](/help/adaptive-forms/assets/formconatiner_showmessage.png)

- **Action Envoyer** - Une action Envoyer est déclenchée lorsqu’un utilisateur ou une utilisatrice clique sur le bouton Envoyer d’un formulaire adaptatif. Les utilisateurs et les utilisatrices peuvent sélectionner les actions Envoyer dans la liste déroulante qui sont prises en charge par défaut. Découvrir comment [configurer une action Envoyer dans l’onglet Envoi](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html?lang=fr#supporting-custom-functions-in-validation-expressions-br).

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

<!--
## Learn more about the hamburger menu

A hamburger menu, often referred to as a mobile menu or navigation drawer, is a popular design element in mobile user interfaces. It features three horizontal lines stacked vertically, resembling a hamburger. The design efficiently conserves screen space by hiding secondary navigation options until they are needed, especially on smaller devices such as mobile. AEM forms can be efficiently organized within the hamburger menu, enabling users to access various panels within a form without overwhelming the main interface.

Consider a scenario, where a financial institution offers an online loan application form that requires users to provide detailed information across several panels, such as personal details, financial information, loan preferences, and supporting documents. The form includes multiple panels and options that can clutter the interface, especially on mobile devices. Users need an organized way to navigate through these panels without feeling overwhelmed. The hamburger menu is implemented to enhance the user experience on mobile devices.

### Components of hamburger menu

![Hamburger Menu](/help/adaptive-forms/assets/hamburger-menu.png){width=50%, align=center}

**A. Hamburger menu**: The hamburger menu features a navigation panel that slides out or drops down when the hamburger icon is clicked or tapped. The menu displays the panel headings, and selecting a panel shifts the focus to that panel. It allows users to easily navigate between different panels.

![Hamburger Menu](/help/adaptive-forms/assets/hamburger-menu-icon.png){width=50%}

**B. Breadcrumb**: Breadcrumbs indicate the user’s current location within the form. They offer a hierarchical trail that shows the user’s navigation path and helps them understand their position in the form.

**C. Active panel**: The active panel refers to the section or part of the form that is currently being displayed. When a user selects an option from the hamburger menu, the corresponding panel becomes the active panel, showing the relevant fields and information for that section.

### Points to consider while working with the hamburger menu

- The hamburger menu displays only the names of the panels. Here are different scenarios illustrating how the panel name appears in the navigation pane of the hamburger menu based on the configuration properties of the panel:  
  
  - If you set the properties of the panel to hidden, the panel's name does not appear in the navigation pane of the hamburger menu. For example, if you configure the properties of the `Financial Information` panel as `hidden`, the panel name does not appear in the navigation pane of the hamburger menu.
    
    ![Hidden panel](/help/adaptive-forms/assets/hidden-panel.png){width=50%}

  - If you set the properties of the panel to `disabled`, its name appears in the navigation pane of the hamburger menu, but you cannot select or edit it. For example, if you configure the properties of the `Financial Information` panel as `disabled`, the panel name appears in the navigation pane, but it cannot be selected or edited. 
     
    ![Disabled panel](/help/adaptive-forms/assets/disabled-panel.png){width=50%}

  - If you hide the  title of the panel, it does not appear in the navigation pane of the hamburger menu. A blank space shows up instead, but you can navigate to the fields of the panel by clicking on that space. For example, if you hide the title of the `Financial Information` panel, the blank space appears in its place in the navigation pane of the hamburger menu. You can navigate to the fields of the panel by clicking on the blank space.
    
    ![Hidden title panel](/help/adaptive-forms/assets/hidden-title-panel.png){width=50%}

- By default, the navigation pane in the breadcrumb component supports up to three levels of navigation. However, with the custom component, you can configure the navigation hierarchy to accommodate as many levels as needed.
- When using the hamburger menu, the user can navigate between panels using arrows. However, once a panel is selected, the menu automatically closes, and focus shifts to the fields within the chosen panel.

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

![Basic tab](/help/adaptive-forms/assets/formcontainer_basictab.png)
-->

## Articles connexes {#related-articles}

{{more-like-this}}

## Voir également {#see-also}

{{see-also}}