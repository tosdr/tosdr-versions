Privacy Policy _Last updated 10th December 2024_

Table of Contents

[Introduction](#Introduction) [Data collection](#Data-collection) [IP Addresses and User Agents](#IP-Addresses-and-User-Agents) [Cookies](#Cookies) [Username and password](#Username-and-password) [Data retention](#Data-retention) [Data sharing](#Data-sharing) [Exceptions](#Exceptions) [qam - qwik account manager](#qam---qwik-account-manager) [XMPP](#XMPP) [Gitea](#Gitea) [Hedgedoc](#Hedgedoc) [Libreddit](#Libreddit) [Recommendations](#Recommendations)

Introduction
============

We want to keep this short but informative, but a _tl;dr:_

We try to collect as little data as possible. We do this by, for example, keeping logs of sensitive data (such as IPs and user agents) to a minimum. We collect a username and a password (which is _salted_ and _hashed_), and then any data published or uploaded to any of the services we provide.

We will change this Privacy Policy from time to time to reflect the current situation. Please keep an eye out. For bigger changes we **might** send out some form of notice.

This policy is somewhat general, so there might be exceptions for individual services. We will list said exceptions further down the privacy policy.

Data collection
===============

IP Addresses and User Agents
----------------------------

We do not keep access logs - so we can't see who has connected. However, our server uses modsecurity to protect against different types of attacks. Most of the time the modsecurity audit log is disabled, meaning it doesn't log anything. However, we might enable it for short periods of time for debugging purposes, after which we would disable and clear the log. Modsecurity logs may contain IP addesses or user agents!

Cookies
-------

Our main page ([qwik.space](https://qwik.space/)) does not have any cookies.

Username and password
---------------------

We will require a username (which could be considered sensitive and/or private and/or personally identfiable). Other users will be able to see your username.

Your password is salted and hashed. (This generally means your password is safe, as long as it is strong enough.)

Data retention
==============

The modsecurity log, when enabled, should be cleared after any debugging is done. We also keep your registration details (username) and published content until you either delete what you can yourself and/or tell us to remove it. (If you want to delete your **entire account** please ask for help, since you can't do that by yourself.)

Data sharing
============

We do not share any data with third parties unless we have to by law or state otherwise.

Exceptions
==========

Here are some services that make exceptions to the above statements:

qam - qwik account manager
--------------------------

Our account manager, _qam (qwik account manager)_ uses a cookie when signing in that keeps an API-token.

All services we provide use the same username and password as you specify in _qam_. All services that we provide will use a _mock/fake email address_ (`username`@qwik.space or `username`@localhost) if they require one.

XMPP
----

Our XMPP server caches messages and uploads for up to seven days. If your client uses encryption (such as OMEMO) the cached messages and uploads will be encrypted. We **strongly** advise using encryption.

Gitea
-----

Gitea also uses some cookies, but this is for your comfort. For example keeping you signed in and remembering your settings or what not.

Hedgedoc
--------

The documents you write will be stored unecrypted. This also applies to image uploads.

Hedgedoc also uses some cookies, they will be used to keeping you signed in and remembering your settings.

Libreddit
---------

These services all use cookies to remember your settings.

Recommendations
===============

**The internet is not a good place when it comes to privacy**. If you want to limit the risks of something or someone invading your privacy online, we recommend:

* Use Tor (properly)
* Use throwaway emails when signing up for stuff
* Use fake names or aliases to protect your name
* (Generally) don't give out personal information online...