## Creating Contribution Pages
This section describes setting up online contribution pages where
visitors to your website can make contributions to your organisation.
CiviContribute is very flexible and includes many optional fields and features
such as recurring contributions, pledges and personal campaign pages. These can
make setting up contribution pages seem like a daunting task.  It can be
quite simple though as shown by the first two procedures.  

## The simplest contribution page (Receipt sent only from payment processor.)
1. Make sure you have a [payment processor configured](payment-processors.md).
2. Go to to **Contributions > New Contribution Page**.
3. Enter the **title** for your website page.
4. Select the appropriate **financial type**.
5. Click on **Continue**.
6. On the next page leave everything as is except for ticking the **Allow Other
Amounts** checkbox and setting **minimum** and/or **maximum** amounts if you want to.
7. Click on **Save and Done**.
8. Follow the steps for your CMS to [display this page on your website](#publicizing-your-contribution-page).  

## A very simple contribution page including receipt from your organisation
1. Make sure you have a [payment processor configured](payment-processors.md).
2. Go to to **Contributions > New Contribution Page**.
3. Enter the **title** for your website page.
4. Select the appropriate **financial type**.
5. Click on **Continue**.
6. On the next page leave everything as is except for ticking the **Allow Other Amounts** checkbox and setting **minimum** and/or **maximum** amounts if you want to.
7. Click on **Save**.
8. Select the **Receipt** tab.
9. Enter the **title** for your Thank-you page.
10. Tick **Email Receipt to Contributor**.
11. Enter the FROM email address in **Receipt From Email**.
12. Click on **Save and Done**.
7. Follow the steps for your CMS to [display this page on your website](#publicizing-your-contribution-page).

## Setting up a contribution page - full details.

Navigate to **Contribution > New Contribution Page**.
(**Contribution > Manage Contribution Pages > Add Contribution Page** takes
  you to the same screen.)  

![New Contribution Page](../img/civicontribute-new-contribution-page.png)

-  The page title and financial type are the only compulsory fields. CiviCRM
comes with four standard financial types, but you can
[create more](key-concepts-and-configurations.md) to meet your
organisation's accounting needs.
-  Link this contribution page to a [campaign](../campaign/what-is-civicampaign.md). (optional)
-  Compose your introductory message. (optional)
-  Compose your footer message. (optional)
-  Set a goal amount. (optional)
-  This contribution page has to be manually enabled or disabled, but you can
   set a **start date** and **end date** that will apply for a Contribution
   Widget and
   [Personal Campaign Pages](personal-campaign-pages.md). (optional)
-  Choose whether or not to accept [Honoree soft crediting.](soft-credits.md)
-  Choose to use a confirmation page where users can check all details are
   correct or to process the payment as soon as the contribution form is submitted.
-  Choose whether or not to display social media links on online pages and in
the automatically emailed receipt (if being sent).
-  Decide whether or not to make the Contribution Page active now.
-  Click **Continue**. (This is when you new contribution page is first
  saved.) You will be able to go back and modify all aspects of this page at
  any time by visiting the **Title** (and Settings) tab.

You will now be on the (Contribution) **Amounts** tab.  All the other
feature tabs for contribution pages will now be visible at the top
of the page.  We will deal with them one by ne

### Amounts tab
![Contributions Amounts Page](../img/civicontribute-online-contribution-amounts.png)

-  The **Execute real-time monetary transactions** box is checked by default.
You would uncheck this box if you are using this contribution page for free
membership signup or to solicit in-kind (non-monetary) donations, or when you
want **all** users to submit their payments offline.
-  Select the **Currency**.
-  Select one or more previously configured [Payment Processors](payment-processors.md)
for this page. Some organizations find it is a good idea to offer a choice of
processors. You can do this by setting up multiple processors, and checking the
    corresponding boxes on this form.
-  Check the **Pay Later** box if you want to give users the option to
    submit payment offline (e.g. mail in a cheque, call in a credit card, deposit directly into your bank account etc.). If you allow pay later contributions you will need to decide on a checkbox label to display to your users and the instructions for submitting these delayed payments.
-  If you uncheck the **Contribution Amounts Section Enabled** the remaining fields on this page will vanish. You will only be able accept fixed-amount membership fees, or, if you configure a membership price set, fixed-amount memberships fees and other contributions as specified in the price set all charged in a **single** transaction.
-  Select a pre-defined **Price Set** (for more complex payment
    options), OR enter up to 10 fixed contribution amounts in the table at the bottom of the page.)
-  You can check **Recurring contributions** if you payment processor and its integration with CiviCRM support recurring billing and you want to allow this feature. (There are restrictions on recurring payments when [membership fees](../membership/defining-memberships.md) are being paid.) If you check **Recurring contributions** further settings become visible.
  - You can either set one frequency (e.g. a user can donate their chosen amount monthly) or allow for more user flexibility, where they can decide their own interval and/or number of installations (e.g. a user can donate their chosen amount once every three months for 12 installments).
-  Check the **Pledges** box to give users the opportunity to [pledge
    future payments](../pledges/what-is-civipledge.md).
-  Decide on the label for the Contribution amount area on your page.
-  Check **Allow other amounts** to give users the option to pay any
    amount they choose. You can set a minimum and a maximum amount for "Other Amount" contributions if you want to.
-  Click **Save and Done**.

### Memberships tab

This is covered in detail in  [Memberships](../membership/online-membership-sign-up.md).

### Profile tab

If you want to collect information such as age, interests and skills that goes
beyond the essential fields required to make a contribution, you can include
existing [CiviCRM Profiles](../organising-your-data/profiles.md) at the beginning or
end of a contribution page. You can also create new profiles.

Each profile appears on the contribution page as a fieldset with a legend
header.  The legend will be the profile Public Title if that is set, or else the
Profile Name.  A good practice is to give profiles names that are useful for
identifying profiles in a list and to give profiles public titles that make a
good header for the form section.

Profiles used in a contribution page can ONLY contain fields which
belong to:

-   contact records
-   contribution records

Profiles which include fields associated with any other record types
will not be available for this purpose.

Contribution pages will always include a required email address field.  If you
do not include any profile with an email address field, an email address field
will be added near the top of the form.

To add a profile to a contribution form:

1.  Navigate to Manage Contribution Pages then for the page you wish to
    configure, click on **Configure > Include Profiles**.
2.  Select a CiviCRM profile from the dropdown menu to be included at
    the top of the contribution page and/or at the bottom of the page (there are drop down menus for each).
    You can then preview your selection(s), edit an existing profile,
    copy an existing profile or create a new profile.
    When you edit or create a new profile you will use the profile drag
    and drop interface pictured here.  You may click the pencil icon to edit the
    profile name, public title, and pre- and post-form help text.
    ![screenshot](../img/Contribution-page-edit-profile.png)

    !!! warning
        If you modify an existing profile whilst configuring your
        Contribution page, the changes you make will apply everywhere that
        profile is being used. So unless an existing profile **exactly**
        matches your requirements you should copy the profile, then rename
        and edit the copy as required.

3.  Click **Save** or **Save and Done** or **Save and Next**.

!!! note "Multiple address blocks"
    Most payment processors add a set of address fields along with the payment
    details.  These fields will be used to save a billing address.

    If you include a profile with address fields at the top of the page, CiviCRM
    automatically generates a checkbox on the contribution form which allows the
    user to indicate that his/her Billing Address is the same as the address
    entered in the profile. When set up correctly, the checkbox is checked by default and reveals billing name and address fields when unchecked. For a checkbox to be generated and hide/reveal the billing address fields, the profile 
    1. Must be included at the top (not the bottom) of the page (there is a drop down menu for each option on the Include Profiles configuration page)
    2. Must have the same fields (First Name, Last Name, Street Address, City, State, Postal Code and  Country) as the Billing Address profile and these fields *must be marked as required.* When the correct fields are included but not marked required the checkbox will still be visible but the javascript won’t work so the billing name and address always be visible.
    ![Include profile top of page listbox, and include profile bottom of page listbox.](../img/Profiles-HomeAddress.png)


A number of the [Advanced
Settings](../organising-your-data/profiles.md#advanced-settings) for profiles take
effect when a profile is included in a contribution page.  You cannot edit these
from the editing interface within the contribution page settings; you must go to
the main profile settings form to make changes.

-   **Adding contacts to a group.**  Note that many donors do not wish to join a
    mailing list merely because they have made a donation.
-   **CMS User account registration options.**  A donor can be presented with
    the option or requirement to log in or create a user account while making a
    contribution.
-   **Including ReCAPTCHA.**  A CAPTCHA can be added to make it more difficult
    for bots and donors to submit the form.

Other advanced settings, such as what to do upon duplicate match, are ignored on
contribution pages.

For more information read [Profiles](../organising-your-data/profiles.md).

## Automatic Contribution Recording

Regardless of how donors get to your contribution page, CiviCRM
automatically records their donations, freeing your staff from doing
manual data entry. If the donors already exist in the database, CiviCRM
adds the contribution to their existing record. If they don't exist,
CiviCRM creates a new record for them.

In situations where people have multiple email addresses, or where more
than one person shares an email address, it can be possible for
contributions to be credited to the wrong contact. To mitigate the
chance of this happening, you can adjust CiviCRM's default duplicate
matching rules. For instructions on how to do this, read
[Deduping and Merging](../common-workflows/deduping-and-merging.md).

### Receipt Tab Thank-you and Receipting

Once you have created your contribution page, you can customise the
Thank-you and Receipt emails that are sent to contributors.

1.  Navigate to **Administer > CiviContribute > Manage Contribution
    Pages**.
2.  Use the **Configure** link at the right-hand side of a contribution
    page in the list to access and edit the page.
3.  Click on **Thank-you and Receipting** and enter the information that
    you wish to appear in the thank-you email. Donors usually expect a
    receipt as soon as their transaction is complete, so it is
    recommended to enable the automatic Email Receipt.
4.  Click **Save and Done**.

## Publicizing your contribution page

Now that you've created your contribution page, it's time to bring
people to the page so they can contribute. You will probably want to
display a link to the page prominently on your website through a donate
button or menu item. Here are some additional tips for promoting a
contribution page in different CiviCRM configurations:

### Menu item in Joomla!

The most direct way to expose your contribution page or membership
signup/renewal page on the front of your web site is by creating a menu
item.

1.  Navigate to a menu and create a new CiviCRM item.
2.  From the list of menu options, choose Contributions.
3.  In the basic parameters section, select the contribution page you
    would like exposed from the dropdown menu.
4.  Save the menu item and view the website to confirm the page's
    functionality.

### Menu item in Drupal

From the contribution page listing, select Live Page to view the
finished page. You can then copy the URL and include it in a content
page or assign it to a menu item.

### Page or Post in WordPress

You can easily embed your contribution page in a post or page on your
WordPress front-end site.

1.  Login to the administration dashboard of your WordPress site.
2.  Click on **Pages** or **Posts > Add New**
3.  Click on the CiviCRM icon next to Upload / Insert
4.  Select Contribution Page as your Frontend Element
5.  Select the desired contribution page
6.  Save the page or post, and your contribution page will automatically
    be embedded within your site's theme on that page.

### "Pretty" URLs

CiviContribute contribution pages have "ugly" URLs - in other words,
they are difficult to remember. An example is *:*

*www.myorganization.org/civicrm/contribute/transact?reset=1&id=1*

On the other hand, "pretty" URLs are much easier to remember and use in
your organization's outreach, for example:

*www.myorganization.org/donate*

A pretty URL is simply a URL redirect (automatically taking people from
one page of your web site to another). Drupal provides a helpful module
called Path Redirect
([http://drupal.org/project/path_redirect](http://drupal.org/project/path_redirect))
that lets you can create URL redirects from the user interface without
complicated web server configuration. Joomla! users also have a
work-around if Search Engine Friendly URLs are enabled in Global
Settings. You can then create a menu link to the contribution page and
define the "pretty" URL using the alias field.

### Personalised Email

Emailing your current membership is the other critical way to publicize
the campaign. The CiviMail component of CiviCRM allows you to send
targeted emails to any group of contacts in your database. Within a
CiviMail message you can include links to the contribution form and use
CiviMail's tracking capability to see how many people click on that
link.

One time-tested way to increase contributions is to use
[checksum tokens](../common-workflows/tokens-and-mail-merge.md#checksum)
to send each constituent a personalized email with a link to the contribution form
that has all of their contact information already filled in. This saves
them the hassle of filling it out and raises the chances that they
donate.
