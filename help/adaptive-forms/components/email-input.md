---
title: Composant principal des formulaires adaptatifs - Entrée d’e-mail
description: Utilisation ou personnalisation du composant principal « Entrée d’e-mail » des formulaires adaptatifs.
role: Architect, Developer, Admin, User
exl-id: f6a2974b-991e-4cea-9ef8-0b03e8975eeb
source-git-commit: 0bebc248ee2b708f7677950d90356abd5bc70a98
workflow-type: tm+mt
source-wordcount: '1756'
ht-degree: 100%

---

# Entrée d’e-mail {#Email-input-adaptive-forms-core-component}

Le composant principal « Entrée d’e-mail » des formulaires adaptatifs est utilisé pour collecter les adresses e-mail des utilisateurs et des utilisatrices. Le champ d’entrée d’e-mail permet au navigateur de vérifier que le format de l’adresse e-mail renseignée est valide. Il est généralement représenté sous la forme d’une zone de texte et comporte des validations de motif pour n’accepter que des adresses e-mail valides. Le champ d’entrée d’e-mail peut être personnalisé de manière plus détaillée avec des attributs supplémentaires tels que « obligatoire », « espace réservé » et « motif » pour définir les validations des données de l’entrée.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

Il existe plusieurs raisons d’inclure un composant « Entrée d’e-mail » dans un formulaire adaptatif, notamment :

* **Convivialité** : une entrée d’e-mail permet aux utilisateurs et utilisatrices de saisir plus facilement leurs adresses e-mail, car elle permet d’indiquer clairement les données attendues dans le champ.

* **Communication personnalisée** : la collecte des adresses e-mail des utilisateurs et utilisatrices par le biais d’un formulaire permet une communication personnalisée, comme l’envoi d’e-mails de confirmation ou de newsletters.

* **Génération de piste** : en collectant les adresses e-mail par le biais d’un formulaire, les entreprises peuvent créer leur liste de diffusion et l’utiliser pour la génération de piste.

* **Authentification de l’utilisateur** : les adresses e-mail peuvent être utilisées comme moyen d’authentification pour accéder à des contenus ou services limités.

* **Collecte de commentaires** : une entrée d’e-mail dans un formulaire de commentaire permet à l’entreprise de communiquer avec l’utilisateur ou l’utilisatrice pour le suivi ou la clarification de ses commentaires.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Accordéon des formulaires adaptatifs a été publié en février 2023 au sein des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec la <br>[version 2.0.4](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible avec les<br>[versions 1.1.12](/help/adaptive-forms/version.md) à 2.0.0 exclue. |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Retrouvez les informations les plus récentes sur le composant principal « Entrée d’e-mail » des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/emailinput/v1/emailinput). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience d’entrée d’e-mail pour les visiteurs et les visiteuses à l’aide de la boîte de dialogue Configurer. Vous pouvez également définir facilement des options d’entrée d’e-mail pour une expérience utilisateur fluide.

### Onglet De base {#basic-tab}

![Onglet De base](/help/adaptive-forms/assets/email_basictab.png)

* **Nom** - Le nom identifie de manière unique le composant dans l’éditeur de règles. Les caractères spéciaux et les espaces ne sont pas autorisés dans les chaînes de nom.

* **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

* **Masquer le titre** - Sélectionnez cette option pour masquer le titre du composant.

* **Texte d’espace réservé** - Le texte d’espace réservé dans un composant de formulaire fait référence à un libellé court ou à une invite qui apparaît dans un champ de saisie comme conseil à l’utilisateur ou à l’utilisatrice sur le type d’information à saisir dans ce champ. Le texte d’espace réservé disparaît lorsque l’utilisateur ou l’utilisatrice commence à saisir du texte dans le champ et réapparaît si le champ est vide. Il fournit un indice visuel à l’utilisateur ou à l’utilisatrice, mais n’agit pas comme une valeur ou un libellé permanent pour le champ.

* **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.
* **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.
* **Désactiver le composant** - Sélectionnez cette option pour désactiver le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.
* **Lecture seule** - Sélectionnez cette option pour rendre le composant non modifiable. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

* **Valeur par défaut** - Cette option vous permet d’ajouter une valeur par défaut dans un champ de formulaire. Si **Composant désactivé** ou **Composant en lecture seule** est sélectionné, la valeur par défaut s’affiche à l’écran. Si aucune valeur n’est saisie par l’utilisateur ou l’utilisatrice dans le champ de formulaire, cette valeur est envoyée au moment de l’envoi du formulaire.


### Onglet Validation {#validation-tab}

![Onglet Validation](/help/adaptive-forms/assets/email_validationtab.png)

* **Obligatoire** : Sélectionnez cette option si vous souhaitez afficher le composant dans un formulaire adaptatif. Vous ne pouvez pas sélectionner **Masquer le composant** ou **Désactiver le composant**  dans l’onglet **De base** lorsque cette option est sélectionnée.

* **Message d’erreur** : Cette option vous permet de saisir un message qui s’affiche si la case à cocher **Obligatoire** est cochée et que le champ de formulaire reste vide.

* **Message de validation de script** - Cette option permet de saisir un message à afficher en cas d’échec de la validation du script.

* **Nombre maximal de caractères** - Cette option permet de spécifier le nombre maximal de caractères autorisés dans le champ. Si vous saisissez un nombre de caractères supérieur à la valeur spécifiée dans **Nombre maximal de caractères**, un message d’erreur s’affiche à l’écran. La boîte de dialogue **Message d’erreur du nombre de caractères maximum** vous permet d’ajouter un message d’erreur personnalisé.

* **Message d’erreur du nombre de caractères maximum** - La boîte de dialogue **Message d’erreur du nombre de caractères maximum** vous permet d’ajouter un message d’erreur personnalisé si vous saisissez un nombre de caractères supérieur à la valeur spécifiée dans l’option **Nombre maximal de caractères**.

* **Nombre minimum de caractères** - Cette option permet de spécifier le nombre minimum de caractères autorisés dans le champ. Si vous saisissez un nombre de caractères inférieur à la valeur spécifiée dans **Nombre minimum de caractères**, un message d’erreur s’affiche à l’écran. La boîte de dialogue **Message d’erreur du nombre de caractères minimum** vous permet d’ajouter un message d’erreur personnalisé.

* **Message d’erreur du nombre de caractères minimum** - La boîte de dialogue **Message d’erreur du nombre de caractères minimum** vous permet d’ajouter un message d’erreur personnalisé si vous saisissez un nombre de caractères inférieur à la valeur spécifiée dans l’option **Nombre minimum de caractères**.
<br>

    L’option **Motif de validation** vous permet de saisir un motif pour valider l’ID d’e-mail saisi. Si la validation de l’ID d’e-mail échoue avec la valeur saisie dans l’option **Motif**, le message d’erreur s’affiche à l’écran.
    * **Motif** - Cette option vous permet de saisir les motifs de vérification autorisés pour les e-mails. Les expressions régulières sont également autorisées.
    * **Message d’erreur** - Cette option permet de saisir un message qui s’affiche à l’écran si la validation de l’ID d’e-mail échoue avec la valeur saisie dans l’option **Motif**

### Onglet Contenu de l’aide {#help-content-tab}

![Onglet Contenu d’aide](/help/adaptive-forms/assets/email_helptab.png)

* **Description courte** : Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez l’option **Toujours afficher une description courte** pour l’afficher sous le composant.

* **Toujours afficher une description courte** - Activez cette option pour afficher la description courte sous le composant.

* **Texte d’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility-tab}

![Onglet Accessibilité](/help/adaptive-forms/assets/email_accessibilitytab.png)

**Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS pour le composant « Entrée d’e-mail ».

### Onglet Styles {#styles-tab}

Cet onglet vous permet de définir et de gérer les styles CSS d’un composant. Le composant principal « Entrée d’e-mail » des formulaires adaptatifs prend en charge le [Système de style](/help/get-started/authoring.md#component-styling) d’AEM.

![Onglet Styles.](/help/adaptive-forms/assets/email_designdialog.png)

* **Classes CSS par défaut** : vous pouvez fournir une classe CSS par défaut pour le composant principal « Entrée d’e-mail » des formulaires adaptatifs.

* **Styles autorisés** : vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé « texte en gras » et fournir la classe CSS « police d’épaisseur : gras ». Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de formulaires adaptatifs. Pour appliquer un style, sélectionnez le composant auquel vous souhaitez appliquer le style dans l’éditeur de formulaires adaptatifs, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans la liste déroulante **Styles**. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

### Onglet Formats {#format-tab}

L’onglet Formats vous permet de définir des formats de date par défaut et personnalisés.

![Onglet Conception.](/help/adaptive-forms/assets/emailinput_designformattab.png)

## Article connexe {#related-article}

* [Création d’un formulaire adaptatif dans une page AEM Sites ou un fragment d’expérience](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=fr)

* [Création d’un formulaire adaptatif autonome](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=fr)

>[!MORELIKETHIS]
>
>* [Accordéon](/help/adaptive-forms/components/accordion.md)
>* [Bouton](/help/adaptive-forms/components/button.md)
>* [Groupe de cases à cocher](/help/adaptive-forms/components/checkbox-group.md)
>* [Sélecteur de date](/help/adaptive-forms/components/date-picker.md)
>* [Liste déroulante](/help/adaptive-forms/components/drop-down.md)
>* [Conteneur de formulaires](/help/adaptive-forms/components/form-container.md)
>* [Pièce jointe](/help/adaptive-forms/components/file-attachment.md)
>* [Pied de page](/help/adaptive-forms/components/footer.md)
>* [En-tête](/help/adaptive-forms/components/header.md)
>* [Onglets horizontaux](/help/adaptive-forms/components/horizontal-tabs.md)
>* [Image](/help/adaptive-forms/components/image.md)
>* [Entrée de nombre](/help/adaptive-forms/components/number-input.md)
>* [Conteneur de panneau](/help/adaptive-forms/components/panel-container.md)
>* [Bouton radio](/help/adaptive-forms/components/radio-button.md)
>* [Bouton de réinitialisation](/help/adaptive-forms/components/reset-button.md)
>* [Bouton Envoyer](/help/adaptive-forms/components/submit-button.md)
>* [Entrée téléphonique](/help/adaptive-forms/components/telephone-input.md)
>* [Entrée de texte](/help/adaptive-forms/components/text-input.md)
>* [Texte](/help/adaptive-forms/components/text.md)
>* [Titre](/help/adaptive-forms/components/title.md)
>* [Assistant](/help/adaptive-forms/components/wizard.md)

## Voir également {#see-also}

{{see-also}}