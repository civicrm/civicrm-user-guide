# Finding and viewing memberships

This chapter describes how to view and search your membership records.

## Viewing Your Memberships

To see a summary of the status of your memberships over recent months,
as well as details about these memberships, you can use the membership
dashboard or view the membership in an individual's contact record.

### The Membership Dashboard

To see a quick snapshot of your recent memberships, use the membership
dashboard: **Memberships > Dashboard**. This screen contains two
blocks of information that display a summary or your recent memberships,
categorised by type and date range, and a list of recent member
activity.

![image](/img/CiviCRM-CiviMember-Memebership-Summary_2.png)


All of the summary numbers are hot-linked. Simply click on a number to
drill down and view a list of members who have joined or renewed over
the last two months or the year-to-date, or who are considered current
according to the membership status definitions. From this list of
members, you can perform additional actions with the memberships, such
as Delete, Edit, Export, Send Email to Contacts.

### Viewing A Contact's Membership Records

Another way to view membership records is by viewing a specific
contact's record and looking at the Membership tab.

!!! note
    If a contact's membership is "pending", the membership will show up when
    the tab is clicked but it will NOT be counted in the number on the tab.

After finding the contact you wish to manage, click the "Membership" tab to
view a summary of the contact's membership records.

![image](/img/CiviCRM_update-CiviCore-Contact_MembershipTabs-en.png)

Membership records appear in a list with active memberships (those with
a current status) first and followed by expired or canceled memberships.

You can edit existing membership records, renew a membership, or create
a new membership record. If you have configured an online credit card
payment processor for use in CiviCRM, you will see two options for
creating or renewing a membership: one for handling an offline record
(no real-time transaction taking place), and one for handling an online
record (using a real-time credit card transaction), which can also be
used to set up auto-renew if the processor supports this. The interface
for each process is very similar, except that the credit card option
includes payment processing and recording options.

If you are looking at the primary member contact record for a
membership type that has inherited membership you will see a list of the
contacta who have inherited the membership.

![image](/img/membership_everyday_for_limited_inherited.png)

In this case a maximum of two inherited memberships are allowed for
people who are employees of the primary membership organisation. If one
of the available inherited memberships is not assigned to the correct
employee then you can click on **Delete** for that contact. This will
free up an inherited membership for you to assign appropriately by
selecting **Create.**

### ![image](/img/membership_everyday_for_limited_inheritedp2.png)

## Sending email to members

After searching your records, you may want to send an email to selected
contacts and include data field [tokens](/common-workflows/tokens-and-mail-merge.md) to personalize the email message.

To send email to members:

-   Click on **Memberships > Find Members**, enter your criteria,
-   then on the "Find Members" search results screen, select the records
    you want to import and in **-actions-** drop down, select **Send
    Email to Contacts**.

## Searching based on membership data {:#searching}

CiviCRM makes an important distinction between contacts and memberships,
which is blurred when we talking about 'members'. Consider the
following question: 'How many members do we have?' This could be taken
to mean 'how many contacts do we have that are members?', or 'how many
memberships have we granted to contacts?'. The answer to these
questions is often the same but what happens if one of your contacts has
more than one membership? The answer is that you'll have two
memberships but only one contact.

There's no right or wrong answer to the question should we look at
contacts or memberships. It just depends on what you are interested
in. It is important to take this into consideration when carrying out a
search.

The **Find members** search allows you to search based on membership
data and return membership data.

-   Click on **Memberships > Find Members**, enter your criteria.
    Click the **Search** button.

![image](/img/memberships_find_memberships.png)

The **Advanced search** allows you to search based on some limited
membership information (combined with other contact information) and
return contacts. You can also choose membership from the **Display
Results As** column to show members rather than contacts. To find out
more about using Advanced Search, refer to the [Searching chapter](/the-user-interface/searching.md).

-   Click on **Search > Advanced Search** and in the **Display Settings For Results** accordion set **Display Results As** to **Memberships**, enter your criteria.
     Click the **Search** button.


![image](/img/z_sprint14_display_Results_as_1.png)

Once you have found the membership information based on your criteria your search results will allow you to view some membership details. You then can perform further
actions on your search results or a smaller subset of selected records,
such as **Email - send now** or **Export members** by clicking
on the **Actions** dropdown menu.
