---
title: Chemins vers le succès avec les composants principaux
description: Comment réussir la mise en oeuvre de votre projet avec les composants principaux
translation-type: tm+mt
source-git-commit: c338428a681f652d17bb972fb6a2abf216a338c3

---


# Chemins vers le succès avec les composants principaux {#paths-to-success}

Les composants principaux sont puissants, flexibles et faciles à utiliser et à personnaliser. Suivez quelques directives clés décrites dans ce pour vous assurer que votre projet avec les composants principaux est un succès.

## Deux chemins vers la réussite {#two-paths}

Il existe deux approches de base pour mettre en oeuvre les éléments de base, qui peuvent mener à la réussite, mais qui ont leurs propres compromis qui doivent être examinées projet par projet.

1. Faites correspondre vos conceptions aux composants principaux et prenez le code HTML qu’elles fournissent. Ou
1. Si vous devez vous conformer à des normes HTML déjà définies, vous devrez faire plus d&#39;efforts et ne pas bénéficier de tous les avantages des composants principaux.

## Pièges courants dans la mise en oeuvre des composants {#common-pitfalls}

Deux problèmes courants qui mènent à des projets qui ne réussissent pas avec les composants principaux sont les suivants :

* **Conceptions** finalisées - Il se peut même qu&#39;elles soient approuvées au niveau C et qu&#39;elles soient remises à l&#39;équipe de développement pour qu&#39;elles soient mises en oeuvre au pixel près sans se soucier de la technologie sous-jacente.
* **Un guide** de style HTML à l’échelle du - Ces guides doivent trop souvent être suivis dogmatiquement par les composants qui appliquent des styles d’un point de vue descendant.

Dans les deux cas, les exigences imposées aux composants sont si strictes et si spécifiques qu’il est difficile de les rendre conformes aux composants principaux ou aux composants prêts à l’emploi, ce qui entraîne le développement massif de composants personnalisés.

##  précoce {#start-early}

Au lieu de considérer uniquement les composants principaux lors de la phase de mise en oeuvre de votre projet, vous  déjà avec les composants principaux pendant la phase de création et de création de structures filaires.

### Utilisation de la bibliothèque de composants {#component-library}

Référencez la bibliothèque [de](https://adobe.com/go/aem_cmp_library) composants déjà en phase de conception. Les composants principaux sont puissants et flexibles et peuvent vous amener loin comme point de départ. Ajoutez uniquement des composants personnalisés lorsqu’il existe un réel besoin commercial qui ne peut pas être raisonnablement réalisé avec un composant principal.

### Utilisation du kit d’interface utilisateur pour Adobe XD {#ui-kit}

Dès qu’un composant personnalisé s’avère nécessaire, utilisez le kit [d’interface utilisateur pour Adobe XD](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_Wireframe.xd) afin que les concepteurs puissent à la création des structures filaires et des conceptions avec les composants principaux comme blocs de création.

## Ne pas ignorer les fonctionnalités puissantes {#powerful-features}

Les fonctionnalités d’AEM et des composants principaux peuvent être très puissantes, mais aussi très subtiles et les possibilités de certaines fonctionnalités peuvent ne pas être immédiatement apparentes pour un concepteur.

### Fragments de contenu {#content-fragments}

[Les fragments de contenu vous permettent de créer du contenu compatible avec tous les canaux, ainsi que des variantes (éventuellement spécifiques aux canaux). ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/content-fragments.html) Vous pouvez ensuite utiliser ces fragments et leurs variantes lors de la création de vos pages de contenu.

En même temps que l’outil d’exportation JSON mis à jour, les fragments de contenu structuré peuvent également être utilisés pour diffuser du contenu AEM via Content Services à des canaux autres que des pages AEM.

### Modèles de fragments d’expérience {#experience-fragment-templates}

Si l’auteur souhaite réutiliser des parties (un fragment d’une expérience) d’une page. Without [Experience Fragments,](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/experience-fragments.html) the author would need to copy and paste that fragment. La création et la gestion de ces expériences de copier/coller sont chronophages et sources d’erreurs pour l’utilisateur. Les fragments d’expérience rendent inutiles les opérations de copier/coller.

### Composant Incorporer {#embed-component}

[Le composant](/help/components/embed.md) Incorporer permet non seulement d’inclure des ressources externes telles que le contenu vidéo YouTube, mais il est également extensible pour lui permettre de s’adapter au contenu spécifique aux besoins d’un projet.