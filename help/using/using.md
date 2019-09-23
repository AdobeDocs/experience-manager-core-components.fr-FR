---
title: Utilisation des composants principaux
seo-title: Utilisation des composants principaux
description: 'null'
seo-description: '« Pour que les composants principaux soient opérationnels dans votre propre projet, suivez les quatre étapes suivantes : téléchargement et installation, création de composants proxy, chargement des styles principaux et autorisation des composants de vos modèles. »'
uuid: a1ef2acf-8226-4510-838b-f5fae196f9f1
contentOwner: Utilisateur
content-type: référence
topic-tags: développement
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 1703a171-830c-477e-a34f-99caba841ec4
disttype: dist5
gnavtheme: light
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a1d725b6fc32112323e9939e8870922410a6c4f3

---


# Utilisation des composants principaux{#using-core-components}

Pour que les [ composants principaux](developing.md) soient opérationnels dans votre propre projet, vous devez suivre quatre étapes qui sont détaillées dans les sections ci-dessous :

1. [Téléchargement et installation](#download-and-install)
1. [Création des composants proxy](#create-proxy-components)
1. [Chargement des styles principaux](#load-the-core-styles)
1. [Autorisation des composants](#allow-the-components)

>[!NOTE]
>
>Pour obtenir des instructions plus générales pour commencer avec la configuration du projet, les composants principaux, les modèles modifiables, les bibliothèques clientes et le développement des composants, le tutoriel en plusieurs parties suivant peut vous intéresser :\
>[Prise en main du développement AEM Sites – Tutoriel WKND](wknd-tutorial.md)

## Téléchargement et installation {#download-and-install}

Les composants principaux ont avant tout été conçus pour être flexibles. La publication plus régulière de nouvelles versions des composants principaux permet à Adobe d'être plus flexible lors de la diffusion de nouvelles fonctionnalités. Les développeurs peuvent ensuite être flexibles dans les composants qu'ils choisissent d'intégrer dans leurs projets et dans la fréquence à laquelle ils souhaitent les mettre à jour.

C'est pourquoi les composants principaux ne font pas partie du démarrage rapide lors du démarrage en mode de production (sans exemple de contenu). Therefore, your first step is to [download the latest released content package from GitHub](https://github.com/adobe/aem-core-wcm-components/releases/latest) and to install it on your AEM environments.

There are several ways to automate this, but the simplest way to quickly install a content package on an instance is by using the Package Manager; see [Install Packages](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/package-manager.html). Also, once you'll have a publish instance running as well, you'll need to replicate that package to the publisher; see [Replicating Packages](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/package-manager.html).

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T16:42:59.142-0400

Should we be promoting embedding the core-component package as an artifact in a customer application, reasoning as follows: 1) a customer application is required to leverage core components (at a minimum, proxy components must be defined) 2) a customer application must be updated to leverage new versions of core components (since it requires adjusting the sling:resourceSuperType to point at the new version of the component) It seems the only time theres an advantage to installing a release directly is if a bug-fix (non version-changing) release of core-components is cut, and it doesnt coincide with an application deployment. WDYT? For example, recommend doing this for ACS Commons which has a similar use-case (https://adobe-consulting-services.github.io/acs-aem-commons/pages/maven.html) We can of course keep the instructions for manually deploying, since some will want to do this, or the bug-fix use-case will appear.

 -->

## Création des composants proxy {#create-proxy-components}

Pour des raisons expliquées dans la section[Modèle de composant proxy](guidelines.md#proxy-component-pattern), les composants principaux ne doivent pas être directement référencés à partir du contenu. Pour éviter cela, ils appartiennent tous à un groupe de composants masqué ( `.core-wcm` ou `.core-wcm-form`), ce qui les empêchera de s'afficher directement dans l'éditeur.

Au lieu de cela, des composants spécifiques au site doivent être créés, pour définir le nom et le groupe du composant que vous souhaitez afficher aux auteurs de page, puis ils doivent être référencés à un composant principal comme super-type. Ces composants spécifiques au site sont parfois nommés « composants proxy », car ils ne doivent rien contenir et servent principalement à définir la version d'un composant à utiliser pour le site. Toutefois, lors de la personnalisation des [composants principaux](customizing.md), ces composants proxy jouent un rôle essentiel pour la personnalisation des balises et des logiques.

Ainsi, pour chaque composant principal à utiliser pour un site, vous devez :

1. créer un composant proxy correspondant dans le dossier des composants du site,

   **Exemple**
sous `/apps/my-site/components` Créer un nœud de titre de type `cq:Component`

1. indiquer la version de composant principal correspondante avec le super-type,

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

For instance, look at the [title component of the We.Retail reference site](https://github.com/Adobe-Marketing-Cloud/aem-sample-we-retail/blob/master/ui.apps/src/main/content/jcr_root/apps/weretail/components/content/title/.content.xml), which is a good example of a proxy component that is built that way.

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

1. If not done yet, create a [Client Library](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html) that contains all of the CSS and JS files that are needed for your site.
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

Assurez-vous que vos composants proxy et vos bibliothèques client ont été déployés dans votre environnement AEM avant de passer à la section suivante.

## Autorisation des composants {#allow-the-components}

The following steps are performed in the [Template Editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html).

1. Dans l'éditeur de modèles, sélectionnez le conteneur de mises en page et ouvrez sa stratégie.
1. Dans la liste des composants autorisés, sélectionnez les composants proxy créés précédemment, qui doivent s'afficher sous le groupe de composants qui leur est affecté. Ensuite, appliquez les modifications.
1. (Facultatif) Les composants qui ont une boîte de dialogue de conception peuvent être préconfigurés.

C’est terminé ! Dans les pages créées à partir du modèle modifié, vous devez maintenant pouvoir utiliser les composants nouvellement créés.

**À lire aussi :**

* [Personnalisation des composants principaux](customizing.md) : pour savoir comment mettre en forme et personnaliser les composants principaux.
* [Instructions sur les composants](guidelines.md) : pour connaître les schémas d’implémentation des composants principaux.
