# Message Templates

## Message Templates Overview

MESSAGE TEMPLATES allow you to create and edit re-usable email and letter messages. There are two categories of Message Templates in CiviCRM:

* **User-driven Messages** - These are messages created by your staff to communicate with constituents that you want to be able to re-use. Examples include thank-you letters, meeting announcements, etc.
* **System Workflow Messages** - These are pre-configured messages used by CiviCRM "features". Examples include contribution receipts, event registration confirmations.

## Modifying System Workflow Message Templates

The content and layout of these messages are pre-configured and include program logic to display all the data being sent to your constituents (e.g. contribution amount, payment method, event fees, etc.). Navigate to Administer > Communication > Message Templates (shown in the following screenshot) and click the System Workflow Message tab to see the list of messages you can modify.

Both HTML and Text formats are provided. Your organization may want to modify or add text to these emails, or add branding such as a logo to the HTML versions. Use caution when editing so as not to modify the program logic. Be sure to test the workflow and review the emails sent after making any changes. In most cases, you can restrict your changes to the the top row in the HTML layout. If you find that your changes have caused problems, errors or missing information, you can always revert to the system default for that workflow.

## Upgrades and Customized System Workflow Templates

When your site is upgraded to a new version of CiviCRM there may be changes needed in the message template program logic to support new features. You will be notified during the upgrade that changes are required. **However, you will need to apply these changes manually for any workflow templates which you have modified previously**. Follow these steps:

* Navigate to Administer > Communication > Message Templates (shown in the following screenshot) and click the System Workflow Message tab
* Click the 'Edit' link
* Open 2 new blank documents in a text editor
* Copy and paste your customized HTML message into one of the blank documents, and your customized TEXT message into the other
* Click 'Cancel' to return to the listing of message templates
* Click 'Revert to Default' for the message template you're updating. This will replace your customized version with the upgraded version included all program logic - but NOT including your customizations.
* Click 'Edit' again to review the new message versions, and compare to the customized versions saved in your text editor.
* Copy / paste your customized changes from your text editor copies back into the new version in the CiviCRM screen. If you've only made changes to the header / introductory section of the message - this should be pretty straightforward. Otherwise you may need to use a command line tool like 'diff' to make sure you've caught all the changes needed.
* Save your newly customized version of the messages.

## Working with User-driven Messages

You can personalize your messages by including "tokens" to represent fields (like a contact's "first name") in your message's subject and body. These "tokens" will be replaced with the actual value of the corresponding field in your message (EXAMPLE: Dear{contact.first_name} = Dear Jose, Dear Vanessa, etc.)

If you are using the CiviMember component, you can also use a message template to send Membership Renewal Reminders.

!!! tip

    If you need to add custom logic to a system message template, [you can do so using "Smarty" coding](https://docs.civicrm.org/sysadmin/en/latest/setup/message-templates/#smarty-in-mail-templates).


## Configure Message Templates

To configure message templates, begin at the **Administer CiviCRM** page.

In the **Communications** section, choose **Message Templates**.

You will see a list of existing templates. If no templates exist, you will see the message:

> There are no Message Templates entered. You can add one.

Click **add one** to create a new template.

You can create NEW message templates or **Edit** , **Preview** , **Disable** or **Delete** EXISTING message templates using the links to the right of each template.

### NEW

To create a NEW message template, choose **>>New Message Template**

You will be taken to the New Message Template page.

Create a **Message Title** for the template. This title is used to organize your messages and will not appear in the email.

**TOKENS** : The next three fields can all use "tokens". You insert a "token" into your message to help personalize your messages with things like names, dates and amounts of gifts, etc. When you send the email, CiviCRM will look at each contact record that is set to receive the message and replace the "token" with the actual value from the contact record. Rather than a generic, impersonal message that says "Dear Friend, Thank you for your recent contribution..", you can create personalized messages like "Dear Eleanor and Franklin, Thank you for your $50 gift on June 6th..."

Here is a list of the tokens you can use

Create the **Message Subject** for your email. Use tokens if desired, i.e., "We need your help, Alice", where you have used the token {contact.first_name} to put recipients first names into the message subject.

Create your **Text Message** and **HTML Message**. Include tokens to personalize your messages.

Choose *Enabled?" to enable the message template for use.

Click **Save** to save the template or **Cancel** to cancel.

If successful, you will see the message:

> "The Message Template "Membership Renewal Initial Message" has been saved."

### EXISTING

For EXISTING templates you can **Edit** , **Disable** or **Delete** each template using the links to the right of each template.

### EDIT

Select **Edit** to view the Edit Template page where you can change the values for each option. Here you can also enable/disable the template by checking or unchecking the box labeled **Enabled?** at the bottom of the page.
 Click **Save** to save the template.

If successful, you will see the message:

> The Message Template "Membership Renewal Initial Message" has been saved.

### DISABLE

Select **Disable** to temporarily disable an Existing Template. You will see the warning:

> "Are you sure you want to disable this Message Template? "

Click **OK** to continue or **Cancel** to cancel disabling the template.

To re-enable the template, simply click on **Enable**.

### DELETE

Select **Delete** to delete the template. You will be given this warning:

> Do you want to delete this message template?

Click **Delete** to continue or **Cancel** to cancel the deletion.
