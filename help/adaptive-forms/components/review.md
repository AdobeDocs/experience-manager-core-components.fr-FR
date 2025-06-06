---
title: Composant principal de Forms adaptatif - Composant de révision
description: Utilisation ou personnalisation du composant principal Révision de Forms adaptatif.
role: Architect, Developer, Admin, User
hide: true
hidefromtoc: true
source-git-commit: 04a685cfa2616839f4fec715847bf0821808bd59
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 14%

---


# Composant de révision

Le composant Révision du Forms adaptatif permet aux utilisateurs et utilisatrices de vérifier les informations qu’ils ou elles ont saisies avant d’envoyer le formulaire. Il sert de page de résumé, offrant une vue en lecture seule de tous les champs et de leurs valeurs dans un format structuré et convivial. Cette fonctionnalité permet aux utilisateurs et utilisatrices d’identifier et de corriger les erreurs ou omissions avant de finaliser leur envoi, ce qui améliore l’expérience globale du formulaire. En cliquant sur l’icône Modifier , ils peuvent modifier les informations saisies avant l’envoi du formulaire.

**Exemple**

![Composant de révision](/help/adaptive-forms/assets/review-component.png){width=50%, align=center}

## Utilisation

Vous trouverez ci-dessous les raisons d’utiliser le composant Révision dans un formulaire adaptatif :

- **Exactitude des données améliorée** : le composant Révision permet aux utilisateurs et aux utilisatrices de réviser toutes les données qu’ils ou elles ont saisies avant envoi. Cela permet de réduire les risques d’erreurs ou d’omissions, en veillant à ce que les données envoyées soient exactes.
- **Expérience utilisateur améliorée** : les utilisateurs et les utilisatrices obtiennent un résumé clair et organisé de toutes les informations qu’ils ou elles ont remplies, ce qui leur donne confiance dans le fait que le formulaire est complet et précis avant l’envoi final, améliorant ainsi l’expérience globale.
- **Détection et correction d’erreurs** : elle permet de modifier les informations au niveau du panneau ou du champ et permet aux utilisateurs et aux utilisatrices de corriger les erreurs sans avoir à revenir sur plusieurs onglets. Cliquez sur l’icône **Modifier** en regard d’un panneau ou d’un champ pour revenir facilement en arrière et résoudre les problèmes.
- **Confiance accrue des utilisateurs** : les utilisateurs et les utilisatrices peuvent vérifier les données saisies, s’assurant ainsi que les informations qu’ils ou elles envoient sont correctes, ce qui entraîne moins d’erreurs d’envoi et une plus grande confiance dans les fonctionnalités du formulaire.
- **Empêcher les envois involontaires** : les utilisateurs cliquent souvent sur **Envoyer** sans examiner tous les détails. Le composant **Examen** leur donne une dernière chance de vérifier leurs données, ce qui réduit la probabilité de soumissions involontaires.


## Détails techniques {#technical-details}

Retrouvez les informations les plus récentes sur le composant principal « Révision de Forms adaptatif » dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser l’expérience des visiteurs et des visiteuses grâce à la boîte de dialogue de configuration pour une expérience utilisateur fluide.

![Boîte de dialogue de configuration](/help/adaptive-forms/assets/review-component-configure-dialog.png)

- **Nom** - Vous pouvez identifier facilement un composant de formulaire en lui attribuant un nom unique dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

- **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.
- **Masquer le titre** - Sélectionnez cette option pour masquer le titre du composant.
- **Activer les actions du mode de modification pour** - Les options **Activer les actions du mode de modification pour** permettent aux utilisateurs de modifier les informations saisies. Les utilisateurs et utilisatrices peuvent modifier les informations au niveau du champ ou du panneau.
   - Lorsque les utilisateurs sélectionnent l’option **Champ**, ils peuvent modifier individuellement les champs de formulaire au cours de la révision.
   - Lorsque les utilisateurs sélectionnent l’option **Panneau**, ils peuvent modifier tous les champs d’une section spécifique (panneau).
   - Lorsque les utilisateurs sélectionnent l’option **Champ et panneau**, ils peuvent cliquer sur l’icône de modification à côté d’un champ pour modifier des informations spécifiques ou à côté d’un panneau pour modifier tous les champs de ce panneau.
   - Lorsque les utilisateurs sélectionnent l’option **Aucun**, ils peuvent modifier n’importe quel champ ou panneau dans l’ensemble du formulaire.

  Par défaut, l’option **Panneau** est sélectionnée.

- **Panneaux de lien** - L’option **Panneaux de lien** permet aux utilisateurs et aux utilisatrices de sélectionner les panneaux à réviser. Lorsque des panneaux sont liés, les utilisateurs peuvent examiner les informations saisies dans le ou les panneaux sélectionnés et les modifier avant l’envoi.

## Cas d’utilisation

Prenons l’exemple d’un **Formulaire de demande de prêt** composé de quatre onglets, où chaque onglet collecte des informations spécifiques sur l’utilisateur :

- **Informations personnelles** : collecte les informations personnelles de base de l’utilisateur, telles que son nom, sa date de naissance, ses coordonnées et son adresse.

- **Détails du prêt** : collecte des informations relatives au prêt, notamment le type de prêt, le montant souhaité, la période de remboursement et les champs calculés automatiquement, tels que le taux d’intérêt et les mensualités.

- **Documents supplémentaires** : permet à l’utilisateur de charger les documents requis, tels que l’épreuve d’identité, l’épreuve d’adresse et l’épreuve de revenus. Il comprend également une case à cocher de déclaration pour confirmer l&#39;accord avec les conditions.

- **Vérifier et envoyer le formulaire** : comprend un composant Vérifier qui résume toutes les entrées des onglets précédents. Les utilisateurs peuvent vérifier et modifier leurs données avant d’envoyer le formulaire. Cet onglet comprend également le bouton **Envoyer** pour envoyer la demande.

La vidéo ci-dessous montre comment configurer le composant **Révision** afin qu’il offre à l’utilisateur la possibilité de modifier les informations :

## Articles connexes {#related-articles}

{{more-like-this}}

## Voir également {#see-also}

{{see-also}}

