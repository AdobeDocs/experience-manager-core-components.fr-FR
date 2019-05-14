---
title: Composant de chemin de navigation
seo-title: Composant de chemin de navigation
description: 'null'
seo-description: Le composant de navigation Composant principal est un composant de navigation qui crée un chemin de navigation des liens en fonction de l'emplacement de la page dans la hiérarchie du contenu.
uuid: 13 e 858 d 5-24 ad -4144-adc 4-0 fa 1 ffd 257 c 1
contentOwner: Utilisateur
content-type: référence
topic-tags: création
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: prêt 237 df -08 b 8-4 deb -9881-66 a 1 f 0 d 65 ef 3
modalsize: 426x240
translation-type: tm+mt
source-git-commit: 1243d6cc1b0b015ee2f37ae89d0e2e42d366cc02

---


# Composant de chemin de navigation{#breadcrumb-component}

Le composant de navigation Composant principal est un composant de navigation qui crée un chemin de navigation des liens en fonction de l&#39;emplacement de la page dans la hiérarchie du contenu.

## Utilisation {#usage}

Le composant de chemin de navigation affiche la position de la page actuelle dans la hiérarchie du site, ce qui permet aux visiteurs de la page de parcourir la hiérarchie de la page à partir de leur emplacement actuel. Cela est souvent intégré aux en-têtes ou aux pieds de page.

Les options disponibles, telles que le niveau de navigation par défaut et la possibilité d&#39;afficher la page ou les pages masquées, peuvent être définies par l&#39;auteur du modèle dans la boîte de dialogue [de conception](#design-dialog). L&#39;éditeur de contenu peut ensuite choisir si les pages masquées doivent être affichées ou non et le niveau de navigation réel du composant dans la boîte de dialogue [Modifier](#edit-dialog).

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de chemin de navigation est v 2, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018 et est décrite dans ce document.

Le tableau suivant détaille toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatible | Compatible | Compatible |
| [v1](breadcrumb-v1.md) | Compatible | Compatible | Compatible |

Pour plus d&#39;informations sur les versions et les versions des composants principaux, consultez les versions des composants de Document [principaux](versions.md).

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple tiré de [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Capture d’écran {#screenshot}

![](assets/chlimage_1.png)

### HTML {#html}

```
<nav class="cmp-breadcrumb">
    <ol class="cmp-breadcrumb__list">
        <li class="cmp-breadcrumb__item">
            <a href="/content/we-retail/us.html" class="cmp-breadcrumb__item-link">
                United States
            </a>
        </li>
    
        <li class="cmp-breadcrumb__item">
            <a href="/content/we-retail/us/en.html" class="cmp-breadcrumb__item-link">
                English
            </a>
        </li>
    
        <li class="cmp-breadcrumb__item cmp-breadcrumb__item--active">
            
                Experience
            
        </li>
    </ol>
</nav>
```

### JSON {#json}

```
"breadcrumb":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     "items":[  
                        {  
                           "page":{  
                              "path":"/content/we-retail/us",
                              "pageTitle":null,
                              "name":"us",
                              "description":null,
                              "title":"United States"
                           },
                           "active":false
                        },
                        {  
                           "page":{  
                              "path":"/content/we-retail/us/en",
                              "pageTitle":null,
                              "name":"en",
                              "description":null,
                              "title":"English"
                           },
                           "active":false
                        },
                        {  
                           "page":{  
                              "path":"/content/we-retail/us/en/experience",
                              "pageTitle":null,
                              "name":"experience",
                              "description":null,
                              "title":"Experience"
                           },
                           "active":true
                        }
                     ],
                     ":type":"weretail/components/content/breadcrumb"
                  }
```

>[!NOTE]
>
>A compter de la version 2.1.0 de Core Components, le composant de chemin de navigation prend en charge [schema.org des microdonnées](https://schema.org/BreadcrumbList).

### Détails techniques {#technical-details}

Vous trouverez la documentation technique la plus récente sur le composant [de chemin de navigation sur github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb).

Vous trouverez plus d&#39;informations sur le développement des composants principaux dans la documentation destinée aux développeurs de composants [principaux](developing.md).

## Modifier le dialogue {#edit-dialog}

Le dialogue Modifier permet à l&#39;auteur de contenu de supprimer les pages masquées et actives dans les chemins de navigation ainsi que la profondeur de la hiérarchie qu&#39;elle doit afficher.

![](assets/screen_shot_2018-01-12at124250.png)

* **Niveau de début de navigation** : dans la hiérarchie, le composant de chemin de navigation doit commencer à descendre jusqu&#39;à la page en cours. Par exemple dans We. Retail :

   * 0 commence à `/content`

   * 1 commence à `/content/we-retail`
   * 2 commence à `/content/we-retail/<country>`

* **Afficher les éléments de navigation masqués** - Afficher les pages marquées comme masquées dans la barre de navigation (elles ne sont pas affichées par défaut)
* **Masquer la page actuelle**- Supprimer la page active dans la barre de navigation (par défaut, elle s&#39;affiche)

## Créer un dialogue {#design-dialog}

Le dialogue de conception permet à l&#39;auteur du modèle de définir les valeurs par défaut des options de suppression des pages masquées et actives dans les chemins de navigation, ainsi que la profondeur de la hiérarchie qu&#39;elle doit afficher.

### Onglet principal {#main-tab}

![](assets/screen_shot_2018-01-12at124437.png)

* **Niveau de début de navigation** : définit la valeur par défaut pour laquelle le composant de chemin de navigation doit commencer à se déplacer jusqu&#39;à la page en cours lorsque le composant de chemin de navigation est ajouté à une page.
* **Afficher les éléments de navigation masqués** : définit la valeur par défaut de l&#39;option **Afficher les éléments** de navigation masqués lorsque le composant de chemin de navigation est ajouté à une page.

   * Elle n&#39;active pas ou ne désactive pas l&#39;option de l&#39;auteur. Il définit uniquement la valeur par défaut.

* **Masquer la page actuelle**: définit la valeur par défaut de l&#39;option **Masquer la page** en cours lorsque le composant de chemin de navigation est ajouté à une page.

   * Elle n&#39;active pas ou ne désactive pas l&#39;option de l&#39;auteur. Il définit uniquement la valeur par défaut.

### Onglet Styles {#styles-tab}

Le composant de chemin de navigation prend en charge le système [de style AEM](authoring.md#component-styling).