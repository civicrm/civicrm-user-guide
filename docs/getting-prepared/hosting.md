Hébergement
===========

Avant d'installer CiviCRM, il faut considérer attentivement où héberger l'application. Les sections ci-dessous survolent les principaux avantages et inconvénients des principales options.

Hébergement interne
-------------------

Si vous avez un département d'informatique ou des employés avec un profil technique, vous voudrez peut-être héberger CiviCRM à l'interne. Pour ce faire, il faudra :

- Des serveurs ou ordinateurs didiés pouvant disponibles pour faire fonctionner un serveur web 24x7.
- Un espace dans vos bureaux où il est possible de faire fonctionner le matériel informatique, idéalement dans un endroit climatisé.
- Une batterie (UPS) pour s'assurer que le serveur ne sera pas affecté par les pannes d'électricité.
- Une connexion Internet stable et suffisamment performante pour permettre l'accès à partir de l'extérieur du bureau, avec une adresse IP fixe.

Il y a d'autres facteurs à considérer. Si vous avez un réseau interne, le serveur web devrait être isolé des autres ordinateurs de votre bureau pour réduire les risques de sécurité (dans le jargon: une zone démilitarisée, DMZ). Un serveur web peut, potentiellement, augmenter les risques en servant de porte d'entrée dans le reste de votre réseau privé. Il est également suggéré de calculer les coûts de maintenance d'un serveur interne, pour mieux comparer avec les coûts d'un serveur hébergé à l'externe.

Hébergement externe
-----------------

Vous pouvez héberger CiviCRM avec un fournisseur d'hébergement externe, mais tout en faisant vous-même l'installation et la configuration de CiviCRM. Dans ce cas, il est recommandé de louer un serveur virtuel privé (VPS) pour avoir le plein contrôle sur les logiciels qui seront disponibles sur le serveur (PHP, MySQL, etc) et pour pouvoir les configurer selon les exigences de CiviCRM.

La majorité des hébergeurs mutualisés restreignent certaines fonctions et ne peuvent pas répondre aux exigences de CiviCRM. Les hébergeurs mutualisés sont aussi susceptibles à des problèmes de performance, ce qui aura un impact négatif sur la perception de l'outil.

**Il est fortement recommandé de faire un essais à court terme avec un hébergeur avant de s'engager sur une plus longue période.**

Hébergement existant
-------------------

Si vous avez déjà un hébergement pour votre site web, contactez-les pour déterminer s'ils supportent les outils nécessaires pour faire fonctionner CiviCRM. Sinon, vous avez deux options :

### Migrer vers un autre hébergement

Selon le système de gestion de contenu que vous utilisez, la procédure pour migrer d'un hébergeur à un autre peut se faire assez facilement. La migration sera plus facile si vous pouvez :

1. demander à vos utilisateurs d'arrêter de publier ou modifier du contenu durant la période de migration,
2. exporter et importer tout le contenu de votre site web (fichiers, base de données),
3. modifier les entrées de votre zone DNS pour « pointer » votre domaine vers le nouvel hébergement.

### Héberger CiviCRM sur un site (serveur) séparé

Si vous ne pouvez pas migrer votre site web vers un autre hébergement, vous pouvez ouvrir un second compte d'hébergement chez un autre hébergeur et rouler les deux sites côte à côte.

Dans ce cas, vous pouvez créer un nouveau « sous-site », par exemple sur https://civicrm.exemple.ca et y ajouter des liens à partir de votre site principal (ex: pour les formulaire de dons).

Cependant, vous devrez clôner le visuel de votre site principal sur votre second site pour ne pas trop désorienter vos visiteurs lorsqu'ils naviguent d'un site à l'autre. Si vous modifiez le visuel sur un site, il faudra aussi modifier l'autre site.

Faire appel à un fournisseur d'hébergement/consultation externe
---------------------------------------------------------------

Il y a des experts en implémentation de CiviCRM qui peuvent gérer l'hébergement et/ou l'installation pour vous. Si nécessaire, certains fournisseurs peuvent aussi gérer l'installation de CiviCRM sur vos serveurs.

Pour consulter une liste d'experts, visiter :  
[https://civicrm.org/providers](https://civicrm.org/providers)


