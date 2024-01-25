---
title: Inclusion de bibliothèques clientes
description: Il existe plusieurs façons d’inclure des bibliothèques clientes en fonction de votre cas d’utilisation.
role: Architect, Developer, Admin
exl-id: 84e7c178-247b-42a2-99bf-6d1699ecee14
source-git-commit: 39a5dee1666fa2645e0579fdfac0400f7fcbdc27
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 100%

---

# Inclusion de bibliothèques clientes {#including-client-libraries}

Il existe plusieurs façons d’inclure des [bibliothèques clientes](/help/developing/archetype/front-end.md#clientlibs) en fonction de votre cas d’utilisation. Ce document fournit des exemples et des [fragments HTL](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html?lang=fr) pour chacun d’eux.

## Utilisation par défaut recommandée {#recommended-default-usage}

Si vous n’avez pas le temps d’étudier ce qui convient le mieux à votre situation, incluez vos bibliothèques clientes en plaçant les lignes HTL suivantes à l’intérieur de votre élément `head` de page :

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base', defer=true}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Cela inclura à la fois les éléments CSS et JS dans votre page `head`, mais en ajoutant l’attribut `defer` à vos inclusions `script` JS, de sorte que les navigateurs attendent que le DOM soit prêt avant d’exécuter vos scripts et, par conséquent, optimise la vitesse de chargement des pages.

## Utilisation de base {#basic-usage}

La syntaxe de base permettant d’inclure à la fois les éléments JS et CSS d’une catégorie de bibliothèque cliente, qui générera tous les éléments `link` CSS et/ou `script` JS correspondants, est la suivante :

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Pour faire de même pour plusieurs catégories de bibliothèques clientes à la fois, un tableau de chaînes peut être transmis au paramètre `categories` :

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories=['wknd.base', 'cq.foundation']}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

## CSS ou JS uniquement {#css-js-only}

Il est fréquent que l’on souhaite placer les inclusions CSS dans l’élément `head` HTML et les inclusions JS juste avant de fermer l’élément `body`.&#x200B;

Dans `head`, pour inclure uniquement les éléments CSS, et non les éléments JS, utilisez `cssIncludes` :

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssIncludes @ context="unsafe"}
</sly>
```

Avant de fermer `body`, pour inclure uniquement les éléments JS, et non les éléments CSS, utilisez `jsIncludes` :

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsIncludes @ context="unsafe"}
</sly>
```

## Attributs {#attributes}

Pour appliquer des attributs aux éléments `link` CSS et/ou aux éléments `script` JS générés, plusieurs paramètres sont possibles :

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base',
    media='print',
    async=true,
    defer=true,
    onload='console.log(\'loaded: \' + this.src)',
    crossorigin='anonymous'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Attributs `link` CSS qui peuvent être transmis à `jsAndCssIncludes` et `cssIncludes` :

* `media` : attributs de chaîne JS `script` qui peuvent être transmis à `jsAndCssIncludes` et `jsIncludes` :
* `async` : booléen
* `defer` : booléen
* `onload` : chaîne
* `crossorigin` : chaîne

## Insertion {#inlining}

Dans certains cas, que ce soit pour l’optimisation ou pour les emails ou [AMP](amp.md), il peut être nécessaire d’insérer les éléments CSS ou JS dans la sortie du code HTML.

Pour insérer les éléments CSS, vous pouvez utiliser `cssInline`, auquel cas vous devez écrire l’élément `style` environnant :

```html
<style type="text/css"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssInline @ context="unsafe"}
</style>
```

De même, pour insérer les éléments JS, vous pouvez utiliser `jsInline`, auquel cas vous devez écrire l’élément `script` environnant :

```html
<script type="text/javascript"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsInline @ context="unsafe"}
</script>
```

## Chargement d’éléments CSS et JavaScript basés sur le contexte {#context-aware-loading}

Le [composant de page](/help/components/page.md) prend également en charge le chargement de balises CSS, JavaScript ou de métadonnées définies par les développeurs.

Pour ce faire, créez une [ressource contextuelle](context-aware-configs.md) pour `com.adobe.cq.wcm.core.components.config.HtmlPageItemsConfig` en utilisant la structure suivante :

```text
com.adobe.cq.wcm.core.components.config.HtmlPageItemsConfig
    - prefixPath="/some/path"
    + item01
        - element=["link"|"script"|"meta"]
        - location=["header"|"footer"]
        + attributes
            - attributeName01="attributeValue01"
            - attributeName02="attributeValue02"
            ...
    + item02
        ...
    ...
```

[Pour plus d’informations, consultez la documentation technique du composant de page.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page#loading-of-context-aware-cssjs)
