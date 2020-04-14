# Mapping and Geocoding

Configure a mapping provider (e.g. OpenStreetMap or Google) to display maps for contact addresses by visiting **Administer > System Settings > Mapping and Geocoding**.

You can choose to use either Google or OpenStreetMap as your mapping provider depending on your preference. Check which service has the best coverage for the locations you expect your contacts to enter. If you've also configured a Geocoding provider and they have coverage for a contact and/or event location - CiviCRM will automatically populate/update the Latitude and Longitude fields (Geocoding) when the record is added or edited.

You can view the provider options at their respective websites:

* [Google Maps API](https://cloud.google.com/maps-platform/)

**Mapping Provider**  
Select the service (OpenStreetMaps or Google) used to build and display the maps shown in the CiviCRM UI.

**Geocoding Provider**  
Select the service (Google) used to translate addresses into a latitude and longditude.

**Geo Provider Key**  
Enter the API key as required by your GeoCoding provider.

Click **Save** to save your action or **Cancel** to cancel it.

If successful you will see the message "Your changes have been saved."

!!! note "Internal Server and/or Firewall Issues"
    If CiviCRM is installed on a server which does not have access to the public internet or there is a firewall which prevents CiviCRM from communicating with your chosen web services - you will see one or more fatal errors when attempting to add or edit contact records. You will need to either disable Mapping and Geocoding - or resolve the connectivity issue to resolve this.

After enabling the mapping provider, you should configure the [job.geocode](scheduled-jobs.md#job_geocode) scheduled job which will geocode addresses without a latitude and longditude according to the configured options.

!!! note "Usage Limits"
    Some providers have usage limits on their Mapping and Geocoding APIs. If you go over the limits you may receive a overlimit error when trying to save an address.
