---
title: Diffusion d’images optimisées pour le web
description: Découvrez comment les composants principaux peuvent exploiter les fonctionnalités de diffusion d’images optimisées pour le web d’AEM as a Cloud Service dans le but de diffuser plus efficacement les images.
role: Architect, Developer, Admin, User
exl-id: 6080ab8b-f53c-4d5e-812e-16889da4d7de
source-git-commit: eb1822cb41a849695afb5125745ed5f78e3e70a4
workflow-type: tm+mt
source-wordcount: '1061'
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

Une fois que vous avez activé la diffusion d’images optimisées pour le web, vous pouvez vérifier la configuration du Dispatcher pour vous assurer qu’il ne bloque pas la requête au service de diffusion d’images. Pour plus d’informations, consultez [cette entrée de questions fréquentes](#failure-to-deliver).

## Vérifier la diffusion WebP {#verifying}

La diffusion d’images optimisées pour le web est transparente pour le consommateur ou la consommatrice du contenu. La seule chose qu’un utilisateur final ou une utilisatrice finale remarquera est un temps de chargement plus rapide. Par conséquent, pour observer tout changement réel de comportement, vous devez vérifier le type de contenu des images rendues dans le navigateur. Tous les navigateurs modernes prennent en charge WebP. Vous pouvez consulter [ce site](https://caniuse.com/webp) pour plus d’informations sur la prise en charge des navigateurs.

1. Dans AEM, modifiez une page basée sur le modèle dans lequel vous [avez activé la diffusion d’images optimisées pour le web](#activating) pour le composant Image.
1. Dans l’éditeur de page, cliquez sur le bouton **Informations sur la page** dans le coin supérieur gauche, puis sur **Afficher comme publié**.
1. Ouvrez les outils de développement de votre navigateur et sélectionnez l’onglet Réseau.
1. Rechargez la page, recherchez les requêtes HTTP chargeant les images et vérifiez le type de contenu de l’image reçue par le navigateur.

## Lorsque la diffusion d’images optimisées pour le web n’est pas disponible. {#fallback}

La diffusion d’images optimisées pour le web n’est disponible que dans AEM as a Cloud Service. Dans les cas où elle n’est pas disponible, par exemple lorsqu’elle s’exécute sur la version 6.5 d’AEM on-premise ou sur une instance de développement locale, la diffusion d’images revient à utiliser [le servlet Image adaptative.](/help/developing/adaptive-image-servlet.md)

Revenir au servlet d’image adaptatif modifie l’attribut `src` des éléments `img` dans la source de la page.

## Questions fréquentes {#faq}

### Pourquoi n’existe-t-il pas une option permettant d’activer les images optimisées pour le web dans mon environnement ? {#missing-option}

Cette fonctionnalité n’est disponible que sur AEM as a Cloud Service. Lorsqu’AEM s’exécute localement ou on-premise, le composant Image [retourne](#fallback) à l’utilisation du servlet Image adaptative.

### Pourquoi le service ne fonctionne-t-il pas avec le SDK local ? {#local-sdk}

Lors de l’utilisation du SDK AEM sur `localhost`, le service d’image n’est pas disponible et le rendu d’image [retourne](#fallback) à l’utilisation du servlet Image adaptative.

Pour utiliser le service de diffusion d’images optimisées pour le web, déployez le projet dans un environnement de développement AEMaaCS afin de pouvoir tester précisément le comportement du service d’images.

### Pourquoi le service ne fonctionne-t-il pas pour certaines images de ma page ? {#some-images}

Le service d’image fonctionne uniquement pour les ressources situées sous `/content/dam` et ne fonctionne pas pour les images téléchargées directement sur la page et stockées sous un objet `cq:Page`. Ces ressources seront toujours diffusées avec le servlet Image adaptative comme [solution de remplacement.](#fallback)

### Pourquoi le service affiche-t-il une image de mauvaise qualité ou limite-t-il la taille des images ? {#quality}

Lorsque des ressources d’image sous `/content/dam` sont traitées, les environnements AEM as a Cloud Service génèrent des rendus optimisés de différentes dimensions. Le service d’images optimisées pour le web analyse la largeur demandée par le composant principal Image, prend en compte l’image d’origine et tous les rendus de 2 048 pixels ou moins, puis sélectionne le plus grand (dans les limites de taille et de dimension que le service peut gérer, actuellement 50 Mo et `12k`x`12k`) comme base à laquelle il appliquera les paramètres demandés (largeur, recadrage, format, qualité, etc.).

Pour préserver la fidélité de la sortie, le service d’images ne met pas à l’échelle les images. Ces rendus définissent la meilleure taille et la meilleure qualité que le service d’image sera en mesure de fournir. Puisque vous ne pouvez souvent pas influencer la taille et/ou les dimensions de la ressource d’image d’origine, assurez-vous que vos ressources d’image disposent toutes d’un rendu de zoom de 2 048 pixels et, dans le cas contraire, retraitez-les.

### L’URL de mes images se termine toujours par .JPG ou .PNG, et non par .WEBP, et il n’existe pas d’attribut SRCSET ni d’élément PICTURE. Utilise-t-on vraiment les formats web optimisés ? {#content-negotiation}

Pour diffuser des formats WebP, le service de diffusion d’images optimisées pour le web utilise [une négociation de contenu orientée serveur.](https://developer.mozilla.org/fr-FR/docs/Web/HTTP/Content_negotiation#server-driven_content_negotiation) Cela permet de sélectionner le format de sortie optimal de l’image en fonction des fonctionnalités publicitaires de la clientèle, ce qui permet au service de diffusion d’images d’ignorer l’extension du fichier.

L’avantage de l’utilisation de la négociation de contenu est que les navigateurs qui ne font pas de publicité pour la prise en charge de WebP obtiendront toujours le format de fichier JPG ou PNG sans aucune modification nécessaire dans le balisage de la page. Cela offre une compatibilité optimale pour les sites existants et garantit un chemin d’accès le plus fluide possible vers une transition vers une diffusion d’images optimisées pour le web.

### Puis-je utiliser la diffusion d’images optimisées pour le web avec mon propre composant ?

Oui, le service de diffusion d’images optimisé pour le web peut être utilisé par des composants personnalisés, qui sont créés par [extension du composant Image,](/help/developing/customizing.md)

Vous trouverez ci-dessous une interface de service que vous pouvez utiliser pour générer l’URL de la ressource.

```
com.adobe.cq.wcm.spi.AssetDelivery.getDeliveryURL(Resource resource, Map<String, Object> parameterMap)
```

>[!WARNING]
>
>Les incorporations d’URL directe dans une expérience qui n’est pas créée par le biais du SPI mentionné ci-dessus (disponible sur les sites AEM as a Cloud Service) ne respectent pas les [Conditions d’utilisation de Media Library](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/admin/medialibrary.html?lang=fr#use-media-library).

### Les images peuvent-elles ne pas s’afficher lorsque vous avez activé les images optimisées pour le web ? {#failure-to-deliver}

Non, cela ne devrait jamais se produire pour les raisons suivantes.

* Dans le HTML, le balisage ne change pas lors de l’activation des images optimisées pour le web. Seule la valeur de l’attribut `src` sur l’élément image change.
* Lorsque le nouveau service d’image n’est pas disponible ou ne peut pas traiter l’image souhaitée, l’URL générée [bascule vers le servlet Image adaptative.](#fallback)

Cependant, les règles du Dispatcher peuvent bloquer le service de diffusion d’images optimisées pour le web. Les URL du service de diffusion d’images commencent par `/adobe`. L’examen des journaux du dispatcher pour les demandes rejetées comme [décrit ici](https://experienceleague.adobe.com/docs/experience-manager-learn/ams/dispatcher/common-logs.html?lang=fr#filter-rejects) doit vous aider à résoudre les problèmes rencontrés lors de la diffusion des images sur le navigateur.
