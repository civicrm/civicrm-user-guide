Email System Configuration
==========================

This chapter covers system configuration necessary so that CiviCRM can
send and receive email. This is a complex task which requires system
administrator level skills. The correct configuration of your email
system is crucial to keep your server off spam lists and black lists.

See the Email sections chapter on Set up for tasks necessary to set up
the sending of messages once these email system configuration settings
have been configured.

Some parts of the configuration are core CiviCRM functionality (basic
sending and receiving of emails) whereas others (mass mailings) require
that the CiviMAIL component be enabled. 

You will need to be able to change the configuration of your DNS, create
email accounts, configure a cron job, read the headers of email
messages, and possibly change the configuration of your SMTP server.

This chapter assumes you are running CiviCRM on a Linux server and that
you are comfortable working with the shell and running some simple
commands. Most of these steps will be similar on other operating
systems, but you will need to adapt them to your system and tools.

The configuration described works fine for mailings to up to about
10,000 people. If you plan on sending email to hundreds of thousands of
contacts, you should benchmark several options and consider a dedicated
SMTP server. This more complex configuration is outside the scope of
this book but you can find community contributed instructions on the
CiviCRM documentation
wiki. ([http://wiki.civicrm.org/confluence/display/CRMDOC/CiviMail+Installation](http://wiki.civicrm.org/confluence/display/CRMDOC/CiviMail+Installation)).

In this chapter we'll use an external Gmail mailbox address to test
configuration. So the first step is to create a Gmail account if you
don't have one already; alternatively, you can use another address for
testing the procedures in this chapter, but you will need to be able to
view the source of the mails you receive.

Once your system is properly configured we are going to use cron to
trigger CiviCRM's **Scheduled Jobs** to ensure your scheduled mailings
are sent. 

Configuring outbound email service
----------------------------------

Outbound email settings are configured at: **Administer > System
Settings > Outbound Email (SMTP/Sendmail)**. The choices here are:

-   **mail()**: This is the default option and if it works for you, you
    should use it. 
-   **SMTP**: If you have a dedicated external mail server, specify its
    details here. Bounce messages generated with SMTP are slightly more
    complete than the ones from mail(), but there is no practical
    benefit to using SMTP if you can use mail(). 
-   **Sendmail**: This option is kept for compatibility with older CiviCRM
    versions. 
-   **Disable Outbound Email**: Works as expected.
-   **Redirect to Database**: All emails will be recorded as archived mailings instead of being sent out. They can be found in the civicrm\_mailing_spool table in the CiviCRM database.

After making a choice, send a test email to your account on Gmail and
verify that you receive it.

If you receive the following error message, you'll need to configure a
default FROM email address (covered in the chapter on CiviMail
configuration). 

```
Sorry. A non-recoverable error has occurred. 
The site administrator needs to enter a valid 'FROM Email Address' in
Administer -> Configure -> Domain Information. 
The email address used may need to be a valid mail account with your
email service provider.
```

Once you have received the email, you will need to view the source.
This is done in Gmail by clicking on "Show original" in the email you
receive.

The email should contain headers that resemble the following.

```
Received: from yourmailserver.example.org (xxx.example.org
[12.45.120.30]) 
by mx.google.com with ESMTP id e31si4519230wej.3.2010.04.26.00.38.16; 
Mon, 26 Apr 2010 00:38:17 -0700 (PDT) Received-SPF: pass 
google.com: best guess record for domain of
[youremail@example.org](mailto:youremail@example.org) designates 
 12.45.120.30 as permitted sender) client-ip=12.45.120.30
 ```

In particular:

* "Received: from" header should correspond to your mail server and be
properly configured. It might contain information about your hosting
provider instead of your domain name. This is not a problem as long as
the mail server is properly configured. If you have a dedicated IP
address for your server, you should try to configure a reverse DNS that
represents your organization instead of the default name.

* "Received-SPF" header should list "pass" or "neutral". Sender
Policy Framework is described later in more detail. 

Sending mass mailing is resource intensive. We don't recommend sending
email messages from budget hosting providers. The time you will spend
troubleshooting will often cost more than upgrading to a more
professional host. Check with your hosting provider to find out whether
they limit the number of email messages you can send and whether they
run PHP in safe mode.

Some of your recipients' mail servers use DNS based blacklisting
services (DNSBL) which keep a blacklist of IP addresses likley to send
spam. Mail from these servers will be flagged as spam and not reach its
intended destination. If your server is blacklisted (for instance,
because enough of your recipients flagged your email as spam, or because
another website on your server has been flagged as spam), you will need
to contact the organizations that have blacklisted you and convince them
to remove you from their list.

They are several websites that help you testing whether you are in a
DNSBL. A web search for "blacklisting email" will turn some up. Test
regularly to find whether you are on a blacklist.

Configuring Sender Policy Framework (SPF)
-----------------------------------------

By default, the Internet allows any mail server to send any email
claiming to be from anyone. This makes it easy for spammers to forge
addresses and send spam using your email address (or any other). SPF
allows you to create a special DNS record listing the IP addresses of
the mail servers that can legitimately send email from
@*yourdomain.org*.

If your domain name already has an SPF record, make sure that it
includes the IP address of your CiviCRM mail server (which might be a
different from the host used for the web server or from your mail
servers), and if it doesn't, add this IP address.

If you don't have an SPF record, consider adding one. You will need to
add at least your mail server and CiviCRM server (if they are different)
to the SPF record.

You can read more about SPF at
[http://www.openspf.org](http://www.openspf.org).

##Configuring inbound email processing

This section explains configuration for bounce processing and auto
filing incoming emails. Configuring **Scheduled Jobs** to do the actual
bounce processing is discussed later in this chapter. 

### Bounce processing 

CiviCRM can automatically receive the [bounced email
notification](http://en.wikipedia.org/wiki/Bounce_message) and, based on
the [type of bounce](http://tools.ietf.org/html/rfc3463) reported by the
recipient's server, flag your contacts accordingly. To accomplish this
you will need to set up an email mailbox to receive bounced email
messages and a schedule the **Bounces Fetcher** job that will
periodically read this mailbox and update your contacts in civicrm.

The bounce email address is an "invisible" email address visible only in
the email message's envelope (hidden fields that precede the headers and
message added by the user). Choose any name you like that is meaningful
to you. In this example we have chosen *return*, so the email address we
need to set up on a mail server for example.org is *return@example.org*.

For each email sent via CiviMail's mass mailing feature, a new unique
"invisible" sender address is created using the [variable envelope
return path or
VERP](http://en.wikipedia.org/wiki/Variable_envelope_return_path). When
CiviCRM receives a bounce, it looks at the invisible sender address to
decide which email bounced. 

CiviCRM then looks a the bounce pattern and type to decide what action
to take. Bounce types fall into two basic categories: permanent failures
(hard bounce) and transient failure (soft bounce). A single
permanent failure triggers CiviCRM to set the contact's email as on
hold. For transient failures, CiviCRM waits for several bounces before
setting the contact's email on hold.

The specific [threshold for each bounce
type](http://wiki.civicrm.org/confluence/display/CRMDOC43/Bounce+Handling)
can be found in the civcirm_mailing_bounce_pattern and
civicrm_mailing_bounce_type. Multiple different bounce reply patterns
are linked to a given type and threshold. 

### **Email-to-Activity processing**

CiviCRM can automatically retrieve email from a specified inbox and file
it as an email activity against contacts of type Individual corresponding to sender and recipients of the email. New individual contacts are created for email adresses not already assigned to individuals in the database. 

**NOTE**: This features only works for the Individual contact type. If the incoming email comes from an email address already record aginast an organization, a new individual contact with that same email address with be created and the activity will be recorded against that new individual contact, not against the organization.

There are two ways to do this (either or both ways can be setup at same
time):

-   **Special email address:** Set up a special email address for your
    organization, e.g. civiemails@example.com. Users can then add this
    address in the Bcc field for your outbound emails; they will get
    auto filed in CiviCRM as described above. No one who receives the
    email will see this special address if the Bcc field is used. 
-   **IMAP Folder:** Set up a folder in your IMAP Inbox where you can
    drag emails that you want filed in CiviCRM. This works with both
    inbound and outbound emails. (this requires that your email be set
    up using IMAP.)

### Special email address for incoming email

There are several ways of configuring your incoming mailbox:

-   **Sub-addressing:**Your mail service might allow you to append a
    +*tag* or -*tag* qualifier to your e-mail address (e.g.
    *return+test@example.org*). Several mail servers, including Gmail,
    Yahoo! and Postfix provide this sub-addressing by default.

    Try to send yourself an email, adding a +*tag* or -*tag*. If you
    received the mail you sent with a tag, it means that you can
    directly use the mailbox you created (*return@example.org* in our
    example) as the VERP.

-   **"Catch-all" account:** If sub-addressing doesn't work on your mail
    server, you need to define the mail account you created
    (*return@example.org*) as the "catch-all" account. Every mail sent
    to an address that isn't a real mail account will end up there,
    including all the bounced email messages.

-   **External address**: If neither of the preceding methods works,
    consider creating a new account on a service such as Gmail and use
    it to receive the bounced emails. You will have to set filters in
    this account so it doesn't discard as spam all the bounced email it
    will receive. 

### Adding an incoming email account for processing bounces and/or email-to-activities

Once you have created your email account to receive bounces or emails
for auto filing, you need to set up CiviMail so it knows how to read it:
**Administer > CiviMail > Mail accounts** as the default email
address.

-   Specify the mail **server, username, and password** you used when
    creating the account.
-   The **local part**is optional and only relevant if you were able to
    set up an account using sub-addressing. It should be the account you
    created with '+' or '-' appended , e.g., "return+" or "return-".
-   The **email domain**is the domain of your email address
    (example.org).
-   You can leave the **return path** empty.
-   If your mail server supports it, specify IMAP **protocol**and check
    **SLL**, otherwise use POP. 
-   You can specify an IMAP folder in the **source** field using the
    syntax INBOX.CiviMail. **Note:**Some exchange servers may not be
    configured in a compatible way. In that case, you can configure a
    script like fetchmail and use Maildir. 
-   In the **Used for?** field you can choose whether you want to use
    the email account for **Bounce Processing** or **Email-to-Activity
    Processing** (or Auto filing). You can have multiple accounts
    specified for auto filing but only one for bounce processing. This
    will be marked as default. 

Once the **Bounce Processing** mailbox is configured, you will need to
configure CiviMail to empty it, read all these bounced messages and
identify the related bounced contacts. This is performed by the
Scheduled Jobs feature of CiviCRM . 

We recommend testing the bounce process by running the process manually
before setting up CiviCRM to process the bounced email messages
automatically. This can be done in **Administer > System Settings >
Scheduled Jobs**. Locate **Fetch Bounces** and select **more > Execute
Now**. Check the Job Log for any error messages. 

Once you have verified that CiviCRM can properly handle the bounce, you
can set it up to automatically process the replies and bounces on a
regular basis.

##Scheduling inbound and outbound mail processing

As discussed in the earlier chapter, mail processing and other jobs may
be automated through the Scheduled Jobs administrative page, cron or a
combination of both. The full range of options is discussed in the
[Manage Scheduled Jobs wiki
page](http://wiki.civicrm.org/confluence/display/CRMDOC43/Managing+Scheduled+Jobs),
but below are specific examples for enabling CiviCRM mail processing.

### Scheduling using the Scheduled Jobs administrative page

Mass mailings are generated via the CiviMail web interface and are
queued to be sent to their recipients. To schedule the regular
processing of this queue and any bounces that are returned go
to **Administer > System Settings > Scheduled Jobs** and find
the **Fetch Bounces** and **Send Scheduled Mailings** jobs. Edit each in
turn, setting their scheduled **Frequency** to "Hourly", "Daily" or
"Every time cron is run". The defaults should be fine for small
installations. Then select **more > Enable** for each.

In this example using the jobs' default frequency and [cron configured
to run at 15 minute
intervals](http://wiki.civicrm.org/confluence/display/CRMDOC/Managing+Scheduled+Jobs),
scheduled mailings would be sent every 15 minutes and bounces would be
fetched and processed hourly.

If you need to send some email from CiviCRM right away, without waiting
for the cron job, you can trigger the sending process by
visiting **Administer > System Settings > Scheduled
Jobs **select **more > Execute Now**. Use this capability sparingly. It
could utilize a lot of server resources and cause CiviCRM to slow down
noticeably. The administrative settings for sending email are usually
configured to minimize the load on the server, and the scheduling the
job is a more efficient way to send mass email.

### Scheduling only the mail jobs using the command-line interface

As an alternative on Linux and other Unix or Unix-like systems,
individual cron jobs may be used to schedule inbound and outbound mail
processing rather than the **Scheduled Jobs** page. This approach gives
experienced system administrators more granular control over these
processes by configuring specific cron jobs apart from other scheduled
jobs.

The cron job needs to run using an account recognized by your CMS.
Create an account dedicated to this task (e.g., *mailprocess, civimail,
etc*), give it a long, secure password (e.g. *seol-lzprm42amv-psyc*) and
grant it access to CiviCRM, CiviMail, and view all contacts. Do not
change the account password without changing the password in the
configuration files of this cron job.

To set up your cron job, first, find out whether php-cli is installed.
From the shell, type *php -v*. If you see **(cli)** in the result, as
in:

```
PHP 5.2.3-1ubuntu6.5 (cli) (built: Feb 11 2009 19:55:53) Copyright (c)
1997-2007 
 The PHP Group Zend Engine v2.2.0, Copyright (c) 1998-2007 
 Zend Technologies with eAccelerator v0.9.5.3, Copyright (c) 2004-2006 
 eAccelerator, by eAccelerator
 ```

This means you have php-cli installed and you should use it, because it
has several advantages:

-   You can run a PHP script at a lower priority than your web server,
    so that even if it takes a lot of CPU, it won't interfere with the
    regular users of your site.
-   You can set different memory limits for the php-cli process and the
    PHP process used by your web server.
-   You avoid the overhead of the web server and the HTTP layer.
-   You won't have any timeout problems.

The following is complete cron configuration to handle CiviCRM's mail
requirements: 

```
# This must be set to the directory where civicrm is installed. 
CIVI_ROOT=/var/www/civicrm 
 
 # Comment: I believe these two lines are unnecessary. 
# USER=www-data 
# MAILTO="you@example.org" 
 
 # Location of the PHP Command Line Interface binary. 
# nice -19 forces to run at a lower priority than the web server 
PHP=nice -n19 /usr/bin/php 
 
# line to be modified according to the informations below 
# like this: PARAMS= -j -s<default or domain> -u<user>
-p<password> -e Job -a process_mailing 
 
PARAMS= -j -sdefault -umailprocess -pseol-lzprm42amv-psyc -e Job -a
process_mailing 
PARAMSBOUNCE= -j -sdefault -umailprocess -pseol-lzprm42amv-psyc -e Job
-a fetch_bounces 
 
 # cronjob send 
# m h dom mon dow command 
*/5 * * * * cd $CIVI_ROOT; $PHP bin/cli.php $PARAMS 
*/15 * * * * cd $CIVI_ROOT; $PHP bin/cli.php $PARAMSBOUNCE
```


The user that run the scripts (*www-data* in this example) needs to be
able to write into the temporary folder. Your configuration might
specify a different user.

You don't have to run both scripts at the same frequency. The preceding
crontab file verifies every 5 minutes whether mail messages need to be
sent, but only every 15 minutes whether bounced email needs to be
processed.

**PARAMS** contains:

1.  The site you used, which is **-sdefault** on Drupal. If you run
    multiple CiviCRM sites on a single server, you need to specify your
    site's domain, such as **-sexample.org**.
2.  The user login account (**-umailprocess**). 
3.  The password you defined (**-pseol-lzprm42amv-psyc**).

