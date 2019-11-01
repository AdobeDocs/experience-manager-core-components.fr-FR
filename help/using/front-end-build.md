---
title: Version front-end de l’archétype de projet AEM
seo-title: Version front-end de l’archétype de projet AEM
description: Modèle de projet pour les applications basées sur AEM
seo-description: Modèle de projet pour les applications basées sur AEM
contentOwner: bohnert
content-type: référence
topic-tags: core-components
translation-type: ht
source-git-commit: 0a61f4e6d1ad8b4d5e3778018838dc70d496e1fc

---


# Version front-end de l’archétype de projet AEM {#aem-project-archetype-front-end-build}

L’archétype de projet AEM comprend un mécanisme de génération front-end dédié facultatif basé sur Webpack avec les fonctionnalités suivantes.

* Prise en charge complète de TypeScript, ES6 et ES5 (avec enveloppes Webpack applicables)
* TypeScript et JavaScript linting avec un jeu de règles TSLint
* Sortie ES5 pour la prise en charge des navigateurs hérités
* Extension métacaractère
   * Inutile d'ajouter des importations
   * Tous les fichiers JS et CSS peuvent désormais être ajoutés à chaque composant
      * Les meilleures pratiques figurent sous `/clientlib/js`, `/clientlib/css` ou `/clientlib/scss`.
   * Aucun fichier `.content.xml` ou `js.txt`/`css.txt` requis car tous les éléments sont exécutés via Webpack
   * Extraction de tous les fichiers JS par l’application globale sous le dossier `/component/`.
      * Webpack permet aux fichiers CSS/SCSS d’être liés via des fichiers JS.
      * Ces fichiers sont extraits via les deux points d'entrée `sites.js` et `vendors.js`.
   * Les seuls fichiers consommés par AEM sont les fichiers de sortie `site.js` et `site.css` dans `/clientlib-site`, ainsi que `dependencies.js` et `dependencies.css` dans `/clientlib-dependencies`
* Blocs
   * Principal (js/css de site)
   * Fournisseurs (js/css de dépendances)
* Prise en charge complète de Sass/Scss (Sass est compilé dans CSS via Webpack).

## Installation {#installation}

1. Installez globalement [NodeJS](https://nodejs.org/en/download/) (v10+). Cela installera également npm.
1. Accédez à ui.frontend dans votre projet et exécutez `npm install`.

## Utilisation {#usage}

Les scripts npm suivants orientent le flux de travail front-end :

* `npm run dev` : version complète avec optimisation JS désactivée (shaking d’arborescence, etc.), cartes source activées et optimisation CSS désactivée.
* `npm run prod` : version complète avec optimisation JS activée (shaking d’arborescence, etc.), cartes source désactivées et optimisation CSS activée.

## Sortie {#output}

### Général {#general}

* Site : `site.js` et `site.css` sont créés dans un dossier « clientlib-site ».
* Dépendances : `dependencies.js` et `dependencies.css` sont créés dans un dossier « clientlib-dependencies ».

### JavaScript {#javascript}

* Optimisation : pour les versions de production, tous les JS qui ne sont pas utilisés ou appelés sont supprimés.

### CSS {#css}

* Indexation automatique : toutes les feuilles de style CSS sont exécutées via un pré-indexeur et les propriétés nécessitant une pré-indexation sont automatiquement ajoutées dans les feuilles de style CSS.
* Optimisation : lors de la publication, toutes les feuilles de style CSS sont exécutées via un optimiseur (cssnano) qui les normalise selon les règles par défaut suivantes :
   * Réduit l’expression calc CSS chaque fois que possible, assurant à la fois la compatibilité du navigateur et la compression.
Convertit entre des valeurs équivalentes de longueur, de temps et d’angle. Notez que, par défaut, les valeurs de longueur ne sont pas converties.
   * Supprime les commentaires dans les règles, les sélecteurs et les déclarations et autour de ceux-ci.
   * Supprime les doublons de règles, de règles at et de déclarations.
      * Notez que cela ne fonctionne que pour les doublons exacts.
   * Supprime les règles vides, les requêtes multimédias et les règles ayant des sélecteurs vides, car elles n’affectent pas la sortie.
   * Fusionne les règles adjacentes par sélecteurs et paires propriété/valeur se chevauchant.
   * Garantit qu’un seul @charset est présent dans le fichier CSS et le déplace en haut du document.
   * Remplace le mot-clé initial CSS par la valeur réelle, lorsque la sortie obtenue est plus petite.
   * Compresse les définitions SVG en ligne avec SVGO.
* Nettoyage : comprend une tâche de nettoyage explicite pour effacer à la demande les fichiers CSS, JS et Map générés.
* Mappage de source : version de développement uniquement

>[!NOTE]
>L’option de version front-end utilise des fichiers de configuration Webpack uniquement destinés au développement et à la production qui partagent un fichier de configuration commun. Les paramètres de développement et de production peuvent ainsi être modifiés indépendamment.
