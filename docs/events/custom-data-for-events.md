Custom data for events
======================

You many want to collect extra information about events and their
participants as part of the event management process. This chapter
explains how you can easily do this with custom data. It describes the
different ways to collect custom data for events and discusses where
best to store each type of information. A general understanding of how
custom data works in CiviCRM is needed to get the most out of this
chapter. The chapter on *Custom fields* in *Organising Your Data* should
give you that understanding.

The key question to ask when adding custom data for event management is
*where* should this custom data go? There are three places that you
typically want to add custom data

-   the participant record
-   the contact record
-   the event record. 

It's important to add custom data in the it in the right place. Adding
it in the wrong place might cause you headaches further down the line.
People often add custom data to the participant record, when they should
probably add it to the contact record, and visa versa. A couple of
examples might help to clarify.

-   dietary preference should be added to contacts since this is
    unlikely to change between events.
-   Session preference should be added to the participant record since
    it is only of interest in the context of the event.

Custom fields can also be added to events. For example, lets say an
organisation holds a series of training workshops throughout the year
and wants to create a custom field to track six common topics covered in
workshops. You could create a checkbox style field with the list of
topic options and add it as custom data for events of the type
workshop. Then, when creating an event of type Workshop, this field
will be available.

Note that you are not required to select a specific event type. Leaving
the dropdown set to Any indicates the field is available to all events,
regardless of the type.

Another common mistake that people make is adding custom data to the
event record, when they should add it to the participant record. The
event record should only be used to collect information about the event
itself, not its participants.

There are a few different options when adding custom data to
participants. 

-   **Participants:**This will add the field to all participant records.
Useful if you are interested in collecting information that applies to
all participants.

-   **Participants (Event Name):**This is identical to the Participants
type, with the exception that it allows you to assign a group of custom
fields to a specific event. Useful for adding complex registration data
for a single event without cluttering up all events. 

-   **Participants (Role):** These fields will only be available for
particular types of participants. Useful, for example, if you need to
collect biographical profile details from your speakers and wish to
record it with their event registration. 


Adding custom data requires the administrator permission. To add custom
data from participants, add new custom fields through **Administer >
Customize Data and Screens > Custom Data**. To create custom fields for
events, first add the **custom field set** on the appropriate record, and
then add the fields themselves.

Alternatively, you can create custom fields on the fly during the event
creation process - see chapter *Creating an event*. 

