---
title: Composant principal des formulaires adaptatifs - Entrée de texte (zone de texte)
description: Utilisation ou personnalisation du composant principal « Entrée de texte » des formulaires adaptatifs.
role: Architect, Developer, Admin, User
exl-id: 49d9fe69-0578-4489-beaa-a18cdb14add7
source-git-commit: 7888cfa0f1358ce8018fc1e3cc3b19eb66a82b9d
workflow-type: ht
source-wordcount: '1786'
ht-degree: 100%

---

# Entrée de texte (zone de texte) {#text-input-adaptive-forms-core-component}

Un composant d’entrée de texte (zone de texte) permet à l’utilisateur ou à l’utilisatrice de saisir et de modifier une ou plusieurs lignes de texte, selon l’attribut type de l’élément d’entrée. Le composant « Entrée de texte » peut être placé dans un formulaire et est généralement étiqueté avec un texte utile qui identifie facilement son objectif. C’est un élément fondamental de tout formulaire, largement utilisé pour collecter différents types de données auprès des utilisateurs et des utilisatrices. Ces éléments sont simples, flexibles, et peuvent être configurés pour valider les entrées et améliorer la précision de la collecte de données.


**Exemple**

![](/help/adaptive-forms/assets/text-input.png)


## Utilisation {#reasons-to-use-text-input-field}

Il existe plusieurs raisons d’inclure un composant « Entrée de texte » dans un formulaire adaptatif :

* **Collecte de données** : les champs de saisie de texte sont l’un des éléments de formulaire les plus courants pour collecter un large éventail d’informations auprès des utilisateurs et des utilisatrices, tels que les noms, adresses e-mails, numéros de téléphone et autres types de données textuelles.

* **Facilité d’utilisation** : les champs d’entrée de texte sont simples et faciles à utiliser, ce qui permet aux utilisateurs et aux utilisatrices de saisir et de modifier facilement du texte.

* **Flexibilité** : les champs d’entrée de texte peuvent être utilisés pour collecter un large éventail d’informations, des entrées de texte courtes sur une seule ligne aux entrées de texte plus longues sur plusieurs lignes.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Accordéon des formulaires adaptatifs a été publié en février 2023 au sein des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec la <br>[version 2.0.4](/help/adaptive-forms/version.md) et les versions ultérieures | Compatible avec les<br>[versions 1.1.12](/help/adaptive-forms/version.md) à 2.0.0 exclue. |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Retrouvez les informations les plus récentes sur le composant principal « Onglet en haut » des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience d’entrée de texte pour les visiteurs et les visiteuses en utilisant la boîte de dialogue Configurer. Vous pouvez également définir facilement des options d’entrée de texte pour une expérience utilisateur fluide.

![Onglet De base](/help/adaptive-forms/assets/textinput_basictab.png)

* **Nom** - Vous pouvez identifier facilement un composant de formulaire avec son nom unique aussi bien dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

* **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

* **Masquer le titre** - Sélectionnez cette option pour masquer le titre du composant.

* **Texte d’espace réservé** - Le texte d’espace réservé dans un composant de formulaire fait référence à un libellé court ou à une invite qui apparaît dans un champ de saisie comme conseil à l’utilisateur ou à l’utilisatrice sur le type d’information à saisir dans ce champ. Le texte d’espace réservé disparaît lorsque l’utilisateur ou l’utilisatrice commence à saisir du texte dans le champ et réapparaît si le champ est vide. Il fournit un indice visuel à l’utilisateur ou à l’utilisatrice, mais n’agit pas comme une valeur ou un libellé permanent pour le champ.

* **Référence Bind** - Une référence Bind est une référence à un élément de données stockée dans une source de données externe et utilisée dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client ou d’une cliente dans un formulaire, en fonction de l’identifiant du client ou de la cliente saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur fluide pour la collecte et la gestion des données.

* **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.

* **Désactiver le composant** - Sélectionnez cette option pour désactiver le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

* **Lecture seule** - Sélectionnez cette option pour rendre le composant non modifiable. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

* **Valeur par défaut** - Cette option vous permet d’ajouter une valeur par défaut dans un champ de formulaire. Le texte disparaît lorsque l’utilisateur ou l’utilisatrice commence à saisir du texte dans le champ. Si **Composant désactivé** ou **Composant en lecture seule** est sélectionné, la valeur par défaut s’affiche à l’écran. Si aucune valeur n’est saisie par l’utilisateur dans le champ de formulaire, cette valeur est envoyée au moment de l’envoi du formulaire.

* **Permettre des lignes multiples** - Cette option permet à l’utilisateur ou à l’utilisatrice de saisir plusieurs lignes dans un champ de formulaire.

* **Autoriser le texte enrichi** - La boîte de dialogue de modification fournit des outils de mise en forme de texte enrichi standard qui permettent à l’utilisateur ou à l’utilisatrice de mettre en forme le texte.

* **Attribut de remplissage automatique** - L’option de remplissage automatique remplit le champ de formulaire selon un motif ou un texte saisi précédemment. Lorsque du texte est saisi dans le champ de formulaire, les suggestions s’affichent dans une liste déroulante à partir de laquelle l’option appropriée peut être sélectionnée.

### Onglet Validation {#validation-tab}

![Onglet Validation](/help/adaptive-forms/assets/textinput_validationtab.png)

* **Obligatoire** : Sélectionnez cette option si vous souhaitez afficher le composant dans un formulaire adaptatif. Vous ne pouvez pas sélectionner **Masquer le composant** ou **Désactiver le composant**  dans l’onglet **De base** lorsque cette option est sélectionnée.

* **Message d’erreur** - Cette option vous permet de saisir un message qui s’affiche si la case à cocher **Obligatoire** est cochée et que le champ n’est pas renseigné.

* **Message de validation de script** - Cette option permet de saisir un message à afficher en cas d’échec de la validation du script.

* **Nombre maximal de caractères** - Cette option vous permet de spécifier le nombre maximal de caractères autorisés dans le composant. Si vous saisissez un nombre de caractères supérieur à la valeur spécifiée dans **Nombre maximal de caractères**, un message d’erreur s’affiche à l’écran. La boîte de dialogue **Message d’erreur du nombre de caractères maximum** vous permet d’ajouter un message d’erreur personnalisé.

* **Message d’erreur du nombre de caractères maximum** - La boîte de dialogue **Message d’erreur du nombre de caractères maximum** vous permet d’ajouter un message d’erreur personnalisé si vous saisissez un nombre de caractères supérieur à la valeur spécifiée dans l’option **Nombre maximal de caractères**.

* **Nombre minimum de caractères** - Cette option permet de spécifier le nombre minimum de caractères autorisés dans le champ. Si vous saisissez un nombre de caractères inférieur à la valeur spécifiée dans **Nombre minimum de caractères**, un message d’erreur s’affiche à l’écran. La boîte de dialogue **Message d’erreur du nombre de caractères minimum** vous permet d’ajouter un message d’erreur personnalisé.

* **Message d’erreur du nombre de caractères minimum** - La boîte de dialogue **Message d’erreur du nombre de caractères minimum** vous permet d’ajouter un message d’erreur personnalisé si vous saisissez un nombre de caractères inférieur à la valeur spécifiée dans l’option **Nombre minimum de caractères**.

L’option **Motif de validation** vous permet de saisir un motif pour valider le texte saisi. Si la validation du texte échoue avec la valeur saisie dans **Motif**, le message d’erreur s’affiche à l’écran.

* **Motif** - Cette option vous permet de saisir les motifs de vérification autorisés pour le texte. Les expressions régulières sont également autorisées.

* **Message d’erreur** - Cette option permet de saisir un message qui s’affiche à l’écran si la validation du texte saisi échoue avec la valeur saisie dans l’option **Motif**.

### Onglet Contenu de l’aide {#help-content-tab}

![Onglet Contenu d’aide](/help/adaptive-forms/assets/textinput_helptab.png)

* **Description courte** : Une description courte est une brève explication textuelle qui fournit des informations supplémentaires ou une clarification sur l’objectif d’un champ de formulaire spécifique. Il permet à l’utilisateur ou l’utilisatrice de comprendre le type de données à saisir dans le champ et peut fournir des conseils ou des exemples pour s’assurer que les informations saisies sont valides et répondent aux critères souhaités. Par défaut, les descriptions courtes restent masquées. Activez l’option **Toujours afficher une description courte** pour l’afficher sous le composant.

* **Toujours afficher une description courte** - Activez cette option pour afficher la description courte sous le composant.

* **Texte d’aide** - Le texte d’aide fait référence à des informations ou des conseils supplémentaires fournis à l’utilisateur ou à l’utilisatrice pour l’aider à remplir correctement un champ de formulaire. Il s’affiche lorsque l’utilisateur ou l’utilisatrice clique sur l’icône d’aide (i) placée à côté du composant. Le texte d’aide fournit des informations plus détaillées que le texte du libellé ou de l’espace réservé d’un champ de formulaire. Il est conçu pour aider l’utilisateur ou l’utilisatrice à comprendre les exigences ou les contraintes du champ. Il peut également proposer des suggestions ou des exemples pour faciliter le remplissage du formulaire et le rendre plus précis.

### Onglet Accessibilité {#accessibility-tab}

![Onglet Accessibilité](/help/adaptive-forms/assets/textinput_accessibiltytab.png)

**Texte pour les lecteurs d’écran** - Le texte destiné aux lecteurs d’écran fait référence à un texte supplémentaire spécialement conçu pour être lu par les technologies d’assistance, comme les lecteurs d’écran, utilisées par les personnes malvoyantes. Ce texte fournit une description audio de l’objectif du champ de formulaire et peut inclure des informations sur le titre, la description, le nom du champ et tout message pertinent (texte personnalisé). Le texte du lecteur d’écran permet de s’assurer que le formulaire est accessible à tous les utilisateurs et utilisatrices, y compris celles et ceux ayant une déficience visuelle, et leur permet de bien comprendre le champ du formulaire et ses exigences.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS du composant « Zone de texte ».

### Onglet Styles {#styles-tab}

Cet onglet vous permet de définir et de gérer les styles CSS d’un composant. Le composant principal « Zone de texte » des formulaires adaptatifs prend en charge le [Système de style](/help/get-started/authoring.md#component-styling) d’AEM.

![Boîte de dialogue de conception.](/help/adaptive-forms/assets/telephoneinput_designdialog.png)

* **Classes CSS par défaut** : vous pouvez fournir une classe CSS par défaut pour le composant principal « Zone de texte » des formulaires adaptatifs.

* **Styles autorisés** : vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé « texte en gras » et fournir la classe CSS « police d’épaisseur : gras ». Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de formulaires adaptatifs. Pour appliquer un style, sélectionnez le composant auquel vous souhaitez appliquer le style dans l’éditeur de formulaires adaptatifs, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans la liste déroulante **Styles**. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

### Onglet Formats {#format-tab}

L’onglet Formats vous permet de définir des formats de nombres par défaut et personnalisés.

![Onglet Format.](/help/adaptive-forms/assets/telephoneinput_format.png)


## Article connexe {#related-article}

* [Création d’un formulaire adaptatif dans une page AEM Sites ou un fragment d’expérience](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=fr)

* [Création d’un formulaire adaptatif autonome](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=fr)
