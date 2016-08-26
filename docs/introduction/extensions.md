Extensions
==========

Les extensions fournissent des fonctions supplémentaires au « coeur » de CiviCRM. C'est la méthode recommandée pour créer de nouvelles fonctionnalités et pour modifier la façon que CiviCRM fonctionne, surtout lorsque ces changements ne sont pas nécessaires ou souhaités par l'ensemble de la communauté CiviCRM.

Plusieurs personnes développement des extensions pour leurs besoins spécifiques, puis les installent dans leur instance de CiviCRM. D'autres écrivent des extensions génériques qui peuvent être utiles pour d'autres organisations également. Ces extensions qui peuvent être utiles à d'autres organisations sont publiées dans le répertoire des extensions CiviCRM.

Le répertoire des extensions CiviCRM
------------------------

Le répertoire des extensions est disponible à l'adresse 
[https://civicrm.org/extensions](https://civicrm.org/extensions). On y retrouve une liste d'extensions développées par la communauté et qui ont été rendues librement et gratuitement disponible à l'ensemble de la communauté. Par défaut, les extensions sont affichées dans l'ordre croissant de popularité (calculé selon le nombre d'instances de CiviCRM qui utilisent l'extension et qui rapportent leurs statistiques).

![image](../img/z-extensions-website_1.png) 

Extensions are organized into two broad categories: 'native' extensions
which work with any CMS, and CMS specific extensions that add
integration between CiviCRM and the CMS and hence are CMS specific. If
you are familiar with your CMS, you may know CMS specific extensions by
another name, for example Drupal specific extensions are typically
called **Drupal Modules** and Wordpress specific extensions are called
**Wordpress Plugins**.

Extensions that have been approved for automated distribution can be
easily installed directly from your CiviCRM installation. 

Installer des extensions
---------------------

When configured correctly, extensions can be installed directly into
CiviCRM via the user interface. Go to **Administer > System Settings >
Manage Extensions**. You should see a list of extensions that are
compatible with your version of CiviCRM. Note that you may not see all
the extensions that were listed in the extensions directory as they may
not be compatible.

![image](../img/z-extensions-ui.png)

If you do not see a list of extensions here, it may be that your system
is not properly configured to manage extensions. You should consult your
system administrator if this is the case. 

Développer des extensions
--------------------

Anyone is free to write an extension to enhance their CiviCRM
installation (or commission someone to do so). Writing an extension is
a task for a developer so a detailed discussion of how to write one is
outside the scope of this book. If you do write an extension to cater
for your particular use case, you may wish to consider if other
organizations would also be able to benefit from your work and hence
whether you should publish your extension and make it more generic.
Publishing your extension and attracting users brings many benefits in
the shape of feedback on how it can be improved, bug reports, and code
contributions that may enhance your extension. 


