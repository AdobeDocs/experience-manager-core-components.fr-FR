---
title: Activation et utilisation de modèles de validation d’entrée de texte dans les formulaires adaptatifs Adobe Experience Manager
description: Découvrez comment configurer des politiques pour les modèles afin d’afficher des modèles de validation tels que des numéros de téléphone, des numéros de sécurité sociale et des codes postaux, puis les utiliser dans vos formulaires adaptatifs.
hide: true
exl-id: e4500666-1346-4558-861d-da9541dcef51
source-git-commit: 59064c359aea14af99675709bbddf9a933a959df
workflow-type: ht
source-wordcount: '861'
ht-degree: 100%

---

# Activation et utilisation de modèles de validation d’entrée de texte dans les formulaires adaptatifs Adobe Experience Manager

## Vue d’ensemble

Dans Adobe Experience Manager (Adobe Experience Manager) Forms, les formats de validation spécifiques (tels que les numéros de sécurité sociale, les adresses e-mail ou les codes postaux) pour les composants Entrée de texte sont contrôlés au niveau de la politique du modèle.Ce guide décrit les actions suivantes :

1. Accéder à l’éditeur de modèles et configurer la politique du composant Entrée de texte pour afficher les modèles de validation
2. Créer un formulaire adaptatif et appliquer ces modèles de validation à un composant Entrée de texte

## Prérequis

- Disposer d’un accès à une instance Adobe Experience Manager avec Forms activé.
- Disposer des autorisations de modification des modèles (qui font généralement partie du groupe `template-authors`).
- Disposer des autorisations pour créer et modifier des formulaires adaptatifs.

## Partie 1 : activer les modèles de validation dans le modèle

>[!VIDEO](https://video.tv.adobe.com/v/3480390/)

### Étape 1 : accéder à la console Modèles

1. Sur l’écran d’accueil d’Adobe Experience Manager, cliquez sur **Outils** (icône de marteau) dans la barre latérale gauche.
2. Accédez à **Général > Modèles**.
3. Sélectionnez le dossier contenant les modèles de votre projet (Exemples de composants principaux, par exemple).
4. Recherchez le modèle spécifique que vous souhaitez modifier (par exemple, FA vide) et sélectionnez-le.
5. Cliquez sur **Modifier** (ou ouvrez directement le modèle).

### Étape 2 : accéder à la structure du composant

1. Assurez-vous que vous êtes dans la vue **Structure** (sélectionnez « Structure » dans la liste déroulante Mode en haut à droite, si nécessaire).
2. Recherchez le **Conteneur de disposition** principal ou le conteneur spécifique pour lequel votre composant Entrée de texte est autorisé.
3. Cliquez sur le conteneur pour afficher la liste des composants autorisés.
4. Recherchez le composant **Zone de texte du formulaire adaptatif** dans la liste.
5. Cliquez sur l’icône **Politique** (représentée par un symbole de fichier/tiroir) en regard du nom du composant.

### Étape 3 : configurer la politique du composant Entrée de texte

1. Dans l’éditeur de politique, sur le côté droit de la fenêtre, cliquez sur l’onglet **Formats**.
2. Une liste des modèles de validation disponibles s’affiche. Cochez les cases correspondant aux formats que vous souhaitez activer :
   - Numéro de téléphone
   - Numéro de sécurité sociale
   - E-mail alphanumérique
   - Code postal

### Étape 4 : définir et enregistrer la politique

1. Revenez à l’onglet **Politique** (ou vérifiez les paramètres à gauche).
2. Dans le champ **Titre de la politique**, saisissez un nom explicite (par exemple, `new-textinput-default-policy`).
3. Dans le coin supérieur droit, cliquez sur **Terminé** (icône de coche) pour enregistrer les modifications.

## Partie 2 : créer un formulaire et utiliser des modèles de validation

Maintenant que les modèles de validation sont activés dans le modèle, vous pouvez créer un formulaire adaptatif et les appliquer aux composants Entrée de texte.

>[!VIDEO](https://video.tv.adobe.com/v/3480391/)

### Étape 1 : créer un formulaire adaptatif

1. Accédez à l’interface **Formulaires et documents**.
2. Sélectionnez **Créer** dans le coin supérieur droit.
3. Sélectionnez **Formulaire adaptatif** dans les options de liste déroulante.
4. Choisissez le modèle dans lequel vous avez activé les modèles de validation (par exemple, **Vide**) et cliquez sur **Suivant**.
5. Sur l’écran Ajouter des propriétés :
   - Indiquez un **Titre** pour votre formulaire (Politique_test, par exemple)Le champ **Nom** est automatiquement renseigné en fonction du champ Titre.
   - Assurez-vous que la **bibliothèque cliente de thème** appropriée est sélectionnée (par exemple, `adaptiveform.theme.canvas3`).
6. Cliquez sur **Créer**. Un message de réussite s’affiche.
7. Cliquez sur **Modifier** pour ouvrir le formulaire dans l’éditeur.

### Étape 2 : ajouter un composant Entrée de texte

1. Dans l’éditeur de formulaire, recherchez le navigateur **Composants** dans la barre latérale gauche.
2. Utilisez la barre de recherche pour rechercher le composant **Zone de texte de formulaire adaptatif**.La saisie du terme « texte » permet de filtrer la liste.
3. Cliquez sur le composant **Zone de texte de formulaire adaptatif** et faites-le glisser sur la zone de travail principale.

### Étape 3 : configurer la mise en forme des composants

1. Cliquez sur le composant **Entrée de texte** nouvellement ajouté pour le sélectionner.
2. Cliquez sur l’icône **Configurer** (représentée par une clé à molette) dans la barre d’outils qui s’affiche au-dessus du composant.
3. Dans la boîte de dialogue des propriétés, accédez à l’onglet **Formats**.
4. Recherchez le menu déroulant **Type** et sélectionnez **Numéro de téléphone** (ou un autre format activé).

### Étape 4 : configurer la validation des données

1. Toujours dans la boîte de dialogue de configuration du composant, accédez à l’onglet **Validation**.
2. Recherchez la section **Modèle de validation**.
3. Cliquez sur le menu déroulant **Type**.
4. Sélectionnez **Numéro de téléphone** dans la liste des modèles de validation.Cela garantit que le formulaire génère une erreur si l’utilisateur ou l’utilisatrice saisit du texte qui ne correspond pas à un format de numéro de téléphone valide.
5. Dans le coin supérieur droit de la boîte de dialogue, cliquez sur **Terminé** (icône de coche) pour enregistrer les modifications.

## Vérification

Pour vérifier que les modèles de validation fonctionnent correctement :

1. Prévisualisez le formulaire dans l’éditeur.
2. Saisissez les données de test dans le composant **Entrée de texte**.
3. Vérifiez les éléments suivants :
   - Les modèles de validation activés apparaissent dans les onglets Formats et Validation du composant.
   - Une entrée non valide déclenche les messages d’erreur appropriés.
   - Une entrée valide est acceptée sans erreur.

## Résolution des problèmes

- **Problème :** les modèles de validation n’apparaissent pas dans le composant de formulaire.
   - **Solution :** assurez-vous que la politique du modèle a été enregistrée correctement et que vous utilisez le modèle correct lors de la création du formulaire.

- **Problème :** impossible d’accéder à l’éditeur de modèle.
   - **Solution :** vérifiez que vous disposez des autorisations nécessaires pour modifier les modèles (appartenance au groupe `template-authors`).

- **Problème :** le composant Entrée de texte ne valide pas correctement la saisie.
   - **Solution :** Vérifiez à nouveau les paramètres du modèle de validation dans l’onglet Validation du composant et assurez-vous que le modèle correct est sélectionné.

## Étapes suivantes

Après avoir activé et utilisé des modèles de validation de saisie de texte dans votre formulaire adaptatif Adobe Experience Manager :

- Configurez des modèles de validation supplémentaires pour d’autres types de données.
- Explorez d’autres politiques de composant pour personnaliser le comportement du formulaire.
- Configurez la logique de gestion et de traitement des données pour l’envoi de formulaires.
