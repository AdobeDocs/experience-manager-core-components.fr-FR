---
title: Extension de la couche de données du client Adobe
description: La couche de données du client d'Adobe peut être étendue selon certains modèles de base.
translation-type: tm+mt
source-git-commit: 896ed679ed3351cb309a34b38bf97fe81adc2cfe
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---


# Extension de la couche de données du client Adobe {#extending-acdl}

Vous pouvez étendre les composants principaux avec des options de boîte de dialogue personnalisées qui permettent aux auteurs de contenu de saisir des informations supplémentaires relatives à la couche de données.

Pour inclure ces champs dans la couche de données fournie par les composants principaux, vous devez étendre le modèle du composant qui implémente ses propres méthodes de couche de données spécifiques.

## Exemple : Composant de titre {#example}

Un composant principal comme le composant [](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) Titre étend le [composant](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) qui possède une `getData` méthode qui, par défaut, renvoie [`ComponentData`la valeur.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/datalayer/ComponentData.java)

`ComponentData` sérialise les champs prédéfinis que votre composant peut implémenter, comme `getDataLayerLinkUrl` et `getDataLayerTitle` pour le [`TitleImpl`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/internal/models/v1/TitleImpl.java)

Par conséquent, votre modèle Sling personnalisé peut comporter une `getData` méthode qui renvoie un objet qui s’étend `ComponentData` à renvoyer davantage de champs.

Cela permet d’ajouter un `data-cmp-data-layer` attribut à l’élément HTML de votre composant avec le JSON des données qui seront renseignées dans la couche de données. A ce stade, vous pouvez implémenter des scripts qui écoutent ces données ou les événements associés.
