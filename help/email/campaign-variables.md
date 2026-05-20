---
title: Variables de campagne
description: Utilisez les variables de campagne comme espaces réservés pour composer du contenu d’e-mail personnalisé.
role: Developer, Admin, User
exl-id: 124ff5bf-6612-4baf-b0ff-6b1a95b455c1
index: false
TQID: https://experienceleague.adobe.com/MB6K-S4DZbsD3puXls8w4rWi6posFFLxJRewKORMkxA
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: eb3ad9f8-54a2-45f3-abb1-d3976415a718
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: ce44533e-8ec8-4e11-a9e9-78b0fe561832
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 100%

---

# Variables de campagne {#campaign-variables}

Utilisez des variables de campagne pour composer du contenu d’e-mail personnalisé. Les variables de campagne agissent comme des espaces réservés pour les valeurs Adobe Campaign que vous pouvez insérer dans le contenu de votre e-mail. Lorsque le contenu est envoyé via Adobe Campaign, Campaign remplace ces variables par le contenu personnalisé du destinataire.

## Utilisation {#usage}

Les composants principaux d’e-mail rendent les variables de campagne facilement accessibles via des boutons de personnalisation en regard des champs de texte communs. Lorsque vous appuyez dessus, une boîte de dialogue s’affiche. Vous pouvez alors sélectionner un champ de personnalisation.

La liste des champs de personnalisation disponibles est synchronisée avec votre instance Adobe Campaign. Les champs sont gérés dans Adobe Campaign, dans le schéma `nms:seedMember`. Tous les champs de `nms:seedMember` doivent également être présents dans le tableau des destinataires.

## Boîte de dialogue Sélectionner la variable Adobe Campaign {#dialog}

La boîte de dialogue Sélectionner la variable Adobe Campaign est disponible dans de nombreuses boîtes de dialogue de modification des composants principaux d’e-mail. Pour l’utiliser, cliquez simplement sur l’icône **Sélectionner la variable Adobe Campaign** en regard du champ applicable. Cette icône peut prendre deux formes.

![Bouton Adobe Campaign](/help/email/assets/campaign-button.png)
![Icône Sélectionner la variable Adobe Campaign](/help/email/assets/select-adobe-campaign-variable-icon.png)

Cliquez sur les deux icônes pour ouvrir la boîte de dialogue **Sélectionner la variable Adobe Campaign**.

![Boîte de dialogue Sélectionner la variable Adobe Campaign](assets/select-campaign-variable-dialog.png)

Utilisez le mode Colonnes pour localiser la variable que vous souhaitez insérer. Cliquez sur un nœud dans une colonne pour afficher ses enfants dans une nouvelle colonne à droite. Vous pouvez ainsi naviguer dans la structure de contenu de la variable.

Sélectionnez la variable que vous souhaitez insérer, puis cliquez sur la coche en haut à droite de la boîte de dialogue.

![Variable Adobe Campaign sélectionnée](assets/select-campaign-variable-dialog-selected.png)

La variable est ensuite insérée dans le champ de la boîte de dialogue de modification du composant principal d’e-mail.

![Variable de campagne insérée dans la boîte de dialogue de modification](assets/campaign-variable.png)

Cliquez à tout moment sur le X en haut à gauche de la boîte de dialogue pour annuler et fermer la boîte de dialogue.
