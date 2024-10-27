[![Debian](../Pics/openlogo-50.png)](https://www.debian.org/ "Debian Home")

  

[Skip Quicknav](#content)

* [Blog](https://bits.debian.org/ "Bits from Debian")
* [Micronews](https://micronews.debian.org/ "Micronews from Debian")
* [Planet](https://planet.debian.org/ "The Planet of Debian")

[Legal issues](https://www.debian.org/legal/) / Privacy Policy

Privacy Policy
==============

The [Debian Project](https://www.debian.org/) is a volunteer association of individuals who have made common cause to create a free operating system, referred to as Debian.

There is no requirement for anyone who wishes to use Debian to provide the project with any personal information; it is freely downloadable without registration or other form of identification from both official mirrors run by the project and numerous third parties.

Various other aspects of interacting with the Debian Project will, however, involve the collection of personal information. This is primarily in the form of names and email addresses in emails received by the project; all Debian mailing lists are publicly archived, as are all interactions with the bug tracking system. This is in keeping with our [Social Contract](https://www.debian.org/social_contract), in particular our statement that we will give back to the free software community (#2), and that we will not hide our problems (#3). We do not perform further processing on any of the information we hold, but there are instances where it is automatically shared with third parties (such as emails to lists, or interactions with the bug tracking system).

The list below categorises the various services run by the project, the information used by those services and the reasons it is required.

Questions about these services are best directed in the first instance to the service owner. If it's unclear who that is then you can contact the Data Protection team at [data-protection@debian.org](mailto:data-protection@debian.org), who will attempt to direct your enquiry to the right team.

Please note that (unless stated otherwise on this page) hosts and services under the **debian.net** domain are not part of the official Debian project; they are run by individuals who have an association with the project rather than the project themselves. Questions about exactly what data those services hold should be directed at the service owners rather than the Debian Project itself.

Contributors ([contributors.debian.org](https://contributors.debian.org/))
--------------------------------------------------------------------------

The Debian Contributors site provides an aggregation of data about where someone has contributed to the Debian Project, whether that's through filing a bug report, making an upload to the archive, posting to a mailing list or various other interactions with the Project. It receives its information from the services in question (details about an identifier such as login name and time of last contribution) and provides a single reference point to see where the Project is storing information about an individual.

The Archive ([ftp.debian.org](https://ftp.debian.org/debian/))
--------------------------------------------------------------

The primary distribution method of Debian is via its public archive network. The archive consists of all of the binary packages and their associated source code, which will include personal information in the form of names and email addresses stored as part of changelogs, copyright information, and general documentation. The majority of this information is provided via the upstream software authors distributed source code, with Debian adding additional information to track authorship and copyright to ensure that licenses are being correctly documented and the Debian Free Software Guidelines adhered to.

Bug Tracking System ([bugs.debian.org](https://bugs.debian.org/))
-----------------------------------------------------------------

The bug tracking system is interacted with via email, and stores all emails received in relation to a bug as part of that bug's history. In order that the project can effectively deal with issues found in the distribution, and to enable users to see details about those issues and whether a fix or workaround is available, the entirety of the bug tracking system is openly accessible. Therefore any information, including names and email addresses as part of email headers, sent to the BTS will be archived and publicly available.

DebConf ([debconf.org](https://www.debconf.org/))
-------------------------------------------------

The DebConf registration structure stores the details of conference attendees. These are required to determine eligibility to bursaries, association to the project, and to contact attendees with appropriate details. They may also be shared with suppliers to the conference, e.g. attendees staying in the conference provided accommodation will have their name and attendance date shared with the accommodation provider.

Debian Account Managers
-----------------------

The Debian Account Managers (DAM) hold information about project members that is mostly exposed via the New Members site ([https://nm.debian.org/](https://nm.debian.org/)) interfaces, described below. In rare cases they also hold personal information in their internal archives, such as when complaints are raised relating to project members and it is necessary to begin an investigation. As it is important to be able to refer to these archives in the future (e.g. if a previous project member wishes to rejoin to know if there circumstance around when they left the project that are relevant to the re-application) there is no fixed expiry date on these archives.

Developers LDAP ([db.debian.org](https://db.debian.org/))
---------------------------------------------------------

Project contributors (developers and others with guest accounts) who have account access to machines within the Debian infrastructure have their details stored within the project's LDAP infrastructure. This primarily stores name, username and authentication information. However it also has the optional facility for contributors to provide additional information such as gender, instant messaging (IRC/XMPP), country and address or phone details, and a message if they are on vacation.

Name, username and some of the voluntarily provided details are freely available via the web interface or LDAP search. Additional details are only shared with other individuals who have account access to the Debian infrastructure and is intended to provide a centralised location for project members to exchange such contact information. It is not explicitly collected at any point and can always be removed by logging into the db.debian.org web interface or sending signed email to the email interface. See [https://db.debian.org/](https://db.debian.org/) and [https://db.debian.org/doc-general.html](https://db.debian.org/doc-general.html) for more details.

Gitlab ([salsa.debian.org](https://salsa.debian.org/))
------------------------------------------------------

salsa.debian.org provides an instance of the [GitLab](https://about.gitlab.com/) DevOps lifecycle management tool. It is primarily used by the Project to allow Project contributors to host software repositories using Git and encourage collaboration between contributors. As a result it requires various pieces of personal information to manage accounts. For Project members this is tied to the central Debian LDAP system, but guests may also register for an account and will have to provide name and email details in order to facilitate the setup and use of that account.

salsa's primary purpose is to manage our git history. See below.

git
---

Debian maintains multiple git servers, containing source code and similar materials, and their revision and contribution histories. Individual Debian contributors also typically have information managed in git.

git history contains the name and email address of contributors (including bug reporters, authors, reviewers, and so on). git retains this information permanently in an append-only history. We use an append-only history because it has important integrity properties, notably significant protection against untracked changes. We retain it indefinitely so that we can always verify the copyright and other legal status of contributions, and so that we can always identify the originators for software integrity reasons.

The append-only nature of the git system implies that any modification to these commit details once they are incorporated into the repository is extremely disruptive and in some cases (such as when signed commits are in use) impossible. So we avoid this in all but extreme cases. Where appropriate, we use git features (eg `mailmap`) to arrange that historical personal information, though it is retained, can be elided or corrected when it is displayed or used.

Unless there are exceptional reasons to do otherwise, Debian's git histories, including the associated personal information about contributors, are completely public.

Gobby ([gobby.debian.org](https://gobby.debian.org/))
-----------------------------------------------------

Gobby is a collaborative online text editor, which tracks contributions and changes against connected users. No authentication is required to connect to the system and users may choose any username they wish. However while no attempt is made by the service to track who owns usernames it should be understand that it may prove possible to map usernames back to individuals based upon common use of that username or the content they post to a collaborative document within the system.

Mailing Lists ([lists.debian.org](https://lists.debian.org/))
-------------------------------------------------------------

Mailing lists are the primary communication mechanism of the Debian Project. Almost all of the mailing lists related to the project are open, and thus available for anyone to read and/or post to. All lists are also archived; for public lists this means in a web accessible manner. This fulfils the project commitment to transparency, and helps our users and developers understand what is happening in the project, or understand the historical reasons for certain aspects of the project. Due to the nature of email these archives will therefore potentially hold personal information, such as names and email addresses.

Alioth Lists ([alioth-lists.debian.net](https://alioth-lists.debian.net/))
--------------------------------------------------------------------------

Alioth Lists provides additional, subject-specific mailing lists for the Debian Project. Most of the mailing lists on this system project are open, and thus available for anyone to read and/or post to. Many lists are also archived; for public lists this means in a web accessible manner. This fulfils the project commitment to transparency, and helps our users and developers understand what is happening in the project, or understand the historical reasons for certain aspects of the project. Due to the nature of email these archives will therefore potentially hold personal information, such as names and email addresses.

The Alioth Lists service is also known as lists.alioth.debian.org.

New Members site ([nm.debian.org](https://nm.debian.org/))
----------------------------------------------------------

Contributors to the Debian Project who wish to formalise their involvement may choose to apply to the New Members process. This allows them to gain the ability to upload their own packages (via Debian Maintainership) or to become full voting members of the Project with account rights (Debian Developers, in uploading and non-uploading variants). As part of this process various personal details are collected, starting with name, email address and encryption/signature key details. Full Project applications also involve the applicant engaging with an Application Manager who will undertake an email conversation to ensure the New Member understands the principles behind Debian and has the appropriate skills to interact with the Project infrastructure. This email conversation is archived and available to the applicant and Application Managers via the nm.debian.org interface. Additionally details of outstanding applicants are publicly visible on the site, allowing anyone to see the state of New Member processing within the Project to ensure an appropriate level of transparency.

Popularity Contest ([popcon.debian.org](https://popcon.debian.org/))
--------------------------------------------------------------------

"popcon" tracks which packages are installed on a Debian system, to enable the gathering of statistics about which packages are widely used and which are no longer in use. It uses the optional "popularity-contest" package to collect this information, requiring explicit opt-in to do so. This provides useful guidance about where to devote developer resources, for example when migrating to newer library versions and having to spend effort on porting older applications. Each popcon instance generates a random 128 bit unique ID which is used to track submissions from the same host. No attempt is made to map this to an individual. Submissions are made via email or HTTP and it is thus possible for personal information to leak in the form of the IP address used for access or email headers. This information is only available to the Debian System Administrators and popcon admins; all such meta-data is removed before submissions are made accessible to the project as a whole. However users should be aware that unique signatures of packages (such as locally created packages or packages with very low install counts) may make machines deducible as belonging to particular individuals.

Raw submissions are stored for 24 hours, to allow replaying in the event of issues with the processing mechanisms. Anonymized submissions are kept for at most 20 days. Summary reports, which contain no personally identifiable information, are kept indefinitely.

snapshot ([snapshot.debian.org](http://snapshot.debian.org/))
-------------------------------------------------------------

The snapshot archive provides a historical view of the Debian archive (ftp.debian.org above), allowing access to old packages based on dates and version numbers. It carries no additional information over the main archive (and can thus contain personal information in the form of names + email address within changelogs, copyright statements and other documentation), but can contain packages that are no longer part of shipping Debian releases. This provides a useful resource to developers and users when tracking down regressions in software packages, or providing a specific environment to run a particular application.

Votes ([vote.debian.org](https://vote.debian.org/))
---------------------------------------------------

The vote tracking system (devotee) tracks the status of ongoing General Resolutions and the results of previous votes. In the majority of cases this means that once the voting period is over details of who voted (usernames + name mapping) and how they voted becomes publicly visible. Only Project members are valid voters for the purposes of devotee, and only valid votes are tracked by the system.

Wiki ([wiki.debian.org](https://wiki.debian.org/))
--------------------------------------------------

The Debian Wiki provides a support and documentation resource for the Project which is editable by everyone. As part of that contributions are tracked over time and associated with user accounts on the wiki; each modification to a page is tracked to allow for errant edits to be reverted and updated information to be easily examined. This tracking provides details of the user responsible for the change, which can be used to prevent abuse by blocking abusive users or IP addresses from making edits. User accounts also allow users to subscribe to pages to watch for changes, or see details of changes throughout the entire wiki since they last checked. In general user accounts are named after the name of the user, but no validation is performed of the account names and a user may choose any free account name. An email address is required for the purposes of providing a mechanism for account password reset, and notifying the user of any changes on pages they are subscribed to.

dgit git server ([\*.dgit.debian.org](https://browse.dgit.debian.org/))
-----------------------------------------------------------------------

The dgit git server is the repository of the git (revision control) histories of packages uploaded to Debian via `dgit push`, used by `dgit clone`. It contains similar information to the Debian archive and the Salsa gitlab instance: copies of (and past snapshots of) of the same information - in git format. Except for packages which are being first-time reviewed by Debian ftpmasters for inclusion in Debian: all this git information is always public, and retained forever. See [git](#git), above.

For access control purposes, there is a hand-maintained list of the ssh public keys of Debian Maintainers who have asked to be added. This manually maintained list is not public. We hope to retire it and instead use complete data maintained by another Debian service.

Echelon
-------

Echelon is a system used by the Project to track member activity; in particular it watches the mailing list and archive infrastructures, looking for posts and uploads to record that a Debian member is active. Only the most recent activity is stored, in the member's LDAP record. It is thus limited to only tracking details of individuals who have accounts within the Debian infrastructure. This information is used when determining if a project member is inactive or missing and thus that there might be an operational requirement to lock their account or otherwise reduce their access permissions to ensure Debian systems are kept secure.

Service related logging
-----------------------

In addition to the explicitly listed services above the Debian infrastructure logs details about system accesses for the purposes of ensuring service availability and reliability, and to enable debugging and diagnosis of issues when they arise. This logging includes details of mails sent/received through Debian infrastructure, web page access requests sent to Debian infrastructure, and login information for Debian systems (such as SSH logins to project machines). None of this information is used for any purposes other than operational requirements and it is only stored for 15 days in the case of web server logs, 10 days in the case of mail log and 4 weeks in the case of authentication/ssh logs.

* * *

Back to the [Debian Project homepage](https://www.debian.org/).

* * *

This page is also available in the following languages:

Select your language dansk español français Italiano Nederlands Português Русский (Russkij) 한국어 (Korean)

How to set [the default document language](https://www.debian.org/intro/cn)

* * *

**[Home](https://www.debian.org/)**

* [About](https://www.debian.org/intro/about)
    * [Social Contract](https://www.debian.org/social_contract)
    * [Code of Conduct](https://www.debian.org/code_of_conduct)
    * [Free Software](https://www.debian.org/intro/free)
    * [Legal Info](https://www.debian.org/legal)
* [Help Debian](https://www.debian.org/intro/help)

* [Getting Debian](https://www.debian.org/distrib/)
    * [Network install](https://www.debian.org/distrib/netinst)
    * [CD/USB ISO images](https://www.debian.org/CD/)
    * [Pure Blends](https://www.debian.org/blends/)
    * [Debian Packages](https://www.debian.org/distrib/packages)
    * [Developers' Corner](https://www.debian.org/devel/)

* [News](https://www.debian.org/News/)
    * [Project News](https://www.debian.org/News/weekly/)
    * [Events](https://www.debian.org/events/)
* [Documentation](https://www.debian.org/doc/)
    * [Release Info](https://www.debian.org/releases/)
    * [Debian Wiki](https://wiki.debian.org/)

* [Support](https://www.debian.org/support)
    * [Debian International](https://www.debian.org/international/)
    * [Security Information](https://www.debian.org/security/)
    * [Bug reports](https://www.debian.org/Bugs/)
    * [Mailing Lists](https://www.debian.org/MailingLists/)

* [Site map](https://www.debian.org/sitemap)
* [Search](https://search.debian.org/)
* [The Debian Blog](https://bits.debian.org/)
* [Debian Micronews](https://micronews.debian.org/)
* [Debian Planet](https://planet.debian.org/)

See our [contact page](https://www.debian.org/contact) to get in touch. Web site source code is [available](https://salsa.debian.org/webmaster-team/webwml).

Last Modified: Tue, Feb 13 13:41:50 UTC 2024   Last Built: Sat, Oct 26 19:49:22 UTC 2024  
Copyright © 1997-2024 [SPI](https://www.spi-inc.org/) and others; See [license terms](https://www.debian.org/license)  
Debian is a registered [trademark](https://www.debian.org/trademark) of Software in the Public Interest, Inc.