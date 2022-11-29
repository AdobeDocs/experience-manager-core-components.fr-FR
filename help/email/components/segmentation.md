---
title: Composant de segmentation des emails
description: Composant Segmentation des emails
role: Architect, Developer, Admin, User
exl-id: 6c88b8c5-189a-40c0-ab28-04d37dc5fbac
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 16%

---


# Composant de segmentation des emails {#email-segmentation-component}

Le composant Segmentation des emails utilise des variables d’Adobe Campaign pour afficher et masquer le contenu en fonction du destinataire du contenu.

## Utilisation {#usage}

Le composant Segmentation des emails permet à l’auteur de contenu de masquer et d’afficher le contenu en fonction des conditions satisfaites par les variables sur le destinataire fourni par Adobe Campaign. Ainsi, les destinataires du contenu voient le contenu en fonction de leur segmentation.

* L’auteur du modèle peut utiliser la variable [boîte de dialogue de conception](#design-dialog) pour définir les composants qui peuvent être ajoutés en tant que segment.
* L’auteur du contenu peut utiliser la variable [boîte de dialogue de configuration](#configure-dialog) pour ajouter des composants en tant que segments et configurer les segments affichés en fonction des variables Adobe Campaign.

Au lieu d’utiliser la boîte de dialogue de configuration, une fois que l’auteur du contenu a ajouté le composant Segmentation des emails à une page de contenu, l’auteur du contenu peut ensuite faire glisser des composants supplémentaires sur les composants de segmentation des emails pour créer de nouveaux segments.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de segmentation des e-mails est v1, qui a été introduite avec la version x des composants principaux d’e-mail en octobre 2022. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatible | Compatible |

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant Segmentation des emails et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la page [Bibliothèque de composants.](https://adobe.com/go/aem_cmp_library_email_segmentation)

### Détails techniques {#technical-details}

Documentation technique la plus récente sur le composant Teaser d’email [est disponible sur GitHub.](https://adobe.com/go/aem_cmp_tech_email_segmentation_v1)

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux.](/help/developing/overview.md)

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de créer, renommer et réorganiser les segments, ainsi que de définir le principal segment. Dans le composant Segmentation des emails , un segment est simplement un autre composant masqué ou affiché selon les conditions satisfaites par le destinataire du contenu. Vous pouvez le comparer au [Composant d’onglet Composants principaux,](/help/components/tabs.md) mais dans le composant Segmentation, seul le contenu de l’onglet dont les conditions sont remplies s’affiche.

### Onglet Éléments {#items-tab}

![Onglet Configurer les éléments de boîte de dialogue du composant Segmentation des emails](/help/email/assets/email-segmentation-configure-items.png)

Utilisez la variable **Ajouter un segment** pour ouvrir le sélecteur de composants afin de choisir le composant à ajouter en tant que segment. Une fois ajoutée, une entrée est ajoutée à la liste, qui contient les éléments suivants :

* **Icône** - Icône du type de composant du segment pour une identification facile dans la liste. Pointez dessus pour afficher le nom complet du composant sous forme d’info-bulle.
* **Condition** - La condition qui doit être remplie pour que ce segment soit présenté au destinataire du contenu.
   * Les conditions disponibles sont définies dans la variable [boîte de dialogue de conception.](#design-dialog)
   * **Par défaut** - Définit le segment par défaut à afficher si aucune autre condition n’est remplie.
   * **Personnalisé** - Permet à l’auteur de définir une condition
      * Les conditions sont basées sur des variables de personnalisation Adobe Campaign
      * [Voir ici pour les ressources de personnalisation Adobe Campaign Standard.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?)
      * [Voir ici pour les ressources de personnalisation de Adobe Campaign Classic.](https://experienceleague.adobe.com/docs/campaign-classic/using/sending-messages/personalizing-deliveries/personalization-fields.html)
* **Supprimer** - Appuyez ou cliquez sur pour supprimer le segment du composant Segmentation des emails .
* **Réorganiser** - Appuyez ou cliquez dessus et faites glisser pour réorganiser les segments.

>[!TIP]
>
>Si la fenêtre d’affichage du contenu est réduite de sorte que la boîte de dialogue de modification s’affiche en plein écran, la variable **Ajouter** est masqué. Vous pouvez toujours ajouter des composants au composant Segmentation des emails en procédant comme suit : [effectuez un glisser-déposer depuis l’explorateur de composants et sur le composant Segmentation des emails dans l’éditeur de contenu.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=fr#inserting-a-component)

### Onglet Propriétés {#properties-tab}

![Onglet Propriétés de la boîte de dialogue de configuration du composant Segmentation des emails](/help/email/assets/email-segmentation-configure-properties.png)

* **ID** - Cette option permet de contrôler l’identifiant unique du composant dans le HTML.
   * Si rien n’est indiqué, un identifiant unique est automatiquement généré et peut être trouvé en examinant le contenu qui en résulte.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur CSS.

### Onglet Accessibilité {#accessibility-tab}

![Onglet Accessibilité de la boîte de dialogue de configuration du composant Segmentation des emails](/help/email/assets/email-segmentation-configure-accessibility.png)

Dans l’onglet **Accessibilité**, les valeurs peuvent être définies pour les étiquettes d’[accessibilité ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) du composant.

* **Étiquette** : Valeur d’un attribut de étiquette ARIA pour le composant

### Onglet Styles {#styles-tab-edit}

Le composant Segmentation des e-mails prend en charge l’AEM [Système de style.](/help/get-started/authoring.md#component-styling)

Utilisez la liste déroulante pour sélectionner les styles à appliquer au composant. Les sélections effectuées dans la boîte de dialogue de modification ou dans la barre d’outils du composant ont le même effet.

Les styles doivent être configurés pour ce composant dans la variable [boîte de dialogue de conception](#design-dialog) pour que l’onglet soit disponible.

## Sélectionner un panneau {#select-panel}

L’auteur du contenu peut utiliser la variable **Sélectionner un panneau** dans la barre d’outils du composant pour passer à un autre segment afin de le modifier et de réorganiser facilement les segments.

![Icône Sélectionner un panneau](/help/email/assets/select-panel-icon.png)

Une fois que vous avez sélectionné la variable **Sélectionner un panneau** dans la barre d’outils du composant, les segments configurés s’affichent sous la forme d’une liste déroulante.

* La liste est classée selon la disposition des segments qui lui est assignée et est répercutée dans la numérotation.
* Le type de composant du segment s’affiche en premier, suivi de la description du segment en police plus claire.

![Fenêtre contextuelle Sélectionner un panneau](/help/email/assets/select-panel-popover.png)

* Appuyez ou cliquez sur une entrée dans la liste déroulante, pour basculer la vue dans l’éditeur vers ce segment.
* Les segments peuvent être réorganisés de manière statique à l’aide des poignées de glissement.

>[!NOTE]
>
>Les segments sont rendus sous forme d’onglets dans l’éditeur de page afin d’indiquer qu’il existe plusieurs options pour le contenu final. Ces onglets ne peuvent pas être sélectionnés par l’auteur dans l’éditeur de page. Utilisez le panneau de sélection pour basculer entre les segments affichés.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir quels composants peuvent être ajoutés en tant que segments au composant Segmentation des emails , ainsi que de définir les styles personnalisés disponibles pour l’auteur du contenu.

### Onglet Composants autorisés {#allowed-components-tab}

Le **Composants autorisés** sert à définir les composants qui peuvent être ajoutés en tant que segments au composant Segmentation des emails par l’auteur du contenu.

Le **Composants autorisés** fonctionne de la même manière que l’onglet du même nom lorsque [définition de la stratégie et des propriétés d’un conteneur de mises en page dans l’éditeur de modèles.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=fr)

### Onglet Styles {#styles-tab}

Le composant Segmentation des e-mails prend en charge l’AEM [Système de style.](/help/get-started/authoring.md#component-styling)

### Onglet Conditions définies {#defined-conditions}

En utilisant la variable **Conditions définies** , l’éditeur de modèles peut définir les conditions que l’auteur de contenu peut sélectionner lors de la création de segments.

![Onglet Conditions définies de la boîte de dialogue de conception](/help/email/assets/email-segmentation-design-defined-conditions.png)

Appuyez ou cliquez sur le bouton **Ajouter** pour créer de nouvelles conditions.

* **Nom de la condition de segment** - Description de la condition
* **Condition de segment** - La condition réelle qui doit être remplie, en fonction des variables de personnalisation Adobe Campaign
   * [Voir ici pour les ressources de personnalisation Adobe Campaign Standard.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?)
   * [Voir ici pour les ressources de personnalisation de Adobe Campaign Classic.](https://experienceleague.adobe.com/docs/)
* **Supprimer** - Appuyez pour cliquer sur pour supprimer la condition.
* **Réorganiser** - Appuyez ou cliquez dessus et faites glisser pour réorganiser l’ordre des conditions.
