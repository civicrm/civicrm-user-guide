Postal mail communications
==========================

This chapter discusses the different ways that CiviCRM helps with postal
mail and postal mail campaigns. It will help if you already have a
strong understanding of CiviCRM's search features as well as custom
fields, activities, profiles, and how to perform mail merges using word
processing software.

Planning Your Mailing
---------------------

Before beginning any communication activity, take the time to identify
your goals and plan the steps. For our purposes, there are a few key
questions to ask before sending out postal mailings.

-   What types of mailing do you send out to your constituents?
-   Are mailings always sent to everyone in the database or are they
    frequently targeted to a select group of contacts?
-   How do you want to greet recipients (e.g. "Dear Jane" or "Dear Jane
    Doe")?

There are three ways that you can use CiviCRM in postal mailings:

1.  Generate labels: print out standard address labels when you don't
    need to personalise the content, for instance to send a printed
    brochure.
2.  Export contacts and do a mail merge to an external tool (such as
    OpenOffice or Microsoft Word). Refer to the chapter on Exporting
    earlier in this section for detailed exporting instructions. 
3.  Use CiviCRM's Print PDF Letters function to do the merge directly in
    CiviCRM (see below for details).

Many nonprofit organisations in the USA need to sort recipients of a
mailing based on zip code for bulk mailing purposes. If this is true for
your organisation, it is recommended that you create your mailing labels
using a word processor where you can control the sort order, rather than
in CiviCRM. You can reuse the same spreadsheet for your mail merge.

Greetings and salutations
-------------------------

You can set a specific postal greeting format for each contact. There
are several options from the friendly "Dear John", to more formal "Dear
Mr. John Doe". You can also enter a *customized greeting* ("Your royal
highness"). Postal greetings can be edited in the Communications
Preferences section of the contact edit form. If you need to set or
reset postal greetings en mass, refer to the chapter on *Scheduled Jobs*
in this section, and to the documentation on the wiki at:

[http://wiki.civicrm.org/confluence/display/CRMDOC/Update+Greetings+and+Address+Data+for+Contacts](http://wiki.civicrm.org/confluence/display/CRMDOC/Update+Greetings+and+Address+Data+for+Contacts)


Print PDF letters
-----------------

The workflow is to first select the contacts you want to target, then
choose to print letter as a batch action. The letters will then be
outputted as a PDF, allowing you to easily print them.

To create the letter:

1.  Go to **Search > Find Contacts or Find Contacts > Advanced
    Search**; if you want to print letters for members of a Group, go
    to **Contacts > Manage Groups** and click "Contacts" next to the
    Group you want.
2.  Enter your search criteria and click Search (not applicable if using
    a Group).
3.  Select the contacts who will receive the letter.
4.  From the Actions dropdown menu, choose "Print PDF Letter for
    Contacts" and click Go.
5.  Review the selections under Page Format and make any desired
    adjustments. This is where you set your paper size, margins, and
    page orientation. 
6.  Enter your text and make formatting adjustments in the WYSIWYG
    editor. You can also insert image files such as your organisation's
    logo, or a signature. Click in the body of the letter where you want
    the image to appear and click the Image icon. 
7.  You can personalise the letter by using tokens; for example, Postal
    Greeting is a commonly used token in this situation. Click in the
    body of the letter where you want to enter the token. Then click on
    "Insert Tokens" located above the letter at the top right and select
    the desired token.

    ![PostalGreetingToken](../_edit/static/CiviCRM_update-CiviCore-PostalGreetingToken-en.png "PostalGreetingToken")

8.  Before you move to the next screen, decide whether the format of
    this letter could be used again. If so, check the Save As New
    Template box and enter a name in the Template Title field.
9.  When your letter is finished, scroll to the bottom and click Make
    PDF Letters.
10. A pop-up window will offer the option of opening or saving the PDF
    (this is the same notification your browser will give you for any
    download). Open the file, review your letters, and then print them,
    or save the PDF and review it at your leisure.

You can use this feature for any kind of document, not only letters. For
example, you could use it to print attendance certificates for a
workshop.

Generate mailing labels
-----------------------

Generating mailing labels is a very easy and useful function.

1.  Perform the search to select the contacts you want to target.
2.  Choose **Mailing Labels** from the **Actions** dropdown menu and
    click Go.
3.  Select the mailing label style
4.  Determine if you want to exclude people with "do not mail" checked
    in their privacy options (checked by default and recommended), and
    whether you want to merge any records with the same mailing address
    into one label.

This last option is very useful when sending a mailing to a households
or organisations where you don't want them to receive duplicate
mailings. When the records are merged, each name at that address is
listed on a separate line on the label.

Your system administrator can configure the fields included in mailing
labels. Read the information on configuring address settings in the
Contacts chapter to learn more about the options.
