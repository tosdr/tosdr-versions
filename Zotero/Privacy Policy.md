[![Zotero](/static/images/theme/zotero-logo.1519224037.svg)](https://www.zotero.org/)
=====================================================================================

[Log In](https://www.zotero.org/user/login/) [Register](https://www.zotero.org/user/register)

 [![](/static/images/theme/archive.png) Upgrade Storage](https://www.zotero.org/storage)

* [Home](https://www.zotero.org/)
* [Groups](https://www.zotero.org/groups/)
* [Documentation](https://www.zotero.org/support/)
* [Forums](https://forums.zotero.org/categories/)
* [Get Involved](https://www.zotero.org/getinvolved/)

 

You are here: [start](https://www.zotero.org/support/start "start") > [privacy](https://www.zotero.org/support/privacy "privacy")

Zotero Privacy Policy
=====================

Overview
--------

Zotero is an open-source project committed to providing the best tool for managing your research. Our philosophy is that what you put into Zotero is yours, and one of our founding principles is to make sure you remain in control of your data and can share it how you like — or choose not to share it at all.

**We are an independent, nonprofit organization and have no financial interest in your private information.** We fund further development by offering additional online storage space to people who find the software useful, not by selling data.

Data We Collect
---------------

Zotero is designed as a local program that saves data to your own computer by default, and it doesn’t require sharing any data with us to be usable. However, some of Zotero’s advanced features require you to supply us with information.

* We collect the information you voluntarily provide (e.g., your name and email address) if you create a Zotero account and use optional Zotero services. Zotero can be used without creating an account.
    
* We collect the library data you upload if you choose to synchronize your library with the Zotero servers. Syncing is entirely optional and is disabled by default.
    
* We collect the attachment files you upload if you choose to use Zotero file syncing. File syncing is optional, and you can choose to sync files in your personal library using a WebDAV server instead.
    
* We keep a record of the most recent IP addresses used to access your synchronized library in order to let you verify the security of your account and allow you to [revoke access](https://www.zotero.org/settings/keys "/settings/keys") in your Zotero settings.
    
* We log visits to our website, including IP address and browser, in order to prevent abuse and to diagnose technical issues. We retain these access logs for 90 days.
    
* We log requests made to our servers by Zotero or third-party software, including IP address and client information, in order to prevent abuse, diagnose technical issues, and assess usage. We retain these logs for up to 90 days. You can [opt out](#disabling_automatic_requests "privacy ↵") of all requests to our servers.
    
* We collect error reports that you submit. See [Support Interactions](#support_interactions "privacy ↵").
    
* If you attempt to save something to Zotero and the save fails, we collect information about the failure, including the URL, browser, and version information, so that we can more quickly fix site compatibility issues. We store this information for up to one week. No additional personally identifying information (e.g., username or IP address) is stored, and reports are generally only viewed in aggregate. This error reporting can be disabled in the Zotero and Zotero Connector preferences.
    

Library Statistics
------------------

Zotero anonymizes and aggregates synchronized user and group library data to generate statistics on readership. This anonymized and aggregated data only includes publicly available metadata (e.g., publication title and author). This data is never sold or made available in any forms other than ones offered publicly. We may also use this anonymized and aggregated user information for auditing, research, and analysis to operate and improve Zotero services.

Security of Stored Data
-----------------------

See [Security of Zotero Data](https://www.zotero.org/support/security "security").

Disabling Automatic Requests
----------------------------

You can disable all automatic communication with Zotero servers from the Zotero and Zotero Connector preferences:

* **Syncing:** Sync preferences → leave unconfigured or disable automatic syncing
    
* **Automatic PDF metadata retrieval:** General preferences → disable “Automatically retrieve metadata for PDFs”
    
    * We do not log any information about the contents of PDF metadata requests.
        
* **Open-access PDF retrieval:** General preferences → disable “Automatically attach associated PDFs and other files when saving items”
    
    * If a PDF can't be saved for an item with a DOI, Zotero will send the DOI to Zotero servers to check for open-access versions. We do not log the contents of these requests. Disabling this preference will disable all automatic attachment saving.
        
* **Broken site translator reporting:** disable “Report broken site translators” in the Advanced pane of Zotero and the Zotero Connector
    
* **Translator/style update checking:** Advanced preferences → disable “Automatically check for updated translators and styles”
    
* **Zotero update checking:** Advanced preferences → Config Editor → set `app.update.auto` to false
    
    * Automatic update checking is strongly recommended for security and stability reasons.
        
* **Retracted item checking:** Advanced preferences → Config Editor → set `retractions.enabled` to false
    
    * Retraction checks are performed [without sharing](https://www.zotero.org/blog/retracted-item-notifications/#designed-for-privacy "/blog/retracted-item-notifications/#designed-for-privacy") the items you have in your database.
        
* **Proxy authentication checking:** Advanced → Config Editor → set `extensions.zotero.triggerProxyAuthentication` to false.
    
    * At Zotero startup, HEAD requests are made to a test file on Amazon S3 and selected publisher websites (controlled by `extensions.zotero.proxyAuthenticationURLs`) to trigger a proxy authentication prompt if and only if Zotero detects that a proxy is required to connect to the internet. If you disable this option and require an authenticated proxy, Zotero network connections will fail.
        

If automatic syncing or automatic translator/style updates are enabled, Zotero will maintain a persistent connection to Zotero servers when it is open in order to provide immediate updates. You can disable this connection by disabling both of those options or by setting `extensions.zotero.streaming.enabled` to false in the Config Editor.

If you use the Zotero Connector without having Zotero open, the Connector will make a daily request to Zotero servers for information on available site translators. It will then download translators for the sites you visit. For example, if you load a _New York Times_ article, the Connector will download Zotero’s _New York Times_ translator and cache it. If Zotero doesn’t have a translator for a specific site, no request will be made. No information on the specific pages you visit is transmitted, and subsequent requests won’t be made for the same translator until you restart your browser or the translator is updated. You can avoid these requests by keeping Zotero open while you browse the web.

Permissions Warnings
--------------------

When using third-party platforms, we request the most restrictive permissions available that still allow Zotero to perform its advertised functions. In some cases, the necessary permissions can sound a bit scary, so we want to explain why they’re necessary.

### Zotero Connector

When installing the Zotero Connector, your browser will warn you that the extension can “Read your browsing history”, “Access your data for all websites”, or similar. These different wordings all mean the same thing: that Zotero can interact with each page as you browse the web. This is the standard permission that browser extensions that run on all pages require. Zotero uses it to determine what content it can save on a given page and update the save button accordingly, as well as to provide advanced features such as automatic proxy redirection and automatic RIS/BibTeX import. Zotero in no way reads your previous browsing history, and no data about your browsing activity is stored except when you choose to save a page to either your local or online Zotero library.

### Google Docs Integration

When you first use Google Docs integration, Google will ask you to grant Zotero Google Docs Integration permission to “See, edit, create, and delete all your Google Docs documents”. The plugin requires this permission to insert citations into your documents. The plugin doesn’t do anything else with your document content and doesn’t access documents other than the ones on which it’s triggered. The integration works entirely locally on your computer, so even when you trigger the plugin on a given document, nothing is sent to Zotero servers.

Storage Purchases
-----------------

We send two pieces of personal data to our payment processor at the time of purchase:

* your Zotero username, in order to associate your payment with your Zotero account
    
* your email address, so that the payment processor can send you a payment receipt
    

Zotero does not collect or store your credit card, banking, or other payment information. When you enter your full name, billing address, and account numbers to complete a Zotero purchase, this information passes directly to our payment processor, and it never touches Zotero servers.

Support Interactions
--------------------

Most Zotero support occurs in the public Zotero Forums. If you would like to remove forum posts you have made, you may clear them yourself at any time, though we encourage you to leave your posts up for the benefit of others. If you’d prefer your forum posts to appear under a different name, you can change your forums username from your account settings.

You may be asked to submit an error report or debug output to help us troubleshoot problems. These reports contain technical information about your computer, such as your operating system and installed browser extensions, and may include incidental personal information such as URLs of sites you visited before or while generating the report. You can review the output of these reports before submitting them. We don’t store any personal information (username, IP address) that links the report to you, and we generally don’t look at reports unless they are referenced by a Report ID or Debug ID in the Zotero Forums. Reports are stored for up to one year.

If you email us, we collect your email address and any other information you provide, and we may store your messages indefinitely to provide context for any future support requests you make.

Third-Party Services Used
-------------------------

* All Zotero server data is stored in the United States in Amazon Web Services. See [Security of Zotero Data](https://www.zotero.org/support/security "security") for more information.
    
* Certain operations you perform in Zotero may trigger requests to public third-party services such as Crossref or the Library of Congress for metadata retrieval. These third parties may log your IP address and search terms (e.g., DOI or ISBN) according to their privacy policies, but no other identifying information is provided.
    
* When you save items to or update items in Zotero, Zotero may, depending on your settings, connect to the associated sites to download metadata or save PDFs or snapshots. This is equivalent to loading those sites in your browser, and similar privacy implications apply. See [Zotero and Firewalls](https://www.zotero.org/support/kb/zotero_and_firewalls "kb:zotero_and_firewalls") for access requirements.
    
* Some fonts on Zotero’s websites are licensed from myfonts.com. In order to verify Zotero’s compliance with this license, myfonts.com collects your IP address and the URL of the accessed Zotero webpage.
    
* When an account is registered, we use Google reCAPTCHA to verify that it is not an automated registration attempt.
    
* Payment processing is provided by [Stripe](https://stripe.com/ "https://stripe.com").
    
* When buyers are unable to use Stripe, we process payments with [PayPal](https://www.paypal.com/ "https://www.paypal.com").
    
* Additional accounting services use [Anrok](https://www.anrok.com/ "https://www.anrok.com/").
    

Deleting Your Data
------------------

You may delete your Zotero account to remove information you voluntarily provided when you registered to use Zotero services and to remove the library data you provided if you chose to synchronize your library with Zotero servers. To delete your account, visit your [Zotero settings](https://www.zotero.org/settings/security#delete "/settings/security#delete") and click “Permanently Delete Account”.

Backed-up Data
--------------

We make regular automated backups of data on our servers to protect against accidental loss of user data. These backups are intended for disaster recovery and would be accessed only in the event of significant data loss. Backups may be retained for up to 6 months.

Legally Compelled Disclosure
----------------------------

We may be legally required to comply with requests for data from law enforcement or government agencies.

Changes
-------

We may update our privacy policies over time. Up-to-date information, including details of new features, will always be available from this page.

Questions
---------

If you have any questions or concerns regarding Zotero’s privacy policies, please ask us in the [Zotero Forums](https://forums.zotero.org/ "https://forums.zotero.org") or email [privacy@zotero.org](mailto:mailto:privacy@zotero.org "mailto:privacy@zotero.org").

### Table of Contents

* [Zotero Privacy Policy](#zotero_privacy_policy)
    
    * [Overview](#overview)
        
    * [Data We Collect](#data_we_collect)
        
    * [Library Statistics](#library_statistics)
        
    * [Security of Stored Data](#security_of_stored_data)
        
    * [Disabling Automatic Requests](#disabling_automatic_requests)
        
    * [Permissions Warnings](#permissions_warnings)
        
        * [Zotero Connector](#zotero_connector)
            
        * [Google Docs Integration](#google_docs_integration)
            
    * [Storage Purchases](#storage_purchases)
        
    * [Support Interactions](#support_interactions)
        
    * [Third-Party Services Used](#third-party_services_used)
        
    * [Deleting Your Data](#deleting_your_data)
        
    * [Backed-up Data](#backed-up_data)
        
    * [Legally Compelled Disclosure](#legally_compelled_disclosure)
        
    * [Changes](#changes)
        
    * [Questions](#questions)
        

privacy.txt · Last modified: 2024/09/10 14:11 by fcheslack

* [Old revisions](https://www.zotero.org/support/privacy?do=revisions "Old revisions [o]")

![](/support/lib/exe/taskrunner.php?id=privacy&1732012809)

* [Blog](https://www.zotero.org/blog/)
* [Forums](https://forums.zotero.org/categories/)
* [Developers](https://www.zotero.org/support/dev/start)
* [Support](https://www.zotero.org/support/)
* [Privacy](https://www.zotero.org/support/privacy)
* [Get Involved](https://www.zotero.org/getinvolved/)
* [Jobs](https://www.zotero.org/jobs)
* [About](https://www.zotero.org/about/)

Zotero is a project of the [Corporation for Digital Scholarship](http://digitalscholar.org/), a nonprofit organization dedicated to the development of software and services for researchers and cultural heritage institutions, and is developed by a [global community](https://www.zotero.org/support/credits_and_acknowledgments).