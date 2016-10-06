Paramétrage
===========

Le but de ce chapitre est de vous aider à paramétrer le composant CiviCampaign.
Cela vous permettra de bien suivre et analyser l'ensemble des activités liées à une campagne, que ce soit des contibutions, des sondages ou enquêtes, des mailings, ou tout autre composant.

Activation de CiviCampaign 
--------------------------

La première étape est l'activation du composant CiviCampaign.

1.  Ouvrir le menu **Administer > Paramètres système > Activer les composants CiviCRM**.
2.  Sélectionner **CiviCampaign**, cliquer sur **Activer** puis **Enregistrer** 

A partir du moment où CiviCampaign est activé, le nouveau menu **Campagnes** apparait dans votre interface CiviCRM.

Add a new campaign type
-----------------------

CiviCampaign provides three default campaign types:

-   Direct Mail
-   Referral Program
-   Constituent Engagement

You can add any campaign type that is appropriate for your work (and
disable those that aren't).

To add a new campaign type:

1.  Go to **Administer > CiviCampaign > Campaign Types**. 
2.  This will display a list of existing campaign types: 
     
    ![image](../img/campaign_configuration_typeoptions_1.png)
3.  Click on **Add Campaign Type**, and give the new type a label and a
    description (optional).
4.  Optionally, change the default weight: this affects the order in
    which this new event type appears in drop-down menus (smallest
    numbers appear highest).
5.  Click **Save**.

The next time you add a new campaign, this campaign type will be
available to assign to your new campaign.

Campaign status
---------------

Assigning a status to your campaign makes it possible to update campaign
activities in the database and track how the campaign is proceeding.

1.  Go to **Administer > CiviCampaign > Campaign Status**. 
    The default statuses are Planned, In Progress, Completed, and
    Cancelled.
2.  Click **Add Campaign Status**, give it a name and, optionally, a
    description.
3.  Changing the weight is not necessary but will affect the order in
    which this new status appears in drop-down menus.
4.  Click **Save** and the new status will then be available to assign
    to campaigns.

![image](../img/campaign_configuration_statuses.png)

Engagement index 
----------------

CiviCampaign allows you to track an individual's level of
interest/engagement in a particular activity. The Engagement Index can
be recorded for general activities or actions, i.e. Send an Email,
Meeting, Phone Call, Interview, and any additional custom
activities/actions you create. To find out more about how to record an
activity to an individual, see Contacts in the Organising Your Data
section. 

To configure the Engagement Index:

1.  Go to **Administer > CiviCampaign > Engagement Index**.
2.  Configure the engagement index as a number, e.g. 1 is a high level
    of engagement, and 5 is low level of engagement.

This information can supplement your outreach employees' or organizers'
assessment of member engagement/interest in your organization.

![image](../img/campaign_configuration_engageoptions.png)
