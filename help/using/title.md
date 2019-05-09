---
title: Composant du titre
seo-title: Composant du titre
description: 'null'
seo-description: Le composant de titre de composant principal est un composant d'en-tête de section qui comporte des fonctions d'édition statique.
uuid: cf 190861-e 5 cd -42 b 8-9193-842 b 8 df 8 c 5 c 6
contentOwner: Utilisateur
content-type: référence
topic-tags: création
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 243 efc 75-fcf 9-427 d -9303-9642 b 0602991
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Composant du titre{#title-component}

Le composant de titre de composant principal est un composant d&#39;en-tête de section qui comporte des fonctions d&#39;édition statique.

## Utilisation {#usage}

Le composant Titre est conçu pour être utilisé comme titre ou en-tête d&#39;une section de contenu. Les niveaux d&#39;en-tête disponibles peuvent être définis par l&#39;auteur du modèle dans la boîte de dialogue [de conception](#design-dialog). L&#39;éditeur de contenu peut sélectionner les niveaux d&#39;en-têtes disponibles dans la boîte de dialogue [Modifier](#edit-dialog). Pour plus de commodité, une simple modification en place du texte d&#39;en-tête est également disponible.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Titre est v 2, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018 et est décrite dans ce document.

Le tableau suivant détaille toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|---|---|---|---|
| v2 | Compatible | Compatible | Compatible |
| [v1](title-v1.md) | Compatible | Compatible | Compatible |

Pour plus d&#39;informations sur les versions et les versions des composants principaux, consultez les versions des composants de Document [principaux](versions.md).

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple tiré de [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Capture d’écran {#screenshot}

![](assets/chlimage_1-36.png)

### Bibliothèque de composants

Pour tester le composant Titre ainsi que les exemples d&#39;options de configuration, ainsi que la sortie HTML et JSON, consultez la [bibliothèque Composant](http://opensource.adobe.com/aem-core-wcm-components/library/title.html).

### Détails techniques {#technical-details}

Vous trouverez la documentation technique la plus récente sur le composant [de titre sur github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/title/v2/title).

Vous trouverez plus d&#39;informations sur le développement des composants principaux dans la documentation destinée aux développeurs de composants [principaux](developing.md).

## Modifier le dialogue {#edit-dialog}

Le dialogue Modifier permet à l&#39;auteur de contenu de définir le texte du titre et de sélectionner le niveau de titre.

* **Titre** : si le titre de la page est vide, le titre de la page est utilisé
* **Type/Taille** : définit le niveau d&#39;en-tête du titre
* **Lien** : définit le contenu auquel le titre sera associé. Il peut s&#39;agir d&#39;un chemin d&#39;accès à une page de contenu, d&#39;une URL externe ou d&#39;une ancre de page.

![](assets/screenshot_2018-10-19at110055.png)

>[!CAUTION]
>
>La possibilité de définir un lien pour le titre a été introduite avec la version 2.2.0 des composants principaux.

L&#39;éditeur statique peut également être utilisé pour modifier le texte du composant de titre.

![](assets/chlimage_1-37.png)

## Créer un dialogue {#design-dialog}

Le dialogue de conception permet à l&#39;auteur du modèle de définir le niveau d&#39;en-tête par défaut que les composants de titre auront lorsqu&#39;ils sont créés par les auteurs de contenu.

### Onglet Tailles {#sizes-tab}

![](assets/screenshot_2018-10-19at110120.png)

* **Types/tailles autorisés pour les auteurs** : activez ou désactivez les types d&#39;en-têtes qui seront disponibles pour les auteurs de contenu lorsqu&#39;ils utilisent le composant Titre.
* **Type/Taille par défaut**: définissez le type d&#39;en-tête qui sera automatiquement attribué lorsqu&#39;un auteur de contenu ajoute le composant Titre à une page.
* **Désactiver le lien**: désactivez la prise en charge des liens dans le composant de titre pour interdire aux auteurs de contenu de lier des titres.

>[!CAUTION]
>
>La possibilité de définir un lien pour le titre a été introduite avec la version 2.2.0 des composants principaux.

### Onglet Styles {#styles-tab}

Le composant Titre prend en charge le système [de style AEM](authoring.md#component-styling).