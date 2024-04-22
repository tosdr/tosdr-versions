[![](/img/white-logo.png)](https://www.anoni.cloud/it/)

* [Perché AnoniCloud](https://www.anoni.cloud/it/#whyAnonicloud)
* [Filosofia](https://www.anoni.cloud/it/#philosophy)
* [Download](https://www.anoni.cloud/it/download)
* [Aiutaci](https://www.anoni.cloud/it/supportus)
* [FAQ](https://www.anoni.cloud/it/faq)
* [Blog](https://www.anoni.cloud/blog)
* [Ita](#)
    
    [Deutsch](https://www.anoni.cloud/de/privacy) [English](https://www.anoni.cloud/en/privacy) [Italiano](https://www.anoni.cloud/it/privacy) [Português](https://www.anoni.cloud/pt/privacy) [Română](https://www.anoni.cloud/ro/privacy)
    

Privacy policy and technical details
====================================

Rev. 12 June 2020

Purpose of the service
----------------------

AnoniCloud is a service aiming to store user's document in the best confidential way, using zero-knowledge encryption, state of art encryption algorithm avoiding decryption of data also with quantum computers.

Service stage
-------------

AnoniCloud is _actually_ in public beta stage. Before going on production stage, all security assessment on machines and protocol has to be performed by AnoniCloud team and / or its consultants.  
User's are kindly invited to use the service, provide a feedback on their experience and don't store any sensitive data.

_At this stage we decline any responsibility for sensitive data disclosure._

Service philosophy
------------------

AnoniCloud is a software conceived sittings on three _technical_ pillars:

* 1\. Anonymity

* The user is not required to provide any personal data, like email, telephone number, real name and surname, to access the service;
* user's identity is determined by the system by means of a "username" that is a string of ASCII printable characters, maximum 255 character long and a "password" a string of ASCII printable characters, maximum 255 character long;
* Over the "username" a user's UUID is generated and used internally by the server system to link user's account and user's data; the "username" is the only data stored as-is into our system;
* The "password" is never sent over the net: Before leaving the user's device, the password, by means of SRP-6a ([Secure Remote Password protocol](http://srp.stanford.edu/)), is used to generate two data (a SALT and a VERIFIER) both stored on the server; by means of them, is actually impossible to revert the original password.

* 2\. Inviolability

* User's documents are divided in chunks and encrypted by means of a document encryption key before leaving the user's device; the encryption algorithm used is AES-256-CBC; to perform encryption and decryption operation the password is temporarily stored on user's device and is used to encrypt and decrypt the document key; once again the original user's password is not known by AnoniCloud and we're not able to recover's original user's documents content;
* Informations over the network are two-layers encrypted: first layer, chunk level encryption and second layer, https traffic encryption;
* All communications between client and server are signed with an ephemeral key, valid and rotated every five minutes; at the expiration, a new key is negotiated; the signing key is never sent over the net.

* 3\. Integrity

* The checksum (technically a SHA256-treehash) of each document is stored on document's metadata; the metadata are encrypted in the same way of the user's document; because of this, they are not readable by us; comparing the stored checksum with the locally calculated when retrieving the document, any alteration in content respect to the original is promptly underlined.

Considering the three points above, AnoniCloud team is not able to access any user's data.

Data storage location
---------------------

All data are stored in Switzerland.

What data are stored
--------------------

1. User's encrypted document - See "Service philosophy" - Not accessible by AnoniCloud team;
2. User's access data - Scrambled by SRP-6a - Not accessible by AnoniCloud team;
3. Limiting to the public beta phase, all user's source IPs and server diagnostic are stored in clear and accessible by AnoniCloud team;
4. User's feedback, support requests email are stored in clear and are used to provide requested support to user and improve our service; these data will be not sent outside AnoniCloud team.

Application log and telemetry
-----------------------------

For product throubleshooting anonymous log data are collected inside each app belonging to AnoniCloud ecosystem; the sending of the log data to AnoniCloud is explicitely triggered by the user. Application log are sent to AnoniCloud via email.

Application log can contains device tecnical informations like operating system version running on device, device model and informations about the battery.

No realtime telemetry is performed on device by AnoniCloud.

Data Processed by Third Parties
-------------------------------

No user's data are processed by third parties.

Data erasure
------------

The user has the full right to erase partly or all his data; as "erasure" we intend the complete data removal without the technical possibility to recover them once deleted. On AnoniCloud app a "Document delete" function and a "Delete user's profile" are available to wipe out partly or all user's data from AnoniCloud server.

About our website
-----------------

No tracking cookies are stored on user's browser starting from our website.

Website is split in two parts:

1. Presentation, corporate informations;
2. Blog.

**Presentation and corporate informations** don't store any cookie. Is a static tailor made website based on Bootstrap 4 and is built to avoid any informations loading from external CDN (Content Delivery Network). Anonymized IP address (last three digit hidden) is stored on our _Open Web Analytics_ (_OWA_ for short) database for statistical purposes. OWA runs on our webserver.

More informations on OWA: [Open Web Analytics official website.](http://www.openwebanalytics.com/)

**Blog** run under WordPress with security and statistical plugins; anonymized (hashed) IP addresses are collected for statistical purposes. Language preferences cookie and session cookies are installed on user's browser; data stored on cookies are scrambled directly by WordPress engine.

Questions and feedback reference
--------------------------------

Questions and feedback from users are welcome and can be addressed at: [contact@anonicloud.ch](mailto:contact@anonicloud.ch).

Responsible body and direct contact for data protection topics:

Francesco Piraneo Giuliano  
Pusgiort 20  
6835 Breggia  
Switzerland

Amendment of the privacy policy
-------------------------------

We reserve the right to change this Privacy Policy from time to time in order to comply with changed legal requirements or to reflect new functionalities of the app. The current Privacy Policy is always available for consultation from within AnoniCloud website.

![](/img/white-logo.png)

6835 Morbio Superiore  
Switzerland

**Scriveteci!**  
[contact@anoni.cloud](mailto:contact@anoni.cloud)  
...oppure usa **[Threema](https://threema.id/C5SZC992)**!

Il mondo di AnoniCloud:

|     |     |
| --- | --- |
| [Perché AnoniCloud](https://www.anoni.cloud/it/#whyAnonicloud) | [Aiutaci](https://www.anoni.cloud/it/supportus) |
| [Filosofia](https://www.anoni.cloud/it/#philosophy) | [FAQ](https://www.anoni.cloud/it/faq) |
| [Download](https://www.anoni.cloud/it/download) | [Privacy policy](https://www.anoni.cloud/it/privacy) |
| [Blog](https://www.anoni.cloud/blog) | [Credits](https://www.anoni.cloud/it/credits) |

I nostri social

[![](/img/social/facebook-white.png)](https://www.facebook.com/anonicloud/) [![](/img/social/x-white.png)](https://twitter.com/anonicloudch) [![](/img/social/linkedin-white.png)](https://www.linkedin.com/company/anonicloud/) [![](/img/social/threema-white.png)](https://threema.id/C5SZC992)