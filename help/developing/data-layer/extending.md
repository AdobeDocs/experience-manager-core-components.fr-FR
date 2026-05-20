---
title: Extension de la couche de données client Adobe
description: La couche de données client Adobe peut être étendue selon certains modèles de base.
feature: Core Components, Adobe Client Data Layer
role: Developer, Admin
exl-id: f3d5555b-4f08-49de-ab0f-dc0fb04aadf8
TQID: https://experienceleague.adobe.com/67YSpRfwNRMDgcBARHKLz51-Er6xb4vp1rXX0r0sbfE
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 289
ht-degree: 100%

---

# Extension de la couche de données client Adobe {#extending-acdl}

Vous pouvez étendre les composants principaux avec des options de boîte de dialogue personnalisées qui permettent aux auteurs de contenu de saisir des informations supplémentaires relatives à la couche de données.

Pour inclure ces champs dans la couche de données fournie par les composants principaux, vous devez étendre le modèle du composant qui implémente ses propres méthodes de couche de données spécifiques.

## Exemple : composant de titre {#example}

Un composant principal, comme le [composant Titre](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java), étend le [composant](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) qui possède une méthode `getData` qui, par défaut, renvoie [`ComponentData`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/datalayer/ComponentData.java)

`ComponentData` sérialise les champs prédéfinis que votre composant peut implémenter, comme `getDataLayerLinkUrl` et `getDataLayerTitle` pour le [`TitleImpl`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/internal/models/v1/TitleImpl.java)

Par conséquent, votre modèle Sling personnalisé peut comporter une méthode `getData` qui renvoie un objet qui étend `ComponentData` de façon à renvoyer davantage de champs.

Cela permet d’ajouter un attribut `data-cmp-data-layer` à l’élément HTML de votre composant avec le JSON des données qui seront renseignées dans la couche de données. À ce stade, vous pouvez implémenter des scripts qui écoutent ces données ou les événements associés.

>[!TIP]
>
>Pour continuer à découvrir toute la flexibilité de la couche de données, passez en revue les options d’intégration, y compris celles concernant la façon d’activer la couche de données pour vos composants personnalisés.
