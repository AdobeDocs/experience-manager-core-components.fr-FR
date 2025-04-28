---
title: Présentation des composants principaux d’e-mail
description: Créez un contenu d’e-mail attrayant à l’aide de la flexibilité des composants principaux d’e-mail et diffusez-le avec la puissance d’Adobe Campaign.
role: Architect, Developer, Admin, User
exl-id: 0a411f28-bd6a-4bad-b473-6bc27c1d1055
source-git-commit: 91cf78d4c6622bbdec5ac7d22954c9c081c839d2
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 98%

---


# Présentation des composants principaux d’e-mail {#email-core-components-introduction}

Créez un contenu d’e-mail attrayant à l’aide de la flexibilité des composants principaux d’e-mail et diffusez-le avec la puissance d’Adobe Campaign.

## Présentation {#overview}

Les composants principaux d’e-mail sont construits sur la même base puissante que les composants principaux. Ils permettent la création simple et flexible par glisser-déposer de contenu d’e-mail qui peut ensuite être diffusé à votre audience à l’aide de la puissance d’Adobe Campaign.

## Avantages {#benefits}

Les e-mails font partie de l’expérience de la marque et du parcours client. Grâce aux composants principaux d’e-mail, vos créateurs peuvent concevoir du contenu d’e-mail à partir d’AEM, offrant ainsi une expérience de marque cohérente et augmentant par la suite la vitesse du contenu.

* Tout comme pour la création de pages avec les composants principaux, les composants principaux d’e-mail permettent aux auteurs d’assembler des e-mails sans connaissance technique tout en s’assurant qu’ils suivent les directives en matière d’image de marque.
* La possibilité de réutiliser des ressources et du contenu encourage également les créateurs à suivre les directives en matière d’image de marque et à optimiser le processus de création de contenu.

## Fonctions {#features}

* Les composants principaux d’e-mail sont basés sur les [composants principaux,](/help/introduction.md) et par conséquent, ils prennent en charge les [modèles modifiables](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=fr) et le [système de style.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=fr)
* Il y a [dix composants prêts pour la production optimisés pour les e-mails](#components) qui permettent de créer du contenu d’e-mail.
* Les composants principaux d’e-mail offrent une personnalisation avancée grâce à l’insertion de [variables Adobe Campaign](campaign-variables.md) dans la plupart des champs de la boîte de dialogue.
* Le [composant Segmentation](/help/email/components/segmentation.md) flexible permet une segmentation avancée de votre contenu.
* Les composants principaux d’e-mail offrent une sortie HTML optimale adaptée aux e-mails grâce à [CSS styles inliner,](https://github.com/adobe/aem-core-email-components/wiki/CSS-Styles-Inliner:-Technical-documentation) [HTML attribute inliner,](https://github.com/adobe/aem-core-email-components/wiki/HTML-Inliner) et [HTML sanitizer.](https://github.com/adobe/aem-core-email-components/wiki/HTML-Sanitizing)
* Vous pouvez créer du contenu d’e-mail n’importe où sous `/content`.
* Les composants principaux d’e-mail sont en [open source.](https://github.com/adobe/aem-core-email-components)

## Conditions requises {#requirements}

Les composants principaux d’e-mail ont les exigences suivantes.

| AEM | Adobe Campaign | Composants principaux |
|---|---|---|
| AEM 6.5.14.0+<br>On-premise ou AMS | Adobe Campaign Classic<br>Adobe Campaign Standard | [Version 2.21.2](/help/versions.md)+ |

>[!NOTE]
>
>Étant donné que les intégrations Adobe Campaign ne sont pas prises en charge dans AEM as a Cloud Service, les composants principaux d’e-mail ne sont pas non plus pris en charge dans AEM as a Cloud Service.

## Composants d’e-mail {#components}

La version actuelle des composants principaux d’e-mail comporte les composants suivants.

* [Page](components/page.md)
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

Consultez le document [Utilisation des composants principaux d’e-mail](using.md) pour plus d’informations sur l’installation des composants principaux d’e-mail.
