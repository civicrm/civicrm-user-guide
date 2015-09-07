Bug Reporting
=============

Like all software there will be times when you use CiviCRM when things
don't work the way you expect them to.

A good first step is to search the forums
([http://forum.civicrm.org](http://forum.civicrm.org/)) for similar
problems and follow advice given there. If your problem hasn't been
addressed, posting to the forum is probably the right thing to do.

Before posting its a good idea to look on the forum for good posting
guidelines and spend a bit of time writing your post. Make sure you are
detailed and specific about what software you are using (i.e. the
version of CiviCRM, which CMS platform and its version, and which
browser and its version), what you are trying to do and how you are
trying to do it. For example letting people know the url you are using
(with any confidential details removed) may cause them to realise that
you are configuring the wrong page. Unclear posts are less likely to get
good replies.

Using older versions of CiviCRM
-------------------------------

If you are using an older version and the problem you are experiencing
is a bug that has been fixed in the lastest release, be prepared for the
answer "that it is time to upgrade to the latest version." Although the
CiviCRM community tries to be as helpful as possible, and we recognize
that upgrading puts a burden on your organisation, it is difficult to
support multiple versions simultaneously.

What causes problems with CiviCRM?
----------------------------------

Check the following possible sources of problems before you report
something on a forum. You can save yourself and a lot of people trouble
by isolating the problem. CiviCRM forums try to be friendly and don't
criticise you for misjudging a problem, but you'll certainly get more
help and resolve problems faster by doing some checking of your own
first.

-   Misunderstanding the software - we don't claim our documentation is
    perfect. But please go back and check it very carefully when you hit
    a barrier. Frustration makes it hard to concentrate, so be sure to
    read slowly and thoroughly. Also remember that different parts of
    CiviCRM depend on each other, so check for problems in related
    modules, besides the one you think the problem is in.
-   Your server set up - servers can be configured in many different
    ways, and these settings can change the way CiviCRM operates.
    Depending on your issue your server configuration may be causing you
    issues.
-   Using older or unsupported versions of CiviCRM, PHP, and MySQL -
    older and unsupported versions of software related to CiviCRM will
    most like cause unpredictable errors, so it is always a good
    practice to use the latest stable version of software.
-   Customisations made to the source code of your installation of
    CiviCRM - any changes made to the source code of CiviCRM may have
    unintended consequences. The community forums may be able to help
    you, but you will have to be patient, share source code, and try out
    suggestions. You may also want to check with your in-house
    development staff or outside consultant / service provider to
    determine whether CiviCRM has been customized in some way that might
    be related to the observed problem.
-   Other newly installed and enabled modules or components - you may
    need to review the additional modules and components you have
    installed and enabled that are not usually included in the install
    package to ensure that you have the latest stable version as well as
    using a ver[](javascript:void(0))sion of the module that works with
    your particular version of CiviCRM.
-   Bugs in the version of CiviCRM you are using - after you have
    eliminated all the previous options, you can report your problem as
    a bug. In fact, we appreciate you doing this, because you are making
    CiviCRM better for everyone.

Recreating your problem on the demo site
----------------------------------------

Recreating your bug on one of the demo sites
([http://demo.civicrm.org](http://demo.civicrm.org) and select the demo
site that matches your CiviCRM version) helps determine whether your
problem is a result of a bug in the source code, or as a result of
changes on your site. If you can show us that the code on the demo site
turns up your bug, it's very likely that the CiviCRM source code is the
problem, and your demonstration will help us find and fix it.

Still, no demo site can cover all possibilities. Issues involving email
output or payment processing cannot be recreated on the demo sites. So
even if you can't reproduce your bug there, it might still be a bug in
CiviCRM. It is, however, probably triggered by your server setup or
other customisations.

Write to the forum and explain the problem you are experiencing. If the
bug was reproduced on the demo site, describe exactly what you did
there, and copy the demo site's URLs to document the steps you used. If
not, include as much information about your server setup as you feasibly
can. Configuration files from the web server, CMS, and CiviCRM will be
valuable, but be careful to not including sensitive information such as
your database log-in.

If the forum suggests you discovered a bug in CiviCRM, you can report it
to the CiviCRM issue tracker
[](http://issues.civicrm.org/jira/browse/CRM)[http://issues.civicrm.org/jira/browse/CRM](http://issues.civicrm.org/jira/browse/CRM).

Writing good bug reports
------------------------

The best bug reports give lots of background and context. Don't forget
that the way you are using CiviCRM is most likely very specific to your
organisation. The more background you can give on the bug, the better.

The best bug reports clearly state:

-   What you did
-   What you expected to happen
-   What actually happened
-   Version of CiviCRM (must be included) 
-   Which CMS platform and CMS version (must be included)
-   Which browser and browser version (must be included)
-   Version of PHP and MySQL
-   Screen shots of the errors or issue
-   History of the bug
-   The recreatibility of the bug (e.g. bug always happens, bug is
    reported by some but can't recreate it or not consistently, bug
    happens when using this browser but not another browser, etc.)

Fixing bugs
-----------

The amount of time taken for the bug to be fixed depends on the severity
and complexity of the bug. It could be as quick as the same day, but it
could take much longer.

To get bug fixes, the easiest way is just to download and install the
latest revision of CiviCRM. Downloading bug fixes between releases and
fixing, called patching, your existing software is possible. If you have
technical abilities, then refer to the CiviCRM Developer's Guide for
instructions on applying a patch, otherwise, seek out technical
assistance to provide tests and a patch for the issue.
