---
title: Composant principal Forms adaptatif - Texte
description: Utilisation ou personnalisation du composant principal Texte de Forms adaptatif .
role: Architect, Developer, Admin, User
exl-id: b8de68e4-ca0d-4ae5-9a04-104cc617f1be
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 2%

---

# Texte {#text-adaptive-forms-core-component}

Dans un formulaire adaptatif, le texte fait référence au contenu affiché dans le formulaire pour que l’utilisateur puisse le lire. Cela peut inclure le texte utilisé pour étiqueter un groupe d’éléments de formulaire, tels que des champs de texte, ainsi que toute instruction ou information supplémentaire fournie à l’utilisateur.

Cela peut également permettre de diviser la structure d’un formulaire en sections logiques, ce qui facilite la compréhension et la saisie du formulaire par les utilisateurs. En outre, il peut être utilisé à des fins d’accessibilité pour donner une brève description de l’élément auquel il est associé. Ce champ de texte est généralement affiché près des composants du formulaire, avant ou après.

**Exemple**

![](/help/adaptive-forms/assets/text.png)

## Utilisation {#reasons-to-use-text-label}

Il existe plusieurs raisons d’utiliser du texte dans un formulaire :

* **Instructions**: Le texte peut être utilisé pour fournir des instructions sur la façon de remplir le formulaire ou sur les informations requises.

* **Fournir un contexte**: Le texte peut être utilisé pour fournir un contexte au formulaire, par exemple pour expliquer l’objet du formulaire ou l’organisation qui collecte les informations.

* **Diviser le formulaire en sections logiques**: Le texte peut être utilisé pour diviser un formulaire en sections logiques, ce qui facilite la compréhension et le remplissage du formulaire par les utilisateurs.

* **Marque et identité**: Le texte peut être utilisé à des fins de valorisation de marque et d’identité, comme l’inclusion du nom de l’organisation dans le formulaire.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Accordéon de Forms adaptatif a été publié en février 2023 dans le cadre des composants principaux 2.0.4 pour Cloud Service et des composants principaux 1.1.12 pour AEM 6.5.16.0 Forms ou version ultérieure. Voici un tableau de toutes les versions prises en charge, de la compatibilité AEM et des liens vers la documentation correspondante :

| Version du composant | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou version ultérieure |
|---|---|---|
| v1 | Compatible avec<br>[version 2.0.4](/help/adaptive-forms/version.md) et plus tard | Compatible avec<br>[version 1.1.12](/help/adaptive-forms/version.md) et plus tard, mais moins de 2.0.0. |

Pour plus d’informations sur les versions et versions des composants principaux, reportez-vous à la section [Versions des composants principaux](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Détails techniques {#technical-details}

Obtenez les dernières informations sur le composant principal Texte adaptatif Forms dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/text/v1/text). Pour plus d’informations sur le développement des composants principaux, consultez la section [Documentation destinée aux développeurs sur les composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser votre expérience textuelle pour les visiteurs qui utilisent la boîte de dialogue Configurer . Vous pouvez également définir facilement des options de texte pour une expérience utilisateur transparente.

![Onglet Simple](/help/adaptive-forms/assets/text_properties.png)

* **Nom** - Vous pouvez identifier facilement un composant de formulaire avec son nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

* **Référence de liaison** - Une référence de liaison est une référence à un élément de données stocké dans une source de données externe et utilisé dans un formulaire. La référence de liaison vous permet de lier dynamiquement les données aux champs du formulaire, de sorte que le formulaire puisse afficher les données les plus récentes de la source de données. Par exemple, une référence de liaison peut être utilisée pour afficher le nom et l’adresse d’un client dans un formulaire, en fonction de l’identifiant du client saisi dans le formulaire. La référence de liaison peut également être utilisée pour mettre à jour la source de données avec les données saisies dans le formulaire. Ainsi, AEM Forms vous permet de créer des formulaires qui interagissent avec des sources de données externes, offrant ainsi une expérience utilisateur transparente pour la collecte et la gestion des données.
* **Masquer le composant** - Sélectionnez l’option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par l’utilisateur.
* **Lecture seule** - Sélectionnez l’option pour rendre le composant non modifiable. L’utilisateur peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.


## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS du composant Texte.

### Onglet Styles {#styles-tab}

L’onglet permet de définir et de gérer les styles CSS d’un composant. Le composant principal Texte Forms adaptatif prend en charge l’AEM [Système de style](/help/get-started/authoring.md#component-styling).

![Boîte de dialogue de conception](/help/adaptive-forms/assets/reset_designdialog.png)

* **Classes CSS par défaut**: Vous pouvez fournir une classe CSS par défaut pour le composant principal Texte de Forms adaptatif .

* **Styles autorisés**: Vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé &quot;bold text&quot; et fournir la classe CSS &quot;font-weight: bold&quot;. Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de Forms adaptatif. Pour appliquer un style, dans l’éditeur de Forms adaptatif, sélectionnez le composant auquel vous souhaitez appliquer le style, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans le **Styles** liste déroulante. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.
