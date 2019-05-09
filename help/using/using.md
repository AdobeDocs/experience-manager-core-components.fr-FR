---
title: Utilisation des composants principaux
seo-title: Utilisation des composants principaux
description: 'null'
seo-description: '« Pour maîtriser les composants principaux de votre propre projet, trois étapes sont possibles : télécharger et installer, créer des composants proxy, charger les styles principaux et autoriser les composants de vos modèles.  » »'
uuid: a 1 ef 2 acf -8226-4510-838 b-f 5 fae 196 f 9 f 1
contentOwner: Utilisateur
content-type: référence
topic-tags: développement
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 1703 a 171-830 c -477 e-a 34 f -99 caba 841 ec 4
disttype: dist5
gnavtheme: light
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Utilisation des composants principaux{#using-core-components}

Pour utiliser les composants [principaux](developing.md) dans votre propre projet, il existe quatre étapes qui sont détaillées individuellement dans les sections ci-dessous :

1. [Téléchargement et installation](#download-and-install)
1. [Création de composants proxy](#create-proxy-components)
1. [Chargement des styles principaux](#load-the-core-styles)
1. [Activation des composants](#allow-the-components)

>[!NOTE]
>
>Pour des instructions plus générales sur la manière de commencer à partir de zéro avec la configuration du projet, les composants principaux, les modèles modifiables, les bibliothèques client et le développement des composants, le didacticiel à parties multiples suivant peut présenter un intérêt :\
>[Prise en main des sites AEM - Didacticiel du week-end](wknd-tutorial.md)

## Téléchargement et installation {#download-and-install}

La souplesse est l&#39;une des idées qui génèrent des idées sous-jacentes aux principaux composants. La publication de nouvelles versions des composants principaux permet plus souvent à Adobe d&#39;être plus flexible lors de la diffusion de nouvelles fonctionnalités. Les développeurs peuvent ensuite être flexibles dans les composants qu&#39;ils choisissent d&#39;intégrer dans leurs projets et à la fréquence à laquelle ils souhaitent les mettre à jour.

C&#39;est pourquoi les composants principaux ne font pas partie du démarrage rapide lors du démarrage en mode de production (sans exemple de contenu). C&#39;est pourquoi la première étape consiste [à télécharger le dernier package de contenu publié depuis github](https://github.com/adobe/aem-core-wcm-components/releases/latest) et à l&#39;installer dans vos environnements AEM.

Il existe plusieurs manières d&#39;automatiser cette opération, mais la méthode la plus simple pour installer rapidement un package de contenu sur une instance consiste à utiliser Package Manager ; Voir [Installation de packages](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/package-manager.html). En outre, une fois qu&#39;une instance de publication s&#39;exécute, vous devrez dupliquer ce package dans l&#39;éditeur ; Voir [Répliquation de packages](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/package-manager.html).

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T16:42:59.142-0400

Should we be promoting embedding the core-component package as an artifact in a customer application, reasoning as follows: 1) a customer application is required to leverage core components (at a minimum, proxy components must be defined) 2) a customer application must be updated to leverage new versions of core components (since it requires adjusting the sling:resourceSuperType to point at the new version of the component) It seems the only time theres an advantage to installing a release directly is if a bug-fix (non version-changing) release of core-components is cut, and it doesnt coincide with an application deployment. WDYT? For example, recommend doing this for ACS Commons which has a similar use-case (https://adobe-consulting-services.github.io/acs-aem-commons/pages/maven.html) We can of course keep the instructions for manually deploying, since some will want to do this, or the bug-fix use-case will appear.

 -->

## Création de composants proxy {#create-proxy-components}

Pour des raisons expliquées dans [la section Modèle](guidelines.md#proxy-component-pattern) de composant proxy, les composants principaux ne doivent pas être directement référencés à partir du contenu. Pour éviter cela, ils appartiennent tous à un groupe de composants masqué ( `.core-wcm` ou `.core-wcm-form`), ce qui les empêchera de s&#39;afficher directement dans l&#39;éditeur.

Au lieu de cela, des composants spécifiques au site doivent être créés, qui définissent le nom et le groupe du composant de votre choix à afficher aux auteurs de page, puis les référencez à un composant principal comme super-type. Ces composants spécifiques au site sont parfois nommés « composants proxy », car ils ne doivent rien contenir et servent principalement à définir la version d&#39;un composant à utiliser pour le site. Toutefois, lors de la personnalisation des composants [principaux](customizing.md), ces composants proxy jouent un rôle essentiel pour la personnalisation des balises et des logiques.

Ainsi, pour chaque composant principal à utiliser pour un site, vous devez :

1. Créez un composant proxy correspondant dans le dossier des composants du site.

   **Exemple**
sous `/apps/my-site/components` Création d&#39;un nœud de titre de type `cq:Component`

1. Pointez vers la version de composant principal correspondante avec le super-type.

   **Exemple**
Ajouter la propriété suivante :\
   `sling:resourceSuperType="core/wcm/components/title/v1/title"`

1. Définissez le groupe, le titre et la description facultative du composant. Ces valeurs sont spécifiques au projet et déterminent la manière dont le composant est exposé aux auteurs.

   **Exemple**
Ajoutez les propriétés suivantes :

   ```shell
   componentGroup="My Site"
   jcr:title="Title"  
   jcr:description="Section Heading"
   ```

Par exemple, examinez le composant [titre du site de référence We. Retail](https://github.com/Adobe-Marketing-Cloud/aem-sample-we-retail/blob/master/ui.apps/src/main/content/jcr_root/apps/weretail/components/content/title/.content.xml), qui est un bon exemple de composant proxy qui est créé de cette manière.

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

1. Si ce n&#39;est pas encore fait, créez une [bibliothèque](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html) client contenant tous les fichiers CSS et JS nécessaires à votre site.
1. Dans la bibliothèque client de votre site, ajoutez les dépendances aux composants principaux qui peuvent être nécessaires. Pour ce faire, ajoutez une `embed` propriété.

   Par exemple, pour inclure les bibliothèques client de tous les composants principaux v 1, la propriété à ajouter serait :

   ```shell
   embed="[  
   core.wcm.components.image.v1,  
   core.wcm.components.list.v1,  
   core.wcm.components.breadcrumb.v1,  
   core.wcm.components.form.container.v1,  
   core.wcm.components.form.text.v1  
   ]"
   ```

Assurez-vous que vos composants proxy et bibliothèques client ont été déployés dans votre environnement AEM avant de passer à la section suivante.

## Autoriser les composants {#allow-the-components}

Les étapes suivantes sont généralement effectuées dans l&#39;éditeur [](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)de modèles, pour les configurations existantes toutefois, en mode Conception :

1. Dans l&#39;éditeur de modèles (ou le mode Création), sélectionnez le conteneur de dispositions (ou parsys), puis ouvrez sa stratégie (ou config de conception).
1. Dans la liste des composants autorisés, sélectionnez les composants proxy créés précédemment, qui doivent s&#39;afficher sous le groupe de composants qui leur est affecté. Ensuite, appliquez les modifications.
1. (Facultatif) Pour les composants qui ont une boîte de dialogue de conception, ils peuvent être préconfigurés.

Ainsi, dans les pages créées à partir du modèle modifié, vous devez maintenant pouvoir utiliser les composants nouvellement créés.

**À lire aussi :**

* [Personnalisation des composants principaux](customizing.md) - pour savoir comment mettre en forme et personnaliser les composants principaux.
* [Instructions sur les composants](guidelines.md) - pour connaître les schémas d&#39;implémentation des composants principaux.
