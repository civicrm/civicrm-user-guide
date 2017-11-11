# Scheduled jobs

CiviCRM relies on a number of scheduled jobs that run automatically on a regular basis. These jobs keep data up-to-date and perform other important tasks. For example, there is a job which sends scheduled reminders, a job which checks for CiviCRM software updates, and many other jobs too. 

## How scheduled jobs are initiated {:#initiation}

An important characteristic of scheduled jobs is that they run *automatically*. However, CiviCRM (like most other web-based applications) actually can't _initiate_ actions itself &mdash; it can only _respond_ to actions that other systems initiate. For most of CiviCRM's functionality, it relies on _people_ to initiate those actions. For example, when a person submits a form, CiviCRM creates a new contact record. Because scheduled jobs must run automatically, CiviCRM relies on a piece of external software called "cron" to initiate them.

### Understanding cron {:#cron}
    
"Cron" is a piece of software, separate from CiviCRM, which is typically installed on server systems to initiate tasks automatically. Here are some important points to understand about cron, as you configure your CiviCRM scheduled jobs:

* Cron must be setup to initiate CiviCRM's scheduled jobs before those scheduled jobs will run automatically. That setup is outside the scope of this User Guide because it involves "system" level tasks that you can't do from within the CiviCRM user interface.

    !!! tip "Cron setup"
        To setup cron, refer to the [Cron setup](https://docs.civicrm.org/sysadmin/en/latest/setup/jobs/#cron) page in the System Administrator Guide.
        
* Cron can be configured in different ways.
        
    * You system administrator will typically configure cron to run on a regular interval with a frequency between 5 and 60 minutes. Each time cron "runs", cron tells CiviCRM to execute whatever scheduled jobs CiviCRM deems necessary at that time. This means that the granularity available to configure specific scheduled jobs is limited by the cron job frequency. For example, if cron only runs once every day, then it will not be possible for a scheduled job to run every hour. So it's best to have your system administrator configure cron to run frequently enough to meet your needs.
    
    * Alternatively, system administrators can configure _separate_ cron jobs to run specific CiviCRM scheduled jobs, although this type of setup is less common.

    * From within the CiviCRM user interface, there is no way to see how cron is configured.

## Configuring scheduled jobs {:#configuring}

To configure scheduled jobs, go to **Administer > System Settings > Scheduled Jobs**.

### Scheduled jobs vs API calls {:#jobs-vs-api}

CiviCRM has a subsystem called the "API" which allows developers and integrators to perform all sorts of useful tasks. (You can read the full [API docs](https://docs.civicrm.org/dev/en/latest/api/) in the Developer Guide.) CiviCRM *users* typically don't need to understand anything about the API, but when interacting with scheduled jobs, some understanding is helpful.

An "API call" is basically an instruction for CiviCRM to do something. For example, the `ContributionPage.create` API call will create a new contribution page &mdash; and the person constructing the API call can add *parameters* to it in order to specify characteristics of that newly created contribution page, like its title and financial type. Each API call has an "entity" (`ContributionPage` in the above example), and an "action" (`create` in the above example). 

A scheduled job is the combination of an API call and a schedule (e.g. "hourly"). When you add a new scheduled job, you can specify *any* API call. So, you could for example, use scheduled jobs to automatically create a new contribution page every day. Of course this example is not very useful. What makes scheduled jobs useful is the fact that the CiviCRM API provides many actions that site maintainers will commonly wish to perform on a regular schedule. For example, the API call `Job.send_reminder` will send scheduled reminders.

### Default scheduled jobs {:#default-jobs}

A fresh install of CiviCRM comes with over a dozen scheduled jobs already partially configured. These "default" scheduled jobs offer a starting point for you to configure your own scheduled jobs. If you like, you can rename them or delete them. Then later on, you can refer to the [specific jobs](#specific-jobs) section of this page for all the necessary details to re-create any of these default scheduled jobs (and other jobs too).

!!! caution "Parameters needed"
    Some of the default scheduled jobs require [parameters](#parameters) to be configured before they can run properly.

### Job frequency {:#frequency}

Some jobs need to be run very frequently, for example the email send task should typically be run once every 5 or 10 minutes. Others need to be run less frequency, for example the membership update script can easily be run just once a day.

When adding or editing a scheduled job you can select a "Run frequency" as follows:

* Yearly
* Quarterly
* Monthly
* Weekly
* Daily
* Hourly
* Every time cron job is run

!!! note
    As described in the [cron](#cron) section above, your system administrator will need to configure cron to run at a specified interval. Every 5 minutes is a common frequency, but from within the CiviCRM user interface it's impossible to determine cron's schedule. Scheduled jobs cannot run more frequently than cron. So if cron is set to run weekly, then choosing the "daily" setting for a scheduled job will mean that it only gets run weekly. 

### Job timing {:#timing}

Let's pretend you want to schedule a job to run monthly, but it's also important to you that the job be run on the 15th day of each month. Unfortunately the scheduled jobs system system does not allow you this level of control. When you set a job to run monthly, it will continue to run one month after the first time it is run.

If you need more control over your job timing, you can [create separate cron jobs to execute specific CiviCRM API calls](https://docs.civicrm.org/sysadmin/en/latest/setup/jobs/#specific-jobs-via-cron).

### Command parameters {:#parameters}

When editing a scheduled job, CiviCRM gives you a "command parameters" field where you can specify input parameters which affect the way the job runs. Each job has its own parameters, and some jobs don't accept any parameters. The parameters for each job are documented in detail within the [specific jobs](#specific-jobs) section below. 

!!! note "Example"
    
    Let's look at an example of how you use these parameters to fill out the "command parameters" field...
    
    The [Job.mail_report](#job_mail_report) job documents the following parameters:
    
    > * `instanceId` (required): ID of report instance to send
    > * `format` (optional)
    >     * `pdf` (default)
    >     * `csv`  to output the report as a CSV file instead of default PDF format
    >     * `print` output the report as printer-friendly HTML
    > * `sendmail` (optional):
    >     * `1` send email
    >     * `0` _don't_ email the report. Use this in combination with `print` or `csv` format to write report to stdout so you can save it to a disk file.
    
    So for example, you might choose to fill out the "command parameters" field as follows:
    
    ```text
    instanceId=7
    format=csv
    ```

As you can see in the example above, you'll need to use the following process to fill out the "command parameters" field:

* Use one parameter per line
* Use an equals sign `=` between the parameter and its value
* Don't use any spaces
* Don't use any quotes

### Manually executing a scheduled job {:#manual-execution}

You can also run scheduled jobs on a one-off basis by clicking the **More > Execute Now** link for the given job on the Scheduled Jobs page. This is useful for some of the scheduled jobs that are designed to be run less frequently, including the geo-coding job and the greetings and addressees job.

### Viewing the job log {:#log}

From the Scheduled Jobs screen, you can click **View Log (all jobs)** or **View Job Log** for a specific scheduled job. Viewing this log is useful for troubleshooting purposes. You can make sure the jobs are running and examine any errors that the jobs output.

!!! note
    The log displays separate entries for the time when a job begins and the time when it finishes. You can examine the time difference between these entries to see how long the job took to complete. Error messages are only displayed in the log entry for the job completion.


## Specific jobs {:#specific-jobs}

### Job.cleanup {:#job_cleanup}

Removes temporary data and files, and clears old data from cache tables. Recommend running this job every hour to help prevent database and file system bloat. 

* Name of scheduled job created by default: Clean-up Temporary Data and Files
* Recommended frequency: hourly
* Parameters: 
    * `session` (optional)
        * `1` (default) clean up session cache
        * `0` skip
    * `tempTables` (optional)
        * `1` (default) clean up tempTables cache
        * `0` skip
    * `jobLog` (optional)
        * `1` (default) clean up jobLog cache
        * `0` skip
    * `prevNext` (optional)
        * `1` (default) clean up prevNext cache
        * `0` skip
    * `dbCache` (optional)
        * `1` clean up dbCache cache
        * `0` (default) skip
    * `memCache` (optional)
        * `1` clean up memCache cache
        * `0` (default) skip
    * `tplCache` (optional)
        * `1` clean up tplCache cache
        * `0` (default) skip
    * `wordRplc` (optional)
        * `1` clean up wordRplc cache
        * `0` (default) skip

### Job.disable_expired_relationships {:#job_disable_expired_relationships}

Disables relationships that have expired (ie. those relationships whose end date is in the past).

* Name of scheduled job created by default: Disable expired relationships
* Recommended frequency: daily
* Parameters: *(none)*

### Job.fetch_activities {:#job_fetch_activities}

Inserts activity for a contact or a case by retrieving inbound emails from a mail directory

* Name of scheduled job created by default: Process Inbound Emails
* Recommended frequency: hourly
* Parameters: *(none)*

### Job.fetch_bounces {:#job_fetch_bounces}

Fetches bounces from mailings and writes them to mailing statistics

* Name of scheduled job created by default: Fetch Bounces
* Recommended frequency: hourly
* Parameters:
    * `is_create_activities` (optional)
        * `1` create activities for bounces
        * `0` (default)

### Job.geocode {:#job_geocode}

Retrieves geocodes (lat and long) and / or parses street addresses (populates street number, street name, etc.)

!!! note
    Geocoding provider must be configured (Administer > System Settings > Mapping and Geocoding). Street Address Parsing must be enabled (Administer > Localization > Address Settings). 

* Name of scheduled job created by default: Geocode and Parse Addresses
* Recommended frequency: daily
* Parameters: 
    * `geocoding` (required)
        * `1` perform geocoding
        * `0` do not perform geocoding
    * `parse` (required)
        * `1` perform parsing
        * `0` do not perform parsing
    * `start` (optional) specify a contact ID (integer) as the point to begin processing
    * `end` (optional) specify a contact ID (integer) as the point to end processing
    * `throttle` (optional)
        * `1` pause for 5 seconds after processing a contact
        * `0` don't pause

### Job.group_cache_flush {:#job_group_cache_flush}

This job purges aged smart group cache data (based on the timeout value). Sites can decide whether they want this job and / or the [group cache rebuild](#job.group_rebuild) job to run. In some cases performance is better when old caches are cleared out prior to any attempt to rebuild them. Also, many sites are very happy to have caches built on demand, provided the user is not having to wait for deadlocks to clear when invalidating them.

* Name of scheduled job created by default: *(none)*
* Recommended frequency: 
* Parameters: *(none)*

### Job.group_rebuild {:#job_group_rebuild}

Rebuilds the smart group cache. 

* Name of scheduled job created by default: Rebuild Smart Group Cache
* Recommended frequency: every time cron job is run
* Parameters: 
    * `limit` (optional): specify a number to limit the number of smart groups that will be rebuilt

### Job.mail_report {:#job_mail_report}

Generates and sends a copy of the specified report instance to the email addresses configured in that instance's Report Settings.

* Name of scheduled job created by default: Mail Reports
* Recommended frequency: daily
* Parameters: 
    * `instanceId` (required): ID of report instance to send
    * `format` (optional)
        * `pdf` (default)
        * `csv`  to output the report as a CSV file instead of default PDF format
        * `print` output the report as printer-friendly HTML
    * `sendmail` (optional):
        * `1` send email
        * `0` _don't_ email the report. Use this in combination with `print` or `csv` format to write report to stdout so you can save it to a disk file.

### Job.process_batch_merge {:#job_process_batch_merge}

* Name of scheduled job created by default: *(none)*
* Recommended frequency: 
* Parameters: 
    * `rule_group_id` Dedupe rule group id, defaults to Contact Unsupervised rule
    * `gid` group id
    * `mode` (optional) helps decide how to behave when there are conflicts.
        * `safe` (default) skips the merge if there are any un-resolved conflicts
        * `aggresive` does a force merge 
    * `auto_flip` (optional)
        `1` let the api decide which contact to retain and which to delete?

### Job.process_mailing {:#job_process_mailing}

* Name of scheduled job created by default: Send Scheduled Mailings
* Recommended frequency: every time cron job is run
* Parameters: *(none)*

### Job.process_membership {:#job_process_membership}

Updates membership statuses

* Name of scheduled job created by default: Update Membership Statuses
* Recommended frequency: daily
* Parameters: *(none)*

### Job.process_participant {:#job_process_participant}

Updates pending event participant statuses based on time. Moves participants from "On waitlist" to "Pending from waitlist" as space becomes available. Moves any type of Pending registrations to "Expired" if expiration period is set for an event. Sends notifications of status changes to participants. 

* Name of scheduled job created by default: Update Participant Statuses
* Recommended frequency: every time cron job is run
* Parameters: *(none)*

### Job.process_pledge {:#job_process_pledge}

Updates pledge payment and pledge statuses and optionally sends payment reminders 

* Name of scheduled job created by default: Process Pledges
* Recommended frequency: daily
* Parameters: 
    * `send_reminders` (optional): 
        * `0` (default)
        * `1` send pledge payment reminder emails 

### Job.process_respondent {:#job_process_respondent}

Releases reserved survey respondents when they have been reserved for longer than the Release Frequency days specified for that survey.

* Name of scheduled job created by default: Process Survey Respondents
* Recommended frequency: every time cron job is run
* Parameters: *(none)*

### Job.process_sms {:#job_process_sms}

Sends out scheduled SMS

* Name of scheduled job created by default: Send Scheduled SMS
* Recommended frequency: every time cron job is run
* Parameters: *(none)*

### Job.run_payment_cron {:#job_run_payment_cron}

Runs handlePaymentCron method in the specified payment processor

* Name of scheduled job created by default: *(none)*
* Recommended frequency: 
* Parameters:
    * `processor_id`
    * `processor_name`

### Job.send_reminder {:#job_send_reminder}

Sends out scheduled reminders via email

* Name of scheduled job created by default: Send Scheduled Reminders
* Recommended frequency: daily
* Parameters: *(none)*

### Job.update_greeting {:#job_update_greeting}

Updates email greeting, postal greeting and / or postal addressee for contacts

!!! note
    To configure the format of the generated values, go to **Administer > Communications > Email Greeting Formats** and **Administer > Communications > Postal Greeting Formats**. 

* Name of scheduled job created by default: Update Greetings and Addressees
* Recommended frequency: daily
* Parameters: 
    * `ct` (required): `Individual`, `Organization`, or `Household`
    * `gt` (required): `email_greeting`, `postal_greeting`, or `addressee`
    * `id` (optional): force script to set a greeting or addressee format other than default for a given contact type, use ID of format option value)
    * `force` (optional):
        * `0` only contacts with null values are updated (default)
        * `1` update all contacts
    * `limit` (optional): specify a number to limit the number of contacts to update

### Job.version_check {:#job_version_check}

Checks for CiviCRM version updates. Important for keeping the database secure. Also sends anonymous usage statistics to civicrm.org to to assist in prioritizing ongoing development efforts.

* Name of scheduled job created by default: CiviCRM Update Check
* Recommended frequency: daily
* Parameters: none

### Mailing.update_email_resetdate {:#mailing_update_email_resetdate}

Updates the reset_date on an email address to indicate that there was a valid delivery to this email address. 

* Name of scheduled job created by default: Validate Email Address from Mailing
* Recommended frequency: daily
* Parameters: 
    * `minDays` (optional)
    * `maxDays` (optional)
