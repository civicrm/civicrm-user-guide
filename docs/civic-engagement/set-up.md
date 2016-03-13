Set-up
======

This chapter describes how to access CiviEngage functionality and gives suggestions
on how to use the custom field sets and profiles that it includes.

Enabling CiviEngage
---------------------

CiviEngage is automatically installed as a Drupal module when you install CiviCRM, so you only need to "turn it on".  You will need Drupal Adminstrator permissions to:

-   enable the CiviEngage component within the CiviCRM module in Drupal
-   update the Permissions for the Adminstrator role to access
    **CivCRM_engage module** by checking the box for **access
    civiengage settings**. 

Note that CiviEngage requires the component CiviCampaign to be enabled.

CiviEngage Contact Subtypes
---------------------------

CiviEngage takes advantage of CiviCRM contact subtypes to expose custom
field sets associated only with specific subtypes (see below for a
description of the custom field sets). The following contact subtypes
are created when you install CiviEngage:

Individual subtypes:

-   **Media Contact**: will expose the custom field set, Media Info,
    containing information specific to media contacts, such as their
    media type (e.g. Newspaper, Radio, TV, etc.), their "beat" (area of
    operation) and media issue interests.
-   **Elected Official**: will expose the custom field set, Elected
    Official Info, containing information specific to elected officials,
    such as their elected level (such as City Council or Senate) and the
    role (such as scheduler or spokesperson).
-   **Funder Contact**: will expose the custom field set, Funder Info,
    containing information specific to funders, such as their programme
    areas and issue interests.

Organisation subtypes:

-   **Media Outlet**: will expose the custom field set, Media Outlet
    Info, containing information about an outlet's type of media, such
    as TV, Radio, Wire, Newspaper, Magazine, etc.
-   **Foundation**: will expose the custom field set, Grant Info,
    containing fields where you track information specific to grants,
    such as the average grant amount a foundation will give and funding
    areas the foundation is interested in. 

Modifying the custom field sets
-------------------------------

When you install CiviEngage, a number of custom fields are automatically
created. These fields are designed to support your community organising
work. Most of these fields are multiple choice fields which have been
pre-populated with sample options. Before you start using CiviEngage,
you need to review and modify the supplied options to meet your needs.

Note that CiviEngage has been developed with the North American context;
if your organisation operates outside the USA you may need to customise
the language but most of the concepts will be similar and useful to your
organisation.

We strongly suggest that you do not delete any custom fields or custom
field sets, since other features such as reports and searches may rely
on these fields; deleting fields could potentially break these and other
CiviEngage features.

To review the custom field sets, go to **Administer > Customize >
Custom Data** in the navigation menu. 

![image](../img/civiengage%20custom%20data%20sets%20small.jpg)

The following list describes each of the custom field sets provided by
CiviEngage; the bulleted items are custom fields within those custom
field sets. You should add, edit, or disable (we highly suggest that you
do not delete) the available options for each custom field to make them
better fit your organisation's needs.

To learn more about using custom fields sets, see the chapter Creating
Custom Fields in the section Your Data and CiviCRM.

### Communications Details

This custom field set can be used to provide more details about when to
best contact your constituents, if they have good addresses, email
addresses, or phone numbers, and the reason why they don't want to be
contacted by email, or phone, or mail.

-   Best Time to Contact: indicate if the best time to contact your
    constituent is in the morning, afternoon, or evening.
-   Communication Status: indicate if you have a bad email, bad address,
    or bad phone for the contact
-   Reason for Do Not Mail
-   Reason for Do Not Phone
-   Reason for Do Not Email

### Voter Info

This custom field set may be used to capture voter demographics about
your constituents. You may also want to add specific local voter fields
that apply to you.

-   State Voter ID
-   Party Registration
-   If Other Party: use this field only if you don't want to add another
    option value in the Party Registration custom field
-   Precinct
-   Ward
-   State District
-   City District
-   Congressional District
-   County Name
-   Voter History: A (Always votes), O (Occasionally votes), N (New
    Voter); you can add other values to describe how your constituents
    votes.

### Constituent Info - Individuals

This custom field set may be used to describe additional information
your individual contacts, such as how you want to classify your contacts
for ease of searching and targeting form communications, which staff
person is responsible for outreach to the individual, and how and when
the individual was brought into your organisation.

-   Constituent Type: This is a required field used to categorize the
    type of contact, such as Volunteer, Activist, Board Member, Donor,
    Ally, etc.
-   Other Name: may be used to contain another name used by the contact,
    for e.g. an individual's name in chinese characters
-   Staff Responsible: note that the values for this field are also used
    for Event Contact Person. Replace the sample names in the list with
    your staff, member or volunteer coordinators, and other folks that
    have individuals assigned to them.
-   Date Started: may be used to indicate the date your constituent was
    brought in to your organisation.
-   How Started: edit this list to fit the ways in which members are
    brought into your organisation.

### Grassroots Info

This custom field set may be used the to further capture information
about how a constituent likes to engage with your organisation, the
types of issues and volunteer activities they're interests, their level
of leadership, and their status as a member. These fields provide
another way to categorise your constituents to better target your
audience for outreach and communications.

-   Member Status: three status choices of Active, Inactive and Deceased
    are included by default. Think about other member statuses that
    might work for your organization and add or remove as needed.
-   Leadership Level: the default options for tracking an individual's
    leadership level within your organisation are 1-5. Change this to
    match however your organisation tracks this information.
-   Issue Interest: this may be used to capture what issues your
    contacts are interest in. This custom field shares the same set of
    options as the Funding Areas (for organisations), Media Issue
    Interest and Funder Issue Interest fields. It is a list of issues
    that your organisation works on or tracks.
-   Volunteer Interests: a list of volunteer activities that your
    members can take on.

### Constituent Info - Organizations

This custom field set may be used to classify the type of organisational
contact so that you can target your outreach and communications.

-   Constituent Type - Org: this custom field is required and may be
    used to classify the type of organisation contact, such as Member
    Organisation, Affiliate Organisation, Business, Government.

### Grant Info

This custom field set may be used to capture information about grants
for a particular foundation. You can view and edit this custom field if
you create an organisation contact with subtype Foundation.

-   Average Amount: average dollar amount for grants
-   Funding Areas: this custom field uses the same set of options for
    Issue Interest and Funder Issue Interest.
-   Requirements Notes

### Proposal Info

This custom field set may be used to capture information about grant
proposals. You can add, view and edit information about proposals when
you create an activity of type Proposal for either a funder contact (an
individual contact with type Funder Contact) or for a foundation contact
(an organisation contact with type Foundation).

-   Ask Amount
-   Proposal Status
-   Amount to be Received
-   Date to be Received
-   Multiyear Grant
-   Years

### Participant Info

This custom field set, which is available when you create a participants
for your events, may be used to capture information about participants
to your events, such as if they need childcare or rides to and from the
event. Organisers who contact potential participants multiple times
before an event can also capture responses from participants to track
over time if they were able to get their constituents to participate and
how many contacts it takes to encourage them to come to the event.

-   Childcare Needed
-   Ride To
-   Ride Back
-   Invitation Date
-   Invitation Response
-   Second Call Date
-   Second Call Response
-   Reminder Date
-   Reminder Response

### Event Details

This custom field set is used to capture additional information about
your event.

-   Event Contact Person: also used for Staff Responsible. Add all
    appropriate people to this list.

### Organizational Details

This custom field set may be used to store information that is specific
to organisations.

-   Rating: if you need to evaluate organisations in some way, change
    the options to reflect that.

### Demographics

This custom field set may be used to capture demographic information
about your constituents.

-   Ethnicity
-   Secondary Language

**Media Outlet Info**

This custom set is only applicable to the organization contacts with
subtype Media Outlet.

-   Media Type - Org: this custom field uses the same set of options as
    Media Type - Ind field - TV, Radio, Wire, Newspaper, Magazine, etc.

### Media Info

This custom field set is only applicable to the individual contacts with
subtype Media Contact.

-   Media Type - Ind: this custom field uses the same set of options as
    Media Type - Org
-   Beat: this refers to the general category of topics that a media
    contact covers, such as local government, education, neighborhoods,
    religion, labor, etc.
-   Media Issue Interest: uses the same option list as Issue Interest.
    As you come to know a reporter, you will learn the issues they are
    particularly interested in, even if it differs from their assigned
    beat.

### Funder Info

This custom field set is only applicable to individual contacts with
subtype Funder Contact and may be used to capture information specific
to the funder contact.

-   Funder Program Areas

-   Funder Issue Interest: this custom field uses the same set of
    options as Issue Interest and Funding Areas.

### Elected Official Info

This custom field set is only applicable to individual contacts with
subtype Elected Official.

-   Elected Level: the governmental body the individual is part of (City
    Council, state legislature, mayor, etc.)
-   Elected Staffer Role: whether the contact is the elected official,
    or the official's staff, spokesperson, etc.

Modifying CiviEngage's custom value options
-------------------------------------------

CiviEngage includes many custom fields with value options. The following
are examples of value options that you may want to consider reviewing
and modifying to match the kinds of information you need to track for
your work.

To learn more about working with value options or multiple choice
options, see the chapter called Creating Custom Fields.

### Value Options for Issue Interests

The value options for Issue Interests contain issues that your
organisation works on or tracks. They are included in CiviEngage as a
single option list shared across multiple contexts:

-   Grassroots Info: Issue Interests for individuals
-   Media Info: Media Issue Interests for Media Contacts
-   Funder Info: Funder Issue Interests for Funder Contacts
-   Grant Info: Funding Areas for organisations

It is important to remember that despite appearing with different labels
in these different contexts, you are still dealing with just one shared
list of options.

In planning to use CiviEngage you should come up with a list of distinct
issues that are important to your organisation and that you will want to
utilise when tracking individuals' interest in your organisation's work,
the issues that your media contacts may be interested in covering, a
funders' general interests and the specific areas of work included in
particular grants.

### Value Options for Volunteer Interests

The value options for Volunteer Interests contain activities that your
organisation's volunteers can take on and participate in; you can
indicate each individual's interest in participating in these ways. They
are included in CiviEngage as an option list. In planning to use
CiviEngage you should establish a list of your organisation's current
volunteer activities as well as any activities that you are planning to
launch in the future. Some examples of volunteer interests are
canvassing, phone banking and tabling.

### Survey Default Result Set Options

When creating a new survey, especially when you have a survey with more
than one quesiton, CiviEngage defines a default set of Result Options
that may be used to indicate if a survey has been completed or why the
survey was not completed:

-   label is Completed with value C
-   label is Not Home with value NH
-   label is Moved with value MV
-   label is Wrong Address with value WA
-   label is Wrong Number with value WN
-   label is Deceased with value DE

We strongly suggest that you create labels with names that are
descriptive, and for the values use abbreviated names so that when
printing out WalkLists or PhoneBank reports using the Survey Report, the
code or value is displayed to keep your report neat and easy to look at
for recording responses.

Custom profiles
---------------

CiviEngage creates several custom profiles for easier batch updating of
individual or organisation information, such as voter demographics,
issue interests, volunteer interests or event participant information.
To learn more about profiles, please refer to the chapter called
Profiles in the Core Functionality section.

Setting up Surveys for Walklists and Phonebanking
-------------------------------------------------

CiviEngage in combination with CiviCampaign allows you to easily set up
your surveys for walklists during door-knocking canvasses and for
phonebanking. You will want to think about the questions and responses
you want to collect from your target audience in a manner that will be
useful in analysing results from your efforts after you've conducted
your canvass or phonebank.

There are a few steps to think about when creating your surveys (you can
find out more about creating surveys in the Survey section of this
book):

1.  create your custom data set of questions and responses you plan to
    use for your survey if you plan to ask more than 1 question that
    extends Activities of type Walklist or Phonebank. 
2.  create the custom profile that includes the questions you will want
    to ask your audience. **Hint:**If you plan on doing a phonebank and
    want to do the data entry directly into civicrm, then you may want
    to add the phone number in the profile, and set it to view only, so
    that you can see the phone numbers when you're interviewing the
    respondents. The profile will allow you to display (view only or you
    can edit data) other fields of information when you're ready to
    interview and enter the data. 
3.  create the group or smart group of the individual contacts you plan
    to survey, which is your target audience.
4.  Make a decision if this survey is part of a larger campaign, and if
    so create the Campaign and indicate this campaign when creating the
    survey (you can find out more about create campaigns in the
    Campaigns section of this book).
5.  When you create your survey, you can then:

     -   indicate if the survey is for a walklist or phonebank
     -   specify if the survey is part of a campaign
     -   include the custom profile of the questions you plan to ask during
         the survey, if you plan on asking more than one question
     -   use the Survey Default Result Set Options that's created by
         CiviEngage to help you track the status of the responses to the
         survey if appropriate. 

**Tips:**

-   If you plan on conducting many surveys throughout the year (let's
    say 20 - 30 surveys in a year) with only a few questions per survey
    (let's say 3-4 questions per survey), then we strongly suggest that
    you create ONE custom data set that includes all the questions for
    each of the survey. Then you can create individual custom profiles
    for each survey that pull in the questions that are particular to
    that survey.
-   If you plan on conducting just a few surveys per year (let's say
    about 3-4 surveys per year) with the number of questions no more
    than 10 per survey, then we suggest that you create different custom
    data sets for each group of questions per survey. Then you can use
    custom profiles to pull in in the questions that are particular to a
    survey.

### Setting up custom data sets and profiles for use with Walklist or Phonebank Surveys

1. Create your custom data set to hold your questions (to learn more
about creating custom data sets and fields, see the *Organising Your Data*
section of this book). 

 -  For WalkList surveys: -   Create your custom data set for use with Activities of type Walklist 

 -  For PhoneBank surveys: -   Create your custom data set for use with Activities of type PhoneBank 
![image](../img/create%20custom%20data%20sets.jpg) 

2. Then for both Walklist or Phonebank surveys you can create the
questions as the custom field labels and the responses you want to
collect as the option values.
![image](../img/custom%20data%20for%20walklists.jpg)

3. Next, create the custom profile that will pull in the questions for
your survey (to learn more about creating profiles, see the *Organising
Your Data* section of this book). 

![image](../img/custom%20profile%20for%20walklist.jpg) 

