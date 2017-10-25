# Mapping and Geocoding

Mapping and Geocoding - Configure a mapping provider (e.g. Google or Yahoo) to display maps for contact addresses.

You can choose to use either Google or OpenStreetMap as your mapping provider depending on your preference. Check which service has the best coverage for your contact's locations. If you've also configured a Geocoding Provide AND the provider has coverage for a contact and / or event location - CiviCRM will automatically populate / update the Latitude and Longitude fields (geocoding) when the record is added or edited.

You can view the provider options at their respective websites:

* [OpenStreetMap](http://www.openstreetmap.org/)
* [Google Maps API](https://developers.google.com/maps/)
* [http://developer.yahoo.com/maps/](http://developer.yahoo.com/maps/)

**Map Provider** - From the drop-down list, choose Google or Yahoo.

**Provider Key** - Google no longer requires an API Key. If using Yahoo, enter the Application ID.

Click **Save** to save your action or **Cancel** to cancel it.

If successful you will see the message "Your changes have been saved."

!!! note "Intranet Server and/or Firewall Issues"
    If CiviCRM is installed on a server which does not have access to the public internet OR there is a firewall which prevents CiviCRM from communicating with the Google or Yahoo web services - you will see one or more fatal errors when attempting to add or edit contact records. You will need to either disable Mapping and Geocoding - or resolve the connectivity issue to resolve this.

After enabling the mapping provider, you may need to use this script to generate latitude/longitude information for existing contact addresses:

[http://wiki.civicrm.org/confluence/display/CRMDOC/Batch+Geocoding+Script](http://wiki.civicrm.org/confluence/display/CRMDOC/Batch+Geocoding+Script)

!!! note "Usage Limits"
    Some providers have usage limits on their Mapping and Geocoding APIs. If you go over the limits you may receive a overlimit error when trying to save an address. Currently there is no support for integrating the [Google APIs Console license](https://developers.google.com/maps/documentation/javascript/usage#usage_limits) (which is needed for sites whose usage is over limit). Contact info at civicrm dot org if you are interested in helping implement this.