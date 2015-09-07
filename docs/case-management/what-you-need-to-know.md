What You Need To Know
=====================

The CiviCase component allows for a high degree of customisation to meet
the needs of a wide variety of organisations and workflows. It is
important to understand CiviCase's underlying principles and
assumptions, as well as the elements that can be customised, before you
begin to plan and configure the component based on your requirements.

Key Concepts
------------

**Activities**: CiviCRM tracks most interactions with activities. These
are particularly useful for single interactions. For example, if a
constituent calls to request information and the staff person directs
them to a web site, this would be recorded as an activity. Activities
have a start date/time, a duration, a status, a priority. They have a
creator and a subject/target and can be assigned to someone for action.


**Cases** are used to track more complex interactions or communication
processes than can be handled by a single activity. CiviCase provides
additional structure around activities:

-   Multiple activities can be grouped together into a case
-   Activities can be optionally structured using a Timeline or a
    Sequence
-   The set of possible activities to track interactions can be
    optionally restricted

CiviCase also identifies the people involved and their role(s) in the
case:

-   Case Coordinator is a pre-defined role
-   Additional roles can be added as required

CiviCase also provides additional options for managing activities:

-   The Case Dashboard allows users to see the cases they are involved
    in
-   Cases provide an extra layer of access control

Using these features, a case can define a workflow with specific steps
that must be followed,. For example: a client fills out an intake form,
then has an initial meeting with a staff person, and finally receives a
certificate from the organisation for meeting certain goals.

### Case Types

One or more Case Types are defined that describe a specific group of
related tasks, interactions, or processes.

For example, the Physician Health Program provides support for
physicians who are experiencing problems related to emotional health
issues, the inappropriate use of alcohol and/or drugs or coping with
physical illness. Some of the case types they use are:

-   In-patient Treatment
-   Referral to Counsellor

For a community services organisation, examples of case types might
include:

-   Housing Assistance
-   Job Training
-   Prenatal Counseling

Think about the multi-step tasks that staff in your organisation do on a
regular basis and make a list of potential case types.

### Case Activities

Activities track specific interactions and tasks within a case.
Activities may be scheduled in advance or created ad-hoc, and they may
involve the case client (a.k.a. the constituent), a third party (such as
a family member or a professional who is assisting with the case), and
other case workers. Each organisation needs to determine the level of
detail to be recorded, but many organisations find it helpful to include
every phone call, meeting or internal discussion in the case story by
recording it as an activity.

### Activity Types

CiviCRM is preconfigured with a number of activity types including Phone
Calls, Meetings, Emails Sent, Interviews and Follow-ups. These may be
sufficient for your needs. However many organisations will want to track
other specific tasks, and activity types can be added for these.

During the life of each case, some activities will be automatically
created, such as:

-   Open Case: created at the same time the case is created.
-   Follow up: you can use this type when it isn't necessary to define a
    more specific one (see Activity Data below).
-   Change Case Type: created every time the type is modified.
-   Change Case Status: created every time the status is updated.

For a community services organisation, additional activity types might
include:

-   Client Intake
-   Skills Evaluation
-   Review
-   Consultant Referral

For each of the case types you identified, create a list of the specific
activities involved. Creating new activity types instead of relying only
on Follow-up will make the list of activities easier to read.

### Activity Data

A standard set of information can be entered whenever an activity is
recorded in CiviCase:

-   who recorded the activity and who reported the activity
-   when and where the activity will (or did) occur
-   free-form subject and detailed description
-   time spent on the activity.

This is sufficient for some types of activities; however, it is often
useful to collect additional structured data. The Open Case (intake)
activity is a common example where you may want to include a set of
specific questions about the client and their situation.

Create a list of additional requirements (custom data) for each activity
type, including the type of data being recorded (free text, multiple
choice, date, etc.) in order to set up the required custom fields.*For
more information about custom data fields refer to the Custom Fields
chapter in the Organising Your Data section*.

### Timelines and the standard timeline

CiviCase allows you to define one or more expected sets of activities
for each type of case and when they should occur. These are called
**timelines**.

For really simple cases, the timeline might include only two items:

-   Open Case
-   Follow up - scheduled for two days after the case is opened

Even in this example, the timeline is useful as it allows you to
predefine when the people assigned to the case should follow up with the
client or constituent. For more complex processes, the timeline provides
a case plan that can help the people involved to stay on track. The
timeline lists all the activities which are expected to occur and should
be accomplished within a certain time-frame. When a timeline is added to
a case the activity dates are pre-computed and do not update
automatically. Any changes to dates must be made manually.

Each case type must have a **standard timeline.** The **standard
timeline** is created automatically when a new case is opened. At its
simplest it consists of just one completed "Open Case" activity. You can
leave it at that or add more activities as required. In a standard
timeline you define the expected number of days between the beginning of
the case and each of the subsequent activities in the timeline. 

You can create mulitple (non-standard) timelines for a case and add them
if/when it is appropriate to do so. For these timelines you can use any
activity as the reference for subsequent activities. So, for example, if
one of the activities in your standard timeline is a medical evaluation,
you could have 2 or more timelines that outline different schedules of
medical treatment and add one of these to the case depending on the
outcome of the original medical evaluation. For this example the
timelines would typically use "medical evaluation" as the reference
activity.

You might also want to define a (non-standard) timeline based on the end
date for a case. When a case has to be completed by a specific date
(e.g. by the start of the school year), each activity can be defined as
needing to happen a number of days before this end date, i.e. you would
define negative offsets in the timeline. You would open the case, add
the final activity with the scheduled end date, then add the timeline.
This would create a series of activities with the scheduled date for
each being the latest it could be completed if the entire case is to be
completed by the end date.

### Sequences

CiviCase lets you define one sequence instead of, or as well as,
timeline(s). A sequence is a set of activities that should follow one
after the other, but no time-offsets are defined for the activities.
Instead the activities are created one at a time, with the first
activity in the sequence created when the case is opened, and the second
activity in the sequence being created as soon as the first activity is
completed and so on. The scheduled date is always the date the activity
is created.

Defining a sequence rather than a timeline may be useful if the
completion of activities in your case are outside your control. However,
as the activities are created progressively it will not provide the same
at-a-glance overview of the case that a timeline does. 
 
**NOTE:** If you want to use both a timeline and a sequence in the same
case you must make sure that there is no overlap in activity types
between the two. For example, you cannot include the activity type of
"Meeting" in both a timeline and the sequence within the same case as
this will create problems. 

Case Roles and Relationships 
------------------------------

CiviCase provides three mechanisms for relating people to cases and
clients:

-   **Case Roles:** people directly involved in this case. Examples
    include Intake Specialist, Case Coordinator, Addiction Counselor,
    Employment Counselor, etc. You can identify one of these roles as
    the case manager for a particular case type.
-   **Other Relationships:** people related to the client, with
    relationships that exist beyond the context of a particular case.
    Examples include Spouse, Sibling, Family Doctor, etc. Generally,
    use relationships when you want someone to appear on ALL cases for
    the same client, otherwise use a case role.
-   **Case Resources:** people and organisations that have involvement
    with many or all cases in your case management setting. Examples
    include: regulatory agency contact(s), service provider, frequent
    referral contacts, etc.

CiviCRM provides relationship type definitions for most of the standard
relationships you might track (e.g. Spouse, Child). However you will
probably need to define additional relationship types for your case
roles, such as:

-   Case Coordinator
-   Addiction Specialist
-   Job Counsellor

Make a list of the expected case roles for each type of case you've
listed, then determine which role will normally be considered the case
manager for that case type.

**Key Questions**

Think about these questions with regard to your organisation's use of
CiviCase:

-   What case types do you have? The first step in planning your
    CiviCase configuration is to think about the types of cases your
    organisation needs to manage. Complex processes which include
    several activities, span several days or weeks, and involve multiple
    people are potentially good candidates for case management. Start by
    listing these processes and defining a case type for each one.
-   What activity types do you need to have in those cases?
-   Who should activities be assigned to? By default everything might be
    assigned to a case coordinator who will then reassign to whoever has
    capacity, or certain activities might require the intervention of a
    particular individual.
-   Do you have a default timeline and what does it look like?
-   Do activities need to be offset from the start, each other or from
    the end?
-   What roles are involved? Are existing relationships adequate, or do
    you need to create some case specific ones?

**Assumptions**

Although CiviCase is quite flexible, there are a number
of case-management assumptions built-in to the component. These
assumptions have been arrived at through an extensive trial and error
process and although some of them may seem new or foreign at first, we
encourage you to approach them with an open mind.

-   Activities are single tasks or interactions between your
    organisation and a client or constituent, or between people within
    your organisation.
-   Cases involve a succession of interactions (activities). The record
    of these activities forms the case story and almost all information
    about a case should be stored as an activity.
-   Classifying cases by case type allows you to define work-flows and
    evaluate results.
-   Cases often have a predictable succession of activities (a standard
    timeline). Creating a schedule with the expected timeline helps
    people working on the case to manage their work, and is a useful way
    to measure progress.
-   Cases often involve a predictable set of people involved (staff,
    professionals, etc.). These are case roles. Knowing who is playing
    what role in a case is helpful, and provides an easy way to
    communicate case activities to other people who are also working on
    that case.
-   Organisations may have additional people and/or outside
    organisations (case resources) who are frequently contacted or
    involved with most or all cases.

