---
title: Composant de navigation dans la langue
seo-title: Composant de navigation dans la langue
description: 'null'
seo-description: Le composant de navigation linguistique fournit une navigation par langue/pays pour un site, de sorte que les visiteurs puissent accéder à la même page dans un autre paramètre régional.
uuid: ce 736458-9 cdf -4 bc 2-b 90 f -9 c 5 a 62 fe 1 ca 0
content-type: référence
topic-tags: création
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 8 f 232 eb 0-65 d 5-4075-8668-75 f 1366882 c 8
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


# Composant de navigation dans la langue{#language-navigation-component}

Le composant Navigation dans la langue fournit une navigation par langue/pays pour un site, de sorte que les visiteurs puissent accéder à la même page dans un autre paramètre régional.

## Utilisation {#usage}

Souvent, les sites Web sont fournis en plusieurs langues pour différentes régions. Le composant de navigation de langue permet à un visiteur d&#39;afficher la même page dans différentes langues/langues.

Le [dialogue Modifier](#edit-dialog) permet la définition de la racine de navigation globale ainsi que la profondeur de la structure de navigation. A l&#39;aide de [la boîte de dialogue de conception](#design-dialog), l&#39;auteur du modèle peut définir les valeurs par défaut des mêmes options.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de navigation en langage est v 1, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018 et est décrite dans ce document.

Le tableau suivant détaille toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Compatible | Compatible | Compatible |


Pour plus d&#39;informations sur les versions et les versions des composants principaux, consultez les versions des composants de Document [principaux](versions.md).

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple tiré de [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Capture d’écran {#screenshot}

![](assets/screen_shot_2018-01-12at133119.png)

### HTML {#html}

```
<nav class="cmp-languagenavigation">
    <ul class="cmp-languagenavigation__group">
        
    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--langcode-en cmp-languagenavigation__item--level-0 cmp-languagenavigation__item--active">
        
    <span class="cmp-languagenavigation__item-title" lang="en">United States</span>

    <ul class="cmp-languagenavigation__group">
        
    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--langcode-en cmp-languagenavigation__item--level-1 cmp-languagenavigation__item--active">

    <a class="cmp-languagenavigation__item-link" href="/content/we-retail/us/en/equipment.html" hreflang="en" lang="en" rel="alternate" title="English">English</a>

    </li>

    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--langcode-es cmp-languagenavigation__item--level-1">

    <a class="cmp-languagenavigation__item-link" href="/content/we-retail/us/es.html" hreflang="es" lang="es" rel="alternate" title="Español">Español</a>

    </li>

    </ul>

    </li>

    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--countrycode-CA cmp-languagenavigation__item--langcode-en-CA cmp-languagenavigation__item--level-0">
        
    <span class="cmp-languagenavigation__item-title" lang="en-CA">Canada</span>

    <ul class="cmp-languagenavigation__group">
        
    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--countrycode-CA cmp-languagenavigation__item--langcode-en-CA cmp-languagenavigation__item--level-1">

    <a class="cmp-languagenavigation__item-link" href="/content/we-retail/ca/en/equipment.html" hreflang="en-CA" lang="en-CA" rel="alternate" title="English">English</a>

    </li>

    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--countrycode-CA cmp-languagenavigation__item--langcode-en-CA cmp-languagenavigation__item--level-1">

    <a class="cmp-languagenavigation__item-link" href="/content/we-retail/ca/fr.html" hreflang="en-CA" lang="en-CA" rel="alternate" title="Français">Français</a>

    </li>

    </ul>

    </li>

    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--countrycode-CH cmp-languagenavigation__item--langcode-de-CH cmp-languagenavigation__item--level-0">
        
    <span class="cmp-languagenavigation__item-title" lang="de-CH">Switzerland</span>

    <ul class="cmp-languagenavigation__group">
        
    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--countrycode-CH cmp-languagenavigation__item--langcode-de-CH cmp-languagenavigation__item--level-1">

    <a class="cmp-languagenavigation__item-link" href="/content/we-retail/ch/de.html" hreflang="de-CH" lang="de-CH" rel="alternate" title="Deutsch">Deutsch</a>

    </li>

    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--countrycode-CH cmp-languagenavigation__item--langcode-de-CH cmp-languagenavigation__item--level-1">

    <a class="cmp-languagenavigation__item-link" href="/content/we-retail/ch/fr.html" hreflang="de-CH" lang="de-CH" rel="alternate" title="Français">Français</a>

    </li>

    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--countrycode-CH cmp-languagenavigation__item--langcode-de-CH cmp-languagenavigation__item--level-1">

    <a class="cmp-languagenavigation__item-link" href="/content/we-retail/ch/it.html" hreflang="de-CH" lang="de-CH" rel="alternate" title="Italiano">Italiano</a>

    </li>

    </ul>

    </li>

    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--langcode-de cmp-languagenavigation__item--level-0">
        
    <span class="cmp-languagenavigation__item-title" lang="de">Germany</span>

    <ul class="cmp-languagenavigation__group">
        
    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--langcode-de cmp-languagenavigation__item--level-1">

    <a class="cmp-languagenavigation__item-link" href="/content/we-retail/de/de.html" hreflang="de" lang="de" rel="alternate" title="Deutsch">Deutsch</a>

    </li>

    </ul>

    </li>

    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--langcode-fr cmp-languagenavigation__item--level-0">
        
    <span class="cmp-languagenavigation__item-title" lang="fr">France</span>

    <ul class="cmp-languagenavigation__group">
        
    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--langcode-fr cmp-languagenavigation__item--level-1">

    <a class="cmp-languagenavigation__item-link" href="/content/we-retail/fr/fr.html" hreflang="fr" lang="fr" rel="alternate" title="Français">Français</a>

    </li>

    </ul>

    </li>

    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--langcode-es cmp-languagenavigation__item--level-0">
        
    <span class="cmp-languagenavigation__item-title" lang="es">Spain</span>

    <ul class="cmp-languagenavigation__group">
        
    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--langcode-es cmp-languagenavigation__item--level-1">

    <a class="cmp-languagenavigation__item-link" href="/content/we-retail/es/es.html" hreflang="es" lang="es" rel="alternate" title="Español">Español</a>

    </li>

    </ul>

    </li>

    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--langcode-it cmp-languagenavigation__item--level-0">
        
    <span class="cmp-languagenavigation__item-title" lang="it">Italy</span>

    <ul class="cmp-languagenavigation__group">
        
    <li class="cmp-languagenavigation__item cmp-languagenavigation__item--langcode-it cmp-languagenavigation__item--level-1">

    <a class="cmp-languagenavigation__item-link" href="/content/we-retail/it/it.html" hreflang="it" lang="it" rel="alternate" title="Italiano">Italiano</a>

    </li>

    </ul>

    </li>

    </ul>
</nav>
```

### JSON {#json}

```
"languagenavigation":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     "items":[  
                        {  
                           "children":[  
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":true,
                                 "title":"English",
                                 "locale":"en",
                                 "country":"",
                                 "language":"en",
                                 "url":"/content/we-retail/us/en/equipment.html",
                                 "path":"/content/we-retail/us/en/equipment",
                                 "description":null,
                                 "lastModified":1515760174857
                              },
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "title":"Español",
                                 "locale":"es",
                                 "country":"",
                                 "language":"es",
                                 "url":"/content/we-retail/us/es.html",
                                 "path":"/content/we-retail/us/es",
                                 "description":null,
                                 "lastModified":1474673505454
                              }
                           ],
                           "level":0,
                           "active":true,
                           "title":"United States",
                           "locale":"en",
                           "country":"",
                           "language":"en",
                           "url":"/content/we-retail/us/en/equipment.html",
                           "path":"/content/we-retail/us/en/equipment",
                           "description":null,
                           "lastModified":1515760174857
                        },
                        {  
                           "children":[  
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "title":"English",
                                 "locale":"en_CA",
                                 "country":"CA",
                                 "language":"en-CA",
                                 "url":"/content/we-retail/ca/en/equipment.html",
                                 "path":"/content/we-retail/ca/en/equipment",
                                 "description":null,
                                 "lastModified":1477493028617
                              },
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "title":"Français",
                                 "locale":"en_CA",
                                 "country":"CA",
                                 "language":"en-CA",
                                 "url":"/content/we-retail/ca/fr.html",
                                 "path":"/content/we-retail/ca/fr",
                                 "description":null,
                                 "lastModified":1474673388792
                              }
                           ],
                           "level":0,
                           "active":false,
                           "title":"Canada",
                           "locale":"en_CA",
                           "country":"CA",
                           "language":"en-CA",
                           "url":"/content/we-retail/ca/en/equipment.html",
                           "path":"/content/we-retail/ca/en/equipment",
                           "description":null,
                           "lastModified":1477493028617
                        },
                        {  
                           "children":[  
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "title":"Deutsch",
                                 "locale":"de_CH",
                                 "country":"CH",
                                 "language":"de-CH",
                                 "url":"/content/we-retail/ch/de.html",
                                 "path":"/content/we-retail/ch/de",
                                 "description":null,
                                 "lastModified":1474673744891
                              },
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "title":"Français",
                                 "locale":"de_CH",
                                 "country":"CH",
                                 "language":"de-CH",
                                 "url":"/content/we-retail/ch/fr.html",
                                 "path":"/content/we-retail/ch/fr",
                                 "description":null,
                                 "lastModified":1474673356319
                              },
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "title":"Italiano",
                                 "locale":"de_CH",
                                 "country":"CH",
                                 "language":"de-CH",
                                 "url":"/content/we-retail/ch/it.html",
                                 "path":"/content/we-retail/ch/it",
                                 "description":null,
                                 "lastModified":1474673460578
                              }
                           ],
                           "level":0,
                           "active":false,
                           "title":"Switzerland",
                           "locale":"de_CH",
                           "country":"CH",
                           "language":"de-CH",
                           "url":"/content/we-retail/ch.html",
                           "path":"/content/we-retail/ch",
                           "description":null,
                           "lastModified":1474673057327
                        },
                        {  
                           "children":[  
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "title":"Deutsch",
                                 "locale":"de",
                                 "country":"",
                                 "language":"de",
                                 "url":"/content/we-retail/de/de.html",
                                 "path":"/content/we-retail/de/de",
                                 "description":null,
                                 "lastModified":1474673744681
                              }
                           ],
                           "level":0,
                           "active":false,
                           "title":"Germany",
                           "locale":"de",
                           "country":"",
                           "language":"de",
                           "url":"/content/we-retail/de.html",
                           "path":"/content/we-retail/de",
                           "description":null,
                           "lastModified":1474673019700
                        },
                        {  
                           "children":[  
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "title":"Français",
                                 "locale":"fr",
                                 "country":"",
                                 "language":"fr",
                                 "url":"/content/we-retail/fr/fr.html",
                                 "path":"/content/we-retail/fr/fr",
                                 "description":null,
                                 "lastModified":1474673321300
                              }
                           ],
                           "level":0,
                           "active":false,
                           "title":"France",
                           "locale":"fr",
                           "country":"",
                           "language":"fr",
                           "url":"/content/we-retail/fr.html",
                           "path":"/content/we-retail/fr",
                           "description":null,
                           "lastModified":1474672999375
                        },
                        {  
                           "children":[  
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "title":"Español",
                                 "locale":"es",
                                 "country":"",
                                 "language":"es",
                                 "url":"/content/we-retail/es/es.html",
                                 "path":"/content/we-retail/es/es",
                                 "description":null,
                                 "lastModified":1474673542068
                              }
                           ],
                           "level":0,
                           "active":false,
                           "title":"Spain",
                           "locale":"es",
                           "country":"",
                           "language":"es",
                           "url":"/content/we-retail/es.html",
                           "path":"/content/we-retail/es",
                           "description":null,
                           "lastModified":1474673075638
                        },
                        {  
                           "children":[  
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "title":"Italiano",
                                 "locale":"it",
                                 "country":"",
                                 "language":"it",
                                 "url":"/content/we-retail/it/it.html",
                                 "path":"/content/we-retail/it/it",
                                 "description":null,
                                 "lastModified":1474673426215
                              }
                           ],
                           "level":0,
                           "active":false,
                           "title":"Italy",
                           "locale":"it",
                           "country":"",
                           "language":"it",
                           "url":"/content/we-retail/it.html",
                           "path":"/content/we-retail/it",
                           "description":null,
                           "lastModified":1474673037021
                        }
                     ],
                     ":type":"core/wcm/sandbox/components/languagenavigation/v1/languagenavigation"
                  }
```

### Détails techniques {#technical-details}

Vous trouverez la documentation technique la plus récente sur le composant [de navigation dans la langue sur github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/languagenavigation/v1/languagenavigation).

Vous trouverez plus d&#39;informations sur le développement des composants principaux dans la documentation destinée aux développeurs de composants [principaux](developing.md).

## Modifier le dialogue {#edit-dialog}

Le dialogue Modifier permet la définition de la racine de navigation globale ainsi que la profondeur de la structure de navigation.

![](assets/screen_shot_2018-01-12at133353.png)

* **Racine
de navigation** Définit la page racine de la structure de navigation.
   * Utilisez le bouton **Ouvrir la boîte de dialogue** de sélection pour parcourir facilement la structure de contenu et sélectionner la racine.
* **Profondeur de profondeur**
de la structure de langue de la structure de langue globale par rapport à la racine de navigation.

## Créer un dialogue {#design-dialog}

A l&#39;aide de la boîte de dialogue de conception, l&#39;auteur du modèle peut définir les valeurs par défaut des mêmes options disponibles dans la boîte de dialogue Modifier.

### Onglet Propriétés {#properties-tab}

![](assets/screen_shot_2018-01-12at133642.png)

* **Valeur par défaut de**navigation racine
de la racine de navigation lorsqu&#39;un auteur de contenu place le composant Sélecteur de langue sur une page de contenu
* **Valeur**par défaut de la structure
de langue de la profondeur de la structure de langue lorsqu&#39;un auteur de contenu place le composant Sélecteur de langue sur une page de contenu

### Onglet Styles {#styles-tab}

Le composant de navigation de langue prend en charge le système [de style AEM](authoring.md#component-styling).