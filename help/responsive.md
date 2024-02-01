---
title: Conception réactive des composants principaux
description: Découvrez la conception réactive des composants principaux et comment elle peut affecter votre projet.
role: Architect, Developer, Admin, User
source-git-commit: d39fe0084522f67664203a026340b23d325c1883
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---


# Conception réactive des composants principaux {#responsive-design}

Tous les composants principaux sont conçus pour être entièrement réactifs, ce qui garantit une expérience transparente sur tous les appareils. Il est important de noter que certains composants avancés, tels que le [Carrousel,](/help/components/carousel.md) [Onglets,](/help/components/tabs.md) et [Composants d’accordéon,](/help/components/accordion.md) peut nécessiter une attention particulière dans le contexte du projet d’implémentation afin de maintenir la réactivité dans toutes les conditions.

Étant donné les différentes façons dont ces composants peuvent présenter un comportement réactif et l’engagement de l’Adobe à garder les composants principaux légers prêts à l’emploi, la responsabilité de la mise en oeuvre d’aspects réactifs détaillés est volontairement laissée au projet.

Par exemple, sur les écrans étroits, le composant Onglets peut s’adapter en brisant de larges onglets sur de nouvelles lignes, en autorisant le défilement vertical, en transformant les onglets en menus déroulants ou en adoptant un style d’accordéon. En raison de l’impact potentiel sur les performances que provoquerait la mise en oeuvre de tous ces comportements, la variable [clientlibs](/help/developing/including-clientlibs.md#provided) sont destinées à servir de point de départ aux implémentateurs plutôt qu’à fournir une solution exhaustive.
