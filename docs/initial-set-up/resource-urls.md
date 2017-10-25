# Resource URLs

**Administer >> System Settings >> Resource URLs** (/civicrm/admin/setting/url?reset=1)

Default values for the settings on this screen are supplied during the automated installation process. In general, you should only need to review and/or modify these settings if you've moved your CiviCRM installation to a different server or directory path OR if you've changed the base URL used to access your site.

**The CiviCRM Resource URL must be an absolute (complete) URL.** For example, in a typical Drupal installation:

```
http://yourorg.civicrm.org/sites/all/modules/civicrm/
```

Click Save to save your action or Cancel to cancel it.

If successful you will see the message "Your settings changes have been saved."

!!! tip "Adding CSS styles for all CiviCRM pages"

    You can also define additional CSS styles to be applied to all or specific page elements by adding CSS styles to the 'extra CSS' file: _css/extras.css_. This file is included in the downloaded code, but is empty by default.


## Trouble-shooting

The following symptoms are all indications that your **CiviCRM Resource URL** setting is incorrect:

* Icons such as the those on the **Administer CiviCRM** screen are missing
* Advanced search is missing the expandable panes for searching on Address Fields, Relationships, etc.
* Fields for selecting Country and State/Province don't work

If you notice these symptoms, use the **View Source** option in your browser and examine the HTML source of any CiviCRM screen. You will see a line like this near the beginning:

```
<style type="text/css">@import url(http://yoursite/sites/all/modules/civicrm/css/civicrm.css);</style>
```

Copy the URL portion of this line ( the portion in parentheses - starting with http:// ) into your browser's location bar and try to navigate to civicrm.css. If you see a css file code in your brower - then your Resource URL setting is correct. If you get **Page Not Found** - then you'll need to examine the URL and modify as needed.

## Base URL Detection problems

Sometimes the CiviCRM Resource URL setting is correct but there are problems with how CiviCRM is determining your base url that then affect the resource URL generation. See the troubleshooting section on [Cleanup Caches and Update Paths](https://wiki.civicrm.org/confluence/display/CRMDOC/Cleanup+Caches+and+Update+Paths).