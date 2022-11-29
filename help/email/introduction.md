---
title: Présentation des composants principaux du courrier électronique
description: Créez un contenu d’email attrayant à l’aide de la flexibilité des composants principaux d’email et diffusez-le avec la puissance d’Adobe Campaign.
role: Architect, Developer, Admin, User
exl-id: 0a411f28-bd6a-4bad-b473-6bc27c1d1055
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 10%

---


# Présentation des composants principaux du courrier électronique {#email-core-components-introduction}

Créez un contenu d’email attrayant à l’aide de la flexibilité des composants principaux d’email et diffusez-le avec la puissance d’Adobe Campaign.

## Présentation {#overview}

Les composants principaux d’email sont construits sur la même base puissante que les composants principaux. Ils permettent la création simple et flexible par glisser-déposer de contenu d&#39;email qui peut ensuite être diffusé à votre audience à l&#39;aide de la puissance d&#39;Adobe Campaign.

## Avantages {#benefits}

Les emails font partie de l’expérience de la marque et du parcours client. Grâce aux composants principaux de messagerie, vos auteurs peuvent concevoir du contenu d’email à partir d’AEM, offrant ainsi une expérience de marque cohérente et augmentant ainsi la vitesse du contenu.

* Tout comme pour la création de pages avec les composants principaux, les composants principaux d’email permettent aux auteurs d’assembler des emails sans connaissance technique tout en s’assurant qu’ils suivent les directives de marque.
* La possibilité de réutiliser des ressources et du contenu encourage également les auteurs à suivre les directives de valorisation de marque et à optimiser le processus de création de contenu.

## Fonctions {#features}

* Les composants de messagerie principaux sont basés sur la variable [Composants principaux,](/help/introduction.md) et donc aussi [Modèles modifiables](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=fr) et le [Système de style.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=fr)
* Il y a [dix composants prêts pour la production optimisés pour les emails](#components) pour créer du contenu d’email.
* Les composants principaux de l’e-mail fournissent une personnalisation avancée grâce à l’insertion de la fonction [Variables Adobe Campaign](campaign-variables.md) dans la plupart des champs de la boîte de dialogue.
* La flexibilité [Composant Segmentation](/help/email/components/segmentation.md) permet une segmentation avancée de votre contenu.
* Les composants principaux de messagerie offrent une sortie de HTML optimale pour les courriers électroniques grâce au [Styles CSS inliner,](https://github.com/adobe/aem-core-email-components/wiki/CSS-Styles-Inliner:-Technical-documentation) [l&#39;attribut HTML inliner,](https://github.com/adobe/aem-core-email-components/wiki/HTML-Inliner) et [l&#39;assainisseur de HTMLS.](https://github.com/adobe/aem-core-email-components/wiki/HTML-Sanitizing)
* Vous pouvez créer du contenu d’email n’importe où en dessous. `/content`.
* Les composants principaux du courrier électronique sont les suivants : [open source.](https://github.com/adobe/aem-core-email-components)

## Conditions requises {#requirements}

Les composants principaux d’email ont les exigences suivantes.

| AEM | Adobe Campaign  | Composants principaux |
|---|---|---|
| AEM 6.5.14.0+<br>On-premise ou AMS | Adobe Campaign Classic<br>Adobe Campaign Standard | [Version 2.21.2](/help/versions.md)+ |

>[!NOTE]
>
>Comme les intégrations Adobe Campaign ne sont pas prises en charge dans AEM as a Cloud Service, les composants principaux d’email ne sont pas non plus pris en charge dans AEM as a Cloud Service.

## Composants Email {#components}

La version actuelle des composants principaux du courrier électronique comprend les composants suivants.

* [État](components/page.md)
* [Conteneur](components/container.md)
* [Titre](components/title.md)
* [Texte](components/text.md)
* [Image](components/image.md)
* [Bouton](components/button.md)
* [Teaser](components/teaser.md)
* [Fragment d’expérience](components/experience-fragment.md)
* [Fragment de contenu](components/content-fragment.md)
* [Segmentation](components/segmentation.md)

## Installation et utilisation {#installation-usage}

Voir [Utilisation des composants principaux de messagerie](using.md) pour plus d’informations sur l’installation des composants principaux d’email.
