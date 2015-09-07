Scheduled jobs
==============

CiviCRM relies on a number of scheduled jobs that are run on a regular
basis to keep data up to date and to perform certain tasks. These jobs
must be triggered by a [cron](http://en.wikipedia.org/wiki/Cron) that
runs regularly on your web hosting server.

Examples of scheduled jobs include:

-   the membership processing job, which updates membership statuses
-   the event waiting list job, which invites people on the waiting list
    to register for events when spaces become available
-   the CiviMail send and process script which handle the sending and
    processing of emails (to
-   the CiviReport scripts which handle the emailing of reports on a
    regular basis.

Some jobs need to be run very frequently, for example the email send
task tends to be run once every 5 or 10 minutes. Others need to be run
less frequency, for example the membership update script may be run just
once a day.

There are two ways of configuring scheduled jobs:

-   via the user interface, which you can configure at **Administer >
    System Settings > Scheduled Jobs** and a single consolidated cron
    job
-   by configuring multiple cron jobs for specific tasks

These methods are discussed below.


##What is cron?

Cron (think "**cron**ology" or "**cron**ograph") is a time-based
automatic scheduler that triggers certain programs to run on your web
server. Generally speaking, cron (also known as 'a cronjob') can be
setup in your web hosting control panel or configured by the server
administrator in charge of your web hosting. We recommend choosing web
hosting that offers cron as a free service.

Before scheduled jobs configured via the user interface will actually
work you will need to configure a web server CRON job. There are CRON
configuration examples found in the [Running Command-line Scripts via
URL](http://wiki.civicrm.org/confluence/display/CRMDOC/Running+Command-line+Scripts+via+URL) wiki
page.


##Configuring Scheduled Jobs via the user interface

The user interface for scheduled tasks is designed to make it easy for
people to set up scheduled jobs, and avoid having to create or edit a
cron job each time you want to make a change to a scheduled job. Most
smaller installations should be fine configuring and running scheduled
jobs via the user interface. Larger sites should consider creating cron
jobs in the normal way for each task. That requires some system
administration skills.

The Scheduled Jobs page (**Administer**> **System Settings** >
**Scheduled Jobs**) is designed to make it easy to set up scheduled jobs
and to monitor when they were last run. It shows a list of all scheduled
jobs and you can edit each one and set its frequency (hourly, daily or
every time the scheduled job is run - typically this is set as every
5-10 minutes) and also any relevant parameters.

You can find an up to date list of all scheduled jobs and the parameters
that can be sent to them on [Managing Scheduled
Jobs](http://wiki.civicrm.org/confluence/display/CRMDOC/Managing+Scheduled+Jobs)
wiki page.

Some jobs perform special data update tasks and are not designed to be
run automatically or repeatedly. These are: "Update Greetings and
Addressees" and "Set Renewal Reminder Dates". Details about when to run
them are provided on the Managing Scheduled Jobs wiki page. 



##Manual execution of scheduled jobs

The scheduled jobs page can also be used to run scheduled jobs on a one
off basis. This is useful for some of the scheduled jobs that are
designed to be run on a less regular basis, including the geo-coding job
and the greetings and addressees job. Execute a job manually by
clicking the **More > Execute Now** link for the given job
at **Administer > System Settings > Scheduled Jobs**.



##Scheduling specific jobs via individual cron tasks

System administrators more commonly talk about scheduled jobs as cron
jobs. If you run a lot of scheduled jobs on large data sets you may wish
to consider getting an experienced system administrator to set these up
using cron.  This will allow more granular control over when and how
these jobs are executed, which may be useful if these processes put
significant load on your server.

Note scheduled jobs that were run via an individual cron job directly do
not automatically appear here. They need to be configured to do so.
Details on triggering specific jobs via command-line, URL, Drush and
other methods can be found in the [Managing Scheduled
Jobs](http://wiki.civicrm.org/confluence/display/CRMDOC/Managing+Scheduled+Jobs)
wiki page.
