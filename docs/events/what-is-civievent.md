Qu'est-ce que CiviEvent?
=======================

CiviEvent fournit un ensemble d'outils pour gérer des événements. Ces outils vous permettent d'être plus efficace en tant qu'organisateur de l'évènement et réduisent le nombre de taches à réaliser 

CiviCRM vous aide à gérer un enregistrement simple ou complexe.
Principales fonctionnalités incluses :

-   Auto inscription des participants, avec possibilité de règlement en ligne par carte de crédit.
-   Suivi des inscriptions, annulations. Affichage de vos évènements sur votre site web.
-   Copie des fonctionnalités et paramétrage d'un évènement pour d'autres similaires ou périodiques
-   Enregistrement des participants de n'importe quel ordinateur avec une connexion à Internet

Scenario: Youth leadership workshop
-----------------------------------

A community arts group, Arts in Action, conducts leadership workshops
for people under age 25 throughout the year. Their goals include
attracting new youth to attend their workshops and enlisting past
attendees to volunteer and teach. Youth from local schools and theater
groups are invited to attend, and there are youth speakers and
volunteers, as well as other speakers for the training workshops.

The Arts in Action communications staff use CiviEvent to efficiently
manage each workshop from the beginning of its planning to the end of
its evaluation. First, a staff member creates an event page that
includes an online registration form. Because this is a regular event, a
staff member has previously created an event template, which fills in
much of the information needed in the event set-up process. There is a
flat fee for registration, with additional fees for optional workshops;
attendees can select what they are registering for and pay for it
online. The registration form also gathers information about
participants' food and lodging preferences using a CiviCRM feature
called a profile.

A targeted list of youth and groups is drawn from existing contacts, and
staff send personalised invitations using CiviMail (also based on a
template, so that information can be reused from one event to the next).
The invitation includes a direct link to the event page so that
participants can arrive at the online registration with a single
click. The event is also announced publicly by posting it on the Arts in
Action website, and the "Tell-a-friend" function is enabled so that the
information can easily be spread through people's networks.

A staff person is designated to manage the process by which participants
register themselves, periodically checking to make sure that payments
are being made, managing the wait list when participant sign-ups exceed
the maximum number, and answering any questions.

On the day of the event, organisers can check in each attendee on-site
to keep track in real time of who is attending and whether there are any
no-shows. Participants with outstanding fees can also be asked to pay at
this time. The database is updated immediately, freeing up spaces for
those on the wait list and recording payments.

After each workshop, Arts in Action staff evaluate the success of the
event and use CiviEvent to quickly generate reports such as the number
of attendees, total event fees paid, and total amount still due. The
event and mail templates can be updated if necessary and saved for the
next event.

Quelques concepts clés 
-------------------
Les chapitres de cette section vous aiderons à tirer le meilleur de ce que vous devez savoir pour optimiser CiviEvent
Avant de commencer, voici quelques points clés qui vous aiderons à configurer votre évènement.
Vous allez mettre ces concepts en pratique en suivant les tâches, étape par étape, dans les chapitres suivants de cet article

### Evenements, participants et contacts

Préalable : CiviCRM permet de créér un ou plusieurs **evenements** auxquels vos **contacts** peuvent participer. 
quand un contact participe à un évènement il est appelé **participant**. 

### Event types

CiviCRM permet de définir différents tyes d'évènements tels que conférences, réunions, présentations, formations,sponsors,...
Vous pouvez créer autant de types d'évènements, en fonction des besoins de votre organisation.

Par exemple, vous pouvez créer des champs personnalisés pour stocker et afficher des données supplémentaires sur un événement en fonction de son type d'événement. Les différents types d'événements sont utiles si vous avez des exigences différentes pour vos événements.
Voir le chapitre * Custom data on events * dans cette section pour plus d'information
Les types d'évènements sont également utiles pour catégoriser et segmenter les événements et les participants, par exemple, vous pouvez facilement trouver tous les contacts qui sont venus à l'une de vos formations ou assisté à l'un de vos événements de collecte de fonds.
 



### Participant roles

Every contact that participates in an event is assigned a participant
role. The most common is probably attendee. Others include volunteer or
speaker.  Participant roles are fully customizable to match the types of
events your organization conducts. This allows you to segment
participants into meaningful categories based on their involvement in
the event, for example for sending an email to volunteers only or
generating a list of past table captains for fundraisers. You can also
create custom fields that apply only to specific roles, for example, to
collect information about availability from volunteers only.

### Participant statuses

Participant statuses (for example, registered, wait-listed, attended or
cancelled) are used to track what stage the contact is at in their
'event journey'. Participant statuses are fully customizable to match
the way your organization does event registration. This allows you to
segment participants into meaningful categories based on their behavior
with respect to the event,for the purpose of things like generating
sign-in sheets, tracking how many people are likely to come to an event,
and tailoring email communications to registrants.

Other parts of CiviCRM that work with CiviEvent 
-------------------------------------------------

CiviEvent is designed to work together with other parts of CiviCRM.  For
example, you can promote the event to a targeted list and communicate
with event participants via email before and after the event using
CiviMail (see the *Email* section, particularly the *Set-up* and
*Scheduled Reminders* chapters, for more information). CiviEvent works
with CiviContribute to allow you to accept event payments online. To do
this, you must enable CiviContribute and set up a payment processor; see
the *Contributions* section for more information.



