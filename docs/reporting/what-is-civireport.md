What is CiviReport?
===================

Reporting helps your organisation to evaluate its impact and achieve its
mission. Sometimes this is a requirement for funders or other
stakeholders. CiviReport allows you to create, run and schedule reports
based on the data CiviCRM has about your contacts and their interactions
with your organisation.

These reports are queries on the database using criteria and fields
available in a report template. Reports can be delivered on the page
when you run them, as a dashlet on the dashboard or a scheduled email
which can include a CSV file or PDF.

Scenario: a simple report to help with fundraising
--------------------------------------------------

1two3, a support organisation for street workers, has launched a capital
campaign to raise money for a new shelter. Anne, the development
director wanted to reach out to donors who made a large donation last
year but haven't given money this year.

She created an instance of the LYBUNT report ("Last year
but unfortunately not this") which filters data to show people who gave
more than €500 last year, then ran the report and used the Add to Group
button to put these donors into a new group so she could send an email
to everyone in the group with information about the capital campaign.

Finally she added the report to her CiviCRM Dashboard so she can review
progress getting this group of prior donors to contribute to the
campaign. Anyone who donates will automatically drop off this list since
they will no longer meet the criteria, and the list remaining in the
dashlet can be used as the basis for follow up phone calls or
other personalised contact.

Scenario: a regular financial report
-------------------------------------

WAM is an academic membership organisation with about 1,500 members.
Their members renew their membership online and pay either online by
card or by offline by direct debit. Mark, the finance officer, needs
several reports to keep track of the money coming in and automation of
this process was a key reason for the implementation of CiviCRM. All
these reports are regular and are sent to him by email with a CSV
attachement so he can import the details into either their accounting
software or their online banking interface. While a couple of the key
reports are outlined here, their requirements were fairly complex and
some custom report templates were required alongside the standard ones.

Every Monday morning, Mark receives a list of all completed online
payments for the previous week to import into Sage; this report contains
the amount and time of the payment along with what it was for
(membership or event) and a reference ID so it can be tracked back to
the record in CiviCRM. At the end of every month, he receives a list of
all members who pay by direct debit whose membership is due to expire in
the following month. This allows him to set up the direct debit payments
for these membership renewals by importing part of the list into their
online banking interface.

These email reports save Mark several hours a month and allow him to
focus on issues that contribute more to the effective management of
WAM's financial resources.

Scenario: determining total contributions for a household
---------------------------------------------------------

A non-profit organisation in Ohio keeps records of individuals organised
by households. A common situation is that the husband in the household
has attended a number of paid events, while his wife has also registered
for other events and made separate donations.

Staff at the organisation want to see the total contributions received
from everyone in a household so that when someone calls the office to
enquire about a donation or event payment made by someone else in the
family, all the relevant information is at hand. Staff can run the
Donation Summary Report (Household) as required, using the name of the
household to find all contributions and relevant information to answer
the caller's questions.


