What is CiviMail?
=================

The CiviMail component is a sophisticated tool for handling mass email
campaigns. It can reliably deliver a high volume of email and provide
detailed reports on the results and effectiveness of those emails.
CiviMail is often used to complement other CiviCRM components, for
example to send emails to non-members to encourage them to become
members or to send emails to people that are yet to register for an
event. 

CiviMail (like all of CiviCRM's mail features) interacts with your mail
server. Configuring the mail server and properly setting up CiviMail are
system administrator tasks and you may require professional assistance.
You will also need to check with your web hosting provider to ensure
that they meet the configuration requirements, and find out about any
limits they may have on how many emails you can send per day. A
misconfigured mail server is a liability and if you don't know what you
are doing you could easily end up on a spam black list. Getting off a
spam black list is much harder that getting on it. For more information
about configuring your mail server, see the "Email system configuration"
chapter in the Initial Setup section.

Scenario: managing email lists
-------------------------------

St Ethelburga's Centre for Peace and Reconciliation uses CiviEvent to
run a yearly event programme on a number of different themes. They have
set up a mailing list page where people can sign up to be informed of
events that interest them. They then use CiviMail to send out emails to
those people based on those events. When someone unsubscribes from an
event theme mailing list, CiviCRM keeps a record of the fact that they
have unsubscribed.

St Ethelburga's also automatically subscribes anyone who has been to an
event on a specific theme to receive emails about that theme. They don't
have to worry about spamming people that have unsubscribed from a
thematic event mailing list, as CiviCRM will remember that they have
unsubscribed and not re-subscribe them.

From time to time, St. Ethelburga's sends out other emails to a mailing
list that includes nearly all contacts in their database with personal
messages from the centre director highlighting particular issues. Often,
two similar versions of the same email are sent to different groups in
their database to test which message formats are more effective. They
can do this by sending the email to half the contacts in a particular
group and then sending another email which excludes contacts that have
already received the first email.

Scenario: mobilising with email
-------------------------------

The Townsville Organisation For Tenants (TOFT) held a survey and
petition to gather data and support for the campaign Demand Affordable
Public Housing. The survey was undertaken by volunteers visiting
selected constituents in their homes, and the petition was widely
promoted to the public who could sign and answer questions online.

In the early stages of the campaign, the TOFT volunteer coordinator
searched for contacts in the group Volunteers and used the Send Email
action to send a general email asking for volunteers to help with the
survey. From those who responded that they were available, a small group
were trained to carry out the home visits and record survey responses.

Once the online petition had been created using tools in CiviCampaign,
the TOFT communications officer created an email including text, images
and links to promote the campaign and encourage people to click through
to the site and complete the online petition. This email was then sent
out to the entire database using CiviMail, including a forwarding link
so that recipients could easily distribute the email widely through
their own networks.

CiviMail enabled TOFT to track responses to this mass emailing; reports
were generated showing that 89% of recipients clicked through to sign
the petition, and 75% forwarded it on to others. This data was then
compared with previous offline petition and survey efforts to
demonstrate the increased reach of the campaign through using CiviCRM.
