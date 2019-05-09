---
title: Composant masqué de formulaire
seo-title: Composant masqué de formulaire
description: 'null'
seo-description: Le composant Formulaire de composant principal masque l'affichage d'un champ masqué.
uuid: 63 a 1 b 381-f 45 c -4241-b 743-dea 8 abd 45 e 11
contentOwner: Utilisateur
content-type: référence
topic-tags: core-components
discoiquuid: 36 e 49035-7641-4 bad -8 a 61-723060032903
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
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Composant masqué de formulaire{#form-hidden-component}

Le composant Formulaire de composant principal masque l&#39;affichage d&#39;un champ masqué.

## Utilisation {#usage}

Le composant masqué Form Component Form (Composant masqué du formulaire) permet la création de champs masqués pour transmettre des informations sur la page actuelle à AEM et est destiné à être utilisé avec le composant de conteneur [de formulaires](form-container.md).

Les propriétés de champ peuvent être définies par l&#39;éditeur de contenu dans [la boîte de dialogue Configurer](form-hidden.md).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant Masqué de formulaire est v 2, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018 et est décrite dans ce document.

Le tableau suivant détaille toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatible | Compatible | Compatible |
| [v1](form-hidden-v1.md) | Compatible | Compatible | Compatible |

Pour plus d&#39;informations sur les versions et les versions des composants principaux, consultez les versions des composants de Document [principaux](versions.md).

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple tiré de [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### HTML {#html}

```
<div class="cmp cmp-form aem-GridColumn aem-GridColumn--default--12">
 <form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
  <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
   <div class="visible aem-GridColumn aem-GridColumn--default--12">
    <input type="hidden" id="ghostToast" name="Invisible Toast" value="ghostToast">
   </div>
 </form>
</div>
```

### JSON {#json}

```
"container": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "columnCount": 12,
              "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
              ":items": {
                "hidden": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/hidden",
                  "name": "Invisible Toast",
                  "id": "ghostToast",
                  "value": "ghostToast"
                }
              },
              ":itemsOrder": [
                "hidden"
              ],
              ":type": "weretail/components/form/container"
            }
```

### Détails techniques {#technical-details}

Vous trouverez la documentation technique la plus récente sur le composant [Masqué de formulaire sur github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v2/hidden).

Vous trouverez plus d&#39;informations sur le développement des composants principaux dans la documentation destinée aux développeurs de composants [principaux](developing.md).

## Configurer le dialogue {#configure-dialog}

La boîte de dialogue Configurer permet à l&#39;auteur de contenu de définir les paramètres du champ masqué.

![](assets/chlimage_1-26.png)

* **Nom Nom**
du champ qui est envoyé avec les données du formulaire
* **Valeur Valeur**
du champ, qui est envoyée avec les données du formulaire
* **Identifiant**
L&#39;identificateur doit être unique sur la page et peut être utilisé pour lier des scripts à ce champ de formulaire.

Etant donné que le composant Formulaire masqué ne comporte normalement aucun attribut visible, l&#39;espace réservé du composant dans l&#39;éditeur affiche les valeurs des champs **Nom** et **Valeur** si elles sont affectées pour aider l&#39;auteur à identifier le composant Masqué de formulaire approprié.

![](assets/screenshot_2018-10-19at094927.png)

## Créer un dialogue {#design-dialog}

Il n&#39;existe pas de dialogue de conception pour le composant Formulaire masqué.