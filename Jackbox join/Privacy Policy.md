[Jackbox join](https://jackjoin.vercel.app/)

[ToS](https://jackjoin.vercel.app/tos) [Privacy policy](https://jackjoin.vercel.app/privacy) [Streamer dashboard](https://jackjoin.vercel.app/dash)

Privacy policy
==============

Last Update 23 September 2022

  

This privacy policy describes our policy when it comes to use & disclosure of your information when you use our service.

We use your information to be able to allow [Twitch](https://twitch.tv/) streamers to host their own [Jackbox Games](https://www.jackboxgames.com/) for their viewers with the ability to moderate who is allowed to join and who isn't on the information given to them.

### Contents

* [Definitions](#definitions)
* [Information we collect/store](#collecting)
* [Information we use from Viewers](#infoViewer)
* [Information we use from Twitch streamers](#infoStreamer)
* [Information we use from other visitors](#informationOther)
* [Cookie usage](#cookies)
* [Information we store on Twitch streamer browser](#informationInTwitchStreamer)
* [How we use Twitch scopes](#twitchscopes)
* [Third party services we use](#thirdparty)
* [Do not track signal](#donottrack)
* [How we notify privacy policy changes](#notification)
* [Advertising](#ads)
* [Consumer privacy rights](#consumerRights)
* [Exercising consumer privacy rights](#exercisingRight)  
    * [Right to be forgotten](#rightToBeForgetten)
    * [Access to my information](#accessMyData)
    * [Rectification of my information](#rectification)
    * [Restricting use of my information](#restrictInformation)
    * [Objecting use of my information](#objectingUsage)
* [Appealing decision regarding request consumer privacy rights](#appealingDecision)
* [Child privacy](#childprivacy)
* [Contact us](#contact)

### Definitions

For the purpose of this privacy policy we use the following Definitions

* "**Jackbox Game**": Jackbox Game refers to the games made by [Jackbox Games](https://www.jackboxgames.com/).
* "**Twitch streamer**": Someone that uses our service to be able to moderate who is allowed to join their Jackbox Games.
* "**Viewer**": Someone that would like to join a Twitch streamer's Jackbox Game.
* "**Visitors**": Visitors are those that use this website without being a viewer or Twitch streamer.
* "**Account**": An unique account for someone to access Twitch and our service.
* "**User Id**": An user id is an unique identifier created per account by Twitch existing out of numbers & letters.
* "**Ban evasion**": Ban evasion is when a viewer tries with alternate Twitch accounts to join the same Twitch streamer while earlier accounts were denied/banned.
* "**Following**": Twitch has a feature to follow a Twitch streamer, when you follow a Twitch streamer you get a notification when a Twitch streamer is live again.
* "**Subscription**": Twitch has a feature to be able to subscribe with money to a Twitch streamer for extra features.
* "**Access Token**": When logging in via twitch for this website Twitch generates a token, this token is used to allow our service to be able to make request to Twitch to be able to get information described later in this policy.
* "**Scopes**": Scopes is a permission system by Twitch that allows when logging via Twitch to set permissions this website requests.
* "**CDN**": A cdn or full "content delivery network" is a public service that hosts many javascript/css open source projects.
* "**Javascript**": Javascript is the programming language used for websites.
* "**CSS**": CSS defines how elements on a website should look like.
* "**Webrtc**": Webrtc is a technology that makes communication between devices/browsers possible in a secure manner, more information can be found [here](https://webrtc.org/) and [here](https://developer.mozilla.org/en-US/docs/Web/API/WebRTC_API).
* "**Stun**": Stun is a protocol of webrtc to discover the public networking information of someone, more info can be found here [here](https://developer.mozilla.org/en-US/docs/Web/API/WebRTC_API/Protocols#stun).
* "**Turn**": Turn is a protocol of webrtc that can be used to relay communication between 2 devices/browsers, more info can be found [here](https://developer.mozilla.org/en-US/docs/Web/API/WebRTC_API/Protocols#turn).

### Information we collect/store

We do not collect/store any information on our servers, all information we use from Twitch is only being used while being on our website and while the twitch streamer is on our website.

### Information we use from Viewers

These are all information we gather & use from viewers when using our service. This only applies when being at "/join/{Twitch streamer name}".

* User id: We use the user id requested from Twitch in the following ways.
    * We use your user id to identify you even when having a different username.
    * We use your user id to be able to make request information about you from Twitch.
    * We use your user id to store temporary who the Twitch streamer has denied with a cookie, check "[Cookie usage](#deniedviewer)" for more information.
    * We use your user id to store on the Twitch streamer's browser temporary when they've approved you for the session/stream, check at "[Information we store on Twitch streamer browser](#sessionApproved)" for more information.
    * We use your user id to store on the Twitch streamer's browser when they've approved you to join their Jackbox Games permanently, check at "[Information we store on Twitch streamer browser](#permanentApproved)" for more information.
    * We use your user id to store on the Twitch streamer's browser temporary when they've denied your request to join their Jackbox Game, check at "[Information we store on Twitch streamer browser](#deniedViewers)" for more information.
* Username: We use your username requested from Twitch to be displayed to you and to the Twitch streamer so they know who wants to join their Jackbox Game and if needed take moderation action on Twitch.
* Email address: We use your email requested from Twitch in 3 ways:
    * We encrypt your email address with an 1 way encryption algorithm to be able to detect multiple viewers/accounts using the same email address on the browser of the Twitch streamer.
    * To detect temporary email addresses and to then alert the Twitch streamer about it to be able to prevent possible ban evasion.
    * To detect unknown email domains from unknown email providers to then alert the Twitch streamer about it to be able to prevent possible ban evasion.
* Profile image: The profile image requested from Twitch is used to be displayed to the Twitch streamer together other information about you.
* Account creation date: The Account creation date request from Twitch is used to give an indication of how old your account is to the Twitch streamer.
* Follow information: When you follow a Twitch streamer it's then be used to give an indication for how long you follow them.
* Ip address: Your ip will be encrypted with a 1 way encryption algorithm to then on the Twitch streamer's browser to detect viewers with multiple accounts on the same ip address.
* Subscription information: When you're subscribed to a Twitch streamer a will be displayed next to your name on the Twitch streamer's browser.

### Information we use from Twitch streamers

These are the information we gather and use from Twitch streamers when using our service. This only applies when being at "/dash".

* User id: the user id requested from Twitch isn't displayed but used internally to be able to request information from Twitch.
* Username: We use your username requested from Twitch in 3 ways:
    * To display your name to yourself.
    * To display your username to your viewers on their browsers.
    * To use your username to be able to make a link to allow your viewers to join.
* Followers information: We use follower information requested from Twitch to show you for how long a viewer follows you.
* Subscriptions information: We use subscriptions information requested from twitch to display anext to the viewer name that are subscribed to you via Twitch.
* Bans information: We use ban information requested from Twitch for your Twitch channel to deny viewers that are (temporary) banned access to your Jackbox Games.

### Information we use from other visitors

We do not use any information from you while you're browsing this website while not being a viewer or twitch streamer.

### Cookie usage

We use cookies to temporary store information when you're using our service.

* Twitch access token: The twitch token is used to be able to make request to Twitch on your behalf for the information described at ["Information we use from Viewers"](#infoViewer) or/and ["Information we use from Twitch streamers"](#infoStreamer).  
    This cookie is removed when you leave this website and is only created after login via Twitch.
* Twitch scopes: Twitch scopes are the permissions for the type of information that we're allowed to request from Twitch or are allowed to request action from Twitch, check at "[How we use Twitch scopes](#twitchscopes)" which scopes/permissions we use and why.  
    This cookie is removed when you leave this website and is only created after login via Twitch.
* Viewer bans: When a viewer tries to join but is banned from a Twitch streamer a cookie will be created to prevent the viewer joining again, even with different accounts.  
    This cookie will be saved for max 18 hours on the banned viewer device/browser, if the ban duration is shorter it will be set for the duration of the ban  
    This cookie is created after receiving the ban information from the Twitch streamer's browser.
* Denied viewer: When a viewer is denied by the Twitch streamer a cookie is created to prevent the viewer from joining again.  
    This cookie saved for 8 hours where after it will be deleted.  
    This Cookie is created when receiving information that the viewer was denied from the Twitch streamer's browser.

### Information we store on Twitch streamer browser

We store some information on the Twitch streamer browser for a better experience for the Twitch Streamer and viewers.

* Session approved viewers: When you approve a viewer for the entire session/stream their user id will be stored in your browser until you leave this website.
* Permanent approved viewers: When you approve a viewer permanently their user id will be store permanently in your browser in a [database](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API) under your username.
* Denied viewers: When you deny a viewer their user id will be store in your browser until you leave this website.

### How we use Twitch scopes

Twitch scopes are used to be able to have permissions for when requesting information from Twitch. Here are all scopes we ask permission for and why.

##### Viewer scopes:

* Email: We request the email scope from viewers so that we're able to do the validation described at "[Information we use from Viewers](#vieweremail)".

##### Twitch streamer scopes:

* Sending announcements: We request the "sending announcements" scope to allow you to use a button that will announce the join link to your Twitch chat, the announcement will look like "Join jackbox via https://jackjoin.vercel.app/join/{your Twitch name}".
* Subscribers information: We request this scope to be able to indicate to you which viewers are subscribed to you and which ones aren't.
* Viewing moderation information: We request this scope to be able to request from Twitch viewers you've banned, how we use this info can be found at "[Information we use from Twitch streamers](#baninfo)".

### Third party services we use

We use some third party services to make our service possible.

* [Twitch](https://twitch.tv/): We use Twitch to be able to request information about you. How we use information can be found at "[Information we use from Viewers](#infoViewer)" and "[Information we use from Twitch streamers](https://jackjoin.vercel.app/infoStreamer)".  
    Twitch's privacy policy can be found [here](https://www.twitch.tv/p/en/legal/privacy-notice/).
* [JsDelivr](https://www.jsdelivr.com/): We use JsDelivr as a cdn provider for the many javascript and css projects we use to make our service possible. You can find what we use [here](https://jackjoin.vercel.app/open).  
    JsDelivr's privacy policy can be found [here](https://www.jsdelivr.com/terms/privacy-policy-jsdelivr-net).
* [Peerjs public cloud service](https://peerjs.com/peerserver): We use the Peerjs public cloud service as a [Webrtc signalling service](https://developer.mozilla.org/en-US/docs/Web/API/WebRTC_API/Signaling_and_video_calling#the_signaling_server) to be able to make the connection between Twitch streamer & viewer as easy as possible. Peerjs public cloud service can also be used as a turn service to relay communication.  
    Peerjs public cloud service doesn't have a privacy policy but will only use networking information to be able to make a connection between Twitch streamer & viewer and if needed also relay information between each other.  
    Any privacy question about their service can be asked [here](https://github.com/peers/peerjs/issues) or [here](https://github.com/peers/peerjs-server/issues) by creating an issue/ticket.
* [Nextcloud](https://nextcloud.com/): We use Nextcloud's stun service to be able to discover networking information for both Twitch streamers and viewers.  
    Nextcloud's privacy policy can be found [here](https://nextcloud.com/privacy/).
* [Open relay Stun & Turn servers](https://www.metered.ca/tools/openrelay/): We use open relay Stun & Turn service by [Metered Video](https://www.metered.ca/) to be able discover network information of either a Twitch streamer and/or viewer and if needed also relay communication between each.  
    Metered Video privacy policy can be found [here](https://www.metered.ca/privacy) and information about GDPR can be found [here](https://www.metered.ca/gdpr).

### Do not track signal

Via browsers it's possible to enable a 'do not track' signal, because we do not track you by default this will be ignored.

### How we notify privacy policy changes

If we need to change the privacy policy because of new addition to our service we will notify you with a notification message when you're on our website for at least a month.

### Advertising

At the moment we do not have any advertising on our service, if we do any advertising we will first notify you with a notification + change the privacy policy if needed

### Consumer privacy rights

Below you will be able to find consumer privacy rights, all links will refer to the official hosted consumer privacy rights of an union, country, state or province. If 1 is incorrect or missing please [contact us](#contact).

* European Union + Norway + Liechtenstein + Iceland: [GDPR - General Data Protection Regulation](https://gdpr.eu/tag/chapter-3/)
* United Kingdom: [UK DPA 2018 - United Kingdom Data Protection Act of 2018](https://www.legislation.gov.uk/ukpga/2018/12/part/3/chapter/3/enacted)
* Canada: [PIPEDA - Personal Information Protection and Electronic Documents Act](https://www.priv.gc.ca/en/about-the-opc/publications/guide_ind/) (at "Your rights under PIPEDA" )
* Australia: [Australia privacy act](https://www.oaic.gov.au/privacy/the-privacy-act/rights-and-responsibilities#who-has-rights-under-the-privacy-act)
* Brazil: LGPD - Brazil General Personal Data Protection Law [Brazilian version (at Article 18)](http://www.planalto.gov.br/ccivil_03/_Ato2015-2018/2018/Lei/L13709.htm), [English version by lgpd-brazil.info](https://lgpd-brazil.info/chapter_03/article_18).
* California: [CCPA - California Consumer Privacy Act](https://www.oag.ca.gov/privacy/ccpa)
* Virginia: [VCDPA - Virginia Consumer Data Protection Act](https://law.lis.virginia.gov/vacode/title59.1/chapter53/section59.1-577/) (effective January 1st 2023)

If your union/country/state/province isn't mentioned we will than apply the consumer privacy rights from the [GDPR](https://gdpr.eu/tag/chapter-3/).

### Exercising consumer privacy rights

You can exercise your consumer privacy rights with the ways below. If a right isn't mentioned but you want to exercise it you can always [contact us](#contact).

##### Right to be forgotten

Because we do not store any information about you except for Twitch user IDs from viewers that are [approved permanently by a twitch streamer](#permanentApproved).  
You can remove your user ID from a Twitch streamer by going to ("/join/{twitch streamer name}") when they're playing jackbox, then by clicking on the menu above in the green bar and than clicking on the option "Remove my permanent information and leave", This will remove your user ID from the Twitch streamer's device and will then send you to the home page of this website.  
You can also have your information be removed from Twitch by clicking by making a ticket [here](https://help.twitch.tv/s/contactsupport).

##### Access to my information

When you're at "/join/{Twitch streamer name}" or "/dash" you can click on the menu button in the green bar above the page and then click on "Information used from me", this will let you see all information we use from you. Don't let someone else see your information!

##### Rectification of my information

You can rectify your information from Twitch at your Twitch profile settings [here](https://www.twitch.tv/settings/profile) or by making a ticket to Twitch [here](https://help.twitch.tv/s/contactsupport).

##### Restricting use of my information

Restricting of the information we use of you is not possible, we use the minimal amount of information to be able to have our service functional.

##### Objecting use of my information

If you don't want our service to use your information anymore. You can revoke the agreement on the terms of service and \[rivacy policy by pressing on the button below.  
You can also disconnect our connection to your twitch account, you can do that [here](https://www.twitch.tv/settings/connections) under "Other Connections" at "Jackbox join".

Revoke agreement to ToS and Privacy Policy

### Appealing decision regarding request consumer privacy rights

You can appeal our decision by replying to our decision or by [contacting us](#contact) again.

### Child privacy

**CHILDREN UNDER THE AGE OF 13 ARE NOT ALLOWED TO USE OUR SERVICE IN ANY MANNER!**  
We do not knowingly use any information from children. If you're a parent or legal guardian of a child that uses our service and Twitch please email Twitch at [privacy@twitch.tv](mailto:privacy@twitch.tv) so that your child's information can be removed as quickly as possible.  
If you're a Twitch streamer and you think a viewer is a child under the age of 13 please do also mail at [privacy@twitch.tv](mailto:privacy@twitch.tv).

### Contact us

We're only available via email. Below you can find our email addresses and for which purpose

* Exercising consumer privacy rights: [jackjoin+privacyrights@proton.me](mailto:jackjoin+privacyrights@proton.me)
* Questions about privacy policy or missing things: [jackjoin+privacypolicy@proton.me](mailto:jackjoin+privacypolicy@proton.me)
* For any other legal basis regarding our service: [jackjoin+legal@proton.me](mailto:jackjoin+legal@proton.me)
* Questions that aren't about the privacy policy: [jackjoin+question@proton.me](mailto:jackjoin+question@proton.me)
* For any feedback: [jackjoin+feedback@proton.me](mailto:jackjoin+feedback@proton.me)

**Notice:** Emails not related to our service or is spam will be ignored, deleted and if needed the email address will be blocked!