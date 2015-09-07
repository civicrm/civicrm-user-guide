Hosting
=======

Before installing CiviCRM, careful consideration must be given to where
it will be hosted. The main options with an outline of the situations in
which you would want to choose them, and the advantages and
disadvantages of doing so are outlined below:

Internal hosting
-----------------

If you have an internal IT department or staff members with a technical
background, you may wish to host CiviCRM internally. To do this, you
will need:

-   Servers or dedicated PC hardware available to run as a web server,
    24-7.
-   A space on premises to permanently store the hardware, possibly air
    conditioned.
-   An un-interrupted power supply (UPS) to ensure the server is still
    available during power outages.
-   Either a stable internet connection with a static IP address and an
    SLA (Service Level Agreement) for high availability, or a leased
    line. It is important to note that should the Internet connectivity
    to the building in which your server resides goes down, only users
    on internal network will be able to access it. External visitors
    will not be able to access your website, including logging into
    CiviCRM and accessing online contribution forms. Widgets posted on
    other sites will also become unavailable. The bandwidth is also an
    important factor, as it must be high enough to serve the amount of
    traffic your website receives.

There are other aspects to address too. If you have an internal network,
the web server should be partitioned from the other computers and
servers to enhance security (e.g. in a Virtual Private Network or DMZ).
A web server could, potentially, introduce vulnerabilities that an
external individual, script or bot could use as a gateway into your
otherwise private, non-Internet facing systems. It is also a good idea
to research the maintenance and daily running costs of having an
internal server, and compare it to that of using an external host.

External hosting 
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


