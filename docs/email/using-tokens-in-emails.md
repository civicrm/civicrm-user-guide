# Using tokens in emails

You can use tokens to insert personalized text (such as a person's
name), to add action links (such as an unsubscribe option), or display
standard organization information (such as domain address) into a mass
mailing sent with CiviCRM. Tokens are replaced by the appropriate value
at the time the email is sent out.

To view the list of available contact tokens, click on **Insert
Tokens**. For more information about tokens in general, see *Mail merge
functions (a.k.a. using Tokens)* in the *Working with Your Data* section
of this book.

## Contact data tokens

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

## **Action and Organizational Tokens**

You can also insert action tokens, such as opt-out, unsubscribe and
forwarding tokens. These tokens insert links to take the specified
action; in order to display the links properly in HTML messages, you'll
need to add the proper link tags using the Source icon in the editor.

You can also insert standard organization information, such as "Domain
(organizational) address," which displays the address of your
organization as defined at **Administer > Communications >
Organization Address and Contact Info**. For a complete list of action
and organizational tokens, see:
[http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens](http://wiki.civicrm.org/confluence/display/CRMDOC/CiviMail+Action+and+Organizational+Tokens).

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


## Custom and Checksum Tokens

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
