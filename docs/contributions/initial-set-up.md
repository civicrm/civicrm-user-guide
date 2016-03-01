You may need to configure the following fields before you begin setting up various methods for recording and managing contributions.

Financial Types
---------------

Financial Types need to be set-up before you begin using CiviCRM for
financial transactions. (In old versions of CiviCRM, financial types
were known as contribution types.) Each financial type will have
financial accounts associated with it. The financial type is created first.

Navigate to **Administer > CiviContribute > Financial Types**, where you can edit one of the existing Financial Types or create a new one by clicking **Add Financial Type**.

As you create a Financial Type of a specific name, CiviCRM creates a
similarly named Revenue Financial Account and assigns it and the default
accounts for Accounts Receivable and a few other account types to the
new financial type. You can edit the financial accounts allocated to your financial type as needed.  The aim behind this two step process is to simplify the
common use case, but provide flexible for more sophisticated
setups. The setup of Financial Types determines how CiviCRM
transactions relate to them. It needs to be done properly in order to
ensure your export from CiviCRM will correctly transfer financial
transactions into your accounting database.

Financial Accounts
------------------

Accounting software such as Quickbooks requires specific fields to be
included in the import file in order to process external data correctly.
From **Administer > CiviContribute > Financial Accounts**, you can set
up specifics of your financial accounts.

It's important that the account codes and names in your organization's
Chart of Accounts be used to set up the financial accounts in CiviCRM. A
variety of accounts are created by default, and it is often easier to
edit these accounts than to delete them all and start from scratch. The
initial financial accounts in a new CiviCRM install include a variety of
revenue accounts, and other ones that your bookkeeper will recognize,
such as accounts receivable. We recommend you configure financial types
and financial accounts in consultation with your bookkeeper or
accountant.

Many accounting software options require the accounting code to match
exactly, so be careful to avoid extra spaces.

## **Payment processors**

CiviCRM provides you with the ability to take payments online on your
website. You can take payments for a variety of reasons including
fundraising campaigns, membership dues and event attendance.

To start taking payments online you need to [configure a payment processor](../contributions/payment-procesors.md) which will connect your website to the credit card and banking
infrastructure that actually processes the payment.

## **Payment Methods**

Navigate to **Administer > CiviContribute > Payment Methods** to
edit existing options that can be used for contributions or to add a new
option through **Add Payment Methods**. The common options - credit
card, cash, check, debit card, and EFT - are installed by default.

## **Accepted Credit Cards**

Navigate to **Administer > CiviContribute > Accepted Credit Cards** to
edit existing acceptable credit cards or define a new option through
**Add Accepted Credit Card**.

Note: If billing information is collected on the payment processor's website then you will need to configure accepted credit cards/payment methods on that site.
