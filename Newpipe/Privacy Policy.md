The NewPipe project
===================

Privacy Policy
--------------

The NewPipe project aims to provide a private, anonymous experience for using media web services.

We provide some self-hosted services that help us develop NewPipe and the related projects, which require a minimum of personal data to be collected by us. We take your privacy seriously and process the data you provide only for the purposes described below. We promise to notify you about changes, as long as we are able to do so (i.e., we have a way to contact you, for example your e-mail address).

We process and store data based on the EU General Data Protection Regulation (Regulation (EU) 2016/679 of the European Parliament and of the Council of April 2016 in combination with the Directive (EU) 2016/680 of the European Parliament and of the Council of 27 April 2016) law as well as the German Bundesdatenschutzgesetz (short BDSG, a German federal data protection law) in its latest version.

The following document fulfills the requirements of the GDPR Articles 13 and 14, and informs you about the collection and processing of personal data within our project.

All data is stored in a German datacenter, and therefore the data is subject to German law as well as EU law.

Person responsible
------------------

The person responsible for the data collection described in this document is:

Christian Schabesberger  
Dürerstr. 3  
91623 Sachsen b. A.  
[chris.schabesberger@mailbox.org](mailto:chris.schabesberger@mailbox.org)

Data collection on the NewPipe website (including blog with comments and press kit)
-----------------------------------------------------------------------------------

We do not collect any personal data of visitors of the NewPipe website. We do not install cookies on your system, and we do not track our users. Personal data such as the IP address are only processed for the purpose of serving the pages by our webserver software, and are deleted from the memory immediately after the page has been sent to the user.

### Server logs

To have a minimum of control in scenarios where our website is abused, for example denial-of-service attacks, we configured our webserver to create a so-called acces log. This log file contains a list of all requests made to this server, each request in a separate line.

The logged lines contain the following information:

* the IP address that was used to make the request
* a timestamp
* the URL
* the HTTP status code
* the user agent the user‘s browser sends automatically

We need to keep logs of the IP addresses sending requests to our server. As IP addresses are considered personal data and we respect the privacy of our users, we only keep enough of the IP address to be able to able to react to abuse (e.g., DoS and other attacks).  
We calculate prefixes of the IP addresses to anonymize them as follows:

* For IPv4 addresses, we remove the last two bytes to anonymize them. For example, an IP address such as `12.34.56.78` would be logged as `12.34.0.0`.
* For IPv6 addresses, we remove all bytes but the first two. For example, an IP address such as `2001:db8:85a3:8d3:1319:8a2e:370:7344` would be logged as `2001:db8:0:0:0:0:0:0` (short `2001:0db8::`).

We can not identify users from combinations of the other data. Therefore, we consider our log anonymized.

### Comments

The NewPipe blog provides a comment section which can be used to provide feedback for the articles or the project itself. Normal visits don‘t yield any private data.

Users have the ability to leave comments themselves. We use the excellent [isso](https://posativ.org/isso) software to provide this feature.

If a user sends a comment, the following data is collected:

* mandatory data:
    * a name (can, but does not have to be a user's real name), allowing users to let others (including the NewPipe project) identify them, for example on other services, such as GitHub; the name is published next to the user's comment
    * a personal comment
* optional data:
    * an e-mail address, users can enter one if they want the NewPipe project to be able to contact them; it is not published and is not and won't ever be shared with third parties
    * a URL to their homepage, which will be published publicly in the form of a link

In order to fulfill legal constraints, i.e., to help investigating insults and similar criminal acts, we store the IP addresses that were used to create the comments. If we would not store them, we could be prosecuted ourselves.

The IP addresses and the other data are stored permanently.

In order to help users to comment more easily in the future, isso stores the contents of the name, e-mail address and URL fields of the comment form in the user's browser's localStorage. LocalStorage is a browser-side method for storing data persistently, and is bound to a single website. It has been standardized by the World Wide Web Consortium (W3C), and has been published in form of a W3C Recommendation in 2016.

LocalStorage behaves different than the well-known cookies. Unlike cookies, the localStorage's contents are never sent to our servers. We cannot change or copy them. They're only used by isso to fill them into the comment form on future visits. If you do not want isso to store anything in your localStorage, please configure your browser accordingly by either adding an exception for the NewPipe website, or deactivating localStorage completely. So-called "private modes" some browsers provide may also prevent localStorage from being created. Please refer to your browser's manual for details.

Data collection and processing by Sentry, our bug report tracking system
------------------------------------------------------------------------

We maintain an instance of [Sentry](https://docs.sentry.io/), a bug tracking and aggregation system, in order to process user-provided bug reports including crash logs and messages.

We implemented a fully self-hosted bug reporting system that provides a unique level of transparency to the user. When NewPipe crashes on an Android device, the user is shown a dialog containing a summary of the information NewPipe was able to gain about the bug. The user can now opt to send the full details to the NewPipe project in order to allow us to identify and hopefully fix the bug. When a user clicks the send button, NewPipe composes an e-mail via the Android system (i.e., in the configured standard e-mail client) containing the details in a machine-readable format called JSON. JSON is a text-based format, allowing users to read the data and check exactly what data could be sent to us. Users can remove or anonymize data which they do not want to be shared, as long as the JSON format is not broken (in this case, our system can not parse the e-mail any more).

The JSON part contains the following information:

* the e-mail address of the sender
* the type/name of the error
* the URL of the requested page that caused NewPipe to crash
* the language set in NewPipe's settings
* time of the incident (minute accuracy)
* name of the used application
* version of the used application
* operating system name, version and API level (e.g., "Linux Android 4.4.4 - 19")
* the error protocol (stacktrace)

Our bug reporting code is implemented to not embed any personal data in the JSON blob. However, we cannot guarantee that there won't be any personal data contained by accident. Also, we cannot control whether the user will add any personal data to the generated JSON data, nor can we control whether users add personal data outside it. Therefore we tried to implement our bug report system as transparently as possible, allowing the user to entirely control what data is sent. We assume that by sending an actual e-mail to the crash reporting system's address, any personal data is sent on behalf and with consent of the user. We preserve the right to process this data automatically in our Sentry system, the crash report importing software, and accompanying software. We store the data as long as it is needed for analyzations. The e-mails are stored on a self-hosted mail server, and won't be deleted before processing takes place. Often, the raw e-mail data is stored even longer, in order to allow re-imports of the data into Sentry.  
Any additional text in the e-mail that is not part of the JSON section is considered a user comment and will be processed and stored by us as well.

Once the data has been imported, our Sentry system reorganizes the data. Bug reports which Sentry considers similar are aggregated. Sentry is configured to strip any personal data from the bug reports. This can be considered a "last line of defence", and doesn't ensure that no private data is ever collected and stored.

Only a small circle of people has access to the Sentry system. We instruct every user to delete any report which contains personal data as soon as it is discovered. Due to the amount of bug reports we receive every day (varies from a few hundred to a few thousand e-mails every week), we can not check every report for personal data by hand. We ask you to ensure you don't send us any personal data you don't want to share with us. We consider any content in the e-mails to be sent with your consent. You may, at any time, request deletion of the data. Please see below for your rights as a user.

Once an issue discovered by Sentry has been resolved, the reports related to it are archived in the database.

Users' rights
-------------

Every user has the right to request details about the personal data stored about them according to GDPR Art. 15.

Every user has the right to request the correction or completion (GDPR Art. 16) or deletion (GDPR Art. 17) or restriction of use (GDPR Art. 18) of the data sent to us at any time.

In many cases, due to our philosophy, the data is highly anonymized. If your data is, and we think it should be, anonymized so that we cannot associate with any user, we can most likely not delete it from our system. In these cases, however, no personal data is collected. Furthermore, if we cannot verify your identity (e.g., you use another e-mail address to request the deletion of data associated with another e-mail address), we can not delete the data from our systems either.

According to GDPR Art. 77, you may, at any time, file a complaint about our data processing at your local data protection officer.

According to GDPR Art. 7 paragraph 3, you may revoke any consent you gave us about storing and processing data at any time for future time.

According to GDPR Art. 21, you may at any time dissent the processing and storing of data listed in the article.

Note on Data Security
---------------------

All data is stored on a dedicated server administrated by the NewPipe project. Neither the hosting provider nor any other third party does have any access to the data, as it is stored encryptedly on the hard disks using so-called full-disk encryption.

Note on Backups
---------------

On a regular basis, backups of the data are created, and stored encryptedly on the server. After encrypting them, they are stored in different locations in Germany in order to create some redundancy, and allowing restoration in case of failures. The backups are stored up to 6 months, and are then deleted securely from the systems. The encrypted backups are stored as-is on the backup system the hosting provider provides. On systems outside the data center, they are stored with the same full-disk encryption mechanisms that are used to prevent unauthorized access to the raw data on the original server.

Note on Abuse
-------------

The data is processed and stored only for the purposes described above. We will not share any of the data with third parties. The published data is available on the Internet publicly, so that we can not tell whether third parties will copy them unauthorizedly. We want to state that we do not authorize any of these uses. If we should be informed about any unauthorized and illegal uses of our data, we will take appropriate measures to prevent further abuse. We encourage our users to actively help us with this by contacting the person responsible listed in this document immediately. If you wish to, you can use PGP encryption to make sure your message can not be read by anybody but you and the NewPipe team. The PGP key's ID and fingerprint can be found below the details of the person responsible.