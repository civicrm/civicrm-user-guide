# Integrating with WordPress

CiviCRM integrates with WordPress as a plugin starting with WordPress version 3.3.1 (those using earlier versions of WordPress will need to upgrade prior to installing CiviCRM).

CiviCRM public forms such as online contribution pages and event registration pages will be shown to the public in your selected WordPress theme. When logged in to your Control Panel, CiviCRCM will be shown as a link in the left sidebar menu.

### Synchronize WordPress Users to CivCRM Contacts

CiviCRM offers a function to Synchronize Users to Contacts: CiviCRM will check each user record for a contact record. A new contact record will be created for each user where one does not already exist. To perform this function go to **Administer -> Users and Permissions -> Synchronize Users to Contacts**

## Using Shortcodes to Publish CiviCRM Content in WordPress

WordPress shortcodes enable a user to be able to very easily display dynamic content within a WordPress Page or Post with the use of just one line of text. For more information about WordPress shortcodes [check here](http://en.support.wordpress.com/category/shortcodes/). After installing CiviCRM within your WordPress environment, you can immediately take advantage of CiviCRM specific shortcodes that enable you to display content that relates to:

-   Contribution Pages
-   Event Pages
-   Profiles
-   User Dashboards
-   Petitions

Keep in mind that prior to being able to display any CiviCRM content on you public website that record will have already been created within CiviCRM.

To add a shortcode either create a new post or new page and you will now see a CiviCRM button next to Add Media.

![image](../img/z_sprint14_shortcode%20insert.png)

After you click on CiviCRM you will be displayed with the following options:

![image](../img/z_sprint14_Wordpress_shortcode.png)

Dependent up the shortcode that you select you will have different sub options to cater the information to the end user.

When selecting a front end element of **Contribution Page** you will have the ability to select the specific Contribution Page that you want to be displayed then you will have the ability to chose between Live or Test mode.

When selecting **Event Pages** you can either chose from the following two options:

-   Information Page: By choosing this option your WordPress page will be populated with the Summary Information about the event. This will include the description as well as the map of the location if you have specified to do so within your event settings. In addition there is a button provided on the Information page that will enable an end user to register for the event

-   Registration page: This option bypasses the Summary Information and displays the page for an end user to register for a specific event.

**Profile Pages** give you 3 options to chose from: Create, View, and Edit.

-   Create: A blank form on your website that an end user can fill out and save which will then write to your CiviCRM database.

-   View: If an end user is logged into WordPress, you can display what information you have on record for them within CiviCRM for this specific profile. For instance if you displayed the New Individual profile which consists of First Name, Last Name, and Email address the end user would be able to view this information.

-   Edit: Similar to view mode, if an end user is logged in, you can display what information you have on record for them but also give them the ability to edit that information. For instance if an individual has recently changed their last name or email address and you are presenting the New Individual profile, they would have the ability to review the information and update it and save that information to CiviCRM all through the website.

When selecting the **User Dashboard** you get no additional options. To identify what related information you have setup to be displayed within the user dashboard i.e. Contributions, memberships, etc. navigate to **Administer > Customize Data and Screens > Display Preferences** and select all of the information you would like to have visible to the user.

Finally, for **Petitions**, the only option presented is to select the specific petition that you wish to display on your website.

## Plugin Integrations

There are several plugins that have been developed to improve the integration between CiviCRM and WordPress.

#### [CiviCRM Admin Utilities](https://wordpress.org/plugins/civicrm-admin-utilities/)

CiviCRM Admin Utilities modifies CiviCRM’s behaviour in single site and multisite installs. It does a number of useful things:

* Modifies the styling of the CiviCRM menu to fix a number of issues
* Allows you to choose which Post Types the CiviCRM shortcode button appears on
* In WordPress multisite, allows you to hide CiviCRM on sub-sites

[Download](https://wordpress.org/plugins/civicrm-admin-utilities/)

#### [CiviCRM WordPress Profile Sync](https://wordpress.org/plugins/civicrm-wp-profile-sync/)

The CiviCRM WordPress Profile Sync plugin keeps the “First Name”, “Last Name”, “Email Address” and “Website” fields of a WordPress (and BuddyPress) user profile in sync with the corresponding fields of a CiviCRM contact. The synchronisation takes place regardless of whether the changes are made in WordPress, BuddyPress or CiviCRM.

[Download](https://wordpress.org/plugins/civicrm-wp-profile-sync/)

#### [CiviCRM WordPress Member Sync](https://wordpress.org/plugins/civicrm-wp-member-sync/)

CiviCRM WordPress Member Sync keeps a WordPress user in sync with a CiviCRM membership by granting either a role or capabilities to a WordPress user who has that membership.

This enables you to have, among other things, members-only content on your website that is only accessible to current members as defined by the membership types and status rules that you set up in CiviCRM. This plugin is compatible with both **[Members](https://wordpress.org/plugins/members/)** and **[Groups](https://wordpress.org/plugins/groups/)** for managing members-only content in WordPress. See the Installation section for details.

[Download](https://wordpress.org/plugins/civicrm-wp-member-sync/)

#### [Caldera Forms CiviCRM](https://github.com/mecachisenros/caldera-forms-civicrm)

A WordPress plugin that integrates the [Caldera Forms plugin](https://wordpress.org/plugins/caldera-forms/) with CiviCRM.

The Caldera Forms CiviCRM plugin contains a set of form processors that interact with CiviCRM's API to retrieve, create and update data in CiviCRM. With this plugin, you can create responsive forms that expose CiviCRM fields and entities like Activities, Relationships, Tags, Groups and more.
Features

* Add up to 10 Contacts on the same form
* Auto-populate form if the user is logged in
* Define Contact Type: Organization, Individual, Household, and Custom Contact Subtypes
* Map Custom Fields data
* Add Relationships to each contact
* Create Activities on form submission
* Checksum support to auto-populate form with URLs like _example.com/support?cid={contact.contact_id}&{contact.checksum}_

**Requirements**

To use this plugin, the following is needed:

* WordPress
* CiviCRM 4.6.x or 4.7.x
* [Caldera Forms](https://wordpress.org/plugins/caldera-forms/) to be installed

[Download](https://github.com/mecachisenros/caldera-forms-civicrm)

#### [Contact Form 7 CiviCRM integration](https://wordpress.org/plugins/contact-form-7-civicrm-integration/)

This plugin adds integration for CiviCRM to contact form 7. With this plugin it is possible to submit a contact for to an external CiviCRM.

[Download](https://wordpress.org/plugins/contact-form-7-civicrm-integration/)

#### [CiviCRM Event Organiser](https://github.com/christianwach/civicrm-event-organiser)

A WordPress plugin for syncing Event Organiser plugin Events with CiviCRM Events. The plugin syncs Event Organiser Events, Venues and Event Categories to their corresponding entities in CiviCRM.
Notes

This plugin requires at least WordPress 3.6 and CiviCRM 4.6.

It also requires:

* [Event Organiser](https://wordpress.org/plugins/event-organiser/) version 3.0 or greater
* [Radio Buttons for Taxonomies](http://wordpress.org/plugins/radio-buttons-for-taxonomies/) to ensure only one event type is selected

[Download](https://github.com/christianwach/civicrm-event-organiser)


### Widgets

WordPress Widgets add content and features to your Sidebars. Examples are the default widgets that come with WordPress: for Categories, Tag cloud, Search, etc. Plugins will often add their own widgets.

#### [CiviEvent Widget](https://wordpress.org/plugins/civievent-widget/)

You can use the CiviEvent widget to add two types of widgets for upcoming public events from CiviCRM. There’s no limit to the number of widgets you can add of either type. You can include the widgets in the sidebar like normal, or you can include them via shortcodes in the body of your posts.

[Download](https://wordpress.org/plugins/civievent-widget/)

#### [CiviCRM Contribution Page Widget](https://wordpress.org/plugins/civicrm-contribution-page-widget/)

CiviCRM contribution pages allow you to generate a “widget” showing the progress toward a goal. This plugin makes it easy to include one or more contribution page “widgets” as actual WordPress widgets on your sidebar.

[Download](https://wordpress.org/plugins/civicrm-contribution-page-widget/)

### BuddyPress

[BuddyPress](https://wordpress.org/plugins/buddypress/) is a suite of components that are common to a typical social network, and allows for great add-on features through WordPress’s extensive plugin system.

#### [BP Groups CiviCRM Sync](https://wordpress.org/plugins/bp-groups-civicrm-sync/)

A port of the Drupal civicrm_og_sync module for WordPress that enables two-way synchronisation between BuddyPress Groups and CiviCRM. It does not rely on any core CiviCRM files, since any required (or adapted) methods are included.

For each BuddyPress group, the plugin will automatically create two CiviCRM groups:

* A “normal” (mailing list) group containing a contact record for each corresponding BuddyPress group member. This group is assigned the same name as the linked BuddyPress group.
* An “ACL” group containing the contact record of the administrators of the corresponding BuddyPress group. This gives BuddyPress group admins the ability to view and edit members of their group in CiviCRM.

When a new user is added to (or joins) a BuddyPress group, they are automatically added to the corresponding CiviCRM group. Likewise, when a contact is added to the “normal” CiviCRM group, they will be added as a member to the corresponding BuddyPress group. If a contact is added to the CiviCRM “ACL” group, they will be added to the BuddyPress group as an administrator.

[Download](https://wordpress.org/plugins/bp-groups-civicrm-sync/)

#### [BP XProfile WordPress User Sync](https://wordpress.org/plugins/bp-xprofile-wp-user-sync/)

The plugin replaces the default BuddyPress xProfile Name field with two fields called (surprisingly) First Name and Last Name. These field values are kept in sync with the corresponding WordPress user profile fields as well as the BuddyPress xProfile Name field itself.

To be used alongside CiviCRM WordPress Profile Sync

[Download](https://wordpress.org/plugins/bp-xprofile-wp-user-sync/)
