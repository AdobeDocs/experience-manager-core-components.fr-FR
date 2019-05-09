---
title: Développement des composants principaux
seo-title: Développement des composants principaux
description: Les composants principaux fournissent des composants de base robustes et extensibles qui offrent des fonctionnalités riches en fonctionnalités, une diffusion continue, un contrôle de version des composants, une mise en œuvre moderne, des balises Lean et une exportation JSON de contenu.
seo-description: Les composants principaux fournissent des composants de base robustes et extensibles qui offrent des fonctionnalités riches en fonctionnalités, une diffusion continue, un contrôle de version des composants, une mise en œuvre moderne, des balises Lean et une exportation JSON de contenu.
uuid: 68569 da 2-9 bc 8-4 e 20-9 a 71-e 5816 ace 51 ce
contentOwner: Utilisateur
content-type: référence
topic-tags: développement
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 157 a 2 ec 3-9 fca -4 fad -977 a-d 93013 eeb 218
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Développement des composants principaux{#developing-core-components}

## Présentation {#overview}

Les composants principaux fournissent des composants de base robustes et extensibles, et les points forts sont les suivants :

* Riches fonctionnalités
   * [Options de configuration souples pour répondre](authoring.md) à de nombreux cas d&#39;utilisation
   * [Fonctionnalités préconfigurables](authoring.md#pre-configuring-core-components) permettant de définir quelles fonctions sont disponibles pour les auteurs de pages
* Disponibilité continue
   * Améliorations fréquentes des fonctionnalités incrémentielles
   * Disponibilité du code [source sur github](https://github.com/adobe/aem-core-wcm-components) pour permettre à la communauté des développeurs de fournir des commentaires et de contribuer
   * Installation via un package de contenu publié [séparément](https://github.com/adobe/aem-core-wcm-components/releases) pour que les mises à niveau des composants soient réalisées indépendamment des mises à niveau AEM
* [Contrôle de version des composants](guidelines.md#component-versioning)
   * [Assurer la compatibilité dans une version](#upgrade-of-core-components), tout en permettant aux composants d&#39;évoluer
   * Autoriser plusieurs versions d&#39;un composant à coexister sur le même environnement
* Implémentation moderne
   * Annotations définies dans [le](https://helpx.adobe.com/experience-manager/htl/using/overview.html) langage HTML (HTML Template Language)
   * Logique du modèle de contenu implémentée avec [les modèles Sling](https://sling.apache.org/documentation/bundles/models.html)
* Balisage Lean
   * Notation BEM ( [Block Block Element)](https://getbem.com/) à compter de la version 2.0.0
      * La version précédente suit [les conventions](https://getbootstrap.com/css/) d&#39;attribution de noms d&#39;amorçage
   * Création autour [des directives d&#39;accessibilité](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)
   * Capacité à être utilisée pour les sites réactifs et mobiles
* Capacité de sérialiser en tant que JSON le modèle de contenu pour des cas d&#39;utilisation CMS sans précédent
* Accessible
   * Conformité à la norme [WCAG 2.0 AA](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)

>[!CAUTION]
>
>Les composants principaux requièrent AEM 6.3 ou une version ultérieure et Java 8.
>
>Les principaux composants ne fonctionnent pas dans l’IU classique.

## Présentation de la session Gems {#gems-session-overview}

Pour une présentation des composants principaux, des fonctionnalités qu&#39;ils proposent et de leur exploitation dans AEM, consultez les composants de [base AEM Gems Session AEM.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[Astuces pour Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) est une série d&#39;épisodes d&#39;épisodes techniques profonds fournis par des experts Adobe. Cette série complète la documentation du produit et de tous les autres canaux techniques, ce qui permet aux développeurs de prendre contact avec eux et d&#39;accéder à une rubrique spécifique.

## WEEKEND Developer Tutorial {#wknd-developer-tutorial}

[Commencez à développer des sites AEM avec des composants principaux en suivant cette étape : Didacticiel d&#39;étape - Par étape.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

## Diffusé sur github {#delivered-over-github}

Les composants principaux sont développés et distribués via github.

CODE SUR GITHUB

Vous pouvez trouver le code de cette page sur GitHub.

* [Ouvrez le projet aem-core-wcm-components sur github](https://github.com/adobe/aem-core-wcm-components)
* Téléchargement du projet au format [ZIP](https://github.com/adobe/aem-core-wcm-components/archive/master.zip)

Reportez-vous à la page [Utilisation de la](using.md) documentation sur les composants principaux pour savoir comment commencer à les utiliser dans votre projet.

L&#39;utilisation des composants principaux sur github permet d&#39;effectuer des mises à jour fréquentes et d&#39;écouter les commentaires de la communauté des développeurs AEM. En outre, cela devrait permettre aux clients et aux partenaires de suivre des modèles similaires lors de la création de composants personnalisés.

>[!NOTE]
>
>Pour connaître les dernières modifications apportées aux composants principaux, vous pouvez regarder le référentiel des composants [principaux](https://github.com/adobe/aem-core-wcm-components) sur github.

## Bibliothèque de composants

Découvrez la [bibliothèque](http://opensource.adobe.com/aem-core-wcm-components/library.html)de composants qui présente la version actuelle des composants principaux et fournit des exemples d&#39;utilisation.

### Exemple d&#39;exécution de contenu d&#39;exemple {#sample-content-run-mode}

Les composants principaux sont visibles dans Quickstart lorsque le contenu d&#39;exemple est présent, car le site de référence [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) les utilise. Toutefois, lors de l&#39;exécution en production (en `nosamplecontent` runmode exécution, sans exemple de contenu activé), les composants principaux ne sont plus présents et doivent être installés sur les instances AEM par l&#39;équipe de développement et/ou d&#39;exploitation.

>[!NOTE]
>
>Dans les environnements de production, exécutez toujours Quickstart en `nosamplecontent` mode exécution. Pour utiliser les composants principaux en `nosamplecontent` runmode d&#39;exécution, suivez les instructions de [la page Utilisation de composants](using.md) principaux.

## Fonctionnalités techniques {#technical-capabilities}

Le tableau suivant présente les différences entre les composants principaux et les composants de base.

Pour plus d&#39;informations sur leurs capacités de création et leurs options pour les préconfigurer, [reportez-vous à la page de création qui leur a été consacrée](authoring.md).

| **Fonction** | **Composant de base** | **Composant Foundation** |
|-----|---|---|
| Implémentation logique | Java pojos avec [annotations modèles](https://sling.apache.org/documentation/bundles/models.html) Sling | Code JSP |
| Définition d&#39;annotation | [Syntaxe HTML (](https://helpx.adobe.com/experience-manager/htl/user-guide.html) HTML Template Language) | Code JSP |
| Assainissement XSS | Automatisée par HTL | Essentiellement manuel |
| Nommage des classes CSS | Convention d&#39;affectation de nom normalisée basée sur [la notation BEM (Bloc Element Modificateur)](https://getbem.com/) (à compter de la version 2.0.0) | Modèles personnalisés |
| Définition de dialogue | [Coral 3](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Interface utilisateur Coral 2 + Classic |
| Sortie JSON | [Sling Models Exporter avec la sérialisation de Jackson](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | Servlet Sling par défaut |
| Création de versions | [Pour le modèle et le HTL](guidelines.md) | Aucun |
| Tests | Tests Unit + Tests d&#39;intégration | Tests d’intégration |
| Diffusion | [Via github public](https://github.com/adobe/aem-core-wcm-components) | Via Quickstart |
| Licence | [Licence Apache](https://www.apache.org/licenses/LICENSE-2.0) | Propriétaire d&#39;Adobe |
| Contribution | Via une demande d&#39;extraction | Impossible |
| Accessibilité | Totalement conforme à [la norme WCAG 2.0 AA](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html) | Partiellement conforme à la norme [WCAG 2.0 AA](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html) |

## Liste des composants {#component-list}

Le tableau suivant répertorie les composants principaux disponibles, liens vers leur API, et indique les composants foundation qu&#39;ils remplacent.

| Composant de base | Description | Remplacement des composants Foundation |
|---|---|---|
| [Page](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page) | Page réactive avec éditeur de modèles | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [Chemin de navigation](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb) | Navigation dans la hiérarchie des pages | `/libs/foundation/components/breadcrumb` |
| [Titre](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v2/title) | Titre H 1-H 6 | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [Texte](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | Texte enrichi | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [Image](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/image/v2/image) | Chargement intelligent et différé de la taille optimale du rendu | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [Liste](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v2/list) | Liste des pages | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [Partage sur les réseaux sociaux](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/sharing/v1/sharing) | Widget de partage Facebook et Pinterest | `-` |
| [Formular-Container](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v2/container) | Système de paragraphe de formulaire réactif | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [Texte du formulaire](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v2/text) | Champ de saisie de texte | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [Options du formulaire](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v2/options) | Champ de saisie d&#39;options multiples | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [Formulaire masqué](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v2/hidden) | Champ de saisie masqué | `/libs/foundation/components/form/hidden` |
| [Bouton de formulaire](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v2/button) | Bouton Envoyer ou personnalisé | `/libs/foundation/components/form/submit` |
| [Navigation](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/navigation/v1/navigation) | Composant de navigation sur le site qui répertorie la hiérarchie de la page imbriquée | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [Navigation par langue](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/languagenavigation/v1/languagenavigation) | Sélecteur de langue et de pays qui répertorie la structure de langue globale | `-` |
| [Recherche rapide](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/search/v1/search) | Un composant de recherche qui affiche les résultats sous forme de suggestions sur place dans un menu déroulant | `/libs/foundation/components/search` |
| [Teaser](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/teaser/v1/teaser) | Permet à l&#39;auteur de contenu de créer facilement un teaser vers un contenu supplémentaire à l&#39;aide d&#39;une image, d&#39;un titre ou d&#39;un texte enrichi et de lier un contenu supplémentaire ou d&#39;autres actions. | `-` |
| [Onglets](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/tabs/v1/tabs) | Permet à l&#39;auteur de contenu d&#39;organiser le contenu de la page dans plusieurs onglets | `-` |
| [Carrousel](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/carousel/v1/carousel) | Permet à l&#39;auteur de contenu d&#39;organiser le contenu dans un carrousel de diapositives. | `/libs/foundation/components/carousel` |
| [Frayer de contenu](https://github.com/adobe/aem-core-wcm-components/tree/master/extension/contentfragment/content/src/content/jcr_root/apps/core/wcm/extension/components/contentfragment/v1/contentfragment) | Autorise l&#39;affichage d&#39;un fragment de contenu | `-` |
| [Liste des fractions de contenu](https://github.com/adobe/aem-core-wcm-components/tree/master/extension/contentfragment/content/src/content/jcr_root/apps/core/wcm/extension/components/contentfragmentlist/v1/contentfragmentlist) | Autorise l&#39;affichage d&#39;une liste de fragments de contenu | `-` |
| [Séparateur](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/separator/v1/separator) | Sépare le contenu d&#39;une page | `-` |

### Composants à venir {#upcoming-components}

Les composants principaux suivants font l&#39;objet d&#39;un travail intensif. Ils n&#39;ont pas encore été publiés, mais peuvent être prévisualisés dans la branche [de développement](https://github.com/adobe/aem-core-wcm-components/tree/development):

* Vidéo
* Télécharger

## Mise à niveau des composants principaux {#upgrade-of-core-components}

L&#39;un des avantages des composants de version est qu&#39;il permet de séparer la migration vers une nouvelle version AEM de la migration vers les nouvelles versions des composants. En outre, si de nouvelles versions de composants sont disponibles, elles permettent la migration individuelle de chaque composant vers la nouvelle version.

Les migrations vers une nouvelle version AEM n&#39;affecteront pas le fonctionnement des composants principaux, à condition que leurs versions prennent également en charge la nouvelle version AEM qui est migrée. Les personnalisations apportées aux composants principaux ne doivent pas non plus être affectées, à condition qu&#39;elles n&#39;utilisent pas les API [obsolètes ou supprimées](https://helpx.adobe.com/experience-manager/6-5/release-notes/deprecated-removed-features.html).

Les migrations vers de nouvelles versions des composants principaux n&#39;auront aucune incidence sur le fonctionnement du composant. De plus, de nouvelles fonctionnalités peuvent être introduites aux auteurs de pages, ce qui peut nécessiter une configuration par un éditeur de modèle, au cas où le comportement par défaut ne serait pas souhaité. Toutefois, il est possible que des personnalisations doivent être adaptées. Pour plus d&#39;informations, consultez la page [Personnalisation des composants](customizing.md#upgrade-compatibility-of-customizations) principaux.

## Quand utiliser les composants principaux ? {#when-to-use-the-core-components}

Les composants principaux étant tout nouveau et offrent plusieurs avantages, il est recommandé que les nouveaux projets AEM les utilisent. Pour les projets existants, une migration doit faire partie d&#39;un effort de projet plus volumineux, par exemple une recomposition ou une restructuration globale.

Par conséquent, Adobe propose les recommandations suivantes :

* **Nouveaux projets**
Les nouveaux projets doivent toujours tenter d&#39;utiliser les composants principaux. Si les composants principaux ne peuvent pas être utilisés directement ou [étendus](customizing.md) pour répondre aux exigences du projet, créez un composant personnalisé après l&#39;architecture du composant définie dans les composants principaux. Sauf si cela est possible autrement, évitez d&#39;utiliser les [composants Foundation](developing.md).
* **La recommandation Projets**
existants continue à utiliser les composants [fondateurs](developing.md), à moins qu&#39;un site ou une restructuration de composants ne soit planifié.\
   Comme la plupart des projets existants sont très utilisés, les composants [fondateurs continueront à être pris en charge.](developing.md)
* **Nouveaux composants
personnalisés** Vous pouvez évaluer si un composant [principal existant peut être personnalisé](customizing.md).\
   Dans le cas contraire, vous devez créer un nouveau composant personnalisé suivant les instructions [des composants](guidelines.md).
* **Composants
personnalisés existants** Si vos composants fonctionnent comme prévu, conservez-les comme ils le sont.\
   Dans le cas contraire, reportez-vous à la section « Nouveaux composants personnalisés » ci-dessus.

### Prise en charge des composants principaux {#core-component-support}

Les composants principaux font partie intégrante d&#39;AEM et pris en charge en l&#39;état, selon les mêmes conditions et conditions que si elles étaient fournies dans le cadre de Quickstart.

À l&#39;instar des autres fonctionnalités du produit AEM, la règle générale est : Les composants doivent d&#39;abord être abandonnés et le plus ancien pour la version AEM suivante. Cela permet aux clients d&#39;au moins un cycle de publication pour passer à la nouvelle version du composant avant de ne pas abandonner sa prise en charge.

La version de chaque composant indique clairement les versions AEM prises en charge. Lorsque la prise en charge d&#39;une version d&#39;AEM est interrompue, la prise en charge des composants principaux de cette version d&#39;AEM est prise en charge.

Pour plus d&#39;informations sur la prise en charge des personnalisations des composants, voir la page [Personnalisation des composants](customizing.md) principaux.

### Prise en charge des composants Foundation {#foundation-component-support}

Dans la mesure où les composants fondateurs ont servi de base à une multitude de développement de projets sur de nombreuses versions, ils seront toujours pris en charge dans un futur prévisible.

Toutefois, l&#39;accent mis sur le développement d&#39;Adobe a été déplacé vers les composants principaux et les nouvelles fonctionnalités lui seront ajoutées alors que seuls les correctifs seront corrigés aux composants fondateurs.

**À lire aussi :**

* [Utilisation des composants](using.md) principaux - Soyez opérationnel avec les composants principaux de votre propre projet.
* [Instructions sur les composants](guidelines.md) - pour connaître les schémas d&#39;implémentation des composants principaux.
