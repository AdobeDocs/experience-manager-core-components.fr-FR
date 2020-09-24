---
title: Inclusion de bibliothèques client
description: Il existe plusieurs façons d’inclure des bibliothèques clientes en fonction de votre cas d’utilisation.
translation-type: tm+mt
source-git-commit: 24f718be2ba66113eda970c213c6ce4baec51752
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 3%

---


# Inclusion de bibliothèques client {#including-client-libraries}

Il existe plusieurs façons d’inclure des bibliothèques [](/help/developing/archetype/uifrontend.md#clientlibs) clientes en fonction de votre cas d’utilisation. Ce document fournit des exemples et des exemples de fragments [](https://docs.adobe.com/content/help/fr-FR/experience-manager-htl/using/overview.html) HTML pour chacun d’eux.

## Utilisation recommandée par défaut {#recommended-default-usage}

Si vous n’avez pas le temps d’étudier ce qui est le mieux dans votre situation, incluez vos bibliothèques clientes en plaçant les lignes HTML suivantes à l’intérieur de votre `head` élément de page :

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base', defer=true}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Cela inclura à la fois le fichier CSS et le fichier JS dans votre page `head`, mais l’ajout de l’ `defer` attribut à vos fichiers JS `script` inclut, de sorte que les navigateurs attendent que le modèle DOM soit prêt avant d’exécuter vos scripts et, par conséquent, optimise la vitesse de chargement des pages.

## Utilisation de base {#basic-usage}

La syntaxe de base permettant d’inclure à la fois les fichiers JS et CSS d’une catégorie de bibliothèque cliente, qui générera tous les éléments CSS `link` et/ou `script` éléments JS correspondants, est la suivante :

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Pour faire de même pour plusieurs catégories de bibliothèque clientes à la fois, un tableau de chaînes peut être transmis au `categories` paramètre :

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories=['wknd.base', 'cq.foundation']}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

## CSS ou JS uniquement {#css-js-only}

Il est fréquent que l’on souhaite placer les CSS inclus dans l’élément HTML `head` et les JS inclus juste avant la fermeture de l’ `body` élément.
&#x200B;
Dans `head`, pour inclure uniquement le CSS, et non le JS, utilisez `cssIncludes`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssIncludes @ context="unsafe"}
</sly>
```

Avant la `body` fermeture, pour inclure uniquement les fichiers JS et non les fichiers CSS, utilisez `jsIncludes`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsIncludes @ context="unsafe"}
</sly>
```

## Attributs {#attributes}

Pour appliquer des attributs aux éléments CSS `link` et/ou `script` aux éléments JS générés, plusieurs paramètres sont possibles :

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

Attributs CSS `link` qui peuvent être transmis à `jsAndCssIncludes` et `cssIncludes`:

* `media`: chaîne &#x200B; attributs JS `script` qui peuvent être transmis à `jsAndCssIncludes` et `jsIncludes`:

* `async`: booléen
* `defer`: booléen
* `onload`: string
* `crossorigin`: string

## Inline {#inlining}

Dans certains cas, que ce soit pour l&#39;optimisation ou pour le courrier électronique ou l&#39; [AMP,](amp.md) il peut être nécessaire d&#39;insérer le CSS ou JS dans la sortie du code HTML. &#x200B;
Pour insérer la page CSS, `cssInline` vous pouvez l’utiliser, auquel cas vous devez écrire l’ `style` élément environnant :

```html
<style type="text/css"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssInline @ context="unsafe"}
</style>
```

De même, pour insérer la JS, `jsInline` vous pouvez utiliser, auquel cas vous devez écrire l’élément `script` qui l’entoure :

```html
<script type="text/javascript"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsInline @ context="unsafe"}
</script>
```
