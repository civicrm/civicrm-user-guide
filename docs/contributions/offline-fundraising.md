# Offline fundraising

Your organisation may collect donations at events, solicit donations via
postal mailings and other offline methods. Any money raised through
offline activities needs to be manually entered into CiviCRM in order to
ensure that final reporting is accurate.

There are three steps within CiviCRM for offline fundraising: creating
your lists, creating your mailings, and
[manually entering contributions](manual-entry-of-contributions.md).

## Creating your lists

This process is fairly straightforward if you are familiar with
CiviCRM's search capabilities.

Go to **Search > Find Contacts** to create a list of records to receive
your offline postal mail appeal (it could be your entire database).

If you want to track the success of a mailing or who receives certain
appeals, save the search results as a group. Use the check box to select
all and choose the appropriate option from the **Action**
dropdown menu i.e. **Group - add contacts** or **Group - create smart group**). Later,
you can mark everyone in that group as recipients of that appeal using
the **Add Activity** option under the **Actions** dropdown menu.

If you want to create letters for postal mailings you can do this using
CiviCRM's internal **PDF letters - print** feature, or you export the list as a
CSV file and use mail merge to a word processor.

To export a list:

1. Select all records or a subset using the checkboxes, and from
    the **Actions** dropdown menu choose **Export Contacts**.
1. Choose whether to **Export PRIMARY fields** or **Select fields for
    export**. If you elect to export primary fields, the CSV file will
    be immediately generated when you click **Continue**. If you opt to
    select which fields you want to export, click **Continue** and a
    list of dropdown options will appear.
1. Select the required fields; if you wish to save the list of exported
    fields as an export mapping for future use, check the **Save this
    field mapping** box.
1. Click **Export** to generate the CSV file.
1. Click **Done** when you have finished to return to the contact list.


## Creating postal mailings

Once your spreadsheet is created, you can do a mail merge using any word
processing software (such as OpenOffice, the free software word
processor) that will insert any fields you want in the letter.

CiviCRM can also create mailing labels for you. Perform the same search
you used in the previous section to create your list of recipients,
then:

1.  From the **Actions** dropdown menu, select **Mailing
    labels - print**.
2.  Select the mailing label number, determine whether you want to
    exclude people with "do not mail" checked in their privacy options
    (checked by default and recommended), and whether you want to merge
    two records that have the same mailing address into one label. This
    last option is very useful when you are mailing a household or
    organization and you don't want them to receive duplicate mailings.
    When the records are merged, each name at that address appears on
    its own line on the label.
3.  Click **Make Mailing Labels** and a printable PDF document will be
    created.

Note that CiviCRM prints labels in the order shown on the research results page
in a column-by-column pattern.
