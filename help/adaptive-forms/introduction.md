---
title: AEM Présentation des composants principaux de Forms adaptatif
description: Créez des expériences d’inscription attrayantes (formulaires) à l’aide de la flexibilité des composants principaux de Forms adaptatif et diffusez-les avec la puissance d’Adobe Experience Manager.
role: Architect, Developer, Admin, User
source-git-commit: 781cf351ef52cbb56ff33c2674c8af591c81a30e
workflow-type: tm+mt
source-wordcount: '1069'
ht-degree: 14%

---


# Présentation des composants principaux de Forms adaptatif {#adaptive-forms-core-components-introduction}

À l’aide des composants principaux de Forms adaptatif dans Adobe Experience Manager, vous pouvez créer des expériences d’inscription attrayantes en utilisant la flexibilité et les options de personnalisation disponibles.

## Composants principaux  {#overview}

Dans Adobe Experience Manager (AEM), les composants sont les blocs de création utilisés pour créer des pages et des formulaires. Ils offrent aux auteurs un moyen simple et puissant de créer et de gérer du contenu, tout en offrant aux développeurs la flexibilité et l’extensibilité nécessaires à la création de composants personnalisés.

Les composants principaux sont un ensemble de composants WCM préconfigurés et normalisés, conçus pour accélérer le temps de développement et réduire les coûts de maintenance des sites web. Ces composants comprennent des éléments tels que des champs de texte, des images, des vidéos, etc. Ils sont conçus pour être flexibles et peuvent être facilement personnalisés en fonction des besoins spécifiques d’un site web.

Les composants principaux sont également conçus pour être réactifs et prendre en charge un large éventail d’appareils, notamment des ordinateurs de bureau, des tablettes et des smartphones. Ils se conforment également aux dernières normes et bonnes pratiques web, ce qui en fait une solution robuste et fiable pour créer du contenu web.

En outre, les composants principaux sont conçus pour fonctionner en toute transparence avec d’autres parties de l’AEM, ce qui permet aux auteurs et aux développeurs de créer des formulaires plus interactifs et plus attrayants avec moins d’effort et de temps.

Dans l’ensemble, les composants principaux sont un outil essentiel pour la création et la gestion de contenu web dans AEM. Ils offrent une solution puissante et flexible qui peut contribuer à réduire le temps de développement et les coûts de maintenance, tout en offrant une expérience utilisateur optimale aux visiteurs du site web.

Dans Adobe Experience Manager, les composants sont des éléments structurels qui constituent le contenu des pages et des formulaires en cours de création. Les composants ont toujours été un élément fondamental de l’expérience AEM, rendant la création de page et de formulaire simple mais puissante pour l’auteur et le développement de composants flexibles et extensibles pour le développeur. Les composants principaux sont un ensemble de composants WCM (Web Content Management) normalisés qui permettent d’accélérer le développement et de réduire les coûts de maintenance de vos sites web.

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
| Accessibles | Ils se conforment aux [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), fournissez des libellés ARIA, prenez en charge la navigation au clavier ([problèmes connus](https://github.com/adobe/aem-core-wcm-components/issues?utf8=✓&amp;q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle)) et le texte pour les technologies d’assistance telles que les lecteurs d’écran. |
| Possibilité d’appliquer des thèmes | Les composants implémentent le [système de style](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=fr) et le balisage suit les [conventions CSS BEM](http://getbem.com/). |
| Personnalisables | Plusieurs modèles permettent une personnalisation facile, depuis l’ajustement du code HTML jusqu’à la réutilisation des fonctionnalités avancées. |
| Contrôle de version | La [politique de contrôle de version](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) garantit que les composants principaux ne rendent pas votre site inopérable lorsqu’ils améliorent des éléments susceptibles de vous affecter. |
| Open source | Si quelque chose ne va pas, contribuez en apportant votre amélioration. |

## Avantages {#benefits}

Les expériences de capture de données sont essentielles pour la génération et l’inscription de pistes. Les composants principaux de Forms adaptatif offrent une solution puissante pour créer des formulaires optimisés pour la capture de données. Voici quelques raisons d’utiliser les composants principaux pour créer ces expériences :

* **Personnalisation**: Les composants principaux de Forms adaptatif permettent aux développeurs de personnaliser facilement l’aspect et le comportement des composants de formulaire, tels que les champs de texte, les cases à cocher et les menus déroulants, pour répondre à des besoins spécifiques.

* **Accessibilité**: Les composants principaux de Forms adaptatif prennent en charge les normes et directives d’accessibilité, telles que  [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), afin de garantir que les formulaires peuvent être utilisés par les personnes présentant un handicap, y compris celles qui utilisent des technologies d’assistance telles que les lecteurs d’écran.

* **Formulaires cohérents**: En utilisant les composants principaux de Forms adaptatif, les développeurs peuvent créer des formulaires à l’apparence cohérente, ce qui facilite la compréhension et l’exécution des formulaires pour les utilisateurs, ce qui accroît l’engagement et améliore l’expérience utilisateur.

* **Éditeur WYSIWYG**: AEM Forms offre une interface conviviale, une facilité d’utilisation de l’éditeur WYSIWYG pour utiliser ces composants afin de créer un formulaire adaptatif. Il permet aux auteurs de formulaires de créer et de modifier des formulaires sans avoir à savoir comment coder. Il comprend également un éditeur de règles visuel qui vous permet de créer facilement des actions basées sur des règles et d’implémenter une logique complexe afin d’automatiser le comportement du formulaire sans avoir à écrire de code.

* **Logique conditionnelle**: Les composants principaux de Forms adaptatif prennent en charge l’utilisation d’une logique conditionnelle, ce qui signifie que l’aspect ou le comportement des composants de formulaire peuvent être modifiés en fonction des valeurs saisies par l’utilisateur. Par exemple, certains champs peuvent être masqués ou rendus obligatoires en fonction de la sélection effectuée dans d’autres champs.

* **Validation des données**: Les composants principaux de Forms adaptatif fournissent des fonctionnalités intégrées de validation des données, ce qui permet aux développeurs de s’assurer que les données entrées par l’utilisateur répondent à des critères spécifiques, tels que les longueurs minimales et maximales, les valeurs requises et des formats spécifiques.

## Conditions requises {#requirements}

Les composants principaux de Forms adaptatif ont les exigences suivantes.

| AEM | Module complémentaire AEM Forms | Composants principaux |
|---|---|---|
| AEM as a Cloud Service | Forms – Inscription numérique | [Version 2.20.8](/help/versions.md)+ |


## Composants principaux de Forms adaptatif {#components}

La version actuelle des composants principaux de Forms adaptatif comprend les composants suivants.

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

