---
title: Composant Incorporer (v1)
description: Le composant Incorporer permet d’incorporer du contenu externe dans une page de contenu AEM.
role: Architect, Developer, Admin, User
exl-id: 28a2d196-cc1f-4e29-a8e4-c2e0acba3bfc
source-git-commit: e291d4c1bfd37292d68c236178f9681c4e5ee741
workflow-type: tm+mt
source-wordcount: '1240'
ht-degree: 100%

---

# Composant Incorporer (v1) {#embed-component}

Le composant Incorporer des composants principaux permet d’incorporer du contenu externe dans une page de contenu AEM.

## Utilisation {#usage}

Le composant Incorporer des composants principaux permet à l’auteur de contenu de définir le contenu externe sélectionné à incorporer dans une page de contenu AEM. En outre, une option permet de définir du code HTML de forme libre à incorporer.

* Les propriétés du composant peuvent être définies dans la [boîte de dialogue de configuration](#configure-dialog).
* Les valeurs par défaut du composant lors de son ajout à une page peuvent être définies dans la [boîte de dialogue de conception](#design-dialog).

## Version et compatibilité {#version-and-compatibility}

Ce document décrit la version v1 du composant Incorporer, qui a été introduite avec la version 2.7.0 des composants principaux en septembre 2019.

>[!CAUTION]
>
>Ce document décrit la version v1 du composant Incorporer.
>
>Pour plus d’informations sur la version actuelle du composant Incorporer, consultez le document [Composant Incorporer](/help/components/embed.md).

## Exemple de sortie de composant {#sample-component-output}

Pour tester le composant Incorporer et obtenir des exemples d’options de configuration, ainsi que des sorties HTML et JSON, consultez la [Bibliothèque de composants](https://adobe.com/go/aem_cmp_library_embed).

## Détails techniques {#technical-details}

La documentation technique la plus récente sur le composant Incorporer [se trouve sur GitHub](https://adobe.com/go/aem_cmp_tech_embed_v1).

Vous trouverez plus d’informations sur le développement des composants principaux dans la [documentation destinée aux développeurs de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

La boîte de dialogue de configuration permet à l’auteur de contenu de définir la ressource externe à incorporer dans la page. Sélectionnez d’abord le type de ressource à incorporer :

* [URL](#url)
* [Élément intégrable](#embeddable)
* [HTML](#html)

Pour chaque type d’intégration, vous pouvez définir un **ID** de publicité. Cette option permet de contrôler l’identifiant unique du composant dans le code HTML et dans la [couche de données](/help/developing/data-layer/overview.md).

* Si rien n’est indiqué, un ID unique est généré automatiquement et peut être trouvé en examinant la page obtenue.
* Si un ID est spécifié, il incombe à l’auteur de s’assurer qu’il est unique.
* La modification de l’ID peut avoir un impact sur le suivi CSS, JS et de couche de données.

### URL {#url}

L’incorporation la plus simple se fait par le biais d’une URL. Il vous suffit de coller l’URL de la ressource à incorporer dans le champ **URL**. Le composant tente d’accéder à la ressource. Si le rendu peut être effectué par l’un des processeurs, il affiche un message de confirmation sous le champ **URL**. Si ce n’est pas le cas, le champ sera indiqué comme étant dans un état d’erreur.

Le composant Incorporer est fourni avec des processeurs pour les types de ressources suivants :

* les ressources conformes à la [norme oEmbed](https://oembed.com/), notamment Facebook Post, Instagram, SoundCloud, Twitter et YouTube ;
* Pinterest.

Les développeurs peuvent ajouter d’autres processeurs d’URL en [consultant la documentation sur le composant Incorporer destinée aux développeurs.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![Boîte de dialogue de modification du composant Incorporer pour l’URL](/help/assets/embed-url.png)

### Élément intégrable {#embeddable}

Les éléments intégrables permettent une plus grande personnalisation de la ressource incorporée, qui peut être paramétrée et inclure des informations supplémentaires. Un auteur peut effectuer un choix parmi des éléments intégrables approuvés préconfigurés. De plus, le composant est fourni avec un élément intégrable YouTube prêt à l’emploi.

Le champ **Élément intégrable** définit le type de processeur que vous souhaitez utiliser. Dans le cas de l’élément intégrable YouTube, vous pouvez ensuite définir les éléments suivants :

* **ID de la vidéo** : identifiant vidéo unique de YouTube de la ressource que vous souhaitez incorporer.
* **Largeur** : largeur de la vidéo incorporée.
* **Hauteur** : hauteur de la vidéo incorporée.
* **Activer Silence** : ce paramètre indique si le son de la vidéo est coupé par défaut. L’activation de cette option améliore les chances que la lecture automatique fonctionne dans les navigateurs modernes.
* **Activer la lecture automatique** : ce paramètre détermine si la lecture de la vidéo initiale démarre automatiquement lors du chargement du lecteur. Il ne s’applique qu’à l’instance de publication ou lors de l’utilisation de l’option **Afficher comme publié(e)** dans l’instance de création.
* **Activer le bouclage** : dans le cas d’une vidéo unique, ce paramètre indique si le lecteur doit lire la vidéo initiale à plusieurs reprises. Dans le cas d’une liste de lecture, le lecteur lit l’intégralité de la liste de lecture, puis repart du début à la première vidéo.
* **Activer la lecture intégrée (iOS)** : ce paramètre détermine si les vidéos sont lues de manière intégrée (activé) ou en plein écran (désactivé) dans un lecteur HTML5 sous iOS.
* **Vidéos connexes sans restriction** : si cette option est désactivée, les vidéos connexes viendront du même canal que la vidéo qui vient d’être lue, sinon elles peuvent provenir de n’importe quel canal.

Notez que les options doivent être activées dans la [boîte de dialogue de conception](#design-dialog) et peuvent être définies comme valeurs par défaut.

D’autres éléments intégrables proposent des champs similaires et peuvent être définis par un développeur en [consultant la documentation sur le composant Incorporer destinée aux développeurs.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![Boîte de dialogue de modification du composant Incorporer pour les éléments intégrables](/help/assets/embed-embeddable.png)

>[!NOTE]
>Pour être accessibles à l’auteur de la page, les éléments intégrables doivent être activés au niveau du modèle au moyen de la [boîte de dialogue de conception](#design-dialog).

### HTML {#html}

Vous pouvez ajouter du code HTML de forme libre à votre page à l’aide du composant Incorporer.

![Boîte de dialogue de modification du composant Incorporer pour le code HTML](/help/assets/embed-html.png)

>[!NOTE]
>Les balises non sécurisées, telles que les scripts, sont filtrées à partir du code HTML entré et ne sont pas affichées sur la page obtenue.

#### Sécurité {#security}

Les balises HTML que l’auteur peut entrer sont filtrées à des fins de sécurité pour éviter toute attaque de script entre sites qui pourrait permettre aux auteurs d’obtenir des droits d’administration, par exemple.

*En règle générale,* tous les scripts et les éléments`style`, ainsi que tous les attributs `on*` et `style` sont supprimés de la sortie.

Toutefois, les règles sont plus complexes, car le composant Incorporer suit l’ensemble de règles de filtrage de la structure d’assainissement HTML AntiSamy d’AEM, qui se trouve à l’adresse `/libs/cq/xssprotection/config.xml`. Cela peut être superposé pour une configuration spécifique au projet par un développeur, si nécessaire.

Vous trouverez des informations de sécurité supplémentaires dans la [documentation du développeur AEM pour les installations On-Premise](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/security.html?lang=fr), ainsi que les [installations AEM as a Cloud Service.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/home.html?lang=fr)

>[!NOTE]
>Bien que les règles de structure d’assainissement AntiSamy puissent être configurées en superposant `/libs/cq/xssprotection/config.xml`, ces modifications ont un impact sur l’ensemble du comportement HTL et JSP et pas seulement sur le composant principal Incorporer.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet à l’auteur du modèle de définir les options disponibles pour l’auteur du contenu qui utilise le composant Incorporer et les valeurs par défaut définies lors du placement de celui-ci.

### Onglet Types incorporables {#embeddable-types-tab}

![Boîte de dialogue de conception du composant Incorporer](/help/assets/embed-design.png)

* **URL de désactivation** : lorsque cette option est sélectionnée, elle désactive l’option **URL** pour l’auteur de contenu.
* **Désactiver les éléments intégrables** : lorsque cette option est sélectionnée, elle désactive l’option **Élément intégrable** pour l’auteur de contenu, quels que soient les processeurs intégrables autorisés.
* **Désactiver HTML** : lorsque cette option est sélectionnée, elle désactive l’option **HTML** pour l’auteur de contenu.
* **Éléments intégrables autorisés** : sélection multiple qui définit les processeurs intégrables accessibles à l’auteur de contenu, à condition que l’option **Élément intégrable** soit active.

### Onglet YouTube {#youtube-tab}

![Onglet YouTube de la boîte de dialogue de conception du composant incorporé](/help/assets/embed-design-youtube.png)

* **Autoriser la configuration du comportement Silence** : permet à l’auteur du contenu de configurer l’option **Activer Silence** dans le composant lorsque le type d’intégration YouTube est sélectionné.
   * **Valeur par défaut du comportement Muet** : définit automatiquement l’option **Activer Silence** lorsque le type d’intégration YouTube est sélectionné.
* **Autoriser la configuration du comportement Lecture automatique** : permet à l’auteur du contenu de configurer l’option **Activer la lecture automatique** dans le composant lorsque le type d’intégration YouTube est sélectionné.
   * **Valeur par défaut de la lecture automatique** : définit automatiquement l’option **Activer la lecture automatique** lorsque le type d’intégration YouTube est sélectionné.
* **Autoriser la configuration du comportement Boucle** : permet à l’auteur du contenu de configurer l’option **Activer le bouclage** dans le composant lorsque le type d’intégration YouTube est sélectionné.
   * **Valeur par défaut de Boucle** : définit automatiquement l’option **Activer le bouclage** lorsque le type d’intégration YouTube est sélectionné.
* **Autoriser la configuration de la lecture intégrée (iOS)** : permet à l’auteur du contenu de configurer l’option **Activer la lecture intégrée (iOS)** dans le composant lorsque le type d’intégration YouTube est sélectionné.
   * **Valeur par défaut de la lecture intégrée (iOS)** : définit automatiquement l’option **Activer la lecture intégrée (iOS)** lorsque le type d’intégration YouTube est sélectionné.
* **Autoriser la configuration des vidéos connexes** : permet à l’auteur du contenu de configurer l’option **Vidéos connexes sans restriction** dans le composant lorsque le type d’intégration YouTube est sélectionné.
   * **Valeur par défaut des vidéos connexes sans restriction** : définit automatiquement l’option **Vidéos connexes sans restriction** lorsque le type d’intégration YouTube est sélectionné.
