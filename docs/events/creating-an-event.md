Création d'un événement
=======================

Ce chapitre décrit la façon de créér un nouvel événement et chacune des options disponibles dans les écrans de saisie.
Pour permettre l'inscription en ligne à un l'événement, vous devez lire le chapitre *online event registration*. Sinon vous pouvez également consulter ce chapitre : *manual event registration*.

Pour commencer, créez un nouvel événement en choisissant le menu : **Events > New Event**.(Si vous ne voyez pas le menu Evénement, assurez-vous que le composant evénement est bien activé. Vous pouvez l'activer ici: **Administer > Configure > Global Settings > Enable Components**.)

Information et paramétrage
------------------------------

Le premier écran que vous voyez lors de la création demande des informations de base sur l'événement.
Vous pouvez cliquer sur l'un des points d'interrogation bleus pour afficher une aide sur chacun des champs à remplir. En cliquant sur le crayon à droite de certains champs vous ouvrez un écran où vous pouvez modifier les options disponibles.
Notez qu'en fonction de vos autorisations vous ne serez pas en mesure de voir ce crayon et vous ne pourrez modifier ces options

![image](../img/4.5_new_event.PNG)

**From template** vous permet de créer un événement à partir d'un modèle (voir le chapitre *Event templates* dans ce document)  plutôt que d'en créer un à partir de zéro.

**Event type** permet de classer l'événement dans une catégorie.

Si vous avez **CiviCampaign** activé, vous pouvez sélectionner une campagne pour que cet événement y soit intégré (voir la section *Campaign* pour plus de détails).

**Rôle** Attribue un type de rôle aux participants, tel que participant, animateur, conférencier, ou bénévole.
Quel est le rôle attribué aux participants lors de leur inscription en ligne pour cet événement?
La valeur placée dans ce champ sera attribué par défaut lorsque les utilisateurs s'enregistrent en ligne ou lorsque vous importez des enregistrements à moins que vous n'insériez le champ "rôle" avec d'autres valeurs dans votre fichier d'importation CSV. La valeur la plus commune est Participant

Voulez-vous que les visiteurs voient la liste des participants, et quelles informations souhaitez-vous afficher sur les participants?

 **Listing Participant **: Afficher la liste des participants permet de montrer leur intérêt et peut susciter d'autres inscriptions du public. Pour cela  cocher l'option * activer * listes de participants - Pour l'afficher, vous aurez besoin de  créer un élément de menu ou un lien vers la liste sur votre site. Une fois que vous avez créé l'événement, l'option lien participant est affiché sur la page de configuration de l'événement. Reportez-vous à la gestion de l'événement chapitre * Event management * pour obtenir des informations sur les listes des participants et d'autres façons de promouvoir vos événements.
 
Quel est le nom de votre événement ? Le ** Titre de l'événement ** apparaîtra sur les pages d'information, d'inscription, sur la liste des d'événements, et dans la Gestion des événements (Page administration). Assurez-vous de choisir un titre significatif qui represente votre événement.
Les deux champs suivants (** Résumé de l'événement ** et ** Description complète **) vous permettent de décrire votre événement. Le résumé et la description complète seront inclus sur les pages d'information de l'événement.Utilisez l'éditeur de texte enrichi prévu pour le champ de description afin d'inclure photos, images et texte formaté.

Entrez le ** Date de début / heure ** et ** Date de fin / heure ** pour votre événement. Celles-ci seront incluses dans les pages d informations et la liste des événements.

Vous pouvez définir un ** Nombre maximum de participants ** pour chaque événement et définir un message à afficher lorsque ce nombre est atteint.
.
Si vous souhaitez afficher une carte montrant l'emplacement de l'événement, vous pouvez le faire en utilisant soit Google Maps ou Open Street (vous devrez configurer votre solution de cartographie par ** Administrer> Paramètres système> cartographie et géocodage **).

Sélectionnez ** Évènement public ** pour inclure l'événement dans les listes promotionnelles telles que des flux RSS, des fichiers ou des flux iCal et la page de liste d'événements.

Sélectionnez ** Autoriser le partage à travers les médias sociaux ** pour inclure des liens de médias sociaux pour le partage de cet événement sur la page Information sur l'événement, page de remerciement, Tell-a-Friend la page (si activé), et dans les courriels de confirmation de l'événement.

Enfin, vous avez la possibilité de choisir que cet événement soit actif ou inactif
Si vous prévoyez de prendre un certain temps pour terminer la configuration de votre événement, choisisez de le rendre inactif jusqu'à ce qu'il soit complet pour s'assurer qu'il ne figure pas par inadvertance sur la liste des flux d'événements. Vous pourrez ainsi  l'activer facilement lorsque vous serez prêt à commencer sa diffusion.

Après avoir vérifié les détails de cette page, cliquez sur ** Continuer >> ** pour créer votre événement et passer à l'étape suivante. Vous pouvez interrompre la configuration sur une page suivante en cliquant sur ** Enregistrer et Terminé ** et revenir plus tard pour examiner et modifier l'un des paramètres.

Pour revenir à un événement enregistré, accédez ** Événements> Événements Manager ** et cliquez sur ** Configurer **  pour continuer à travailler ou modifier l'événement.

Localisation
--------------

L'étape suivante consiste à compléter la localisation et les coordonnées de l'événement.

Une fois que vous avez saisi un lieu de l'événement, vous pouvez le réutiliser pour des événements ultérieurs en cliquant sur ** Utiliser un emplacement existant  ** et en le sélectionnant dans la liste déroulante. Notez que si vous choisissez un emplacement existant et de que vous le modifiez, il mettra à jour ce lieu pour tous les événements qui l'utilisent.

![image](../img/event%20location%20with%20warning.PNG)

Vous pouvez aussi lister les numéros de téléphone et adresses e-mail sur la page d'information de l'événement si vous voulez donner aux inscrits un moyen de communiquer directement avec les organisateurs de l'événement. Si l'événement a lieu hors site de l'emplacement principal, vous pouvez également fournir des informations de contact sur le lieu de la réunion.


Frais
-----

Si l'événement est gratuit, cochez ** Evénement payant ** à ** Non **, puis cliquez sur  ** Enregistrer ** et passez à l'inscription en ligne.
Si l'événement payant, cliquez sur ** Oui **. L'écran affiche les options disponibles (voir l'ensemble des captures d'écran ci-dessous).


What **Contribution Type** (financial type) will be assigned to paid
registrations for this event? Although the most common value for this
field is simply Event Fee, CiviCRM provides the flexibility to define
multiple Financial Types and assign them to different events as needed.
See *Set-Up* in the *Contributions* section for details.

If you plan to accept credit card payments through the online
registration form, you need to configure a **payment processor** prior
to creating your event. Find more information about this, see *Payment
Processors* in the *Contributions* section.

Do you want to allow registrants to pay later by mailing in a check,
paying on-site with cash or credit card, or arranging some other payment
method? If so, you can enable the **Pay Later option** and define a
label and payment instructions. If you keep this unchecked, registrants
will be required to pay by credit card.

![EventFeesPayLater](../img/CiviCRM_update-CiviEvent-EventFeesPayLater-en.png "EventFeesPayLater")

**Regular Fees** provide a set of price levels from which the registrant
must select a single level (e.g. an individual registration for $50 or
a family registration for $100). Each fee amount has a label assigned
and you can set a default fee. This approach works well for many events
and is easy to set up. Here's a simple example:

![EventRegFees](../img/CiviCRM_update-CiviEvent-EventRegFees-en.png "EventRegFees")

If your event requires a more complex pricing structure, with more
options or additional add-ons, you may wish to use **price sets** or
**discounts**. For more information about this, see the *Complex event
fees* chapter in this section.

Online registration
--------------------

Allowing people to register online (self-service) through your web site
offers many benefits. Online registration is convenient for your
constituents and can save staff time and resources. If you do not need
to offer online registration, do not check **Allow Online
Registration** and move onto the next step. If you do want to allow
online registration, please see the *Online event registration* chapter
in this section.

Scheduled reminders
-------------------

Scheduled reminders can be used to automatically send event registrants
emails at certain times before or after events, for example

-   a week before: remind them that they should check out the conference
    schedule
-   a day after: ask them to fill in the feedback form
-   Two days before payment is due for a Pending from Pay Later
    registration: warn them that their registration will be cancelled if
    they don't provide payment details in the next 48 hours.

To set up a scheduled reminder for a specific event, click on the
scheduled reminders tab, which will show you already existing scheduled
reminders for this event (if any) and click on **Add Reminder**.

![image](../img/scheduled-reminder-events.png)Fill in the details on
this form to send, for example, an email to all registered speakers 3
days before the event start date.  Note that you can limit recipients by
status (registered, attended, etc.) and also by role (speaker, attendee,
volunteer, etc.).  You can either use a template or compose your own
message in the HTML format box.

![image](../img/scheduled-reminder-events-compose.png)

As well as setting up reminders on an event by event basis, you can also
set them up for specific event types. and add them to specific event
templates.  The idea is basically the same as above, but you can access
this functionality from **Administer > Communications > Scheduled
reminders**.

Tell-A-Friend
-------------

CiviEvent makes it easy to leverage the social networking power of your committed
constituents by empowering them to quickly and easily share details
about your organization and event with their friends and colleagues. The
final step in the event creation is a page where you can enable
"Tell-A-Friend" capabilities. You can define the text and links to be
included on that page and in the email sent from the tool (see the
following screenshot).

![EventTellFriend](../img/CiviCRM_update-CiviEvent-EventTellFriend-en.png "EventTellFriend")

A "Tell a friend" activity record will be added to a participant's
Activities tab each time she sends mail to her friends. This allows you
to track your most active supporters and engage them further. The people
who are emailed using this feature are also automatically added to
CiviCRM as contacts.

Registration confirmation and receipting
----------------------------------------

You can send automated confirmation and receipt emails to participants
who register for an event, whether they register online are registered
by your staff or volunteers. The content and layout of these emails are
controlled by message templates*.*Both HTML and Text formats are
provided. You can modify or add text to these emails, or add branding
such as a logo to the HTML versions. To set up a from email address from
which to send the confirmation and receipts, see Set-Up in the Email
section.

Navigate to **Administer > Communications > Message Templates** (shown
in the following screenshot) and click the **System Workflow Message**
tab to see the list of messages you can modify. Click **Edit** next to
"Events - Registration Confirmation and Receipt" rows to edit the
content and layout.

![WorkflowMsgTpls](../img/CiviCRM_update-CiviEvent-WorkflowMsgTpls-en.png "WorkflowMsgTpls")


The templates for these messages include both the text shown and
necessary program logic. Use caution when editing so as not to modify
the program logic. Be sure to test the workflow and review the emails
sent after making any changes. If you find that your changes have caused
problems, errors or missing information, you can always revert to the
system default for that workflow.  
