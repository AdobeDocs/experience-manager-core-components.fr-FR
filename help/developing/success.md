---
title: Chemins vers la réussite avec les composants principaux
description: Réussir la mise en œuvre de votre projet avec les composants principaux
translation-type: tm+mt
source-git-commit: c338428a681f652d17bb972fb6a2abf216a338c3
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 100%

---


# Chemins vers la réussite avec les composants principaux {#paths-to-success}

Les composants principaux sont puissants, flexibles et faciles à utiliser et personnaliser. Suivez les instructions décrites dans ce document pour vous assurer que votre projet utilisant les composants principaux soit une réussite.

## Deux chemins vers la réussite {#two-paths}

Il existe deux approches de base pour mettre en œuvre les composants principaux. Elles peuvent toutes deux mener à la réussite, mais elles présentent des arbitrages qui doivent être examinés projet par projet.

1. Faites correspondre vos conceptions aux composants principaux et utilisez le code HTML qu’ils fournissent. Ou
1. Si vous devez vous conformer à des normes HTML déjà définies, vous devrez faire un travail supplémentaire et ne pourrez pas bénéficier de tous les avantages des composants principaux.

## Pièges courants dans la mise en œuvre des composants {#common-pitfalls}

Voici deux problèmes courants qui peuvent entraver la réussite des projets utilisant les composants principaux :

* **Conceptions finalisées** : il peut même s’agir de conceptions approuvées par la direction et qui sont remises à l’équipe de développement pour leur mise en œuvre au pixel près sans se soucier de la technologie sous-jacente.
* **Un guide de style HTML à l’échelle de l’entreprise** : ces guides doivent trop souvent être suivis dogmatiquement par les composants en appliquant les styles d’un point de vue descendant.

Dans les deux cas, les exigences imposées sont si strictes et si spécifiques qu’il est difficile de rendre les composants principaux ou prêts à l’emploi conformes, ce qui entraîne le développement massif de composants personnalisés.

## Commencez tôt {#start-early}

Au lieu de considérer uniquement les composants principaux lors de la phase de mise en œuvre de votre projet, démarrez avec les composants principaux pendant la phase de conception et de création de maquettes.

### Utilisez la bibliothèque de composants {#component-library}

Consultez la [bibliothèque de composants](https://adobe.com/go/aem_cmp_library) dès la phase de conception. Les composants principaux sont puissants et flexibles et peuvent vous amener loin dès le début. Ajoutez uniquement des composants personnalisés lorsqu’il existe un réel besoin métier qui ne peut pas être réalisé de manière raisonnable avec un composant principal.

### Utilisez le kit d’interface utilisateur pour Adobe XD {#ui-kit}

Dès qu’un composant personnalisé s’avère nécessaire, utilisez le [kit d’interface utilisateur pour Adobe XD](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_Wireframe.xd) afin que les concepteurs puissent commencer à créer les maquettes et les conceptions en se servant des composants principaux comme blocs de création.

## Ne passez pas à côté de leurs puissantes fonctionnalités {#powerful-features}

Les fonctionnalités d’AEM et des composants principaux peuvent être très puissantes, mais aussi très subtiles et les possibilités de certaines fonctionnalités peuvent ne pas être immédiatement apparentes pour un concepteur.

### Fragments de contenu {#content-fragments}

[Les fragments de contenu vous permettent de créer du contenu compatible avec tous les canaux, ainsi que des variantes (éventuellement spécifiques aux canaux). ](https://docs.adobe.com/content/help/fr-FR/experience-manager-cloud-service/sites/authoring/fundamentals/content-fragments.html) Vous pouvez ensuite utiliser ces fragments et leurs variantes lors de la création de vos pages de contenu.

En même temps que l’outil d’exportation JSON mis à jour, les fragments de contenu structuré peuvent également être utilisés pour diffuser du contenu AEM via Content Services à des canaux autres que des pages AEM.

### Modèles de fragment d’expérience {#experience-fragment-templates}

Si l’auteur souhaite réutiliser des parties (un fragment d’une expérience) d’une page. Sans les [fragments d’expérience](https://docs.adobe.com/content/help/fr-FR/experience-manager-cloud-service/sites/authoring/fundamentals/experience-fragments.html), il doit copier et coller ce fragment. La création et la gestion de ces expériences de copier/coller sont chronophages et sources d’erreurs pour l’utilisateur. Les fragments d’expérience rendent inutiles les opérations de copier/coller.

### Le composant Incorporer {#embed-component}

[Le composant Incorporer](/help/components/embed.md) permet non seulement d’inclure des ressources externes telles que le contenu vidéo YouTube, mais il est également extensible pour s’adapter selon le contenu spécifique aux besoins d’un projet.