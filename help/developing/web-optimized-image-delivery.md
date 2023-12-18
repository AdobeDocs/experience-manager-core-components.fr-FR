---
title: Diffusion d’images optimisées pour le web
description: Découvrez comment les composants principaux peuvent exploiter les fonctionnalités de diffusion d’images optimisées pour le web d’AEM as a Cloud Service dans le but de diffuser plus efficacement les images.
role: Architect, Developer, Admin, User
exl-id: 6080ab8b-f53c-4d5e-812e-16889da4d7de
source-git-commit: d8c8f4c3395313b21f56fd7d98175924287c367c
workflow-type: ht
source-wordcount: '1022'
ht-degree: 100%

---

# Diffusion d’images optimisées pour le web {#web-optimized-image-delivery}

Découvrez comment les composants principaux peuvent exploiter les fonctionnalités de diffusion d’images optimisées pour le web d’AEM as a Cloud Service dans le but de diffuser plus efficacement les images.

## Présentation {#overview}

La fonction de diffusion d’images optimisées pour le web d’AEM as a Cloud Service offre des ressources d’image à partir de la gestion des ressources numériques au format [WebP.](https://developers.google.com/speed/webp) WebP peut réduire la taille de téléchargement d’une image d’environ 25 % en moyenne, ce qui accélère le chargement des pages.

L’activation de la diffusion d’images optimisées pour le web dans les composants principaux est simple. Parce que tous les navigateurs courants prennent en charge WebP, l’expérience est transparente pour l’utilisateur final. La seule différence qu’ils remarqueront sera le chargement plus rapide du contenu.

## Activer la diffusion d’images optimisées pour le web pour les composants principaux {#activating}

Pour activer la diffusion d’images optimisées pour le web, modifiez un modèle de page et activez simplement l’option **Activer les images optimisées pour le web** dans la boîte de dialogue de conception du [composant Image.](/help/components/image.md#design-dialog) Cette option est disponible dans les versions 1, 2 et 3 du composant Image.

Si vous ne connaissez pas bien les boîtes de dialogue de conception et les modèles de page d’AEM, [veuillez consulter ce document.](/help/get-started/authoring.md#pre-configuring-core-components)

![Activer la diffusion d’images optimisées pour le web dans la boîte de dialogue de conception](/help/assets/web-optimized-image-delivery.png)

C’est terminé ! Les images sont désormais diffusées par le composant Image au format WebP.

Une fois que vous avez activé la diffusion d’images optimisées pour le web, vous pouvez également vérifier la configuration du Dispatcher pour vous assurer qu’il ne bloque pas la requête au service d’images. Les URL de ce service se présentent comme suit.

```text
/adobe/dynamicmedia/deliver/dm-aid--741ed388-d5f8-4797-8095-10c896dc9f1d/skitouring.jpg?quality=80&preferwebp=true
```

Cette opération peut être généralisée avec cette expression régulière.

```text
\/adobe\/dynamicmedia\/deliver\/([^:[]|*\/])\/([\w-])\.(gif|png|png8|jpg|pjpg|bjpg|webp|webpll|webply)(?[a-z0-9=&]*)?
```

## Vérifier la diffusion WebP {#verifying}

La diffusion d’images optimisées pour le web est transparente pour le consommateur du contenu et n’affecte pas les balises. La seule chose qu’un utilisateur final remarquera sera un temps de chargement plus rapide.

Par conséquent, pour observer le changement de comportement réel, vous devez afficher la source de la page.

1. Dans AEM, modifiez une page basée sur le modèle dans lequel vous [avez activé la diffusion d’images optimisées pour le web](#activating) pour le composant Image.
1. Dans l’éditeur de page, cliquez sur le bouton **Informations sur la page** dans le coin supérieur gauche, puis sur **Afficher comme publié**.
1. À l’aide des outils de développement de vos navigateurs, affichez la source de la page et voyez comment les balises rendues restent identiques, mais aussi comment l’image dans l’attribut `src` pointe vers [l’URL du nouveau service d’image.](#activating)

## Lorsque la diffusion d’images optimisées pour le web n’est pas disponible. {#fallback}

La diffusion d’images optimisées pour le web n’est disponible que dans AEM as a Cloud Service. Dans les cas où elle n’est pas disponible, par exemple lorsqu’elle s’exécute sur la version 6.5 d’AEM on-premise ou sur une instance de développement locale, la diffusion d’images revient à utiliser [le servlet Image adaptative.](/help/developing/adaptive-image-servlet.md)

De même que l’activation de la diffusion d’images optimisées pour le web n’affecte pas les balises, le retour au servlet Image adaptative ne les affecte pas non plus, car seule l’URL de l’attribut `src` de l’élément `img` est modifiée.

## Questions fréquentes {#faq}

### Pourquoi n’existe-t-il pas une option permettant d’activer les images optimisées pour le web dans mon environnement ? {#missing-option}

Cette fonctionnalité n’est disponible que sur AEM as a Cloud Service. Lorsqu’AEM s’exécute localement ou on-premise, le composant Image [retourne](#fallback) à l’utilisation du servlet Image adaptative.

### Pourquoi le service ne fonctionne-t-il pas avec le SDK local ? {#local-sdk}

Lors de l’utilisation du SDK AEM sur `localhost`, le service d’image n’est pas disponible et le rendu d’image [retourne](#fallback) à l’utilisation du servlet Image adaptative.

Pour utiliser le service de diffusion d’images optimisées pour le web, déployez le projet dans un environnement de développement AEMaaCS afin de pouvoir tester précisément le comportement du service d’images.

### Pourquoi le service ne fonctionne-t-il pas pour certaines images de ma page ? {#some-images}

Le service d’image fonctionne uniquement pour les ressources situées sous `/content/dam` et ne fonctionne pas pour les images téléchargées directement sur la page et stockées sous un objet `cq:Page`. Ces ressources seront toujours diffusées avec le servlet Image adaptative comme [solution de remplacement.](#fallback)

### Pourquoi le service affiche-t-il une image de mauvaise qualité ou limite-t-il la taille des images ? {#quality}

Le service d’image optimisées pour le web prend en compte tous les rendus d’image de 2 048 pixels et plus petits, et en désigne les plus grands comme base sur laquelle il appliquera les paramètres demandés (largeur, recadrage, format, qualité, etc.).

Le service d’image n’améliore jamais la qualité des images. Par conséquent, ces rendus définissent la meilleure taille et la meilleure qualité que le service d’image sera en mesure de fournir. Par conséquent, assurez-vous que vos ressources disposent toutes d’un rendu de zoom 2 048 pixels et, dans le cas contraire, traitez-les à nouveau.

### L’URL de mes images se termine toujours par .JPG ou .PNG, et non par .WEBP, et il n’existe pas d’attribut SRCSET ni d’élément PICTURE. Utilise-t-on vraiment les formats web optimisés ? {#content-negotiation}

Pour diffuser des formats WebP, le service de diffusion d’images optimisées pour le web utilise une technique appelée « négociation de contenu ». Celle-ci consiste à renvoyer un format de fichier WebP, même lorsque vous demandez une extension de fichier JPG ou PNG, mais uniquement lorsque le navigateur qui a émis la requête a fourni un en-tête HTTP Accept `image/webp`. Les navigateurs prenant en charge cette technique peuvent ensuite fournir cet en-tête, et les navigateurs plus anciens obtiennent toujours le format de fichier JPG ou PNG.

L’avantage de cette technique est que l’élément `img` et ses attributs peuvent rester identiques, ce qui permettra une compatibilité optimale des sites existants et garantira le chemin d’accès le plus fluide possible vers une diffusion d’images optimisées pour le web.

### Puis-je utiliser la diffusion d’images optimisées pour le web avec mon propre composant ?

Oui, le service de diffusion d’images optimisées pour le web peut être utilisé par des composants personnalisés. Adobe recommande [l’extension du composant Image](/help/developing/customizing.md) dans ce cas.

Vous trouverez ci-dessous une interface de service que vous pouvez utiliser pour générer l’URL de la ressource.

```
com.adobe.cq.wcm.spi.AssetDelivery.getDeliveryURL(Resource resource, Map<String, Object> parameterMap)
```

**Notez que les incorporations d’URL directe dans une expérience qui n’est pas créée par le biais des composants principaux s’exécutant sur AEM Sites CS sont contraires aux conditions de licence de Media Library.**

### Quelle est l’URL d’une image fournie par le nouveau service d’images ? {#url}

Reportez-vous à la section précédente [Activer la diffusion d’images optimisées pour le web pour les composants principaux](#activating) pour un exemple d’URL et d’expression régulière.

### Les images peuvent-elles ne pas s’afficher lorsque vous avez activé les images optimisées pour le web ?

Non, cela ne devrait jamais arriver.

* Dans le HTML, le balisage ne change pas lors de l’activation des images optimisées pour le web. Seule la valeur de l’attribut SRC sur l’élément image change.
* Lorsque le nouveau service d’image n’est pas disponible ou ne peut pas traiter l’image souhaitée, l’URL générée [basculera vers le servlet Image adaptative.](#fallback)
* Les règles de Dispatcher peuvent bloquer le service d’images optimisées pour le web et [doivent être cochées lors de l’activation de la fonctionnalité.](#activating)
