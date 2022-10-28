---
title: Composant de fragment d’expérience de courrier électronique
description: Le composant de fragment d’expérience de courrier électronique permet à l’auteur de contenu de placer une variation de fragment d’expérience dans son contenu tout en prenant en charge une structure de contenu localisée.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '927'
ht-degree: 27%

---


# Composant de fragment d’expérience de courrier électronique {#email-experience-fragment-component}

Le composant de fragment d’expérience de courrier électronique permet à l’auteur de contenu de placer une variation de fragment d’expérience dans son contenu tout en prenant en charge une structure de contenu localisée.

## Utilisation {#usage}

Le composant de fragment d’expérience de courrier électronique permet à l’auteur de contenu de sélectionner des variations de fragment d’expérience existantes et d’en placer une dans le contenu. Un fragment d’expérience est un groupe de contenu qui comprend du contenu et une mise en page et qui est réutilisable sur plusieurs canaux.

* Les propriétés du composant peuvent être définies dans la [boîte de dialogue de configuration](#configure-dialog).
* Les valeurs par défaut du composant lors de son ajout au contenu peuvent être définies dans la variable [boîte de dialogue de conception](#design-dialog).

Le composant Fragment d’expérience de courrier électronique prend en charge une structure de site localisée.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de fragment d’expérience de courrier électronique est v1, qui a été introduite avec la version X des composants principaux du courrier électronique en octobre 2022. Elle est décrite dans ce document.

Le tableau ci-après présente en détail toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatible | Compatible |

Pour plus d’informations sur les versions et versions des composants principaux de messagerie, consultez le document . [Envoi des versions des composants principaux par courrier électronique.](/help/email/versions.md)

## Prise en charge de la structure de site localisée {#localized-site-structure}

Le composant de fragment d’expérience de courrier électronique est adaptatif aux structures de contenu localisées et effectue le rendu du fragment d’expérience approprié en fonction de la localisation du contenu. Pour ce faire, le fragment d’expérience doit respecter les conditions suivantes.

* Le composant de fragment d’expérience de courrier électronique est ajouté à une [modèle de page.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/templates.html)
* Ce modèle est utilisé pour créer une page de contenu qui fait partie d’une structure localisée sous `/content/<site>`.
* Le fragment d’expérience référencé sur une page de contenu fait partie d’une structure de fragment d’expérience localisée sous `/content/experience-fragments` qui suit les mêmes schémas que le site ci-dessous `/content/<site>` en utilisant les mêmes noms de composant.

Dans ce cas, le fragment avec la même localisation ([langue, plan directeur ou Live Copy](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/reusing-content/msm-and-translation.html)), car la page active est rendue dans le modèle.

Ce comportement est limité aux composants de fragment d’expérience de courrier électronique ajoutés aux modèles. Les composants de fragment d’expérience ajoutés à des pages de contenu individuelles affichent les rendus de fragment d’expérience exacts configurés dans le composant.

* Pour un exemple du fonctionnement des fonctions de localisation du composant de fragment d’expérience, voir [la section ci-dessous](#example).
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

Dans ce cas, si le composant Fragment d’expérience de courrier électronique `/content/experience-fragments/wknd/us/en/footerTextXf` est placé sur un modèle, les pages localisées créées à partir de ce modèle affichent automatiquement le fragment d’expérience localisé correspondant à la page de contenu localisée.

Ainsi, si vous accédez à une page de contenu sous `/content/wknd/ch/de` qui utilise le même modèle, on obtiendra `/content/experience-fragments/wknd/ch/de/footerTextXf` comme rendu au lieu de `/content/experience-fragments/wknd/us/en/footerTextXf`.

### Secours {#fallback}

Le composant de fragment d’expérience de courrier électronique tentera de trouver un composant localisé correspondant dans l’ordre suivant.

1. Il tente d’abord de trouver une racine de langue.
1. Si elle est introuvable, il tente de trouver un plan directeur.
1. S’il est introuvable, il tente de trouver une live copy.
1. S’il est introuvable, il correspond par défaut au fragment d’expérience configuré dans le composant.

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant de fragment d’expérience de courrier électronique et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la page [Bibliothèque de composants.](https://adobe.com/go/aem_cmp_library_email_xf)

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant de fragment d’expérience [se trouve sur GitHub.](https://adobe.com/go/aem_cmp_email_tech_xf_v1)

Vous trouverez plus d’informations sur le développement des composants principaux dans la section [Documentation destinée aux développeurs sur les composants principaux.](/help/developing/overview.md)

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de sélectionner la variation de fragment d’expérience qui doit être rendue dans le contenu.

![Boîte de dialogue de modification du composant Fragment d’expérience de courrier électronique](/help/email/assets/email-experience-fragment-edit.png)

Utilisez la variable **Boîte de dialogue Ouvrir la sélection** pour ouvrir le sélecteur de composants afin de choisir la variation de composant Fragment d’expérience à ajouter à la page de contenu.

Si vous ajoutez le composant de fragment d’expérience de courrier électronique à un modèle, il sera automatiquement localisé à condition que les fragments d’expérience soient localisés. Par conséquent, le rendu sur la page peut différer du composant que vous sélectionnez explicitement. Pour plus d’informations, [reportez-vous à l’exemple ci-dessus](#example).

Vous pouvez également définir un **ID**. Cette option permet de contrôler l’identifiant unique du composant dans le fichier HTM.

* Si rien n’est indiqué, un identifiant unique est automatiquement généré et peut être trouvé en examinant le contenu qui en résulte.
* Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
* La modification de l’ID peut avoir un impact sur CSS.

### Onglet Styles {#styles-tab-edit}

Le composant Fragment d’expérience de courrier électronique prend en charge l’AEM [Système de style.](/help/get-started/authoring.md#component-styling)

Utilisez la liste déroulante pour sélectionner les styles à appliquer au composant. Les sélections effectuées dans la boîte de dialogue de modification ou dans la barre d’outils du composant ont le même effet.

Les styles doivent être configurés pour ce composant dans la variable [boîte de dialogue de conception](#design-dialog) pour que l’onglet soit disponible.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les options disponibles pour l’auteur du contenu qui utilise le composant Fragment d’expérience de courrier électronique et les valeurs par défaut définies lors du placement du composant Fragment d’expérience de courrier électronique.

### Onglet Styles {#styles-tab}

Le composant Fragment d’expérience de courrier électronique prend en charge l’AEM [Système de style.](/help/get-started/authoring.md#component-styling)
