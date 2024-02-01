---
title: Composant principal de formulaires adaptatifs - Conteneur de formulaires
description: Ajoutez un formulaire adaptatif à une page Web.
role: Architect, Developer, Admin, User
exl-id: 03c4cf7c-51d6-4850-a566-1c0514d52dab
source-git-commit: 4d01c75fadb0220f0093a6647c27c4002cc979c9
workflow-type: ht
source-wordcount: '1297'
ht-degree: 100%

---

# Conteneur de formulaires {#form-container-adaptive-forms-core-component}

Les formulaires permettent aux visiteurs et aux visiteuses d’un site Web d’interagir avec ce site en fournissant des informations précieuses, ce qui peut augmenter l’engagement et la satisfaction des utilisateurs et des utilisatrices. Un conteneur de formulaires adaptatifs dans Adobe Experience Manager (AEM) Sites permet aux propriétaires de sites Web d’ajouter facilement des formulaires à leurs pages. Cela facilite la communication entre les visiteurs et les visiteuses du site Web et le/la propriétaire ou l’organisation du site Web en permettant aux visiteurs et aux visiteuses de fournir des commentaires, de répondre à des questions et de terminer d’autres actions de manière simplifiée.

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

![Onglet De base](/help/adaptive-forms/assets/formcontainer_basictab.png)

- **Services de préremplissage** : cette option permet à l’utilisateur ou à l’utilisatrice de sélectionner un service de préremplissage pour récupérer les données lors de la génération du formulaire adaptatif. En savoir plus sur [comment créer et configurer un service de préremplissage](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=fr#aem-forms-custom-prefill-service).

- **Catégorie de bibliothèque cliente** - L’utilisateur ou l’utilisatrice peut configurer une bibliothèque JavaScript personnalisée par formulaire adaptatif. Il est recommandé de ne conserver que les fonctions réutilisables de la bibliothèque, qui dépendent des bibliothèques tierces jquery et underscore.js.
Parfois, en cas de **règles de validation complexes**, le script de validation exact réside dans des fonctions personnalisées que l’utilisateur ou l’utilisatrice doit appeler à partir de l’expression du champ de validation. Pour rendre cette bibliothèque de fonctions personnalisées visible et disponible lors des validations côté serveur, l’utilisateur ou l’utilisatrice de formulaires peut configurer le nom de la bibliothèque cliente AEM sous l’onglet **[!UICONTROL Réglages de base]** des propriétés de conteneur de formulaires adaptatifs comme illustré ci-dessous.

L’utilisateur ou l’utilisatrice peut configurer la bibliothèque personnalisée JavaScript pour chaque formulaire adaptatif. Dans la bibliothèque, conservez uniquement les fonctions réutilisables ayant une dépendance sur les bibliothèques tierces jquery et underscore.js.

### Onglet Modèle de données {#data-model-tab}

![Onglet Envoi](/help/adaptive-forms/assets/formcontainer_fdmtab.png)

Vous pouvez utiliser le modèle de données de formulaire pour connecter un formulaire à une source de données afin d’envoyer et de recevoir des données en fonction des actions de l’utilisateur ou de l’utilisatrice. Vous pouvez également connecter un formulaire à un schéma JSON pour recevoir les données envoyées dans un format prédéfini. Selon les besoins, connectez votre formulaire à un schéma JSON ou à un modèle de données de formulaire :
- Créer un schéma JSON et le charger dans votre environnement
- Créer un modèle de données de formulaire

### Onglet Envoi {#submission-tab}

![Onglet Envoi](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

Les utilisateurs et les utilisatrices peuvent configurer différentes actions pour les envois de formulaires adaptatifs.

- **URL/chemin de redirection** - Cette option permet à l’utilisateur ou à l’utilisatrice de configurer une page pour chaque formulaire, vers laquelle les utilisateurs et utilisatrices du formulaire sont redirigés après l’envoi d’un formulaire adaptatif. Cliquez ici pour plus d’informations sur [la façon de configurer des pages de redirection](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html?lang=fr).

![Onglet Afficher le message](/help/adaptive-forms/assets/formconatiner_showmessage.png)

- **Afficher le message** - Cette option permet aux utilisateurs et utilisatrices d’ajouter un message qui s’affiche lorsque le formulaire adaptatif est envoyé avec succès. Le texte prédéfini est inclus dans la boîte de dialogue et peut être modifié par l’utilisateur ou l’utilisatrice. La boîte de dialogue Afficher le message prend en charge les outils de mise en forme de texte enrichi qui permettent aux utilisateurs et aux utilisatrices de mettre en forme le texte ajouté.

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

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Articles connexes {#related-articles}

{{more-like-this}}

## Voir également {#see-also}

{{see-also}}