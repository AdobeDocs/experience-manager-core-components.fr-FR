---
title: Instructions relatives aux composants
seo-title: Instructions relatives aux composants
description: Les composants principaux suivent les modèles de mise en œuvre modernes qui sont très différents des composants de base.
seo-description: Les composants principaux suivent les modèles de mise en œuvre modernes qui sont très différents des composants de base.
uuid: b 1 daea 89-da 3 c -454 f -8 ab 5-d 75 a 19412954
contentOwner: Utilisateur
content-type: référence
topic-tags: développement
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 170 dba 8 f-a 2 ed -442 e-a 56 e -1126 b 338 c 36 e
translation-type: tm+mt
source-git-commit: 62643e5bd49ab006230f65004bb9374822dcc017

---


# Instructions relatives aux composants {#component-guidelines}

Les composants [principaux](developing.md) suivent les modèles de mise en œuvre modernes qui sont très différents des composants de base.

Cette page explique ces modèles et à quel moment les utiliser pour créer vos propres composants. La première section [Modèles généraux de composants](guidelines.md) s&#39;applique à n&#39;importe quel type de composant, tandis que la deuxième section [Modèles de composants réutilisables](guidelines.md) s&#39;applique aux composants destinés à être réutilisés sur plusieurs sites ou projets, comme les composants principaux d&#39;une instance.

## Modèles généraux de composants {#general-component-patterns}

Les instructions de cette section sont recommandées pour tout type de composant, que le composant soit spécifique à un projet unique ou qu&#39;il soit censé être largement réutilisé sur plusieurs sites ou projets.

### Composants configurables {#configurable-components}

Les composants peuvent avoir des dialogues avec diverses options. Cela doit être utilisé pour rendre les composants souples et configurables et éviter de mettre en œuvre plusieurs composants qui sont principalement des variantes les uns des autres.

En règle générale, si une structure filaire ou une conception contient des variations d&#39;éléments similaires, ces variations ne doivent pas être implémentées comme des composants différents, mais comme un composant avec des options pour choisir entre les variations.

Pour aller plus loin, si les composants sont réutilisés sur plusieurs sites ou projets, reportez-vous à la [section](#pre-configurable-capabilities) Fonctionnalités préconfigurables.

### Séparation des préoccupations {#separation-of-concerns}

Le maintien de la logique (ou du modèle) d&#39;un composant distinct du modèle d&#39;annotation (ou affichage) est généralement une bonne pratique. Il existe plusieurs manières d&#39;obtenir ce résultat. Toutefois, il est recommandé d&#39;utiliser [les modèles](https://sling.apache.org/documentation/bundles/models.html) Sling pour la logique et la langue de modèle [HTML](https://helpx.adobe.com/experience-manager/htl/using/overview.html) (HTL) pour les balises, comme les composants principaux.

Les modèles Sling sont un ensemble d&#39;annotations Java permettant d&#39;accéder facilement aux variables nécessaires à partir des POJO. Ils offrent par conséquent une manière simple, puissante et performante d&#39;implémenter la logique Java pour les composants.

HTL a été conçu pour être un langage de modèle sécurisé et simple adapté à AEM. Elle peut appeler de nombreuses formes de logique, ce qui la rend très souple.

## Modèles de composants réutilisables {#reusable-component-patterns}

Les instructions de cette section peuvent également être utilisées pour tout type de composant, mais elles sont plus logiques pour les composants destinés à être réutilisés sur plusieurs sites ou projets, comme les composants principaux d&#39;une instance. Ces instructions peuvent donc être ignorées pour les composants qui ne sont utilisés que sur un seul site ou projet.

### Fonctionnalités préconfigurables {#pre-configurable-capabilities}

Outre la modification de la boîte de dialogue utilisée par les auteurs de pages, les composants peuvent également avoir un dialogue de conception pour les auteurs de modèles afin de les préconfigurer. L&#39;éditeur [de modèles](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) permet de configurer toutes ces préconfigurations, appelées « Stratégies ».

Pour rendre les composants aussi réutilisables que possible, ils doivent être fournis avec des options significatives pour préconfigurer. Cela permet d&#39;activer ou de désactiver les fonctionnalités des composants pour répondre aux besoins spécifiques des différents sites.

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T17:49:04.584-0400

Unclear how I can add my own capability toggle (for example, if i extend a component and want to toggle that extended functionality ... )

 -->

### Modèle de composant proxy {#proxy-component-pattern}

Comme chaque ressource de contenu possède `sling:resourceType` une propriété qui référence le composant pour le rendre, il est généralement recommandé d&#39;avoir ces propriétés pointant vers des composants spécifiques au site au lieu de pointer vers des composants partagés par plusieurs sites. Ceci offre davantage de souplesse et évite la restructuration du contenu si un site nécessite un comportement différent pour un composant, car cette personnalisation peut alors être obtenue sur le composant spécifique au site et n&#39;affectera pas les autres sites.

Toutefois, pour que les composants spécifiques au projet ne dupliquent aucun code, ils doivent chacun faire référence au composant parent partagé avec la `sling:resourceSuperType` propriété. Ces composants spécifiques au projet qui font principalement référence aux composants parents sont appelés « composants proxy ». Les composants proxy peuvent être entièrement vides s&#39;ils héritent entièrement de la fonctionnalité ou qu&#39;ils peuvent redéfinir certains aspects du composant.

### Contrôle des composants {#component-versioning}

Les composants doivent être maintenus entièrement : compatible avec le temps, mais parfois les modifications qui ne peuvent pas être toujours compatibles sont nécessaires. Une solution à ces besoins opposés consiste à introduire le contrôle de version des composants en ajoutant un nombre dans leur chemin de type de ressource et, dans le cas complet, les noms de classe Java qualifiés de leurs implémentations. Ce numéro de version représente une version majeure définie par [des instructions](https://semver.org/)de contrôle sémantique, qui n&#39;est incrémentée que pour les modifications qui ne sont pas rétrocompatibles.

Les modifications incompatibles aux aspects suivants des composants entraîneront une nouvelle version :

* Modèles Sling (suivant les instructions de création sémantique)
* Scripts et modèles HTL
* Balises HTML et sélecteurs CSS
* Représentation JSON
* Boîtes de dialogue

Pour plus d&#39;informations, reportez-vous au [document Stratégies de contrôle](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-Policies) de version de github.

Le contrôle de version des composants crée une forme de contrat important pour les mises à niveau car elle précise quand un élément doit être restructuré. Voir aussi la section [Compatibilité de mise à niveau de la section des personnalisations](customizing.md#upgrade-compatibility-of-customizations), qui explique quelles sont les différents types de personnalisation requis pour la mise à niveau.

Pour éviter des migrations de contenu douloureuses, il est important de ne jamais pointer directement sur les composants de version des ressources de contenu. En règle générale, une `sling:resourceType` du contenu ne doit jamais comporter de numéro de version, ou la mise à niveau des composants nécessite que le contenu soit également restructuré. Le meilleur moyen pour éviter cela est de suivre le [modèle de composant proxy](#proxy-component-pattern) décrit ci-dessus.

### Interfaces de modèles {#model-interfaces}

Il s&#39;agit de l `data-sly-use` &#39;instruction du HTL de pointer vers une interface Java, tandis que l&#39;implémentation du modèle Sling s&#39;inscrit également au type de ressource du composant.

Lorsqu&#39;il est combiné avec le [modèle de composant proxy](#proxy-component-pattern) décrit ci-dessus, cette forme de liaison double offre des points d&#39;extension suivants :

1. Un site peut redéfinir l&#39;implémentation d&#39;un modèle Sling en l&#39;enregistrant au type de ressource du composant proxy, sans avoir à tenir compte du fichier HTL qui peut toujours pointer vers l&#39;interface.
1. Un site peut redéfinir l&#39;annotation HTL d&#39;un composant, sans avoir à tenir compte de la logique d&#39;implémentation à pointer.

## Ensemble {#putting-it-all-together}

Vous trouverez ci-dessous un aperçu de la structure de liaison du type de ressource entière, en prenant l&#39;exemple du composant principal Titre. Il illustre la manière dont un composant proxy spécifique au site permet de résoudre le contrôle des composants, afin d&#39;éviter que la ressource de contenu contienne un numéro de version. Il indique ensuite comment le fichier `title.html`[HTL](https://helpx.adobe.com/experience-manager/htl/using/overview.html) du composant utilise l&#39;interface de modèle, tandis que l&#39;implémentation se lie à la version spécifique du composant par le biais [des annotations du modèle](https://sling.apache.org/documentation/bundles/models.html) Sling.

![Présentation de la liaison des ressources](assets/chlimage_1-32.png)

Vous trouverez ci-dessous un autre aperçu qui n&#39;affiche pas les détails du POJO d&#39;implémentation, mais révèle la manière dont les modèles et [stratégies associés](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/page-templates-editable.html) sont référencés.

`cq:allowedTemplates` La propriété indique les modèles qui peuvent être utilisés pour un site et indique `cq:template` à chaque page quel est le modèle associé. Chaque modèle est composé de trois parties :

* **structure**
contient les ressources qui seront forcées à être présentes sur chaque page et que l&#39;auteur de la page ne pourra pas supprimer, comme par exemple les composants d&#39;en-tête de page et de pied de page.
* **initial**
Contient le contenu initial qui sera dupliqué dans la page lors de sa création.
* **stratégies**
contient pour chaque composant le mappage à une stratégie, qui est la préconfiguration du composant. Ce mappage permet de réutiliser les stratégies dans les modèles et donc d&#39;être gérées de manière centralisée.

![Modèles et présentation de la stratégie](assets/screen_shot_2018-12-07at093102.png)

**À lire aussi :**

* [Utilisation des composants](using.md) principaux - Soyez opérationnel avec les composants principaux de votre propre projet.
* [Personnalisation des composants principaux](customizing.md) - pour savoir comment mettre en forme et personnaliser les composants principaux.
