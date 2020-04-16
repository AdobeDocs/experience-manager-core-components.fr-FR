---
title: Utilisation des composants principaux
description: '« Pour que les composants principaux soient opérationnels dans votre propre projet, suivez les quatre étapes ci-après : téléchargement et installation, création de composants proxy, chargement des styles principaux et autorisation des composants de vos modèles. »'
translation-type: ht
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Utilisation des composants principaux{#using-core-components}

Pour que les composants principaux soient opérationnels dans votre propre projet, vous devez suivre quatre étapes qui sont détaillées dans les sections ci-dessous :

1. [Téléchargement et installation](#download-and-install)
1. [Création des composants proxy](#create-proxy-components)
1. [Chargement des styles principaux](#load-the-core-styles)
1. [Autorisation des composants](#allow-the-components)

>[!NOTE]
>
>Pour obtenir des instructions plus générales pour commencer avec la configuration du projet, les composants principaux, les modèles modifiables, les bibliothèques clientes et le développement des composants, le tutoriel en plusieurs parties suivant peut vous intéresser :\
>[Prise en main du développement AEM Sites – Tutoriel WKND](https://docs.adobe.com/content/help/fr/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

## Téléchargement et installation {#download-and-install}

Les composants principaux ont avant tout été conçus pour être flexibles. La publication plus régulière de nouvelles versions des composants principaux permet à Adobe d&#39;être plus flexible lors de la diffusion de nouvelles fonctionnalités. Les développeurs peuvent ensuite être flexibles dans les composants qu&#39;ils choisissent d&#39;intégrer dans leurs projets et dans la fréquence à laquelle ils souhaitent les mettre à jour.

C&#39;est pourquoi les composants principaux ne font pas partie du démarrage rapide lors du démarrage en mode de production (sans exemple de contenu). C’est pourquoi la première étape consiste [à télécharger le dernier module de contenu publié à partir de GitHub](https://github.com/adobe/aem-core-wcm-components/releases/latest) et à l’installer dans vos environnements AEM.

Il existe plusieurs manières d’automatiser cette opération, mais la méthode la plus simple pour installer rapidement un module de contenu sur une instance consiste à utiliser le gestionnaire de modules. Consultez la section [Installation des modules](https://docs.adobe.com/content/help/en/experience-manager-65/administering/contentmanagement/package-manager.html#installing-packages). En outre, une fois qu’une instance de publication s’exécute, vous devrez répliquer ce module dans l’éditeur. Consultez la section [Réplication des modules](https://docs.adobe.com/content/help/en/experience-manager-65/administering/contentmanagement/package-manager.html#replicating-packages).

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T16:42:59.142-0400

Should we be promoting embedding the core-component package as an artifact in a customer application, reasoning as follows: 1) a customer application is required to leverage core components (at a minimum, proxy components must be defined) 2) a customer application must be updated to leverage new versions of core components (since it requires adjusting the sling:resourceSuperType to point at the new version of the component) It seems the only time theres an advantage to installing a release directly is if a bug-fix (non version-changing) release of core-components is cut, and it doesnt coincide with an application deployment. WDYT? For example, recommend doing this for ACS Commons which has a similar use-case (https://adobe-consulting-services.github.io/acs-aem-commons/pages/maven.html) We can of course keep the instructions for manually deploying, since some will want to do this, or the bug-fix use-case will appear.

 -->

## Création des composants proxy {#create-proxy-components}

Pour des raisons expliquées dans la section[Modèle de composant proxy](/help/developing/guidelines.md#proxy-component-pattern), les composants principaux ne doivent pas être directement référencés à partir du contenu. Pour éviter cela, ils appartiennent tous à un groupe de composants masqué ( `.core-wcm` ou `.core-wcm-form`), ce qui les empêchera de s&#39;afficher directement dans l&#39;éditeur.

Au lieu de cela, des composants spécifiques au site doivent être créés, pour définir le nom et le groupe du composant que vous souhaitez afficher aux auteurs de page, puis ils doivent être référencés à un composant principal comme super-type. Ces composants spécifiques au site sont parfois nommés « composants proxy », car ils ne doivent rien contenir et servent principalement à définir la version d&#39;un composant à utiliser pour le site. Toutefois, lors de la personnalisation des [composants principaux](/help/developing/customizing.md), ces composants proxy jouent un rôle essentiel pour la personnalisation des balises et des logiques.

Ainsi, pour chaque composant principal à utiliser pour un site, vous devez :

1. créer un composant proxy correspondant dans le dossier des composants du site,

   **Exemple**
sous `/apps/my-site/components` Créer un nœud de titre de type `cq:Component`

1. pointer vers la version de composant principal correspondante avec le super-type,

   **Exemple**
Ajouter la propriété suivante :\
   `sling:resourceSuperType="core/wcm/components/title/v1/title"`

1. définir le groupe, le titre et la description facultative du composant. Ces valeurs sont spécifiques au projet et déterminent la manière dont le composant est exposé aux auteurs.

   **Exemple**
Ajoutez les propriétés suivantes :

   ```shell
   componentGroup="My Site"
   jcr:title="Title"  
   jcr:description="Section Heading"
   ```

Par exemple, consultez le composant [Titre du site de référence We.Retail ](https://github.com/Adobe-Marketing-Cloud/aem-sample-we-retail/blob/master/ui.apps/src/main/content/jcr_root/apps/weretail/components/content/title/.content.xml), qui constitue un bon exemple de composant proxy créé de cette manière.

## Chargement des styles principaux {#load-the-core-styles}

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T16:57:16.414-0400

Styles is odd in that most Core Components do not have CSS; very few even have structural CSS (breadcrumbs, list) It may be more apt to title this section: Load the Core JavaScript and CSS or Load the Core Client Libraries ?

 -->

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T17:41:37.115-0400

This section seems to cover the "sites" clientlibs for core components; Do we need a section for ensuring the editor clientlibs are loaded in the Page Editor? Pending: https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/issues/15

 -->

<!-- 

Comment Type: annotation
Last Modified By: cotescu
Last Modified Date: 2018-03-09T10:45:52.812-0500

Load the Core Client Libraries sounds way better

 -->

1. Si ce n’est pas encore fait, créez une [bibliothèque cliente](https://docs.adobe.com/content/help/en/experience-manager-65/developing/introduction/clientlibs.html) qui contient tous les fichiers CSS et JS nécessaires à votre site.
1. Dans la bibliothèque cliente de votre site, ajoutez les dépendances aux composants principaux qui peuvent être nécessaires. Pour ce faire, ajoutez une propriété `embed`.

   Par exemple, pour inclure les bibliothèques clientes de tous les composants principaux v1, la propriété à ajouter serait :

   ```shell
   embed="[  
   core.wcm.components.image.v1,  
   core.wcm.components.list.v1,  
   core.wcm.components.breadcrumb.v1,  
   core.wcm.components.form.container.v1,  
   core.wcm.components.form.text.v1  
   ]"
   ```

Assurez-vous que vos composants proxy et vos bibliothèques clientes ont été déployés dans votre environnement AEM avant de passer à la section suivante.

## Autorisation des composants {#allow-the-components}

Les étapes suivantes sont effectuées dans l’[éditeur de modèles](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

1. Dans l&#39;éditeur de modèles, sélectionnez le conteneur de mises en page et ouvrez sa stratégie.
1. Dans la liste des composants autorisés, sélectionnez les composants proxy créés précédemment, qui doivent s&#39;afficher sous le groupe de composants qui leur est affecté. Ensuite, appliquez les modifications.
1. (Facultatif) Les composants qui ont une boîte de dialogue de conception peuvent être préconfigurés.

C’est terminé ! Dans les pages créées à partir du modèle modifié, vous devez maintenant pouvoir utiliser les composants nouvellement créés.

**À lire aussi :**

* [Personnalisation des composants principaux](/help/developing/customizing.md) : pour savoir comment mettre en forme et personnaliser les composants principaux.
* [Instructions sur les composants](/help/developing/guidelines.md) : pour connaître les schémas d’implémentation des composants principaux.
