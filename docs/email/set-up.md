# Set-up

This chapter describes how to set up information such as From email
addresses, Mailing List Groups and email templates. It assumes that the
basic functionality necessary for your server to send and process emails
in the first place has already been configured. See *CiviMail Setup* in 
the [System Administrator Guide](https://docs.civicrm.org/sysadmin/en/latest)
for details.

## Configuring your organisation's contact information

In order to send mass emails you must fill in some basic information:
your organisation's name, a short description, your email address, and
your postal address. CiviMail requires that you include the sender's
postal address along with unsubscribe/opt-out links in any mass mailing
you send, in order to comply with privacy laws in many countries. This
information is made available via tokens and must be included in any
mail sent with CiviMail.

To configure this information, go to: **Administer > Communications >
Organization Address and Contact Info**.

## Mailing groups

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

1.  Go to **Advanced Search** or **Find Contact** and run a search query
    based on the criteria for your group.
2.  On the search results page, click the radio button that selects all
    the records.
3.  From the **Actions** drop-down menu, select **Group - create smart group**.
4.  The next screen provides a review of the criteria chosen for the
    Smart Group. Give the Smart Group a name and (optionally) a
    description, and make the Smart Group a Mailing List.
5.  Click **Save Smart Group**.

!!! info
    You can also create a Smart Group based on a Participant
    search. However, the Smart Group save page will not offer you the option
    to make this group a Mailing List. To make this Smart Group available to
    CiviMail, you must change its settings through **Contacts > Manage
    Groups**. This same thing happens if you use the Advanced Search and
    choose Event Participants under "Display results as."

You cannot create smart groups based on Membership, Contributions or
Pledge searches, or based on results of an Advanced Search if the
"Display results as" option is set to anything but Contacts.

## Allow people to sign up for your mailing lists online

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

Alternatively, you can use [profiles](/organising-your-data/profiles.md) to collect more information from people who sign up to
your mailing list.

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

Alternatively, for WordPress you can display the form publicly by using a shortcode. On any WordPress Page, click the **CiviCRM** button above the editor. For **Page Type** select **Profile**. On the next drop-down that appears, select the name of the profile that you have created. Select **Edit** on the radio button option just below the drop-downs, so that you give users access to edit data in your database (i.e. to add their email address and name to your database). Click **Insert Form** and the shortcode will be added to the editor.

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

After people subscribe to mailing list groups &mdash; via the subscribe link or
a profile &mdash; CiviCRM will automatically send them an email asking them to
confirm their subscription. Until they click the confirmation link in
the email, their contact information will appear in CiviCRM with their
group subscription set to Pending. When they confirm, CiviCRM will
automatically change their group subscription status to Added and they
will be sent a welcome message.

!!! note
    When users subscribe to multiple groups at once, a confirmation email is 
    sent for each group separately.

## Scheduled jobs and cron jobs

After people have signed up on your mailing list(s), you will want to be able to send them mass mailings. You will also want to automatically handle any bounced email messages. These topics are dealt with in detail in the **Everyday tasks** and **Maintaining Healthy Email Lists** parts of this book, respectively. Here in this section we are going to look at some backend and server options that enable the sending of mass mailings and the bounce handling to happen.

Go to **Administer > System Settings > Scheduled Jobs** and you will see all scheduled jobs that CiviCRM uses to do certain tasks on a regular basis. One such task is the actual sending of mass mailings, which is handled by the **Send Scheduled Mailings** scheduled job. Another task is the processing of bounced emails, for which the **Fetch Bounces** scheduled job is responsible. You will need to enable these two scheduled jobs (and any others that you want to be run on a regular basis). Without these two, CiviMail will not be sending any mailings and will not be processing the bounces.

Now, CiviCRM's scheduled jobs cannot self-trigger themselves. Something on your server has to trigger them. The most common option for this is to set up a cron job on your server. This cron job can trigger one or more (or all) of the scheduled jobs. For more detailed explanations and examples of how to do this, see the [Managing Scheduled Jobs](http://wiki.civicrm.org/confluence/display/CRMDOC/Managing+Scheduled+Jobs) wiki page.

## Automated Messages and mailing list management

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

For more information on email list management see [Maintaining healthy email lists](/email/maintaining-healthy-email-lists.md) which explores how CiviCRM handles
unsubscribes, bounces and email holds.

## Creating headers and footers

Headers and footers can be used only in mass mailings using CiviMail.
They are not available unless CiviMail is enabled.

The header is the area at the top of the email; it should include
elements that you want to be displayed before the main content body,
such as the logo of your organization and the title of the newsletter.

The footer is always the last thing in the email. The footer is an ideal
place for the compulsory [unsubscribe tokens](/common-workflows/tokens-and-mail-merge.md#opt-out).

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

## Testing templates

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

## Auto-filing email conversations in CiviCRM

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

### Allowing users to edit inbound e-mails
 
Activities created by CiviCRM as a result of email-to-activity processing 
are not editable by users, as there is a restriction enforced on the Inbound 
Email activity type. To allow users to be able to edit these activities, an
administrator can enable the **CiviCRM: edit inbound email basic information** 
or the **CiviCRM: edit inbound email basic information and content** permissions
for the roles that require it.

**CiviCRM: edit inbound email basic information** will allow users to edit every
field of the activity, except the original message, stored int the activity's 
details.

**CiviCRM: edit inbound email basic information and content** will allow users
to edit every field of the activity, including the original message's content.
