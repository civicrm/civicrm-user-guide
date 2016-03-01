Creating Contribution Pages
-----------------------------
This chapter describes setting up a simple contribution page where visitors to your website can make contributions to your organisation.

Create a new contribution page by navigating to **Contributions > New Contribution Page** or **Contributions > New Contribution Page** then click on **Add Contribution Page**.

-  Give the page a title.
-  Select the Financial Type. CiviCRM comes with four standard financial types, but you can create more to meet your [organisation's accounting needs](../../accounting-integration).
-  Link this contribution page to a [campaign](../../campaign). (optional)
-  Compose your introductory message. (optional)
-  Compose your footer message. (optional)
-  Set a goal amount. (optional)
-  This contribution page has to be manually enabled or disabled, but you can set a **start date** and **end date** that will apply for the Contribution Widget and [Personal Campaign Pages](../../personal-campaign-pages). (optional)
-  Choose whether or not to accept [Honoree soft crediting.](../../soft-credits.md)
-  Choose to use a confirmation page where users can check all details are correct or to
  process the payment as soon as the contribution form is submitted.
-  Choose whether or not to display social media links on online pages and in the automatically emailed receipt (if being sent).
-  Decide whether or not to make the Contribution Page active now.
-  Click **Continue**. (This is when you new contributions page is first saved.)  You will be able to go back and modify all aspects of
    this page at any time by visiting the **Title** (and Settings) tab.

You will now be on the (Contribution) **Amounts** tab.

-  The **Execute real-time monetary transactions** box is checked by default. You would uncheck this box if you are using this contribution page for free membership signup or to solicit in-kind (non-monetary) donations, or when you want **all** users to submit their payment offline.
-  Select the **Currency**.
-  Select one or more **Payment Processors** for this page (which
    you have previously configured). Some organizations find it
    advantageous to give their constituents a choice of processors. You
    can do this by setting up multiple processors, and checking the
    corresponding boxes on this form.
-  Check the **Pay Later** box if you want to give users the option to
    submit payment offline (e.g. mail in a cheque, call in a credit card, deposit directly into your bank account etc.).
-  Check the **Contribution Amounts Section Enabled** box to allow
    various specific amounts to be presented. Leave this unchecked if,
    for example, you are using the page for membership sign-ups that
    have fixed amounts, which will show only the fixed membership
    amounts and not allow custom amounts to be entered.
-  Select a pre-defined **Price Set** (for more complex payment
    options), OR enter up to 10 fixed contribution amounts in the table at the bottom of the page.)
-  You can check **Recurring contributions** if you payment processor and its integration with CiviCRM support recurring billing and you want to allow this feature. (There are restrictions on recurring payments when [membership fees](../membership/defining-memberships) are being paid.) If you check **Recurring contributions** further settings become visible.
-  Check the **Pledges** box to give users the opportunity to [pledge
    future payments](../pledges).
-  Decide on the label for the Contribution amount area on your page.
-  Check **Allow other amounts** to give users the option to pay any
    amount they choose. You can set a minimum and a maximum amount for "Other Amount" contributions if you want to.
-  Click **Save and Done**.

### Include Profiles

If you want to collect information from contributors beyond what is
required to make a contribution only, such as volunteer age and skills,
you can include existing CiviCRM Profiles at the beginning or end of a
contribution page. You can also create new profiles.

Profiles used in a contribution page can ONLY contain fields which
belong to:

-   contact records
-   contribution records

Profiles which include fields associated with any other record types
will not be available for this purpose.

Contribution pages will always include a required email address field,
regardless of whether you include any other fields in your profile(s).

1.  Navigate to Manage Contribution Pages then for the page you wish to
    configure, click on **Configure > Include Profiles**.
2.  Select a CiviCRM profile from the dropdown menu to be included at
    the top of the contribution page and/or at the bottom of the page.
    You can then preview your selection(s), edit an existing profile,
    copy an existing profile or create a new profile.
    When you edit or create a new profile you will use the profile drag
    and drop interface pictured here.

    ![](../img/Contribution-page---edit-profile2.gif)

    WARNING: If you modify an existing profile whilst configuring your
    Contribution page, the changes you make will apply everywhere that
    profile is being used. So unless an existing profile **exactly**
    matches your requirements you should copy the profile, then rename
    and edit the copy as required.
3.  Click **Save** or **Save and Done** or **Save and Next**.

Read more about profiles in the *Profiles* chapter of *Organizing your
Data*.

Automatic Contribution Recording
--------------------------------

Regardless of how donors get to your contribution page, CiviCRM
automatically records their donations, freeing your staff from doing
manual data entry. If the donors already exist in the database, CiviCRM
adds the contribution to their existing record. If they don't exist,
CiviCRM creates a new record for them.

In situations where people have multiple email addresses, or where more
than one person shares an email address, it can be possible for
contributions to be credited to the wrong contact. To mitigate the
chance of this happening, you can adjust CiviCRM's default duplicate
matching rules. For instructions on how to do this, *see the chapter
Merging and Deduping in the Basic Concepts section of this book*.

### Thank-you and Receipting

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

Publicizing your contribution page
----------------------------------

Now that you've created your contribution page, it's time to bring
people to the page so they can contribute. You will probably want to
display a link to the page prominently on your website through a donate
button or menu item. Here are some additional tips for promoting a
contribution page in different CiviCRM configurations:

### **Menu item in Joomla!**

The most direct way to expose your contribution page or membership
signup/renewal page on the front of your web site is by creating a menu
item.

1.  Navigate to a menu and create a new CiviCRM item.
2.  From the list of menu options, choose Contributions.
3.  In the basic parameters section, select the contribution page you
    would like exposed from the dropdown menu.
4.  Save the menu item and view the website to confirm the page's
    functionality.

### **Menu item in Drupal**

From the contribution page listing, select Live Page to view the
finished page. You can then copy the URL and include it in a content
page or assign it to a menu item.

### **Page or Post in WordPress**

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

A pretty URL is simply a URL redirect (autmoatically taking people from
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

One time-tested way to increase contributions is to send each targeted
constituent a personalized email with a link to the contribution form
that has all of their contact information already filled in. This saves
them the hassle of filling it out and raises the chances that they
donate. Using CiviMail, you can use this feature by creating a special
link in the body of your CiviMail message that includes a *checksum
token*. A checksum is a unique and pseudo-random number assigned to each
recipient of the mailing that points back to their contact information,
securely stored in your database.

When people click on the special link, CiviCRM looks them up in the
database and pre-fills fields on the contribution form (core fields or
fields exposed via a profile) with any information in their contact
record. To read more on how to do this and what the link path must be,
visit:
[http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens](http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens)
