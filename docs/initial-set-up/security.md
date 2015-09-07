Security
========

CiviCRM is a web based solution, and as such, requires a web server to
run. When web servers store sensitive data and are publicly available
over the Internet - as CiviCRM is designed to be - security is an
important aspect to consider. The recommended approach to securing CRM
data is to use a VPN (Virtual Private Network) to encapsulate data
transferred over public networks in encrypted packets. One of the
simplest methods of implementing this is through forcing the use of
encrypted tunnels when accessing the server through various data
protocols (e.g. SSH, SSL and FTPS, explored below); this effectively
wraps and the data in a protective shell, which can only be opened by
the user's web browser, and the server.

Encrypted data transfer
-----------------------

There are a number of different protocols (methods) for transferring
data from one point to another.

-   **FTPS**: for uploading files to the server outside of the CiviCRM
    interface (admins only), you may wish to use a FTPS (Secure File
    Transfer Protocol) client. If possible, set up FTPS accounts with
    usernames and passwords.
-   **SSH**: the SSH (Secure Shell) is a method which can be used to
    authenticate a user - by password or a key - and tunnel them into
    the server to execute command-line instructions.
-   **SSL**: this affects your everyday users accessing CiviCRM through
    a web browser. SSL (Secure Sockets Layer) encrypts the data
    submitted on a page by a user and sends it to the server - the only
    entity holding the 'key' to decrypt the data, and vice versa. SSL
    may be required for PCI compliance, or simply to prevent the
    interception of sensitive information during transit. By default,
    CiviCRM is *not* secured for browser access, please read the section
    'Setting up SSL' for configuration instructions.

Note: ensure passwords used by one person across several protocols are
different, as each carry with it varying levels of control.

Should I use SSL (Secure Sockets Layer)? 
-------------------------------------------

### PCI compliance

American Express, Discover Financial Services, JCB International,
MasterCard Worldwide, and Visa Inc. work together to form standards for
online payment processing (see
[https://www.pcisecuritystandards.org/organization_info/index.php](https://www.pcisecuritystandards.org/organization_info/index.php)).

Hosting for websites that accept payments using CiviContribute and
CiviEvent should comply with their standards if the plug-in you are
using does not route the user to external pages for payment processing
(e.g. PayPal Standard redirects users to PayPal pages to make the
transaction before returning to your website, and should therefore meet
these standards). If credit card information *is* being processed or
stored on your server, there are a number of PCI Payment Application
Data Security Standards (PCI PA-DSS) which must be met, including the
need to use SSL. Each CiviCRM installation must also be tested for PCI
compliance every 4-12 months. Consider the payment processing method you
intend to use carefully before implementing it, use SSL if you are using
a credit card payment processor, and seek security consultation if you
decide to store credit card information on your server (this is not
recommended).

For further information, see:
[https://www.pcisecuritystandards.org/merchants/index.php](https://www.pcisecuritystandards.org/merchants/index.php).

### Unauthorised data access

Aside from the potential need to meet PCI compliance, you should use SSL
if you wish to ensure:

-   your data cannot be read by unauthorised users (e.g. through
    intercepting un-encrypted data during transit between the user and
    server).
-   a user's session is not hi-jacked through acquiring the cookie used
    to authenticate their access. If this occurs, an unauthorised
    individual could assume their identity and proceed to use the system
    through their account.

Setting up SSL
--------------

Before choosing a hosting company or web server provider, check that
they support SSL certificates. As explained above, SSL encrypts the data
transferred between a user's web browser and the server, but this is
*not* enabled upon installation as it requires the purchase of an SSL
certificate from a trusted vendor. To install SSL:

1.  Determine what your server requirements or procedures are for
    enabling an SSL certificate. On shared servers this may require
    purchasing a static IP from your host. **Important**: your host must
    be willing to install the certificate on your *domain*, not one at a
    higher level. CiviCRM does not support shared SSL.
2.  Purchase an SSL certificate from a security vendor.
3.  Install the SSL on your server following the procedure you learned
    in step 1.
4.  Enable 'HTTPS' redirection on your CiviCRM site so that the login,
    online contribution, member, event and administrator pages use SSL
    encryption. CiviCRM has an option in global settings to check the
    certificate and enable SSL for these pages (**Administer** >
    **System Settings** > **Resource URLs**). To use SSL for *all*
    CiviCRM pages, either edit the server's apache .htaccess file to
    force SSL and redirect HTTP requests to HTTPS, or enable the option
    in Drupal.

Backups and their security
--------------------------

All computer systems are prone to failures - both hardware and software.
It is advisable to create periodic backups of all existing data (and
possibly the software) to fulfil two important purposes: recovery and
retention. In regards to recovery, the organisation can ensure that the
data gathered and stored in its database is not lost in the event of
failure. Backups can also aid in the strengthening of service
continuity. In some situations it is essential that data gathering or
analysis operations do not cease, and the ability to build a working
tool from a backup (while the issue is being addressed) minimises
downtime. Conversely, retention is useful when the organisation needs to
check the state of data gathered at a given time in the past.

Once made, the backups themselves must also be secured from natural
disasters, fire, vandalism and theft. It is good practice to encrypt
backups and duplicate them, keeping one copy on premises, and sending
the other to storage at another external location.

Data storage jurisdiction
-------------------------

CiviCRM can be run on a web server managed by your organisation, or by
an external hosting provider. When working with issues related to human
rights, or if your organisation is gathering sensitive information about
a country's government or its officials, it may be important to know
where your data is stored. Consider gathering detailed information about
where the servers are physically located, and the country whose
jurisdiction the data will fall under in case a governmental agency
requests information.

Other security concerns
-----------------------

Data may be accessed by unauthorised individuals through a
variety of methods, many of which do not directly relate to the CRM's
security. Amongst others, the following are areas that should be
examined:

-   Physical access to the server: the building holding the servers
    should be adequately protected against break-in.
-   Passwords: an organisational policy should be implemented where
    passwords are of a sufficient complexity and length (e.g. minimum 8
    characters, including letters and numbers), and must not be shared
    or divulged over insecure communications like email.
