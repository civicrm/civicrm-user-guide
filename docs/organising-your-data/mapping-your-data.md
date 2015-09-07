Mapping your data
=================

Your existing data may be coming from multiple sources, some electronic,
some paper based and some residing in people's memory. "Mapping" refers
to the activity of taking existing data that was labeled in a certain
way and "slotting" it into a CiviCRM structure. This is a very important
step and skipping it may cause undesired consequences in the future. For
example, you may not be able to control or report on data the way you
expect.

Everyone thinks about data differently, based on experience with another
CRM or no CRM at all. For example, "Donation", "Opportunity", and
"Contribution" all refer to money given to your organization. CiviCRM
was designed to be flexible and adaptable, so you should have no problem
finding the proper place for every piece of information relevant to your
organization.

Resist the temptation to add custom fields right away. Instead of adding
a new field for manually entering membership expiration dates, learn
about CiviCRM's membership module that automates membership duration,
expiration and renewal reminders. Having multiple fields to collect the
same data will cause confusion later. Avoid data duplication by making
informed choices up front. 

The following sections will introduce you to options CiviCRM provides
out of the box with tips along the way for mapping your data. Instead of
using "flat" spreadsheets, **relationships** will tie your data
together. Using relationships, you will be able to create a more
complete picture of the community that supports your organization. 

Basic information about your constituents
-----------------------------------------

CiviCRM comes with default fields to store constituent names, addresses,
phone numbers, emails, notes and other contact information.
Since CiviCRM was designed for non-profits, the mapping of your most
basic constituent information should be very easy. 

CiviCRM divides constituents into 3 categories (Contact Types) based on
who or what they are:

-   Individuals: any person your organisation wants to keep a record of
-   Organizations: this could be another non-profit, a company, a
    chapter of your organisation, or a committee. You will generally
    want to create at least one contact of the Organization type to
    represent your organization. This is particularly useful when you
    are configuring memberships
-   Households: a family or group of people who share a physical
    location

Each contact type comes with different fields, according to the
different kinds of data you will probably want to track. For example,
gender only applies to individuals, not organisations or households, so
the gender field is only available for Individual contact types and
subtypes.

To read more on built-in CiviCRM basic constituents fields and how to
use them, please see the *Contacts* chapter in *Organising Your Data*.

Information about your constituents that is specific to your organization (basic introduction to Custom Fields)
---------------------------------------------------------------------------------------------------------------

Many organizations collect data specific to their mission or structure.
Even though CiviCRM comes with fields to store basic data that all
non-profits collect, similarities between non-profits end at a certain
point. For example, your organisation may be interested in information
about constituent allergies (for individuals) or service area
(organizations).

When mapping data into CiviCRM, decide if the information pertains to an
individual, organization, or household. Additional information like
"service area" only makes sense for Organizations. To find out how you
can create custom fields, please see the *Custom fields* chapter in
*Organising Your Data*.

Relationships between constituents
----------------------------------

Relationships capture current and historical information about how two
records connect to each other.

You or your colleagues probably know more about your constituents than
what has been written down. You may not have previously collected that
information because there was no space in your "flat" spreadsheet or you
may have collected it as a "mental note" about a given person or
organization. The name of their family members, place of employment,
and relationship to other constituents in your database can all be
captured with a Relationship. 

CiviCRM comes with a predefined set of relationship Types including
"employer--employee", "parent--child", and "employee--employer". You can
create more relationships to describe your organization specific
relationships, for example you might define a relationship type of
"vicar--church". When you create a new Relationship, you can define when
the Relationship began and, if relevant, ends. Previous relationships
can still be accessed when they end. For example, you can see where
someone used to work even after the relationship has been severed.

The term Household and relationship Types "household member of--head of
the household" confuses many new CiviCRM users. It's useful to group
individuals who share a common address in one household, so that they
only receive one letter. The designation "head of the household" helps
organizations know who the letter should address. For example, you want
to address the parent and not the child.

To read more about configuring and using relationships, please see the
the *Relationships*chapter in *Organising Your Data*. 

Activities
----------

It is important to know how and when constituents engage with your
organization. Knowing that someone gives monthly or volunteers
frequently and renews her membership yearly suggests that she may
respond well to opportunities that strengthen her relationship with your
organization. CiviCRM allows you to record interactions such as phone
calls, emails, and meetings between staff and constituents. These
features help an organization build a lasting memory of its
relationships.

CiviCRM calls these kinds of exchanges Activities. They are tightly
linked to other CiviCRM modules. When you record contributions, event
attendance, membership subscriptions, and emails, CiviCRM will
automatically create a related activity in the Contact record. Decide
whether your organization needs different activity types in addition to
those provide, such as training, review, exam, support etc.

To read more about configuring and using activities, please see the
*Activites* chapter in *Organising Your Data*.

Webinars, events, performances, and meetings (CiviEvents)
---------------------------------------------------------

CiviCRM helps manage and track any occasion in which you bring community
members together at a certain place and time. Webinars, events,
performances, and meetings have specific start and end dates and times,
meeting places (including online) and reasons for bringing people
together. They can be ticketed, RSVP only, or no reservation required.
CiviCRM comes with functionality to promote events and record
registrations. If you have records of who has participated in past
events, you can transfer these valuable records into CiviEvents.

The **Event Types** field helps you to distinguish between different
types of events your organization hosts. This is helpful for evaluating
how many people have participated in a similar series of events or
whether someone prefers one kind of event over another.

To read more about configuring and using relationships, please see the
*Events* section later in this book.

Memberships
-----------

Many organizations offer a structured program in which community members
can sign up to receive certain benefits for a pre-defined period of
time. Members choose from a variety of dues levels that have associated
benefits, generally the more you give the organization the more you get
in return. Organizations can also give membership at no price, perhaps
as an award. For example, a long-time volunteer might receive a
life-time membership to the organization. Common benefits include access
to member directories, extra content, discounts, etc. Individuals,
families or households, and organizations can all sign up for
memberships.

The main difference between membership dues and a donation is that
memberships redefine someone's relationship to the organization for a
period of time. Organizations often expect that memberships will be
renewed from year to year, while a donation is a one-time gift.
Organizations need to send an acknowledgement letter, but they have not
promised to serve the donor advertised benefits in response to a
donation or Contribution in CiviCRM.

Analyze your current membership structure before importing membership
records into CiviCRM. Take time to eliminate unused membership levels or
simplify the benefits you promise. The only information you really need
to transfer for each member is start date, duration, membership dues
paid, and type of membership.

Generally speaking, having more than 10-15 membership types may be hard
to manage. Sometimes organizations may have many membership types in
order to preserve other information about constituents in the membership
record. It's recommended to verify first whether or not CiviCRM already
has existing data fields related to memberships to keep track of that
information before extending membership records.

Some information that you may have recorded as static information before
can now be calculated dynamically, and displayed in reports or other
fields. For example, CiviCRM can dynamically calculate the number of
years a given constituent has been a member based on the
"Membership since" date.

To read more about configuring and managing memberships, please see the
*Memberships*section later in this book.  

Contributions
-------------

Contribution in CiviCRM refers to money, goods, or services coming in to
your organization. Money is still money whether someone buys an event
ticket, signs up for a membership, or any other activity that requires
payment. CiviCRM allows you to record all money coming into your
organization as a Contribution with different Types to preserve
information about where it came from. You will also be able to specify
the date the contribution came in, it's status (you can record a
contribution as pending before the money is deposited to your bank
account) and the form it was delivered in (check, cash, etc.).

If you are planning to keep using an external donations system, you may
leave transactions there. On the other hand, you may want to transfer to
CiviCRM information about past event/webinar registrations because they
tell you the history of constituent involvement in your organization.
Also consider how far back you want to import the history of
contributions. Large contributions should be preserved, but the fact
that someone donated 5 dollars 10 years ago may no longer be relevant. 

To read more about configuring and using relationships, please see the
*Contributions* section later in this book. 

Campaigns
---------

Sometimes organizations host a fundraising gala, send an email appeal,
and record contributions all to support one goal. E.g., raise $50,000
to support a kids camp. Campaigns are usually time limited and tie
together a range of activities and give you a high-level view to compare
how people responded to your initiatives.

You can start taking advantage of campaigns if your organization's
fundraising initiatives fit well into a unique themes. Some examples of
campaigns are year end pledge drives, or project specific fundraisers.
Organizations often send several email appeals encouraging donors to
support a particular project or fundraiser, such as a 'final notice' and
one or more 'countdown' appeals.

Grouping and tagging constituents
---------------------------------

Development directors, volunteer coordinators, and program managers
store a wealth of information in their heads. They often make decisions
about who to invite to an event, who should not receive an appeal,
and/or who would be perfect for a volunteer opportunity.

Groups and tags can store that kind of information and act as the
building blocks for creating email and invitation lists. **Groups** are
useful to identify two or more contacts with something in common, as
opposed to relationships which can only capture information about two
contacts. Groups can also act as mailing lists. A group of people who
subscribe to your newsletter(s) is a good start. 

Organizations can have complex communication strategies, in which they
send different letters to several subsets of their community. One
Individual can be tagged member and volunteer, so that she receives
member specific communications as well as volunteer specific
communications. Groups are also useful to store issue or program
specific communication preferences. For example, consider a group of
people who have specifically requested not to receive fundraising
appeals. When you go to create an email appeal mailing, you can exclude
the group of Individuals who have requested not to receive fundraising
appeals.

Try to avoid creating groups based on information that can be stored by
other fields in CiviCRM. You don't need a group for individuals who have
opted-out of bulk mailings, because that option will be selected on
their Contact record. CiviCRM automatically excludes these constituents
from any bulk mailing. Likewise, you don't need a group called "donors"
because you can run an advanced search to find any **Contact** record
that has a **Contribution** associated with it, even between any date
ranges. Most functions available to groups are also available through
the search results screen.

If you want new records that meet a particular criteria to be
automatically added to a group, create a **Smart Group** from any
**advanced search**. For example, you may want to have a Smart Group
that calls the Contact record of all members who also donated more then
$100 in the past year. When a member makes a new $100 donation after
the group has been created, their record will be added to the Smart
Group.

**Tags** are more like keywords that you want to associate with a
record.  You can easily add or remove tags, but there is no easy way to
see the history of changes. Relationships are a much better tool for
seeing information history.

Profiles
--------

CiviCRM allows you to pull together sets of fields for different
purposes, and help you reduce the amount of time staff spends on
administrative tasks. These sets of fields are known as profiles.

Profiles are about how your data is edited or displayed to your staff or
other groups of users, not how your data is stored.

Read the *Profiles* chapter in this section for detailed information
about how to make use of profiles.

Where next?
-----------

In the sections above we've tried to describe how your existing data may
be mapped into CiviCRM. We've only touched on basic CiviCRM
functionality or "spaces" where your data may fit. To read more about
how CiviCRM can work with your data, please see information in this book
about specific CiviCRM components: **CiviEvent**, **CiviMember**,
**CiviMail**, **CiviContribute**, **CiviCase**, **CiviCampaign**, and
**CiviGrant**.

Each of the above components will help you streamline administrative
tasks related to event management, membership, sending communications,
receiving contributions and donations, case management, conducting
campaigns, administering grants programs, and more.

The sections on **Survey**, **Petition**, and **CiviEngage** (the latter
is actually a Drupal module) relate closely to **CiviCampaign** and
their special functionality is described in the respective chapters.

There is also a separate reporting section related specifically to using
reports and doing analysis on your data for ongoing evaluation of your
work. 
