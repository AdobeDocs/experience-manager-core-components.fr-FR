---
title: Composant principal Forms adaptatif - Google reCAPTCHA
description: Améliorez la sécurité des formulaires avec le service Google reCAPTCHA sans effort avec AEM Forms. Explication des propriétés de reCaptcha du formulaire adaptatif
role: Architect, Developer, Admin, User
source-git-commit: 4c510b8fe59f4be6e1b329ee4257ab1b780fbf22
workflow-type: tm+mt
source-wordcount: '1325'
ht-degree: 82%

---


# reCAPTCHA du formulaire adaptatif {#google-recaptcha}

CAPTCHA (Completely Automated Public Turing Test to say Computers and Humans Separ) est un programme couramment utilisé dans les transactions en ligne pour distinguer les humains des programmes ou robots automatisés. Il présente un test et évalue la réponse de l’utilisateur ou de l’utilisatrice pour déterminer s’il s’agit d’une personne humaine ou d’un robot qui interagit avec le site. Cela empêche l’utilisateur ou l’utilisatrice de continuer si le test échoue et permet de sécuriser les transactions en ligne en empêchant les robots d’envoyer du spam ou des éléments malveillants.

AEM Forms as a Cloud Service prend en charge Google reCAPTCHA v2 dans les formulaires adaptatifs. Vous pouvez l’utiliser pour présenter un défi Captcha lors de l’envoi du formulaire.

## Utilisation {#reasons-to-use-google-recaptcha}


- **Prévention contre le spam et les robots** : l’une des principales raisons d’utiliser reCAPTCHA est d’empêcher les envois de spam et l’afflux de robots malveillants dans votre formulaire. Les algorithmes avancés de reCAPTCHA peuvent détecter les tentatives automatisées d’envoi du formulaire, assurant ainsi que seuls les utilisateurs et utilisatrices légitimes peuvent interagir avec celui-ci.

- **Sécurité renforcée** : en implémentant reCAPTCHA, vous ajoutez une couche supplémentaire de sécurité à votre formulaire adaptatif. Cela permet de protéger les informations sensibles et d’empêcher les utilisateurs et utilisatrices malveillants d’exploiter les vulnérabilités.

- **Expérience client** : bien que les Captcha puissent parfois être considérés comme un inconvénient, l’approche adaptative de reCAPTCHA signifie que la plupart des utilisateurs et utilisatrices se voient présenter une expérience rationalisée et conviviale qui nécessite une interaction minimale. Cela peut aider à maintenir une expérience client positive tout en dissuadant les robots.

- **Adaptabilité** : le mécanisme adaptatif de reCAPTCHA analyse le comportement et les interactions des utilisateurs et utilisatrices pour déterminer s’ils sont humains ou non. Cela signifie que le niveau de défi présenté à la personne utilisatrice peut varier en fonction de la probabilité qu’elle soit un robot. Cette adaptabilité réduit la friction pour les utilisateurs et utilisatrices authentiques tout en maintenant une sécurité renforcée.

- **Modération manuelle réduite** : en réduisant de manière significative le nombre d’envois de spam et le contenu généré par les robots, reCAPTCHA peut faire économiser du temps et des ressources qui seraient autrement utilisés pour la modération manuelle et le nettoyage.

## Version et compatibilité {#version-and-compatibility}

Le composant principal Google reCAPTCHA du formulaire adaptatif a été publié en août 2023 dans le cadre de la « version » des composants principaux. Vous trouverez ci-dessous un tableau détaillant les versions prises en charge, la compatibilité avec AEM et les liens vers la documentation correspondante :


| Version du composant | AEM as a Cloud Service |
|--- |--- |
| v1 | Compatible avec la <br>[version 2.0.4](/help/versions.md) et les versions ultérieures | Compatible | Compatible |

Pour plus d’informations sur les versions et publications des composants principaux, consultez le document [Versions des composants principaux](/help/versions.md).

## Détails techniques {#technical-details}

Retrouvez les informations les plus récentes sur le composant principal Google reCAPTCHA des formulaires adaptatifs dans la documentation technique sur [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/recaptcha/v1/recaptcha). Pour plus d’informations sur le développement des composants principaux, consultez la [documentation destinée aux développeurs et développeuses de composants principaux](/help/developing/overview.md).

## Boîte de dialogue de configuration {#configure-dialog}

Vous pouvez facilement personnaliser votre expérience Google reCAPTCHA pour les visiteurs et les visiteuses à l’aide de la boîte de dialogue de configuration. Vous pouvez également définir facilement des options de Google reCAPTCHA pour une expérience client fluide.

### Onglet De base {#basic-tab}

![Onglet De base](/help/adaptive-forms/assets/recaptcha-basictab.png)

- **Nom** - Vous pouvez identifier facilement un composant de formulaire avec son nom unique aussi bien dans le formulaire et dans l’éditeur de règles, mais le nom ne doit pas contenir d’espaces ni de caractères spéciaux.

- **Titre** - Avec son titre, vous pouvez facilement identifier un composant dans un formulaire. Par défaut, le titre s’affiche au-dessus du composant. Si vous n’ajoutez pas de titre, le nom du composant s’affiche à la place du texte du titre.

- **Autoriser le texte enrichi pour le titre** : cette fonctionnalité permet aux personnes de mettre en forme les titres en texte brut en y incorporant des fonctionnalités telles que le texte en gras, en italique et souligné, diverses polices, tailles de police et couleurs, et d’autres options pour améliorer la présentation visuelle et la personnalisation. Elle offre une plus grande flexibilité et un contrôle créatif pour faire ressortir les titres dans les documents, sites web ou applications.\
  Lorsque vous cochez la case **Autoriser le texte enrichi pour le titre, les options de mise en forme deviennent visibles pour appliquer un style au titre du composant. Pour accéder à toutes les options de formatage disponibles, vous pouvez cliquer sur l’onglet ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Prise en charge de texte enrichi](/help/adaptive-forms/assets/richtext-support-title.png)

- **Masquer le titre** - Sélectionnez cette option pour masquer le titre du composant.
- **Marquer comme élément de formulaire non lié** : sélectionnez cette option pour configurer un champ de formulaire qui n’est lié à aucun schéma. Cette option vous permet d’enregistrer des données sans mettre à jour la source de données. Elle vous permet également de gérer les données de manière personnalisée, en les séparant de l’intégration de base de données standard.
- **Paramètres de configuration**: sélectionnez le conteneur de configuration qui contient la configuration cloud connectant AEM Forms au service reCAPTCHA de Google.

  >[!NOTE]
  >
  > Voir [Utilisation de Google reCAPTCHA dans un formulaire adaptatif AEM basé sur les composants principaux](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components) article pour découvrir comment créer et configurer Google reCAPTCHA pour votre environnement.

- **Type**: choisissez cette option pour sélectionner la taille de reCAPTCHA.
   - **Normal**: fait référence à la version standard plus grande du widget reCAPTCHA, qui peut être plus visible et plus facile à utiliser pour les utilisateurs, en particulier sur les périphériques dotés d’écrans plus volumineux.
   - **Compact**: fait référence à une version plus petite du widget reCAPTCHA. Cette option est adaptée aux situations dans lesquelles l’espace est limité, par exemple sur les appareils mobiles ou dans des dispositions étroites sur les pages web.

- **Masquer le composant** - Sélectionnez cette option pour masquer le composant du formulaire. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles. Cela s’avère utile lorsque vous devez stocker des informations qui n’ont pas besoin d’être affichées ou directement modifiées par les utilisateurs ou les utilisatrices.

- **Désactiver le composant** - Sélectionnez cette option pour désactiver le composant. Le composant désactivé n’est pas actif ni modifiable par l’utilisateur final ou l’utilisatrice finale. Les données du composant désactivé ne sont pas envoyées. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

- **Lecture seule** - Sélectionnez cette option pour rendre le composant non modifiable. L’utilisateur ou l’utilisatrice peut voir la valeur du champ mais ne peut pas la modifier. Le composant reste accessible à d’autres fins, par exemple pour les calculs dans l’éditeur de règles.

### Onglet Validation {#validation-tab}

![Onglet Validation](/help/adaptive-forms/assets/recaptcha-validationtab.png)

- **Message d’erreur** : Cette option vous permet de saisir un message qui s’affiche si la case à cocher **Obligatoire** est cochée et que le champ de formulaire reste vide.

- **Message de validation de script** - Cette option permet de saisir un message à afficher en cas d’échec de la validation du script.

## Boîte de dialogue de conception {#design-dialog}

La boîte de dialogue de conception permet de définir et de gérer les styles CSS du composant reCAPTCHA.

### Onglet Styles {#styles-design-tab}

Le composant principal reCAPTCHA de Forms adaptatif prend en charge l’AEM [Système de style](/help/get-started/authoring.md#component-styling).

![Boîte de dialogue de conception](/help/adaptive-forms/assets/checkbox-style.png)

- **Classes CSS par défaut**: vous pouvez fournir une classe CSS par défaut pour le composant principal reCAPTCHA de Forms adaptatif.

- **Styles autorisés** : vous pouvez définir des styles en fournissant un nom et la classe CSS qui représente le style. Par exemple, vous pouvez créer un style nommé « texte en gras » et fournir la classe CSS « police d’épaisseur : gras ». Vous pouvez utiliser ou appliquer ces styles à un formulaire adaptatif dans l’éditeur de formulaires adaptatifs. Pour appliquer un style, sélectionnez le composant auquel vous souhaitez appliquer le style dans l’éditeur de formulaires adaptatifs, accédez à la boîte de dialogue Propriétés, puis sélectionnez le style de votre choix dans la liste déroulante **Styles**. Si vous devez mettre à jour ou modifier les styles, revenez simplement à la boîte de dialogue Conception, mettez à jour les styles dans l’onglet Styles et enregistrez les modifications.

### Propriétés personnalisées

![Boîte de dialogue Propriétés personnalisées](/help/adaptive-forms/assets/checkbox-customproperties.png)

Les propriétés personnalisées vous permettent d’associer des attributs personnalisés (paires clé-valeur) à un composant principal de formulaire adaptatif à l’aide du modèle de formulaire. Les propriétés personnalisées sont répercutées dans la section des propriétés du rendu déocuplé du composant. Cela permet de créer un comportement de formulaire dynamique qui s’adapte en fonction des valeurs d’attributs personnalisés. Par exemple, les développeurs et développeuses peuvent concevoir plusieurs rendus d’un composant de formulaires découplés pour des plateformes mobiles, de bureau ou web, ce qui améliore considérablement l’expérience client sur un large éventail d’appareils.
- **Nom du groupe** : vous pouvez fournir un nom pour identifier le groupe de propriétés personnalisées. Vous pouvez ajouter, supprimer ou réorganiser plusieurs groupes de propriétés personnalisées. Après avoir ajouté le groupe de propriétés personnalisées, vous pouvez voir les options suivantes :

   - **Paires clé-valeur** : vous pouvez ajouter plusieurs noms et valeurs de propriétés personnalisées en cliquant sur le bouton **Ajouter** pour chaque groupe de propriétés personnalisées.

   - **Supprimer** : appuyez ou cliquez pour supprimer le nom et la valeur des propriétés personnalisées.

   - **Réorganiser** : appuyez ou cliquez et faites glisser pour réorganiser le nom et la valeur des propriétés personnalisées.


## Articles connexes {#related-articles}

{{more-like-this}}

## Voir également {#see-also}

{{see-also}}
