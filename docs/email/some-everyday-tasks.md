# Some everyday tasks

This chapter contains step-by-step instructions for performing some important
everyday tasks with email. Sending a mass mailing through CiviMail is covered
in [Mass mailings using CiviMail](.../email/mass-mailings-using-civimail)

## Send an email to one person (with CC and BCC)

You can use CiviCRM to send an email to individuals. Using CiviCRM for
this purpose is useful if you want other people at your organisation to
see the email or if you want to send an email based on a pre-defined
template.

1.  Find the person you wish to email. There are two common ways to do
    this:
    -   Use the Quick Search box on the top left. Click inside the box
        and begin typing a part of the person's name or email address.
        Choose the person from the choices that are presented.
    -   Navigate to **Search > Find Contact**. Enter part of the
        person's name or email address. Click Search and click on the
        person's name when it shows up on the search results screen.
2.  From the contact summary page, click **Actions > Send an email** or
    click the **Activities** tab and choose **Send an Email** from the
    dropdown menu.
3.  You can add additional recipients using the CC and BCC fields.
4.  If you have templates defined, you can choose one from the Use
    Template dropdown menu. Selecting a template populates the text
    content and HTML content fields with the message content from the
    particular template you have chosen. You can then edit that
    content.
5.  Enter your content or add content to your template. If you just wish
    to send a Plain Text version of your email, ignore the HTML Format
    section and click on the Plain Text Format section. Enter your
    message in the box.
6.  Click **Send** to send your message.

To see the activity that was just recorded of the email sent, click the
Activities tab of the contact.

## Sending a quick email to less than 50 contacts

In the results from a search, CiviCRM makes "Send Email to Contacts"
available from the actions dropdown menu. This allows you to send an
email to more than one contact at a time. Sending an email this way is
relatively quick, but it provides no options for tracking email and
doesn't give contacts the option to opt out. It is bad practice to use
this method for mass mailings, which is why it is limited to 50
contacts. For mass mailings, use CiviMail.

1.  Click **Search > Find Contacts** (or **Advanced
    Search**). Choose your search criteria and click Search (or use
    any other search to find the contacts that you wish to email).
2.  From the search results screen, choose some or all of the contacts
    and click **- actions - > Send Email to Contacts**.
3.  Follow the same steps as in sending an email to one person.

Each of the recipient contacts will have this email recorded as an
Activity in their record. An activity will also be recorded for the
sender. The activity record will also list all the other message
recipients. Unlike with mass mailing (see below) there is no one place
where all emails sent via the Send Email function are listed.

**Note:** If a message is sent to multiple recipients, each recipient
will see only their own email address in the To field. Because the
recipients don't see who else received the email, you might want to
mention whom you are sending it to in the text of your mail (for
instance: "TO: Members of the board, staff")

## Inserting an image in an email

Click the **image button** in the WYSIWYG editor.

![](../img/Screen%20Shot%202015-04-25%20at%203.06.40%20PM.png)

The Image Properties window will appear. Click **Browse Server** to look
for image files on your server.

![](../img/civimail_window%20to%20browse%20server%202.jpg)
In the left sidebar, you will see a directory of files. If the image you
need is already uploaded to your server, navigate to it in the directory
and select it. If not, Click **Upload** to choose a file from your
computer.

![](../img/civimail_file%20directory%203.jpg)

Your computer's file-browsing window will open. Find the image file you
want,
click to select it and click **Open**. You can repeat this process to
upload multiple files to CiviCRM at once.

To insert, double click on the image you want. You'll return to the
Image Properties window of your email.

Here you can add adjust the size and alignment of the image and the
border around it. You can also fill in the Alternative Text field, which
is text that appears when the image is not available to the reader (if
they choose not to load images in their email client, or are using
a[](http://en.wikipedia.org/wiki/Screen_reader "Screen reader") screen
reader due to a visual impairment). The alternative text ensures no
information is lost; it's a best practice to always include alt text for
images to make email accessible to all user communities.

Click **OK** to insert the image.

![](../img/civimail_Insert%20image%206.jpg)



Using tokens in emails
----------------------

You can use tokens to insert personalized text (such as a person's
name), to add action links (such as an unsubscribe option), or display
standard organization information (such as domain address) into a mass
mailing sent with CiviCRM. Tokens are replaced by the appropriate value
at the time the email is sent out.

To view the list of available contact tokens, click on **Insert
Tokens**. For more information about tokens in general, see *Mail merge
functions (a.k.a. using Tokens)* in the *Working with Your Data* section
of this book.

### Contact data tokens

If you want each email to address the person by first name after "Dear,"
you would type a space and then click on **Insert Tokens** at the top
right of the HTML Format field. The popup that appears enables you to
find the appropriate token by typing "First name" in the box and choose
the token that corresponds. Click Close and you will see that your
message now reads "Dear {firstname}." When the email is sent, the
appropriate first name will be inserted into each message. Browse the
Inset Tokens pop-up for a complete list of contact data tokens,
including any of the custom fields that have been created for your site.
You can also refer to:
[http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens](http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens)
for more details.

### **Action and Organizational Tokens**

You can also insert action tokens, such as opt-out, unsubscribe and
forwarding tokens. These tokens insert links to take the specified
action; in order to display the links properly in HTML messages, you'll
need to add the proper link tags using the Source icon in the editor.

You can also insert standard organization information, such as "Domain
(organizational) address," which displays the address of your
organization as defined at **Administer > Communications >
Organization Address and Contact Info**. For a complete list of action
and organizational tokens, see:
[http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens](http://wiki.civicrm.org/confluence/display/CRMDOC41/CiviMail+Action+and+Organizational+Tokens).

Note: You are required to include a token for either opt-out OR
unsubscribe, as well as the organizational (domain) address token in
every CiviMail mailing. These can be placed directly in the body of your
mailing body, or you can put them in the mailing header or footer. If
your organization has developed a standard mailing footer, just include
these tokens in the footer so that folks don't have to think about them
each time they create a new mailing.

In general, including click-able unsubscribe and opt-out links are a bit
friendlier for recipients (as opposed to the reply-to via email method).
You can also provide both options. More details at:
[http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens](http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens)


### Custom and Checksum Tokens

Only contact fields, action links and organizational information can be
inserted in your email as tokens. Related records, such as the name of
the event for which the contacts have pending enrollments, cannot be
included. However, you can provide a link to the person's contact
dashboard so that they can review their registration details for
themselves (once logged in).

You can create and use a token for custom data fields that you have
created to store data about your contacts. You can also create a
checksum token that generates a unique URL for each contact so they can
modify their information without having to log in. See more information
about custom and checksum tokens, including how to construct URLs you
need, at
[http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens](http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens).


**Note:** In the HTML format editing area, tokens that generate URLs
(links) need to be placed in the URL field of the Link creation screen.
Otherwise, they will display as text and not a clickable link in the
email client of the recipient.
