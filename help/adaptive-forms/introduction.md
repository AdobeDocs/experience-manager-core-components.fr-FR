---
title: AEM Présentation des composants principaux de Forms adaptatif
description: Créez des expériences d’inscription attrayantes (formulaires) à l’aide de la flexibilité des composants principaux de Forms adaptatif et diffusez-les avec la puissance d’Adobe Experience Manager.
role: Architect, Developer, Admin, User
source-git-commit: b378fbd5695f82b8fc9de3a2d53a8387099ae33b
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 13%

---


# Présentation des composants principaux de Forms adaptatif {#adaptive-forms-core-components-introduction}

À l’aide des composants principaux de Forms adaptatif dans Adobe Experience Manager, vous pouvez créer des expériences d’inscription attrayantes en utilisant la flexibilité et les options de personnalisation disponibles.

## Composants principaux  {#overview}

Dans Adobe Experience Manager (AEM), les composants sont les blocs de création utilisés pour créer des pages et des formulaires. Ils offrent aux auteurs un moyen simple et puissant de créer et de gérer du contenu, tout en offrant aux développeurs la flexibilité et l’extensibilité nécessaires à la création de composants personnalisés. Ils sont conçus pour accélérer le développement et réduire les coûts de maintenance des sites web et des formulaires, être flexibles et peuvent être facilement personnalisés en fonction des besoins spécifiques d’un site web et d’un formulaire.

Les composants principaux sont également conçus pour être réactifs et prendre en charge un large éventail d’appareils, notamment des ordinateurs de bureau, des tablettes et des smartphones. Ils se conforment également aux dernières normes et bonnes pratiques web, ce qui en fait une solution robuste et fiable pour créer du contenu web.

Dans l’ensemble, les composants principaux sont un outil essentiel pour la création et la gestion de contenu web dans AEM. Ils offrent une solution puissante et flexible qui peut contribuer à réduire le temps de développement et les coûts de maintenance, tout en offrant une expérience utilisateur optimale aux visiteurs du site web.

## Composants principaux de Forms adaptatif

Les composants principaux de Forms adaptatif sont un ensemble de 24 composants Open Source compatibles avec BEM qui sont construits sur la base des composants principaux de la gestion de contenu web Adobe Experience Manager. Elles sont spécialement conçues pour être utilisées pour créer des Forms adaptatives, qui sont des formulaires qui s’adaptent au périphérique, au navigateur et à la taille d’écran de l’utilisateur.

Ces composants peuvent être utilisés pour créer des expériences de capture et d’inscription de données exceptionnelles en proposant un large éventail d’options de champ de formulaire, notamment des champs de texte, des cases à cocher, des menus déroulants, etc. Ils comprennent également des fonctionnalités telles que la validation, la logique conditionnelle et la conception réactive, qui peuvent être utilisées pour créer des formulaires conviviaux et faciles à utiliser.

En outre, comme ces composants sont Open Source, les développeurs peuvent facilement personnaliser et étendre les composants pour répondre aux besoins spécifiques de leur entreprise. Et ces composants sont construits sur une méthodologie BEM qui garantit qu&#39;ils sont extensibles et maintenables.

![](assets/sample-adaptive-form.png)

## Fonctions {#features}

|  |  |
|---|---|
| Prêts pour la production | Les composants principaux de Forms adaptatif sont 24 composants WCM robustes. |
| Prêts pour le cloud | Disponible pour  [AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/home.html). |
| Polyvalents | Les composants représentent des concepts génériques avec lesquels les auteurs Forms peuvent assembler pratiquement n’importe quelle mise en page. |
| Configurables | Au niveau du modèle [stratégies de contenu](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html?lang=fr#content-policies) définir les fonctionnalités qui peuvent être utilisées ou non. |
| Accessibles | Ils fournissent des libellés ARIA, prennent en charge la navigation au clavier ([problèmes connus](https://github.com/adobe/aem-core-wcm-components/issues?utf8=✓&amp;q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle)) et le texte pour les technologies d’assistance telles que les lecteurs d’écran. |
| Thème utilisable | Les composants implémentent le [système de style](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=fr) et le balisage suit les [conventions CSS BEM](https://getbem.com/). |
| Personnalisables | Plusieurs modèles permettent une personnalisation facile, depuis l’ajustement du code HTML jusqu’à la réutilisation des fonctionnalités avancées. |
| Contrôle de version | La [politique de contrôle de version](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) garantit que les composants principaux ne rendent pas votre site inopérable lorsqu’ils améliorent des éléments susceptibles de vous affecter. |
| Open source | Si quelque chose ne va pas, contribuez en apportant votre amélioration. |

<!-- comply with [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), -->


## Avantages {#benefits}

Les expériences de capture de données sont essentielles pour la génération et l’inscription de pistes. Les composants principaux de Forms adaptatif offrent une solution puissante pour créer des formulaires optimisés pour la capture de données. Voici quelques raisons d’utiliser les composants principaux pour créer ces expériences sur les composants de base :

* **Disponibilité sur GitHub et documentation complète**: Les composants principaux de Forms adaptatif AEM sont Open Source et disponibles sur GitHub, avec une documentation complète. Cela permet aux développeurs de comprendre plus facilement les composants et leur fonctionnement, ainsi que de contribuer à leur développement. Le [aemcomponents.dev](https://www.aemcomponents.dev/) Le site web est également une ressource précieuse, où les développeurs peuvent voir les composants en action et accéder à la documentation détaillée.

* **Modèle BEM pour le style**: Les composants principaux suivent le modèle BEM (Block Element Modifier) pour le style, qui est une méthodologie bien établie et largement utilisée pour organiser les CSS. Cela permet aux développeurs de comprendre plus facilement comment les styles sont organisés et comment les modifier en fonction de leurs besoins spécifiques.

* **Aucune dépendance sur les bibliothèques tierces**: L’un des avantages des composants principaux est qu’ils ne dépendent pas des bibliothèques JavaScript tierces, y compris JQuery et Underscore. Les composants sont ainsi plus rapides et plus légers, et plus faciles à intégrer dans une mise en oeuvre d’AEM existante.

* **Concentrez-vous sur les performances et l’accessibilité**: Les composants principaux sont conçus en tenant compte des performances et de l’accessibilité, qui se reflètent dans leurs scores Google Lighthouse élevés et dans leurs scores web vitaux. Cela facilite la création de pages web accessibles et performantes pour les développeurs, ce qui est de plus en plus important dans le paysage numérique actuel.

* **Composants de formulaire dans le modèle et les thèmes Sites 30**: Les composants principaux prennent en charge les composants de formulaire dans le modèle et les thèmes Sites 30, ce qui facilite la création et la personnalisation de formulaires dans AEM.

* **Style plus facile**: Les composants principaux sont plus faciles à mettre en forme que leurs homologues des composants de base. Le processus de création du thème est similaire à Sites, avec la possibilité d’hériter du même thème/CSS de la page Sites parente. En outre, le modèle BEM pour le style facilite la compréhension et la modification des styles.

* **Accessibilité**: Les composants principaux de Forms adaptatif prennent en charge les normes et directives d’accessibilité afin de s’assurer que les formulaires peuvent être utilisés par les personnes présentant un handicap, y compris celles qui utilisent des technologies d’assistance telles que les lecteurs d’écran.


<!-- >, such as  [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), to ensure that forms can be used by people with disabilities, including those using assistive technologies such as screen readers.

*   **Alignment with AEM Sites**: The Core Components are designed to be more aligned with AEM Sites, making it easier for Sites users to adopt and use them without having to learn anything new. The components use the same front-end pipeline as Sites, making it easier to style and modify their appearance. 

<!-- Additionally, the following points further illustrate this alignment:

    *   **Authoring experience inline with Page editor**: The Core Components have an authoring experience that is inline with the Sites editor, with dialogs and other experiences similar to the Page editor. This makes it easier for Sites users to create and manage forms within the familiar context of the Sites editor.

    *   **Inline form editing in Sites editor**: The Core Components allow  inline form editing within the Sites editor, avoiding the need to switch back and forth between editors. This streamlines the authoring experience and makes it easier to create and manage forms.

    *   **Inheriting Sites features in Forms**: Forms authored within a Sites page inherit the same features as Sites. This provides a seamless and integrated experience for creating and managing forms within the context of AEM Sites 
    
    <!--including Multi Site Manager, the ability to use Sites components within a form for static content, support for scheduled publish/unpublish, form translation aligned with Sites translation, versioning, and targeting -->



## Conditions requises {#requirements}

Les composants principaux de Forms adaptatif ont les exigences suivantes.

| AEM | Module complémentaire AEM Forms | Composants principaux |
|---|---|---|
| AEM as a Cloud Service | Forms – Inscription numérique | [Version 2.20.8](/help/versions.md)+ |


## Composants principaux de Forms adaptatif {#components}

Vous pouvez utiliser [Éditeur Forms adaptatif](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html) pour créer un Forms adaptatif basé sur des composants principaux. La version actuelle des composants principaux de Forms adaptatif comprend les composants répertoriés ci-dessous.

* Accordéon
* Bouton
* Case à cocher Groupe
* Sélecteur de date
* Liste déroulante
* Entrée email
* Conteneur de formulaires
* Pièce jointe
* Pied de page
* En-tête
* Onglets horizontaux
* Image
* Entrée numérique
* Conteneur de panneau
* Bouton radio
* Bouton Réinitialiser
* Bouton Envoyer
* Entrée téléphonique
* Entrée de texte
* Texte
* Titre
* réactif

