---
title: Composant Bouton de formulaire
seo-title: Composant Bouton de formulaire
description: 'null'
seo-description: Le composant Formulaire de composant principal permet l'inclusion d'un champ masqué dans un formulaire.
uuid: 22 c 53 cd 0-d 0 bc -4 e 5 d -89 f 3-5 ac 4 f 61 a 9100
contentOwner: Utilisateur
content-type: référence
topic-tags: création
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: a 6 e 2974 a -243 f -40 ab -903 c-c 7 d 3 e 8615 bcc
disttype: dist5
gnavtheme: light
groupsectionnavitems: non
hidemerchandisingbar: inherit
hidepromocomponent: inherit
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1243d6cc1b0b015ee2f37ae89d0e2e42d366cc02

---


# Composant Bouton de formulaire{#form-button-component}

Le composant Bouton de formulaire principal permet l&#39;inclusion d&#39;un bouton pour déclencher une action sur une page.

## Utilisation {#usage}

Le composant Bouton de formulaire principal permet la création de champs de bouton, souvent pour déclencher l&#39;envoi du formulaire et est destiné à être utilisé avec le composant Conteneur [de formulaires](form-container.md).

Les propriétés de bouton peuvent être définies par l&#39;éditeur de contenu dans [la boîte de dialogue Configurer](form-button.md).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Bouton de formulaire est v 2, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018 et est décrite dans ce document.

Le tableau suivant détaille toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatible | Compatible | Compatible |
| [v1](form-button-v1.md) | Compatible | Compatible | Compatible |

Pour plus d&#39;informations sur les versions et les versions des composants principaux, consultez les versions des composants de Document [principaux](versions.md).

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple tiré de [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Capture d’écran {#screenshot}

![](assets/screen_shot_2018-01-12at120021.png)

### HTML {#html}

```
<div class="container responsivegrid aem-GridColumn aem-GridColumn--default--12">
<form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="cmp-form aem-Grid aem-Grid--12 aem-Grid--default--12">
    <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
    
    <div class="button aem-GridColumn aem-GridColumn--default--12">
<button type="BUTTON" class="cmp-form-button" name="loveToast" value="ILoveToast">Click here if you love toast!</button>
</div>

</form>
</div>
```

### JSON {#json}

```
"button":{  
                           "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                           ":type":"core/wcm/sandbox/components/form/button/v2/button",
                           "name":"loveToast",
                           "jcr:title":"Click here if you love toast!",
                           "type":"button",
                           "value":"ILoveToast"
                        }
```

### Détails techniques {#technical-details}

Vous trouverez la documentation technique la plus récente sur le composant [Form Button sur github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v2/button).

Vous trouverez plus d&#39;informations sur le développement des composants principaux dans la documentation destinée aux développeurs de composants [principaux](developing.md).

## Configurer le dialogue {#configure-dialog}

La boîte de dialogue Configurer permet à l&#39;auteur de contenu de définir les paramètres du bouton.

### Onglet Propriétés {#properties-tab}

![](assets/screen_shot_2018-01-12at120433.png)

* **Type**

   * **Bouton**
   * **Envoyer**

* **Titre** - Texte affiché sur le bouton

   * Si aucune valeur n&#39;est définie par défaut sur le type de bouton

* **Nom** : nom du bouton qui est envoyé avec les données du formulaire.
* **Valeur** - Valeur du bouton qui est envoyée avec les données du formulaire.

## Créer un dialogue {#design-dialog}

### Onglet Styles {#styles-tab}

Le composant Bouton de formulaire prend en charge le système [de style AEM](authoring.md#component-styling).