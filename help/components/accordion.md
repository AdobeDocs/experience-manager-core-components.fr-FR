---
title: 'Composant d’accordéon '
description: Le composant d’accordéon des composants principaux permet la création d’un ensemble de panneaux organisés dans un accordéon sur une page.
role: Architect, Developer, Admin, User
exl-id: 1deb570a-3d8d-409e-805f-8460c49cf9bb
source-git-commit: 9767a3a10cb9a77f385edc0ac3fb00096c0087af
workflow-type: ht
source-wordcount: '1067'
ht-degree: 100%

---

# Composant d’accordéon {#accordion-component}

Le composant d’accordéon des composants principaux permet la création d’un ensemble de panneaux organisés dans un accordéon sur une page.

## Utilisation {#usage}

Le composant d’accordéon des composants principaux permet la création d’un ensemble de composants, présentés sous forme de panneaux, et organisés dans un accordéon sur une page. Semblable au [composant Onglets](tabs.md), il autorise toutefois le développement et la réduction des panneaux.

* Les propriétés de l’accordéon peuvent être définies dans la [boîte de dialogue de configuration](#configure-dialog).
* L’ordre des panneaux de l’accordéon peut être défini dans la boîte de dialogue de configuration, ainsi que dans la [fenêtre contextuelle de sélection d’un panneau](#select-panel-popover).
* Les valeurs par défaut du composant d’accordéon lors de son ajout à une page peuvent être définies dans la [boîte de dialogue de conception](#design-dialog).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant d’accordéon est v1, qui a été introduite avec la version 2.5.0 des composants principaux en février 2019. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible avec la <br>[version 2.17.4](/help/versions.md) et versions antérieures | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant d’accordéon et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [Bibliothèque de composants](https://adobe.com/go/aem_cmp_library_accordion).

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant d’accordéon [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_accordion_v1).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Liaison profonde vers un panneau {#deep-linking}

Les composants Accordéon et [Onglets](tabs.md) prennent en charge la liaison directe à un panneau au sein du composant.

Pour ce faire :

1. Affichez la page avec le composant à l’aide de l’option **[Afficher comme publié(e)](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=fr#view-as-published)** dans l’éditeur de page.
1. Examinez le contenu de la page et identifiez l’ID du panneau.
   * Par exemple, `id="accordion-86196c94d3-item-ca319dbb0b"`
1. L’ID devient l’ancre que vous pouvez ajouter à l’URL à l’aide d’un hachage (`#`).
   * Par exemple, `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

En accédant à l’URL avec l’ID de panneau comme ancre, le navigateur fait défiler directement le composant et affiche le panneau spécifié. Si le panneau est configuré pour ne pas être développé par défaut, il sera développé automatiquement.

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de définir l’élément d’accordéon, ses panneaux et la façon dont il se comporte et s’affiche pour un visiteur sur la page.

### Onglet Éléments {#items-tab}

![Onglet Éléments de la boîte de dialogue de modification du composant Accordéon](/help/assets/accordion-edit-items.png)

Utilisez le bouton **Ajouter** pour ouvrir le sélecteur de composants afin de choisir le composant à ajouter sous forme de panneau. Une fois le composant ajouté, une entrée est ajoutée à la liste qui contient les colonnes suivantes :

* **Icône** : icône du type de composant du panneau pour une identification facile dans la liste. Pointez dessus pour afficher le nom complet du composant sous forme d’info-bulle.
* **Description** : description utilisée comme texte du panneau. Par défaut, il s’agit du nom du composant sélectionné pour le panneau.
* **Supprimer** : appuyez ou cliquez sur cette option pour supprimer le panneau du composant d’accordéon.
* **Réorganiser** : appuyez ou cliquez dessus et faites glisser pour réorganiser l’ordre des panneaux.

>[!TIP]
>
>Si la fenêtre d’affichage de la page est réduite, de sorte que la boîte de dialogue de modification s’affiche en plein écran, le bouton **Ajouter** est masqué. Vous pouvez toujours ajouter des composants au composant d’accordéon en [les faisant glisser depuis l’explorateur de composants et en les déposant ensuite sur le composant d’accordéon dans l’éditeur de page](https://helpx.adobe.com/fr/experience-manager/6-5/sites/authoring/using/editing-content.html#InsertingaComponent).

### Onglet Propriétés {#properties-tab}

![Onglet Propriétés de la boîte de dialogue de modification du composant Accordéon](/help/assets/accordion-edit-properties.png)

* **Développement d’un seul élément** : lorsqu’elle est sélectionnée, cette option force le développement d’un seul élément d’accordéon à la fois. Le développement d’un élément réduit alors tous les autres.
* **Éléments développés** : cette option définit les éléments qui sont développés par défaut lorsque la page est chargée.
   * Lorsque l’option **Développement d’un seul élément** est sélectionnée, un panneau doit être sélectionné. Par défaut, il s’agit du premier panneau.
   * Lorsque l’option **Développement d’un seul élément** n’est pas sélectionnée, cette option propose une sélection multiple et est facultative.
* **ID** : cette option permet de contrôler l’identifiant unique du composant dans le code HTML ainsi que dans la [couche de données](/help/developing/data-layer/overview.md).
   * Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
   * Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
   * La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

## Fenêtre contextuelle Sélectionner un panneau {#select-panel-popover}

L’auteur du contenu peut utiliser l’option **Sélectionner un panneau** de la barre d’outils du composant pour choisir un panneau différent pour l’édition, ainsi que pour réorganiser l’ordre des panneaux au sein de l’accordéon.

![Icône Sélectionner un panneau](/help/assets/select-panel-icon.png)

Lorsque vous sélectionnez l’option **Sélectionner un panneau** dans la barre d’outils des composants, les panneaux d’accordéon configurés s’affichent sous forme de liste déroulante.

![Fenêtre contextuelle Sélectionner un panneau](/help/assets/select-panel-popover.png)

* La liste est triée selon la disposition assignée des panneaux et est répercutée dans la numérotation.
* Le type de composant du panneau est affiché en premier, suivi de la description du panneau en police plus claire.
* Lorsque vous appuyez ou cliquez sur une entrée dans la liste déroulante, la vue est basculée dans l’éditeur vers ce panneau.
* Vous pouvez réorganiser les panneaux statiques à l’aide des poignées de glissement.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les options disponibles pour l’auteur du contenu qui utilise le composant d’accordéon et les valeurs par défaut définies lors du placement de celui-ci.

### Onglet Propriétés {#properties-tab-design}

![Onglet Propriétés de la boîte de dialogue de conception](/help/assets/accordion-design-properties.png)

* **Éléments de titre autorisés** : cette liste déroulante à sélection multiple définit les éléments HTML d’en-tête de l’élément d’accordéon qui sont autorisés à être sélectionnés par un auteur.
* **Élément de titre par défaut** : cette liste déroulante définit l’élément HTML d’en-tête de l’élément d’accordéon par défaut.

### Onglet Composants autorisés {#allowed-components-tab}

L’onglet **Composants autorisés** permet de définir quels composants peuvent être ajoutés en tant qu’éléments aux panneaux dans le composant d’accordéon par l’auteur du contenu.

L’onglet Composants autorisés fonctionne de la même manière que l’onglet du même nom lors de la [définition de la stratégie et des propriétés d’un conteneur de mises en page dans l’éditeur de modèles](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=fr#editing-a-template-layout-template-author).

### Onglet Styles {#styles-tab}

Le composant d’accordéon prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

## Couche de données client Adobe {#data-layer}

Le composant Accordéon prend en charge la [couche de données client Adobe](/help/developing/data-layer/overview.md).
