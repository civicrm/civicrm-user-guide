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


### **Accepted Credit Cards**

Navigate to **Administer > CiviContribute > Accepted Credit Cards** to
edit existing acceptable credit cards or define a new option through
**Add Accept Creditcard**.

### **Payment Instruments**

Navigate to **Administer > CiviContribute > Payment Instruments** to
edit existing options that can be used for contributions or to add a new
option through Add Payment Instruments. The common options - credit
card, cash, check, debit card, and EFT - are installed by default.


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
