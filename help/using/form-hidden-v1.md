---
title: Composant masqué de formulaire (v 1)
seo-title: Composant masqué de formulaire (v 1)
description: Le composant Formulaire de composant principal masque l'affichage d'un champ masqué.
seo-description: Le composant Formulaire de composant principal masque l'affichage d'un champ masqué.
uuid: f 5005346-def 5-4 e 1 f -8 f 93-e 4 cfc 67 a 9329
content-type: référence
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: d 35 f 4 e 71-ec 7 f -4128-9123-b 997 dbb 5 f 0 cf
index: n
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Composant masqué de formulaire (v 1){#form-hidden-component-v}

Le composant Formulaire de composant principal masque l&#39;affichage d&#39;un champ masqué.

## Utilisation {#usage}

Le composant masqué Form Component Form (Composant masqué du formulaire) permet la création de champs masqués pour transmettre des informations sur la page actuelle à AEM et est destiné à être utilisé avec le composant de conteneur [de formulaires](form-container.md).

Les propriétés de champ peuvent être définies par l&#39;éditeur de contenu dans [la boîte de dialogue Configurer](#configure-dialog).

## Version et compatibilité {#version-and-compatibility}

Ce document décrit la version v 1 du composant Masqué de formulaire, introduite à l&#39;origine avec la version 1.0.0 des composants principaux avec AEM 6.3.

Le tableau suivant répertorie la compatibilité de la version v 1 du composant masqué de formulaire.

| Version d’AEM | Composant masqué de formulaire v 1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Ce document décrit la version v 1 du composant Masqué de formulaire.
>
>Pour plus d&#39;informations sur la version actuelle du composant Masqué de formulaire, voir le document [du composant](form-hidden.md) masqué de formulaire.

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple tiré de [We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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

>[!NOTE]
>
>L&#39;exportation JSON à partir des composants principaux nécessite la version 1.1.0 des composants principaux. Pour plus d&#39;informations, consultez les [informations de compatibilité des composants principaux v 1](versions.md#release-history-and-compatibility) .

## Configurer le dialogue {#configure-dialog}

La boîte de dialogue Configurer permet à l&#39;auteur de contenu de définir les paramètres du champ masqué.

![](assets/chlimage_1-26.png)

* **Nom** : nom du champ qui est envoyé avec les données du formulaire.
* **Valeur** - Valeur du champ, qui est envoyée avec les données du formulaire
* **Identifiant** : l&#39;identifiant doit être unique sur la page et peut être utilisé pour lier des scripts à ce champ de formulaire.

## Créer un dialogue {#design-dialog}

Il n&#39;existe pas de dialogue de conception pour le composant Formulaire masqué.

## Détails techniques {#technical-details}

Vous trouverez la documentation technique la plus récente sur le composant [Masqué de formulaire sur github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v1/hidden).

Le projet de composants principaux peut être téléchargé depuis github.

Vous trouverez plus d&#39;informations sur le développement des composants principaux dans la documentation destinée aux développeurs de composants [principaux](developing.md).
