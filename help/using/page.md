---
title: Composant de page
seo-title: Composant de page
description: Le composant Page est un composant de page extensible conçu pour fonctionner avec l'éditeur de modèles et permet l'assemblage de composants d'en-tête/de pied de page et de structure à l'aide de l'éditeur de modèles.
seo-description: Le composant Page est un composant de page extensible conçu pour fonctionner avec l'éditeur de modèles et permet l'assemblage de composants d'en-tête/de pied de page et de structure à l'aide de l'éditeur de modèles.
uuid: 7052 a 5 b 1-e 7 f 1-4944-a 55 c-faf 739 b 6 e 89 c
contentOwner: Utilisateur
content-type: référence
topic-tags: création
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: cb 1 a 745 a -30 c 4-4 ad 6-a 04 f-fefb 3666 cd 95
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Composant de page{#page-component}

Le composant Page est un composant de page extensible conçu pour fonctionner avec l&#39;éditeur [de modèles](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) et permet l&#39;assemblage de composants d&#39;en-tête/de pied de page et de structure à l&#39;aide de l&#39;éditeur de modèles.

## Utilisation {#usage}

Le composant de page sert de base à toutes les pages conçues avec les composants principaux ainsi que les modèles modifiables. En utilisant le composant de page, les en-têtes, les pieds de page et la structure de la page peuvent être définis comme un modèle à l&#39;aide des autres composants principaux.

Grâce au dialogue [de conception](#design-dialog), les bibliothèques côté client personnalisées peuvent être définies pour la page. Contrairement aux autres composants dont le dialogue de modification est accessible directement à partir du composant, puisque le composant est la page elle-même, la [boîte de dialogue Modifier](#edit-dialog) du composant de page est la fenêtre des propriétés de la page.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de page est v 2, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018 et est décrite dans ce document.

Le tableau suivant détaille toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|---|---|---|---|
| [v2](page-v1.md) | Compatible | Compatible | Compatible |
| v1 | Compatible | Compatible | Compatible |

Pour plus d&#39;informations sur les versions et les versions des composants principaux, consultez les versions des composants de Document [principaux](versions.md).

>[!NOTE]
>
>Pour activer la redirection au `cq:Page` niveau de la version 2 du composant de page et d&#39;AEM 6.3, [le service Pack 2](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp2-release-notes.html) ou une version ultérieure est requis. Cette redirection n&#39;était pas disponible dans les versions précédentes.

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple tiré de [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Capture d’écran {#screenshot}

![](assets/chlimage_1.png)

### Détails techniques {#technical-details}

Vous trouverez la documentation technique la plus récente sur le composant [de page sur github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page).

Vous trouverez plus d&#39;informations sur le développement des composants principaux dans la documentation destinée aux développeurs de composants [principaux](developing.md).

## Modifier le dialogue {#edit-dialog}

Etant donné que le composant représente la page entière, les paramètres qui seraient normalement dans un dialogue de modification se trouvent dans [la fenêtre Propriétés](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-page-properties.html) de la page.

## Créer un dialogue {#design-dialog}

Etant donné que le composant représente la page entière, le dialogue de conception est accessible via **les informations de page -&gt; Stratégie de page** lors de la modification du modèle de page.

![](assets/screen_shot_2018-04-03at113410.png)

>[!NOTE]
>
>Dans les versions précédentes d&#39;AEM, **la stratégie** de page était appelée **Conception de page**.

### Onglet Propriétés {#properties-tab}

A l&#39;aide de la fenêtre Conception de page, vous pouvez définir les bibliothèques client à charger ainsi que la bibliothèque de ressources Web pour la page.

* **Bibliothèques
client** Cette option définit les catégories de bibliothèque client à charger. JavaScript est ajouté à la fin du corps et le CSS est ajouté à l&#39;en-tête de la page.
* **Bibliothèques client JavaScript En tête**
de page Ceci définit les catégories de bibliothèque Client JavaScript à charger dans l&#39;en-tête de la page.
   * Les catégories définies ici dans le champ Bibliothèques **client ont** le code JavaScript chargé dans l&#39;en-tête de la page et non dans la fin du corps.
   * Aucun CSS ne sera chargé, sauf si la catégorie est également présente dans **le champ Bibliothèques** client.

* **Bibliothèque**
cliente Ressources Web La catégorie Bibliothèque cliente sert à servir des ressources Web telles que les favicons.

![](assets/screenshot_2018-10-19at104949.png)

Les bibliothèques peuvent être configurées pour les champs Bibliothèques **client** et **Bibliothèques clientes JavaScript de** la manière suivante :

* Pour ajouter un nouveau champ, cliquez sur **le** bouton Ajouter ou appuyez dessus sous les champs.
* Pour supprimer un champ ou appuyer sur l&#39;icône de corbeille en regard du champ à supprimer.
* Pour réorganiser l&#39;ordre de chargement, cliquez ou appuyez et faites glisser la poignée en regard du champ à déplacer.

Pour plus d&#39;informations sur l&#39;utilisation des bibliothèques côté client, voir [Utilisation des bibliothèques côté client](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html).

>[!CAUTION]
>
>La possibilité de définir séparément les bibliothèques client pour l&#39;en-tête de page a été introduite avec la version 2.2.0 des composants principaux.

### Onglet Styles {#styles-tab}

Le composant Page prend en charge le système [de style AEM](authoring.md#component-styling).