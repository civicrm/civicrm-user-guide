Installation et configuration de base
=====================================

Avant d'aller plus loin, n'oubliez pas que la plupart des informations contenues ici sont destinées aux techniciens et peuvent être difficiles à comprendre si vous avez peu ou pas d'expérience dans la configuration d'applications Web. Si vous ne comprenez pas ce sujet, vous pouvez demander de l'aide sur nos forums ou faire intervenir les personnes compétentes de votre organisation.

Prérequis 
---------

Avant d'explorer l'installation de CiviCRM, assurez-vous d'avoir lu le chapitre 'hébergement' pour vérifier que votre hébergeur puisse le supporter.

CiviCRM doit être installé sur un ordinateur configuré avec un serveur Web (tel que Apache ou ngnx), PHP et MySQL. Certaines personnes préfèrent tester CiviCRM sur leur propre ordinateur local avant de l'installer sur un serveur web dédié. Si vous n'avez pas les préalables ci-dessus sur votre ordianteur, vous pouvez télécharger des plateformes de développement Web telles que WAMP, XAMPP, MAMPP et LAMP, qui installeront rapidement un serveur Web Apache, PHP et MySQL. (Les deux premières sont pour Windows et les deux autres pour Macintosh et Linux respectivement).

Avant de pouvoir commencer l'installation, vous devez décider quel système de gestion de contenu (CMS) vous souhaitez intégrer pour construire et gérer votre site : Choisir entre les options open-source: Drupal, Joomla ou Wordpress!.

Vous trouverez des instructions complètes sur l'installation de CiviCRM ici : [
http://wiki.civicrm.org/confluence/display/CRMDOC/Installation+and+Upgrades](http://wiki.civicrm.org/confluence/display/CRMDOC/Installation+and+Upgrades%20)[](http://wiki.civicrm.org/confluence/display/CRMDOC/Installation+and+Upgrades%20)

Intallation locale ou Internet ?
--------------------------------

La plupart des organisations accèdent à CiviCRM via Internet. Toutefois certaines organisations, qui souhaitent uniquement que le personnel interne ait accès à CiviCRM et veulent préserver la sécurité des données, choisissent d'installer CiviCRM sur un réseau local et de le rendre accessible uniquement en interne. L'inconvénient d'une telle installation, qui n'est pas accessible au public, est que vos contacts ne peuvent pas s'inscrire directement à vos manifestations et n'ont pas accès à leurs données pour mise à jour.

Mises à jour
------------

Les nouvelles versions de CiviCRM sont diffusées environ deux fois par an (une au printemps et une en automne).
Vous devrez appliquer les mises à jour à votre site CiviCRM régulièrement si vous souhaitez profiter des nouvelles fonctionnalités et des améliorations, et aussi pour maintenir votre site sécurisé. Certaines mises à niveau contiennent des correctifs de sécurité et il est crucial que ces dernières soient appliquées immédiatement. Il est important que vous planifiez des ressources (personnes et temps) pour appliquer les mises à niveau à votre site. Vous pouvez executer, par prudence, les mises à niveau sur une copie de votre site en production pour s'assurer que le processus fonctionne correctement. Il est  essentiel de faire une sauvegarde de votre site et de votre base de données avant d'exécuter une mise à niveau, même si vous aviez testé le processus sur un site de test..

Les mises à jour sont un processus important. De nombreuses organisations emploient les services de professionnels agréés par CIVICRM pour les réaliser.


Configuration
-------------

Une fois CiviCRM installé, vous devez personnaliser CiviCRM et paramétrer la configuration de votre site : 

Connectez-vous à votre site CiviCRM et accédez à **Administer> Console d'administration> Checklist de configuration**. Cette section permet de paramétrer les tâches générales, tandis que la configuration spécifique aux composants sera effectuée dans chaque section de composant.

Utilisez cette liste de contrôle pour paramétrer et enregistrer les tâches de configuration de votre site. Vous serez redirigé vers cette liste après avoir enregistré chaque paramètre. Les paramètres que vous n'avez pas encore initialisés s'affichent en rouge. Après avoir visité une page, les liens s'affichent en vert (mais vous aurez peut-être besoin revenir sur une section afin de completer ou mettre à jour les paramètres, vous pourrez le faire plus tard).

![image](../img/checklist-de-config-4-4.PNG )

### Localization

La localisation implique l'adaptation de CiviCRM pour une utilisation dans un pays ou une langue spécifique en traduisant le texte affiché à l'écran et en définissant des formats régionaux spécifiques pour les dates et la monnaie. Par défaut, CiviCRM est initialisé pour les États-Unis. Si vous utilisez CiviCRM dans un pays différent, vous devez paramétrer et mettre à jour les valeurs sur cet écran. 

CiviCRM a été traduit dans de nombreuses langues différentes et les traductions sont incluses lorsque vous téléchargez CiviCRM. Ces traductions sont fournies par les membres de la communauté. Si CiviCRM n'est pas disponible dans votre langue, vous pouvez envisager de le traduire. Vous trouverez un guide de traduction sur le wiki.

Vous pouvez aussi configurer votre site pour prendre en charge plusieurs langues. Dans ce mode, vos utilisateurs pourront choisir parmi une liste de langues disponibles après leur connexion. Vous pouvez également créer et stocker des versions multilingues de texte. Les exemples comprennent des étiquettes de champs personnalisées, une page de contribution en ligne, des informations sur les campagnes et des descriptions d'événements.

Pour plus d'info, consulter:
[http://wiki.civicrm.org/confluence/pages/viewpage.action?pageId=88408149](http://wiki.civicrm.org/confluence/pages/viewpage.action?pageId=88408149)

Sous Localisation, vous trouverez également les **Paramètres d'entrée de date**.

, CiviCRM fournit par défaut des intervalles pour l'entrée sur des champs de date spécifiques. Par exemple, la fourchette par défaut pour les dates d'activité est 20 ans avant l'année en cours jusqu'à 10 ans au-delà de l'année en cours. Si vous souhaitez suivre les activités qui ont eu lieu, disons, il ya 25 ans, vous devriez mettre à jour cette option pour permettre à vos utilisateurs finaux de consigner ces activités. Pour mettre à jour ces paramètres dans la plage appropriée, allez dans **Administer> Personnalisez les données> Dates Préférences**. Si vous deviez laisser ces paramètres par défaut, vous verrez ce  message d'erreur: 
*By default, CiviCRM provides ranges for input on specific date fields. For instance, the default range for Activity Dates are 20 years prior to the current year all the way through to 10 years beyond the current year. If you would like to track activities that have occurred, say, 25 years ago then you would need to update this range to enable your end users to log these activities.*
Pour mettre à jour ces paramétrages, menu : **Administer> Personnalisez les données> Dates Préférences**.

![Advanced Date Input Settings](../img/configure-localization-advanced-date-input-settings.png)

### Adresse et coordonnées de votre organisation

Utilisez cet écran pour saisir les informations d'identification pour l'organisation ou l'entité qui «est propriétaire» de cette installation CiviCRM. Le nom et l'adresse de l'organisation sont utilisés pour identifier votre organisation dans les envois CiviMail lorsque vous incluez les jetons domain.name et domain.address.

Vous devez également saisir une adresse e-mail valide appartenant à votre organisation, qui sera utilisée comme champ "De" dans les courriels simples ou automatisés générés par le système.

### Activer les composants

C'est ici que vous pouvez activer ou désactiver les composants pour votre système CiviCRM.

Lorsque vous installez CiviCRM pour la première fois, les composants les plus utilisés (CiviContribute, CiviEvent, CiviMail, CiviMember, CiviReport) sont déjà activés. Si vous n'avez pas besoin de ces composants, vous pouvez les désactiver. Vous pouvez également activer tout ou partie de CiviCampaign, CiviCase, CiviGrant et CiviPledge. Vous pouvez modifier cette page à tout moment pour activer ou desactiver les composants.

Vous pouvez désactiver un composant que vous avez déjà utilisé. Les données et informations contenues dans le composant sont conservées et seront toujours là si vous le réactivez. Il serait inhabituel de désactiver un composant que vous avez déjà utilisé. Si vous souhaitez simplifier le menu d'administration et la page de recherche avancée, une meilleure approche peut consister à utiliser les autorisations (voir le chapitre Autorisations et contrôle d'accès).

### Préférences d'affichage
Cet écran vous permet de modifier l'affichage des éléments à l'écran et les formulaire pour les tâches suivantes:


-   **Affichage des contacts**  - Contrôle les onglets affichés lors de l'affichage d'un enregistrement de contact. EXEMPLE:   Si votre organisation ne suit pas les relations entre les contacts, désélectionnez cette option pour simplifier l'affichage à l'écran. Les onglets des contributions, annonces de contributions, adhésions, événements, subventions et cas sont également masqués si le composant correspondant n'est pas activé.
-   **Affichage des Groupes intelligents** - Contrôle l'affichage des groupes intelligents auxquels un contact appartient.
-   **Modification des contacts** - Contrôle les sections incluses lors de l'ajout ou de l'édition d'un enregistrement de contact. EXEMPLE: Si votre organisation ne gére pas le sexe ni la date de naissance des individus, simplifiez le formulaire en désélectionnant les données démographiques.
-   **Recherche de contacts** - Contrôle les sections comprises dans le formulaire Recherche avancée. EXEMPLE: Si vous ne suivez pas les relations, vous ne chercherez pas cette section. Simplifiez le formulaire en désélectionnant cette option.
-  - **tableau de bord de contact** - Permet à vos contacts de voir les groupes auxquels ils sont abonnés, leur historique de contribution, les informations d'inscription à un événement... et plus encore. Vous pouvez contrôler les sections qui doivent être incluses dans le tableau de bord ici. EXEMPLE: Si vous ne voulez pas que les électeurs voient leur propre historique de contribution, désélectionnez cette option.
-  **Editeur WYSIWYG** - Sélectionnez **CKEditor** pour que les utilisateurs disposent d'un moyen simple d'entrer du texte dans des champs qui permettent le formatage HTML (comme par exemple la section d'introduction de vos pages de contribution en ligne). Vous pouvez configurer CKEditor (voir http://ckeditor.com/) comme vous le souhaitez pour ajouter ou supprimer des fonctionnalités. Sélectionnez **Zone de texte** si vous ne souhaitez pas fournir d'éditeur WYSIWYG.
-  ** Activer les formulaires Popup** - cette option est activée par défaut. Décochez pour revenir à l'ouverture du formulaire en rafraîchissant la page.
-  **Affichage du nom individuel** - Format d'affichage du nom des noms d'affichage des contacts individuels.
-  **Nom de classement individuel** - Format de nom de tri pour les noms de tri des contacts individuels.


### Address Settings

At **Localization > Address Settings** CiviCRM allows you to modify the default fields for adding and editing
contact and event address data. You can also change the address field
layout used for screen display and mailing labels. Review the
out-of-the-box defaults by adding a new contact record and noting the
address fields provided on the form. Save the record and note the order
in which the fields are displayed on the Contact Summary screen. If you
plan on generating mailing labels for contacts, review the label layout
(select Mailing Labels from the *-actions-* drop-down after doing a
search using the Find Contacts menu option).

After reviewing the default fields and layouts, review the Address
Settings screen and make changes as needed.

-   **Mailing Labels** - Controls formatting of mailing labels here. The
    default format is:

    *{contact.addressee}
    {contact.street_address}
    {contact.supplemental_address_1}
    {contact.supplemental_address_2}
    {contact.city}{, }{contact.state_province}{ }{contact.postal_code}
    {contact.country}*  

  You must include the *{contact.addressee}* token here in order to
    include the name of the addressee in your labels. Users will be able
    to select from a variety of label types corresponding to the label
    manufacturer code when they generate the labels from a list of
    contacts. It's a good idea to test your format with the type of
    label and printer you plan on using to verify spacing.
-   **Address Display** - Controls the layout of contact and event
    location addresses displayed on CiviCRM screens. The default format
    is:

    *{contact.address_name}
    {contact.street_address}
    {contact.supplemental_address_1}
    {contact.supplemental_address_2}
    {contact.city}{, }{contact.state_province}{ }{contact.postal_code}
    {contact.country}*

    This format also applies to event locations, despite the use of the
    *contact* record type in the layout. The *{contact.address_name}*
    token is particularly useful for events where you need to include a
    location name (e.g. "Smithson Hall").

-   **Address Editing Fields** - Modify the available address
    editing fields here. You can hide fields that you don't plan on
    using in order to simplify the forms. EXAMPLE: If you don't plan on
    recording latitude and longitude for contacts, you can deselect
    those field.
    -   **Street Address Parsing**- CiviCRM uses the US Postal Service's
        (USPS) Postal Addressing Standards to parse an address into
        fields to hold the address elements: Street Number, Street Name,
        and Apt/Unit/Suite. It's best to enter address information
        that conforms to the Postal Addressing Standards, not only for
        consistency in your data, but also to best take advantage of the
        the Street Address Parsing function. When address parsing is turned on you can edit and or view
        the parsed address by clicking on Edit Address Elements when you are editing a address.

    ![Configuration Address Parsing](../img/basic-set-up-address-parsing.png)  

   You can learn more about USPS' Postal Addressing Standards at          [http://pe.usps.com/text/pub28/welcome.htm](http://pe.usps.com/text/pub28/welcome.htm).
-   **Address Standardization** - CiviCRM includes an optional feature
    for interfacing to the United States Postal Services (USPS) Address
    Standardization web service. You must register to use the USPS
    service at
    [https://www.usps.com/business/web-tools-apis/welcome.htm](https://www.usps.com/business/web-tools-apis/welcome.htm).
    If you are approved, they will provide you with a User ID and the
    URL for the service. The URL provided by USPS will not be prefixed
    with "http://". When entering this URL into the CiviCRM settings
    field, you must prefix it with "http://".

### Mapping and Geocoding

CiviCRM includes support for both the Google and OpenStreetMap mapping
services. These services allow your users to display contact addresses
and event locations on a map. To enable this feature, select your
mapping provider and obtain a key for your site from that provider.

You can also select a Geocoding Provider. This can be that same or
different form you mapping provider. Once this service is enabled, your
contact and event records will be automatically geocoded (the latitude
and longitude for that address is inserted) as you add or edit address
data.

### Search Settings

These let you adjust search behaviors such as the use of wildcards and
which data to include in quick search results. Adjusting search settings
can improve performance for large datasets.

A wildcard character is a special character that can be used to
substitute for any other character or characters in searches. CiviCRM
allows you to use the percent character "%" to substitute for zero or
more characters, and the underscore character "_" to substitute for any
single character. Wildcards are useful for broadening your search
results.

For example, typing 'Volunteer%' as your Activity Subject will match any
record whose subject starts with "Volunteer" (e.g. "Volunteer for Open
House" or "Volunteering Opportunities").

-   **Automatic Wildcards** - By default, when users search for contacts
    by Name, the Search interface treats the text as if it was
    surrounded by percent signes. EXAMPLE: Searching for 'ada' will
    return any contact whose name includes those letters - 'Adams,
    Janet', 'Nadal, Jorge', etc. Disabling this feature will speed up
    searches significantly for large databases, but will make users
    explicitly use wildcard characters ("%" or "_") for partial name
    searches.
-   **Include Email** - By default, when users search contacts by Name,
    the Search interface also searches for the text in email addresses.
    Disabling this feature will speed up searches significantly for
    large databases, but users will need to use the Email search fields
    (from Advanced Search, Search Builder, or Profiles) to find contacts
    by email address.
-   **Include Nickname** - By default, nicknames are automatically *not*
    included when users search by Name. Change this value to Yes if you
    want nicknames to be included.
-   **Include Alphabetical Pager** - If disabled, the alphabetical pager
    will not be displayed on the search screens. This will improve
    response time for search results on large datasets.
-   **Include Order By Clause**- If disabled, search results will not be
    ordered. This will improve response time for search results on large
    datasets significantly.
-   **Default Contact Search Profile** - You can select a Profile to
    override the columns displayed by default in Find Contacts search
    results.
-   **Smart group cache timeout** - Smart groups are basically saved
    searches. The list of contacts for each smart group is cached in the
    database in order to avoid running the saved search every time you
    access a smart group. This field determines the number of minutes to
    maintain the cache before refreshing it. The default value of 0
    means the cache is emptied immediately when any contact is edited or
    a new one is added. If your contact data changes frequently, you may
    want to try setting this to a value of 5 minutes (or even longer) to
    reduce processing load on your server. The drawback of delaying the
    refreshing of the cache is that old data will still be served up to
    users for a few minutes after new data is added.
-   **Autocomplete Contact Search** - If enabled, selected fields will
    be displayed in auto-complete dropdown lists and the "Quick Search"
    box on the navigation menu. The contact name is always included.
-   **Contact Reference Options** - Selected fields will be displayed in
    autocomplete dropdown search results for 'Contact Reference' custom
    fields. Contact Name is always included. Note: You must assign
    'access contact reference fields' permission to the anonymous role
    if you want to use custom contact reference fields in profiles on
    public pages. For most situations, you should use the 'Limit List to
    Group' setting when configuring a contact reference field which will
    be used in public forms to prevent exposing your entire contact
    list.
-   **Autocomplete Results**- This specifies the maximum number of
    contacts to show at a time when typing in an autocomplete field. The
    default is 10.
-   **InnoDB Full Text Search -** If you are using MySQL 5.6+ you can
    enable InnoDB full-text search optimizations.

### Miscellaneous (Undelete, PDFs, Limts, Logging, reCAPTCHA, etc.)

Use the Miscellaneous Settings screen to configure and control the
following behaviors:

-   **Dashboard Cache Timeout -** The number of minutes to cache dashlet
    content on the dashboard.

-   **Checksum Lifespan -** The number of days before a personalized
    (hashed) link will expire.

-   **Contact Trash and Undelete** - If enabled, deleted contacts will
    be moved to the trash (instead of being destroyed). Users with the
    proper permission are able to search for the deleted contacts and
    restore them (or delete them permanently).
-   **Logging** - If enabled, all actions performed on non-cache tables
    will be logged (in the respective log_\* tables). By default, these
    tables will be created in the same database. However you can
    configure CiviCRM to write logging tables to a different database by
    editing your site's *civicrm.settings.php* file. Specify
    the separate logging database in the CIVICRM_LOGGING_DSN setting.
    After enabling this feature you can review changes to contact
    records using the Contact Logging Report. Go to **Reports > Reports
    Listing > Contact Logging Report (Summary)**.
-   **Attach PDF copy to receipts** - If enabled, CiviCRM sends PDF
    receipt as an attachment during event signup or online contribution.
-   **Path to wkhtmltopdf executable -** wkhtmltopdf is an alternative
    utility for generating PDF's which may provide better performance
    especially if you are generating a large number of PDF letters or
    receipts. Your system administrator will need to download and
    install this utility, and enter the executable path here.
-   **New Version Alerts** - If enabled on-screen alerts will be
    displayed to users with "Administer CiviCRM" permissions when a new
    version of CiviCRM is available. This setting will only work if the
    "Version Check & Statistics Reporting" setting is enabled.
-   **Version Checking and Statistics Reporting** -This feature
    automatically checks the availability of a newer stable version of
    CiviCRM. New version alerts are displayed on the main CiviCRM
    Administration page. Statistics about your CiviCRM installation are
    also reported anonymously to the CiviCRM team to assist in
    prioritizing ongoing development efforts. The following information
    is gathered: CiviCRM version, versions of PHP, MySQL and framework
    (Drupal/Joomla!/Wordpress), and default language. Record counts (but
    no actual data) are also reported. You can set this field to No if
    you are not comfortable with having this information reported for
    your site.
-   **Display "empowered by CiviCRM** - When enabled, "empowered by
    CiviCRM" is displayed at the bottom of public forms. This will help
    increase awareness of CiviCRM.
-   **Maximum Attachments** - You can increase or decrease the maximum
    number of files (documents, images, etc.) that can be attached to
    emails, activities, and grant records. The default value is 3.
-   **Maximum File Size (in MB)** - Maximum size of a file (documents,
    images, etc.) which can attached to emails or activities. Note that
    your PHP configuration files, *php.ini*, should support at least as
    big a file size as the value specified here.
-   **Allow second-degree relationship permissions -** If enabled,
    contacts with the permission to edit a related contact will inherit
    that contact's permission to edit other related contacts. This can
    be used, for example, to let the teacher of a class edited the
    records for students in that class when they are both linked to the
    class (set up as an organisation sub-type) via relationships.
-   **reCAPTCHA** - reCAPTCHA is a free service that helps prevent
    automated abuse of your site by requiring users to read a random
    pair of words and type them into the form. To use reCAPTCHA on
    public-facing CiviCRM forms, sign up at
    [recaptcha.net](http://recaptcha.net/), enter the provided public
    and private reCAPTCHA keys here, then enable reCAPTCHA under the
    Advanced Settings section in a Profile where you want it used.

    If you want to use reCAPTCHA protection for online contribution,
    membership signup or event registration forms, you'll need to
    configure a Profile with reCAPTCHA enabled, and then include it in
    those forms.

### Contact Types

You can modify the names of the built in Contact Types (Individual,
Household, Organizations), and you can create and modify "contact
subtypes" for more specific uses (e.g. Student, Parent, Team, etc..)

### Outbound email

If you are sending emails to contacts using CiviCRM, you need to enter
settings which allow CiviCRM to connect to your mail server. Such emails
include sending receipts to contributors, sending confirmations to
people registering for events, and using CiviMail to send bulk mailings.

CiviCRM supports three different methods of connecting to a mail server:
mail (the built-in PHP mail function); SMTP (Simple Mail Transport
Protocol); and Sendmail. Each method requires that you enter specific
settings. If you're unfamiliar with these terms, or unsure of the
correct values for these settings, check with your system administrator,
ISP or hosting provider.

You should always send a test email after you enter or modify the
settings. Simply click "Save and Send Test Email"(shown in the following
screenshot). An email will be sent to the email address associated with
your user login account. The From email address will be the default From
address you've configured in the previous section.

![Picture_11](../img/CiviCRM-Configuring-Picture_11-en.png "Save and Send Test Email")

If CiviCRM is unable to send the test email, you will see a message on
your screen with the specific error and some suggestions for
trouble-shooting the problem.

### Disabling outbound email

If you do *not* want users to send outbound emails from CiviCRM at all,
select "Disable Outbound Email". However, if you disable outbound email,
and you are using Online Contribution pages or online Event
Registration, you will need to turn off the automated receipting and
registration confirmation features (these are enabled by default).
Otherwise your constituents will see error messages after they've
completed a contribution or registration.

**Redirect to Database**- If this option is selected, all emails will be
recorded as archived mailings instead of being sent out.

See **Email System Configuration** for more details.

### From Email Addresses

CiviCRM will use the default From address defined here when sending
automated emails. If you've already entered an email address in the
Domain Information screen, that address will be listed here (as
illustrated on the leftmost field of the following screenshot).

![image](../img/From%20email.PNG)

When users send an email using CiviCRM, their primary email address is
used as the From address by default. However, they can also select one
of the general email addresses defined here as an alternative.

### Payment Processors

Payment processors are companies that handle credit card transactions
for merchants and non-profit organizations and then transfer funds to
the organization's bank account. If you plan on using CiviCRM to accept
online contributions, online membership signup and renewal or online
event registration, you will need to select and configure a payment
processor for your site.

CiviCRM includes support for several different processors, and provides
a way for third-party developers to add support for additional
processors based on their clients' needs. Each processor has their own
pricing structure and features, and you will want to investigate each
available option to determine the best fit for your organization. Refer
to the "Contributions" section for a list of factors to consider in
selecting a processor.

The actual steps involved in configuring and testing your payment
processor connection are different for each processor. For more
information, visit:
[http://wiki.civicrm.org/confluence/display/CRMDOC/Payment+Processors](http://wiki.civicrm.org/confluence/display/CRMDOC/Payment+Processors)

### Permissions for anonymous users

This link is only present on Drupal sites. On Joomla! and WordPress
(and Drupal) Sites permissions for anonymous and other users are set
after navigating to **Administer > Users and Permissions >
Permissions** > **Drupal (or Joomla! or WordPress) Access Control**.
See the *Permissions and Access Control* chapter in this section for
information on setting permissions.

### System Workflow Templates

CiviCRM comes with a set of system-generated emails, including
contribution receipts and event registration confirmations. These are
known as system workflow templates, and it's a good idea to review them.
They will be sent out with your organization's name on them. You can
customize the style and wording of these messages here.

Workflow messages include text AND necessary program logic. Use caution
when editing so as not to modify the program logic. Be sure to test the
workflow and review the emails sent after making any changes. If you
find that your changes have caused problems, errors or missing
information - you can always "Revert" to the system default for that
workflow.


You should now have reviewed all the basic configuration tasks. The
remaining tasks on the checklist involve an understanding of the ways in
which you can record and use contact data and are best left until you
have read more in this book.
