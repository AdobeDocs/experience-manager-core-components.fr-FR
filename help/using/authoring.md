---
title: Création à l’aide des composants principaux
seo-title: Création à l’aide des composants principaux
description: 'Dans AEM, les composants sont les éléments structurels qui représentent le contenu des pages créées : les composants principaux offrent une fonctionnalité de création flexible et riche en fonctionnalités.'
seo-description: 'Dans AEM, les composants sont les éléments structurels qui représentent le contenu des pages créées : les composants principaux offrent une fonctionnalité de création flexible et riche en fonctionnalités.'
uuid: 4 a 54 cd 4 c -3 d 89-4683-8301-bf 1 e 634736 e 3
content-type: référence
topic-tags: création
discoiquuid: 8751 e 490-d 427-44 f 2-b 767-51935 afda 988
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Auteur avec composants principaux

Dans Adobe Experience Manager, les composants sont des éléments structurels qui constituent le contenu des pages en cours de création. Cette section aborde les composants principaux qui fournissent des types de contenu essentiels pour créer des pages.

Les composants principaux offrent une fonctionnalité de création flexible et riche en fonctionnalités. Le [site de référence We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) illustre comment les composants principaux peuvent être utilisés.

>[!NOTE]
>
>Les composants principaux ne sont pas immédiatement disponibles pour les auteurs, l&#39;équipe [de développement doit d&#39;abord les intégrer à votre environnement](using.md). Une fois intégré, elles peuvent être rendues disponibles et préconfigurées via l&#39;éditeur [de modèles](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) ou en mode [de conception](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-designmode.html).

>[!CAUTION]
>
>Les composants principaux [requièrent AEM 6.3 ou une version ultérieure](versions.md) et ne fonctionnent pas avec l&#39;interface utilisateur classique.

## Création à l’aide des composants principaux {#authoring-with-core-components}

Pour comprendre les composants principaux, consultez la [bibliothèque de composants](http://opensource.adobe.com/aem-core-wcm-components/library.html)qui présente les composants principaux et fournit des exemples d&#39;utilisation.

En tant qu&#39;auteur, vous remarquerez plusieurs avantages des composants principaux, notamment :

* Simple d&#39;utilisation et bien intégré à l&#39;éditeur [de page](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html)
* Fonctionnalités riches en fonctionnalités pour répondre à de nombreux cas d&#39;utilisation comme [illustré dans We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html)
* [Préconfigurable](#pre-configuring-core-components) pour définir les fonctions disponibles pour les auteurs de pages
   * Via l&#39;éditeur [de modèles](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) pour [les modèles modifiables](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/page-templates-editable.html)
   * Via [le mode de création](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-designmode.html) pour [les modèles statiques](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/page-templates-static.html)

* Création autour [des directives d&#39;accessibilité](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)

* Création pour la [mise en page réactive](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/responsive-layout.html)

Les composants sont disponibles dans l&#39;onglet **Composants** du panneau latéral de l&#39;éditeur de page lors [de la modification d&#39;une page](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html).

Les composants sont regroupés selon des catégories appelées groupes de composants afin d&#39;organiser et de filtrer facilement les composants. Le nom du groupe de composants s&#39;affiche avec le composant dans l&#39;explorateur [de composants](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html) et il est également possible de filtrer par groupe pour trouver facilement le composant approprié.

>[!NOTE]
>
>Les composants principaux sont par défaut associés à un groupe masqué et ne sont pas visibles dans l&#39;explorateur de composants.
>
>Ajoutez les composants requis à un groupe visible ou personnalisez-les pour qu&#39;ils soient disponibles pour les auteurs.

## Préconfiguration des composants principaux {#pre-configuring-core-components}

La configuration des composants Foundation a été la tâche d&#39;un développeur. Toutefois, avec les composants principaux, un auteur de modèles peut maintenant configurer plusieurs fonctionnalités via l&#39;éditeur de modèles ou en mode de conception.

Par exemple, si un composant d&#39;image ne doit pas autoriser le chargement d&#39;images à partir du système de fichiers ou si un composant de texte doit autoriser uniquement la mise en forme des paragraphes, ces fonctions peuvent être activées ou désactivées en un simple clic.

Voir [Création de modèles de page](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) pour plus d&#39;informations.

### Modification et création de dialogues {#edit-and-design-dialogs}

Les composants principaux pouvant être préconfigurés par les auteurs de modèles pour définir les options autorisées dans le cadre d&#39;un modèle, puis configurés par l&#39;auteur de la page pour définir le contenu réel de la page, chaque composant peut avoir des options dans deux boîtes de dialogue différents.

|  | Description | Ce qu&#39;il contrôle | Exemples |
|--- |--- |--- |--- |
| **Modifier le dialogue** | Options qu&#39;un auteur **de page** peut modifier lors de l&#39;édition normale des pages pour les composants importés | Contenu affiché par le composant et mode d&#39;affichage final sur la page. | Formatage du texte du contenu, rotation d&#39;une image sur une page |
| **Créer un dialogue** | Options qu&#39;un **auteur** de modèle peut modifier lors de la configuration d&#39;un modèle de page. | Quelles options de l&#39;auteur de la page sont disponibles lors de la modification du composant ? | Quelles options de formatage de texte sont disponibles, quelles options d&#39;image sont disponibles |

### Style des composants {#component-styling}

Les styles de la plupart des composants principaux peuvent être définis à l&#39;aide du système de style AEM.

* Un auteur de modèle peut définir les styles disponibles pour un composant particulier dans la conception de dialogue de ce composant.
* L&#39;auteur du contenu peut ensuite choisir les styles à appliquer lors de l&#39;ajout du composant et la création de contenu.

Pour plus d&#39;informations, reportez-vous à [la documentation Système](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/style-system.html) de style.

>[!NOTE]
>
>Dans AEM 6.3, Service Pack 2 (6.3.2.0) ou plus récent est requis pour activer la fonctionnalité du système de style.

## Liste des composants principaux disponibles {#list-of-core-components-available}

Vous trouverez ci-dessous la liste des composants principaux disponibles liés aux pages décrivant leurs fonctionnalités de modification et de conception de conception en détails.

La version actuelle des composants principaux comporte les composants suivants.

* [Chemin de navigation](breadcrumb.md)
* [Bouton de formulaire](form-button.md)
* [Carrousel](carousel.md)
* [Formular-Container](form-container.md)
* [Fragment de contenu](content-fragment-component.md)
* [Liste des fragments de contenu](content-fragment-list.md)
* [Formulaire masqué](form-hidden.md)
* [Options du formulaire](form-options.md)
* [Texte du formulaire](form-text.md)
* [Image](image.md)
* [Navigation par langue](language-navigation.md)
* [Liste](list.md)
* [Navigation](navigation.md)
* [Page](page.md)
* [Recherche rapide](quick-search.md)
* [Séparateur](separator.md)
* [Partage sur les réseaux sociaux](sharing.md)
* [Teaser](teaser.md)
* [Texte](text.md)
* [Titre](title.md)

>[!CAUTION]
>
>Certaines versions de composants principaux individuels peuvent uniquement être compatibles avec certaines versions d&#39;AEM.
>
>Pour plus d&#39;informations, reportez-vous à la page d&#39;aide individuelle (liée à dans la liste précédente) pour le composant spécifique ou référencez le [document Versions](versions.md) des composants principaux.

>[!NOTE]
>
>En fonction de votre instance, vous disposez peut-être de composants personnalisés développés explicitement pour vos besoins. Ces composants peuvent même avoir le même nom que certains composants traités ici.
>Les composants principaux du formulaire ne sont pas liés à AEM Forms.

## Références pour les développeurs {#developer-resources}

Pour obtenir des informations techniques sur les composants principaux, reportez-vous à [la documentation Developing Core Components](developing.md) (Développement de composants principaux).
