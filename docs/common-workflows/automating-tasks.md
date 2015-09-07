Automating tasks
================

If you find yourself making the same set of decisions regularly, more
often than not, CiviCRM can free you from having to make them again.
Automating administrative or routine tasks, more commonly referred to as
workflows, take quite a bit of work to set up, but save a tremendous
amount of time in the long run. To get started, realize that every
decision, no matter how arbitrary it may feel, can be made based on a
set of criteria and information that satisfies that criteria. We'll help
you think through what criteria you might be using to make decisions
that CiviCRM could easily make for you. The second step will be to find
places for information that corresponds with your criteria in CiviCRM
and then teach CiviCRM which action to take in response. Here is an
example:

> *Goal*: Automatically personalize acknowledgment letters

> *Focus Questions*: What letters do I edit and what information do I
> add? Where do I find information that needs to be added? What CiviCRM
> features can help accomplish this task?
>
> *Strategy*: Create custom tokens and print to PDF function in CiviCRM
>
> *Custom Fields*: Fund Name, Tag “Works with Organization,” Tax Receipt
> Pull-Down (No Tax Receipt, Extra Tax Receipt to Soft Credit, Tax
> Receipt to Hard Credit), Relationship “Known by Organization Staff”
>
> *Existing Fields*: Thank You Letter Sent, Soft Credit
>
> *Custom Tokens*: First Gift Date, Financial Type, Soft Credit Address
> and Main Contact
>
> *Variations in Template Language*:
>
> -   Include/Exclude Fund Name - based on the fact that the money was
>     donated to the fund or as a generic donation
> -   Include/Exclude Tax Receipt - based on information if this
>     contribution is eligible for tax receipt
> -   Include/Exclude Invitation for Sponsorship - based on the fact
>     that the organization receiving this email was a sponsor in the
>     past
> -   Include/Exclude Invitation to Visit Office - based on the address
>     of the recipient; if constituent is located close by, include the
>     invitation.

The goal refers to which routine task you would like to automate. It can
be: email me a report of major donations the organization receives each
day, send a reminder email to anyone who has registered for an upcoming
event, remind me when it's time to follow up with a donor about an
outstanding invitation to meet for lunch, send a renewal notice to
anyone whose membership is about to expire, or send a reminder email to
anyone who has promised to make 4 more donations to your organization.
CiviCRM has the capability of doing all these things out-of-the box. To
learn more about how you can set these tasks up, visit the chapters that
discuss functionality of CiviCRM components (chapters like Events,
Membership, Contributions, Scheduled Jobs, Reporting etc.).

But there are probably a number of other, more complicated tasks, that
with a little customization, CiviCRM could do for you as well. These
might include sending personalized acknowledgment letters to certain
donors or giving members access to member-only content, discounts,
mailings and other benefits on your site.

Answering focus questions will require reflection and research. As an
expert in what you do, try to articulate what piece of information helps
you realize that this person, donation or organization deserves
different treatment. Maybe this individual is personally known by
someone at your organization, maybe this donation requests a unique
language in their acknowledgment letter, maybe this volunteer only wants
to hear about opportunities to support a particular program.

When you make the decision to give someone or something different
treatment, do you have to hunt down any additional information? For
example, do you have to find a spouse's name or the address of someone's
company? Write out what pieces of information you add or what language
you change. If you are familiar with writing conditional statements,
try explaining your decision making process in the following format:

*If the Spouse Name field is not empty, include spouse name in the line
address*

*If last contribution amount is greater than $10,000 and City is within
the Zip Code Range 94110 to 94114, include as the last line in the
opening paragraph: "It looks like you're in the neighborhood. Would you
enjoy stopping by the office to speak more about our work and meet the
staff?"*

CiviCRM has myriad features that can be used to help you automate simple
tasks. Sometimes the hardest part is finding them. The case studies
available on civicrm.org can introduce you to how other organizations
are using CiviCRM and subsequent chapters in this book describe what
features are available and how you can start using them. If you are
poking around the CiviCRM interface, the small speech bubbles can also
be a great source for more information on the capabilities each field
offers. To create a complicated workflow, you will ultimately want to
tie several of these features together.

You will most likely have to create custom fields and custom tokens in
order to accomplish your goal. Once you have planned what task you want
to automate and how, create custom fields from the Administrator
Console. Create custom fields carefully. It's always easy to choose a
text field, but they can be impossible to use later in reports or
searches because everyone enters information differently. It's better to
create fields that have pre-defined answers so spelling mistakes are not
an issue. CiviCRM along with any computer program is great at executing
on the basis of well defined facts. They aren't as good at comparing two
facts that look the same, even if the difference is only one letter in a
differently spelled word. You might also be tempted to create several
Yes/No radio buttons to capture a set of facts that might work better as
a drop down menu.

To be a good database manager, you don't have to understand everything
about relational databases. It can, however, be helpful to understand
your system's underlying structure in order to understand some of the
consequences related to that structure.

For example, you might wonder why you can't create a friend relationship
between two organizations. The organizations might be partners, but if
the database was told to only recognize the relationship type "friend"
between two individuals, that constraint on the database will not let
you freely use relationship "friend" for organizations. A fix to that
relationship definition will fix the problem but people are often
tempted to find a workaround for a problem rather then actually fix the
problem. We strongly recommend looking into the reasons why something
doesn't work for you and addressing the problem at its root instead of
applying a "patch".

CiviCRM comes with multiple pre-defined reports that should cover most
of your needs, but more complicated searches may require creating custom
reports. You may hesitate to hire a professional to create a proper
report to search your specific criteria, but if you are currently
copying/pasting information to spreadsheets, you may consider this one
time expense worthwhile in the long run.

In general, our advice is to have high expectations of your CiviCRM (and
other software) and automate as much of your manual work into the system
as you can to free yourself from daunting administrative activities that
computers can do faster and more accurately.
