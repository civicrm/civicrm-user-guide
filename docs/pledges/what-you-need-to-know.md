# What you need to know

Before using CiviPledge, you must enable it for your installation, if
you have not done so already. Go to **Administer > System Settings > Enable CiviCRM Components**, and move CiviPledge into the
box on the right to enable it.

## New Pledges

To create a new pledge on behalf of a constituent, navigate to
**Contributions** > **Pledges** > **New Pledge** (note that an
individual may do this themselves through an online contribution form;
see the 'contributions' section).

The options available are as follows:

-   **Select contact**: type the name of an existing contact, or create
    a new one before setting up the pledge (a new window will open)
-   **Total pledge amount**: enter the total amount to be donated
-   **To be paid in**: specify the number of instalments and time period
    for payment, if greater than one
-   **Payments are due on the**: choose the day on which a payment is
    due during that instalment cycle (e.g. the second day of the
    week/month/year)
-   **Pledge made**: select the date on which the pledge was promised
-   **Payments start**: set the date the scheduled payments will start
-   **Send Acknowledgment?**: if outgoing mail is configured, and an
    email address is available for that contact, check this box to send
    a notification email
-   **Acknowledgement date**: the date the individual was notified of
    the pledge's creation (automatically populated if an email was sent)
-   **Financial Type**: choose the Financial Type of the contribution
    (e.g. donation or event fee) to denote what the pledged money is
    meant for
-   **Campaign**: if available, you may assign the pledge to a campaign
    if the money is intended to go towards that fundraising effort
-   **Self-service payments page**: give donors the ability to make a
    payment online by selecting an online contribution form to collect
    the money through
-   **Honoree information**: you may also enter honoree information if
    the individual elects to dedicate the pledge to someone, and set
    payment reminders



![image](../img/new_pledge2.png)

## Payment reminders

One or more payment reminders can be emailed to the donor prior to the
scheduled payment date. If a 'Self-service Payments Page' has been
selected (see below), the reminder will include a link for the
contributor to make their payment online.

In order for reminders to be sent:

1.  The Process Pledges (process_pledge) scheduled job must be enabled
    to updates pledge payment statuses and sends the payment reminders.
    Alternatively a cron job can be scheduled to run this specific task
    apart from other scheduled jobs. Refer to the *Scheduled Jobs*
    chapter for more information.
2.  The donor must have a valid email address (and must not have the "Do
    Not Email" flag checked).

Once these pre-requisites have been met, you can choose the payment
reminder schedule for an individual when creating a new pledge. The
settings are:

-   **Send initial reminder**: enter the number of days, prior to the
    payment date, that a reminder will be sent
-   **Send up to**: specify the maximum number of reminders an
    individual will receive for one scheduled payment
-   **Send additional reminders**: set the interval period between
    reminders, by the number of days, e.g. 5 days before the next
    reminder is sent.

## Self service payments

A donor can be given the option to make a scheduled payment online if a
contribution page (with payment processor) has been created. To do this,
select a contribution page from the drop-down menu 'self-service
payments page' when creating a new pledge. If reminders have been
enabled for the pledge, a link to this page will be included in the body
of the emails.

## Finding Pledges

To search for existing pledges, go to: **Contributions > Pledges >  Find Pledges**. You may search by name, email address, or any
discrete feature of the pledges themselves (e.g. payment start date,
pledge status and honoree information). The search results page will
display a summary of the pledges found, and view, edit and delete
options are available for each record at the end of the rows. If the
status of a pledge is 'in progress', there is also an option to cancel
the pledge.

![image](../img/pledge_menu.png)

## Dashboard

You can view a list of recent pledges and a summary table of pledges
recorded over the current month and past year on the pledges dashboard.
This can be reached through the Contributions menu: **Contributions >
Pledges > Dashboard**.

![image](../img/pledge%20table.png)
