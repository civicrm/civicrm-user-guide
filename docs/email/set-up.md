Set-up
======

This chapter describes how to set up information such as From email
addresses, Mailing List Groups and email templates. It assumes that the
basic functionality necessary for your server to send and process emails
in the first place has already been configured. See *Email System
Configuration* in *Advanced configuration* for details.

Configuring your organisation's contact information
---------------------------------------------------

In order to send mass emails you must fill in some basic information:
your organisation's name, a short description, your email address, and
your postal address. CiviMail requires that you include the sender's
postal address along with unsubscribe/opt-out links in any mass mailing
you send, in order to comply with privacy laws in many countries. This
information is made available via tokens and must be included in any
mail sent with CiviMail.

To configure this information, go to: **Administer > Communications >
Organization Address and Contact Info**.

Mailing groups
--------------

CiviMail uses Groups to organise recipients of mass mailings. To create
a group, go to **Contacts > New Group**. When you create and configure
a Group for this purpose, make sure to check Mailing List under Group
Type so that it is available as a Mailing List in CiviMail. You can then
do a search and add contacts to the Group.

You can also create Smart Groups based on search results, which will
update the Group with any contacts that fit the search criteria. For
example, based on the results of Advanced Search you can create a Smart
Group of contacts who have active memberships, or a Smart Group of
contacts in a given city. As people become members or move to the city
you've searched on, they will be automatically added to the Smart Group.
This makes it possible to to send mailings without having to first
update the contacts in a group.

To create a **Smart Group**:

1.  Go to **Advanced Search** or **Find Contact**and run a search query
    based on the criteria for your group.
2.  On the search results page, click the radio button that selects all
    the records.
3.  From the**- more actions -**drop-down menu, select **New Smart
    Group** and then click **Go**.
4.  The next screen provides a review of the criteria chosen for the
    Smart Group. Give the Smart Group a name and (optionally) a
    description, and make the Smart Group a Mailing List.
5.  Click **Save Smart Group**.

**Note:** You can also create a Smart Group based on a Participant
search. However, the Smart Group save page will not offer you the option
to make this group a Mailing List. To make this Smart Group available to
CiviMail, you must change its settings through **Contacts > Manage
Groups**. This same thing happens if you use the Advanced Search and
choose Event Participants under "Display results as."

You cannot create smart groups based on Membership, Contributions or
Pledge searches, or based on results of an Advanced Search if the
"Display results as" option is set to anything but Contacts.

Allow people to sign up for your mailing lists online 
-------------------------------------------------------

CiviCRM makes it possible for people to sign themselves up for your
mailing lists online.

To allow this, you must designate the group as a mailing list. If you
didn't do this when you created the Group, go to **Contacts** >
**Manage Groups**. Click **Settings** on the group that holds your
mailing list recipients and check the Mailing List next to Group Type.
You must also change the Visibility to Public Pages. 

For this to work for users who don't have a log-in to your CiviCRM, you
must ensure that anonymous users in Drupal have the following permission
checked: "Access CiviMail subscribe/unsubscribe pages."

### Using the subscribe link 

One way to allow users to subscribe to an email list online is by
directing them to www.*yourdomain.org*/civicrm/mailing/subscribe. You
and anyone who accesses this link can subscribe to the available mailing
list groups.

### Using a profile 

Alternatively, you can collect more information when people sign up to
your mailing lists with the use of a profile that is then displayed on a
public page. Guidelines on what is you need to think about when using
profiles for mailing list sign-ups are below; for more complete
information about profiles, how they work, and how to set them up, see
the **Profiles** chapter in the **Data in CiviCRM** section.

For example, you could create a new Profile called Newsletter Sign-up.
Add to this profile the fields that you'd like website visitors who want
to join your mailing list to fill out. Each of the fields in the profile
must have its Visibility set to Public Pages.

For each field you include, you can choose whether it is required or
optional for people filling out the public form. The one exception is
that the profile must include an email field that is required. This is
so that an email can be sent to the person to confirm that they wanted
to sign up for the mailing list. Until they confirm, they will have a
status of "Pending" in the mailing list group.

There are two ways to display the profile publicly:

1.  Share a link directly. Return to the listing of profiles (at
    **Administer > Custom Data and Screens > Profiles**) and click
    **More** to the far right of your profile. Click **Use
    Profile-Create Mode**. Your browser will open up the public page;
    you can publish this link to allow users to sign up for your mailing
    lists.
2.  Embed this set of fields as a form in your website. Return to the
    listing of profiles (at **Administer > Custom Data and Screens >
    Profiles**) and click **More** to the far right of your profile.
    Select **HTML Form Snippet**. This will open a window in your
    browser that has a box with HTML code in it. Copy and paste the
    contents of the box into a page on your website. Website visitors
    will be able to sign up to your mailing lists on this page.

Alternatively, for Wordpress you can display the form publicly by using a shortcode. On any Wordpress Page, click the **CiviCRM** button above the editor. For **Page Type** select **Profile**. On the next drop-down that appears, select the name of the profile that you have created. Select **Edit** on the radio button option just below the drop-downs, so that you give users access to edit data in your database (i.e. to add their email address and name to your database). Click **Insert Form** and the shortcode will be added to the editor.

### Using a Webform (Drupal)

Many Drupal site administrators prefer to use a webform instead of a
profile to create their newsletter sign-up, because it provides
additional features such as advanced spam control and flexible theming.
For more information see:

[http://wiki.civicrm.org/confluence/display/CRMDOC/Webform+CiviCRM+Integration](http://wiki.civicrm.org/confluence/display/CRMDOC/Webform+CiviCRM+Integration)

### Adding people to your mailing list group by using a profile

To get a user automatically added to your mail list group(s) when they fill out your Newsletter Sign-up form (CiviCRM profile), you have two options:

Option A: On the profile, you can add a field for the mailing lists groups that you want
users to be able to sign up for. Go to the profile's fields and click **Add Field**. For Field Name,
select Contacts. When the possible selections load in the second field,
select Group(s). In Field Label, you can leave "Group(s)" or you may
want to change it to something more intuitive to your website visitors
such as "Newsletter Sign-up." Visibility for this field must be set
to Public Pages. When the profile displays publicly, this field will
show check boxes for all Mailing List Groups that have their Visibility
set to Public Pages. This way users can add themselves to all of your Mailing List Groups that they want to by putting a tick on the appropriate checkboxes.

Option B: Go to the profile settings. In the Advanced Settings section, select your desired Mailing List Group for **Add new contacts to a Group?**. Now when users fill out your form, they will be automatically added to this group. 

### Mailing list confirmation workflow

For this to work, first make sure that you have put a tick on the desired **Enable Double Opt-in** options in **Administer > Administration Console > CiviMail Component Settings**.

After people subscribe to mailing list groups—via the subscribe link or
a profile—CiviCRM will automatically send them an email asking them to
confirm their subscription. Until they click the confirmation link in
the email, their contact information will appear in CiviCRM with their
group subscription set to Pending. When they confirm, CiviCRM will
automatically change their group subscription status to Added and they
will be sent a welcome message. (Note: When users subscribe to multiple
groups at once, a confirmation email is sent for each group
separately.) 

Scheduled jobs and cron jobs
----------------------------

After people have signed up on your mailing list(s), you will want to be able to send them mass mailings. You will also want to automatically handle any bounced email messages. These topics are dealt with in detail in the **Everyday tasks** and **Maintaining Healthy Email Lists** parts of this book, respectively. Here in this section we are going to look at some backend and server options that enable the sending of mass mailings and the bounce handling to happen.

Go to **Administer > System Settings > Scheduled Jobs** and you will see all scheduled jobs that CiviCRM uses to do certain tasks on a regular basis. One such task is the actual sending of mass mailings, which is handled by the **Send Scheduled Mailings** scheduled job. Another task is the processing of bounced emails, for which the **Fetch Bounces** scheduled job is responsible. You will need to enable these two scheduled jobs (and any others that you want to be run on a regular basis). Without these two, CiviMail will not be sending any mailings and will not be processing the bounces.

Now, CiviCRM's scheduled jobs cannot self-trigger themselves. Something on your server has to trigger them. The most common option for this is to set up a cron job on your server. This cron job can trigger one or more (or all) of the scheduled jobs. For more detailed explanations and examples of how to do this, see the [Managing Scheduled Jobs](http://wiki.civicrm.org/confluence/display/CRMDOC/Managing+Scheduled+Jobs) wiki page.

Automated Messages and mailing list management 
------------------------------------------------

CiviCRM sends emails automatically when your participants take certain
actions:

-   When someone signs up for a mailing list, they get a confirmation
    email with a link that that they must click.
-   When they confirm, they get a welcome email.
-   When they unsubscribe, opt-out of all emails from your domain, or
    resubscribe to a list they have previously unsubscribed from, they
    get a confirmation email that does not require any action.
-   When they reply to a message you have sent through CiviMail, you can
    set up an autoresponse to their reply. 

In CiviCRM, these are called Automated Messages, and you can edit them
and add new ones at **Mailings > Headers, Footers, and Automated
Messages**.

For more information on email list management see the chapter entitled
**Maintaining Healthy Email Lists** which explores how CiviCRM handles
unsubscribes, bounces and email holds.

Creating and maintaining message templates
------------------------------------------

Message templates help to streamline your communications by allowing you
to reuse entire emails or parts of emails in both mass mailings and when
using the Send Email activity.

The easiest way to create a new message template is to check the Save as
New Template box on the message creation screen. This is available both
when using the Send Email activity and when sending a mass mailing. 

You can also create message templates from scratch or edit existing
templates by going to **Mailings > Message Templates** OR **Administer > Communications > Message Templates**.

1.  Click on **Add Message Template**.
2.  Enter a Message Title and a Message Subject. You can choose to use
    tokens to personalize your subject line.
3.  Scroll down to the HTML Format section and create your template.
    There are online resources, not specific to CiviCRM, that offer
    instructions on creating an HTML email templates. One suggestion is
    to find and copy an email template from a website that offers
    samples. 
4.  In the WYSIWYG editor toolbar, there is an icon called "Source" (the
    appearance and labelling of this icon changes depending on whether
    you are using Drupal, Joomla, or WordPress). When you click on it,
    the template changes the view to show the HTML code that is being
    used. If you want to paste in HTML from a template you found
    externally, or if you want to write HTML directly into your template
    or modify the HTML that you've created with the WYSIWYG editor, you
    need to switch to this view. 

Message templates are available even when CiviMail is disabled.

### Tips for creating templates

HTML code allowed in emails is more restricted than HTML used for web
pages. For instance, it needs to use tables for layout, inline CSS, and
must not include background images. Here are some tips for creating a
template that will look good in all mail clients: 

-   **Table border**: The HTML <table> element includes an optional
    border attribute. Since the default value is 0, it doesn't appear
    unless you choose to use it. Adding it (or editing it if it is
    available) and setting it to 1 (e.g. `<table border="1">`) allows
    you to see the edges of your table and helps identify potential
    places to fix problems. Please note that HTML email templates
    usually have multiple tables and nested tables (tables inside
    tables). Make changes one at a time and switch to the HTML view to
    see the results. A table usually has more than one parameter, so
    make sure to place spaces between parameters. 
-   **Table cellpadding and cellspacing**: these table parameters are
    very useful when trying to improve the readability of your email.
    Play with these settings in different tables and see what works for
    you. 
-   **Width**: Do not send an email that is wider than 600 pixels, to
    ensure maximum compatibility across email clients. Make sure your
    outermost table does not exceed 600 pixels. Do the same for any
    other tables inside your main table. Also make sure that the total
    width of each image does not exceed 600 pixels. Images have a width
    parameter, but they can also have a horizontal padding parameter
    that, if set, can increase the width of the image. 
-   **Images**: these need to be online and accessible in order for you
    to use them. First edit your image so that its width and height is
    appropriate for your email template. Next, save it so that its file
    size is as small as possible. If you do not have image editing
    software, or do not know how to use it, there are free online
    resources that can help you resize your image.
-   **HTML editor**: CiviCRM comes with two WYSIWYG editors (CKEditor
    and TinyMCE) and Textarea, a plain text editor. If you have another
    editor configured as part of your Drupal, Joomla, or WordPress
    installation, you can choose to use that instead. go to:
    **Administer** > **Customize Data and Screens** > **Display
    Preferences** > and select a different WYSIWYG Editor.

To see examples of message templates, see
[http://wiki.civicrm.org/confluence/display/CRMDOC/Sample+CiviMail+Messages](http://wiki.civicrm.org/confluence/display/CRMDOC/Sample+CiviMail+Messages)
[](http://wiki.civicrm.org/confluence/display/CRMDOC41/Sample+CiviMail+Messages).

### Plain text and HTML formats

All messages can be sent either in plain text or in HTML. Today the vast
majority of people use email clients that can read messages received in
HTML. However, the best practice is to offer the option to send a plain
text email version to ensure all recipients can view the message. Plain
text email readers may display HTML email as blank. HTML email may also
present accessibility issues to people using screen readers.

However, there is a risk that if users modify an email based on a
template that contains both plain text and HTML, they will forget to
modify the plain text version of this message. This will mean that
people using plain text-only email clients will receive an incorrect or
incomplete message.

One solution to this problem is to either use plain text emails only or
to set templates without the plain text option and ask users to create a
plain text version before sending their mailings.

To create a plain text version of a message from HTML:

1.  Copy and paste the text from HTML Format field into the Plain Text
    Format field. When you do this, make sure you are not in the Source
    view; you don't want all the code, just the text. When you copy from
    the WYSIWYG view, the plain text field will automatically strip out
    the formatting and any other elements that do not work in plain
    text. 
2.  Copy the URLs of all links to the appropriate places in the Plain
    Text Format field.
3.  If the HTML version contained tables, modify the layout of your text
    manually to ensure the text version is readable. 

Creating headers and footers
----------------------------

Headers and footers can be used only in mass mailings using CiviMail.
They are not available unless CiviMail is enabled. 

The header is the area at the top of the email; it should include
elements that you want to be displayed before the main content body,
such as the logo of your organization and the title of the newsletter.

The footer is always the last thing in the email. The footer is an ideal
place for the compulsory unsubscribe tokens (see **What You Need to
Know** for more information).

You can manage the content of headers and footers in **Mailings >
Headers, Footers, and Automated Messages**. You can create different
headers and footers for different purposes; for example, you might want
to create a set of headers with different images and titles that can be
used for different campaigns or programs. It is recommended to style
them similarly, to present a coherent visual identity across all your
messages. 

After headers and footers are configured, staff who prepare a new
mailing will be able to select them from available headers and footers.
This helps staff create more standardized mailings with elements that
help your readers identify the contents of the mailing or find
information.

Like the Message Templates, headers and footers have both a text and an
HTML version. Unlike Message Templates, however, the header and footer
creation pages do not offer a WYGIWYG editor. You will need to write
header and footer HTML directly or use another HTML editor to produce
the HTML code. 

Testing templates
-----------------

Once your templates are ready, we strongly recommend that you test them
in various email clients, such as Mozilla Thunderbird, MS Outlook, Mac
Mail and web-based e-mail such as Gmail, Yahoo and Hotmail. An easy way
to do this is to create a group that includes a test contact for each of
those destinations and use it each time you create a new mailing.

Because email clients can display the HTML very differently from each
other, we recommended that you keep the HTML as simple as possible and
use only inline CSS or tables for formatting. Include as much of the
layout as possible in the templates so that each new mailing will not
require too much reviewing, since the template will have already been
tested.

Auto-filing email conversations in CiviCRM
------------------------------------------

It is possible to have emails sent to and from your regular email client
automatically filed in CiviCRM. This is done by including a designated
email address in the To, Cc, or Bcc field (Bcc is recommended, as it is
invisible to the recipient.) Emails that include this designated email
get filed as an activity for the contact(s) that match the other email
addresses in the From, To, and Cc fields. If any of these email
addresses are not already in the system, a new contact record will be
created. (Technically, this can work for inbound emails as well;
however, it does depend on the person sending the mail to you including
the auto-filing address in the To, Cc, or Bcc field.) 

For this, your administrator should have configured IMAP or other mail
accounts and set them up in CiviMail (see **Email System
Configuration**, especially **Adding an incoming email account for
handling bounces or auto filing to CiviMail**, in **Initial Set-Up** for
more details). 

