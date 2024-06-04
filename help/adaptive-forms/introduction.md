---
title: Présentation des composants principaux des formulaires adaptatifs AEM
description: Créez des expériences d’inscription attrayantes (formulaires) grâce à la flexibilité des composants principaux des formulaires adaptatifs et diffusez-les avec la puissance d’Adobe Experience Manager.
role: Architect, Developer, Admin, User
source-git-commit: e1ee09854a40c960f8a907149240b755c95fe176
workflow-type: tm+mt
source-wordcount: '2229'
ht-degree: 99%

---

# Composants principaux des formulaires adaptatifs  {#adaptive-forms-core-components-introduction}

À l’aide des composants principaux des formulaires adaptatifs dans Adobe Experience Manager, vous pouvez créer des expériences d’inscription attrayantes.

## Composants principaux {#overview}

Dans Adobe Experience Manager (AEM), les composants sont les blocs de création utilisés pour créer des pages et des formulaires. Ils offrent aux créateurs et aux créatrices un moyen simple et puissant de créer et de gérer du contenu, tout en offrant aux développeurs et aux développeuses la flexibilité et l’extensibilité nécessaires à la création de composants personnalisés. Ils sont conçus pour accélérer le développement et réduire les coûts de maintenance des sites Web et des formulaires, être flexibles et peuvent être facilement personnalisés en fonction des besoins spécifiques d’un site Web ou d’un formulaire.

Les composants principaux sont également conçus pour être réactifs et prendre en charge un large éventail d’appareils, notamment les ordinateurs, les tablettes et les smartphones. Ils se conforment également aux dernières normes et bonnes pratiques Web, ce qui en fait une solution robuste et fiable pour créer du contenu Web.

Dans l’ensemble, les composants principaux sont un outil essentiel pour la création et la gestion de contenu Web dans AEM. Ils offrent une solution puissante et flexible qui peut contribuer à réduire le temps de développement et les coûts de maintenance, tout en offrant une expérience utilisateur optimale aux visiteurs et visiteuses du site Web.

## Composants principaux des formulaires adaptatifs

Les composants principaux des fomulaires adaptatifs sont un ensemble de 29 composants open source conformes à BEM qui sont construits sur la base des composants principaux de la gestion de contenu web d’Adobe Experience Manager. Ils sont spécialement conçus pour créer des formulaires adaptatifs, qui sont des formulaires qui s’adaptent au périphérique, au navigateur et à la taille d’écran de l’utilisateur ou de l’utilisatrice.

Ces composants peuvent être utilisés pour créer des expériences de capture de données et d’inscription exceptionnelles en proposant un large éventail d’options de champ de formulaire, notamment des champs de texte, des cases à cocher, des menus déroulants, etc. Ils comprennent également des fonctionnalités telles que la validation, la logique conditionnelle et la conception réactive, qui peuvent être utilisées pour créer des formulaires conviviaux et simples.

En outre, comme ces composants sont en open source, les développeurs et les développeuses peuvent facilement les personnaliser et les étendre pour répondre aux besoins spécifiques de leur entreprise. De plus, ces composants sont construits sur une méthodologie BEM qui garantit leur évolutivité et leur maintenance.

![image de formulaire adaptatif](assets/sample-adaptive-form.png)

## Fonctions {#features}

|  |  |
|---|---|
| Prêts pour la production | Les composants principaux des formulaires adaptatifs sont 24 composants robustes de gestion de contenu web. |
| Prêts pour le cloud | Disponibles pour [AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/home.html?lang=fr). |
| Polyvalents | Les composants représentent des concepts génériques avec lesquels les créateurs et créatrices peuvent assembler pratiquement n’importe quelle disposition. |
| Configurables | Des [politiques de contenu](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html?lang=fr#content-policies) au niveau du modèle définissent les fonctionnalités que les créateurs et créatrices de pages peuvent ou non utiliser. |
| Accessibles | Elles fournissent des libellés ARIA et prennent en charge la navigation au clavier et le texte pour les technologies d’assistance telles que les lecteurs d’écran. |
| Thème utilisable | Les composants implémentent le [système de style](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=fr) et le balisage suit les [conventions CSS BEM](https://getbem.com/). |
| Personnalisables | Plusieurs modèles permettent une personnalisation facile, depuis l’ajustement du code HTML jusqu’à la réutilisation des fonctionnalités avancées. |
| Contrôle de version | La [politique de contrôle de version](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) garantit que les composants principaux ne rendent pas votre site inopérable lorsqu’ils améliorent des éléments susceptibles de vous affecter. |
| Open source | Si quelque chose ne fonctionne pas correctement, contribuez en apportant vos améliorations. |

<!-- comply with [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), -->


## Avantages {#benefits}

Les expériences de capture de données sont essentielles pour la génération de pistes et l’inscription. Les composants principaux des formulaires adaptatifs offrent une solution puissante pour créer des formulaires optimisés pour la capture de données. Voici quelques raisons d’utiliser les composants principaux pour créer ces expériences sur les composants de base :

* **[Disponibilité sur GitHub](https://github.com/adobe/aem-core-forms-components)** : les composants principaux des formulaires adaptatifs d’AEM sont en open source et disponibles sur GitHub, avec une documentation complète. Cela permet aux développeurs et aux développeuses de comprendre plus facilement les composants et leur fonctionnement, ainsi que de contribuer à leur développement. Le site Web [aemcomponents.dev](https://www.aemcomponents.dev/) est également une ressource précieuse, où les développeurs et les développeuses peuvent voir les composants en action et accéder à la documentation détaillée.

* **[Modèle BEM pour le style](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components)** : les composants principaux suivent le modèle BEM (Block Element Modifier) pour le style, qui est une méthodologie bien établie et largement utilisée pour organiser le CSS. Cela permet aux développeurs et aux développeuses de comprendre plus facilement comment les styles sont organisés et comment les modifier en fonction de leurs besoins spécifiques.

* **Aucune dépendance aux bibliothèques tierces** : l’un des avantages des composants principaux est qu’ils ne dépendent pas des bibliothèques JavaScript tierces, y compris JQuery et Underscore. Les composants sont ainsi plus rapides et plus légers, et plus faciles à intégrer dans une implémentation AEM existante.

* **Centrés sur les performances et l’accessibilité** : les composants principaux sont conçus en tenant compte des performances et de l’accessibilité, qui se reflètent dans leurs scores Google Lighthouse élevés et dans leurs scores Web vitaux. Cela facilite la création de pages Web accessibles et performantes pour les développeurs et les développeuses, ce qui est de plus en plus important dans le paysage numérique actuel.

* **Composants de formulaire dans le modèle et les thèmes Sites 30** : les composants principaux prennent en charge les composants de formulaire dans le modèle et les thèmes Sites 30, ce qui facilite la création et la personnalisation de formulaires dans AEM.

* **[Style plus facile](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components)** : les composants principaux sont plus faciles à mettre en forme que leurs composants de base homologues. Le processus de création du thème est similaire à Sites, avec la possibilité d’hériter du même thème/CSS de la page Sites parente. En outre, le modèle BEM pour le style facilite la compréhension et la modification des styles.

* **Accessibilité** : les composants principaux des formulaires adaptatifs prennent en charge les normes et directives d’accessibilité afin de s’assurer que les formulaires peuvent être utilisés par les personnes présentant un handicap, y compris celles qui utilisent des technologies d’assistance telles que les lecteurs d’écran.

* **[Contrôle des versions](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/add-comments-annotations-versioning-adaptive-form-core-components)** : vous pouvez créer et gérer plusieurs versions de formulaires adaptatifs basés sur des composants principaux, participer à des discussions collaboratives via des commentaires et joindre des annotations à des composants de formulaire spécifiques, améliorant ainsi l’expérience globale de création de formulaires.

## Composants disponibles : répartition par type de composant

La version actuelle d’AEM Forms comporte les composants principaux suivants : [Composants de base](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/create-an-adaptive-form-on-forms-cs/introduction-forms-authoring#component-toolbar) et [Composants de bloc de formulaire (Edge Delivery Services)](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/edge-delivery/build-forms/forms-references/form-components).

| Composants | Composants de base | Composants principaux | Composants de bloc de formulaire | Informations complémentaires |
|------------|:---------------------:|:---------------:|:---------------------:|-----------------------|
| Bloc Adobe Sign | ✔️ | | | [L’intégration d’Adobe Sign](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/integrate/services/adobe-sign-integration-adaptive-forms#adobe-acrobat-sign-for-government) est disponible uniquement pour les composants de base. |
| Accordéon | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/accordion.md)</span> | | Pour les composants de base, vous pouvez configurer la mise en page en accordéon dans les [propriétés des composants du panneau](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout). |
| Fragment de formulaire adaptatif | ✔️ | ✔️ | | Pour les composants de base, vous pouvez [ajouter un fragment](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/forms/adaptive-forms-basic-authoring/adaptive-form-fragments#insert-a-fragment-in-an-adaptive-form) à partir de l’explorateur de ressources. |
| reCAPTCHA du formulaire adaptatif | ✔️ | ✔️ | ✔️ | Pour les composants de base, utilisez le composant Captcha pour [ajouter Google reCaptcha à un formulaire](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/captcha-adaptive-forms#google-reCAPTCHA). |
| Bouton | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/button.md)</span> | ✔️ | |
| CAPTCHA | ✔️ |  |  | Pour les composants de base, utilisez le composant Captcha pour [ajouter Google reCaptcha à un formulaire](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/captcha-adaptive-forms#google-reCAPTCHA). |
| Graphique | ✔️ | | | |
| Case à cocher | ✔️ | ✔️ | | |
| Groupe de cases à cocher | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/checkbox-group.md)</span> | ✔️ | Pour les composants de base, utilisez le composant de case à cocher pour ajouter plusieurs cases à cocher. |
| Champ de saisie de date | ✔️ | | | Pour les composants principaux, utilisez le composant [Sélecteur de date](/help/adaptive-forms/components/date-picker.md). Vous pouvez également ajouter des composants [zone de texte](/help/adaptive-forms/components/text-box.md) ou [champ numérique](/help/adaptive-forms/components/numeric-box.md) distincts pour saisir le jour, le mois et l’année. |
| Sélecteur de date | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/date-picker.md)</span> | ✔️ | |
| Liste déroulante | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/drop-down-list.md)</span> | ✔️ | |
| E-mail | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/email.md)</span> | ✔️ | |
| Pièce jointe | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/file-attachment.md)</span> | ✔️ | |
| Liste des pièces jointes | ✔️ | | | |
| Pied de page | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/footer.md)</span> | ✔️ | |
| Espace réservé de note de bas de page | ✔️ | | | |
| Conteneur de formulaires | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/form-container.md)</span> | ✔️ | Pour les composants de base, utilisez le [composant de panneau racine](https://experienceleague.adobe.com/fr/docs/experience-manager-learn/cloud-service/forms/create-first-af/configure-root-panel). |
| Titre du formulaire | ✔️ | ✔️ | | Pour les composants de base, utilisez le composant de titre. |
| hCaptcha | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/hcaptcha.md)</span> |  | |
| En-tête | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/header.md)</span> | ✔️ | |
| Onglets horizontaux | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/horizontal-tabs.md)</span> | | Pour les composants de base, vous pouvez configurer la [disposition des onglets en haut (onglets horizontaux)](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout) dans les propriétés des composants du panneau. |
| Image | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/image.md)</span> | ✔️ | |
| Choix d’image | ✔️ | | | |
| Bouton Suivant | ✔️ | ✔️ | | Utilisez le [composant « Assistant »](/help/adaptive-forms/components/wizard.md) pour les boutons suivant et précédent afin de basculer entre plusieurs panneaux. |
| Zone numérique | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/numeric-box.md)</span> | ✔️ | |
| Procédure pas à pas numérique | ✔️ | | | |
| Panneau | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/panel.md)</span> | ✔️ | |
| Zone de mot de passe | ✔️ | | ✔️ | |
| Téléphone | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/phone.md)</span> | ✔️ | |
| Bouton Précédent | ✔️ | | | Utilisez le [composant « Assistant »](/help/adaptive-forms/components/wizard.md) pour les boutons suivant et précédent afin de basculer entre plusieurs panneaux. |
| Bouton radio | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/radio-button.md)</span> | | |
| Groupe de boutons radio | | | ✔️ | |
| Bouton de réinitialisation | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/reset-button.md)</span> | ✔️ | |
| Signature tactile | ✔️ | | | |
| Séparateur | ✔️ | | | |
| Bouton Envoyer | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/submit-button.md)</span> | ✔️ | |
| Étape de résumé | ✔️ | | | |
| Basculer | ✔️ | <span style="color:blue"> [✔️](/help/adaptive-forms/components/adaptive-form-switch.md) | | |
| Tableau | ✔️ | | | |
| Conditions générales | ✔️ | ✔️ | | |
| Texte | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/text.md)</span> | ✔️ | |
| Zone de texte | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/text-box.md)</span> | ✔️ | |
| Titre | ✔️ | | | Pour les composants principaux, utilisez le composant [Titre du formulaire](/help/adaptive-forms/components/form-title.md). |
| Captcha Turnstile | ✔️ | | | [Captcha Turnstile](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile) est disponible uniquement pour les composants de base. |
| Onglets verticaux | ✔️ | ✔️ | | Pour les composants de base, vous pouvez configurer la [disposition des onglets à gauche (onglets verticaux)](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout) dans les propriétés des composants du panneau. |
| Assistant | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/wizard.md)</span> | ✔️ | Pour les composants de base, vous pouvez configurer la [disposition de l’assistant](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout) dans les propriétés des composants du panneau. |




>[!NOTE]
>
>
> * En plus des composants répertoriés ci-dessus, le bloc de formulaires prend en charge tous les [types d’entrée HTML5](https://developer.mozilla.org/fr-fr/docs/Web/HTML/Element/input#input_types) et [zones de texte](https://developer.mozilla.org/fr-fr/docs/Web/HTML/Element/textarea) valides en tant que composants.
> * Besoin d’un composant non répertorié ci-dessus ? Envoyez une demande par e-mail à aem-forms-ea@adobe.com depuis votre adresse officielle.


<!-- >
* [Accordion](/help/adaptive-forms/components/accordion.md)
* [Adaptive Form Fragment](/help/adaptive-forms/components/adaptive-form-fragment.md)
* [Adaptive Form Switch](/help/adaptive-forms/components/adaptive-form-switch.md)
* [Button](/help/adaptive-forms/components/button.md)
* [Check Box Group](/help/adaptive-forms/components/checkbox-group.md)
* [Date Picker](/help/adaptive-forms/components/date-picker.md)
* [Drop-down list](/help/adaptive-forms/components/drop-down-list.md)
* [Email](/help/adaptive-forms/components/email.md)
* [Form Container](/help/adaptive-forms/components/form-container.md)
* [File Attachment](/help/adaptive-forms/components/file-attachment.md)
* [Footer](/help/adaptive-forms/components/footer.md)
* [Header](/help/adaptive-forms/components/header.md)
* [Horizontal Tabs](/help/adaptive-forms/components/horizontal-tabs.md)
* [Image](/help/adaptive-forms/components/image.md)
* [Numeric Box](/help/adaptive-forms/components/numeric-box.md)
* [Panel](/help/adaptive-forms/components/panel.md)
* [Phone](/help/adaptive-forms/components/phone.md)
* [Radio Button](/help/adaptive-forms/components/radio-button.md)
* [Adaptive Form reCAPTCHA](/help/adaptive-forms/components/adaptive-form-recaptcha.md)
* [Reset Button](/help/adaptive-forms/components/reset-button.md)
* [Submit Button](/help/adaptive-forms/components/submit-button.md)
* [Text Box](/help/adaptive-forms/components/text-box.md)
* [Text](/help/adaptive-forms/components/text.md)
* [Form Title](/help/adaptive-forms/components/form-title.md)
* [Wizard](/help/adaptive-forms/components/wizard.md)

-->

## Éditeur de formulaires facile à utiliser

L’éditeur de formulaires adaptatifs basés sur les composants principaux est similaire à celui que vous utilisez déjà pour créer des pages AEM Sites. Voici ce dont vous bénéficiez :


* **Éléments et paramètres habituels de l’interface d’utilisation** : lors de la configuration des propriétés des composants de formulaire, la boîte de dialogue des propriétés ressemble à celle que vous utilisez pour les composants principaux de gestion de contenu web. Cela permet de trouver plus rapidement les options dont vous avez besoin. Comme les composants principaux de gestion de contenu web, pour les composants de formulaire, la boîte de dialogue des propriétés apparaît au centre de l’éditeur avec des onglets clairs séparant les options de base et avancées, le texte d’aide et les informations d’accessibilité, le tout sous forme d’onglets pour une navigation facile.

* **[Éditeur de règles](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/rule-editor-core-components)** : vous pouvez ajouter des fonctionnalités logiques et dynamiques à vos formulaires sans écrire de code. Vous pouvez utiliser l’éditeur de règles intégré pour :
   * afficher ou masquer les champs en fonction des choix de l’utilisateur ou de l’utilisatrice ;
   * Activer ou désactiver un objet
   * Définir une valeur pour un objet
   * effectuer des calculs ;
   * définir la propriété d’un objet ;
   * valider la saisie des données ;
   * invoquer un service (appeler une fonctionnalité externe) ;
   * utiliser des fonctions intégrées (fonctions prédéfinies pour les tâches courantes) ;
   * utiliser des fonctions personnalisées (votre propre code pour des besoins spécifiques) ;
   * valider les champs et les panneaux (s’assurer que les données répondent aux exigences) ;
   * Valider la valeur d’un objet
   * Exécuter les fonctions de calcul de la valeur d’un objet
   * appeler un service de modèle de données de formulaire (FDM) et exécuter une opération ;
   * ajouter dynamiquement des styles (modifier l’apparence en fonction des conditions) ;
   * créer d’autres règles (actions en chaîne et logique) ;
   * et plus encore !

  L’éditeur de règles n’a pas d’éditeur de code. Vous pouvez utiliser des [fonctions personnalisées](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-and-use-custom-functions) pour ajouter votre propre code pour des besoins spécifiques à l’éditeur de règles.



* **Formulaires à pré-remplir** : vous pouvez remplir automatiquement certains champs d’un formulaire avec des données existantes lorsqu’il est ouvert. Les utilisateurs et utilisatrices peuvent remplir le formulaire plus rapidement et facilement sans avoir besoin de saisir manuellement des informations qui pourraient déjà être disponibles. L’éditeur de composants principaux fournit un service de pré-remplissage prêt à l’emploi pour remplir les champs du formulaire à l’aide d’un modèle de données de formulaire. Vous pouvez également créer des services de pré-remplissage personnalisés pour des scénarios plus complexes.

* **[Document d’enregistrement (DoR)](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/generate-document-of-record-core-components)** : un document d’enregistrement fait référence à une représentation formelle et imprimable des données soumises via le formulaire. Il sert d’enregistrement permanent des informations saisies par un utilisateur ou une utilisatrice, fournissant un instantané des données soumises dans un format convivial, généralement un document PDF. Vous pouvez utiliser l’éditeur pour configurer facilement un modèle personnalisé ou utiliser un modèle prêt à l’emploi pour générer un DoR.

* **[Modèle de données de formulaire](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/using-form-data-model)** : un modèle de données de formulaires adaptatifs (FDM) agit comme un pont entre vos formulaires adaptatifs et vos sources de données. Il définit essentiellement la structure et l’organisation des données que vos formulaires collectent et avec lesquelles ils interagissent. Vous pouvez utiliser l’éditeur pour connecter facilement votre formulaire à un modèle de données de formulaires (FDM).

* **[Envois de formulaires](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Adaptive%20Form%20Submit%20Action&amp;text=Adobe%20recommends%20using%20Core%20Components,to%20create%20standalone%20Adaptive%20Forms.&amp;text=A%20Submit%20Action%20lets%20you,button%20on%20an%20Adaptive%20Form)** : l’envoi d’un formulaire fait référence au processus par lequel les utilisateurs et utilisatrices remplissent et envoient leurs formulaires remplis. Cela déclenche une série d’actions définies dans la configuration du formulaire, conduisant finalement au stockage ou au traitement des données soumises. L’éditeur de formulaires adaptatifs offre une variété d’options pour configurer les envois de formulaires. Voici certaines des actions d’envoi courantes :

   * [Envoyer un e-mail](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Adaptive%20Form%20Submit%20Action&amp;text=Adobe%20recommends%20using%20Core%20Components,to%20create%20standalone%20Adaptive%20Forms.&amp;text=A%20Submit%20Action%20lets%20you,button%20on%20an%20Adaptive%20Form.)
   * [Appeler un flux Power Automate](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/integrate/services/forms-microsoft-power-automate-integration)
   * [Envoyer à SharePoint](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-action-sharepoint)
   * [Invoquer Workfront Fusion](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Invoke%20a%20Workfront%20Fusion)
   * [Envoyer à l’aide du modèle de données de formulaire](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/using-form-data-model)
   * [Envoyer au stockage Blob Azure](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Submit%20to%20Azure%20Blob%20Storage)
   * [Envoyer vers le point d’entrée REST](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-action-restpoint)
   * [Envoyer à OneDrive](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=to%20REST%20endpoint-,Submit%20to%20OneDrive,-Invoke%20an%20AEM)
   * [Appeler un processus AEM](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Invoke%20an%20AEM%20Workflow)


* [Composants principaux des formulaires adaptatifs dans l’éditeur de pages de Sites](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page) : vous pouvez activer et utiliser les composants de base des formulaires adaptatifs dans l’éditeur de pages AEM et les fragments d’expérience AEM pour créer directement une expérience de capture de données en même temps que la construction d’une page Sites.

  >[!VIDEO](https://video.tv.adobe.com/v/3419284?quality=12&learn=on)


<!-- 
* **Preview Forms**: You can use the editor to  simulates how the form would appear on various devices like desktops, tablets, and smartphones.
-->



## Activer les composants principaux des formulaires adaptatifs

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
