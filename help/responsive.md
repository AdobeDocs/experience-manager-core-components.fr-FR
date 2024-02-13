---
title: Conception réactive des composants principaux
description: Découvrez la conception réactive des composants principaux et comment elle peut affecter votre projet.
role: Architect, Developer, Admin, User
source-git-commit: d39fe0084522f67664203a026340b23d325c1883
workflow-type: ht
source-wordcount: '174'
ht-degree: 100%

---


# Conception réactive des composants principaux {#responsive-design}

Tous les composants principaux sont conçus pour être entièrement réactifs, ce qui garantit une expérience transparente sur tous les appareils. Il est important de noter que certains composants avancés, tels que le [Carousel](/help/components/carousel.md), les [Onglets](/help/components/tabs.md) et les [Composants Accordéon](/help/components/accordion.md), peuvent nécessiter une attention particulière dans le contexte du projet d’implémentation afin de maintenir la réactivité dans toutes les conditions.

Étant donné les différentes façons dont ces composants peuvent présenter un comportement réactif, et du fait de l’engagement d’Adobe à garder les composants principaux légers et prêts à l’emploi, la responsabilité de l’implémentation des aspects réactifs détaillés est volontairement laissée au projet.

Par exemple, sur les écrans étroits, le composant Onglets peut s’adapter en répartissant les onglets larges sur de nouvelles lignes, en autorisant le défilement vertical, en transformant les onglets en menus déroulants ou en adoptant un style en accordéon. En raison de l’impact potentiel sur les performances que provoquerait la mise en œuvre de tous ces comportements, les [bibliothèques clientes](/help/developing/including-clientlibs.md#provided) sont destinées à servir de point de départ aux personnes implémentant le projet plutôt qu’à fournir une solution exhaustive.
