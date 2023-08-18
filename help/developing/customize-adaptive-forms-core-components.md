---
title: Personnalisation des composants principaux de Forms adaptatif
description: Découvrez comment étendre ou créer un composant principal Forms adaptatif pour mettre en oeuvre des fonctionnalités adaptées à votre entreprise.
role: Architect, Developer, Admin
source-git-commit: 9a80b453d6a6cf7b347128654d3b5e673a063505
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 4%

---


# Personnalisation des composants principaux de Forms adaptatif

La personnalisation des composants principaux de Forms adaptatif vous permet d’adapter les fonctionnalités prêtes à l’emploi à vos besoins. Ce guide vous guide tout au long du processus de personnalisation de ces composants pour créer une expérience plus personnalisée.

## Condition préalable

Avant de passer à la personnalisation des composants principaux de Forms adaptatif,

* En savoir plus sur les [Architecture d’un composant principal](customizing.md#customizing-the-markup-customizing-the-markup) et parcourez les [documentation officielle sur les composants principaux Adobe Experience Manager](customizing.md). Ces ressources complètes constituent votre guide tout au long du processus de personnalisation.
* Configurez votre environnement de développement. Cela garantit un processus fluide pour apporter des modifications aux composants principaux. Lors de la configuration de l’environnement de développement, utilisez un projet AEM Archetype basé sur le dernier projet AEM Archetype. En fonction de votre environnement, vous pouvez :

   * [Configuration d’un environnement de développement local pour Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/setup-local-development-environment.html).
   * [Configuration d’un environnement de développement local pour AEM 6.5 Forms](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html?lang=fr)

## Personnalisation d’un composant principal Forms adaptatif

Suivez les étapes ci-dessous pour modifier l’apparence, le comportement et les fonctionnalités d’un composant principal Forms adaptatif.

1. **Identification et duplication du composant principal**

   Lors de la configuration de l’environnement de développement, vous avez créé un projet basé sur l’archétype. Dans le projet d’archétype AEM, identifiez le composant principal spécifique que vous souhaitez personnaliser. Une fois identifié, créez un doublon du composant dans votre projet basé sur AEM Archetype. Conservez-le en parallèle à d’autres composants principaux de Forms adaptatif. Cette étape permet de s’assurer que vos efforts de personnalisation n’affectent pas le composant d’origine, ce qui vous permet d’effectuer librement des expériences.

1. **Personnalisation du composant copié**

   Ouvrez le composant dupliqué et commencez à apporter les modifications nécessaires en fonction de vos besoins :

   * **Personnalisation de la structure de HTML**: personnalisez la structure de HTML en fonction de vos besoins en matière de conception tout en adhérant aux [BEM (Block Element Modifier)](https://github.com/adobe/aem-core-wcm-components/wiki/css-coding-conventions) les pratiques de style pour le code gérable et évolutif.
   * **Mettre à jour le libellé**: mettez à jour le libellé du composant pour fournir un nom clair et descriptif pour la version personnalisée. Reportez-vous aux [Modèle de libellé prêt à l’emploi](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/label.html) pour assurer la cohérence.
   * **Personnalisation du widget**: ajustez le widget utilisé dans le composant (listes déroulantes, cases à cocher) pour l’aligner sur votre cas d’utilisation spécifique. Voir [exemple d’implémentation de widget](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/textinput.html) à titre de référence.
   * **Texte d’aide et info-bulles**: personnalisez le texte d’aide ou les info-bulles associés au composant pour offrir du contexte et des conseils aux utilisateurs. Utilisez la variable [Modèle de texte d’aide prêt à l’emploi](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/questionMark.html) comme point de départ.
   * **Attributs de données**: Incorporez tous les attributs de données nécessaires dans les éléments de HTML du composant. Ces attributs sont essentiels au bon fonctionnement du composant au moment de l’exécution. Consultez la [documentation](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput) pour comprendre le rôle des attributs de données dans les composants principaux de Forms adaptatif.

1. **Mise en oeuvre de la logique du serveur principal**

   Si votre personnalisation nécessite une logique d’arrière-plan, vous pouvez étendre les modèles Sling existants. Reportez-vous aux [example](https://github.com/adobe/aem-core-forms-components/blob/master/bundles/af-core/src/main/java/com/adobe/cq/forms/core/components/internal/models/v1/form/TextInputImpl.java) pour intégrer de manière transparente la fonctionnalité souhaitée à votre composant personnalisé.

1. **Configuration de la boîte de dialogue du composant**

   Configurez la boîte de dialogue associée à votre composant personnalisé. Utilisation de l’exemple [boîte de dialogue du composant](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/_cq_dialog/.content.xml) fourni dans la documentation pour garantir que les interactions et les paramètres utilisateur sont gérés de manière appropriée.

1. **Déployer et tester le composant dans votre environnement de développement local**

   Utilisation [Maven pour créer et déployer le composant](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html#building-and-installing) dans votre environnement de développement local. Une fois le composant déployé, créez un formulaire adaptatif pour le tester.

1. **Déployer le composant personnalisé dans votre environnement de production**

   Après avoir testé le composant sur votre environnement de développement local, déployez-le sur vos environnements de production.

