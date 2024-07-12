---
title: Composant Onglets
description: Le composant Onglets permet la création de plusieurs onglets pour disposer le contenu sur une page.
role: Architect, Developer, Admin, User
exl-id: 0031c5f3-447c-4932-898f-2f453801e492
source-git-commit: d39fe0084522f67664203a026340b23d325c1883
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 100%

---


# Composant Onglets {#tabs-component}

Le composant Onglets des composants principaux permet l’organisation de contenu sur plusieurs onglets.

## Utilisation {#usage}

Le composant Onglets permet à l’auteur de contenu d’organiser le contenu de la page dans plusieurs onglets.

La [boîte de dialogue de modification](#edit-dialog) permet à l’auteur de contenu de définir plusieurs onglets et de définir l’onglet actif. À l’aide de [la boîte de dialogue de conception](#design-dialog), l’auteur du modèle peut définir les composants qui peuvent être ajoutés aux onglets et personnaliser les styles.

>[!TIP]
>
>Les composants d’onglets imbriqués (onglets dans les onglets) sont pris en charge.
>
>Les composants des onglets simples (non imbriqués) peuvent être localisés/sélectionnés à l’aide de l’[arborescence de contenu](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=fr#content-tree), mais les onglets imbriqués ne peuvent pas l’être.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Onglets est v1, qui a été introduite avec la version 2.2.0 des composants principaux d’octobre 2018. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatible avec la <br>[version 2.17.4](/help/versions.md) et versions antérieures | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant Onglets, des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [Bibliothèque de composants](https://adobe.com/go/aem_cmp_library_tabs_fr).

### Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Onglets [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_tabs_v1_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Créer un lien profond vers un panneau {#deep-linking}

Les composants Onglets, [Carrousel](carousel.md) et [Accordéon](accordion.md) prennent en charge le lien direct vers un panneau au sein du composant.

Pour ce faire :

1. Affichez la page avec le composant à l’aide de l’option **[Afficher comme publié(e)](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=fr#view-as-published)** dans l’éditeur de page.
1. Examinez le contenu de la page et identifiez l’ID du panneau.
   * Par exemple, `id="accordion-86196c94d3-item-ca319dbb0b"`
1. L’ID devient l’ancre que vous pouvez ajouter à l’URL à l’aide d’un hachage (`#`).
   * Par exemple, `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

En accédant à l’URL avec l’ID de panneau comme ancre, le navigateur fait défiler directement le composant et affiche le panneau spécifié. Si le panneau est configuré pour ne pas être développé par défaut, il sera développé automatiquement.

## Onglet et conception réactive {#responsive-design}

Tous les composants principaux sont conçus pour être entièrement réactifs, ce qui garantit une expérience transparente sur tous les appareils.

Certains composants avancés, tels que le composant Onglet, peuvent nécessiter une prise en compte spécifique dans le contexte du projet d’implémentation afin de maintenir la réactivité dans toutes les conditions. Consultez le document [Conception réactive des composants principaux](/help/responsive.md) pour plus d’informations.

## Boîte de dialogue de modification {#edit-dialog}

La boîte de dialogue de modification permet à l’auteur de contenu de créer, renommer et réorganiser les onglets et de définir l’onglet actif.

### Onglet Éléments {#items-tab}

![Onglet Éléments de la boîte de dialogue de modification du composant Onglets](/help/assets/tabs-edit-items.png)

Utilisez le bouton **Ajouter** pour ouvrir le sélecteur de composants afin de choisir le composant à ajouter sous forme d’onglet. Une fois le composant ajouté, une entrée est ajoutée à la liste qui contient les colonnes suivantes :

* **Icône** : icône du type de composant de l’onglet pour une identification facile dans la liste. Pointez dessus pour afficher le nom complet du composant sous forme d’info-bulle.
* **Description** : description utilisée comme texte de l’onglet. Par défaut, il s’agit du nom du composant sélectionné pour l’onglet.
* **Supprimer** : appuyez ou cliquez dessus pour supprimer l’onglet du composant Onglets.
* **Réorganiser** : appuyez ou cliquez dessus et faites glisser pour réorganiser l’ordre des onglets.

>[!TIP]
>
>Si la fenêtre d’affichage de la page est réduite, de sorte que la boîte de dialogue de modification s’affiche en plein écran, le bouton **Ajouter** est masqué. Vous pouvez toujours ajouter des composants au composant Onglets en [les faisant glisser depuis l’explorateur de composants et en les déposant ensuite sur le composant Onglets dans l’éditeur de page](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=fr#inserting-a-component).

### Onglet Propriétés {#properties-tab}

![Onglet Propriétés de la boîte de dialogue de modification du composant Onglets](/help/assets/tabs-edit-properties.png)

* **Élément actif** : l’auteur du contenu peut définir quel onglet est actif lorsque la page est chargée.
   * Avec l’option **Par défaut**, le premier onglet est sélectionné.
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

### Onglet Accessibilité {#accessibility-tab}

![Onglet Accessibilité de la boîte de dialogue de modification du composant Onglets](/help/assets/tabs-edit-accessibility.png)

Dans l’onglet **Accessibilité**, les valeurs peuvent être définies pour les étiquettes d’[accessibilité ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) du composant.

* **Étiquette** : Valeur d’un attribut de étiquette ARIA pour le composant

## Sélectionner un panneau {#select-panel}

L’auteur du contenu peut utiliser l’option **Sélectionner un panneau** dans la barre d’outils du composant pour choisir un panneau différent, ainsi que pour réorganiser l’ordre des onglets.

![Icône Sélectionner un panneau](/help/assets/select-panel-icon.png)

Lorsque vous sélectionnez l’option **Sélectionner un panneau** dans la barre d’outils du composant, les onglets configurés s’affichent sous forme de liste déroulante.

* La liste est classée en fonction de la disposition des onglets et est reflétée dans la numérotation.
* Le type de composant de l’onglet est affiché en premier, suivi de la description de l’onglet une police plus claire.

![Fenêtre contextuelle Sélectionner un panneau](/help/assets/select-panel-popover.png)

* Vous pouvez commuter la vue de l’éditeur dans cet onglet en appuyant ou en cliquant sur une entrée dans la liste déroulante.
* Vous pouvez réorganiser les onglets statiques à l’aide des poignées de glissement.

>[!NOTE]
>
>Les onglets ne sont pas sélectionnables par l’auteur en mode **Édition**. Utilisez le mode **[Aperçu](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=fr#preview-mode)** ou l’option **[Afficher comme publié(e)](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=fr#view-as-published)** pour interagir avec les onglets comme un lecteur du contenu publié.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir quels composants peuvent être ajoutés en tant qu’éléments au composant Onglets et de définir les styles personnalisés disponibles pour l’auteur du contenu.

### Onglet Composants autorisés {#allowed-components-tab}

L’onglet **Composants autorisés** permet de définir quels composants peuvent être ajoutés en tant qu’éléments au composant Onglets par l’auteur ou l’autrice du contenu.

L’onglet Composants autorisés fonctionne de la même manière que l’onglet du même nom lors de la [définition de la politique et des propriétés d’un conteneur de disposition dans l’éditeur de modèles](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=fr).

### Onglet Styles {#styles-tab}

Le composant Onglets prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

## Couche de données client Adobe {#data-layer}

Le composant Onglets prend en charge la [couche de données client Adobe](/help/developing/data-layer/overview.md).
