Personalisation de l'interface utilisateur
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
-   Type d'adresse : (exemple : Principale, domicile, Bureaux, Compta, Facturation,..). Notez que l'adresse de facturation est attribuée lorsque les membres contribuent ou paient les frais d'inscription et d'inscription en ligne.Le type d'adresse ne doit pas contenir d'espaces.(ex : "Résidence secondaire", n'est pas permis).

Les choix des Moyens de communication préférées (par exemple, Téléphone, Email, Courrier postal, SMS) dans le formulaire d'édition/saisie de contact peuvent également être modifiés. Allez à **Administrer> Communications> Méthodes de communication préférées**.

Les choix de Méthodes de communication préférées (par exemple, Téléphone, Email, Courrier postal, SMS) dans le formulaire d'édition / saisie de contact peuvent également être modifiés; Allez à **Administrer> Communications> Méthodes de communication préférées**.

La modification des options de liste déroulante qui définissent des données, telles que Type d'activité, Relations, etc., ne relèvent pas du champ d'application de ce chapitre. Voir *Organiser vos données* et les sections sur les différents composants CiviCRM.

Modification des préférences d'affichage
----------------------------------------

S'il existe des types d'activités ou des catégories de données que vous ne souhaitez pas utiliser, vous pouvez faire que ces champs et ces onglets ne s'affichent pas lorsque vos utilisateurs utilisent CiviCRM. Ce qui permet de faciliter la formation des utilisateurs et l'utilisation quotidienne. Pour cela allez à : **Administer > Personnaliser les données et écrans > Préférences d'affichage**.
Ensuite : **Informations à afficher** : vous pouvez modifier les onglets disponibles en cochant et en désélectionnant les cases appropriées pour voir ce que vous désirez lorsque vous consulterez les enregistrements de contact.

You can change which tabs are available when you are viewing contact records by checking and un-checking the appropriate boxes next to **Viewing Contacts**.

![Display Preferences Viewing Contacts](../img/Viewing%20Contacts.png)

Par exemple, si votre organisation n'utilise pas les Dossiers ou les Subventions, vous pouvez les décocher. Ces onglets ne s'afficheront plus dans l'interface utilisateur. Si vous décidez plus tard de les utiliser, il suffit de ré-afficher l'onglet en cochant la case appropriée. Les informations stockées dans les onglets que vous masquez restent dans votre base de données. Vous pouvez masquer les onglets que vous avez déjà utilisés, et lorsque vous choisirez de les afficher à nouveau, toutes les informations s'afficheront comme auparavant.

Vous pouvez choisir les informations qui apparaitront sur les fiches de contact en cochant ou décochant les cases appropriées en regard de ** Modification des contacts **:

You can change which blocks of information appear when you are editing a contact by checking and unchecking the appropriate boxes next to **Editing Contacts**:

![Display Preferences Editing Contacts](../img/Editing%20Contacts.png)

For example, if your organization doesn't collect information
Demographics or Communication Preferences, you could uncheck those boxes
to streamline the editing screen. As with the Viewing Contacts
preferences, any information contained in fields you choose not to
display remains in your database, and you can choose to display it again
at any time by re-checking the boxes in this setting.

### Disabling Popup Forms

The CiviCRM user-interface makes extensive use of popup dialog boxes to
enable quick viewing and easy editing of data. You can disable this
feature and limit the interface to traditional browsing by deselecting
the checkbox **Enable Popup Forms** in **administer > customize data and
screens > display preferences**. Note that CiviCRM will be slower with
this feature disabled as every form will require a complete page load in
the browser.

![Display Preferences Disabling Popup Forms](../img/Contact%20Dashboard.png)

Customizing search preferences
------------------------------

You can change CiviCRM's default search behavior at **Administer >
Customize Data and Screens > Search Preferences**. Available options
are:

-   **Automatic Wildcard** (choose Yes or No): If you choose Yes,
    wildcards are automatically added to the beginning AND end of the
    search term when users search for contacts by Name. For example,
    searching for "ada" will return any contact whose name includes
    those letters: Adams, Janet; Nadal, Jorge; etc. If disabled, a
    wildcard is still added, but only to the end of the search term. In
    this case, searching for "ada" will return any contact whose last
    name begins with those letters: Adams, Janet' but not Nadal, Jorge.
-   **Include Email** (choose Yes or No): If you choose Yes, email
    addresses will be automatically included when users search by Name.
-   **Include Nickname** (choose Yes or No): If you choose Yes, contents
    of the Nickname field will be automatically included when users
    search by Name.
-   **Include Alphabetical Pager** (choose Yes or No): If you choose
    Yes, a bar will appear at the top of your search results allowing
    you to choose a letter of the alphabet. Clicking A, for example,
    will take you to a page displaying only contacts that begin with A.

-   **Include Order By Clause** (choose Yes or No): If you choose No,
    your search results will not be ordered.
-   **Smart group cache timeout**: This determines how often the smart group cache is refreshed. For most sites this value should not be set to zero, since that means no caching at all and will slow down your site.  Even on sites where contact data changes frequently, the suggested minimum value is 5 minutes.
-   **Autocomplete Contact Search**: This is a series of checkboxes for
    basic contact fields (name, email, phone, etc). The fields that are
    checked will show up in the autocomplete results list that appears
    when you use the Quick Search bar at the top left of all screens.
-   **Contact Reference Options**: This is a series of checkboxes for basic contact fields (name, email, phone, etc). The fields that are checked will show up in the autocomplete dropdown search results for 'Contact Reference' custom fields.
-   **Autocomplete Results**: This determines the maximum number of results that will be displayed when typing in an autocomplete field.

If your database is large and your searches are slow, consider disabling
some of these options to increase your speed.

There is one more place to customize search search settings:
**Administer > Customize Data and Screens > Display Preferences** has
a block of **Contact Search** settings:

![Display Preferences Contact Search](../img/Contact%20Search.png)

These check boxes modify the **Search > Find Contacts** and **Search >
Advanced Search** screens. Uncheck the boxes to remove the corresponding
types of fields from your search screens.

Customizing date preferences
----------------------------

The default display preference for dates is set at **Administer >
Localization > Date Formats**.

You can override this default setting and define the range of allowed
dates for specific field types at **Administer > Customise Data and
Screens > Date
Preferences[](http://drupal.screenshots.civicrm.org/civicrm/admin/setting/preferences/date?action=reset=1)**.
By default, CiviCRM provides ranges for input on specific date fields.
For instance, the default range for Activity Dates are 20 years prior to
the current year all the way through to 10 years beyond the current
year. If you would like to track activities that have occurred, say, 25
years ago then you would need to update this range to enable your end
users to log these activities.

Customizing the navigation menu
-------------------------------

You can add, delete, rename, and move all items in the CiviCRM
navigation bar to better meet the needs of your users. Some things you
might want to do are:

-   Streamline the navigation by removing menu items you don't use
-   Add items to support specific workflows (e.g. data entry Profiles)
-   Add links to non-CiviCRM web pages or apps
-   Rename menu items to use terms for familiar to your users
-   Move menu items to better support the flow of your work

To customize menu items, go to **Administer > Customize Data and
Screens > Navigation Menu**. You will see a file structure containing
all of your menu items, with the items represented by folder icons.
Expand folders by clicking the small triangles to the left of their
names.

-  To delete an item, right-click it and select **Delete**.
-  To rename an item, right-click it and select **Rename**.
-  To move an item, drag and drop it to the desired location in the tree structure.
-  To add an item:
 1.  Click on the **Add Menu Item** button.
 2.  Enter the text you want to appear in the menu in the **Title**
    field.
 3.  Enter the link to your item in the **Url** field.
 4.  Select the location of your new item from the **Parent** dropdown
    menu. You can place the item anywhere in the navigation, at any
    level. If you want your new item to be in the top level of the
    navigation, do not select anything from this dropdown.
 5.  Check the **Separator** box if you want to add a line below your new
    item to separate it form the item below.

Making custom data entry forms
------------------------------

If you have staff or volunteers who are often entering batches of
similar contacts manually, you can create a tool called a Profile with
only the fields they need. This can speed up data entry considerably.

1.  Go to **Administer > Customize Data and Screens > Profiles**and
    click**Add Profile**.
2.  Give your Profile a clear name that relates to its purpose (e.g.,
    Name and Address Data Entry Form)
3.  Check the Standalone Form or Directory box in the **Used For**
    field.
4.  Use the **Pre-form Help** and **Post-form Help** fields to add any
    text you'd like to display to hose doing data entry.
5.  Click **Save**; this takes you to the Add Fields screen so you can
    choose which fields to put in your Profile.
6.  From the **Field Name** dropdown menu, select the contact record
    type where your desired field is found. This will be Contact,
    Individual, Organization, Household, or any custom contact subtypes
    you may have created. (The other record types available on this menu
    will not work with data entry forms, so do not choose them.) It's
    important to note that any field applying to more than one kind of
    contact record type (such as Phone or Email, which applies to both
    Individuals and Organizations) will be found on the Contacts menu.
7.  Once you have chosen a contact type, another dropdown menu will
    appear listing the available fields. Choose your desired fields.
8.  If the text that appears automatically in the **Field Label** field
    is not what you would like to appear on the form, edit it.
9.  If every record entered through this form must have data in this
    field, check the **Required?** box.
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
