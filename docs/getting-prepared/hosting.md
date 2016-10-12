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

With internal expertise you could manage the install and configuration
in-house, but host CiviCRM with an external provider. In this instance,
we recommended you rent a VPS (Virtual Private Server) to ensure you
have complete control of all packages and libraries (e.g. PHP, MySQL,
etc), and are therefore able to configure it to your specific
requirements.

Many shared hosts restrict the level of access you have, and may not
support CiviCRM if you are unable to install the required
pre-requisites. Shared hosts can also be prone to performance issues, as
the hardware is shared between a group of customers with varying usage
levels; if one customer's website suddenly receives a large spike in
traffic, every website on that server could experience a lengthy outage.

Disadvantages aside, leasing space on a shared host is typically cheaper
than a VPS, and both are subscription services on a monthly or annual
basis (discounts may be available for longer leases.

**We advise that you trial run any service for a short-term before
committing to a longer period.**

Existing hosting
----------------

If you are already using a website host, contact your provider to
determine whether they support the packages and libraries required by
CiviCRM. If they do not, there are two options available to you:

### **Migrate to another host**.

Depending on the CMS you are using, the process of moving from one host
to another may be fairly straightforward. You are in a good position to
transfer to another host if you can:  

1.  request that your users **stop creating and updating content**
    during the migration,
2.  **export and import** all of the content from/to the chosen CMS,
3.  **edit your DNS records** to switch the 'pointers' to your
    website from the old host to the new host

### **Run the website and CiviCRM in parallel, on different servers**.

If you cannot move your website to a different host, you could purchase
a second account on a host capable of running CiviCRM, and run the two
systems alongside each other.

In this instance, you would use a CNAME DNS record to point to a second
copy of the CMS and CiviCRM on the other host (e.g.
civicrm.yourwebsite.com; the CNAME effectively adds a prefix to your
website's address), and link to it from your website, perhaps in form of
a log-in button.

Aside from paying a second bill, one of the limitations to this approach
is the need to clone the style of your website on the second host to
give the visitor the illusion that they are in the same place. If
changes to the style are changed, the work must be duplicated.

Outsourcing to a CiviCRM implementer/host
-----------------------------------------

There are implementers and experts in the CiviCRM community able to
manage the hosting and/or installation for you. If requested, they may
also be available to manage a local implementation and configuration on
your premises.

For a list of experts recommended within the community, visit:
[https://civicrm.org/providers](https://civicrm.org/providers)


