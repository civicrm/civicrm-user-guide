Creating Contribution Pages
-----------------------------

To create a new contribution page:

1.  Navigate to **Contributions > Manage Contribution Pages**and
    click on **Add Contribution Page**.
2.  Give the page title, select the Financial Type (donation, campaign
    contribution, etc.), goal amount, introductory message, whether to
    accept Honoree soft crediting, and any other relevant information
    such as dates. You will be able to go back and modify all aspects of
    this page at any time after completing the setup wizard. Click
    **Continue**.
3.  The **Execute real-time monetary transactions** box is checked by
    default, to enable monetary donations. You would only uncheck this
    box if you are using this contribution page to solicit in-kind
    (non-monetary) donations.
4.  Select the **Currency**
5.  Select one or more **Payment Processors** for this page (which
    you have previously configured). Some organizations find it
    advantageous to give their constituents a choice of processors. You
    can do this by setting up multiple processors, and checking the
    corresponding boxes on this form.
6.  Check the **Pay Later** box if you want to give users the option to
    submit payment offline (e.g. mail in a check, call in a credit card,
    etc.).
7.  Check the **Contribution Amounts Section Enabled** box to allow
    various specific amounts to be presented. Leave this unchecked if,
    for example, you are using the page for membership sign-ups that
    have fixed amounts, which will show only the fixed membership
    amounts and not allow custom amounts to be entered.
8.  Select a pre-defined **Price Set**(for more complex payment
    options), OR enter up to 10 fixed contribution amounts in the table.
9.  Check the **Pledges** box to give users the opportunity to pledge
    future payments. To learn more about configuring pledges, refer to
    the Pledges chapter.
10. Check **Allow other amounts** to give users the option to pay any
    amount they choose.
11. Click **Save and Done**.



###Include Profiles

If you want to collect information from contributors beyond what is
required to make a contribution only, such as volunteer age and skills,
you can include existing CiviCRM Profiles at the beginning or end of a
contribution page. You can also create new profiles.

Profiles used in a contribution page can ONLY contain fields which
belong to:

-   contact records
-   contribution records

Profiles which include fields associated with any other record types
will not be available for this purpose.

Contribution pages will always include a required email address field,
regardless of whether you include any other fields in your profile(s).

1.  Navigate to Manage Contribution Pages then for the page you wish to
    configure, click on **Configure > Include Profiles**.
2.  Select a CiviCRM profile from the dropdown menu to be included at
    the top of the contribution page and/or at the bottom of the page.
    You can then preview your selection(s), edit an existing profile,
    copy an existing profile or create a new profile.
    When you edit or create a new profile you will use the profile drag
    and drop interface pictured here.

    ![](../_edit/static/Contribution-page---edit-profile2.gif)

    WARNING: If you modify an existing profile whilst configuring your
    Contribution page, the changes you make will apply everywhere that
    profile is being used. So unless an existing profile **exactly**
    matches your requirements you should copy the profile, then rename
    and edit the copy as required.
3.  Click **Save** or **Save and Done** or **Save and Next**.

Read more about profiles in the *Profiles* chapter of *Organizing your
Data*.

Automatic Contribution Recording
--------------------------------

Regardless of how donors get to your contribution page, CiviCRM
automatically records their donations, freeing your staff from doing
manual data entry. If the donors already exist in the database, CiviCRM
adds the contribution to their existing record. If they don't exist,
CiviCRM creates a new record for them.

In situations where people have multiple email addresses, or where more
than one person shares an email address, it can be possible for
contributions to be credited to the wrong contact. To mitigate the
chance of this happening, you can adjust CiviCRM's default duplicate
matching rules. For instructions on how to do this, *see the chapter
Merging and Deduping in the Basic Concepts section of this book*.
