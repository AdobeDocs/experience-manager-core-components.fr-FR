---
title: Activation et utilisation de modèles de validation d’entrée de texte dans Adobe Experience Manager Adaptive Forms
description: Découvrez comment configurer des stratégies de modèle pour afficher des modèles de validation tels que des numéros de téléphone, des numéros de sécurité sociale et des codes postaux, puis les utiliser dans votre Forms adaptative.
hide: true
hidefromtoc: true
source-git-commit: 1ac3d987337f8279e762ab5357d32bb732dea0be
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 1%

---


# Activation et utilisation de modèles de validation d’entrée de texte dans Adobe Experience Manager Adaptive Forms

## Vue d’ensemble

Dans Adobe Experience Manager (Adobe Experience Manager) Forms, les formats de validation spécifiques (tels que les numéros de sécurité sociale, les adresses e-mail ou les codes postaux) pour les composants Entrée de texte sont contrôlés au niveau de la stratégie du modèle. Ce guide explique comment :

1. Accédez à l’éditeur de modèles et configurez la stratégie du composant Entrée de texte pour afficher les modèles de validation.
2. Créez un formulaire adaptatif et appliquez ces modèles de validation à un composant Entrée de texte.

## Prérequis

- Accès à une instance Adobe Experience Manager avec Forms activé.
- Les autorisations de modification des modèles (qui font généralement partie du groupe `template-authors`).
- Autorisations de création et de modification de Forms adaptatif.

## Partie 1 : activer les modèles de validation dans le modèle

>[!VIDEO](https://video.tv.adobe.com/v/3480390/)

### Étape 1 : accéder à la console Modèles

1. Sur l’écran d’accueil de Adobe Experience Manager, cliquez sur **Outils** (icône de marteau) dans la barre latérale gauche.
2. Accédez à **Général > Modèles**.
3. Sélectionnez le dossier contenant les modèles de votre projet (par exemple, Exemples de composants principaux).
4. Recherchez le modèle spécifique que vous souhaitez modifier (par exemple, AF Blank) et sélectionnez-le.
5. Cliquez sur **Modifier** (ou ouvrez directement le modèle).

### Étape 2 : accéder à la structure du composant

1. Assurez-vous que vous êtes dans la vue **Structure** (sélectionnez « Structure » dans la liste déroulante Mode en haut à droite, si nécessaire).
2. Recherchez le **Conteneur de disposition** principal ou le conteneur spécifique dans lequel votre composant Entrée de texte est autorisé.
3. Cliquez sur le conteneur pour afficher la liste des composants autorisés.
4. Recherchez le composant **Zone de texte de formulaire adaptatif** dans la liste.
5. Cliquez sur l’icône **Stratégie** (représentée par un symbole de fichier/tiroir) en regard du nom du composant.

### Étape 3 : configurer la stratégie du composant d’entrée de texte

1. Dans l’éditeur de politiques, cliquez sur l’onglet **Formats** sur le côté droit de la fenêtre.
2. Une liste des modèles de validation disponibles s’affiche. Cochez les cases correspondant aux formats que vous souhaitez activer :
   - Numéro de téléphone
   - Numéro de sécurité sociale
   - E-mail alphanumérique
   - Code postal

### Étape 4 : définir et enregistrer la politique

1. Revenez à l’onglet **Politique** (ou vérifiez les paramètres à gauche).
2. Dans le champ **Titre de la politique**, saisissez un nom clair (par exemple, `new-textinput-default-policy`).
3. Cliquez sur l’icône **Terminé** (coche) dans le coin supérieur droit pour enregistrer vos modifications.

## Partie 2 : créer un formulaire et utiliser des modèles de validation

Maintenant que les modèles de validation sont activés dans le modèle, vous pouvez créer un formulaire adaptatif et les appliquer aux composants Entrée de texte.

>[!VIDEO](https://video.tv.adobe.com/v/3480391/)

### Étape 1 : créer un formulaire adaptatif

1. Accédez à l’interface **Forms et documents**.
2. Cliquez sur le bouton **Créer** dans le coin supérieur droit.
3. Sélectionnez **Formulaire adaptatif** dans les options de liste déroulante.
4. Choisissez le modèle dans lequel vous avez activé les modèles de validation (par exemple, **Vide**) et cliquez sur **Suivant**.
5. Sur l’écran Ajouter des propriétés :
   - Saisissez un **Titre** pour votre formulaire (par exemple, « testPolicy »). Le champ **Nom** est automatiquement renseigné en fonction du titre.
   - Assurez-vous que la **bibliothèque cliente de thème** appropriée est sélectionnée (par exemple, `adaptiveform.theme.canvas3`).
6. Cliquez sur **Créer**. Un message de réussite s’affiche.
7. Cliquez sur **Modifier** pour ouvrir le formulaire dans l’éditeur.

### Étape 2 : ajouter un composant Entrée de texte

1. Dans l’éditeur de formulaire, recherchez le navigateur **Composants** dans la barre latérale gauche.
2. Utilisez la barre de recherche pour rechercher le composant **Zone de texte de formulaire adaptatif**. La saisie de « texte » filtre la liste.
3. Cliquez sur le composant **Zone de texte de formulaire adaptatif** et faites-le glisser sur la zone de travail principale.

### Étape 3 : Configurer le formatage des composants

1. Cliquez sur le composant **Entrée de texte** nouvellement ajouté pour le sélectionner.
2. Cliquez sur l’icône **Configurer** (représentée par une clé à molette) dans la barre d’outils qui s’affiche au-dessus du composant.
3. Dans la boîte de dialogue des propriétés, accédez à l’onglet **Formats**.
4. Recherchez le menu déroulant **Type** et sélectionnez **Numéro de téléphone** (ou un autre format activé).

### Étape 4 : Configurer La Validation Des Données

1. Toujours dans la boîte de dialogue de configuration du composant, accédez à l’onglet **Validation**.
2. Recherchez la section **Modèle de validation**.
3. Cliquez sur le menu déroulant **Type**.
4. Sélectionnez **Numéro de téléphone** dans la liste des modèles de validation. Cela garantit que le formulaire génère une erreur si l’utilisateur ou l’utilisatrice saisit du texte qui ne correspond pas à un format de numéro de téléphone valide.
5. Cliquez sur l’icône **Terminé** (coche) en haut à droite de la boîte de dialogue pour enregistrer vos modifications.

## Vérification

Pour vérifier que les modèles de validation fonctionnent correctement :

1. Prévisualisez le formulaire dans l’éditeur.
2. Saisissez les données de test dans le composant **Entrée de texte**.
3. Confirmez que :
   - Les modèles de validation activés apparaissent dans les onglets Formats et Validation du composant.
   - Une entrée non valide déclenche les messages d’erreur appropriés.
   - Une entrée valide est acceptée sans erreur.

## Résolution des problèmes

- **Problème :** les modèles de validation n’apparaissent pas dans le composant de formulaire.
   - **Solution :** assurez-vous que la stratégie du modèle a été enregistrée correctement et que vous utilisez le modèle correct lors de la création du formulaire.

- **Problème :** impossible d’accéder à l’éditeur de modèles.
   - **Solution :** vérifiez que vous disposez des autorisations nécessaires pour modifier les modèles (appartenance au groupe `template-authors`).

- **Problème :** le composant Entrée de texte ne valide pas correctement la saisie.
   - **Solution :** Vérifiez à nouveau les paramètres du modèle de validation dans l’onglet Validation du composant et assurez-vous que le modèle correct est sélectionné.

## Étapes suivantes

Après avoir activé et utilisé des modèles de validation de saisie de texte dans votre Forms adaptatif Adobe Experience Manager :

- Configurez des modèles de validation supplémentaires pour d’autres types de données.
- Explorez d’autres politiques de composant pour personnaliser le comportement du formulaire.
- Configurez la logique de gestion et de traitement des données pour l’envoi de formulaires.
