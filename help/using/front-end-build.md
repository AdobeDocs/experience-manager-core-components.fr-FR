---
title: Version frontale de l’archétype de projet AEM
seo-title: Version frontale de l’archétype de projet AEM
description: Modèle de projet pour les applications AEM
seo-description: Modèle de projet pour les applications AEM
contentOwner: bohnert
content-type: référence
topic-tags: core-components
translation-type: tm+mt
source-git-commit: 0a61f4e6d1ad8b4d5e3778018838dc70d496e1fc

---


# Version frontale de l’archétype de projet AEM {#aem-project-archetype-front-end-build}

L’archétype de projet AEM comprend un mécanisme de génération frontale dédié facultatif basé sur Webpack avec les fonctionnalités suivantes.

* Prise en charge complète de TypeScript, ES6 et ES5 (avec wrappers Webpack applicables)
* Linting TypeScript et JavaScript à l’aide d’un ensemble de règles TSLint
* sortie ES5 pour la prise en charge des navigateurs hérités
* Expansion de nom de fichier
   * Pas besoin d'ajouter des importations
   * Tous les fichiers JS et CSS peuvent désormais être ajoutés à chaque composant.
      * Les meilleures pratiques sont sous `/clientlib/js`, `/clientlib/css`ou `/clientlib/scss`
   * Aucun fichier `.content.xml` ou `js.txt`/`css.txt` requis car tout est exécuté via Webpack
   * L’application globale extrait tous les fichiers JS sous le `/component/` dossier.
      * Webpack permet aux fichiers CSS/SCSS d’être liés via des fichiers JS.
      * Ils sont attirés par les deux points d'entrée `sites.js` et `vendors.js`.
   * Le seul fichier consommé par AEM est les fichiers de sortie `site.js` et `site.css` dans `/clientlib-site` , `dependencies.js` ainsi que dans et `dependencies.css` dans `/clientlib-dependencies`
* Chunks
   * Principal (js/css du site)
   * Fournisseurs (dépendances js/css)
* Prise en charge complète de Sass/Scss (Sass est compilé en CSS via Webpack).

## Installation {#installation}

1. Installez [NodeJS](https://nodejs.org/en/download/) (v10+), globalement. Cela installera également npm.
1. Accédez à ui.frontend dans votre projet et exécutez `npm install`.

## Utilisation {#usage}

Les scripts npm suivants pilotent le flux de travaux frontal :

* `npm run dev` - compilation complète avec l'optimisation JS désactivée (tremblement de l'arbre, etc.) et les cartes source activées et l'optimisation CSS désactivée.
* `npm run prod` - compilation complète avec l'optimisation JS activée (tremblement de l'arbre, etc.), les cartes source désactivées et l'optimisation CSS activée.

## Sortie {#output}

### Général {#general}

* Site : `site.js` et `site.css` sont créés dans un dossier clientlib-site.
* Dépendances : `dependencies.js` et `dependencies.css` sont créées dans un dossier clientlib-dependences.

### JavaScript {#javascript}

* Optimisation : pour les versions de production, tous les JS qui ne sont pas utilisés ou appelés sont supprimés.

### CSS {#css}

* Fixation automatique : toutes les feuilles de style CSS sont exécutées via un préfixeur et toutes les propriétés nécessitant un préfixe seront automatiquement ajoutées dans la feuille de style CSS.
* Optimisation - Dans la publication, toutes les feuilles CSS sont exécutées via un optimiseur (cssnano) qui les normalise selon les règles par défaut suivantes :
   * Réduit autant que possible l’expression CSS calc, assurant ainsi à la fois la compatibilité du navigateur et la compression. Convertit entre des valeurs équivalentes de longueur, de temps et d’angle. Notez que, par défaut, les valeurs de longueur ne sont pas converties.
   * Supprime les commentaires dans les règles, les sélecteurs et les déclarations et les alentours
   * Supprime les règles, règles et déclarations dupliquées
      * Notez que cela ne fonctionne que pour les doublons exacts.
   * Supprime les règles vides, les requêtes multimédias et les règles avec des sélecteurs vides, car elles n’affectent pas la sortie
   * Fusionne les règles adjacentes par des sélecteurs et des paires propriété/valeur qui se chevauchent
   * Garantit qu’un seul @charset est présent dans le fichier CSS et le déplace en haut du document
   * Remplace le mot-clé initial CSS par la valeur réelle, lorsque la sortie obtenue est plus petite.
   * Compresse les définitions SVG intégrées avec SVGO
* Nettoyage : comprend une tâche explicite de nettoyage pour effacer à la demande les fichiers CSS, JS et Map générés.
* Mappage de source - création de développement uniquement

>[!NOTE]
>L’option de génération frontale utilise des fichiers de configuration webpack uniquement destinés au développement et au développement qui partagent un fichier de configuration commun. Ainsi, les paramètres de développement et de production peuvent être modifiés indépendamment.
