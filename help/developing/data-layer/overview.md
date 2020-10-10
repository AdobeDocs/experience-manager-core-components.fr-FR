---
title: Utilisation de la couche de données client Adobe avec les composants principaux
description: Utilisation de la couche de données client Adobe avec les composants principaux
translation-type: ht
source-git-commit: 79a063951a790261e2f00c33d8a76f31f781da0c
workflow-type: ht
source-wordcount: '868'
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

Depuis la version 2.9.0 des composants principaux, la couche de données est distribuée avec les composants principaux sous la forme d’une bibliothèque cliente AEM et aucune installation n’est nécessaire. Tous les projets générés par l’[archétype de projets AEM v. 24+](/help/developing/archetype/overview.md) incluent par défaut une couche de données activée.

Pour activer manuellement la couche de données, vous devez créer une [configuration contextuelle](/help/developing/context-aware-configs.md) :

1. Créez la structure suivante dans le dossier `/conf/<mySite>`, où `<mySite>` est le nom du projet de votre site :
   * `/conf/<mySite>/sling:configs/com.adobe.cq.wcm.core.components.internal.DataLayerConfig`
   * Où chaque nœud a une valeur `jcr:primaryType` définie sur `nt:unstructured`.
1. Ajoutez une propriété booléenne appelée `enabled` et définissez-la sur `true`.

   ![Emplacement de DataLayerConfig dans le site de référence WKND](/help/assets/datalayer-contextaware-sling-config.png)

   *Emplacement de DataLayerConfig dans le site de référence WKND*

1. Ajoutez une propriété `sling:configRef` sur le nœud `jcr:content` de votre site ci-dessous `/content` (par exemple, `/content/<mySite>/jcr:content`) et définissez-la sur `/conf/<mySite>` par rapport à l’étape précédente.

1. Une fois activée, vous pouvez vérifier l’activation en chargeant une page du site en dehors de l’éditeur. Inspectez la source de la page. La balise `<body>` doit contenir un attribut `data-cmp-data-layer-enabled`.

   ```html
   <body class="page basicpage" id="page-id" data-cmp-data-layer-enabled>
       <script>
         window.adobeDataLayer = window.adobeDataLayer || [];
         adobeDataLayer.push({
             page: JSON.parse("{\x22page\u002D6c5d4b9fdd\x22:{\x22xdm:language\x22:\x22en\x22,\x22repo:path\x22:\x22\/content\/wknd\/language\u002Dmasters\/en.html\x22,\x22xdm:tags\x22:[],\x22xdm:template\x22:\x22\/conf\/wknd\/settings\/wcm\/templates\/landing\u002Dpage\u002Dtemplate\x22,\x22@type\x22:\x22wknd\/components\/page\x22,\x22dc:description\x22:\x22WKND is a collective of outdoors, music, crafts, adventure sports, and travel enthusiasts that want to share our experiences, connections, and expertise with the world.\x22,\x22dc:title\x22:\x22WKND Adventures and Travel\x22,\x22repo:modifyDate\x22:\x222020\u002D09\u002D29T07:50:13Z\x22}}"),
             event:'cmp:show',
             eventInfo: {
                 path: 'page.page\u002D6c5d4b9fdd'
             }
         });
       </script>
   ```

1. Vous pouvez également ouvrir les outils de développement de votre navigateur. Dans la console, l’objet JavaScript `adobeDataLayer` doit être disponible. Saisissez la commande suivante pour obtenir l’état de la couche de données de votre page actuelle :

   ```javascript
   window.adobeDataLayer.getState();
   ```

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

Un événement `cmp:show` est déclenché au chargement de la page. Cet événement est distribué à partir du code JavaScript intégré immédiatement au-dessous de la balise d’ouverture `<body>`, ce qui en fait le premier événement de la file d’attente des événements de la couche de données. 

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

## Événements des composants principaux {#events}

Un certain nombre d’événements sont déclenchés par les composants principaux au moyen de la couche de données. La bonne pratique pour interagir avec la couche de données consiste à [enregistrer un listener d’événement](https://github.com/adobe/adobe-client-data-layer/wiki#addeventlistener), *puis* à effectuer une action en fonction du type d’événement et/ou du composant qui a déclenché l’événement. Il est ainsi possible d’éviter les conditions de concurrence potentielle avec des scripts asynchrones.

Vous trouverez ci-dessous les événements prêts à l’emploi fournis par les composants principaux d’AEM :

* **`cmp:click`** - Lorsque vous cliquez sur un élément cliquable (élément doté d’un attribut `data-cmp-clickable`), la couche de données déclenche un événement `cmp:click`.
* **`cmp:show`** et **`cmp:hide`** - Manipuler l&#39;accordéon (développer/réduire), le carrousel (boutons Suivant/Précédent) et les composants des onglets (sélection par onglets) provoque le déclenchement des événements `cmp:show` et `cmp:hide`, respectivement, par la couche de données. Un événement `cmp:show` est également distribué au chargement de la page et devrait être le premier.
* **`cmp:loaded`** - Dès que la couche de données est remplie avec les composants principaux sur la page, elle déclenche un événement `cmp:loaded`.

### Événements déclenchés par le composant {#events-components}

Les tableaux suivants répertorient les composants principaux standard qui déclenchent des événements avec ces événements.

| Composant | Événement(s) |
|---|---|
| [Accordéon](/help/components/accordion.md) | `cmp:show` et `cmp:hide` |
| [Bouton](/help/components/button.md) | `cmp:click` |
| [Chemin de navigation](/help/components/breadcrumb.md) | `cmp:click` |
| [Carrousel](/help/components/carousel.md) | `cmp:show` et `cmp:hide` |
| [Navigation par langue](/help/components/language-navigation.md) | `cmp:click` |
| [Navigation](/help/components/navigation.md) | `cmp:click` |
| [Page](/help/components/page.md) | `cmp:show` |
| [Onglets](/help/components/tabs.md) | `cmp:show` et `cmp:hide` |
| [Teaser](/help/components/teaser.md) | `cmp:click` |

### Infos sur le chemin de l’événement {#event-path-info}

Chaque événement de la couche de données déclenché par un composant principal d’AEM inclura une charge utile associée à l’objet JSON suivant :

```json
eventInfo: {
    path: '<component-path>'
}
```

Où `<component-path>` est le chemin JSON vers le composant de la couche de données qui a déclenché l’événement. La valeur, disponible dans `event.eventInfo.path`, est importante, car il est possible de l’utiliser comme paramètre pour `adobeDataLayer.getState(<component-path>)`. Elle sert à récupérer l’état actuel du composant qui a déclenché l’événement, ce qui permet au code personnalisé d’accéder à des données supplémentaires et de les ajouter à la couche de données.

Par exemple :

```javascript
function logEventObject(event) {
    if(event.hasOwnProperty("eventInfo") && event.eventInfo.hasOwnProperty("path")) {
        var dataObject = window.adobeDataLayer.getState(event.eventInfo.path);
        console.debug("The component that triggered this event: ");
        console.log(dataObject);
    }
}

window.adobeDataLayer = window.adobeDataLayer || [];
window.adobeDataLayer.push(function (dl) {
     dl.addEventListener("cmp:show", logEventObject);
});
```

## Tutoriel

Souhaitez-vous explorer plus en détail la couche de données et les composants principaux ? [Consultez ce tutoriel pratique](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/integrations/adobe-client-data-layer/data-layer-overview.html).
