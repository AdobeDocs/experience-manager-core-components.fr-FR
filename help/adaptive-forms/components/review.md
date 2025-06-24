---
title: Composant principal des formulaires adaptatifs - Composant de révision
description: Utilisation ou personnalisation du composant principal de révision des formulaires adaptatifs.
role: Architect, Developer, Admin, User
hide: true
hidefromtoc: true
exl-id: acd230ed-284b-4df2-98e0-a0090cd73611
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Composant de révision

Le composant de révision des formulaires adaptatifs permet aux utilisateurs et utilisatrices de vérifier les informations qu’ils ont saisies avant d’envoyer le formulaire. Il sert de page de résumé, offrant une vue en lecture seule de tous les champs et de leurs valeurs dans un format structuré et convivial. Cette fonctionnalité permet aux utilisateurs et utilisatrices d’identifier et de corriger les erreurs ou omissions avant de finaliser leur envoi, ce qui améliore l’expérience globale du formulaire. En cliquant sur l’icône Modifier, il est possible de modifier les informations saisies avant l’envoi du formulaire.

{{traditional-aem}}

**Exemple**

![Composant Révision](/help/adaptive-forms/assets/review-component.png){width=50%, align=center}

## Utilisation

Il existe plusieurs raisons d’inclure un composant Révision dans un formulaire adaptatif :

- **Amélioration de l’exactitude des données** : le composant Révision permet aux utilisateurs et aux utilisatrices de réviser toutes les données qu’ils ou elles ont saisies avant envoi. Cela permet de réduire les risques d’erreurs ou d’omissions, en veillant à ce que les données envoyées soient exactes.
- **Expérience d’utilisation améliorée** : les utilisateurs et utilisatrices obtiennent un résumé clair et organisé de toutes les informations qu’ils ou elles ont remplies, s’assurant ainsi que le formulaire est complet et précis avant l’envoi final, pour une expérience globale améliorée.
- **Détection et correction d’erreurs** : permet de modifier les informations au niveau du panneau ou du champ pour que les utilisateurs et utilisatrices corrigent les erreurs sans avoir à revenir sur plusieurs onglets. Cliquez sur l’icône **Modifier** en regard d’un panneau ou d’un champ pour revenir facilement en arrière et résoudre les problèmes.
- **Confiance accrue des personnes** : les utilisateurs et les utilisatrices peuvent vérifier les données saisies, s’assurant ainsi que les informations qu’ils ou elles envoient sont correctes, ce qui entraîne moins d’erreurs d’envoi et une plus grande confiance dans les fonctionnalités du formulaire.
- **Empêcher les envois involontaires** : les personnes cliquent souvent sur **Envoyer** sans examiner tous les détails. Le composant **Révision** leur donne une dernière chance de vérifier leurs données, ce qui réduit la probabilité d’envois involontaires.


## Détails techniques {#technical-details}

Retrouvez les dernières informations sur le composant principal Révision des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience des visiteurs et des visiteuses grâce à la boîte de dialogue de configuration pour une expérience d’utilisation fluide.

![Boîte de dialogue de configuration](/help/adaptive-forms/assets/review-component-configure-dialog.png)

- **Nom** - Vous pouvez identifier facilement un composant de formulaire en lui attribuant un nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

- **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.
- **Masquer le titre** - Sélectionnez cette option pour masquer le titre du composant.
- **Activer les actions du mode de modification pour** : les options **Activer les actions du mode de modification pour** permettent de modifier les informations saisies. Les personnes peuvent modifier les informations au niveau du champ ou du panneau.
   - Lorsque les personnes sélectionnent l’option **Champ**, elles peuvent modifier individuellement les champs de formulaire au cours de la révision.
   - Lorsque les personnes sélectionnent l’option **Panneau**, elles peuvent modifier tous les champs d’une section spécifique (panneau).
   - Lorsque les personnes sélectionnent l’option **Champ et panneau**, elles peuvent cliquer sur l’icône de modification en regard d’un champ pour modifier des informations spécifiques ou en regard d’un panneau pour modifier tous les champs de ce panneau.
   - Lorsque les personnes sélectionnent l’option **Aucun**, elles peuvent modifier n’importe quel champ ou panneau dans l’ensemble du formulaire.

  Par défaut, l’option **Panneau** est sélectionnée.

- **Panneaux de lien** : l’option **Panneaux de lien** permet aux utilisateurs et aux utilisatrices de sélectionner les panneaux à réviser. Lorsque des panneaux sont liés, les personnes peuvent examiner les informations saisies dans le ou les panneaux sélectionnés et les modifier avant l’envoi.

## Cas d’utilisation

Prenons l’exemple d’un **Formulaire de demande de prêt** composé de quatre onglets, où chaque onglet collecte des informations spécifiques sur la personne :

- **Informations personnelles** : collecte les informations personnelles de base de la personne, telles que son nom, sa date de naissance, ses coordonnées et son adresse.

- **Détails du prêt** : collecte des informations relatives au prêt, notamment le type de prêt, le montant souhaité, la période de remboursement et les champs calculés automatiquement, tels que le taux d’intérêt et les mensualités.

- **Documents supplémentaires** : permet à la personne de charger les documents requis, tels que l’épreuve d’identité, l’épreuve d’adresse et l’épreuve de revenus. Il comprend également une case à cocher de déclaration pour confirmer l’accord avec les conditions.

- **Vérifier et envoyer le formulaire** : comprend un composant Vérifier qui résume toutes les entrées des onglets précédents. Les personnes peuvent vérifier et modifier leurs données avant d’envoyer le formulaire. Cet onglet comprend également le bouton **Envoyer** pour envoyer la demande.

La vidéo ci-dessous montre comment configurer le composant **Révision** afin qu’il offre la possibilité de modifier les informations :

## Articles connexes {#related-articles}

{{more-like-this}}

## Voir également {#see-also}

{{see-also}}
