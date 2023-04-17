---
title: Présentation des composants principaux des formulaires adaptatifs AEM
description: Créez des expériences d’inscription attrayantes (formulaires) grâce à la flexibilité des composants principaux des formulaires adaptatifs et diffusez-les avec la puissance d’Adobe Experience Manager.
role: Architect, Developer, Admin, User
exl-id: 6d0f2845-bbb8-4488-a254-b69d7a6290b1
source-git-commit: 1ac6ed00c19a8ae00e6a53d18419890a88235158
workflow-type: tm+mt
source-wordcount: '1169'
ht-degree: 90%

---

# Présentation des composants principaux des formulaires adaptatifs {#adaptive-forms-core-components-introduction}

À l’aide des composants principaux des formulaires adaptatifs dans Adobe Experience Manager, vous pouvez créer des expériences d’inscription attrayantes grâce à la flexibilité et aux options de personnalisation disponibles.

## Composants principaux  {#overview}

Dans Adobe Experience Manager (AEM), les composants sont les blocs de création utilisés pour créer des pages et des formulaires. Ils offrent aux créateurs et aux créatrices un moyen simple et puissant de créer et de gérer du contenu, tout en offrant aux développeurs et aux développeuses la flexibilité et l’extensibilité nécessaires à la création de composants personnalisés. Ils sont conçus pour accélérer le développement et réduire les coûts de maintenance des sites Web et des formulaires, être flexibles et peuvent être facilement personnalisés en fonction des besoins spécifiques d’un site Web ou d’un formulaire.

Les composants principaux sont également conçus pour être réactifs et prendre en charge un large éventail d’appareils, notamment les ordinateurs, les tablettes et les smartphones. Ils se conforment également aux dernières normes et bonnes pratiques Web, ce qui en fait une solution robuste et fiable pour créer du contenu Web.

Dans l’ensemble, les composants principaux sont un outil essentiel pour la création et la gestion de contenu Web dans AEM. Ils offrent une solution puissante et flexible qui peut contribuer à réduire le temps de développement et les coûts de maintenance, tout en offrant une expérience utilisateur optimale aux visiteurs et visiteuses du site Web.

## Composants principaux des formulaires adaptatifs

Les composants principaux des fomulaires adaptatifs sont un ensemble de 24 composants Open Source compatibles avec BEM qui sont construits sur la base des composants principaux de la gestion de contenu web d’Adobe Experience Manager. Ils sont spécialement conçus pour créer des formulaires adaptatifs, qui sont des formulaires qui s’adaptent au périphérique, au navigateur et à la taille d’écran de l’utilisateur ou de l’utilisatrice.

Ces composants peuvent être utilisés pour créer des expériences de capture de données et d’inscription exceptionnelles en proposant un large éventail d’options de champ de formulaire, notamment des champs de texte, des cases à cocher, des menus déroulants, etc. Ils comprennent également des fonctionnalités telles que la validation, la logique conditionnelle et la conception réactive, qui peuvent être utilisées pour créer des formulaires conviviaux et simples.

En outre, comme ces composants sont en open source, les développeurs et les développeuses peuvent facilement les personnaliser et les étendre pour répondre aux besoins spécifiques de leur entreprise. De plus, ces composants sont construits sur une méthodologie BEM qui garantit leur évolutivité et leur mise à jour.

![](assets/sample-adaptive-form.png)

## Fonctions {#features}

|  |  |
|---|---|
| Prêts pour la production | Les composants principaux des formulaires adaptatifs sont 24 composants robustes de gestion de contenu web. |
| Prêts pour le cloud | Disponible pour [AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/home.html?lang=fr). |
| Polyvalents | Les composants représentent des concepts génériques avec lesquels les créateurs et créatrices peuvent assembler pratiquement n’importe quelle disposition. |
| Configurables | Des [politiques de contenu](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html?lang=fr#content-policies) au niveau du modèle définissent les fonctionnalités que les créateurs et créatrices de pages peuvent ou non utiliser. |
| Accessibles | Ils fournissent des libellés ARIA, prennent en charge la navigation au clavier ([problèmes connus](https://github.com/adobe/aem-core-wcm-components/issues?utf8=✓&amp;q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle)) et le texte pour les technologies d’assistance telles que les lecteurs d’écran. |
| Thème utilisable | Les composants implémentent le [système de style](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=fr) et le balisage suit les [conventions CSS BEM](https://getbem.com/). |
| Personnalisables | Plusieurs modèles permettent une personnalisation facile, depuis l’ajustement du code HTML jusqu’à la réutilisation des fonctionnalités avancées. |
| Contrôle de version | La [politique de contrôle de version](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) garantit que les composants principaux ne rendent pas votre site inopérable lorsqu’ils améliorent des éléments susceptibles de vous affecter. |
| Open source | Si quelque chose ne fonctionne pas correctement, contribuez en apportant vos améliorations. |

<!-- comply with [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), -->


## Avantages {#benefits}

Les expériences de capture de données sont essentielles pour la génération de pistes et l’inscription. Les composants principaux des formulaires adaptatifs offrent une solution puissante pour créer des formulaires optimisés pour la capture de données. Voici quelques raisons d’utiliser les composants principaux pour créer ces expériences sur les composants de base :

* **Disponibilité sur GitHub et documentation complète** : les composants principaux des formulaires adaptatifs d’AEM sont en open source et disponibles sur GitHub, avec une documentation complète. Cela permet aux développeurs et aux développeuses de comprendre plus facilement les composants et leur fonctionnement, ainsi que de contribuer à leur développement. Le site Web [aemcomponents.dev](https://www.aemcomponents.dev/) est également une ressource précieuse, où les développeurs et les développeuses peuvent voir les composants en action et accéder à la documentation détaillée.

* **Modèle BEM pour le style** : les composants principaux suivent le modèle BEM (Block Element Modifier) pour le style, qui est une méthodologie bien établie et largement utilisée pour organiser le CSS. Cela permet aux développeurs et aux développeuses de comprendre plus facilement comment les styles sont organisés et comment les modifier en fonction de leurs besoins spécifiques.

* **Aucune dépendance aux bibliothèques tierces** : l’un des avantages des composants principaux est qu’ils ne dépendent pas des bibliothèques JavaScript tierces, y compris JQuery et Underscore. Les composants sont ainsi plus rapides et plus légers, et plus faciles à intégrer dans une implémentation AEM existante.

* **Centrés sur les performances et l’accessibilité** : les composants principaux sont conçus en tenant compte des performances et de l’accessibilité, qui se reflètent dans leurs scores Google Lighthouse élevés et dans leurs scores Web vitaux. Cela facilite la création de pages Web accessibles et performantes pour les développeurs et les développeuses, ce qui est de plus en plus important dans le paysage numérique actuel.

* **Composants de formulaire dans le modèle et les thèmes Sites 30** : les composants principaux prennent en charge les composants de formulaire dans le modèle et les thèmes Sites 30, ce qui facilite la création et la personnalisation de formulaires dans AEM.

* **Style plus facile** : les composants principaux sont plus faciles à mettre en forme que leurs composants de base homologues. Le processus de création du thème est similaire à Sites, avec la possibilité d’hériter du même thème/CSS de la page Sites parente. En outre, le modèle BEM pour le style facilite la compréhension et la modification des styles.

* **Accessibilité** : les composants principaux des formulaires adaptatifs prennent en charge les normes et directives d’accessibilité afin de s’assurer que les formulaires peuvent être utilisés par les personnes présentant un handicap, y compris celles qui utilisent des technologies d’assistance telles que les lecteurs d’écran.

## Composants principaux des formulaires adaptatifs {#components}

La version actuelle des composants principaux des formulaires adaptatifs comprend les composants répertoriés ci-dessous.

* [Accordéon](/help/adaptive-forms/components/accordion.md)
* [Bouton](/help/adaptive-forms/components/button.md)
* [Case à cocher Groupe](/help/adaptive-forms/components/checkbox-group.md)
* [Sélecteur de date](/help/adaptive-forms/components/date-picker.md)
* [Liste déroulante](/help/adaptive-forms/components/drop-down.md)
* [Entrée d’e-mail](/help/adaptive-forms/components/email-input.md)
* [Conteneur de formulaires](/help/adaptive-forms/components/form-container.md)
* [Pièce jointe](/help/adaptive-forms/components/file-attachment.md)
* [Pied de page](/help/adaptive-forms/components/footer.md)
* [En-tête](/help/adaptive-forms/components/header.md)
* [Onglets horizontaux](/help/adaptive-forms/components/horizontal-tabs.md)
* [Image](/help/adaptive-forms/components/image.md)
* [Entrée de nombre](/help/adaptive-forms/components/number-input.md)
* [Conteneur de panneau](/help/adaptive-forms/components/panel-container.md)
* [Bouton radio](/help/adaptive-forms/components/radio-button.md)
* [Bouton de réinitialisation](/help/adaptive-forms/components/reset-button.md)
* [Bouton Envoyer](/help/adaptive-forms/components/submit-button.md)
* [Entrée téléphonique](/help/adaptive-forms/components/telephone-input.md)
* [Entrée de texte](/help/adaptive-forms/components/text-input.md)
* [Texte](/help/adaptive-forms/components/text.md)
* [Titre](/help/adaptive-forms/components/title.md)
* [Assistant](/help/adaptive-forms/components/wizard.md)

## Configuration des composants principaux


Les composants principaux des formulaires adaptatifs ont les exigences suivantes.

| AEM | Module complémentaire AEM Forms | Composants principaux |
|---|---|---|
| AEM as a Cloud Service | Forms – Inscription numérique | [Version 2.20.8](version.md)+ |
| AEM 6.5 | Module complémentaire Forms | [Version 1.1.12](version.md)+ |

### Création d’un formulaire adaptatif basé sur les composants principaux

**AEM Forms as a Cloud Service :** Lorsque vous créez un programme AEM Forms as a Cloud Service, les composants principaux du Forms adaptatif sont déjà activés pour votre environnement. Si vous disposez d’un environnement Forms as a Cloud Service basé sur Archetype 39 ou une version antérieure, vous devez [activer les composants principaux des formulaires adaptatifs pour votre environnement](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/setup-local-development-environment.html?#enable-adaptive-forms-core-components-for-an-existing-aem-archetype-based-project).

Lors de l’activation des composants principaux pour votre environnement, le modèle **Formulaires adaptatifs (composant principal)** et le thème de la zone de travail sont ajoutés à votre environnement. Si votre SDK AEM version antérieure à la version 2023.02.0, [assurez-vous que vous avez `prerelease` indicateur activé dans votre environnement](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=en#new-features) car les composants principaux de Forms adaptatif faisaient partie de la version préliminaire avant la version 2023.02.0.

Pour utiliser l’assistant de Forms adaptatif et l’éditeur de formulaires adaptatifs pour créer un formulaire adaptatif, voir Créer un formulaire adaptatif ([Composants principaux](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=fr?)).





<!-- >, such as  [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), to ensure that forms can be used by people with disabilities, including those using assistive technologies such as screen readers.

*   **Alignment with AEM Sites**: The Core Components are designed to be more aligned with AEM Sites, making it easier for Sites users to adopt and use them without having to learn anything new. The components use the same front-end pipeline as Sites, making it easier to style and modify their appearance. 

<!-- Additionally, the following points further illustrate this alignment:

    *   **Authoring experience inline with Page editor**: The Core Components have an authoring experience that is inline with the Sites editor, with dialogs and other experiences similar to the Page editor. This makes it easier for Sites users to create and manage forms within the familiar context of the Sites editor.

    *   **Inline form editing in Sites editor**: The Core Components allow  inline form editing within the Sites editor, avoiding the need to switch back and forth between editors. This streamlines the authoring experience and makes it easier to create and manage forms.

    *   **Inheriting Sites features in Forms**: Forms authored within a Sites page inherit the same features as Sites. This provides a seamless and integrated experience for creating and managing forms within the context of AEM Sites 
    
    <!--including Multi Site Manager, the ability to use Sites components within a form for static content, support for scheduled publish/unpublish, form translation aligned with Sites translation, versioning, and targeting -->
