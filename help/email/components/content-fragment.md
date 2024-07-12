---
title: Composant de fragment de contenu d’e-mail
description: Le composant de fragment de contenu d’e-mail permet d’afficher un fragment de contenu dans votre contenu.
role: Architect, Developer, Admin, User
exl-id: 9bc6b730-0d2a-4e5b-891c-d2f67f600bcc
source-git-commit: 3abc29e0c186a84f079d5938b8b716f4c7378d65
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 100%

---


# Composant de fragment de contenu d’e-mail {#email-content-fragment-component}

Le composant de fragment de contenu d’e-mail permet d’afficher un [fragment de contenu](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=fr) dans votre contenu.

## Utilisation {#usage}

Le composant de fragment de contenu d’e-mail permet d’inclure un [fragment de contenu](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=fr) dans le contenu de votre e-mail. Les fragments de contenu sont du contenu structuré multicanal qui peut être créé de manière centralisée et facilement réutilisé.

* Le fragment et ses propriétés peuvent être sélectionnés dans la [boîte de dialogue de configuration](#configure-dialog).
* Les types de ressources qui permettent de gérer certaines images et grilles peuvent être définis dans la [boîte de dialogue de conception](#design-dialog).
* L’option d’édition ouvre le fragment sélectionné dans l’[éditeur de fragment de contenu](#edit-dialog), conçu pour être utilisé avec les composants principaux d’e-mail.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de fragment de contenu d’e-mail est la v1, qui a été introduite avec la version X des composants principaux d’e-mail en octobre 2022. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatible | - |

Pour plus d’informations sur les versions et les publications des composants principaux d’e-mail, voir le document sur les [versions des composants principaux d’e-mail](/help/email/versions.md).

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant de fragment de contenu d’e-mail [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_email_cf_v1).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de définir le fragment de contenu et les éléments de ce fragment à inclure.

### Onglet Propriétés {#properties-tab}

![Composant de fragment de contenu d’e-mail](/help/email/assets/email-content-fragment-edit-properties.png)

* **Fragment de contenu**

   * Chemin d’accès au fragment de contenu souhaité
   * Vous pouvez utiliser la **boîte de dialogue de sélection** pour localiser le fragment.

* **Mode d’affichage**
   * **Un seul élément texte** : permet la sélection d’un élément de texte multiligne et active les options de contrôle des paragraphes.
* **Variation** : variante du fragment de contenu à utiliser (par défaut, **Gabarit**).

* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML.
   * Si rien n’est indiqué, un ID unique est généré automatiquement pour vous. Vous le trouverez en examinant le contenu obtenu.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur CSS.

### Onglet Contrôle de paragraphe {#paragraph-control-tab}

![Composant de fragment de contenu d’e-mail](/help/assets/content-fragment-edit-paragraph.png)

* **Paragraphes** : permet la sélection de tous les paragraphes ou d’une plage.
   * **Tout** : permet d’afficher tous les paragraphes.
   * **Étendue**
      * Spécifiez les plages de paragraphes à afficher, séparées par un point-virgule.
      * Par exemple, `1;3-5;7;9-*` pour inclure les premier, troisième au cinquième, septième et neuvième au dernier paragraphes.
* **Gérer les en-têtes comme paragraphes**

## Boîte de dialogue de modification {#edit-dialog}

Une fois que vous avez utilisé le composant de fragment de contenu d’e-mail pour configurer un fragment de contenu, lorsque vous sélectionnez le composant dans l’éditeur de contenu, un message avec l’option **Modifier** s’affiche.

![Barre d’outils du composant de fragment de contenu d’e-mail](/help/email/assets/email-content-fragment-edit-toolbar.png)

Appuyez ou cliquez sur le bouton **Modifier** pour ouvrir l’éditeur de fragment de contenu. L’éditeur de fragment de contenu a été étendu afin d’inclure des boutons **Sélectionner la variable Adobe Campaign** pour insérer des variables Adobe Campaign dans vos fragments de contenu.

![Éditeur de fragment de contenu pour les e-mails](/help/email/assets/email-content-fragment-editor.png)

Pour plus d’informations sur la modification et la création de fragments de contenu, consultez le document [Création de contenu de fragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/content-fragments/content-fragments-variations.html?lang=fr).

## Boîte de dialogue de conception {#design-dialog}

Lorsqu’un composant de fragment de contenu d’e-mail est configuré avec un fragment de contenu, lorsque vous le sélectionnez dans l’éditeur de contenu, la barre d’outils affiche un bouton pour ouvrir l’éditeur de fragment de contenu.


### Onglet Principal {#main-tab}

![Boîte de dialogue de conception du composant de fragment de contenu d’e-mail](/help/email/assets/email-content-fragment-design.png)

* **Grille réactive interne**

   * Type de ressource Sling utilisé pour la grille réactive interne

### Onglet Styles {#styles-tab}

Le composant de fragment d’expérience d’e-mail prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.
