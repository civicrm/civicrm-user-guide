Integrating with WordPress
==========================

CiviCRM integrates with WordPress as a plugin starting with Wordpress
version 3.3.1 (those using earlier versions of WordPress will need to
upgrade prior to installing CiviCRM).

CiviCRM public forms such as online contribution pages and event
registration pages will be shown to the public in your selected
WordPress theme. When logged in to your Control Panel, CiviCRCM will be
shown as a link in the left sidebar menu.



###Synchronize WordPress Users to CivCRM Contacts

CiviCRM offers a function to Synchronize Users to Contacts: CiviCRM will
check each user record for a contact record. A new contact record will
be created for each user where one does not already exist. To perform
this function go to **Administer -> Users and Permissions
-> Synchronize Users to Contacts**

Using Shortcodes to Publish CiviCRM Content in Wordpress
--------------------------------------------------------

Wordpress shortcodes enable a user to be able to very easily display
dynamic content within a Wordpress Page or Post with the use of just one
line of text. For more information about Wordpress shortcodes check
here: 
http://en.support.wordpress.com/category/shortcodes/ 
After installing CiviCRM within your Wordpress environment, you can
immediately take advantage of CiviCRM specific shortcodes that enable
you to display content that relates to:

-   Contribution Pages

-   Event Pages

-   Profiles

-   User Dashboards

-   Petitions

Keep in mind that prior to being able to display any CiviCRM content on
you public website that record will have already been created within
CiviCRM.

To add a shortcode either create a new post or new page and you will now
see a CiviCRM button next to Add Media.

![image](../img/z_sprint14_shortcode%20insert.png) 

After you click on CiviCRM you will be displayed with the following
options:

![image](../img/z_sprint14_Wordpress_shortcode.png) 

Dependent up the shortcode that you select you will have different sub
options to cater the information to the end user.

When selecting a front end element of **Contribution Page** you will
have the ability to select the specific Contribution Page that you want
to be displayed then you will have the ability to chose between Live or
Test mode.

When selecting **Event Pages** you can either chose from the following
two options:

-   Information Page: By choosing this option your Wordpress page will
    be populated with the Summary Information about the event. This will
    include the description as well as the map of the location if you
    have specified to do so within your event settings. In addition
    there is a button provided on the Information page that will enable
    an end user to register for the event
-   Registration page: This option bypasses the Summary Information and
    displays the page for an end user to register for a specific event.

**Profile Pages** give you 3 options to chose from: Create, View, and
Edit.

-   Create: A blank form on your website that an end user can fill out
    and save which will then write to your CiviCRM database.

-   View: If an end user is logged into Wordpress, you can display what
    information you have on record for them within CiviCRM for this
    specific profile. For instance if you displayed the New Individual
    profile which consists of First Name, Last Name, and Email address
    the end user would be able to view this information.

-   Edit: Similar to view mode, if an end user is logged in, you can
    display what information you have on record for them but also give
    them the ability to edit that information. For instance if an
    individual has recently changed their last name or email address and
    you are presenting the New Individual profile, they would have the
    ability to review the information and update it and save that
    information to CiviCRM all through the website. 

When selecting the **User Dashboard** you get no additional options. To
identify what related information you have setup to be displayed within
the user dashboard i.e. Contributions, memberships, etc. navigate
to **Administer > Customize Data and Screens > Display
Preferences** and select all of the information you would like to have
visible to the user.

Finally, for **Petitions**, the only option presented is to select the
specific petition that you wish to display on your website. 




