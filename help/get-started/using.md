---
title: Utilisation des composants principaux
description: '« Pour que les composants principaux soient opérationnels dans votre propre projet, suivez les quatre étapes ci-après : téléchargement et installation, création de composants proxy, chargement des styles principaux et autorisation des composants de vos modèles. »'
role: Architect, Developer, Administrator, Business Practitioner
exl-id: ee2d25e4-e2b8-4ecc-a62c-f0066de2bf2d
source-git-commit: 45a17fe42146516f351f897e85a4a48dcf3aadab
workflow-type: tm+mt
source-wordcount: '977'
ht-degree: 100%

---

# Utilisation des composants principaux {#using-core-components}

Pour que les composants principaux soient opérationnels dans votre propre projet, vous devez suivre quatre étapes qui sont détaillées dans les sections ci-dessous :

1. [Téléchargement et installation](#download-and-install)
1. [Création des composants proxy](#create-proxy-components)
1. [Chargement des styles principaux](#load-the-core-styles)
1. [Autorisation des composants](#allow-the-components)

>[!TIP]
>
>Pour obtenir des instructions plus générales pour commencer avec la configuration du projet, les composants principaux, les modèles modifiables, les bibliothèques clientes et le développement des composants, le tutoriel en plusieurs parties suivant peut vous intéresser :\
>[Prise en main du développement AEM Sites – Tutoriel WKND](https://docs.adobe.com/content/help/fr-FR/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

>[!TIP]
>
>Si vous utilisez l’[archétype de projet AEM](/help/developing/archetype/overview.md), les composants principaux sont automatiquement inclus dans votre projet conformément aux recommandations de bonnes pratiques d’Adobe.

## Téléchargement et installation {#download-and-install}

Les composants principaux ont avant tout été conçus pour être flexibles. La publication plus régulière de nouvelles versions des composants principaux permet à Adobe d’être plus flexible lors de la diffusion de nouvelles fonctionnalités. Les développeurs peuvent ensuite être flexibles dans les composants qu’ils choisissent d’intégrer dans leurs projets et dans la fréquence à laquelle ils souhaitent les mettre à jour. La publication des composants AEM et celle des composants principaux se déroulent ainsi au travers de processus distincts.

Par conséquent, les étapes d’installation se déroulent différemment selon que vous exécutiez AEM as a Cloud Service ou On-Premise.

### AEM as a Cloud Service {#aemaacs}

Vous n’avez rien à faire. AEM as a Cloud Service est automatiquement fourni avec la dernière version des composants principaux. AEM as a Cloud Service vous offre également les dernières fonctionnalités d’AEM et fait en sorte que vos composants principaux soient automatiquement mis à jour.

Gardez à l’esprit les points suivants lorsque vous utilisez les composants principaux sur AEM as a Cloud Service :

* Les composants principaux sont inclus dans `/libs`.
* Le pipeline de génération de projet génère des avertissements dans le journal s’il inclut également les composants principaux dans `/apps`. Il ignorera alors la version intégrée dans le cadre de votre projet.
   * Dans une prochaine version, l’ajout de composants principaux supplémentaires causera l’échec du processus de génération du pipeline.
* Si votre projet incluait précédemment les composants principaux dans `/apps`, [vous devrez peut-être le paramétrer différemment](/help/developing/overview.md#via-aemaacs).
* Même si les composants principaux se trouvent maintenant dans `/libs`, il n’est pas recommandé de créer un recouvrement du même chemin dans `/apps`. Si un élément quelconque des composants devait être personnalisé, nous vous recommandons d’utiliser [le modèle de composant de proxy](/help/developing/guidelines.md#proxy-component-pattern) à la place.

### AEM 6.5 et version antérieure {#aem-65}

Les composants principaux ne font pas partie du démarrage rapide lors du lancement en mode de production (sans exemple de contenu). C’est pourquoi la première étape consiste [à télécharger le dernier module de contenu publié à partir de GitHub](https://github.com/adobe/aem-core-wcm-components/releases/latest) et à l’installer dans vos environnements AEM.

Il existe plusieurs manières d’automatiser cette opération, mais la méthode la plus simple pour installer rapidement un module de contenu sur une instance consiste à utiliser le gestionnaire de modules. Consultez la section [Installation des modules](https://docs.adobe.com/content/help/fr-FR/experience-manager-65/administering/contentmanagement/package-manager.html#installing-packages). En outre, une fois qu’une instance de publication s’exécute, vous devrez répliquer ce module dans l’éditeur. Consultez la section [Réplication des modules](https://docs.adobe.com/content/help/fr-FR/experience-manager-65/administering/contentmanagement/package-manager.html#replicating-packages).

## Création des composants proxy {#create-proxy-components}

Pour des raisons expliquées dans la section [Modèle de composant proxy](/help/developing/guidelines.md#proxy-component-pattern), les composants principaux ne doivent pas être directement référencés à partir du contenu. Pour éviter cela, ils appartiennent tous à un groupe de composants masqué ( `.core-wcm` ou `.core-wcm-form`), ce qui les empêchera de s’afficher directement dans l’éditeur.

Au lieu de cela, des composants spécifiques au site doivent être créés, pour définir le nom et le groupe du composant que vous souhaitez afficher aux auteurs de page, puis ils doivent être référencés à un composant principal comme super-type. Ces composants spécifiques au site sont parfois nommés « composants proxy », car ils ne doivent rien contenir et servent principalement à définir la version d’un composant à utiliser pour le site. Toutefois, lors de la personnalisation des [composants principaux](/help/developing/customizing.md), ces composants proxy jouent un rôle essentiel pour la personnalisation des balises et des logiques.

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
Ajoutez les propriétés suivantes :

   ```shell
   componentGroup="My Site"
   jcr:title="Title"  
   jcr:description="Section Heading"
   ```

Par exemple, consultez le [composant Titre du site WKND](https://github.com/adobe/aem-guides-wknd/blob/master/ui.apps/src/main/content/jcr_root/apps/wknd/components/title/.content.xml), qui constitue un bon exemple de composant proxy créé de cette manière.

## Chargement des styles principaux {#load-the-core-styles}

1. Si ce n’est pas encore fait, créez une [bibliothèque cliente](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html?lang=fr-FR) qui contient tous les fichiers CSS et JS nécessaires à votre site.
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

Les étapes suivantes sont effectuées dans l’[éditeur de modèles](https://docs.adobe.com/content/help/fr-FR/experience-manager-cloud-service/sites/authoring/features/templates.html).

1. Dans l’éditeur de modèles, sélectionnez le conteneur de mises en page et ouvrez sa stratégie.
1. Dans la liste des composants autorisés, sélectionnez les composants proxy créés précédemment, qui doivent s’afficher sous le groupe de composants qui leur est affecté. Ensuite, appliquez les modifications.
1. (Facultatif) Les composants qui ont une boîte de dialogue de conception peuvent être préconfigurés.

C’est terminé ! Dans les pages créées à partir du modèle modifié, vous devez maintenant pouvoir utiliser les composants nouvellement créés.

**À lire aussi :**

* [Personnalisation des composants principaux](/help/developing/customizing.md) : pour savoir comment mettre en forme et personnaliser les composants principaux.
* [Instructions sur les composants](/help/developing/guidelines.md) : pour connaître les schémas d’implémentation des composants principaux.
