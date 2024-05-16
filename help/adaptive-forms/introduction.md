---
title: Présentation des composants principaux des formulaires adaptatifs AEM
description: Créez des expériences d’inscription attrayantes (formulaires) grâce à la flexibilité des composants principaux des formulaires adaptatifs et diffusez-les avec la puissance d’Adobe Experience Manager.
role: Architect, Developer, Admin, User
exl-id: 6d0f2845-bbb8-4488-a254-b69d7a6290b1
source-git-commit: 23ad6de410aaf4952607d9a4aa44864b0743c479
workflow-type: tm+mt
source-wordcount: '2154'
ht-degree: 57%

---

# Présentation des composants principaux des formulaires adaptatifs {#adaptive-forms-core-components-introduction}

À l’aide des composants principaux des formulaires adaptatifs dans Adobe Experience Manager, vous pouvez créer des expériences d’inscription attrayantes grâce à la flexibilité et aux options de personnalisation disponibles.

## Composants principaux  {#overview}

Dans Adobe Experience Manager (AEM), les composants sont les blocs de création utilisés pour créer des pages et des formulaires. Ils offrent aux créateurs et aux créatrices un moyen simple et puissant de créer et de gérer du contenu, tout en offrant aux développeurs et aux développeuses la flexibilité et l’extensibilité nécessaires à la création de composants personnalisés. Ils sont conçus pour accélérer le développement et réduire les coûts de maintenance des sites Web et des formulaires, être flexibles et peuvent être facilement personnalisés en fonction des besoins spécifiques d’un site Web ou d’un formulaire.

Les composants principaux sont également conçus pour être réactifs et prendre en charge un large éventail d’appareils, notamment les ordinateurs, les tablettes et les smartphones. Ils se conforment également aux dernières normes et bonnes pratiques Web, ce qui en fait une solution robuste et fiable pour créer du contenu Web.

Dans l’ensemble, les composants principaux sont un outil essentiel pour la création et la gestion de contenu Web dans AEM. Ils offrent une solution puissante et flexible qui peut contribuer à réduire le temps de développement et les coûts de maintenance, tout en offrant une expérience utilisateur optimale aux visiteurs et visiteuses du site Web.

## Composants principaux des formulaires adaptatifs

Les composants principaux des fomulaires adaptatifs sont un ensemble de 24 composants Open Source compatibles avec BEM qui sont construits sur la base des composants principaux de la gestion de contenu web d’Adobe Experience Manager. Ils sont spécialement conçus pour créer des formulaires adaptatifs, qui sont des formulaires qui s’adaptent au périphérique, au navigateur et à la taille d’écran de l’utilisateur ou de l’utilisatrice.

Ces composants peuvent être utilisés pour créer des expériences de capture de données et d’inscription exceptionnelles en proposant un large éventail d’options de champ de formulaire, notamment des champs de texte, des cases à cocher, des menus déroulants, etc. Ils comprennent également des fonctionnalités telles que la validation, la logique conditionnelle et la conception réactive, qui peuvent être utilisées pour créer des formulaires conviviaux et simples.

En outre, comme ces composants sont en open source, les développeurs et les développeuses peuvent facilement les personnaliser et les étendre pour répondre aux besoins spécifiques de leur entreprise. De plus, ces composants sont construits sur une méthodologie BEM qui garantit leur évolutivité et leur mise à jour.

![image de formulaire adaptatif](assets/sample-adaptive-form.png)

## Fonctions {#features}

|  |  |
|---|---|
| Prêts pour la production | Les composants principaux des formulaires adaptatifs sont 24 composants robustes de gestion de contenu web. |
| Prêts pour le cloud | Disponible pour [AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/home.html?lang=fr). |
| Polyvalents | Les composants représentent des concepts génériques avec lesquels les créateurs et créatrices peuvent assembler pratiquement n’importe quelle disposition. |
| Configurables | Des [politiques de contenu](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html?lang=fr#content-policies) au niveau du modèle définissent les fonctionnalités que les créateurs et créatrices de pages peuvent ou non utiliser. |
| Accessibles | Ils fournissent des libellés ARIA, prennent en charge la navigation au clavier et le texte pour les technologies d’assistance telles que les lecteurs d’écran. |
| Thème utilisable | Les composants implémentent le [système de style](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=fr) et le balisage suit les [conventions CSS BEM](https://getbem.com/). |
| Personnalisables | Plusieurs modèles permettent une personnalisation facile, depuis l’ajustement du code HTML jusqu’à la réutilisation des fonctionnalités avancées. |
| Contrôle de version | La [politique de contrôle de version](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) garantit que les composants principaux ne rendent pas votre site inopérable lorsqu’ils améliorent des éléments susceptibles de vous affecter. |
| Open source | Si quelque chose ne fonctionne pas correctement, contribuez en apportant vos améliorations. |

<!-- comply with [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), -->


## Avantages {#benefits}

Les expériences de capture de données sont essentielles pour la génération de pistes et l’inscription. Les composants principaux des formulaires adaptatifs offrent une solution puissante pour créer des formulaires optimisés pour la capture de données. Voici quelques raisons d’utiliser les composants principaux pour créer ces expériences sur les composants de base :

* **[Disponibilité sur GitHub](https://github.com/adobe/aem-core-forms-components)**: les composants principaux de Forms adaptatif AEM sont Open Source et disponibles sur GitHub, avec une documentation complète. Cela permet aux développeurs et aux développeuses de comprendre plus facilement les composants et leur fonctionnement, ainsi que de contribuer à leur développement. Le site Web [aemcomponents.dev](https://www.aemcomponents.dev/) est également une ressource précieuse, où les développeurs et les développeuses peuvent voir les composants en action et accéder à la documentation détaillée.

* **[Modèle BEM pour le style](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components)**: les composants principaux suivent le modèle BEM (Block Element Modifier) pour le style, qui est une méthodologie bien établie et largement utilisée pour organiser les CSS. Cela permet aux développeurs et aux développeuses de comprendre plus facilement comment les styles sont organisés et comment les modifier en fonction de leurs besoins spécifiques.

* **Aucune dépendance aux bibliothèques tierces** : l’un des avantages des composants principaux est qu’ils ne dépendent pas des bibliothèques JavaScript tierces, y compris JQuery et Underscore. Les composants sont ainsi plus rapides et plus légers, et plus faciles à intégrer dans une implémentation AEM existante.

* **Centrés sur les performances et l’accessibilité** : les composants principaux sont conçus en tenant compte des performances et de l’accessibilité, qui se reflètent dans leurs scores Google Lighthouse élevés et dans leurs scores Web vitaux. Cela facilite la création de pages Web accessibles et performantes pour les développeurs et les développeuses, ce qui est de plus en plus important dans le paysage numérique actuel.

* **Composants de formulaire dans le modèle et les thèmes Sites 30** : les composants principaux prennent en charge les composants de formulaire dans le modèle et les thèmes Sites 30, ce qui facilite la création et la personnalisation de formulaires dans AEM.

* **[Style plus facile](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components)**: les composants principaux sont plus faciles à mettre en forme que leurs homologues des composants de base. Le processus de création du thème est similaire à Sites, avec la possibilité d’hériter du même thème/CSS de la page Sites parente. En outre, le modèle BEM pour le style facilite la compréhension et la modification des styles.

* **Accessibilité**: les composants principaux de Forms adaptatif prennent en charge les normes et directives d’accessibilité afin de s’assurer que les formulaires peuvent être utilisés par les personnes présentant un handicap, y compris celles qui utilisent des technologies d’assistance telles que les lecteurs d’écran.

* **[Contrôle de version](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/add-comments-annotations-versioning-adaptive-form-core-components)**: vous pouvez créer et gérer plusieurs versions d’un Forms adaptatif basé sur les composants principaux, engager des discussions collaboratives par le biais de commentaires et attacher des annotations à des composants de formulaire spécifiques, améliorant ainsi l’expérience globale de création de formulaire.

## Comparaison des composants principaux, des composants de base et des composants de bloc de formulaire {#components}

La version actuelle d’AEM comporte les composants principaux et les composants de base suivants.

| Composants | Composants de base | Composants principaux | Composants de bloc de formulaire | Informations complémentaires |
|------------|:---------------------:|:---------------:|:---------------------:|-----------------------|
| Bloc Adobe Sign | ✔️ | | | L’intégration d’Adobe Sign est disponible uniquement pour les composants de base. |
| Accordéon | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/accordion.md)</span> | | Pour les composants de base, vous pouvez configurer la disposition en accordéon dans les propriétés du composant Panneau. |
| Fragment de formulaire adaptatif | ✔️ | ✔️ | | Pour les composants de base, vous pouvez ajouter un fragment à partir des propriétés d’un composant de panneau. |
| reCAPTCHA du formulaire adaptatif | ✔️ | ✔️ | ✔️ | Pour les composants de base, utilisez le composant Captcha pour ajouter Google reCaptcha à un formulaire. |
| Bouton | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/button.md)</span> | ✔️ | |
| Captcha | ✔️ | | | Pour les composants de base, utilisez le composant Captcha pour ajouter Google reCaptcha à un formulaire. |
| Graphique | ✔️ | | | |
| Case à cocher | ✔️ | ✔️ | | |
| Groupe de cases à cocher | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/checkbox-group.md)</span> | ✔️ | Pour les composants de base, utilisez le composant de case à cocher pour ajouter plusieurs cases à cocher. |
| Champ de saisie de date | ✔️ | | | Pour les composants principaux, utilisez le sélecteur de date ou des composants de zone de texte ou numériques distincts pour capturer un jour, un mois et une année. |
| Sélecteur de date | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/date-picker.md)</span> | ✔️ | |
| Liste déroulante | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/drop-down-list.md)</span> | ✔️ | |
| E-mail | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/email-input.md)</span> | ✔️ | |
| Pièce jointe | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/file-attachment.md)</span> | ✔️ | |
| Liste des pièces jointes | ✔️ | | | |
| Pied de page | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/footer.md)</span> | ✔️ | |
| Espace réservé de note de bas de page | ✔️ | | | |
| Conteneur de formulaires | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/form-container.md)</span> | ✔️ | Pour les composants de base, utilisez le composant Panneau racine. |
| Titre du formulaire | ✔️ | ✔️ | | Pour les composants de base, utilisez le composant de titre. |
| En-tête | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/header.md)</span> | ✔️ | |
| Onglets horizontaux | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/horizontal-tabs.md)</span> | | Pour les composants de base, vous pouvez configurer les onglets dans la disposition supérieure (onglets horizontaux) des propriétés du composant Panneau. |
| Image | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/image.md)</span> | ✔️ | |
| Choix d’image | ✔️ | | | |
| Bouton Suivant | ✔️ | ✔️ | | Utilisez le composant Assistant pour que les boutons suivant et précédent se déplacent entre plusieurs panneaux. |
| Zone numérique | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/numeric-box.md)</span> | ✔️ | |
| Procédure pas à pas numérique | ✔️ | | | |
| Panneau | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/panel.md)</span> | ✔️ | |
| Champ de mot de passe | ✔️ | | ✔️ | |
| Téléphone/Téléphone | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/telephone-input.md)</span> | ✔️ | |
| Bouton Précédent | ✔️ | | | Utilisez le composant Assistant pour que les boutons suivant et précédent se déplacent entre plusieurs panneaux. |
| Bouton radio | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/radio-button.md)</span> | | |
| Groupe de boutons radio | | | ✔️ | |
| Bouton de réinitialisation | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/reset-button.md)</span> | ✔️ | |
| Signature tactile | ✔️ | | | |
| Sperator | ✔️ | | | |
| Bouton Envoyer | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/submit-button.md)</span> | ✔️ | |
| Étape de résumé | ✔️ | | | |
| Basculer | ✔️ | ✔️ | | |
| Tableau | ✔️ | | | |
| Termes et conditions | ✔️ | ✔️ | | |
| Texte | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/text.md)</span> | ✔️ | |
| Zone de texte | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/text-box.md)</span> | ✔️ | |
| Titre | ✔️ | | | Pour les composants principaux, utilisez le composant Titre du formulaire . |
| Onglets verticaux | ✔️ | ✔️ | | Pour les composants de base, vous pouvez configurer la disposition des onglets sur la gauche (onglets verticaux) dans les propriétés du composant Panneau. |
| Assistant | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/wizard.md)</span> | ✔️ | Pour les composants de base, vous pouvez configurer la disposition de l’assistant dans les propriétés du composant Panneau. |




>[!NOTE]
>
>
> * Outre les composants répertoriés ci-dessus, le bloc Forms prend en charge tous les composants valides [Types d’entrée HTML5](https://developer.mozilla.org/fr-fr/docs/Web/HTML/Element/input#input_types) et [textarea](https://developer.mozilla.org/fr-fr/docs/Web/HTML/Element/textarea) en tant que composants.
> * Vous avez besoin d’un composant qui n’est pas répertorié ci-dessus ? Demandez-le en envoyant un courrier électronique à l’adresse aem-forms-ea@adobe.com de votre adresse officielle.


<!-- >
* [Accordion](/help/adaptive-forms/components/accordion.md)
* [Button](/help/adaptive-forms/components/button.md)
* [Check Box Group](/help/adaptive-forms/components/checkbox-group.md)
* [Date Picker](/help/adaptive-forms/components/date-picker.md)
* [Drop-down list](/help/adaptive-forms/components/drop-down-list.md)
* [Email-input](/help/adaptive-forms/components/email-input.md)
* [Form Container](/help/adaptive-forms/components/form-container.md)
* [File Attachment](/help/adaptive-forms/components/file-attachment.md)
* [Footer](/help/adaptive-forms/components/footer.md)
* [Header](/help/adaptive-forms/components/header.md)
* [Horizontal Tabs](/help/adaptive-forms/components/horizontal-tabs.md)
* [Image](/help/adaptive-forms/components/image.md)
* [Numeric Box](/help/adaptive-forms/components/numeric-box.md)
* [Panel](/help/adaptive-forms/components/panel.md)
* [Radio Button](/help/adaptive-forms/components/radio-button.md)
* [Reset Button](/help/adaptive-forms/components/reset-button.md)
* [Submit Button](/help/adaptive-forms/components/submit-button.md)
* [Telephone input](/help/adaptive-forms/components/telephone-input.md)
* [Text Box](/help/adaptive-forms/components/text-box.md)
* [Text](/help/adaptive-forms/components/text.md)
* [Title](/help/adaptive-forms/components/title.md)
* [Wizard](/help/adaptive-forms/components/wizard.md)

-->

## Éditeur de formulaires convivial

L’éditeur de Forms adaptatif basé sur les composants principaux est similaire à celui que vous utilisez déjà pour créer des pages AEM Sites. Voici ce que vous obtenez :


* **Eléments et paramètres d’IU familiers**: lors de la configuration des propriétés pour les composants de formulaire, la boîte de dialogue des propriétés ressemble à celles que vous utilisez pour les composants principaux de la gestion de contenu web. Cela permet de trouver plus rapidement les options dont vous avez besoin. Comme les composants principaux de la gestion de contenu web, la boîte de dialogue des propriétés s’affiche au centre de l’éditeur avec des onglets clairs séparant les options de base et avancées, le texte d’aide et les informations d’accessibilité. Le tout dans un format d’onglets pour une navigation facile.

* **[Éditeur de règles](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/rule-editor-core-components)**: vous pouvez ajouter une logique et des fonctions dynamiques à vos formulaires sans écrire de code. Vous pouvez utiliser l’éditeur de règles intégré pour :
   * Afficher ou masquer des champs en fonction des choix des utilisateurs
   * Activer ou désactiver un objet
   * Définir une valeur pour un objet
   * Exécution de calculs
   * Définir la propriété d’un objet
   * Validation de la saisie de données
   * Appeler un service (appeler une fonctionnalité externe)
   * Utilisation de fonctions intégrées (fonctions prédéfinies pour les tâches courantes)
   * Utilisation de fonctions personnalisées (votre propre code pour des besoins spécifiques)
   * Validation des champs et des panneaux (assurez-vous que les données répondent aux exigences)
   * Valider la valeur d’un objet
   * Exécuter les fonctions de calcul de la valeur d’un objet
   * Appeler un service de modèle de données de formulaire (FDM) et effectuer une opération
   * Ajouter dynamiquement des styles (modifier l’aspect en fonction de conditions)
   * Créer d’autres règles (actions de chaîne et logique)
   * et plus encore !

  L’éditeur de règles ne dispose pas de l’éditeur de code. Vous pouvez utiliser [fonctions personnalisées](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-and-use-custom-functions) pour ajouter votre propre code en fonction des besoins spécifiques de l’éditeur de règles.



* **Formulaires de préremplissage**: vous pouvez renseigner automatiquement certains champs d’un formulaire avec des données existantes lorsqu’un utilisateur l’ouvre. Cela permet d’économiser du temps et des efforts sur les utilisateurs en éliminant la nécessité de saisir manuellement des informations qui pourraient déjà être disponibles. L’éditeur des composants principaux fournit un service de préremplissage prêt à l’emploi pour remplir les champs de formulaire à l’aide d’un modèle de données de formulaire. Vous pouvez également créer des services de préremplissage personnalisés pour des scénarios plus complexes.

* **[Document d’enregistrement (DE)](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/generate-document-of-record-core-components)**: un document d’enregistrement (DE) fait référence à une représentation formelle et imprimable des données envoyées par le biais du formulaire. Il sert d’enregistrement permanent des informations saisies par un utilisateur, fournissant un instantané des données envoyées dans un format convivial, généralement sous la forme d’un document PDF. Vous pouvez utiliser l’éditeur pour configurer facilement un modèle personnalisé ou utiliser un modèle prêt à l’emploi pour générer un document d’enregistrement.

* **[Modèle de données de formulaire](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/using-form-data-model)**: un modèle de données de Forms adaptatif (FDM) fait office de pont entre votre Forms adaptatif et vos sources de données. Il définit essentiellement la structure et l’organisation des données que vos formulaires collectent et interagissent avec eux. Vous pouvez utiliser l’éditeur pour connecter facilement votre formulaire à un modèle de données Forms (FDM).

* **[Envois de formulaire](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Adaptive%20Form%20Submit%20Action&amp;text=Adobe%20recommends%20using%20Core%20Components,to%20create%20standalone%20Adaptive%20Forms.&amp;text=A%20Submit%20Action%20lets%20you,button%20on%20an%20Adaptive%20Form)**: un envoi de formulaire fait référence au processus de remplissage et d’envoi de formulaires par les utilisateurs. Cela déclenche une série d’actions définies dans la configuration du formulaire, ce qui entraîne le stockage ou le traitement des données envoyées. L’éditeur de Forms adaptatif propose diverses options pour configurer les envois de formulaire. Certaines des actions d’envoi courantes sont les suivantes :

   * [Envoyer un e-mail](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Adaptive%20Form%20Submit%20Action&amp;text=Adobe%20recommends%20using%20Core%20Components,to%20create%20standalone%20Adaptive%20Forms.&amp;text=A%20Submit%20Action%20lets%20you,button%20on%20an%20Adaptive%20Form.)
   * [Appeler un flux d’automatisation de puissance](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/integrate/services/forms-microsoft-power-automate-integration)
   * [Envoyer à SharePoint](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-action-sharepoint)
   * [Appeler une fusion Workfront](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Invoke%20a%20Workfront%20Fusion)
   * [Envoyer à l’aide du modèle de données de formulaire (FDM)](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/using-form-data-model)
   * [Envoyer vers le stockage Azure Blob](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Submit%20to%20Azure%20Blob%20Storage)
   * [Envoyer vers le point d’entrée REST](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-action-restpoint)
   * [Envoyer à OneDrive](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=to%20REST%20endpoint-,Submit%20to%20OneDrive,-Invoke%20an%20AEM)
   * [Appeler un processus AEM](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Invoke%20an%20AEM%20Workflow)


<!-- 
* **Preview Forms**: You can use the editor to  simulates how the form would appear on various devices like desktops, tablets, and smartphones.
-->



## Activation des composants principaux de Forms adaptatif

L’activation des composants principaux des formulaires adaptatifs sur AEM Forms as a Cloud Service vous permet de commencer à créer, à publier et à diffuser des formulaires adaptatif et des formulaires découplés basés sur les composants principaux à l’aide de vos instances Cloud Service d&#39;AEM Forms sur plusieurs canaux. Pour obtenir des instructions détaillées sur l’activation des composants principaux des formulaires adaptatifs, voir [Activer les composants principaux des formulaires adaptatifs sur AEM Forms as a Cloud Service et dans l’environnement de développement as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html?lang=fr).

Les composants principaux des formulaires adaptatifs ont les exigences suivantes.

| Version d’AEM | Module complémentaire AEM Forms | Composants principaux des formulaires adaptatifs |
|---|---|---|
| AEM as a Cloud Service | Forms – Inscription numérique | [Version 2.0.10](version.md)+ |
| AEM 6.5 | Module complémentaire Forms | [Version 1.1.12](version.md)+ |

Si votre version d&#39;AEM Cloud Service est antérieure à 2023.02.0, [assurez-vous que l’indicateur `prerelease` est activé dans votre environnement](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=fr#new-features), car les composants principaux des formulaires adaptatifs faisaient partie de la version préliminaire avant la version 2023.02.0.


## Création d’un formulaire adaptatif basé sur des composants principaux

Vous pouvez effectuer les actions suivantes dans les environnements AEM Forms as a Cloud Service ou AEM 6.5 Forms :

| Action | Version d’AEM Forms |
|--------|------------------|
| Création d’un formulaire adaptatif autonome | [AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=fr) |
| Création d’un formulaire adaptatif dans une page AEM Sites | [AEM 6.5 Forms](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=fr#create-an-adaptive-form-in-sites-editor-or-experience-fragment), [AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=fr#create-an-adaptive-form-in-sites-editor-or-experience-fragment) |
| Création d’un formulaire adaptatif dans un fragment d’expérience AEM | [AEM 6.5 Forms](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=fr#create-an-adaptive-form-in-experience-fragment), [AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=fr#create-an-adaptive-form-in-experience-fragment) |
| Conversion d’un formulaire adaptatif en un fragment d’expérience | [AEM 6.5 Forms](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=fr#convert-an-adaptive-form-in-sites-page-to-an-experience-fragment), [AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=fr#convert-an-adaptive-form-in-sites-page-to-an-experience-fragment) |





<!-- >, such as  [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), to ensure that forms can be used by people with disabilities, including those using assistive technologies such as screen readers.

*   **Alignment with AEM Sites**: The Core Components are designed to be more aligned with AEM Sites, making it easier for Sites users to adopt and use them without having to learn anything new. The components use the same front-end pipeline as Sites, making it easier to style and modify their appearance. 

<!-- Additionally, the following points further illustrate this alignment:

    *   **Authoring experience inline with Page editor**: The Core Components have an authoring experience that is inline with the Sites editor, with dialogs and other experiences similar to the Page editor. This makes it easier for Sites users to create and manage forms within the familiar context of the Sites editor.

    *   **Inline form editing in Sites editor**: The Core Components allow  inline form editing within the Sites editor, avoiding the need to switch back and forth between editors. This streamlines the authoring experience and makes it easier to create and manage forms.

    *   **Inheriting Sites features in Forms**: Forms authored within a Sites page inherit the same features as Sites. This provides a seamless and integrated experience for creating and managing forms within the context of AEM Sites 
    
    <!--including Multi Site Manager, the ability to use Sites components within a form for static content, support for scheduled publish/unpublish, form translation aligned with Sites translation, versioning, and targeting -->

## Voir également {#see-also}

{{see-also}}
