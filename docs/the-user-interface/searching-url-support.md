# URL filter support in searches

In some cases it is possible to bookmark search urls with parameters in them in order to quickly re-access searches.

The parameters that are accepted by CiviCRM has been changing across versions. However, we have been standardising our approach and the parameters documented here have been added in a 
standardised manner and can be expected to work going forwards. Testing is done on 5.20 & 5.21 but some are available in earlier versions.

To construct a parameterised url you need to 
1) ensure the url contains 'reset=1&force=1' (after the question mark)
2) add additional supported parameters.

So, for example, in 5.20 the following url works on drupal to find contributions made by a person with a name like 'Bob', a contribution source like dad made on or before 01 Jan 2018
`civicrm/contribute/search?reset=1&reset=1&force=1&sort_name=bob&receive_date_high=20180101&contribution_source=dad`

The following parameters work in a supported way on contribution search:

|Field|Example|Comments|Min version (where known)|
|-----|-------|-------|-------|
|sort_name|sort_name=bob|Sort name is like 'bob%' or '%bob% depending on your site config*|
|contribution_source|contribution_source=dad|Contribution source like '%dad%' or 'dad%'|
|cancel_reason|cancel_reason=dunno|Contribution source like '%dunno%' or 'dunno%'
|invoice_number|invoice_number_reason=xyz|Invoice Number like '%xyz%' or 'xyz%'
|contribution_page_id|contribution_page_id=1||5.21 PR https://github.com/civicrm/civicrm-core/pull/15785|
|receive_date_high|receive_date_high=20180101132323|Contribution received on or before 01 Jan 2018, 1.23 pm|
|receive_date_low|receive_date_low=20161001|Contribution received on or after 01 Oct 2016|
|receive_date_relative|receive_date_relative=this.year|Contribution received this year|
|contribution_cancel_date_high|contribution_cancel_date_high=20180101132323|Contribution cancelled on or before 01 Jan 2018, 1.23 pm|
|contribution_cancel_date_low|contribution_cancel_date_low=20161001|Contribution cancelled on or after 01 Oct 2016|
|contribution_cancel_date_relative|contribution_cancel_date_relative=this.year|Contribution cancelled this year|
|event_high|event_high=201901010000|Event end date on or before 1 January 2019|5.12 [PR](https://github.com/civicrm/civicrm-core/pull/15791)|
|event_low|event_low=201901010000|Event Start date on or after 1 January 2019|5.12 [PR](https://github.com/civicrm/civicrm-core/pull/15791)|
|event_relative|event_relative=this.year|Event Start Date on or after ths start of this year and the event end date on or before the end of the year|5.12 [PR](https://github.com/civicrm/civicrm-core/pull/15791)|
|participant_registration_date_high|participant_registration_date_high=201901010000|Participant Registration Date on or before 1 January 2019|5.12 [PR](https://github.com/civicrm/civicrm-core/pull/15791)|
|participant_registration_date_low|participant_registration_date_low=201901010000|Participant Registration date on or after 1 January 2019|5.12 [PR](https://github.com/civicrm/civicrm-core/pull/15791)|
|participant_registration_date_relative|participant_registration__date_relative=this.year|Participant Registration Date on or after ths start of this year and the event end date on or before the end of the year|5.12 [PR](https://github.com/civicrm/civicrm-core/pull/15791)|
|participant_status_id|participant_status_id=1,2|Participant Status in Registered and Pending Pay Later|5.12 [PR](https://github.com/civicrm/civicrm-core/pull/15791)|
|participant_role_id|participant_role_id=1,2|Participant Role IN (Attendee, Host)|5.12 [PR](https://github.com/civicrm/civicrm-core/pull/15791)|


* Whether text fields search for LIKE '%dad%' or LIKE 'dad%' depends on the site wide setting
'Automatic Wildcard' under Administer CiviCRM->Customize data and screens -> search preferences
For large sites turning this off gives a significant performance improvement but it means
that searching for 'dad' will return 'daddy' but not 'grandad'.

## Date Formats

In general there are 2 types of date formats to use
1) _high or _low fields take an 8 or 14 digit number representing Year,month, day and optionally
hour, minute and second - eg. 20180921235959 means 21 Septembers 2018 at 23 hours, 59 minutes and 59 seconds.
You could leave off 235959 and it would mean at zero o'clock - ie midnight

2) Relative date fields.  The available options are somewhat configurable by site but
most sites should have the following

| value | Means |
| ---- | ---- |
| current.month | Current calendar month to-date |
| current.year | Current calendar year to-date |
| current.quarter | Current quarter to-date |
| current.week | Current week to-date |
| previous\_before.day | Day prior to yesterday |
| greater\_previous.month | From end of previous calendar month |
| greater\_previous.year | From end of previous calendar year |
| greater\_previous.quarter | From end of previous quarter |
| greater\_previous.week | From end of previous week |
| greater.month | From start of current calendar month |
| greater.year | From start of current calendar year |
| greater.day | From start of current day |
| greater.quarter | From start of current quarter |
| greater.week | From start of current week |
| ending.year | Last 12 months including today |
| ending\_2.year | Last 2 years including today |
| ending\_3.year | Last 3 years including today |
| ending\_30.day | Last 30 days including today |
| ending\_60.day | Last 60 days including today |
| ending.week | Last 7 days including today |
| ending\_90.day | Last 90 days including today |
| previous\_before.month | Month prior to previous calendar month |
| starting.year | Next 12 months including today |
| starting.month | Next 30 days including today |
| starting\_2.month | Next 60 days including today |
| starting.week | Next 7 days including today |
| starting.quarter | Next 90 days including today |
| next.month | Next calendar month |
| next.year | Next calendar year |
| next.fiscal\_year | Next fiscal year |
| next.quarter | Next quarter |
| next.week | Next week |
| previous\_2.month | Previous 2 calendar months |
| previous\_2.year | Previous 2 calendar years |
| previous\_2.day | Previous 2 days |
| previous\_2.quarter | Previous 2 quarters |
| previous\_2.week | Previous 2 weeks |
| previous.month | Previous calendar month |
| previous.year | Previous calendar year |
| previous.fiscal\_year | Previous fiscal year |
| previous.quarter | Previous quarter |
| previous.week | Previous week |
| previous\_before.quarter | Quarter prior to previous quarter |
| this.month | This calendar month |
| this.year | This calendar year |
| this.fiscal\_year | This fiscal year |
| this.quarter | This quarter |
| this.week | This week |
| less.month | To end of current calendar month |
| less.year | To end of current calendar year |
| less.quarter | To end of current quarter |
| less.week | To end of current week |
| earlier.month | To end of previous calendar month |
| earlier.year | To end of previous calendar year |
| earlier.quarter | To end of previous quarter |
| earlier.week | To end of previous week |
| earlier.day | To end of yesterday |
| this.day | Today |
| starting.day | Tomorrow |
| previous\_before.week | Week prior to previous week |
| previous\_before.year | Year prior to previous calendar year |
| previous.day | Yesterday |
