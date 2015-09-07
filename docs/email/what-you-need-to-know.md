What You Need To Know
=====================

This chapter outlines some key concepts and questions that are useful
for planning the use of CiviCRM's email capabilities. This chapter
should be read before you start sending emails to contacts. Detailed
information on how to carry out the activities mentioned can be found in
the **Everyday Tasks** section. 

Key Concepts
-------------

As you might expect for a web-based CRM, email plays a central role in
CiviCRM. Broadly speaking, there are three situations in which email is
sent from CiviCRM:

-   to individuals and small groups of people via the Send Email action
-   to a large group of people as a mass mailing via CiviMail
-   to individuals who trigger an email as part of workflows in other
    components, for example, an event registration confirmation email  

The advantage of sending email through CiviCRM (rather than through your
email client or through a bulk email tool other than CiviMail) is that
every email sent, via the Send Email action or using CiviMail, is
treated as an activity and stored in the activity history of each
recipient. This allows you to see, for example, that John Doe made a
donation three days after he received your April newsletter, or that
your volunteer coordinator emailed Jane Smith and asked her to staff the
information table at an upcoming event. 

### Send Email versus CiviMail 

CiviCRM offers two options for sending email to contacts:

-   Send an email as an activity for a contact: this is suitable for
    sending emails to individuals and small groups.
-   Send a mailing to a group using CiviMail: this is ideal for mass
    mailings or scheduled emails to small groups.

In order to send mass emails, the CiviMail component must be enabled and
set up (see the Set-up chapter in this section for details). The Send
Email action is available even when the CiviMail component is disabled.

There are crucial differences between the Send Email action and the
CiviMail component:

-   Emails sent via the Send Email action are limited to a maximum of 50
    email addresses, and there is no reporting other than an activity
    record for each recipient.
-   CiviMail emails have sophisticated bounce processing and reporting.
-   CiviMail allows recipients to manage their own subscriptions.
-   CiviMail can be configured to automatically track replies.

CiviMail requires more work to configure, and there are more steps
involved; however, once you have enabled and configured CiviMail, you
will have greatly enhanced mass email capabilities.

Working out which method to use for each email might not be immediately
apparent. Over time, the best practices and the right tool for each
situation will become more obvious and can be shared among your users.

#### When to use the Send Email action

As long as you are contacting fewer than 50 recipients and you don't
need to track whether recipients opened the email or clicked on any
links, the Send Email action is quicker and easier than sending a mass
mailing in CiviMail.

The Send Email activity offers all the functionality of sending through
an email client: you can attach files, CC and BCC contacts, and use
message templates. 

Note that CiviCRM records only the messages you send; replies from the
recipient come to your email address and are not recorded in the
database. For this reason, you should not rely on the Send Email action
for conducting extended email exchanges. If you want to record the fact
that you had an email exchange with somebody, you could create an
activity called Email Exchange and copy and paste your email
conversation in the body as you would a record of a telephone call.

You can also record emails sent through your email client using the
autofiling outbound email option described below.

#### When to use CiviMail 

If you want to send mail to 50 or more contacts at once, you must use
CiviMail.

You also should use CiviMail whenever you want to capture statistics
about the success of your mailing, including bounce statistics and
click-throughs. For more information on this, see **Reporting and
Analysis**. 

CiviMail also enables people to sign up for your mailing lists on your
website, and automatically keeps track of their unsubscription or
opt-out requests. It also lets you file any emails that your recipients
send as replies to the mailing, and send them an autoresponse to their
replies.

### Choosing recipients

Send Email allows you to choose recipients in two ways: from a contact
record and from search results. 

CiviMail also allows you to choose recipients in two ways: with Groups
marked as Mailing Lists, which must be created prior to setting up your
mailing, and from search results. However, there is one complication
with using search results: All mail sent from CiviMail must have an
unsubscribe link. If recipients are included in a Group, any unsubscribe
requests simply remove them from the mailing list for that Group. But if
they are not in a Group, they must be added to one when they unsubscribe
so the unsubscription request can be recorded in CiviCRM. 

### Personalisation with tokens 

Emails sent with both Send Email and CiviMail can include personalised
text, such as a person's name. This is done with tokens, which are
placeholders that CiviCRM recognizes and replaces with an appropriate
value when sending each message. You can include tokens for standard
fields and also custom data fields that you have created. Note that
there are some tokens available in CiviMail that are not available in
the Send Email activity.

A particularly useful token is the checksum. The checksum allows you to
give people links to contribution forms, profiles, petitions, and event
registration forms that are prefilled with information that is already
in their contact record. 

This saves your constituents the hassle of filling out forms and
increases the chances they will take action (e.g., donate, sign up for
an event, sign the petition). It can also be a simple way to keep your
data current by asking people to review and update their contact
information.

Detailed instructions for using tokens, including custom tokens and
using checksums, are available in the **Everyday Tasks** section,
under the heading "Using tokens in emails." 

### From Email Addresses 

Both mass and regular email can be sent from your personal address, from
a general email address associated with your organisation, or from
another person's address. For example, an assistant can send official
email messages under the name of his manager.

### Headers and Footers

In mass mailings only, you can include customised headers and footers.
You can configure custom headers and footers under **Administer >
CiviMail > Headers, Footers, and Automated Messages**. 

### Templates

Templates for emails or parts of emails help to streamline your
communications by reusing entire emails or parts of emails such as
headers and footers. Email templates can be created either beforehand or
when you send an email, and edited at any time.

### Reporting

CiviMail can track mass mailings, providing useful information to help
you understand the areas your recipients are interested in and gauge the
effectiveness of your communications. You can track how many recipients
opened the email and which links in the email were popular.

#### Mailing List Sign-Up and Unsubscribing

CiviCRM allows you to publish a sign-up page or form (called a profile)
where people can sign up for your mailing list on your website. It
requires that you allow recipients to unsubscribe from any mailing list
*and* opt out of ever getting email from you, and CiviCRM will
automatically keep track of these requests. For more information, see
the **Set-Up** chapter. 

### Autofiling external emails in CiviCRM

CiviCRM lets you automatically record email sent via your email client
in contact records in your database. To do this, you need to set up a
special email address that you include in the BCC field of an email you
are sending. This will be read by the database and converted into an
activity. This activity gets filed in the record of the contact that
matches the email address. If that email address does not exist in your
database a new contact record will be created. See the **Email System
Configuration** chapter of the **Intial Setup** section for details.

Key Questions
-------------

When planning your use of CiviCRM's email capabilities, it may be
helpful to answer these questions to guide your setup and use:

-   Are there any types of emails that you send again and again and thus
    want to create templates for?
-   Is there content you'd like to include in the header and/or footer
    in every mailing?
-   Do you want a web page where people can sign up for your emails?
-   What kinds of emails are important to you to store in recipients'
    contact records? 

When planning to send a specific email through CiviCRM, it is helpful to
consider the following:

-   How many people are you sending your email to?
-   Do you want to know who is opening your email and clicking on links
    in it? 
-   Have you created a list (a Group or Smart Group) to which to send
    your email?
-   Do you want recipients to be able to view your mailing in a browser
    window if they have trouble viewing it from their email browser?
-   Who should be the sender of the email? This could be a generic
    organisation address, or personalised with someone's name.

### **Other considerations**

### 

Many CiviCRM components interact with email functionality and with
CiviMail, for example to send confirmation, thank-you and receipt
emails. The sections of this book relating to each component will
include some information about customising these emails, and should be
read in conjunction with this section in order to give you a full
understanding of how email works in the broader context of CiviCRM.

#### Privacy issues

We encourage you to consider privacy issues. Different countries have
different laws relating to email privacy, including opt out/unsubscribe
options. There may also be issues related to CiviMail's tracking tools;
for instance, you may wish to avoid tracking who has clicked on the "how
to deal with drug issues*"* link on a specific mailing.

#### Spam and email deliverability

When sending mass emails, there is always a risk that your emails will
be marked as spam. This affects both the delivery of your current email
and also the future delivery of all emails sent from your server.
Managing these issues is complex and outside the scope of this book. If
your organisation does not have a system administrator, consultant, or
email hosting service that is knowledgeable about these issues, you may
want to seek the advice of an expert. 




