---
title: Composant Segmentation d’e-mail
description: Composant Segmentation d’email
role: Architect, Developer, Admin, User
exl-id: 6c88b8c5-189a-40c0-ab28-04d37dc5fbac
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 100%

---


# Composant Segmentation d’e-mail {#email-segmentation-component}

Le composant Segmentation d’e-mail utilise des variables d’Adobe Campaign pour afficher et masquer le contenu en fonction du destinataire du contenu.

## Utilisation {#usage}

Le composant Segmentation d’e-mail permet à l’auteur de contenu de masquer et d’afficher le contenu en fonction des conditions remplies par les variables sur le destinataire fourni par Adobe Campaign. Ainsi, le contenu que les destinataires voient dépend de la segmentation.

* L’auteur du modèle peut utiliser la [boîte de dialogue de conception](#design-dialog) pour définir les composants qui peuvent être ajoutés en tant que segment.
* L’auteur du contenu peut utiliser la [boîte de dialogue de configuration](#configure-dialog) pour ajouter des composants en tant que segments et configurer les segments à afficher en fonction des variables Adobe Campaign.

Au lieu d’utiliser la boîte de dialogue de configuration, après avoir ajouté le composant Segmentation d’e-mail à une page de contenu, l’auteur de contenu peut glisser-déposer des composants supplémentaires sur les composants Segmentation d’e-mail pour créer des segments.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Segmentation d’e-mail est v1. Celle-ci a été introduite avec la version X des composants principaux d’e-mail en octobre 2022. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatible | Compatible |

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant Segmentation d’e-mail et voir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_email_segmentation).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Teaser d’e-mail [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_email_segmentation_v1).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de créer, renommer et réorganiser les segments ainsi que de définir le segment actif. Dans le composant Segmentation d’e-mail, un segment est simplement un autre composant masqué ou affiché selon les conditions remplies par le destinataire du contenu. Vous pouvez le comparer au [composant Onglets des composants principaux](/help/components/tabs.md). Cependant, dans le composant Segmentation, seul le contenu de l’onglet dont les conditions sont remplies s’affiche.

### Onglet Éléments {#items-tab}

![Onglet Éléments de la boîte de dialogue de configuration du composant Segmentation d’e-mail](/help/email/assets/email-segmentation-configure-items.png)

Utilisez le bouton **Ajouter un segment** pour ouvrir le sélecteur de composants et choisir le composant à ajouter en tant que segment. Une fois le composant ajouté, une entrée est ajoutée à la liste qui contient les éléments suivants :

* **Icône** : icône du type de composant du segment pour une identification facile dans la liste. Pointez dessus avec la souris pour afficher le nom complet du composant sous forme d’info-bulle.
* **Condition** : la condition qui doit être remplie pour que ce segment soit affiché au destinataire du contenu.
   * Les conditions disponibles sont définies dans la [boîte de dialogue de conception](#design-dialog).
   * **Par défaut** : définit le segment par défaut à afficher si aucune autre condition n’est remplie.
   * **Personnalisé** : permet à l’auteur de définir une condition.
      * Les conditions sont basées sur des variables de personnalisation Adobe Campaign.
      * [Cliquez ici pour découvrir les ressources de personnalisation Adobe Campaign Standard.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?lang=fr)
      * [Cliquez ici pour découvrir les ressources de personnalisation Adobe Campaign Classic.](https://experienceleague.adobe.com/docs/campaign-classic/using/sending-messages/personalizing-deliveries/personalization-fields.html?lang=fr)
* **Supprimer** : appuyez ou cliquez sur cette option pour supprimer le segment du composant Segmentation d’e-mail.
* **Réorganiser** : appuyez ou cliquez sur les segments et faites-les glisser pour les réorganiser.

>[!TIP]
>
>Si la fenêtre d’affichage du contenu est réduite, de sorte que la boîte de dialogue de modification s’affiche en plein écran, le bouton **Ajouter** est masqué. Vous pouvez toujours ajouter des composants au composant Segmentation d’e-mail en [les faisant glisser de l’explorateur de composants vers le composant Segmentation d’e-mail dans l’éditeur de contenu](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=fr#inserting-a-component).

### Onglet Propriétés {#properties-tab}

![Onglet Propriétés de la boîte de dialogue de configuration du composant Segmentation d’e-mail](/help/email/assets/email-segmentation-configure-properties.png)

* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML.
   * Si rien n’est indiqué, un ID unique est généré automatiquement pour vous. Vous le trouverez en examinant le contenu obtenu.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur CSS.

### Onglet Accessibilité {#accessibility-tab}

![Onglet Accessibilité de la boîte de dialogue de configuration du composant Segmentation d’e-mail](/help/email/assets/email-segmentation-configure-accessibility.png)

Dans l’onglet **Accessibilité**, les valeurs peuvent être définies pour les étiquettes d’[accessibilité ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) du composant.

* **Étiquette** : Valeur d’un attribut de étiquette ARIA pour le composant

### Onglet Styles {#styles-tab-edit}

Le composant Segmentation d’e-mail prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

Utilisez la liste déroulante pour sélectionner les styles à appliquer au composant. Les sélections effectuées dans la boîte de dialogue de modification ou dans la barre d’outils du composant ont le même effet.

Pour que l’onglet soit disponible, les styles doivent être configurés pour ce composant dans la [boîte de dialogue de conception](#design-dialog).

## Sélectionner un panneau {#select-panel}

L’auteur de contenu peut utiliser l’option **Sélectionner un panneau** dans la barre d’outils de composants pour passer à un autre segment. Il peut alors modifier et réorganiser facilement l’ordre des segments.

![Icône Sélectionner un panneau](/help/email/assets/select-panel-icon.png)

Lorsque vous sélectionnez l’option **Sélectionner un panneau** dans la barre d’outils de composants, les segments configurés s’affichent sous forme de liste déroulante.

* La liste est triée selon la disposition assignée des segments et est répercutée dans la numérotation.
* Le type de composant du segment est affiché en premier, suivi de la description du segment dans une police plus claire.

![Fenêtre contextuelle Sélectionner un panneau](/help/email/assets/select-panel-popover.png)

* Appuyez ou cliquez sur une entrée dans la liste déroulante pour commuter la vue de l’éditeur dans ce segment.
* Vous pouvez réorganiser les segments sur place à l’aide des poignées de glissement.

>[!NOTE]
>
>Les segments sont rendus sous forme d’onglets dans l’éditeur de page afin d’indiquer qu’il existe plusieurs options pour le contenu final. Ces onglets ne peuvent pas être sélectionnés par l’auteur dans l’éditeur de page. Utilisez l’option Sélectionner un panneau pour basculer entre les segments affichés.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir quels composants peuvent être ajoutés en tant que segments au composant Segmentation d’e-mail et de définir les styles personnalisés disponibles pour l’auteur de contenu.

### Onglet Composants autorisés {#allowed-components-tab}

L’onglet **Composants autorisés** permet de définir les composants pouvant être ajoutés en tant que segments au composant Segmentation d’e-mail par l’auteur de contenu.

L’onglet **Composants autorisés** fonctionne de la même manière que l’onglet du même nom lors de la [définition de la stratégie et des propriétés d’un conteneur de dispositions dans l’éditeur de modèles](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=fr).

### Onglet Styles {#styles-tab}

Le composant Segmentation d’e-mail prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

### Onglet Conditions définies {#defined-conditions}

À l’aide de l’onglet **Conditions définies**, l’éditeur de modèles peut définir les conditions que l’auteur de contenu peut sélectionner lors de la création de segments.

![Onglet Conditions définies de la boîte de dialogue de conception](/help/email/assets/email-segmentation-design-defined-conditions.png)

Appuyez ou cliquez sur le bouton **Ajouter** pour créer des conditions.

* **Nom de la condition de segment** : description de la condition.
* **Condition de segment** : condition réelle qui doit être remplie, en fonction des variables de personnalisation Adobe Campaign.
   * [Cliquez ici pour découvrir les ressources de personnalisation Adobe Campaign Standard.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?)
   * [Cliquez ici pour découvrir les ressources de personnalisation Adobe Campaign Classic.](https://experienceleague.adobe.com/docs/
* **Supprimer** : appuyez ou cliquez pour supprimer la condition.
* **Réorganiser** : appuyez ou cliquez sur les conditions et faites-les glisser pour les réorganiser.
