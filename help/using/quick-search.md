---
title: Composant de recherche rapide
seo-title: Composant de recherche rapide
description: 'null'
seo-description: Le composant Recherche rapide fournit des fonctionnalités de recherche à un site Web et présente les résultats de recherche afin que les visiteurs puissent effectuer des recherches sur le site et filtrer les résultats.
uuid: 1 ba 69 be 3-537 e -4 f 20-9 f 17-b 4 b 7174 a 8 e 88
content-type: référence
topic-tags: création
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 906 a 684 d -5663-4497-bef 3-37 f 13 d 5 b 46 c 7
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


# Composant de recherche rapide{#quick-search-component}

Le composant Recherche rapide fournit des fonctionnalités de recherche à un site Web et présente les résultats de recherche afin que les visiteurs puissent facilement trouver le contenu correspondant et afficher les résultats.

## Utilisation {#usage}

Le composant Recherche rapide permet aux visiteurs du site de rechercher du contenu, d&#39;afficher les résultats en place et de naviguer facilement vers les pages correspondantes. De nouveaux résultats sont extraits dynamiquement lorsque l&#39;utilisateur fait défiler les résultats de la recherche.

La boîte de dialogue [Modifier](#edit-dialog) permet à l&#39;auteur de contenu de définir l&#39;emplacement où doit commencer la recherche dans l&#39;arborescence de contenu. A l&#39;aide de [la boîte de dialogue de conception](#design-dialog), l&#39;auteur du modèle peut définir la valeur par défaut pour laquelle la recherche doit commencer dans l&#39;arborescence de contenu, ainsi qu&#39;une taille de jeu de résultats maximale et une durée minimale de recherche.

## Version et compatibilité {#version-and-compatibility}

La version actuelle du composant de recherche rapide est v 1, qui a été introduite avec la version 2.0.0 des composants principaux en janvier 2018 et est décrite dans ce document.

Le tableau suivant détaille toutes les versions prises en charge du composant, les versions AEM avec lesquelles les versions du composant sont compatibles et les liens vers la documentation pour les versions précédentes.

| Version du composant | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Compatible | Compatible | Compatible |

Pour plus d&#39;informations sur les versions et les versions des composants principaux, consultez les versions des composants de Document [principaux](versions.md).

## Exemple de sortie de composant {#sample-component-output}

Voici un exemple tiré de [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Capture d’écran {#screenshot}

![](assets/screen_shot_2018-01-19at094248.png)

### HTML {#html}

```
<section class="cmp-search" role="search" data-cmp-is="search" data-cmp-min-length="3" data-cmp-results-size="10">
    <form class="cmp-search__form" data-cmp-hook-search="form" method="get" action="/content/we-retail/us/en/equipment.searchresults.json/_jcr_content/root/responsivegrid/search" autocomplete="off">
        <div class="cmp-search__field">
            <i class="cmp-search__icon" data-cmp-hook-search="icon"></i>
            <span class="cmp-search__loading-indicator" data-cmp-hook-search="loadingIndicator"></span>
            <input class="cmp-search__input" data-cmp-hook-search="input" type="text" name="fulltext" placeholder="Search" role="combobox" aria-autocomplete="list" aria-haspopup="true" aria-invalid="false">
            <button class="cmp-search__clear" data-cmp-hook-search="clear">
                <i class="cmp-search__clear-icon"></i>
            </button>
        </div>
    </form>
    <div class="cmp-search__results" data-cmp-hook-search="results" role="listbox" aria-multiselectable="false"></div>
    
<script data-cmp-hook-search="itemTemplate" type="x-template">
    <a class="cmp-search__item" data-cmp-hook-search="item">
        <span class="cmp-search__item-title" data-cmp-hook-search="itemTitle"></span>
    </a>
</script>
</section>
```

### JSON {#json}

```
"search":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     "relativePath":"/jcr:content/root/responsivegrid/search",
                     "resultsSize":10,
                     "searchTermMinimumLength":3,
                     ":type":"core/wcm/components/search/v1/search"
                  }
```

### Détails techniques {#technical-details}

>[!NOTE]
>
>La protection du composant de recherche ou de toute application basée sur AEM par rapport aux attaques DOS doit être implémentée à un niveau supérieur, par exemple à l&#39;aide `mod_security` du répartiteur.

Vous trouverez la documentation technique la plus récente sur le composant [de recherche rapide sur github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/search/v1/search).

Vous trouverez plus d&#39;informations sur le développement des composants principaux dans la documentation destinée aux développeurs de composants [principaux](developing.md).

## Modifier le dialogue {#edit-dialog}

La boîte de dialogue Modifier permet à l&#39;auteur de contenu de définir l&#39;emplacement où doit commencer la recherche dans l&#39;arborescence de contenu.

![](assets/screen_shot_2018-04-03at120132.png)

**Racine** de recherche : page racine d&#39;où lancer la recherche. La racine de recherche peut être un gabarit principal, une page principale ou une page normale.

## Créer un dialogue {#design-dialog}

A l&#39;aide de la boîte de dialogue de conception, l&#39;auteur du modèle peut définir la valeur par défaut pour laquelle, dans l&#39;arborescence de contenu, la recherche doit commencer, ainsi qu&#39;une taille de jeu de résultats maximale et la longueur minimale du terme. Le dialogue de conception permet à l&#39;auteur du modèle de définir quelles options de formatage de texte sont disponibles pour les auteurs de contenu.

### Onglet Propriétés {#properties-tab}

![](assets/screen_shot_2018-04-03at120028.png)

* **Racine**
de recherche La valeur par défaut de la racine de recherche lorsqu&#39;un auteur de contenu place le composant Recherche rapide sur une page de contenu
* **Taille**
des résultats Le nombre maximal de résultats extraits par une requête de recherche
* **Longueur minimale du terme de recherche Longueur** minimale du terme de recherche pour lancer la recherche

>[!NOTE]
>
>**La taille des résultats** et la **longueur minimum du terme de recherche** ne peuvent être définies qu&#39;en mode de conception et, par conséquent, au niveau du modèle, ce qui signifie que les auteurs de contenu ne peuvent pas modifier ces valeurs.

>[!CAUTION]
>
>**La taille des résultats** et la **longueur minimale du terme de recherche** peuvent avoir un impact sur les performances si elles sont trop élevées ou trop faibles, respectivement.

### Onglet Styles {#styles-tab}

Le composant de recherche rapide prend en charge le système [de style AEM](authoring.md#component-styling).