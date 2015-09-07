Accounting Integration
======================

The accounting integration feature provides the capability to assign
financial transactions to a batch, or to use batches created from batch
data entry, then export the batch to be imported into accounting
software.

Financial Types Set-Up
----------------------

Financial Types need to be set-up before you begin using CiviCRM for
financial transactions. (In old versions of CiviCRM, financial types
were known as contribution types. Each financial type will have
financial accounts associated with it.

From **Administer > CiviContribute > Financial Types,** you can set up
the different financial accounts that are associated with each type. As
you create a Financial Type of a specific name, CiviCRM creates a
similarly named Revenue Financial Account and assigns it and the default
accounts for Accounts Receivable and a few other account types to the
new financial type. The aim behind these actions is to simplify the
common use case, but provide flexible for more sophisticated
setups. The setup of Financial Types determines how CiviCRM
transactions relate to them. It needs to be done properly in order to
ensure your export from CiviCRM will correctly transfer financial
transactions into your accounting database.

Financial Accounts Set-Up
-------------------------

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
and financial accounts in coordination with your bookkeeper or
accountant.

Many accounting software options require the accounting code to match
exactly, so be careful to avoid extra spaces.

Accounting Batches
------------------

From the Accounting Batches main page, you may search for existing
batches or create a new batch.

Batches can be created through the batch data entry tool or by grouping
existing transactions.

Create a New Batch Through Batch Data Entry 
---------------------------------------------

Select **Contributions > Batch Data Entry** or **Memberships > Batch
Data Entry**. Give the Batch a name, choose either contribution or
membership as the type and enter the number of transactions that
will appear in the batch and the total amount of all the contributions.
You can later return to edit these parameters as long as the batch
remains open. 

On the next screen you can begin entering your contribution data, if
membership was chosen as the type during batch set-up you will be able
to add membership information as well. If the contact is new, you can
add them during the batch. 

After entering your batch through the batch data entry tool, then
validate and close, it will appear in the accounting batch listing with
a status of Closed.

Create a New Batch from Existing Transactions 
-----------------------------------------------

Select "New Accounting Batch." This opens the batch creation screen.
Before you assign transactions to a batch, you will first define the
parameters.

Enter the batch name (required). CiviCRM will create a default batch
name ("Batch N" + open date), which you can edit. You may optionally
enter a description of the batch.

You may also set several Optional Constraint parameters:

If you want this batch to contain only transactions paid by a specific
Payment Instrument, select it from the drop down: Credit Card, Debit
Card, Check, Cash, or EFT, or any custom Payment Instruments you may
have set up.

If you know in advance the number of transactions that will be in the
batch, enter it in Number of Transactions. When you close the batch,
CiviCRM will verify that you have entered the correct number (you will
have the opportunity to override the warning if they do not match).

If you know in advance the total amount of the transactions that will be
in the batch, enter it in Total Amount. When you close your batch,
CiviCRM will verify the totals entered match this number (you will have
the opportunity to override the warning if they do not match).

You can later return to edit these parameters as long as the batch
remains open. 

Assign Transactions to a Batch
------------------------------

From the Accounting Batches screen, select an open batch. Click
"Transactions." This opens the transaction assignment screen.

At the top of the screen is displayed the parameters of the batch:

-   created by 
-   status (open, closed, or exported) 
-   the description entered when the batch was created

-   the specified payment instrument (if one was selected when the batch
    was created)
-   the number of entered transactions (if a number of transactions was
    specified when the batch was created)
-   the number of assigned transactions (which will update as you assign
    transactions to the batch)
-   the entered total amount of the transactions (if a total amount was
    specified when the batch was created)
-   the assigned total amount (which will update as you assign
    transactions to the batch)
-   the date the batch was opened.

Below that is a list of transactions assigned to the batch. This will be
empty until you assign transactions to the batch. There is also an
action dropdown selection that will not be available until transactions
are assigned to the batch.

### Find and Assign Transactions

At the bottom of the page is search pane to find transactions to assign
to the batch. Click "Edit Search Criteria" to open a search pane. If a
Payment Instrument was selected when the batch was created, this option
will be selected by default. Search for the contributions you want to
add to the batch.

From the search results list, you may assign a single transaction to the
batch by clicking "Assign" at the end of the result row. Or you may
select multiple transactions and use the action menu above the results
to select "Assign to Batch." The transactions will be added to the
assigned transaction list, and will be removed from the search results
list.

### View and Remove Assigned Transactions 

Once you have assigned transactions to the batch, they will appear in
the assigned transactions list in the middle of the page. If you need to
remove transactions from the batch, select "Remove" at the end of a row
of an individual transaction, or select multiple transactions and use
the action menu above the list to select "Remove from Batch."

You will also see changes to the parameters table at the top of the
page, reflecting the new number and total amount of assigned
transactions.

If you want to return and edit the batch later, simply return to the
Accounting Batch main page. The batch status will remain "Open." 

Close and Export a Completed Batch
----------------------------------

Once you have completed assigning the transactions, you may close the
batch, or close and export it.

If you attempt to close the batch and your assigned number of
transactions does not match the entered number of transactions, or if
the assigned total transaction amount does not match the entered total
amount, a "Mismatch" error message will appear. You may close the error
message and return to the batch to correct the mismatch, or you may
click "OK" to override the error; the entered transaction number and
total amount will update to match the assigned transaction number and
total amount, and the batch will be closed. 

If you close the batch without exporting it, the batch status will
change to Closed. You may re-open the batch later, before exporting it,
or you may export the transactions later. 

If you close and export the batch, you may choose your export format.
CSV will produce a spreadsheet of comma-separated values. IIF will
produce a file in Intuit Interchange Format, which is used by Intuit
products such as Quickbooks to import transactions. Once the
transactions are exported, the batch status changes to Exported. An
exported batch cannot be re-opened. 

Searching and Acting on Batches 
---------------------------------

From the Accounting Batch main page, you may filter the list of
displayed batches by status (Open, Closed, or Exported); batch name; the
user who created it; the Payment Instrument; the entered number of
transactions; and the entered total amount.

If a batch has the status Open, select "Transactions" to assign or
remove transactions, or select "Edit" to edit the batch parameters.
Under "more" you can choose to close, export, or delete the batch. 

If a batch has the status Closed, select "Transactions" to view the
assigned transactions, or select "Export" to export the assigned
transactions to a CSV or IFF export file. Under "more" you can choose to
re-open or delete the batch.

If a batch has the status Exported, select "Transactions" to view the
transactions assigned to the batch; select "Download" to export the CSV
or IIF file of assigned transactions; or select "Delete" to delete the
batch. Once a batch is exported it cannot be re-opened. 

From the search results page, you may also take action on more than one
batch. Select all the batches to be updated, and choose an option from
the action dropdown menu: Re-open, Close, Export, or Delete.

Finding Transactions by Batch
-----------------------------

From the Advanced Search Contribution pane, or from Find Contributions,
you can search by Batch Name. Select a batch and the results will return
all transactions stored in the batch. 



