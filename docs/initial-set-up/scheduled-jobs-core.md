# Core jobs

Below is a table of common jobs which might appear on a CiviCRM install.Extensions can add their own jobs - jobs for your site are in CiviCRM under Administer ▶ System Settings ▶ Scheduled Jobs.

name | entity.action | run_frequency | description
--- | --- | --- | ---
Send Scheduled Mailings | job.process_mailing | Always | Sends out scheduled CiviMail mailings
Fetch Bounces | job.fetch_bounces | Hourly | Fetches bounces from mailings and writes them to mailing statistics
Process Inbound Emails | job.fetch_activities | Hourly | Inserts activity for a contact or a case by retrieving inbound emails from a mail directory
Process Pledges | job.process_pledge | Daily | Updates pledge records and sends out reminders
Geocode and Parse Addresses | Job.geocode | Daily | Retrieves geocodes (lat and long) and / or parses street addresses (populates street number, street name, etc.)
Update Greetings and Addressees | job.update_greeting | Daily | Goes through contact records and updates email and postal greetings, or addressee value
Mail Reports | job.mail_report | Daily | Generates and sends out reports via email
Send Scheduled Reminders | job.send_reminder | Daily | Sends out scheduled reminders via email
Update Participant Statuses | job.process_participant | Always | Updates pending event participant statuses based on time
Update Membership Statuses | job.process_membership | Daily | Updates membership statuses. WARNING: Membership renewal reminders have been migrated to the Schedule Reminders functionality, which supports multiple renewal reminders.
Process Survey Respondents | job.process_respondent | Always | Releases reserved survey respondents when they have been reserved for longer than the Release Frequency days specified for that survey.
Clean-up Temporary Data and Files | job.cleanup | Hourly | Removes temporary data and files, and clears old data from cache tables. Recommend running this job every hour to help prevent database and file system bloat.
Send Scheduled SMS | job.process_sms | Always | Sends out scheduled SMS
Rebuild Smart Group Cache | job.group_rebuild | Always | Rebuilds the smart group cache.
Disable expired relationships | job.disable_expired_relationships | Daily | Disables relationships that have expired (ie. those relationships whose end date is in the past).
Validate Email Address from Mailings. | mailing.update_email_resetdate | Daily | Updates the reset_date on an email address to indicate that there was a valid delivery to this email address.
Call SumFields.Gendata API | SumFields.Gendata | Hourly | Call SumFields.Gendata API
Civirules cron | Civirules.Cron | Daily | Trigger civirules cron triggers
Process delayed civirule actions | CiviRuleAction.Process | Always | 
