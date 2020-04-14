# Contributing to this guide

The documentation on this page is a starting point for contributing to the CiviCRM user guide.  There is also more advanced documentation for contributing in the [developer guide](https://docs.civicrm.org/dev/en/latest/documentation/).

## Style guide {:#style_guide}
When proposing changes please follow the [Documentation style guide](https://docs.civicrm.org/dev/en/master/best-practices/documentation-style-guide/).  

## Contributing a single change {:#single_changes}

1. [Sign up for a github account](https://github.com/join) (if you don't already have one) and [login](https://github.com/login).
2. Find the page in the manual that you want to edit.  For example, [Menu, Dashboard and Dashlets](../the-user-interface/menu-dashboard-and-dashlets.md)
3.  Click the pencil icon next to the page title.

![Image of the pencil icon](../img/contributing_to_this_manual.png)

4. You will be taken to an editing screen on GitHub.  Make your changes and then *Propose file change* including a descriptive comment.  

This will create a pull request (PR) for your changes.  Edit will be published as soon as they are reviewed by someone on our documentation team.

## Contributing multiple changes {:#multiple_changes}

1. [Sign up for a github account](https://github.com/join) (if you don't already have one) and [login](https://github.com/login).
2. Create a *Fork* with the fork button on the top right of the page.  

![Fork icon from github.com](../img/fork.png)


3. In your [git client](https://git-scm.com/download/gui/linux) clone the CiviCRM user guide repository to your computer.  
4. Locate the Markdown file (`.md`) in your file system that you want to edit by matching it to the file that that you want to change. For example, if you want to edit ["What is CiviCRM?"](../introduction/what-is-civicrm.md) you would find `<your_file_system>/docs/getting-prepared/is-civicrm-for-you.md`. 
5. Make one or more related changes and commit them in your git client.  
4. Push your changes from your git client to your fork.
5. In github.com click *New pull request* to create the new pull request (PR). 

![New PR in Github Interface](../img/new_pr.png)

6. Click *Create pull request*. 
7. Leave a descriptive message and then click *Create pull request *. 

Your PR will be reviewed by someone on the documentation team and published once they are approved.  

## Additional resources {:#additional_resources}

Additional resources on how CiviCRM does documentation and Markdown can be found in the [developer docs](https://docs.civicrm.org/dev/en/latest/documentation/#resources). 

## Versioning (which version should I edit?) {:#versioning}

All edits based on the current version of CiviCRM should be committed against the master branch.  The [Developer guide](https://docs.civicrm.org/dev/en/latest/documentation/#versions) has more detailed information. 
