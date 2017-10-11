# Tokens and mail merge

You can use data in your CiviCRM database to set up mail merge
communications both for emails and printed materials such as letters and
mailing labels. The mail merging functionality relies on Tokens, which
represent items in your database. This chapter explains how tokens work
and how to use them in generating printing materials. Using tokens in
emails is further addressed in the Email section of this book.

## Tokens

Tokens are the equivalent of mail merge fields in CiviCRM. This means
that it is possible to insert information from the database into an
email or a letter that is different for every recipient. For example,
use the Postal Greeting token to include a customized greeting for each
recipient in your PDF letters. Most contact fields, including custom
fields you've created, are available as mail merge tokens. You can view
available tokens by clicking the **Insert Token** link in the top right
corner of the message editing area.

Most of the tokens contain information that is in the database fields.
However, there are some special tokens that accomplish specific tasks in
emails, such as a link to an opt-out page or link to choose mail
formats. Some tokens are only available for mass mailings, such as the
token to provide a link to a message stored online.

![New email screen with the token list expanded.](../img/Tokens-4.5.png)

### Checksum token

A particularly useful token is the checksum. The checksum allows you to
give people links to contribution forms, profiles, petitions, and event
registration forms that are prefilled with information that is already
in their contact record. The image above shows an example of this.

Only contact fields and actions can be inserted in your email as tokens.
Related records, such as the name of the event for which the contacts
have pending enrollments, cannot be included. However, you could provide
a link to the person's contact dashboard so that they can review their
registration details for themselves (once logged in), or you could use a
checksum token to allow access to a profile through which they can
modify their information without having to log in.

Go to this page for further details on using the checksum
token: [http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens](http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens).

### Custom tokens

It is also possible to have custom tokens created by a developer. For
instance, the total amount of contributions from a contact. To find out
more about working with custom tokens, refer to the discussion about
custom mail merge tokens in the Hooks chapter of the Extending CiviCRM
section of this book and look at the wiki:
[http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens](http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens).

Another task for a developer is to create if/then logic for your mail
merge. This is done using the smarty template language as described here
[http://www.smarty.net/docs/en/language.function.if.tpl](http://www.smarty.net/docs/en/language.function.if.tpl).


-
