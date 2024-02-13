---
title: Bibliothèques clientes et composants principaux
description: Les composants principaux sont fournis avec un certain nombre de bibliothèques clientes et offrent la possibilité d’inclure les vôtres.
role: Architect, Developer, Admin
exl-id: 84e7c178-247b-42a2-99bf-6d1699ecee14
source-git-commit: d39fe0084522f67664203a026340b23d325c1883
workflow-type: ht
source-wordcount: '518'
ht-degree: 100%

---


# Bibliothèques clientes et composants principaux {#client-libraries}

Les composants principaux sont fournis avec un certain nombre de bibliothèques clientes et offrent la possibilité d’inclure les vôtres.

## Bibliothèques clientes fournies {#provided}

Les composants principaux fournissent les bibliothèques clientes suivantes prêtes à l’emploi.

* Les bibliothèques clientes **site** fournissent le comportement fonctionnel minimaliste des composants à appliquer au site.
   * Elles servent de point de départ à l’accélération des projets, avec des mises en œuvre encouragées à les étendre et à les [personnaliser](/help/developing/customizing.md) pour obtenir l’apparence et la fonctionnalité souhaitées.
* Les bibliothèques clientes **editor** sont appliquées à la boîte de dialogue de création pour garantir les fonctionnalités et l’aspect attendus.
* Les bibliothèques clientes **editorhook** sont appliquées au site lorsqu’elles sont chargées en mode d’édition.
   * Elles contiennent du code JavaScript exécuté sur des événements déclenchés lors de l’édition, ce qui facilite l’initialisation des fonctionnalités dynamiques.
* Certains composants peuvent avoir des bibliothèques clientes supplémentaires spécifiques, conçues pour être utilisées dans des situations particulières, par exemple avec [Dynamic Media](/help/components/image.md#dynamic-media).

## Inclusion de bibliothèques clientes {#including}

Il existe plusieurs façons d’inclure des [bibliothèques clientes](/help/developing/archetype/front-end.md#clientlibs) en fonction de votre cas d’utilisation. Voici des exemples de [fragments de code HTL](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html?lang=fr) pour chacun d’eux.

### Utilisation par défaut recommandée {#recommended-default-usage}

Si vous n’avez pas le temps d’étudier ce qui convient le mieux à votre situation, incluez vos bibliothèques clientes en plaçant les lignes HTL suivantes à l’intérieur de votre élément `head` de page :

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base', defer=true}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Cela inclura à la fois les éléments CSS et JS dans votre page `head`, mais en ajoutant l’attribut `defer` à vos inclusions `script` JS, de sorte que les navigateurs attendent que le DOM soit prêt avant d’exécuter vos scripts et, par conséquent, optimise la vitesse de chargement des pages.

### Utilisation de base {#basic-usage}

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

### CSS ou JS uniquement {#css-js-only}

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

### Attributs {#attributes}

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

### Insertion {#inlining}

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

### Chargement d’éléments CSS et JavaScript basés sur le contexte {#context-aware-loading}

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
