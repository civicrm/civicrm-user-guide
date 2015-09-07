Set-up
======

This chapter shows you how to set up CiviContribute and related
components of CiviCRM to support fundraising.

This chapter assumes you have a working understanding of custom
fields, contact matching rules, CiviCRM Profiles, and the
CiviMember and CiviMail components. The chapter also assumes you have
already set up your payment processor and created any custom fields
you want to use when tracking contributions. If you have not done these
things, please refer to the appropriate sections of this manual for more
information.

General Configurations
----------------------

You may need to configure the following fields before you begin setting
up various methods for recording and managing contributions.

### **Financial Types and Accounting Codes**

If you need to add Financial Types or accounting codes, do this first.

1.  Navigate to **Administer > CiviContribute > Financial Types**,
    where you can edit one of the existing Financial Types or create a
    new one by clicking **Add Financial Type**.
2.  Once you edit or add a Financial Type, you can define an accounting
    code that corresponds to your accounting system (the accounting code
    will be exported along with the contribution data if you do an
    export), and indicate whether this type of contribution is
    tax-deductible.

Be careful when editing core Financial Types or adding new types,
because CiviCRM has useful built-in functionality that depends on the
core Financial Types. 

### **Premiums**

Configure premiums, such as T-shirts or subscriptions, that you want to
offer on your contribution pages:

1.  Navigate to **Administer > CiviContribute > Premiums (Thank-You
    Gifts)**.
2.  You can edit an existing premium or click **Add Premium** to add a
    new one.
3.  Once you edit or add a premium, you can then enter additional
    information: Name, Description, SKU (an optional product code),
    Premium Image (an optional image of the item), Minimum Contribution
    Amount to receive the premium, Market Value of the premium, Actual
    Cost, and Options (e.g., colors and sizes).
4.  If you're offering a subscription or service, you can also click on
    the **Subscription** or **Service Settings** and define additional
    information here, such as Period type (e.g., Fixed or Rolling), the
    Fixed Period Start Day, the Duration, and the Frequency.

### **Accepted Credit Cards**

Navigate to **Administer > CiviContribute > Accepted Credit Cards** to
edit existing acceptable credit cards or define a new option through
**Add Accept Creditcard**.

### **Payment Instruments**

Navigate to **Administer > CiviContribute > Payment Instruments** to
edit existing options that can be used for contributions or to add a new
option through Add Payment Instruments. The common options - credit
card, cash, check, debit card, and EFT - are installed by default. 

Creating Contribution Pages 
-----------------------------

To create a new contribution page:

1.  Navigate to **Contributions > Manage Contribution Pages**and
    click on **Add Contribution Page**.
2.  Give the page title, select the Financial Type (donation, campaign
    contribution, etc.), goal amount, introductory message, whether to
    accept Honoree soft crediting, and any other relevant information
    such as dates. You will be able to go back and modify all aspects of
    this page at any time after completing the setup wizard. Click
    **Continue**. 
3.  The **Execute real-time monetary transactions** box is checked by
    default, to enable monetary donations. You would only uncheck this
    box if you are using this contribution page to solicit in-kind
    (non-monetary) donations.
4.  Select the **Currency**
5.  Select one or more **Payment Processors** for this page (which
    you have previously configured). Some organizations find it
    advantageous to give their constituents a choice of processors. You
    can do this by setting up multiple processors, and checking the
    corresponding boxes on this form.
6.  Check the **Pay Later** box if you want to give users the option to
    submit payment offline (e.g. mail in a check, call in a credit card,
    etc.).
7.  Check the **Contribution Amounts Section Enabled** box to allow
    various specific amounts to be presented. Leave this unchecked if,
    for example, you are using the page for membership sign-ups that
    have fixed amounts, which will show only the fixed membership
    amounts and not allow custom amounts to be entered.
8.  Select a pre-defined **Price Set**(for more complex payment
    options), OR enter up to 10 fixed contribution amounts in the table.
9.  Check the **Pledges** box to give users the opportunity to pledge
    future payments. To learn more about configuring pledges, refer to
    the Pledges chapter.
10. Check **Allow other amounts** to give users the option to pay any
    amount they choose.
11. Click **Save and Done**. 



###Include Profiles

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
     
    ![](../_edit/static/Contribution-page---edit-profile2.gif) 
     
    WARNING: If you modify an existing profile whilst configuring your
    Contribution page, the changes you make will apply everywhere that
    profile is being used. So unless an existing profile **exactly**
    matches your requirements you should copy the profile, then rename
    and edit the copy as required.
3.  Click **Save** or **Save and Done** or **Save and Next**.

Read more about profiles in the *Profiles* chapter of *Organizing your
Data*.


###Thank-you and Receipting

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

Offline fundraising 
---------------------

Your organisation may collect donations at events, solicit donations via
postal mailings and other offline methods. Any money raised through
offline activities needs to be manually entered into CiviCRM in order to
ensure that final reporting is accurate. 

There are three steps within CiviCRM for offline fundraising: creating
your lists, creating your mailings, and manually entering contributions.

### Creating your lists

This process is fairly straightforward if you are familiar with
CiviCRM's search capabilities.

Go to **Search > Find Contacts** to create a list of records to receive
your offline postal mail appeal (it could be your entire database).

If you want to track the success of a mailing or who receives certain
appeals, save the search results as a group. Use the check box to select
all and choose the appropriate option from the **"- actions -"**
dropdown menu (e.g. New Smart Group or Add Contacts to Group). Later,
you can mark everyone in that group as recipients of that appeal using
the **Record Activity for Contacts** option under the **"- actions-"**
dropdown menu. 

If you want to create letters for postal mailings you can do this using
CiviCRM's internal Print PDF letter feature, or you export the list as a
CSV file and use mail merge to a word processor.

To export a list:

1. Select all records or a subset using the checkboxes, and from
    the **"- actions -"** dropdown menu choose **Export Contacts** and
    click **Go**.
1. Choose whether to **Export PRIMARY fields** or **Select fields for
    export**. If you elect to export primary fields, the CSV file will
    be immediately generated when you click **Continue**. If you opt to
    select which fields you want to export, click **Continue** and a
    list of dropdown options will appear.
1. Select the required fields; if you wish to save the list of exported
    fields as an export mapping for future use, check the **Save this
    field mapping** box.
1. Click **Export** to generate the CSV file.
1. Click **Done** when you have finished to return to the contact list.


### Creating postal mailings

Once your spreadsheet is created, you can do a mail merge using any word
processing software (such as OpenOffice, the free software word
processor) that will insert any fields you want in the letter. 

CiviCRM can also create mailing labels for you. Perform the same search
you used in the previous section to create your list of recipients,
then:

1.  From the **"- actions -"** dropdown menu, select **Mailing
    Labels**.
2.  Select the mailing label number, determine whether you want to
    exclude people with "do not mail" checked in their privacy options
    (checked by default and recommended), and whether you want to merge
    two records that have the same mailing address into one label. This
    last option is very useful when you are mailing a household or
    organization and you don't want them to receive duplicate mailings.
    When the records are merged, each name at that address appears on
    its own line on the label.
3.  Click **Make Mailing Labels** and a printable PDF document will be
    created.

Note that many non-profit organizations in the United States have to
sort recipients of a mailing based on zip code for bulk mailing
purposes. If this is true for your organization, it is recommended you
do *not* create your mailing labels within CiviCRM, but instead create
them using word processor merge functions where you have control over
the sort order. You can reuse the same spreadsheet for the mail merge
you exported in the previous section.

Batch Entry of Contributions, Membership or Pledge Payments 
-------------------------------------------------------------

The **Batches** feature allows you to enter multiple membership, pledge
or contribution payments as well as add new contacts on the fly in a
grid-style input screen. The fields of information that you see and want
to collect in the batch entry input grid for **Batches** are determined
by several CiviCRM reserved profiles. If you want to collect other
kinds of information that are not currently included in these profiles,
you will need to alter these profiles to reflect the fields you want to
display.

### Configuring Profiles for Batch Entry of Contribution, Membership and Pledge Payments

To alter the profile used when you want to create a new contact for an
Individual, Household, or Organization while recording the contribution,
update the reserved profiles called **New Individual, New Household**,
or **New Organization** accordingly. To change the fields of
information you want to collect for these contacts: 

-   Go to the menu and click **Administer > Customize Data and Screens > Profiles**, then click on **Reserved Profiles** tab. Click on
    **Fields** next to called **New Individual, New Household**, or
    **New Organization**.
-   You can then add, edit or rearrange the fields as you want to see
    them in the batch entry input grid.*To find out more about how to
    use profiles, see the chapter called “Profiles” in the “User
    Interface” section*. 

**TIP:** Reserved profiles for **New Individual, New Organization**,
and **New Household**, are used in other areas of CiviCRM. Be aware
that if you alter these profiles for use with **Batches**, these same
changes you’ve made will also appear on other screens where you have the
option to create a new contact inline. 

![](/img/CiviCRM-Contributions-SetUp-new-individual-profile.jpg)

Above is CiviCRM’s default configuration of the New Individual profile,
which is used when you select to create a new contact for an individual
during batch entry of contributions or membership payments.

To alter the profile of fields of information you want to collect for
contributions or membership payments, you will need to update the
reserved profiles called **Contribution Batch Entry** or **Membership
Batch Entry**: 

-   Go to the menu and click **Administer > Customize Data and Screens > Profiles**, then click on **Reserved Profiles** tab. Click on
    **Fields** next to **Contribution Batch Entry** profile or the
    **Membership Batch Entry** profile.
-   You can then add, edit , or rearrange the fields in this profile,
    e.g. you may have other custom contribution fields you would like to
    display and collect information, and display in the batch entry
    input grid. *To find out more about how to use profiles, see the
    chapter called “Profiles” in the “User Interface” section*. 

![](/img/CiviCRM-Contributions-SetUp-contribution-batch-entry-profile.jpg)

Above is CiviCRM’s default configuration for the Contribution Batch
Entry profile, which is used when you record information about a
contact’s contribution or pledge payment.



![](/img/CiviCRM-Contributions-SetUp-membership-batch-entry-profile.jpg)

Above is CiviCRM’s default configuration for the Membership Batch Entry
profile, which is used when you record information about a contact’s
membership payment. 

Importing contributions
-----------------------

If you have not imported data before, please refer to the chapter
'importing data' first.

When preparing your data import it is helpful to know what fields are
required for Import. You'll want to be sure that these fields are
included in your CSV import file. Below is a list of the required
fields. Please note that the fields marked **(Match to
Contact)**indicated that only one of those options must be included for
import. You do not need all of those fields to be included.

-   **Contact ID (Match to Contact)**
-   **Email (Match to Contact)**
-   **External Identifier (Match to Contact)**
-   **Financial Type**
-   **Total Amount**

 

The import tool for contributions is similar to that of contacts, but
there are some pre-requisites which must be met before running the
import. Firstly, contributions cannot be imported unless the
contributors already exist in the database as contacts. If you need to
import contributions for contacts that are not yet available, run a
contact import first, preferably including a unique external identifier
(most often an ID assigned by the database or application you are
importing records from). There are two ways to match a contribution to a
contact:

-   Use the external ID of the contact by including the ID in a column
    of the CSV file (if this ID was not imported with contacts, but you
    have them on record, a second contact import could be run to update
    this field, after which you may import contributions).
-   Alternatively, you can match contributions to contacts based on your
    contact de-dupe rules, e.g. through including the first name, last
    name and email address of the donor against each contribution in the
    file. If a contact matches these three fields, the contribution will
    be assigned to it.

Remember, CSV files must be less than 2MB in size. If the file size
exceeds this, create multiple CSV files and distribute the data between
them.

[](https://www.pcisecuritystandards.org/)
