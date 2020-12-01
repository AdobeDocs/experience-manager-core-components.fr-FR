---
title: Composant de fragment d’expérience
description: Le composant de fragment d’expérience permet à l’auteur de contenu d’ajouter une variation de fragment d’expérience à une page.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 100%

---


# Composant de fragment d’expérience{#experience-fragment-component}

Le composant de fragment d’expérience de composant principal permet à l’auteur du contenu de placer une variation de fragment d’expérience sur une page tout en prenant en charge une structure de site localisée.

## Utilisation {#usage}

Le composant de fragment d’expérience des composants principaux permet à l’auteur du contenu d’effectuer une sélection parmi les variations de fragments d’expérience existantes et d’en placer une dans la page de contenu. Le composant de fragment d’expérience prend également en charge une structure de site localisée.

* Les propriétés du composant peuvent être définies dans la [boîte de dialogue de configuration](#configure-dialog).
* Les valeurs par défaut du composant lors de son ajout à une page peuvent être définies dans la [boîte de dialogue de conception](#design-dialog).

## Prise en charge de la structure de site localisée {#localized-site-structure}

Le composant de fragment d’expérience s’adapte aux structures localisées du site et assure le rendu du fragment d’expérience approprié en fonction de la localisation de la page. Pour ce faire, le fragment d’expérience doit respecter les conditions suivantes.

* Le composant de fragment d’expérience est ajouté à un modèle.
* Ce modèle est utilisé pour créer une page de contenu qui fait partie d’une structure localisée sous `/content/<site>`.
* Le fragment d’expérience référencé sur une page de contenu fait partie d’une structure de fragment d’expérience localisée sous `/content/experience-fragments` qui suit les mêmes schémas que le site sous `/content/<site>`, y compris l’utilisation des mêmes noms de composant.

Dans ce cas, le fragment avec la même localisation (langue, plan directeur ou live copy) que la page active est rendu dans le modèle.

Ce comportement est limité aux composants de fragments d’expérience ajoutés aux modèles. Les composants de fragments d’expérience ajoutés aux pages de contenu individuelles affichent les rendus de fragments d’expérience exacts configurés dans le composant.

* Pour un exemple du fonctionnement des fonctions de localisation du composant de fragment d’expérience, reportez-vous à [la section ci-dessous](#example).
* Pour un exemple de la façon dont les fonctions de localisation des composants principaux fonctionnent ensemble, reportez-vous à la page [Fonctions de localisation de la page Composants principaux](/help/get-started/localization.md).

### Exemple {#example}

Imaginons que votre contenu ressemble à ceci :

```
/content
+-- experience-fragments
   \-- wknd
      +-- language-masters
      +-- us
         +-- en
            +-- footerTextXf
            \-- headerTextXf
         \-- es
            +-- footerTextXf
            \-- headerTextXf
      \-- ch
         +-- de
            +-- footerTextXf
            \-- headerTextXf
         +-- fr
            +-- footerTextXf
            \-- headerTextXf
         \-- it
            +-- footerTextXf
            \-- headerTextXf
+-- wknd
   +-- language-masters
   +-- us
      +-- en
      \-- es
   +-- ch
      +-- de
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

Notez que la structure sous `/content/experience-fragments/wknd` reflète la structure de `/content/wknd`.

Dans ce cas, si le composant de fragment d’expérience `/content/experience-fragments/wknd/us/en/footerTextXf` est placé sur un modèle, les pages localisées créées à partir de ce modèle afficheront automatiquement le fragment d’expérience localisé correspondant à la page de contenu localisée.

Ainsi, si vous accédez à une page de contenu sous `/content/wknd/ch/de` qui utilise le même modèle, on obtiendra `/content/experience-fragments/wknd/ch/de/footerTextXf` comme rendu au lieu de `/content/experience-fragments/wknd/us/en/footerTextXf`.

### Secours {#fallback}

Le composant de fragment d’expérience tentera de trouver un composant localisé correspondant dans l’ordre suivant.

1. Il tente d’abord de trouver une racine de langue.
1. Si elle est introuvable, il tente de trouver un plan directeur.
1. S’il est introuvable, il tente de trouver une live copy.
1. Si elle est introuvable, il correspond par défaut au fragment d’expérience configuré dans le composant.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de fragment d’expérience est v1, qui a été introduite avec la version 2.6.0 des composants principaux en septembre 2019. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible | Compatible | Compatible |

Pour plus d’informations sur les versions et les publications des composants principaux, voir le document sur les [versions des composants principaux](/help/versions.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant de fragment d’expérience et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library_xf).

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant de fragment d’expérience [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_xf_v1).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de sélectionner la variation de fragment d’expérience qui doit être rendue sur la page.

![Boîte de dialogue de modification du composant Fragment d’expérience](/help/assets/experience-fragment-edit.png)

Utilisez le bouton **Ouvrir la boîte de dialogue de sélection** pour ouvrir le sélecteur de composants afin de choisir la variation de composant de fragment d’expérience à ajouter à la page de contenu.

Si vous ajoutez le composant de fragment d’expérience à un modèle, notez qu’il sera automatiquement localisé à condition que les fragments d’expérience soient localisés. Ainsi, ce qui est généré sur la page peut différer du composant que vous sélectionnez explicitement. Pour plus d’informations, [reportez-vous à l’exemple ci-dessus](#example).

Vous pouvez également définir un **ID**. Cette option permet de contrôler l’identifiant unique du composant dans le code HTML et dans la [couche de données](/help/developing/data-layer/overview.md).

* Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
* Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
* La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les options disponibles pour l’auteur du contenu qui utilise le composant de fragment d’expérience et les valeurs par défaut définies lors du placement de celui-ci.

### Onglet Styles {#styles-tab}

Le composant de fragment d’expérience prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.
