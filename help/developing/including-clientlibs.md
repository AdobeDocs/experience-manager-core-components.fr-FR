---
title: Inclusion de bibliothèques clientes
description: Il existe plusieurs façons d’inclure des bibliothèques clientes en fonction de votre cas d’utilisation.
translation-type: tm+mt
source-git-commit: 87e39566617f64b91bd8e98b3779b9b5c426c31c
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 82%

---


# Inclusion de bibliothèques clientes {#including-client-libraries}

Il existe plusieurs façons d’inclure des [bibliothèques clientes](/help/developing/archetype/uifrontend.md#clientlibs) en fonction de votre cas d’utilisation. Ce document fournit des exemples et des [fragments HTL](https://docs.adobe.com/content/help/fr-FR/experience-manager-htl/using/overview.html) pour chacun d’eux.

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

Frequently, one wants to place the CSS includes in the HTML `head` element, and the JS includes just before the closing of the `body` element.

Dans `head`, pour inclure uniquement les éléments CSS, et non les éléments JS, utilisez `cssIncludes` :

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssIncludes @ context="unsafe"}
</sly>
```

Avant de fermer `body`, pour inclure uniquement les·éléments JS, et non les éléments CSS, utilisez `jsIncludes` :

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

* `media` : chaîne

JS `script` attributes that can be passed to `jsAndCssIncludes` and `jsIncludes`:

* `async` : booléen
* `defer` : booléen
* `onload` : chaîne
* `crossorigin` : chaîne

## Insertion {#inlining}

In some cases, either for optimization, or for email or [AMP,](amp.md) it might be required to inline the CSS or JS into the output of the HTML.

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
