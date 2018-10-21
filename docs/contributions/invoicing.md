# Invoicing

Invoicing works for all Financial Types and Completed and Pending
Contribution Statuses and has to be enabled. To enable invoicing go
to **Administer > CiviContribute > CiviContribute Component Settings** and
check the "Enable Tax and Invoicing" box.

In this screen you can set certain settings for invoices as well:

-   add a prefix for invoices
-   the interval of days, weeks, or years until due date
-   customized notes or standard terms you want to appear on your
    invoice

![screenshot](/img/civicontribute_comp_settings.png)

## Creating an Invoice

Once Invoicing has been enabled, you can easily email or print invoices
for Complete or Pending Contributions from a contact's **Contribution**
Tab.

1.  Go to Contact's Contribution tab
2.  View the record you want to create an invoice for

![List of contributions for a specific contact.](/img/contribution_summary.png)

1.  Once you are viewing the record you have the option to Print Invoice
    or Email Invoice. Printing an Invoice will download a pdf and
    Emailing an Invoice will provide an additional Options screen.

![The print invoice and email invoice buttons are at the bottom of the contrbution screen.](/img/contributiion_view_Screen.png)

1.  Once you have chosen the Email Invoice option you have options
    before sending:

-   From Email Address

-   Type an additional message

![E-mail message.](/img/email_invoice.png)

Here is an example of a printed invoice. Invoices can be customized.

![Invoice example.](/img/invoice.png)

## Invoice Customization

The out of the box template code populates the Company Name, Address,
and Website Information listed on the top right of invoices come
directly from the Organization Address and Contact Info. To make any
edits to this information, you can access it at **Administer Console >
Configuration Checklist > Organization Address and Contact Info**.

The look of the invoice and invoice image can be edited and customized
in **Administer > Communications > Message Templates > System Workflow Messages > Contributions-Invoice.**

To change the image on the invoice you will need to modify the code on
line 10, replacing the image source (img src).

```html
<td><img src = "{$resourceBase}/i/civi99.png" height = "34px" width
= "99px"></td>
```
For more advanced configuration with accounting software packages like
QuickBooks, you should involve your organization's bookkeeper or
accountant in setting up your Financial Types and Financial Accounts.
See Accounting Integration and the Wiki Page for more information.
