---
title: Variables de campagne
description: Utilisez les variables de campagne comme espaces réservés pour composer du contenu d’email personnalisé.
role: Architect, Developer, Admin, User
exl-id: 124ff5bf-6612-4baf-b0ff-6b1a95b455c1
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---


# Variables de campagne {#campaign-variables}

Utilisez des variables de campagne pour composer du contenu d’email personnalisé. Les variables de campagne agissent comme des espaces réservés pour les valeurs Adobe Campaign que vous pouvez insérer dans le contenu de votre email. Lorsque le contenu est envoyé via Adobe Campaign, Campaign remplace ces variables par le contenu personnalisé du destinataire.

## Utilisation {#usage}

Les composants principaux d’email rendent les variables de campagne facilement accessibles via des boutons de personnalisation en regard des champs de texte communs. Lorsque vous appuyez dessus, une boîte de dialogue s’affiche, dans laquelle vous pouvez sélectionner un champ de personnalisation.

La liste des champs de personnalisation disponibles est synchronisée avec votre instance Adobe Campaign. Les champs sont gérés dans Adobe Campaign dans le schéma. `nms:seedMember`. Tous les champs de `nms:seedMember` doit également être présent dans la table des destinataires.

## Boîte de dialogue Sélectionner une variable Adobe Campaign {#dialog}

La boîte de dialogue Sélectionner la variable Adobe Campaign est disponible dans de nombreuses boîtes de dialogue de modification des composants principaux du courrier électronique. Pour l’utiliser, cliquez simplement sur le bouton **Sélectionner la variable Adobe Campaign** en regard du champ correspondant. Cette icône peut prendre deux formes.

![Bouton Adobe Campaign](/help/email/assets/campaign-button.png)
![Icône Sélectionner la variable Adobe Campaign](/help/email/assets/select-adobe-campaign-variable-icon.png)

Cliquez sur les deux icônes pour ouvrir la **Sélectionner la variable Adobe Campaign** boîte de dialogue.

![Boîte de dialogue Sélectionner la variable Adobe Campaign](assets/select-campaign-variable-dialog.png)

Utilisez le mode Colonnes pour localiser la variable que vous souhaitez insérer. Cliquez sur un noeud dans une colonne pour afficher ses enfants dans une nouvelle colonne à droite. Vous pouvez ainsi naviguer dans la structure de contenu de la variable.

Sélectionnez la variable à insérer, puis cliquez sur la coche en haut à droite de la boîte de dialogue.

![Variable Adobe Campaign sélectionnée](assets/select-campaign-variable-dialog-selected.png)

La variable est ensuite insérée dans le champ de la boîte de dialogue de modification du composant principal Email.

![Variable de campagne insérée dans la boîte de dialogue de modification](assets/campaign-variable.png)

Cliquez à tout moment sur le X en haut à gauche de la boîte de dialogue pour annuler et fermer la boîte de dialogue.
