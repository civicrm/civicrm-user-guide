# Dates

## Date Formatting

Use **Administer > Localization > Date Formats** to configure formats for date display and date input fields.
Defaults are provided for standard United States formats. Settings use standard POSIX specifiers.

Date Display - Type in the values you want for:
**Complete Date and Time**, **Complete Date**, **Month and Year** and **Year Only**.

Date Input Fields - Type in the values you want for: **Date Input Format**, **Time Input Format**.

## Date Preferences

By default, CiviCRM provides ranges for input on specific date fields. For instance, the default range for Activity Dates are 20 years prior to the current year all the way through to 10 years beyond the current year. If you would like to track activities that have occurred, say, 25 years ago then you would need to update this range to enable your end users to log these activities. To update these settings to the appropriate range go to **Administer > Customize Data and Screens > Date Preferences**. If you were to leave these settings as the default you will see an error such as this: Please enter a date between 01/01/1994 and 21/31/2024.

![Advanced Date Input Settings](../img/configure-localization-advanced-date-input-settings.png)
