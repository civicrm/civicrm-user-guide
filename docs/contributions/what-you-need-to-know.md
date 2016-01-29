What You Need To Know
=====================

This chapter provides information that you need to think about before
configuring and using CiviContribute. CiviContribute allows you to:

-   accept donations and other financial contributions
-   process membership signups and renewals
-   run specific fundraising campaigns
-   batch enter contribution and membership payments using "batches"
-   report and evaluate fundraising results and trends

Throughout CiviCRM, the term *contribution* refers to any financial
transaction or payment taking place in the system such as a donation,
event fee payment or membership fee payment.

It is helpful to list out the types of contributions your organisation
receives (or wants to receive), and identify which of those you want to
track using CiviCRM. Then consider the following concepts and answer the
key questions listed below before you begin to work with CiviContribute.

Key Concepts
-------------

### Data needs and fields

CiviContribute has a set of predefined fields to track contribution
information. If you need to track more information about contributions,
you can do this by defining new custom data fields. Custom data might be
useful to further categorize your contributions or track additional
information.

Write down all the information you want to track about your
contributions, including reports (described later in this chapter), then
compare your data needs to CiviCRM's predefined fields. An easy way to
do this is is to look at the screen for adding a new contribution. A lot
of useful functionality is built in to the core contribution fields so
there's no point in duplicating them with custom fields, but your
organisation may have specific needs that require custom fields.

If you do need to create custom fields to meet your needs, see the
chapter *Creating Custom Fields* in the *Understanding Your Data section*.

### Types and accounting codes

CiviContribute categorises contributions by Financial Type. Examples
of Financial Types include event fees, membership fees, donations and
grants.

To aid integration with your accounting software, you can assign an
Accounting Code to each Financial Type. This code is included when you
export contributions for import into your accounting package.

### Financial Accounts and Financial Types

New to the CiviContribute module in 4.3 is CiviAccounts which allows
wider integration with accepted accounting principles and workflows
typical to most organizations.

"Contribution Type Accounts" are now called "Financial Type Accounts".
New to this administration page is a column named "Accounts" (see screen
capture) which reflects the new Financial Account object associated with
each type. Now, an organization may better manage and report in relation
to both the income and expenses on a Financial Type.

For example, a fund raising dinner that charges $100/person may now
allocate the true costs toward the relevant accounts i.e. $75 donation
posted to the Income account named "Donations" and the $25 Cost of
Sales account to "Event Fees".

As with the types, the list of associated preconfigured accounts will
suit the needs of most organizations and may also be customized if your
organization requires changes or additions.

You will want to check the list of Accounting Codes that are assigned to
each account to ensure that they correspond with those used in your
organization's chart of accounts.

Set-up
======

This chapter shows you how to set up CiviContribute and related
components of CiviCRM to support fundraising.

This chapter assumes you have a working understanding of custom
fields, contact matching rules, CiviCRM Profiles, and the
CiviMember and CiviMail components. The chapter also assumes you have
already set up your payment processor and created any custom fields
you want to use when tracking contributions. If you have not done these
things, please refer to the appropriate sections of this manual for more
information.

General Configurations
----------------------

You may need to configure the following fields before you begin setting
up various methods for recording and managing contributions.

### **Financial Types and Accounting Codes**

If you need to add Financial Types or accounting codes, do this first.

1.  Navigate to **Administer > CiviContribute > Financial Types**,
    where you can edit one of the existing Financial Types or create a
    new one by clicking **Add Financial Type**.
2.  Once you edit or add a Financial Type, you can define an accounting
    code that corresponds to your accounting system (the accounting code
    will be exported along with the contribution data if you do an
    export), and indicate whether this type of contribution is
    tax-deductible.

Be careful when editing core Financial Types or adding new types,
because CiviCRM has useful built-in functionality that depends on the
core Financial Types.


### **Accepted Credit Cards**

Navigate to **Administer > CiviContribute > Accepted Credit Cards** to
edit existing acceptable credit cards or define a new option through
**Add Accept Creditcard**.

### **Payment Instruments**

Navigate to **Administer > CiviContribute > Payment Instruments** to
edit existing options that can be used for contributions or to add a new
option through Add Payment Instruments. The common options - credit
card, cash, check, debit card, and EFT - are installed by default.
