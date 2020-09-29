---
title: Utilisation de la couche de données client Adobe avec les composants principaux
description: Utilisation de la couche de données client Adobe avec les composants principaux
translation-type: ht
source-git-commit: 4a44a5f584efa736320556f6b4e2f4126d058a48
workflow-type: ht
source-wordcount: '575'
ht-degree: 100%

---


# Utilisation de la couche de données client Adobe avec les composants principaux {#data-layer-core-components}

L’objectif de la couche de données client Adobe est de réduire les efforts d’instrumentalisation des sites web en fournissant une méthode normalisée afin d’exposer et d’accéder à tout type de données pour tout script.

La couche de données client Adobe est indépendante de la plate-forme, mais elle est entièrement intégrée aux composants principaux pour l’utilisation avec AEM.

Tout comme les composants principaux, le code de la couche de données client Adobe est disponible sur GitHub avec sa documentation destinée aux développeurs. Ce document donne un aperçu de la façon dont les composants principaux interagissent avec la couche de données ; les détails techniques complets sont disponibles dans la documentation GitHub.

>[!TIP]
>
>Pour plus d’informations sur la couche de données client Adobe, [reportez-vous aux ressources de son référentiel GitHub.](https://github.com/adobe/adobe-client-data-layer)
>
>Pour obtenir des détails techniques sur l’intégration de la couche de données client Adobe avec les composants principaux, voir le fichier [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) dans le référentiel des composants principaux.

## Installation et activation {#installation-activation}

Depuis la version 2.9.0 des composants principaux, la couche de données est distribuée avec ceux-ci en tant que bibliothèque cliente. Aucune installation n’est nécessaire.

Cependant, la couche de données n’est pas activée par défaut. Pour activer la couche de données   vous devez créer une [configuration basée sur le contexte](/help/developing/context-aware-configs.md) :

1. Créez la structure suivante sous le nœud `/conf` :
   * `/conf/<mySite>/sling:configs/com.adobe.cq.wcm.core.components.internal.DataLayerConfig`
   * Type de nœud : `nt:unstructured`
1. Ajoutez une propriété booléenne appelée `enabled` et définissez-la sur `true`.
1. Ajoutez une propriété `sling:configRef` sur le nœud `jcr:content` de votre site ci-dessous `/content` (par exemple, `/content/<mySite>/jcr:content`) et définissez-la sur `/conf/<mySite>`.

Une fois activée, vous pouvez vérifier l’activation en chargeant une page du site en dehors de l’éditeur. Lorsque vous examinez la page, vous constatez que la couche de données client Adobe est chargée.

## Schémas de données des composants principaux {#data-schemas}

Voici une liste de schémas que les composants principaux utilisent avec la couche de données.

### Schéma d’élément de composant/conteneur {#item}

Le schéma d’élément de composant/conteneur est utilisé dans les composants suivants :

* [Chemin de navigation](/help/components/breadcrumb.md)
* [Bouton](/help/components/button.md)
* [Navigation par langue](/help/components/language-navigation.md)
* [Liste](/help/components/list.md)
* [Navigation](/help/components/navigation.md)
* [Teaser](/help/components/teaser.md)
* [Texte](/help/components/text.md)
* [Titre](/help/components/title.md)

Le schéma d’élément de composant/conteneur est défini comme suit.

```javascript
id: {                   // component ID
    @type               // resource type
    repo:modifyDate     // last modified date
    dc:title            // title
    dc:description      // description
    xdm:text            // text
    xdm:linkURL         // link URL
    parentId            // parent component ID
}
```

L’[événement](#events) suivant correspond au schéma d’élément de composant/conteneur :

* `cmp:click`

### Schéma de page {#page}

Le schéma de page est utilisé par le composant suivant :

* [Page](/help/components/page.md)

Le schéma de page est défini comme suit.

```javascript
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    xdm:tags            // page tags
    repo:path           // page path
    xdm:template        // page template
    xdm:language        // page language
}
```

### Schéma de conteneur {#container}

Le schéma de conteneur est utilisé par les composants suivants :

* [Accordéon](/help/components/accordion.md)
* [Onglets](/help/components/tabs.md)
* [Carrousel](/help/components/carousel.md)

Le schéma de conteneur est défini comme suit.

```javascript
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    shownItems          // array of the displayed item IDs
}
```

Les [événements](#events) suivants correspondent au schéma de conteneur :

* `cmp:click`
* `cmp:show`
* `cmp:hide`

### Schéma d’image {#image}

Le schéma d’image est utilisé par le composant suivant :

* [Image](/help/components/image.md)

Le schéma d’image est défini comme suit.

```javascript
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    image               // asset detail (see below section)
}
```

L’[événement](#events) suivant correspond au schéma d’image :

* `cmp:click`

### Schéma de ressource {#asset}

Le schéma de ressource est utilisé dans le [composant Image.](/help/components/image.md)

Le schéma de ressource est défini comme suit.

```javascript
id: {
    repo:id             // asset UUID
    repo:path           // asset path
    @type               // asset resource type
    xdm:tags            // asset tags
    repo:modifyDate
}
```

L’[événement](#events) suivant correspond au schéma de ressource :

* `cmp:click`

## Événements {#events}

La couche de données déclenche plusieurs événements.

* **`cmp:click`** - Lorsque vous cliquez sur un élément cliquable (élément doté d’un attribut `data-cmp-clickable`), la couche de données déclenche un événement `cmp:click`.
* **`cmp:show`** et **`cmp:hide`** - Manipuler l&#39;accordéon (développer/réduire), le carrousel (boutons Suivant/Précédent) et les composants des onglets (sélection par onglets) provoque le déclenchement des événements `cmp:show` et `cmp:hide`, respectivement, par la couche de données.
* **`cmp:loaded`** - Dès que la couche de données est remplie avec les composants de base sur la page, elle déclenche un événement `cmp:loaded`.

### Événements déclenchés par le composant {#events-components}

Les tableaux suivants répertorient les composants principaux standard qui déclenchent des événements avec ces événements.

| Composant | Événement(s) |
|---|---|
| [Navigation](/help/components/navigation.md) | `cmp:click` |
| [Navigation par langue](/help/components/language-navigation.md) | `cmp:click` |
| [Chemin de navigation](/help/components/breadcrumb.md) | `cmp:click` |
| [Bouton](/help/components/button.md) | `cmp:click` |
| [Carrousel](/help/components/carousel.md) | `cmp:show` et `cmp:hide` |
| [Onglets](/help/components/tabs.md) | `cmp:show` et `cmp:hide` |
| [Accordéon](/help/components/accordion.md) | `cmp:show` et `cmp:hide` |
