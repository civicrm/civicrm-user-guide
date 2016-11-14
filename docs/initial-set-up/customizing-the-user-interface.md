Personnalisation de l'interface utilisateur
==========================================

CiviCRM est très flexible et personnalisable. Ce chapitre donne des informations sur les nombreuses façons de modifier l'interface en fonction de vos besoins et de la rendre plus conviviable pour vos utilisateurs.

La façon de personnaliser vous-même vos données est traité dans *Organiser vos données* et dans les chapitres *Ce que vous devez savoir* et *Configurer* dans les sections des différents composants CiviCRM (exemple : La personnalisation des types d'événements dans la section *Evenements*).

Modifier les listes déroulantes
-------------------------------

Les options incluses dans les champs déroulants que vous voyez dans les formulaires de saisie/d'édition de contact dans CiviCRM peuvent être modifiées (vous pouvez ajouter, renommer, désactiver ou supprimer des options) dans **Administer> Personnaliser les données et les écrans> Listes déroulantes**. Ceci inclus:

-   Le sexe : Homme, Femme
-   Préfixe et suffixe individuel (exemple : Mme., Mr., Docteur, Me., et Jr., Sr.)
-   Type de téléphone (exemple : Téléphone, Mobile, Fax..)
-   Fournisseurs de téléphonie mobile (exemple : orange, SFR, Free,...)
-   Messagerie - Chat : (exemple: Yahoo, MSN, Skype, ... )
-   Type de site Web : (exemple : Personnel,Entreprise, Facebook, Linkedln, Twitter,...)
-   Type d'adresse : (exemple : Principale, domicile, Bureaux, Compta, Facturation,..). Notez que l'adresse de facturation est attribuée lorsque les membres contribuent ou paient les frais d'inscription et d'inscription en ligne. Le type d'adresse ne doit pas contenir d'espaces.(ex : "Résidence secondaire", n'est pas permis).

Les choix des Moyens de communication préférées (par exemple, Téléphone, Email, Courrier postal, SMS) dans le formulaire d'édition/saisie de contact peuvent également être modifiés. Allez à **Administrer> Communications> Méthodes de communication préférées**.

Les choix de Méthodes de communication préférées (par exemple, Téléphone, Email, Courrier postal, SMS) dans le formulaire d'édition / saisie de contact peut également être modifié.  Allez à **Administrer> Communications> Méthodes de communication préférées**.

La modification des options de liste déroulante qui définissent des données, telles que Type d'activité, Relations, etc., ne relève pas du champ d'application de ce chapitre. Voir *Organiser vos données* et les sections sur les différents composants CiviCRM.

Modification des préférences d'affichage
----------------------------------------

S'il existe des types d'activités ou des catégories de données que vous ne souhaitez pas utiliser, vous pouvez faire que ces champs et ces onglets ne s'affichent pas lorsque vos utilisateurs utilisent CiviCRM. Ce qui permet de faciliter la formation des utilisateurs et l'utilisation quotidienne. Pour cela allez à : **Administer > Personnaliser les données et écrans > Préférences d'affichage**.
Ensuite : **Informations à afficher** : vous pouvez modifier les onglets disponibles en cochant ou décochant les cases appropriées pour voir ce qui est nécessaire lorsque vous consulterez les enregistrements de contact.

![Display Preferences Viewing Contacts](../img/Viewing%20Contacts.png)

Par exemple, si votre organisation n'utilise pas les Dossiers ou les Subventions, vous pouvez les décocher. Ces onglets ne s'afficheront plus dans l'interface utilisateur. Si vous décidez plus tard de les utiliser, il suffit de ré-afficher l'onglet en cochant la case appropriée. Les informations stockées dans les onglets que vous masquez restent dans votre base de données. Vous pouvez masquer les onglets que vous avez déjà utilisés, et lorsque vous choisirez de les afficher à nouveau, toutes les informations s'afficheront comme auparavant.

Vous pouvez choisir les informations qui apparaitront sur les fiches de contact en cochant ou décochant les cases appropriées en regard de **Information éditables**:

![Display Preferences Editing Contacts](../img/Editing%20Contacts.png)

Par exemple, si votre organisation ne collecte pas d'informations démographiques ou de préférences de communication, vous pouvez les décocher pour rationaliser l'écran d'édition. Comme pour les préférences *informations à afficher*, toutes les informations contenues dans les champs que vous choisissez de ne pas afficher restent dans votre base de données et vous pouvez choisir de l'afficher à tout moment en cochant de nouveau les cases de ce paramètre.

### Désactiver les boites de dialogue (popup)

L'interface utilisateur CiviCRM fait un usage étendu des boîtes de dialogue contextuelles (popup) pour permettre une visualisation rapide et une édition facile des données. Vous pouvez désactiver cette fonctionnalité et limiter l'interface à la navigation traditionnelle en désélectionnant la case à cocher **Enable popup** dans **Administrer> Personnaliser les données et les écrans> Préférences d'affichage **. Notez que CiviCRM sera plus lent avec cette fonction désactivée car chaque formulaire nécessitera une charge de page complète dans le navigateur.

![Display Preferences Disabling Popup Forms](../img/Contact%20Dashboard.png)

Personnalisation des préférences de recherche
---------------------------------------------

Vous pouvez modifier le paramétrage de recherche par défaut de CiviCRM dans **Administer> Personnaliser les données et les écrans> Préférences de recherche**. Les options disponibles sont:

-   **Recherche aproximative** : (choisissez Oui ou Non): Si vous choisissez Oui, les caractères génériques sont automatiquement ajoutés au début ET à la fin du terme de recherche lorsque les utilisateurs recherchent des contacts par Nom. Par exemple, la recherche de "ada" renverra n'importe quel contact dont le nom inclut ces lettres: Adams, Janet; Nadal, Jorge; Etc. Si elle est désactivée, un caractère générique est ajouté, mais uniquement à la fin du terme de recherche. Dans ce cas, la recherche de "ada" renverra tout contact dont le nom de famille commence par ces lettres: Adams, Janet 'mais pas Nadal, Jorge.

-   **Inclure l'adresse électronique** : (Choisissez Oui ou Non): Si vous choisissez Oui, les adresses électroniques seront automatiquement incluses lorsque les utilisateurs effectueront une recherche par nom.

-   **Inclure le surnom** : (choisir Oui ou Non): Si vous choisissez Oui, le contenu du champ Surnom sera automatiquement inclus lorsque les utilisateurs effectueront une recherche par nom.

-   **Inclure une pagination alphabétique** : (choisissez Oui ou Non): Si vous choisissez Oui, une barre apparaît en haut de vos résultats de recherche vous permettant de choisir une lettre de l'alphabet. En cliquant sur A, par exemple, vous accédez à une page affichant uniquement les contacts commençant par A.

-   **Inclure la clause « order by »** (Choisissez Oui ou Non): Si vous choisisez NON, les résultats de recherche ne seront pas ordonnés.

-   **Délai d'attente de cache de groupe intelligent**: Détermine la fréquence à laquelle le cache de groupe intelligent est actualisé. Pour la plupart des sites cette valeur ne doit pas être définie à zéro, car cela signifie pas de mise en cache du tout et ralentira votre site. Même sur les sites où les données de contact changent fréquemment, la valeur minimale proposée est de 5 minutes.

-   **Expiration de la mémoire cache des groupes dynamiques**: Détermine la fréquence à laquelle le cache de groupe intelligent est actualisé. Pour la plupart des sites cette valeur ne doit pas être définie à zéro, car cela signifie pas de mise en cache du tout et ralentira votre site. Même sur les sites où les données de contact changent fréquemment, la valeur minimale proposée est de 5 minutes.

-   **Recherche de contacts avec autocomplétion**: Il s'agit d'une série de cases à cocher pour les champs de contact de base (nom, courriel, téléphone, etc.). Les champs cochés apparaissent dans la liste des résultats de la saisie semi-automatique qui s'affiche lorsque vous utilisez la barre de recherche rapide en haut à gauche de tous les écrans.

-   **Options référence à contact**: Il s'agit d'une série de cases à cocher pour les champs de contact de base (nom, courriel, téléphone, etc.). Les champs sélectionnés seront inclus dans les listes déroulantes de résultats de recherche pour les champs personnalisés de type référence contact. Le nom de contact est toujours inclus. Note: Vous devez assigner au rôle "public" la permission d'accès aux champs de référence contact si vous voulez utiliser des champs personnalisés de référence contact dans des profils sur des pages publiques. Dans la plupart des situations, vous devrez cocher le paramètre « Restreindre la liste au groupe » lorsque vous configurez un champ de référence contact qui est inclus dans des formulaires publics pour ne pas afficher la liste complète de vos contacts.

-  **Autocomplete Results**: Détermine le nombre maximal de résultats qui s'afficheront lors de la saisie d'un champ de saisie semi-automatique.

Si votre base de données est importante et que vos recherches sont lentes, envisagez de désactiver certaines de ces options pour augmenter votre vitesse.


Personnalisation des préférences de date
----------------------------------------
L'affichage par défaut des dates est définie sur **Administer> Localisation> Formats de date**.
Vous pouvez remplacer les paramètre par défaut et définir la plage de dates autorisées pour les types de champs spécifiques à :  **Administer> Données et écrans personnalisés> Préférences de date**

[](http://drupal.screenshots.civicrm.org/civicrm/admin/setting/preferences/date?action=reset=1)

Par défaut, CiviCRM fournit des fourchettes de date sur des champs de date spécifiques.

Par exemple, la fourchette par défaut pour les dates d'activité est 20 ans avant l'année en cours jusqu'à 10 ans au-delà de l'année en cours. Si vous souhaitez suivre les activités qui ont eu lieu, disons, il ya 25 ans, vous devez modifier le nombre d'années d'activités à consulter pour vos utilisateurs finaux.


Personnalisation du menu de navigation
--------------------------------------

Vous pouvez ajouter, supprimer, renommer et déplacer tous les éléments de menu dans la barre de navigation CiviCRM pour mieux répondre aux besoins de vos utilisateurs. Certaines choses que vous pourriez vouloir faire sont

You can add, delete, rename, and move all items in the CiviCRM navigation bar to better meet the needs of your users. Some things you might want to do are:

-   Rationaliser la navigation en supprimant les éléments de menu que vous n'utilisez pas
-   Ajouter des éléments pour prendre en charge des taches spécifiques (par exemple, saisie de données dans les profils )
-   Ajouter des liens vers des pages Web ou des applications autres que CiviCRM
-   Renommer les éléments du menu pour utiliser les termes habituels de vos utilisateurs
-   Déplacer les éléments du menu pour mieux organiser les flux de travail

Pour personnaliser les éléments de menu, allez dans **Administer> Personnaliser les données et les écrans> Menu Navigation**. Vous verrez une structure de fichier contenant tous vos éléments de menu, avec les éléments représentés par des icônes de dossier. Vous pouvez développer les dossiers en cliquant sur les petits triangles à gauche de leur nom :

-  Pour supprimer un élément, cliquez dessus avec le bouton droit de la souris et sélectionnez **Supprimer**.
-  Pour renommer un élément, cliquez dessus avec le bouton droit de la souris et sélectionnez **Renommer**.
-  Pour déplacer un élément, faites-le glisser vers l'emplacement souhaité dans l'arborescence.
-  Pour ajouter un élément de menu :
   -  1.  Cliquez sur le bouton **Ajouter élément de menu**.
   -  2.  Entrez le texte que vous souhaitez afficher dans le menu dans le champ **Titre**. 
   -  3.  Entrez le lien vers votre élément dans le champ **Url**.
   -  4.  Sélectionnez l'emplacement de votre nouvel élément dans le menu déroulant **Parent**. Vous pouvez placer l'élément n'importe où dans la navigation, à n'importe quel niveau. Si vous souhaitez que votre nouvel élément soit au niveau supérieur de la navigation, ne sélectionnez rien dans cette liste déroulante. 
    - 5.  Cochez la case **Séparateur** si vous souhaitez ajouter une ligne au-dessous de votre nouvel élément pour le séparer de l'élément suivant.

Création de formulaires de saisie personnalisés
-----------------------------------------------

Si vous avez du personnel ou des bénévoles qui saisissent souvent manuellement des types de contacts similaires , vous pouvez créer un outil appelé "profil" avec seulement les champs dont ils ont besoin. Cela peut accélérer considérablement l'enregistrement des données.

1.  Allez dans **Administer> Personnaliser les données et les écrans> Profils** et cliquez sur **Ajouter un profil**.
2.  Donnez à votre profil un nom clair qui se rapporte à son objet (par exemple, Saisie du nom et d'adresse de bénévoles)

3.  Cochez la case Formulaire autonome ou Répertoire dans le champ **Utilisé pour**.
4.  Utilisez les champs **Aide avant le formulaire** et **Aide aprés le formulaire** pour ajouter le texte que vous souhaitez afficher au formulaire lors de la saisie des données.
5.  Cliquez sur **Enregistre **  pour accéder à l'écran **Ajouter des champs** afin que vous puissiez choisir les champs à mettre dans votre profil.
6.  Dans le champ déroulant **Nom de champ**, sélectionnez le type d'enregistrement de contact où se trouve votre champ recherché. Ce contact sera "individuel, organisation, ménage", ou tout sous-types de contact personnalisé que vous avez peut-être créé. (Les autres types d'enregistrements disponibles dans ce champ ne fonctionneront pas avec les formulaires de saisie des données. Il ne faut donc pas les choisir.) Il est important de noter que tout champ s'appliquant à plus d'un type d'enregistrement de contact (tel que téléphone ou Email, pour les personnes et les organisations) se trouvent dans le menu Contacts.      
7. Une fois que vous avez choisi un type de contact, un autre champ déroulant apparaîtra à droite avec la liste des champs disponibles. Choisissez le champ que vous désirez. 
8.  Si le texte qui apparaît automatiquement dans le champ **Nom de champ** n'est pas ce que vous souhaitez afficher sur le formulaire, vous pouvez en choisir un autre.  
9.  Si les enregistrements saisis dans ce champ doivent obligatoirement contenir des données alors cochez la case **Obligatoire?**.


10. Use the **Field Pre Help** and **Field Post Help** fields to add any
    text you'd like to display to those doing data entry.
11. You can use the **Order** field to change the order in which fields
    are displayed on the form. Lower numbers are displayed ahead of
    higher numbers.
12. Click on **Save and New** to add more fields, and **Save** when are
    finished.
13. You'll be taken to a screen listing all your fields and their
    settings. Click **Preview (all fields)** to make sure your form
    looks the way you want it to. Click **Use (create mode)** to go to
    the page containing your form. Copy the link and use it to create a
    navigation menu item (see the previous section for instructions).

Customizing search views
------------------------

To do this:

1.  Create or open a profile and mark it as used for Search Views (known
    as Search Results in 4.1 and previous):
2.  When adding fields to this profile, you will need to set Visibility
    for the fields to Public Pages and check the Results Column box.

When conducting your advanced search, use the **Search Views** dropdown
menu in the top right of the page to select your Profile (see image
below).

![Customize Search Views](../img/configure-customize-search-views.png)

Using Word Replacement to change terminology
----------------------------------------------

CiviCRM has a Word Replacement setting that lets you replace existing
text found in the system with your desired text. For example, if your
organization does not typically refer to monetary transactions as
"contributions," but prefers to use the term "donations," you can define
a word replacement and have it automatically altered throughout your
instance of CiviCRM.

To use Word Replacement:

1.  Go to **Administer > Customize Data and Screens > Word
    Replacements**.
2.  Enter the original text in the Original column on the left, and the
    replacement text in the Replacement column on the right.
3.  Check the Exact Match box on the right to replace only instances of
    the word or phrase that match exactly. For example, if Exact Match
    is not checked checked, replacing "Contribution" with "Donation"
    would also replace "Contributions" with "Donations"; if it is
    checked, this would not happen.
4.  Check the Enabled box to the left to replacement of the word or
    phrase.
5.  You can add additional rows using the **Add row** button.
6.  Click **Save** when you are finished entering replacements.

When using this function, be sure to anticipate alternate forms of words
and different ways your chosen word or phrase may appear in CiviCRM.
