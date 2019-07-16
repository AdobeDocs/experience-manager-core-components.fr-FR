---
title: Composant de liste de fragments de contenu
seo-title: Composant de liste de fragments de contenu
description: 'null'
seo-description: Le composant de liste de fragments de contenu des composants principaux permet d’afficher une liste de fragments de contenu.
contentOwner: bohnert
content-type: référence
topic-tags: création
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
translation-type: ht
source-git-commit: 632d6abb1f13667cc0457152268d50af3bfabfc4

---


# Composant de liste de fragments de contenu{#content-fragment-list-component}

Le composant de liste de fragments de contenu des composants principaux permet d’afficher une liste de [fragments de contenu](https://helpx.adobe.com/experience-manager/6-5/assets/using/content-fragments.html).

## Utilisation {#usage}

Le composant de liste de fragments de contenu des composants principaux permet d’inclure une liste de [fragments de contenu](https://helpx.adobe.com/experience-manager/6-5/assets/using/content-fragments.html) sur une page basée sur un modèle de fragment de contenu. Cette opération peut s’avérer particulièrement utile pour créer un [contenu sans en-tête ](https://helpx.adobe.com/experience-manager/6-5/sites/developing/user-guide.html?topic=/experience-manager/6-5/sites/developing/morehelp/headless.ug.js) qui peut être facilement utilisé par d’autres applications.

* La liste et ses propriétés peuvent être sélectionnées dans la [boîte de dialogue de configuration](#configure-dialog).
* Des styles peuvent être appliqués au composant dans la [boîte de dialogue de conception](#design-dialog).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de fragment de contenu est v1, qui a été introduite avec la version 2.4.0 des composants principaux en mai 2019. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant de liste de fragments de contenu et voir des exemples d’options de configuration et de sortie HTML et JSON, consultez la [bibliothèque de composants](http://opensource.adobe.com/aem-core-wcm-components/library/content-fragment-list.html).

## Détails techniques {#technical-details}

Vous trouverez la documentation technique la plus récente sur le composant de liste de fragments de contenu [sur GitHub ](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/contentfragmentlist/v1/contentfragmentlist).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](developing.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur du contenu de définir les fragments de contenu compris dans la liste et les éléments de ces fragments à inclure.

### Onglet Propriétés

L’onglet **Propriétés** définit les fragments de contenu inclus dans la liste. Cela repose principalement sur un modèle de fragment de contenu sélectionné, mais il existe d’autres options de filtrage disponibles.

![](assets/screen-shot-2019-05-08-10.47.19.png)

* **Modèle** : chemin d’accès au modèle de fragment de contenu sur lequel repose la liste.
   * Par défaut, tous les fragments de contenu du modèle définis comme **chemin d’accès au modèle** sont inclus dans la liste.
* **Chemin d’accès parent** : chemin d’accès parent à partir duquel la liste doit être créée.
   * Les fragments de contenu reposant sur le **chemin d’accès au modèle** sélectionné sont filtrés sur ceux du **chemin d’accès parent** spécifié.
   * Cliquez ou appuyez sur le bouton **Boîte de dialogue Ouvrir la sélection** à droite du champ pour spécifier le chemin.
* **Balises** : seuls les fragments de contenu avec les balises spécifiées seront inclus dans la liste.
   * Cliquez ou appuyez sur le bouton **Boîte de dialogue Ouvrir la sélection** à droite du champ pour spécifier les balises.
   * Cliquez ou appuyez sur le X à côté des balises sélectionnées pour les supprimer.


### Onglet Éléments

Par défaut, tous les éléments du modèle de fragment de contenu sont inclus dans la liste. Les **éléments** vous permettent de spécifier que quelques éléments spécifiques à inclure.

![](assets/screen-shot-2019-05-08-10.47.34.png)

* **Éléments** : seuls les éléments des fragments de contenu figurant dans la liste spécifiée apparaissent.
   * Cliquez ou appuyez sur le bouton **Ajouter** pour ajouter un nouvel élément.
   * Cliquez ou appuyez sur le bouton **Supprimer** pour supprimer un élément sélectionné.
   * Faites glisser la poignée **Ordre** pour réorganiser l’ordre des éléments.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les styles appliqués au composant de liste de fragments de contenu.