[Skip to main content](#content)

Toggle navigation [![SIP2SIP](../images/sip2sip.svg)](https://sip2sip.info/)

* [Sign In](https://mdns.sipthor.net/sip_settings.phtml)
* [Help](https://sip2sip.info/help/)

[Terms and Conditions](https://sip2sip.info/privacy/)
=====================================================

Contents

* [General](#general)
    
* [Terms of use](#terms-of-use)
    
* [Data Storage Policy](#data-storage-policy)
    
    * [General](#general-1)
        
    * [Accounts](#accounts)
        
    * [Media](#media)
        
    * [Call Detail Records](#call-detail-records)
        
    * [Protection strategies](#protection-strategies)
        

[General](#toc-entry-1)
-----------------------

SIP2SIP is a real time communications service provided by AG Projects, a limited liability company registered in the Netherlands.

The purpose of this service is testing of the software deployed by AG Projects to its customers.

[Terms of use](#toc-entry-2)
----------------------------

You may use this service as an end-user for establishing real time communications with other end-users on the same platform or external users serviced by third parties that are using SIP protocol.

AG Projects reserves the right to remove any account that behaves in an undesirable way.

Usage of accounts provided by this service by intermediaries or corporations deploying services to their own end-users is prohibited. Any party that wishes to deploy their own service must have commercial agreement with AG Projects.

[Data Storage Policy](#toc-entry-3)
-----------------------------------

As a general rule, no end-user's data is collected on purpose nor shared with any third-parties, with the exception of push notifications. However there is data visible or stored implicitely by using the service, due to the inner working of the protocols involved.

If you are concerned about privacy of your data and how it is used inside the platform, read below.

### [General](#toc-entry-4)

When using Internet servers, one should not expect that information remains private. Everything that goes through a server is subject to forces outside the control of the clients using it. You may safely assume all data exchanged through a server is compromised by design. If you care about privacy of your data, you should find clients that reveal as less data as possible, then encrypt all the data that is possible and never share the private key used to encrypt data with anyone. Still, no matter what client technique you are using, it is impossible when using a server to completely hide when communication takes place, between which accounts takes place and the source and destination IP addresses of the end-points.

### [Accounts](#toc-entry-5)

SIP2SIP accounts and related information are stored in the platform database. Passwords are stored in an encrypted form in the database. It is advisable to use strong passwords that cannot be guessed by dictionary brute force attacks.

#### Account deletion

You can request deletion of you account. We will delete your account and its associated data providing that no commercial services has been purchased (e.g. credit to call to PSTN network). If you did make a purchase, we are required by law to keep records of all monetary transactions like full name and addresses for up to seven years after purchase.

To delete your account login to [http://x.sip2sip.info](http://x.sip2sip.info/). In the Identity tab click on the remove account button.

#### Email addresses

Email addresses are solely used for recovering lost passwords or account deletion confirmations.

#### Contacts

The contacts present in your operating system address-book are not share with anyone and remain local to your SIP client.

Contacts used for presence, for example by Blink client, are stored inside the platform XCAP servers.

#### Sessions

Individual SIP messages for session establishment are stored temporary in the platform databases. Both end-users and the platform operator have access to this information for troubleshooting purposes.

#### Registrations

Registration messages are not stored.

#### Subscriptions

Presence dialogs and related payloads are NOT stored.

#### Push notifications

Push notifications used for waking up mobile devices to receive incoming calls or messages are logged temporary for troubleshooting purposes. Apple and Google have a copy of these notifications.

### [Media](#toc-entry-6)

#### Text Messages

Messages sent using SIP MESSAGE method by Sylk client are encrypted end-to-end using PGP, the private key used for decryption is NOT known by the server. The encrypted messages are stored on the server for later retrieval and synchronization between multiple devices. Other devices may send such SIP MESSAGES unencrypted, which may be visible in the logs stored by the servers.

If either client does not suppoort PGP, the messages are stored in clear text.

#### File transfers

Files exchanged by Sylk client are encrypted end-to-end using PGP, the private key used for decryption is NOT known by the server. The encrypted files are stored for a limited time depending on storage availability on the server for later retrieval and synchronization between multiple devices.

If either client does not support PGP, the files are stored unencrypted.

#### RTP Media

RTP streams used for audio and video are relayed by media relays running on the platform. The stream data is not stored.

#### MSRP Media

MSRP sessions used for chat and file transfers are relayed via the platform MSRP relay servers. The content of the messages and files is not stored.

#### Voicemail

Voicemail message can be sent un-encrypted over email as attachments and are stored un-encrypted on the server voicemail server (option controlled by end users). Voicemail can be enabled/disabled for each SIP account.

#### Conferences

Data exchanged during multi-party conferences is not stored.

### [Call Detail Records](#toc-entry-7)

Call Details Records (CDRs) are stored for up to six months. CDRs contain metadata information about who called whom and what time and for how long. The IP addresses used for signaling and media are also stored in the CDRs.

### [Protection strategies](#toc-entry-8)

#### Illegal Intercept

To protect your data against being tapped over the Internet:

* Use `TLS` for SIP signaling (this will encrypt signaling between client and server)
    
* Use `zRTP` for audio and video (Blink and Jitsi clients support `zRTP`)
    
* Use `TLS` for `MSRP` media
    
* Use `OTR` for MSRP media (Blink client supports `OTR`)
    
* Use `PGP` for SIP Messages (Sylk client supports `PGP`)
    

These would protect your data against those who try to illegally sniff your network traffic (like breaking into your LAN/WiFi) but have no access to the client or server software. These measures will not protect your data privacy against legal intercept measures if enforced and applied to the server infrastructure that relays the messages (you will likely not know if and when this happens).

#### Lawful Intercept

In case any entitled government agency requires access to the meta-data stored by SIP2SIP infrastructure, all SIP account data stored on the server can be considered compromised. Use client side encryption to mitigate this risk.

© 2023 [AG Projects](http://ag-projects.com/) — Real Time Communications Experts [Status](https://sip2sip.info/status/) | [Privacy](https://sip2sip.info/privacy/)

![](https://piwik.ag-projects.com/piwik.php?idsite=33)