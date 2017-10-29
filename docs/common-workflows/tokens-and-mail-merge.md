# Tokens and mail merge

You can use data in your CiviCRM database to set up mail merge
communications both for emails and printed materials such as letters and
mailing labels. The mail merging functionality relies on Tokens, which
represent items in your database. This chapter explains how tokens work
and how to use them in generating printing materials. Using tokens in
emails is further addressed in the Email section of this book.

## Tokens

Tokens are the equivalent of mail merge fields in CiviCRM. This means
that it is possible to insert information from the database into an
email or a letter that is different for every recipient. For example,
use the Postal Greeting token to include a customized greeting for each
recipient in your PDF letters. Most contact fields, including custom
fields you've created, are available as mail merge tokens. You can view
available tokens by clicking the **Insert Token** link in the top right
corner of the message editing area.

Most of the tokens contain information that is in the database fields.
However, there are some special tokens that accomplish specific tasks in
emails, such as a link to an opt-out page or link to choose mail
formats. Some tokens are only available for mass mailings, such as the
token to provide a link to a message stored online.

![New email screen with the token list expanded.](../img/Tokens-4.5.png)

CiviMail uses a number of **action** and **mail-merge tokens** and which can be placed in mailing labels, PDF letters, email messages and message templates, mailing headers and footers, and system-workflow (automated) messages. These tokens are converted dynamically to text, reply-to email addresses, and URLs.

The best source of documentation for tokens is the [token page within the User Guide](https://docs.civicrm.org/user/en/stable/common-workflows/tokens-and-mail-merge/).

This page gives supplemental information for working with tokens. [You can also customize or create new tokens relatively painlessly](/framework/civimail/index.md#extending-the-token-system).

This table documents the available action tokens, their purpose and the place(s) they can be used.

| Token | Purpose | Where used... | Example | 
| --- | --- | --- | --- |
| **{action.forward}** | Provides a link for each recipient to forward the mailing to others.| Mailing Body, Header, Footer| To forward this mailing to friends or colleagues, click `<a href="{action.forward}" >here</a>`.| 
| **{action.optOutUrl}** | Provides an opt-out link for each recipient.| Mailing Body, Header, Footer,unsubscribe,resubscribe| To opt-out of all future mailings from us, click `<a href="{action.optOutUrl}" >here</a>`.| 
| **{action.optOut}** | Provides an opt-out email address for each recipient.| Mailing Body, Header, Footer,unsubscribe,resubscribe| To opt-out of all mailings from us, send mail to {action.optOut}| 
| **{action.reply}** |  Provides a reply-to email address for each recipient| Mailing Body, Header, Footer,unsubscribe,resubscribe| To reply to this mailing, send mail to {action.reply}| 
| **{action.resubscribeUrl}** | Provides a re-subscribe link for each recipient| Mailing Body, Header, Footer,unsubscribe,resubscribe| To resubscribe to this mailing, click `<a href="{action.resubscribeUrl}" >here</a>`.| 
| **{action.resubscribe}** | Provides a re-subscribe email address for each recipient.| Mailing Body, Header, Footer,unsubscribe,resubscribe| To resubscribe to this mailing, send mail to {action.resubscribe}| 
| **{action.subscribe.gid}** | Provides an email address to subscribe to a specific group.| Mailing Body, Header, Footer| To subscribe to our Monthly Newsletter, send mail to {action.subscribe}.| 
| **{action.subscribeUrl.gid}** | Provides a link to subscribe to a specific group (gid = CiviCRM ID of that group).|   Mailing Body, Header, Footer|  To subscribe to our Monthly Newsletter, click `<a href="{action.subscribeUrl.2}" >here</a>`.| 
| **{action.subscribeUrl}** | Provides a link to view and subscribe to any public mailing lists.| Mailing Body, Header, Footer| To see our mailing lists and join the ones you're interested in, click `<a href="{action.subscribeUrl}" >here</a>`.| 
| **{action.unsubscribeUrl}** | Provides an unsubscribe link for each recipient.| Mailing Body, Header, Footer,unsubscribe,resubscribe| To unsubscribe from this mailing, click `<a href="{action.unsubscribeUrl}" >here</a>`.| 
| **{action.unsubscribe}** | Provides an unsubscribe email address for each recipient| Mailing Body, Header, Footer,unsubscribe,resubscribe| To unsubscribe from this mailing, send mail to {action.unsubscribe}| 
| **{contact.custom_nn}** | Displays content of custom contact field nn | Mailing Body, Subject, not sure about elsewhere | Thanks for indicating your interest in {contact.`custom_1`}. We will keep you updated on that topic.| 
| **{contribution.custom_nn}** | Displays content of custom field nn for the contribution | Mailing Body, Subject, not sure about elsewhere | Thanks for indicating that if your first choice for where we should use your contribution is {contribution.`custom_42`}.|
| **{domain.address}** | Displays postal address for your domain.| Mailing Body or any message templates | Mailing Address:  {domain.address}| 
| **{domain.email}** | Displays email address of domain.| Mailing Body or any message templates|  Or send a mail to {domain.email}.| 
| **{domain.name}** | Displays your domain name.| Mailing Body or any message templates| This mailing is from {domain.name}.| 
| **{domain.phone}** | Displays phone number of domain.| Mailing Body or any message templates| To contact us call {domain.phone}.| 
| **{mailing.group}** | Displays a listing of the names of the groups to which a mailing has been sent.| Mailing Body, Header, Footer,resubscribe,unsubscribe or optout| This mailing has been sent to the members of {mailing.group}.| 
| **{mailing.name}** | Displays name of mailing.| Mailing Body, Header, Footer,resubscribe,unsubscribe or optout| Name of this mailing is {mailing.name}.| 
| **{mailing.viewUrl}** | Will create a 'View in Browser' url | Mailing Body  | Can't see this email? `<a href="{mailing.viewUrl}"><strong>View in Browser</strong></a>`|
| **{resubscribe.group}** | Displays group name in re-subscribe messages.| Resubscribe Message| As requested, you have been resubscribed to {resubscribe.group}.| 
| **{subscribe.group}** | Displays group name in subscription confirmation requests.| Subscription confirmation request | You requested to be subscribed to the {subscribe.group}.| 
| **{unsubscribe.group}** | Displays group name in unsubscribe confirmation messages.| Unsubscribe Message| You have been unsubscribed from {unsubscribe.group}.| 
| **{welcome.group}** | Displays the newly joined group name in a welcome messages.| Welcome message| Welcome to {welcome.group}.| 


### Checksum token

A particularly useful token is the checksum. The checksum allows you to
give people links to contribution forms, profiles, petitions, and event
registration forms that are prefilled with information that is already
in their contact record. The image above shows an example of this.

Only contact fields and actions can be inserted in your email as tokens.
Related records, such as the name of the event for which the contacts
have pending enrollments, cannot be included. However, you could provide
a link to the person's contact dashboard so that they can review their
registration details for themselves (once logged in), or you could use a
checksum token to allow access to a profile through which they can
modify their information without having to log in.

There is a very powerful feature to allow you to send an email with CiviMail to your constituents with a link to the contribution form, profile, or event registration form with all of their contact information already filled in! This saves them the hassle of filling it out and increasing the chances they would ultimately donate.  Or it can be a simple way to periodically allow people to review their contact info and update it if applicable.

The way it works is you create a "special" link in the CiviMail message that includes the checksum token `{contact.checksum}`. When people click on the special link, it looks them up in the database and prefills any information on the contribution form or profile with any data that exists in their record. The special link lasts for seven days from the time it was sent out.

DEVELOPER NOTE: the checksum token outputs the QS param, so if you are building a URL using `CRM_Contact_BAO_Contact_Utils::generateChecksum()`, you should include 'cs='

**Checksum for Contribution Pages**: To send people to a contribution page use this path where **IDNUMBER** is the ID of your contribution page:

-   Drupal: `http://www.myorganization.org/civicrm/contribute/transact?reset=1&id=IDNUMBER&{contact.checksum}&cid={contact.contact_id}`
-   Joomla!: `http://www.myorganization.org/index.php?option=com_civicrm&task=civicrm/contribute/transact&reset=1&id=IDNUMBER&{contact.checksum}&cid={contact.contact_id}`
-   WordPress: `http://wwww.myorganization.org/?page=CiviCRM&q=civicrm/contribute/transact&reset=1&id=IDNUMBER&{contact.checksum}&cid={contact.contact_id}`

**Checksum for standard Profiles** (edit mode): To send people to a profile use this path where **IDNUMBER** is the ID of the Profile you want to send them to:

-   Drupal: `http://www.myorganization.org/civicrm/profile/edit?reset=1&gid=IDNUMBER&{contact.checksum}&id={contact.contact_id}`
-   Joomla!: `http://www.myorganization.org/index.php?option=com_civicrm&task=civicrm/profile/edit&reset=1&gid=IDNUMBER&{contact.checksum}&id={contact.contact_id}`
-   WordPress:`http://www.myorganization.org/?page=CiviCRM&q=civicrm/profile/edit&reset=1&gid=IDNUMBER&{contact.checksum}&id={contact.contact_id}`

**Checksum for Event Registration Pages**: To send people to an event registration page use this path where **IDNUMBER** is the ID of your event:

-   Drupal: `http://www.myorganization.org/civicrm/event/register?reset=1&id=IDNUMBER&{contact.checksum}&cid={contact.contact_id}`
-   Joomla!: `http://www.myorganization.org/index.php?option=com_civicrm&task=civicrm/event/register&reset=1&id=IDNUMBER&{contact.checksum}&cid={contact.contact_id}`
-   WordPress: `http://wordpress.demo.civicrm.org/?page=CiviCRM&q=civicrm/event/register&reset=1&id=IDNUMBER&{contact.checksum}&cid={contact.contact_id}`

**Checksum for Petition Signature Pages**: To send people to sign a Petition, use this path where **IDNUMBER** is the ID of your petition:

-   Drupal: `http://www.myorganization.org/civicrm/petition/sign?reset=1&sid=IDNUMBER&{contact.checksum}&cid={contact.contact_id}`
-   Joomla!: `http://www.myorganization.org/index.php?option=com_civicrm&task=civicrm/petition/sign&reset=1&sid=IDNUMBER&{contact.checksum}&cid={contact.contact_id}`
-   WordPress: `http://www.myorganization.org/?page=CiviCRM&q=civicrm/petition/sign&sid=IDNUMBER&reset=1&{contact.checksum}&cid={contact.contact_id}`

### Custom tokens

It is also possible to have custom tokens created by a developer. For
instance, the total amount of contributions from a contact. To find out
more about working with custom tokens, refer to the discussion about
custom mail merge tokens in the Hooks chapter of the Extending CiviCRM
section of this book and look at the wiki:
[http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens](http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens).

### Smarty in mail templates

Mail templates use Smarty to include variables, tokens & functions. A more thorough tutorial can be found at [http://www.smarty.net/manual](http://www.smarty.net/manual).

!!! warning "System administrator required"
    For Smarty to work you must add (or modify) the following line to your `civicrm.settings.php` file located under `sites/default/` for Drupal and `administrator/components/com_civicrm` for Joomla.

    ```php
    define('CIVICRM_MAIL_SMARTY', 1);
    ```

Tips

* To make CiviCRM tokens available to Smarty functions, you'll need to use the `{capture}` function as follows:

    ```smarty
    {capture assign=first_name}{contact.first_name}{/capture}
    Dear {$first_name|default:Friend},
    {if $first_name}
      Hello, {$first_name}, how are you?
    {/if}
    ```

* You also need to use `{capture}` for custom fields. For example, if `{contact.custom_16}` is a Yes/No field designating a membership as a gift, and `{contact.custom_17}` is a text field with the name of the gift giver, then the following will print a line to that effect in a PDF letter:

    ```smarty
    {capture assign=gift}{contact.custom_16}{/capture}
    
    {if $gift == Yes}
      This membership is a gift from {contact.custom_17}.
    {/if}
    ```

* Another possibility is to create if/then logic for your mail
merge. This is done using the smarty template language as described here
[http://www.smarty.net/docs/en/language.function.if.tpl](http://www.smarty.net/docs/en/language.function.if.tpl).
