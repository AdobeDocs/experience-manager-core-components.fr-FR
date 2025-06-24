---
title: Personnaliser les composants principaux des formulaires adaptatifs
description: Découvrez comment étendre ou créer un composant principal de formulaire adaptatif pour mettre en œuvre des fonctionnalités adaptées à votre organisation.
role: Architect, Developer, Admin
exl-id: f3ab12aa-d48d-47e9-a965-15052cac6f18
source-git-commit: 5994133947ff697f7c866fe61598c58e37e77008
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Personnaliser les composants principaux des formulaires adaptatifs

La personnalisation des composants principaux de formulaires adaptatifs vous permet d’adapter les fonctionnalités prêtes à l’emploi à vos besoins. Ce guide vous dirige tout au long du processus de personnalisation de ces composants pour créer une expérience plus personnalisée.

{{traditional-aem}}

## Condition préalable

Avant de passer à la personnalisation des composants principaux des formulaires adaptatifs,

* découvrez l’[architecture d’un composant principal](customizing.md#customizing-the-markup-customizing-the-markup) et parcourez la [documentation officielle sur les composants principaux d’Adobe Experience Manager](customizing.md). Ces ressources complètes constituent votre guide tout au long du processus de personnalisation.
* Configurez votre environnement de développement. Cela garantit un workflow fluide pour apporter des modifications aux composants principaux. Lors de la configuration de l’environnement de développement, utilisez le dernier projet d’archétype AEM. En fonction de votre environnement, vous pouvez :

   * [Configurer un environnement de développement local pour Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/setup-local-development-environment.html?lang=fr).
   * [Configurer un environnement de développement local pour AEM 6.5 Forms](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html?lang=fr).

## Personnaliser un composant principal de formulaire adaptatif

Suivez les étapes ci-dessous pour modifier l’apparence, le comportement et les fonctionnalités d’un composant principal de formulaire adaptatif.

1. **Identifier et dupliquer le composant principal**

   Lors de la configuration de l’environnement de développement, vous avez créé un projet basé sur l’archétype. Dans le projet d’archétype AEM, identifiez le composant principal spécifique que vous souhaitez personnaliser. Une fois identifié, créez un duplicata du composant dans votre projet basé sur l’archétype AEM. Conservez-le en parallèle à d’autres composants principaux de formulaire adaptatif. Cette étape permet de s’assurer que vos efforts de personnalisation n’affectent pas le composant original, ce qui vous donne plus de liberté dans vos expériences.

1. **Personnaliser le composant copié**

   Ouvrez le composant dupliqué et commencez à apporter les modifications nécessaires en fonction de vos besoins :

   * **Personnaliser la structure de HTML** : personnalisez la structure de HTML en fonction de vos besoins en matière de conception tout en respectant les bonnes pratiques en matière de style des [BEM (Block Element Modifier)](https://github.com/adobe/aem-core-wcm-components/wiki/css-coding-conventions) pour un code gérable et évolutif.
   * **Mettre à jour le libellé** : mettez à jour le libellé du composant pour fournir un nom clair et descriptif à la version personnalisée. Reportez-vous aux [modèle de libellé prêt à l’emploi](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/label.html) pour assurer la cohérence.
   * **Personnaliser le widget** : ajustez le widget utilisé dans le composant (listes déroulantes, cases à cocher) pour l’aligner sur votre cas d’utilisation spécifique. Consultez l’[exemple d’implémentation de widget](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/textinput.html) à titre de référence.
   * **Texte d’aide et info-bulles** : personnalisez le texte d’aide ou les info-bulles associés au composant pour offrir du contexte et des conseils aux utilisateurs et utilisatrices. Utilisez le [modèle de texte d’aide prêt à l’emploi](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/questionMark.html) comme point de départ.
   * **Attributs de données** : incorporez tous les attributs de données nécessaires dans les éléments de HTML du composant. Ces attributs sont essentiels au bon fonctionnement du composant au moment de l’exécution. Consultez la [documentation](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput) pour comprendre le rôle des attributs de données dans les composants principaux de formulaire adaptatif.

1. **Implémenter la logique back-end**

   Si votre personnalisation nécessite une logique back-end, vous pouvez étendre les modèles Sling existants. Reportez-vous à l’[exemple](https://github.com/adobe/aem-core-forms-components/blob/master/bundles/af-core/src/main/java/com/adobe/cq/forms/core/components/internal/models/v1/form/TextInputImpl.java) fourni pour intégrer de manière transparente la fonctionnalité souhaitée à votre composant personnalisé.

1. **Configurer la boîte de dialogue du composant**

   Configurez la boîte de dialogue associée à votre composant personnalisé. Utilisez l’exemple de [boîte de dialogue du composant](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/_cq_dialog/.content.xml) fourni dans la documentation pour garantir que les interactions et les paramètres d’utilisation sont gérés de manière appropriée.

1. **Déployer et tester le composant dans votre environnement de développement local**

   Utilisez [Maven pour créer et déployer le composant](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html?lang=fr#building-and-installing) dans votre environnement de développement local. Une fois le composant déployé, créez un formulaire adaptatif pour tester le composant personnalisé.

1. **Déployer le composant personnalisé dans votre environnement de production**

   Après avoir testé le composant dans votre environnement de développement local, déployez-le dans vos environnements de production.
