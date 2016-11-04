Données personnalisées pour les événements
==========================================

Dans le cadre du processus de gestion des événements vous souhaiterez certainement recueillir des informations supplémentaires sur les événements ou sur leurs participants . Ce chapitre vous explique comment faire, facilement, avec les données personnalisées et vous informe des différentes façons de recueillir ces données pour les événements et comment mieux insérer chaque type d'information. Comprendre la façon dont les données personnalisées fonctionnent dans CiviCRM est nécessaire pour tirer le meilleur parti de ce chapitre. Pour mieux comprendre voir le chapitre *Champs personnalisés* dans *Organiser vos données*.

La question clé à se poser lors de l'ajout de données personnalisées pour la gestion des événements est *où ces données  doivent-elles aller?*
Il ya trois endroits où vous pouvez ajouter des données personnalisées

-   le dossier des participants
-   le dossier de contact
-   l'enregistrement d'événement.

Il est important d'ajouter des données personnalisées au bon endroit. Les ajouter au mauvais endroit pourrait vous causer des soucis ultérieurement. Exemple : Ajouter des données à l'enregistrement du participant, alors qu'elles devraient être ajoutées à l'enregistrement de contact, et vice-versa. 

Quelques exemples vous aiderons à clarifier .

-  Les préférences alimentaires devraient être ajoutées aux contacts car il est peu probable que cela change d'un événement à l'autre.
-  La préférence de choix d'une session (réunion, conférence, formation,...) doit être ajoutée au dossier du participant puisqu'elle n'est intéressante que dans le contexte de l'événement

Des champs personnalisés peuvent également être ajoutés aux événements. Par exemple : une organisation organise une série d'ateliers de formation tout au long de l'année et veut créer un champ personnalisé pour suivre six sujets communs developpés dans ces ateliers. Vous pouvez alors créer un champ de type "case à cocher" avec la liste des six options et l'ajouter en tant que donnée personnalisée pour les événements de cet atelier de formation. Ensuite, lors de la création d'un événement de type atelier de formation, ce champ sera disponible.

Notez que vous n'êtes pas obligé de sélectionner un type d'événement spécifique. En laissant la liste déroulante sur "Tout", cela indique que le champ est disponible pour tous les événements, quel que soit le type.

Une autre erreur classique que vous pouvez faire est d'ajouter des données personnalisées à l'enregistrement d'événement, quand vous devez les ajouter à l'enregistrement du participant. L'enregistrement de l'événement ne doit être utilisé que pour recueillir des informations sur l'événement lui-même, et non sur ses participants.

Différentes options lorsque vous ajoutez des données personnalisées aux participants :

-   **Participants:** ajoute le champ à tous les enregistrements des participants.
Utile si vous souhaitez recueillir des informations qui s'appliquent à tous les participants.

-   **Participants(Nom de l'évènement):**  identique pour tous les participants
Vous permet d'affecter un groupe de champs personnalisés à un événement spécifique. 
Utile pour ajouter des données d'enregistrement complexes pour un seul événement sans encombrer tous les événements.

-   **Participants (Rôle):** Ce champ ne sera disponible que pour certains types de participants.
Utile, par exemple, si vous avez besoin de recueillir des détails sur le profil de vos conférenciers (Social, Sponsor, Médecin,..) et souhaitez l'enregistrer lorsqu'il participe à l'événement.

L'ajout de données personnalisées requiert l'autorisation de l'administrateur. Pour ajouter des données personnalisées aux participants, ajoutez de nouveaux champs personnalisés via **Administer> Personnaliser les données et les écrans> Données personnalisées**. Pour créer des champs personnalisés pour les événements, ajoutez d'abord le champ **Personnalisé** sur l'enregistrement approprié, puis ajoutez les champs eux-mêmes.

Alternativement, vous pouvez créer des champs personnalisés à la demande pendant le processus de création d'événement - voir le chapitre *Création d'un événement*.
