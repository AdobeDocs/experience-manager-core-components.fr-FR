---
title: Utilisation de la couche de données client Adobe avec les composants principaux
description: Utilisation de la couche de données client Adobe avec les composants principaux
translation-type: tm+mt
source-git-commit: 539a4250c954ac830731a9ecf010e129b2cf9c3a
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 3%

---


# Utilisation de la couche de données client Adobe avec les composants principaux {#data-layer-core-components}

L&#39;objectif de la couche de données client Adobe est de réduire les efforts d&#39;instrumentalisation des sites Web en fournissant une méthode normalisée pour exposer et accéder à tout type de données pour tout script.

La couche de données du client Adobe est indépendante de la plate-forme, mais est entièrement intégrée dans les composants principaux pour une utilisation avec AEM.

Tout comme les composants principaux, le code de la couche de données du client Adobe est disponible sur GitHub avec sa documentation destinée aux développeurs. Ce document donne un aperçu de la façon dont les composants principaux interagissent avec la couche de données, mais des détails techniques complets sont renvoyés à la documentation GitHub.

>[!TIP]
>
>Pour plus d’informations sur la couche de données du client Adobe, [reportez-vous aux ressources de son référentiel GitHub.](https://github.com/adobe/adobe-client-data-layer)
>
>Pour plus d’informations techniques sur l’intégration de la couche de données client Adobe avec les composants principaux, voir le [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) fichier dans le référentiel des composants principaux.


## Installation et Activation {#installation-activation}

Depuis la version 2.9.0 des composants principaux, la couche de données est distribuée avec les composants principaux en tant que bibliothèque cliente. Aucune installation n’est nécessaire.

Cependant, la couche de données n&#39;est pas activée par défaut. Pour activer la couche de données

1. Créez la structure suivante sous le `/conf` noeud :
   * `/conf/<mySite>/sling:configs/com.adobe.cq.wcm.core.components.internal.DataLayerConfig`
1. Ajoutez une propriété booléenne appelée `enabled` et définissez-la sur `true`.
1. Ajoutez une `sling:configRef` propriété sur le `jcr:content` noeud de votre site ci-dessous `/content` (ex. `/content/<mySite>/jcr:content`) et définissez-la sur `/conf/<mySite>`.

Une fois activée, vous pouvez vérifier l’activation en chargeant une page du site en dehors de l’éditeur. Lorsque vous examinez la page, vous constatez que la couche de données du client Adobe est chargée.

## Schémas de données des composants principaux {#data-schemas}

Voici une liste de schémas que les composants principaux utilisent avec la couche de données.

### Schéma d&#39;élément composant/Conteneur {#item}

Le schéma Composant/Article Conteneur est utilisé dans les composants suivants :

* [Chemin de navigation](/help/components/breadcrumb.md)
* [Bouton](/help/components/button.md)
* [Navigation par langue](/help/components/language-navigation.md)
* [Liste](/help/components/list.md)
* [Navigation](/help/components/navigation.md)
* [Teaser](/help/components/teaser.md)
* [Texte](/help/components/text.md)
* [Titre](/help/components/title.md)

Le schéma Composant/Article Conteneur est défini comme suit.

```
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


### Schéma de page {#page}

Le schéma de page est utilisé par le composant suivant :

* [Page](/help/components/page.md)

Le schéma de page est défini comme suit.

```
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

### Schéma Conteneur {#container}

Le schéma de Conteneur est utilisé par les composants suivants :

* [Accordéon](/help/components/accordion.md)
* [Onglets](/help/components/tabs.md)
* [Carrousel](/help/components/carousel.md)

Le schéma de Conteneur est défini comme suit.

```
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

### Schéma d’image {#image}

Le schéma Image est utilisé par le composant suivant :

* [Image](/help/components/image.md)

Le schéma d’image est défini comme suit.

```
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

### Schéma de ressources {#asset}

Le schéma de ressources est utilisé dans le composant [Image.](/help/components/image.md)

Le schéma de ressources est défini comme suit.

```
id: {
    repo:id             // asset UUID
    repo:path           // asset path
    @type               // asset resource type
    xdm:tags            // asset tags
    repo:modifyDate
}
```

