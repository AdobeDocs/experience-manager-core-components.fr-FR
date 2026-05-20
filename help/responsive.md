---
title: Conception réactive des composants principaux
description: Découvrez la conception réactive des composants principaux et comment elle peut affecter votre projet.
role: Developer, Admin, User
exl-id: c0eff174-6803-4b44-aeb1-eae3bc8a36ea
TQID: https://experienceleague.adobe.com/wUpRlK8WxDuQzmFJFWAwFZUY-1fo9qOOgbOn-GEwBok
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 178
ht-degree: 100%

---

# Conception réactive des composants principaux {#responsive-design}

Tous les composants principaux sont conçus pour être entièrement réactifs, ce qui garantit une expérience transparente sur tous les appareils. Il est important de noter que certains composants avancés, tels que le [Carousel](/help/components/carousel.md), les [Onglets](/help/components/tabs.md) et les [Composants Accordéon](/help/components/accordion.md), peuvent nécessiter une attention particulière dans le contexte du projet d’implémentation afin de maintenir la réactivité dans toutes les conditions.

Étant donné les différentes façons dont ces composants peuvent présenter un comportement réactif, et du fait de l’engagement d’Adobe à garder les composants principaux légers et prêts à l’emploi, la responsabilité de l’implémentation des aspects réactifs détaillés est volontairement laissée au projet.

Par exemple, sur les écrans étroits, le composant Onglets peut s’adapter en répartissant les onglets larges sur de nouvelles lignes, en autorisant le défilement vertical, en transformant les onglets en menus déroulants ou en adoptant un style en accordéon. En raison de l’impact potentiel sur les performances que provoquerait la mise en œuvre de tous ces comportements, les [bibliothèques clientes](/help/developing/including-clientlibs.md#provided) sont destinées à servir de point de départ aux personnes implémentant le projet plutôt qu’à fournir une solution exhaustive.
