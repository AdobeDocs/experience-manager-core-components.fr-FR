---
title: Versions des composants principaux d’AEM Forms
description: Les composants principaux d’AEM sont publiés sous forme de versions qui peuvent contenir plusieurs versions des mêmes composants principaux. Ce document explique les versions et les mises à jour ainsi que comment comprendre la compatibilité avec les composants principaux et AEM.
role: Architect, Developer, Admin, User
exl-id: 8146a5b1-acf6-4b54-ad6b-6e1747a137f6
source-git-commit: a567b5ad937d426abe16c34e039e19cd0b1af5b0
workflow-type: ht
source-wordcount: '821'
ht-degree: 100%

---

# Versions des composants principaux {#core-components-versions}

La version la plus récente des composants principaux 2.0.10 est compatible avec [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=fr). La version 1.1.12 des composants principaux est compatible avec les installations d’[AEM 6.5 Forms On-Premise et AMS](https://experienceleague.adobe.com/docs/experience-manager-65/user-guide/home.html?lang=fr).

## Historique des versions d’AEM as a Cloud Service {#aem-as-cs-version-history}

Le tableau suivant dresse la liste des versions des composants principaux compatibles avec AEM as a Cloud Service disponibles sur [GitHub avec toutes les informations de version](https://github.com/adobe/aem-core-forms-components/releases).

| Mise à jour | Description | AEM as a Cloud Service | Java™ | Date de publication |
|---|---|---|---|---|
| [2.0.74](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.74) | Avec cette version, l’erreur de soumission est mise à jour pour l’action Soumettre dans AEM Forms. | En continu | 8, 11 | 15 novembre 2023 |
| [2.0.70](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.70) | Cette version a ajouté la prise en charge de la langue des pages de sites dans le conteneur de formulaires. | En continu | 8, 11 | 10 novembre 2023 |
| [2.0.64](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.64) | Prise en charge du texte enrichi pour les libellés des composants de case à cocher/boutons radio. Cette version comprend également des correctifs pour le composant Conditions générales. | En continu | 8, 11 | 6 novembre 2023 |
| [2.0.62](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.62) | Avec cette version, la prise en charge du composant Conditions générales est ajoutée. Ajout également de la prise en charge du nom qualifié dans les composants principaux. | En continu | 8, 11 | 16 octobre 2023 |
| [2.0.60](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.60) | Cette version comprend des correctifs relatifs aux fonctionnalités de propriétés personnalisées, ainsi qu’aux composants Assistant et Sélecteur de date. | En continu | 8, 11 | 12 septembre 2023 |
| [2.0.56](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.56) | Avec cette version, la prise en charge des propriétés personnalisées pour tous les composants principaux est ajoutée. | En continu | 8, 11 | 12 septembre 2023 |
| [2.0.54](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.54) | Cette version a corrigé le problème lié à la localisation avec le composant Sélecteur de date. | En continu | 8, 11 | 30 août 2023 |
| [2.0.52](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.52) | Prise en charge de l’utilisation du composant de case à cocher dans un formulaire adaptatif. | En continu | 8, 11 | 25 août 2023 |
| [2.0.50](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.50) | Ajout de la prise en charge des fragments de formulaire dans un formulaire adaptatif avec cette version. | En continu | 8, 11 | 4 août 2023 |
| [2.0.48](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.48) | Les principales améliorations apportées à cette version concernent les performances de Lighthouse. | En continu | 8, 11 | 25 juillet 2023 |
| [2.0.42](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.42) | La version intègre des améliorations au niveau de la programmation. | En continu | 8, 11 | 18 juillet 2023 |
| [2.0.38](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.38) | La fonctionnalité d’accessibilité a été améliorée avec cette version. | En continu | 8, 11 | 17 juillet 2023 |
| [2.0.36](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.36) | Avec cette version, vous pouvez utiliser le gestionnaire d’erreurs personnalisé à l’aide du service Invoke de l’éditeur de règles. | En continu | 8, 11 | 3 juillet 2023 |
| [2.0.34](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.34) | Ajout de la prise en charge de la localisation des messages d’erreur par défaut, ainsi que du bouton Ajouter/Supprimer pour le composant Répétable. | En continu | 8, 11 | 28 juin 2023 |
| [2.0.32](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.32) | Avec cette version, la prise en charge de Captcha est ajoutée pour les formulaires adaptatifs. | En continu | 8, 11 | 15 juin 2023 |
| [2.0.26](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.26) | Prise en charge de l’ajout de formulaires adaptatifs sur AEM Sites. | En continu | 8, 11 | 7 juin 2023 |
| [2.0.18](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.18) | Avec cette version, la prise en charge d’une répétition pour le composant Accordéon a été ajoutée. Un nouveau composant sous la forme d’onglets verticaux a également été ajouté. | En continu | 8, 11 | 5 juin 2023 |
| [2.0.10](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.10) | Cette version offre la prise en charge du composant Conteneur des formulaires adaptatifs dans l’éditeur de Sites. | En continu | 8, 11 | 17 mars 2023 |
| [2.0.8](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.8) | Cette version ajoute la fonction de répétition au composant Assistant. | En continu | 8, 11 | 3 mars 2023 |
| [2.0.6](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.6) | Cette version introduit plusieurs formats pour le composant principal Saisie numérique. | En continu | 8, 11 | 8 février 2023 |
| [2.0.4](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.6) | Cette version offre la prise en charge des composants principaux dans AEM as a Cloud Service. | En continu | 8, 11 | 30 janvier 2023 |

## Historique des versions d’AEM 6.5 Forms {#aem-as-form-version-history}

Le tableau suivant dresse la liste des versions des composants principaux compatibles avec AEM 6.5 Forms On-Premise et AMS disponibles sur [GitHub avec toutes les informations de version](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.12).

| Mise à jour | Description | AEM 6.4 | AEM 6.5 | Java™ | Date de publication |
|---|---|---|---|---|---|
| [1.1.32](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.32) | Cette version a mis à jour les informations relatives aux packages du Pack de services AEM 6.5.18.0. | - | 6.5.16.0 et version ultérieure | 8, 11 | 15 octobre 2023 |
| [1.1.28](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.28) | Prise en charge du texte enrichi pour les libellés des composants de case à cocher/boutons radio. Cette version comprend également la prise en charge du composant Conditions générales. | - | 6.5.16.0 et version ultérieure | 8, 11 | 15 octobre 2023 |
| [1.1.26](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.26) | Avec cette version, la prise en charge du composant de case à cocher pour le formulaire adaptatif a été ajoutée. Elle comprend également des améliorations des performances de Lighthouse. Le gestionnaire d’erreurs personnalisé à l’aide du service Invoke de l’éditeur de règles est également inclus dans cette version. | - | 6.5.16.0 et version ultérieure | 8, 11 | 15 octobre 2023 |
| [1.1.24](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.24) | Ajout de la prise en charge de la localisation des messages d’erreur par défaut, ainsi que du bouton Ajouter/Supprimer pour le composant Répétable. Ajout également de la prise en charge du reCAPTCHA dans les formulaires adaptatifs. | - | 6.5.16.0 et version ultérieure | 8, 11 | 29 juin 2023 |
| [1.1.22](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.22) | Prise en charge de l’ajout de formulaires adaptatifs sur AEM Sites. Ajout de l’onglet Éléments dans la boîte de dialogue de modification des composants Assistant et Onglets verticaux. | - | 6.5.16.0 et version ultérieure | 8, 11 | 07 juin 2023 |
| [1.1.12](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.12) | La prise en charge des composants principaux pour AEM Forms On-Premise et AMS est introduite dans cette version. | - | 6.5.16.0 et version ultérieure | 8, 11 | 8 février 2023 |

## Voir également {#see-also}

{{see-also}}