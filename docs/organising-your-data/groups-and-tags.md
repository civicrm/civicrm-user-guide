# Groups and tags

Groups and tags are two key methods of organising data in CiviCRM. When
used properly, both allow for powerful segmentation and searching of
your database.

Since both groups and tags are methods of categorisation, it can be
difficult to determine whether a tag or a group is more appropriate in a
given situation. Identifying the differences in their functionality will
help you to decide which to use.

It can also be good to have a conceptual understanding of the
differences between the two. Though there are different takes on how
tags and groups should be used, a common philosophy is that tags should
be used for descriptive categories of contacts, activities, and cases,
while groups should be used for grouping people within an entity that
needs to be treated like a cohesive unit (to send mailings to, for
example). From this perspective, things like *volunteer*, *ally
organisation*, *vegetarian* and *musician* would be tags with which you
could categorise contacts while *Volunteer Committee, Allied
Organisations Coalition, Vegetarian Newsletter*, and *This Awesome Band
With A Bad Name* would be groups to which you could add contacts.

## Groups

Groups are an incredibly important feature within CiviCRM. In addition
to their fundamental use as collections of contacts that have something
in common, they play a critical role in CiviMail and Profiles, and can
be used to set up advanced access rights (on Drupal). Well-defined
groups are one of the most important tools available when segmenting
your CiviCRM contact database.

There are two kinds of Groups &mdash; (Regular) **Groups** and **Smart Groups**.

-   Regular groups are just called **Groups**.  You manually place contacts into and remove contacts from a (regular) group. For example, you can manually assign your organisation's
    board members to a Board of Directors group. You can then
    easily send board-related emails to each person who is a member of
    the Board of Directors group without having to search through
    CiviCRM and select each member individually for the mailing.
-   **Smart Groups** are automatically populated groups that are
    configured to include contacts that share a certain set of
    characteristics or activities. As contacts are added or edited,
    CiviCRM automatically checks them and adds them to Smart Groups if
    they meet the characteristics that you have configured. For example,
    you can create a Smart Group for "2010 Contributors from California"
    that includes contacts who have made a contribution in the year 2010
    (an activity) and have an address in California (a characteristic).
    When new contacts located in California make a contribution in 2010,
    they are automatically added to this group. Another example is a
    Smart Group of all donors who have not yet been sent a thank-you
    letter. As you send your letters, the donors receiving them will
    automatically leave the smart group, allowing you to always have an
    accurate list to work from.

### Group settings and functionality

Each group should have a clear, easily understandable group name and a
description of its purpose that other database users will be able to
understand. Both the name and the description should allow users to
quickly figure out what particular groups are for when working in
different contexts (e.g. CiviMail). This clarity and specificity is
especially important once your organisation has amassed many different
groups. If a group is created for a specific person within your
organisation, it is a good idea to mention who the group owner is in the
description so that in the future someone can check if this group is
still used or if it can be deleted.

Groups can be assigned the following standard types:

-   **Mailing List** is used if you plan to use this group as a mailing
    list in CiviMail. This group type is available for both Regular and
    Smart Groups.
-   **Access Control** (Drupal only) is used to assign CiviCRM access
    permissions to a set of contacts. Only Regular Groups can be
    assigned the Access Control group type.

It is possible to create additional group types to reflect your specific
needs. This is particularly useful if your organisation has hundreds of
groups as group type can be used as a filter on the Manage Groups
screen. To create additional group types go to **Administer>System
Settings>Option Groups**and select Group Type.

### Visibility

Visibility determines permissions for joining and removing contacts from
groups. Select "User and User Admin Only" if membership in this group is
controlled only by authorised CiviCRM users. Select "Public Pages" if
you want to allow contacts to join and remove themselves from this group
via Registration and Account Profile forms.

Some organisations find it useful to create a hierarchy of groups. In
CiviCRM, this is done by creating one or more parent groups and then
assigning other groups to them. When a user sends a mailing to a parent
group or searches for contacts in a parent group, all contacts in the
associated child groups are automatically included.

For example, an organisation that has a national office and 5 regional
offices puts constituents in each region into their own group. Then they
create a National group which is assigned as the parent group for all
regional groups. The national office can now send mailings to the
National group, knowing that all contacts in the regional groups that
are children of the National group will be included.

### Group IDs

CiviCRM assigns a unique numeric ID to each group. These group IDs can
be used for a variety of operations. For example, the group ID can be
used to define a URL for group sign-ups. You can find a group's ID by
checking the ID column in the tabled list of groups at **Navigation Menu > Contacts > Manage Groups**.

## Tags

**Tags** are used to categorise contacts, activities and cases in
CiviCRM. You can create as many tags as needed to classify the contacts
in your database, though it is advisable to avoid duplicating existing
tags or adding too many tags that aren't really necessary. It can be
useful to create a standard process for creating and using tags within
your organisation to avoid these problems.

## Groups versus tags {#groups-vs-tags}

This is a common question on any project, and the philosophy described
in the introduction of this chapter is a guideline, but rules might need
to be bent based on how you intend to use your contact segmentation.

One interesting benefit of having both groups and tags is that you can
perform more refined searches using AND and OR. For instance, if you
have journalists, volunteers and members as groups and use tags to
identify topics of interests such as development, art and history, you
can find all the journalists who are interested in art or development,
all the volunteers or members that are interested in history, or any
other combination.

Beside that, groups have some features that tags don't:
-   Groups are integrated into several other CiviCRM functions (most
    notably CiviMail).

-   Contacts can be added to smart groups automatically based on
    characteristics.
-   Groups can be associated to Drupal Organic Groups.

Think of it this way: tags can be applied to contacts, activities, and
cases, whereas groups can only consist of contacts.

The following outlines the pros and cons of groups vs. tags

#### Benefits of tags
-   Easy to setup and use
-   Easy to search by tags (can use either Basic or Advanced Search)
-   Easy to combine with other properties (like residence
    state/province) to create Smart Groups

#### Limitations of tags

-   You can not create Tags for use with specific types of contacts
    (i.e. you can't create tags that are ONLY for use with Individual
    contacts)
-   When you export Tags, all Tags assigned to a record are exported in
    a single "cell" as a list (e.g. "Teacher, Volunteer")
-   Tags allow multiple selections - so they may not be appropriate for
    mutually exclusive characteristics (e.g. "Democrat", "Republican",
    "Green Party")
-   You cannot selectively hide or permission Tags on built-in or
    Profile create and edit forms (you get ALL Tags ALL THE TIME on edit
    forms)

#### Benefits of Groups

-   Groups are the most flexible way of segmenting your contacts for a
    wide variety of purposes.
-   Groups facilitate recurring tasks like sending an enewsletter,
    printing mailing labels, etc.
-   Groups allow you to restrict access to "special" sets of contacts
-   Groups support both administrative and end-user "subscribe" and
    "unsubscribe" actions - and a history of these actions is kept in
    the system
-   Visibility settings allow you to decide which Groups are shown to
    end-users on Profile forms (i.e. some Groups can be "private")
-   You can create Smart Groups that combine members of Group A + Group
    B

#### Limitations of Groups

-   All existing Groups are listed under Manage Groups and in the search
    forms. This may cause group "overload" if your organization winds up
    with "too many" Groups.
-   Groups used for short-term projects should be "purged" when they're
    no longer needed
-   When exporting contact records, all the Groups a contact belongs to
    are exported as a single comma-separate list (e.g.
    "Administrators,Newsletter Subscribers")

You can add contacts to groups in multiple ways:

-   through the Tags and Groups section of the Contact Details edit
    screen
-   through a contact's Groups tab
-   by using the "Add Contacts to Group/Tag contacts" batch action after
    conducting a search
-   by clicking a group's Contacts link in **Navigation Menu > Contacts > Manage Groups**.

The first two methods also allow you to remove individual contacts from
a group. The last two methods allow you to add multiple contacts to
groups at once.

Individual contacts can be added to a Group either in the contact edit
screen or via the Groups tab. Multiple contacts can be added to a group
at once by conducting a search, and then selecting Add Contacts to a
Group using the More Actions menu. The second way allows you to add
multiple contacts to a group by going to Manage Groups, selecting
Members for the relevant Group and then using the Add Members to this
Group option at the top of the screen.

Contacts can also be added to a group as a result of filling out a
Profile (see below).

## Managing Groups

To view and manage all groups, go to: Navigation Menu > Contacts >
Manage Groups.

![image](/img/ManageGroups.png)

You can use the Find Groups form at the top of the Manage Groups screen
to search for groups by name, type, visibility and whether the group is
enabled or disabled. You can also scroll or browse through the list of
groups further down the Manage Groups screen. This list includes both
regular and smart groups.

You can:

-   add contacts to a group by clicking the Contacts link in the group's
    row
-   edit the group by clicking the Settings link
-   disable or delete a group using the links in the "more" pop-up
    menu.
-   see how many contacts are currently in each group.

## Finding contacts in a group

The Contacts page for each group includes a form for finding contacts
within the group. You can search contacts within a group by name, email
address, contact type, group status (added, removed, or pending) and
tags.

![Groups_searchwithin](/img/CiviCRM_update-CiviCore-Groups_searchwithin-en.png "Groups_searchwithin")

## Groups and ACL

Access Control Lists (ACL) provide finer grained permissioning than what
is available through Drupal's Permissions and Roles. Setting up ACLs
requires a good understanding of the concept, which is thoroughly
explained in the online CiviCRM documentation here:
[http://wiki.civicrm.org/confluence/display/CRMDOC/Access+Control](http://wiki.civicrm.org/confluence/display/CRMDOC/Access+Control%20)

As with many processes, the key is to make sure you have assembled all
the parts before you try to join them together. In this case, you must
set up the required Groups, Custom Data Groups, Profiles and Roles
before you can use them in ACL.

!!! note
    ACL support for Joomla was introduced in Joomla version 1.6.

## Removing versus deleting contacts from groups

One of the advantages to using groups over tags is that CiviCRM maintains a historical record of group membership. If you **Remove** a contact from a group, you can see when they were removed and by whom. This can be useful in a number of use cases (e.g. you can track former members of a volunteer group, or if an email subscriber asks why they are no longer receiving your newsletter, you can provide details on when they opted out).

![img](/img/GroupRemove.png)

If a contact was removed in error, there is an option to **Rejoin Group** and the contact will be added again. Every group record has a status attached to it: **Added**, **Removed**, or **Pending**. You can search for all of the members of a group by status. Navigate to **Contacts > Manage Groups**. Identify the group that you want to search within and select **Contacts** on the right-hand column. From there you can expand the search criteria and you are given an option to search by status. This could be used, for example, if you want to generate a list of all of your former Advisory Board members.

![img](/img/GroupStatusSearch.png)

You can also **Delete** a contact from a group. That will eliminate any record of the contact being in the group.

## Working with tags

To view tags, go to: **Contacts > Manage Tags (Categories)** in the
navigation menu.

A tag can be edited or deleted using the respective links in its row.
New tags can be created by clicking the Add Tag button on the Manage
Tags (Categories) screen or by going to Contacts > New Tag in the
navigation menu.

![admin_tags](/img/CiviCRM_update-CiviCore-resized_600x158_admin_tags-en.png "admin_tags")

Each tag should have a clear and unique name and an explanatory
description to help users understand the tag's purpose. Tags can be
structured hierarchically and designated as subtags of an existing tag
by selecting a Parent tag from the dropdown list.

Tags can be designated for use for contacts, activities and/or cases. If
a tag is designated for use for contacts, it will be available for all
contact types and subtypes; tags cannot be specifically designated for
use for only one type of contact.

Tags are a flexible tool and every user can create more if needed.
However, very important tags can be locked to prevent them from being
modified or deleted by users who do not have the "administer reserved
tags" permission (this permission is available in Drupal only).

Tags can be assigned to contacts, activities and cases in the following
ways:

-   while creating or editing the record
-   from the Contact Summary Tags tab
-   by using the Tag Contacts batch action after conducting a search.

You can also use the first two methods to remove tags.

## Tag sets

Tag sets are a free-form way of tagging contacts and are similar to
regular tags, but they differ from regular tags in a few key ways:

-   they act as a "bucket" to allow you to group tags (i.e. an Issues
    People Care About tag set might contain the tags "affordable
    housing", "racial justice", or "water quality")
-   they allow tags to be created on the fly without you having to
    access the Manage Tags page
-   adding them creates an additional search field in the Basic Criteria
    section of the Advanced Search

Tag sets are created by going to: **Contacts > Manage Tags
(Categories)**in the navigation menu and clicking the Add Tag Set
button. Give the tag set a name, a description, and indicate whether the
tag set will apply to contacts, activities, or cases.

![image](/img/Tag_Set_-_Create.png)

Clicking the Reserved checkbox makes a tag set more permanent - this
will prevent a tag set from being deleted by someone without
Administrator permission. (Read more about permissions, in the
*Permissions and Access Control* chapter of *Initial Set Up* section.)

Now you can use the tag set to freely tag a contact, activity, or case
record.

When you create a new tag set, a new field shows up on the edit pages of
the entity's activities or cases as well as in the Tags tab for
contacts. For example, if you create a tag set called "Issues Folks Care
About" an associate it with Contacts, you will see the tag set next time
you go to the Tags tab of a contact's record.

![image](/img/Tag_Set_-_Creating_tags_on_the_fly.png)


This is an autocomplete field: as you begin to type, CiviCRM looks for
matching tags in this tag set and displays any matches below the field.
You can select an existing tag or create a new one by typing the entire
tag and pressing the Enter key. The tag will then appear within the
field in a box. Clicking on the X will untag the record that you are
editing (contact, case or activity).

Tags created within a tag set will automatically appear in the normal
**Contacts > Manage Tags (Categories)**list and can be viewed and
edited from there. However, tags created within a tag set will only be
available within that particular tag set.

### A Note About Searching on Tags and Tag Sets

For each tag set you create, a new field will appear in the Basic
Criteria section of Advanced Search. You can only search on tags that
already exist in this tag set.

Searching in the All Tags field will allow you to find records with tags
(regular or tagset tag) which contain a complete or partial word or
phrase. EXAMPLE: If you have several tags that contain the word 'Donor',
you can find contacts tagged with any of them by entering 'Donor' in
this field.

Read extensively on using Advanced Search in the Searching section.
