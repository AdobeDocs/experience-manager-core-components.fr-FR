---
title: Composant Fragment d’expérience d’e-mail
description: Le composant Fragment d’expérience d’e-mail permet au créateur du contenu de placer une variation de fragment d’expérience sur une page tout en prenant en charge une structure de site localisée.
role: Architect, Developer, Admin, User
exl-id: 861c1fd1-6d6d-426c-a338-a558326fe16e
source-git-commit: e5afead6bfdcc59cbd6da888f4e1e36038c6c0f8
workflow-type: tm+mt
source-wordcount: '862'
ht-degree: 100%

---


# Composant Fragment d’expérience d’e-mail {#email-experience-fragment-component}

Le composant Fragment d’expérience d’e-mail permet au créateur du contenu de placer une variation de fragment d’expérience sur une page tout en prenant en charge une structure de site localisée.

## Utilisation {#usage}

Le composant Fragment d’expérience d’e-mail permet au créateur de contenu d’effectuer une sélection parmi les variations de fragments d’expérience existantes et d’en placer une dans le contenu. Un fragment d’expérience est un groupe de contenu qui comprend du contenu et une mise en page. Il est réutilisable sur plusieurs canaux.

* Les propriétés du composant peuvent être définies dans la [boîte de dialogue de configuration](#configure-dialog).
* Les valeurs par défaut du composant lors de son ajout à du contenu peuvent être définies dans la [boîte de dialogue de conception](#design-dialog).

Le composant Fragment d’expérience d’e-mail prend également en charge une structure de site localisée.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Fragment d’expérience d’e-mail est v1. Celle-ci a été introduite avec la version X des composants principaux d’e-mail en octobre 2022. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatible | - |

Pour plus d’informations sur les versions et les publications des composants principaux d’e-mail, voir le document sur les [versions des composants principaux d’e-mail.](/help/email/versions.md)

## Prise en charge de la structure de site localisée {#localized-site-structure}

Le composant Fragment d’expérience d’e-mail s’adapte aux structures de contenu localisées du site et assure le rendu du fragment d’expérience approprié en fonction de la localisation du contenu. Pour ce faire, le fragment d’expérience doit respecter les conditions suivantes.

* Le composant Fragment d’expérience d’e-mail est ajouté à un [modèle de page.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/templates.html?lang=fr)
* Ce modèle est utilisé pour créer une page de contenu qui fait partie d’une structure localisée sous `/content/<site>`.
* Le fragment d’expérience référencé sur une page de contenu fait partie d’une structure de fragment d’expérience localisée sous `/content/experience-fragments`. Celle-ci suit les mêmes modèles que le site sous `/content/<site>`, y compris l’utilisation des mêmes noms de composant.

Dans ce cas, le fragment ayant la même localisation ([langue, plan directeur ou Live Copy](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/reusing-content/msm-and-translation.html?lang=fr)) que la page active est rendu dans le modèle.

Ce comportement est limité aux composants Fragment d’expérience d’e-mail ajoutés aux modèles. Les composants Fragment d’expérience ajoutés à des pages de contenu individuelles afficheront le rendu exact des fragments d’expérience configurés dans le composant.

* Pour un exemple du fonctionnement des fonctions de localisation du composant Fragment d’expérience, reportez-vous à [la section ci-dessous](#example).
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

Dans ce cas, si le composant Fragment d’expérience d’e-mail `/content/experience-fragments/wknd/us/en/footerTextXf` est placé sur un modèle, les pages localisées créées à partir de ce modèle rendront automatiquement le fragment d’expérience localisé correspondant à la page de contenu localisée.

Ainsi, si vous accédez à une page de contenu sous `/content/wknd/ch/de` qui utilise le même modèle, on obtiendra `/content/experience-fragments/wknd/ch/de/footerTextXf` comme rendu au lieu de `/content/experience-fragments/wknd/us/en/footerTextXf`.

### Secours {#fallback}

Le composant Fragment d’expérience d’e-mail tentera de trouver un composant localisé correspondant dans l’ordre suivant.

1. Il tente d’abord de trouver une racine de langue.
1. Si elle est introuvable, il tente de trouver un plan directeur.
1. S’il est introuvable, il tente de trouver une live copy.
1. S’il est introuvable, il correspond par défaut au fragment d’expérience configuré dans le composant.

## Détails techniques {#technical-details}

Consultez la dernière [documentation technique sur le composant de fragment d’expérience](https://www.adobe.com/go/aem_cmp_xf_v1_fr).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux.](/help/developing/overview.md)

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet au créateur de contenu de sélectionner la variation de fragment d’expérience qui doit être rendue dans le contenu.

![Boîte de dialogue de modification du composant Fragment d’expérience d’e-mail](/help/email/assets/email-experience-fragment-edit.png)

Utilisez le bouton **Ouvrir la boîte de dialogue de sélection** pour ouvrir le sélecteur de composants afin de choisir la variation de composant de fragment d’expérience à ajouter à la page de contenu.

Si vous ajoutez le composant Fragment d’expérience d’e-mail à un modèle, notez qu’il sera automatiquement localisé à condition que les fragments d’expérience soient localisés. Ainsi, ce qui est généré sur la page peut différer du composant que vous sélectionnez explicitement. Pour plus d’informations, [reportez-vous à l’exemple ci-dessus](#example).

Vous pouvez également définir un **ID**. Cette option permet de contrôler l’identifiant unique du composant dans le HTM.

* Si rien n’est indiqué, un ID unique est généré automatiquement pour vous. Vous le trouverez en examinant le contenu obtenu.
* Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
* La modification de l’ID peut avoir un impact sur CSS.

### Onglet Styles {#styles-tab-edit}

Le composant Fragment d’expérience d’e-mail prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.

Utilisez la liste déroulante pour sélectionner les styles à appliquer au composant. Les sélections effectuées dans la boîte de dialogue de modification ou dans la barre d’outils du composant ont le même effet.

Pour accéder à l’onglet, les styles doivent être configurés pour ce composant dans la [boîte de dialogue de conception](#design-dialog).

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet au créateur du modèle de définir les options disponibles pour le créateur de contenu qui utilise le composant de fragment d’expérience d’e-mail et les valeurs par défaut définies lors du placement du composant.

### Onglet Styles {#styles-tab}

Le composant de fragment d’expérience d’e-mail prend en charge le [système de style](/help/get-started/authoring.md#component-styling) AEM.
