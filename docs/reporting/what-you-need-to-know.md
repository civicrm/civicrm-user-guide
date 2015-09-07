What You Need To Know
=====================

This chapter explains key ideas that are useful when planning your use
of CiviReport. It should be read by system administrators before they
start to configure CiviReport for daily use. It will also be useful for
anyone who wants to better understand the thinking behind CiviReport.
Skip this chapter if you just want to look at specific reports that have
already been configured by your administrator.

CiviReport can be used as a management tool in organisational planning
and as an analysis tool for membership or donor development. Tabular or
graphical output can be produced and set up to email reports to specific
people according to a schedule.

The number of questions an organisation might want to ask about their
data is pretty much unlimited. The CiviCRM approach to solving this
problem is to aim to cater for 90% of the scenarios and allow the system
to be easily extendible by administrators and developers to cover the
last 10%.

Key Concepts
------------

### Report templates

A report template is the base for creating any number of reports.
CiviCRM comes with a number of predefined report templates that can be
used to create specific reports. For example, the Membership
Report(Detail) template can be used to create a report that shows all
student members that have joined your organisation within the past
quarter or another that shows all cancelled memberships this year.

These templates are built to satisfy the basic needs of non-profits and
organisations and future versions of CiviCRM are likely to include
further report templates. You can create new templates to meet the
specific requirements of your organisation and contribute these reports
back to the CiviCRM community for others who have the same reporting
needs. Writing a new report template requires some PHP and SQL skills.
See the Developer Guide for details of how to do this. 

### Report vs. Search

CiviCRM has inbuilt search functionality that covers most scenarios, so
it's important to know when to use a report and when to
search. CiviReport gives users the ability to easily display complex
information about their data, and to display answers to questions about
this information in accessible ways. It is useful when you need to
repeatedly ask the same question, or a set of similar questions, about
your data.

The current report interface does not support most common batch actions
such as Update via Batch Profile, Smart Group creation and so on. This
means that if you want to perform any action against a result set, it is
better to use search rather than report.

However, in some cases reports are more flexible than searches, and each
has its own set of features. For example, reports allow you to change
the columns displayed and in summary reports you can order by whichever
display results you choose.

### Report options

-   **Run the report:** you can **Print Report** so it is viewable in
    browser or you can generate a PDF or Export to CSV. All of these run
    the report once when you hit the button and allow you work with it.

-   **Dashlet:** if you make a report **Available for Dashboard** users
    with appropriate permissions can add this report to their dashboard.
    This is useful for information that you want to see on a regular
    basis, such as a list of new members, or donations this month, etc.
    In this case the report is run every time the dashboard is loaded.
-   **Email:** schedule a regular email of the report so that your
    finance office can receive a monthly email of all event fees
    received or your membership administrator gets a weekly email of
    overdue renewals.

### Detail vs summary reports

Reports often come in pairs: one showing a summary and the other showing
the detail. These reports can be linked, allowing users to see
information at a glance with the option to drill down in a certain
report for more detail.

Key Questions
-------------

-   Should you use CiviReport for a particular task, or could it be
    better achieved with a search?
-   What reports are available? The list is constantly growing; for a
    complete list of reports available in your version, along with an
    explanation how the reports can be used, look at the page **Create
    reports from templates** (in the **Reports** dropdown menu).
-   What questions do you want to ask about your data? For example, you
    may want to know how many new members you have in a certain period,
    or how much money was collected during a fundraising campaign.
-   What fields do you need to include?
-   Does the report provide enough options or will you need to analyse
    further in a spreadsheet?
-   Is it a one off report or will you need to run it regularly? Could
    you make a report template to streamline future reports?
-   Who needs to see this report? Will it provide sensitive information
    that should only be available to privileged users or does it give
    useful daily updates to all?

Details of available report templates and comparison with searches are
provided for each component throughout the rest of this book; refer to
the relevant section for more details about component-specific reports.

