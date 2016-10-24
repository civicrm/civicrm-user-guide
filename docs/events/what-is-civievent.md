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
Vous allez mettre ces concepts en pratique en suivant les tâches, étape par étape, dans les chapitres suivants de cet article.

### Evenements, participants et contacts

Préalable : CiviCRM permet de créér un ou plusieurs **evenements** auxquels vos **contacts** peuvent participer. 
quand un contact participe à un évènement il est appelé **participant**. 

### Event types

CiviCRM permet de définir différents tyes d'évènements tels que conférences, réunions, présentations, formations,sponsors,...
Vous pouvez créer autant de types d'évènements, en fonction des besoins de votre organisation.

Par exemple, vous pouvez créer des champs personnalisés pour stocker et afficher des données supplémentaires sur un événement en fonction de son type d'événement. Les différents types d'événements sont utiles si vous avez des exigences différentes pour vos événements.
Voir le chapitre * Custom data on events * dans cette section pour plus d'information
Les types d'évènements sont également utiles pour catégoriser et segmenter les événements et les participants, par exemple, vous pouvez facilement trouver tous les contacts qui sont venus à l'une de vos formations ou assisté à l'un de vos événements de collecte de fonds.
 



### Role des Participants 

A chaque contact qui participe à un événement est attribué un "rôle" de participant. Le plus courant est probablement participant mais aussi animateur, formateur, conférencier, journaliste, invité, etc...
Les rôles des participants sont entièrement personnalisables pour correspondre aux types d'événements de votre organisation.
Ceci vous permet de sectoriser les participants dans des catégories significatives en fonction de leur participation à l'événement, par exemple pour l'envoi d'un e-mail à des bénévoles uniquement ou générer une liste de journalistes ayant assisté à vos évènements. 
Vous pouvez également créer des champs personnalisés qui ne concernent que des rôles spécifiques, par exemple, pour recueillir des informations sur la disponibilité des bénévoles seulement.


### Statut des Participants 

Le statut des participants (par exemple, enregistrés, liste d'attente, assisté ou annulé) est utilisé pour suivre le stade du contact par rapport à l'évènement. Les statuts des participants sont entièrement personnalisables pour correspondre à la façon dont votre organisation enregistre ses événements. Cela vous permet de segmenter les participants en catégories significatives en fonction de leur comportement à l'égard de l'événement, dans le but, par exemple, de générer des feuilles de présence, faire le suivi du nombre de personnes susceptibles de venir à un autre événement, et d'adapter les communications par courriel aux personnes inscrites.


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



