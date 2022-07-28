---
title: Diffusion d’images optimisée pour le web
description: Découvrez comment les composants principaux peuvent tirer parti des fonctionnalités de diffusion d’images optimisées pour le web d’AEM pour diffuser plus efficacement les images.
role: Architect, Developer, Admin, User
exl-id: 6080ab8b-f53c-4d5e-812e-16889da4d7de
source-git-commit: a134c2593593efef4df7b01e3a870e03e9860640
workflow-type: tm+mt
source-wordcount: '1169'
ht-degree: 0%

---

# Diffusion d’images optimisée pour le web {#web-optimized-image-delivery}

Découvrez comment les composants principaux peuvent tirer parti des fonctionnalités de diffusion d’images optimisées pour le web d’AEM pour diffuser plus efficacement les images.

>[!NOTE]
>
>Le service de diffusion d’images optimisé pour le web est une version préliminaire de la version de juin 2022 d’AEM as a Cloud Service avec disponibilité générale prévue pour juillet.
>
>Pour plus d’informations sur les fonctionnalités de version préliminaire d’AEMaaCS, consultez le document . [Canal de version préliminaire Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=fr)

## Présentation {#overview}

La fonction de diffusion d’images optimisée pour le web d’AEM as a Cloud Service fournit des ressources d’image à partir de la gestion des actifs numériques dans [Format WebP.](https://developers.google.com/speed/webp) WebP peut réduire la taille de téléchargement d’une image d’environ 25 % en moyenne, ce qui se traduit par un chargement de page plus rapide.

L’activation de la diffusion d’images optimisée pour le web dans les composants principaux est simple. Comme tous les navigateurs courants prennent en charge WebP, l’expérience est transparente pour l’utilisateur final. La seule différence qu’ils remarqueront est que le contenu se charge plus rapidement.

## Activation de la diffusion d’images optimisée pour le web pour les composants principaux {#activating}

Pour activer la diffusion d’images optimisée pour le web, éditez un modèle de page et activez simplement l’option . **Activer les images optimisées pour le web** dans la boîte de dialogue de conception de [Composant d’image.](/help/components/image.md#design-dialog) Cette option est disponible pour les versions 1, 2 et 3 du composant Image.

Si vous ne connaissez pas les boîtes de dialogue de conception et les modèles de page d’AEM, [veuillez consulter ce document.](/help/get-started/authoring.md#pre-configuring-core-components)

![Activation de la diffusion d’images optimisée pour le web dans la boîte de dialogue de conception](/help/assets/web-optimized-image-delivery.png)

C’est terminé ! Les images sont désormais diffusées par le composant Image au format WebP.

Une fois que vous avez activé la diffusion avec image optimisée pour le web, vous pouvez également vérifier la configuration de Dispatcher pour vérifier qu’elle ne bloque pas la demande au service d’images. Les URL de ce service se présentent comme suit.

```text
/adobe/dynamicmedia/deliver/dm-aid--741ed388-d5f8-4797-8095-10c896dc9f1d/skitouring.jpg?quality=80&preferwebp=true
```

Cela peut être généralisé avec cette expression régulière.

```text
\/adobe\/dynamicmedia\/deliver\/([^:[]|*\/])\/([\w-])\.(gif|png|png8|jpg|pjpg|bjpg|webp|webpll|webply)(?[a-z0-9=&]*)?
```

## Vérification de la diffusion WebP {#verifying}

La diffusion d’images optimisées pour le web est transparente pour le consommateur du contenu et n’affecte pas les balises. La seule chose qu’un utilisateur final remarquera est un temps de chargement plus rapide.

Par conséquent, pour observer le changement de comportement réel, vous devez afficher la source de la page.

1. Dans AEM, modifiez une page basée sur le modèle dans lequel vous [diffusion d’images optimisée pour le web activée](#activating) pour le composant d’image.
1. Dans l’éditeur de page, sélectionnez la variable **Informations sur la page** en haut à gauche, puis **Afficher comme publié(e)**.
1. À l’aide des outils de développement de vos navigateurs, affichez la source de la page et voyez comment les balises rendues restent identiques, mais que l’image dans la variable `src` pointe vers [URL du nouveau service d’image.](#activating)

## Lorsque la diffusion d’images optimisée pour le web n’est pas disponible {#fallback}

La diffusion d&#39;images optimisées pour le web n&#39;est disponible que dans AEM as a Cloud Service. Dans les cas où il n’est pas disponible, par exemple lorsqu’il exécute AEM 6.5 sur site ou sur une instance de développement locale, la diffusion d’image revient à utiliser [la servlet d’image adaptative.](/help/developing/adaptive-image-servlet.md)

De même que l’activation de la diffusion d’images optimisée pour le web n’a aucune incidence sur les balises, la revente à la servlet d’image adaptative n’a aucun effet sur les balises, car seule l’URL dans la variable `src` de l’attribut `img` est modifié.

## Questions fréquentes {#faq}

### Pourquoi n’existe-t-il pas une telle option pour activer les images optimisées pour le web dans mon environnement ? {#missing-option}

Cette fonctionnalité n’est disponible que sur AEM as a Cloud Service. Exécution d’AEM localement ou sur site, le composant d’image [retours](#fallback) à l’aide de la servlet d’image adaptative.

### Pourquoi le service ne fonctionne-t-il pas avec le SDK local ? {#local-sdk}

Lors de l’utilisation du SDK AEM sur `localhost`, le service d’image n’est pas disponible et le rendu d’image [retours](#fallback) à l’aide de la servlet d’image adaptative.

Pour utiliser le service de diffusion d’images optimisé pour le web, déployez le projet dans un environnement de développement AEMaaCS afin de pouvoir tester précisément le comportement du service d’images avec le service d’images.

### Pourquoi le service ne fonctionne-t-il pas pour certaines images de ma page ? {#some-images}

Le service d’image fonctionne uniquement pour les ressources situées sous `/content/dam` et ne fonctionne pas pour les images téléchargées directement sur la page et stockées sous un `cq:Page` . Ces ressources seront toujours diffusées avec la servlet d’image adaptative en tant que [de secours.](#fallback)

### Pourquoi le service affiche-t-il une image de mauvaise qualité ou limite-t-il la taille des images ? {#quality}

Le service d’image optimisé pour le web prend en compte tous les rendus d’image de 2 048 pixels et plus petits, et en désigne le plus grand comme base sur laquelle il appliquera les paramètres demandés (largeur, recadrage, format, qualité, etc.).

Le service d’image ne met jamais à niveau les images. Ces rendus définissent donc la meilleure taille et la meilleure qualité que le service d’image sera en mesure de fournir. Par conséquent, assurez-vous que vos ressources disposent toutes du rendu de zoom 2 048 pixels et, dans le cas contraire, retraitez-les.

### L’URL de mes images se termine toujours par .JPG ou .PNG, et non .WEBP, et il n’existe aucun attribut SRCSET ni élément PICTURE. Est-ce vraiment en utilisant des formats web optimisés ? {#content-negotiation}

Pour diffuser des formats WebP, le service de diffusion d’images optimisé pour le web utilise une technique appelée &quot;négociation de contenu&quot;. Cela consiste à renvoyer un format de fichier WebP, même lorsque vous demandez une extension de fichier JPG ou PNG, mais uniquement lorsque le navigateur qui a émis la requête a fourni une `image/webp` En-tête HTTP accept . Les navigateurs prenant en charge cette technique peuvent ensuite fournir cet en-tête, et les navigateurs plus anciens obtiennent toujours le format de fichier JPG ou PNG.

L’avantage de cette technique est que la variable `img` et ses attributs peuvent rester identiques, ce qui permettra une compatibilité optimale pour les sites existants et garantira le chemin le plus fluide possible vers une diffusion d’images optimisée pour le web.

### Puis-je utiliser la diffusion d’images optimisée pour le web avec mon propre composant ?

Oui, le service de diffusion d’images optimisé pour le web peut être utilisé par des composants personnalisés. Adobe recommande [extension du composant d’image](/help/developing/customizing.md) dans ce cas.

Vous trouverez ci-dessous une interface de service qui peut être utilisée pour générer l’URL de la ressource.

```
com.adobe.cq.wcm.spi.AssetDelivery.getDeliveryURL(Resource resource, Map<String, Object> parameterMap)
```

Ce service prend une ressource de ressource comme premier paramètre obligatoire et peut prendre une carte facultative des transformations d’image souhaitées à appliquer, qui peut contenir les paramètres suivants.

* `path` - ID de ressource à diffuser, doit être du modèle `([^:\[\]\|\*\/]+)` (par exemple : `unicorn–1234`)
* `seoname` : nom défini par l’utilisateur et centré sur l’optimisation pour les moteurs de recherche à ajouter à l’URL de l’image ; il peut contenir des tirets ; il doit s’agir d’un motif. `([\w-]+)` (par exemple : `my-friend-the-unicorn`)
* `format` - Le format d’image souhaité peut être `gif`, `png`, `png8`, `jpg`, `pjpg`, `bjpg`, `webp`, `webpll`, `webply` (par exemple : `webp`)
* `preferwebp` - Si possible, diffusez la sortie WebP, en ignorant la variable `format` paramètre ([voir FAQ sur la négociation de contenu](#content-negotiation)), booléen (par exemple : `true`)
* `width` - La résolution d’image souhaitée en pixels doit être supérieure à 1 (par exemple : `400`)
* `quality` - la compression souhaitée, entre `1` et `100` (par exemple : `75`)
* `c` - Coordonnées de recadrage d’image de votre choix, valeurs de pixels séparées par des virgules (par exemple : `100,100,400,200`)
* `r` - La rotation de l’image souhaitée peut être `90`, `180`, `270` (par exemple : `90`)
* `flip` - Le changement d’image souhaité peut être `h`, `v`, `hv` (par exemple : `h`)

### Quelle est l’URL d’une image fournie par le nouveau service d’images ? {#url}

Voir la section précédente [Activation de la diffusion d’images optimisée pour le web pour les composants principaux](#activating) pour un exemple d’URL et d’expression régulière.

### Les images peuvent-elles ne pas s’afficher après avoir activé les images optimisées pour le web ?

Non, ça ne devrait jamais arriver.

* Dans le HTML, le balisage ne change pas lors de l’activation des images optimisées pour le web. Seula la valeur de l’attribut SRC sur l’élément image change.
* Lorsque le nouveau service d’image n’est pas disponible ou ne peut pas traiter l’image souhaitée, l’URL générée [Basculement vers la servlet d’image adaptative.](#fallback)
* Les règles de Dispatcher peuvent bloquer le service d’images optimisé pour le web et [doit être cochée lors de l’activation de la fonctionnalité.](#activating)
