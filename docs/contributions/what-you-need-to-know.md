What You Need To Know
=====================

This chapter provides information that you need to think about before
configuring and using CiviContribute. CiviContribute allows you to:

-   accept donations and other financial contributions
-   process membership signups and renewals
-   run specific fundraising campaigns
-   batch enter contribution and membership payments using "batches"
-   export batches of financial transactions to import to your accounting software
-   report and evaluate fundraising results and trends

Throughout CiviCRM, the term *contribution* refers to any financial
transaction or payment taking place in the system such as a donation,
event fee payment or membership fee payment and includes in-kind contributions.

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

### Financial types, financial accounts and accounting codes

Financial types are used to categorize contributions for reporting and accounting purposes. The standard financial types included with CiviCRM are event fee, member dues, donation and
campaign contribution but you can set up as many financial types as you need.

Each financial type relates to a number of financial accounts that can track income, accounts receivable, fees, cost of sales and liabilities as required. As with financial types, the list of associated preconfigured financial accounts will
suit the needs of many organizations but may also be customized if your
organization requires changes or additions.

To aid integration with your accounting software, you can assign an
accounting code to each financial account. This code is included when you
export contributions for import into your accounting package.

[Setting up financial accounts and financial types](../../contributions/accounting-integration.md) is best done in consultation with your organization's bookkeeper or accountant.

Be careful when editing core Financial Types or adding new types,
because CiviCRM has useful built-in functionality that depends on the
core Financial Types.
