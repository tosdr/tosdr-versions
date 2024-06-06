[Jump to content](#bodyContent)

 Main menu

Main menu

move to sidebar hide

Navigation

* [Main page](https://community.kde.org/Main_Page "Visit the main page [z]")
* [Community portal](https://community.kde.org/KDE_Community_Wiki:Community_portal "About the project, what you can do, where to find things")
* [Current events](https://community.kde.org/KDE_Community_Wiki:Current_events "Find background information on current events")
* [Recent changes](https://community.kde.org/Special:RecentChanges "A list of recent changes in the wiki [r]")

contributor help pages

* [Tasks and Tools](http://userbase.kde.org/Tasks_and_Tools)
* [Modify a page](http://userbase.kde.org/Ub-helpfiles-modify-redirect#Update_Existing_Content)
* [Add new content](http://userbase.kde.org/Ub-helpfiles-new-content-redirect#Add_New_Pages)
* [Page elements](http://userbase.kde.org/PageLayout)
* [Typographical guidelines](http://userbase.kde.org/Typographical_Guidelines)
* [More markup help](http://userbase.kde.org/Toolbox)

[![KDE Community Wiki](/images/kde-logo-white-blue-source.svg)](https://community.kde.org/Main_Page)

[Search](https://community.kde.org/Special:Search "Search KDE Community Wiki [f]")

Search

* [Log in](https://community.kde.org/index.php?title=Special:UserLogin&returnto=Policies%2FTelemetry+Policy "You are encouraged to log in; however, it is not mandatory [o]")

 Personal tools

* [Log in](https://community.kde.org/index.php?title=Special:UserLogin&returnto=Policies%2FTelemetry+Policy "You are encouraged to log in; however, it is not mandatory [o]")

Contents
--------

move to sidebar hide

* [Beginning](#)
* [1Transparency](#Transparency)
    
* [2Control](#Control)
    
* [3Anonymity](#Anonymity)
    
* [4Minimalism](#Minimalism)
    
* [5Privacy](#Privacy)
    
* [6Compliance](#Compliance)
    

Toggle the table of contents

 Toggle the table of contents

Policies/Telemetry Policy
=========================

* [Page](https://community.kde.org/Policies/Telemetry_Policy "View the content page [c]")
* [Discussion](https://community.kde.org/Talk:Policies/Telemetry_Policy "Discussion about the content page [t]")

 English

* [Read](https://community.kde.org/Policies/Telemetry_Policy)
* [View source](https://community.kde.org/index.php?title=Policies/Telemetry_Policy&action=edit "This page is protected.
    You can view its source [e]")
* [View history](https://community.kde.org/index.php?title=Policies/Telemetry_Policy&action=history "Past revisions of this page [h]")

 Tools

Tools

move to sidebar hide

Actions

* [Read](https://community.kde.org/Policies/Telemetry_Policy)
* [View source](https://community.kde.org/index.php?title=Policies/Telemetry_Policy&action=edit)
* [View history](https://community.kde.org/index.php?title=Policies/Telemetry_Policy&action=history)

General

* [What links here](https://community.kde.org/Special:WhatLinksHere/Policies/Telemetry_Policy "A list of all wiki pages that link here [j]")
* [Related changes](https://community.kde.org/Special:RecentChangesLinked/Policies/Telemetry_Policy "Recent changes in pages linked from this page [k]")
* [Special pages](https://community.kde.org/Special:SpecialPages "A list of all special pages [q]")
* [Printable version](javascript:print(); "Printable version of this page [p]")
* [Permanent link](https://community.kde.org/index.php?title=Policies/Telemetry_Policy&oldid=87332 "Permanent link to this revision of this page")
* [Page information](https://community.kde.org/index.php?title=Policies/Telemetry_Policy&action=info "More information about this page")

From KDE Community Wiki

< [Policies](https://community.kde.org/Policies "Policies")

Application telemetry data can be a valuable tool for tailoring our products to the needs of our users. The following rules define how KDE collects and uses such application telemetry data. As privacy is of utmost importance to us, the general rule of thumb is to err on the side of caution here. Privacy always trumps any need for telemetry data, no matter how legitimate.

These rules apply to all products released by KDE. We ask all distributors of KDE products as well as all vendors of addons for KDE products to respect them as well.

Transparency
------------

We provide detailed information about the data that is going to be shared, in a way that:

* is easy to understand
* is precise and complete
* is available locally without network connectivity

Any changes or additions to the telemetry functionality of an application will be highlighted in the corresponding release announcement.

Control
-------

We give the user full control over what data they want to share with KDE. In particular:

* application telemetry is always opt-in. That means off by default and only activated by the explicit action of the user (inaction is not good enough).
* application telemetry settings can be changed at any time, and are provided as prominent in the application interface as other application settings
* application telemetry settings are independent of any other settings, features or functionality, that is applications can't tie the availability of unrelated aspects of the application to telemetry being enabled
* applications honor system-wide telemetry settings where they exist (global "kill switch")
* we provide detailed documentation about how to control the application telemetry system

In order to ensure control over the data after it has been shared with KDE, applications will only transmit this data to KDE servers, that is servers under the full control of the KDE sysadmin team. Any data transmission has to be done using appropriate transport security.

We will provide a designated contact point for users who have concerns about the data they have shared with KDE. While we are willing to delete data a user no longer wants to have shared, it should be understood that the below rules are designed to make identification of data of a specific user impossible, and thus a deletion request effectively impossible.

Anonymity
---------

We do not transmit data that could be used to identify a specific user. In particular:

* we will not use anything that would be considered personal data by common sense or data protection laws and regulations (such as e.g. EU GDPR)
* we will not use any unique device, installation or user id
* data is stripped of any unnecessary detail and downsampled appropriately before sharing to avoid fingerprinting
* network operation data (such as IP addresses inevitably exposed as part of the data transmission) is not stored together with the telemetry data, and must not be used in combination with telemetry data for any kind of data analysis. Network operation data is only stored and used for enabling a secure and effective operation of the KDE infrastructure (for example for abuse counter-measures on the telemetry system), as deemed necessary by the KDE sysadmins.

Minimalism
----------

We only track the bare minimum of data necessary to answer specific questions, we do not collect data preemptively or for exploratory research. In particular, this means:

* collected data must have a clear purpose
* data is downsampled to the maximum extent possible at the source
* relevant correlations between individual bits of data should be computed at the source whenever possible
* data collection is stopped once the corresponding question has been answered

Privacy
-------

We will never transmit anything containing user content, or even just hints at possible user content such as e.g. file names, URLs, etc.

We will only ever track:

* system information that is specific to the installation/environment, but independent of how the application/machine/installation is actually used
* statistical usage data of an installation/application

Compliance
----------

KDE only releases products capable of acquiring telemetry data if compliance with these rules has been established by a public review on \[kde-core-devel|kde-community\]@kde.org from at least two reviewers. The review has to be repeated for every release if changes have been made to how/what data is collected. The result of the review, together with documentation of the data tracked and the reason for the data collection, is tracked on [Telemetry Use](https://community.kde.org/Telemetry_Use "Telemetry Use").

Received data is regularly reviewed for violations of these rules, in particular for data that is prone to fingerprinting. Should such violations be found, the affected data will be deleted, and data recording will be suspended until compliance with these rules has been established again. In order to enable reviewing of the data, every KDE contributor with a developer account will have access to all telemetry data gathered by any KDE product.

Retrieved from "[https://community.kde.org/index.php?title=Policies/Telemetry\_Policy&oldid=87332](https://community.kde.org/index.php?title=Policies/Telemetry_Policy&oldid=87332)"

* This page was last edited on 17 January 2020, at 12:44.
* Content is available under [Creative Commons License SA 4.0](https://community.kde.org/KDE_Community_Wiki:Copyrights) unless otherwise noted.

* [Privacy policy](https://community.kde.org/KDE_Community_Wiki:Privacy_policy)
* [About KDE Community Wiki](https://community.kde.org/KDE_Community_Wiki:About)
* [Disclaimers](https://community.kde.org/KDE_Community_Wiki:General_disclaimer)

* [![Creative Commons License SA 4.0](/resources/assets/licenses/gfdlcc.png)](https://community.kde.org/KDE_Community_Wiki:Copyrights)
* [![Powered by MediaWiki](/resources/assets/poweredby_mediawiki_88x31.png)](https://www.mediawiki.org/)

* Toggle limited content width

![](https://stats.kde.org/piwik.php?idsite=25&rec=1)