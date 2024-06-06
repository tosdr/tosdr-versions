 [IRCCloud](https://www.irccloud.com/) 
=======================================

Abuse and Harassment Policy
===========================

We take abuse and harassment very seriously; we do not want IRCCloud to become a tool for ban evasion, and we're happy to work with network and channel operators to make sure this is the case.

How to ban IRCCloud users
-------------------------

The **ideal ban mask** for banning a specific IRCCloud account is: **`*!*id12345@*.irccloud.com`**, where `12345` is the user's ID. Note that **`uid`** indicates a free account, paid accounts have the prefix **`sid`**.

* Each IRCCloud user is allocated a unique, static user ID which they cannot change.
* This ID is included in the username and is verified by IDENT, so it can be used to positively identify one user for banning.

The hostname that an IRCCloud account connects from can vary:

* If the connection is made using IPv4, they may originate from a number of IPv4 connection pools. See our [networks FAQ](https://www.irccloud.com/networks) for the full list.
* If the connection is made using IPv6, they will originate from their own IPv6 address.
* All of these addresses will have a reverse DNS entry pointing to a subdomain of irccloud.com.

When NOT to report abuse
------------------------

In general we defer to network and channel staff in cases where a simple ban will suffice, or where it's more difficult to make a judgment call. These include:

* A single abusive user who isn't evading bans and never comes back. A ban solves the problem.
* Someone’s squatting your nick or channel. This is what Nickserv/Chanserv etc. are for. If you need to reclaim your nick or channel and haven't registered it, please appeal to network staff. This isn't an area we get involved in unless widespread impersonation and abusive behaviour is taking place.
* Any situation where using the /ignore feature of your client would solve it.

How to report abuse or harassment
---------------------------------

If a user continues to use IRCCloud to evade bans, please let us know and we will take action. To file a report, send the following details to **[abuse@irccloud.com](mailto:abuse@irccloud.com)**:

* All usernames, hosts and nicks used by the abuser
* IRC server and channel details where the abuse occured
* Time and date of incident (include your timezone!)
* Excerpt of relevant logs/conversations or other information

### Example Report

Subject: Abuse report for user 123456

This user was spamming in #mychannel on irc.example.com
Here are logs from 10 minutes ago (10 Sept, 3pm GMT)

2:58pm annoyinguser joined #mychannel (uid123456@gateway/web/irccloud.com/x-gdulkwifcaxpoiuq)
2:58pm <annoyinguser> SPAM
2:58pm <annoyinguser> SPAM
2:58pm <annoyinguser> SPAM

... more supporting information ...

How we will respond
-------------------

* We will investigate abuse reports and either warn the user or ban them outright in particularly egregious cases.
* We will not tell you their email address, IP address, or any other personal information.

[API](https://github.com/irccloud/irccloud-tools/wiki/API-Overview) [About](https://www.irccloud.com/about) [Blog](https://blog.irccloud.com/) [Pricing](https://www.irccloud.com/pricing) [Changelog](https://www.irccloud.com/changelog) [FAQ](https://www.irccloud.com/faq) [Jobs](https://www.irccloud.com/jobs)  
[Terms of Service](https://www.irccloud.com/terms) [Privacy Policy](https://www.irccloud.com/privacy) [IP Addresses](https://www.irccloud.com/networks) [Report Abuse](https://www.irccloud.com/abuse)  
[@irccloud](https://twitter.com/irccloud) [team@irccloud.com](mailto:team@irccloud.com)  
Apps:  [iOS](https://itunes.apple.com/app/irccloud/id672699103)  [Android](https://play.google.com/store/apps/details?id=com.irccloud.android)

© 2024 IRCCloud Ltd.