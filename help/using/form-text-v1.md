---
title: Composant de texte de formulaire (v 1)
seo-title: Composant de texte de formulaire (v 1)
description: 'null'
seo-description: Le composant Texte de formulaire principal permet l'entrée de texte de formulaire pour envoi.
uuid: 30123 aba -57 a 8-4 ed 4-93 cb -6 a 3 d 2 edff 9 a 7
content-type: référence
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: bd 4 e 9930-4 d 81-49 ae-a 3 d 1-9 a 8740418 dae
index: n
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Composant de texte de formulaire (v 1){#form-text-component-v}

Le composant Texte de formulaire principal permet l&#39;entrée de texte de formulaire pour envoi.

## Utilisation {#usage}

Le composant de texte de formulaire permet l&#39;envoi de différents types de texte et est conçu pour être utilisé avec le composant de conteneur [de formulaires](form-container.md).

Le type de validation de texte, d&#39;étiquettes et d&#39;aide peut être défini par l&#39;éditeur de contenu dans [la boîte de dialogue Configurer](form-text-v1.md#main-pars_title).

## Version et compatibilité {#version-and-compatibility}

Ce document décrit la version v 1 du composant de texte de formulaire, introduite à l&#39;origine avec la version 1.0.0 des composants principaux avec AEM 6.3.

Le tableau suivant répertorie la compatibilité de la version v 1 du composant de texte de formulaire.

| Version d’AEM | Composant de texte de formulaire v 1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Ce document décrit la version v 1 du composant de texte de formulaire.
>
>Pour plus d&#39;informations sur la version actuelle du composant de texte de formulaire, voir [le document Composant](form-text.md) de texte de formulaire.

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple tiré de [We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Capture d’écran {#screenshot}

![](assets/chlimage_1-22.png)

### HTML {#html}

```
<div class="cmp cmp-form aem-GridColumn aem-GridColumn--default--12">
 <form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
     <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
     <div class="cmp cmp-form-field aem-GridColumn aem-GridColumn--default--12">
   <div class="form-group">
       <label for="form-text-978484744">How many pieces of toast would you like?</label>
          <input type="number" id="form-text-978484744" name="pieces">
   </div>
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
                "text": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/text",
                  "name": "piecesOfToast",
                  "jcr:title": "How many pieces of toast would you like?",
                  "type": "number",
                  "rows": "2"
                }
              },
              ":itemsOrder": [
                "text"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>L&#39;exportation JSON à partir des composants principaux nécessite la version 1.1.0 des composants principaux. Pour plus d&#39;informations, consultez les [informations de compatibilité des composants principaux v 1](versions.md#main-pars_title_236368006) .

## Configurer le dialogue {#configure-dialog}

La boîte de dialogue Configurer permet à l&#39;auteur de contenu de définir le type de texte à saisir, ainsi que les valeurs et étiquettes par défaut.

### Principal {#main}

![](assets/chlimage_1-23.png)

* **Contrainte** - Type de texte à saisir et validé par rapport à

   * **Texte**
   * **Zone de texte**
   * **Courriel**
   * **Téléphone**
   * **Date**
   * **Nombre**
   * **Mot de passe**

* **Lignes de texte** - Nombre de lignes à afficher dans la zone de texte (affiché uniquement lorsque **la contrainte** est définie sur **Zone de texte**)

* **Étiquette** - Libellé qui s&#39;affiche pour le champ
* **Masquer l&#39;étiquette d&#39;être affichée** - Nécessaire si l&#39;étiquette est requise uniquement à des fins d&#39;accessibilité et ne part pas d&#39;informations visuelles supplémentaires sur le champ
* **Nom d&#39;élément** : nom du champ envoyé avec les données du formulaire.
* **Valeur** - Valeur par défaut prérenseignée dans le champ

### À propos {#about}

![](assets/chlimage_1-24.png)

* **Message d&#39;aide** - Conseil à l&#39;intention de l&#39;utilisateur qui peut être saisi dans le champ
* **Afficher le message d&#39;aide comme espace réservé** - Pour afficher le message d&#39;aide à l&#39;intérieur de l&#39;entrée de formulaire lorsqu&#39;il est vide et non ciblé

### Contraintes {#constraints}

![](assets/chlimage_1-25.png)

* **Message de contrainte**

   * Message affiché sous forme d’info-bulle lors de l’envoi du formulaire si la valeur ne valide pas le type sélectionné
   * Non affiché pour **les types de contraintes de zone** **de texte** et de texte

* **Obligatoire** - Si l&#39;utilisateur sélectionné doit remplir une valeur avant d&#39;envoyer le formulaire
* **Make Read only** - If selected the user can not modify the value of the field

## Créer un dialogue {#design-dialog}

Il n&#39;existe pas de dialogue de conception pour le composant Texte de formulaire.

## Détails techniques {#technical-details}

Vous trouverez la documentation technique la plus récente sur le composant [de texte de formulaire sur github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v1/text).

Le projet de composants principaux peut être téléchargé depuis github.

Vous trouverez plus d&#39;informations sur le développement des composants principaux dans la documentation destinée aux développeurs de composants [principaux](developing.md).
