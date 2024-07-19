LAST UPDATED May 14, 2024

Brave Browser Privacy Policy
============================

_Our company does not store any record of people’s browsing history. We don’t write any personal data to the blockchain. The only way a user’s data is stored by Brave is if the user has switched on Rewards or Sync._

Read this document to understand how the Brave Browser uses data.

To learn how we use data to operate our websites, forums, and communications, visit the [Website Privacy Policy](https://brave.com/privacy/website/). To learn how we use data for publishers and creators visit the [Publisher Privacy Policy](https://brave.com/privacy/publishers-creators/) on the Basic Attention Token website.

In this policy “we”, “us”, etc. refers to Brave Software Inc, while “Brave” refers to the browser.

Security & updates[](#updates "Permalink to this headline")
-----------------------------------------------------------

Brave automatically checks with us for updates. This ensures that you always have access to the latest security fixes. We count the number and type of these requests when we receive them to produce aggregate statistics. No particular person’s information can be identified in the statistics we produce.

You can also update to the latest version [here](https://brave.com/download/).

### Safe Browsing[](#safe-browsing "Permalink to this headline")

The Brave Browser automatically uses Google Safe Browsing to help protect you against websites, downloads and extensions that are known to be unsafe (such as sites that are fraudulent or that host malware). On desktop, we use the Safe Browsing [Update API](https://developers.google.com/safe-browsing/v4/update-api) which relies on storing URL hashes locally on your device. We proxy these requests through Brave’s servers to reduce the amount of information sent to Google (for example, we remove your IP address) to protect against Google profiling or tracking you when using Safe Browsing. On iOS, Apple proxies Google Safe Browsing through their own servers. For iOS users in mainland China, Apple may also use the Tencent Safe Browsing service. More details at [https://www.apple.com/legal/privacy/data/en/safari/](https://www.apple.com/legal/privacy/data/en/safari/). On Android, we use the [SafetyNet Safe Browsing API](https://developer.android.com/training/safetynet/safebrowsing) which sends partial URL hashes directly to Google when a URL is determined to be potentially malicious by the list stored locally on your device, as per the Safe Browsing Update API.

If you prefer not to use Safe Browsing, just visit `brave://settings/security` to change your settings to “No protection (not recommended)”. On iOS, open “Brave Shields & Privacy” inside settings and disable “Block Dangerous Sites”. On Android, open “Brave Shields & privacy” inside settings and then set the Safe Browsing option to “No protection (not recommended)”.

Sync[](#sync "Permalink to this headline")
------------------------------------------

If you switch on Sync then your bookmarks (and soon passwords and other data) will be saved in an encrypted file on a cloud storage service, to which you will have the only decryption key. The data[1](#fn:1) are entirely inaccessible to Brave and to the cloud storage provider. [Learn how](https://support.brave.com/hc/en-us/articles/360021218111-How-do-I-set-up-Sync-) to switch on Sync here.

Unused Sync chains expire after 12 months and the associated server data is permanently deleted.

Location[](#location "Permalink to this headline")
--------------------------------------------------

If you use Brave to visit a website that wants to determine your location, you will be asked whether you want it to be allowed to know where you are. If you click yes to this message, then the website will be sent an approximation of where you are based on your IP address. Your IP address will not be stored by Brave, but it may be stored by the website you have visited. [See data processing details](#table-location).

Brave Rewards[](#rewards "Permalink to this headline")
------------------------------------------------------

If you enable [Brave Rewards](https://brave.com/brave-rewards/), we assign your Brave browser a “Rewards Payment ID”, which is used to account for Basic Attention Token ([BAT](https://brave.com/brave-rewards/)) rewards you may earn for seeing [Brave Private Ads](https://brave.com/brave-ads/). We will also ask you to select your country, which we will use to assign a country code to your Rewards Payment ID. The country code helps us ensure Ads are displayed to individuals depending on their country. We will also use the country code to help us prevent fraud. You can find your Rewards Payment ID by navigating to brave://rewards-internals.

Even with Brave Rewards enabled and a Rewards Payment ID assigned, we never collect your browsing history or similar information, and we can’t derive this information from your contributions to content creators or sites. We also [cannot tell which specific Brave Private Ads you’ve seen or interacted with](https://github.com/brave/brave-browser/wiki/Security-and-privacy-model-for-ad-confirmations).

Note that we record the identifiers mentioned herein on servers located in the United States. We take a range of technical and organisational measures to safeguard personal data.

### Connecting a custodial account[](#connecting-a-custodial-account "Permalink to this headline")

When you choose to connect a custodial account to Brave Rewards using one of our custodial partners such as [Uphold](https://uphold.com/), [Gemini](https://www.gemini.com/), [bitFlyer](https://bitflyer.com/) (Japan only), or [ZebPay](https://zebpay.com/) (India only), three things become associated with your Rewards Payment ID: a custodian ID, deposit address(es), and a country code. All three are assigned by the custodial partner. The deposit address allows us to make deposits to your custodial account, while the country code helps us prevent fraud and limit service to users in countries where Brave Rewards is supported. In addition, we also use IP addresses and Rewards Payment IDs associated with monthly BAT payments to safeguard against fraud. See the [Brave Rewards data processing table](#rewards-detail)

When you make an on-demand contribution to Brave Creators using BAT from your linked custodial account(s), the custodian can see and record the details of your contribution transactions (such as, but not limited to, the amount and the recipient). This is subject to the privacy policies of [Uphold](https://uphold.com/legal/privacy-policy), [Gemini](https://www.gemini.com/legal/privacy-policy), [bitFlyer](https://bitflyer.com/), or [ZebPay](https://zebpay.com/legal-privacy#privacy-policy). However, when using the [Auto-Contribute](https://support.brave.com/hc/en-us/articles/360027276731-Brave-Rewards-FAQ) feature to support Brave creators with BAT from your custodial account, [neither Brave nor your custodian can tell which specific creators you’re contributing to](https://github.com/brave/brave-browser/wiki/Security-and-privacy-model-for-rewards-auto-contribute).

### Connecting a self-custody account[](#connecting-a-self-custody-account "Permalink to this headline")

When you choose to connect a self-custody account/address (such as a Solana address), your Rewards Payment ID will be associated with your self-custody address. See the [Brave Rewards data processing table](#rewards-detail) for details of what data we process and why and for how long.

_Cookies:_ As part of the process to connect your Solana address to your Rewards Payment ID, a temporary, security-related cookie will be set in your browser for one of our Rewards-related service domains. The purpose of this cookie is to protect you against cross-site forgery attacks during the connection process. The moment the cookie is done playing its role in the connection process, the cookie is immediately cleared from your browser.

Ads[](#ads "Permalink to this headline")
----------------------------------------

If you switch on Brave Rewards we automatically enable Brave Ads. This means you will receive ads in the form of notifications and in-browser sponsored content, and Basic Attention Tokens to reward you for viewing those ads. While the categories of ads that you see and when you see them are inferred from your browsing activity, the data are stored on your device and are inaccessible to us. We will receive anonymized confirmations for ads that you have viewed, but no data that identifies you or that can be linked to you as an individual leaves the Brave browser on your device. You can disable Ads by visiting `Settings > Brave Rewards > Ads` and turning off the Ads default.

In the cases where we collect high-level statistics relating to web activity data (e.g. what are the estimated amount of ads that can be served to different content categories that users encounter as they browse the web) we use proven privacy mechanisms like local differential privacy that guarantee that no information about individual users will ever be revealed to us. Read more about how we achieve this with [Privacy Preserving Product Analytics](https://brave.com/privacy/browser/#privacy-preserving-product-analytics) and [Private Advertising Analytics](https://github.com/brave/brave-browser/wiki/Randomized-Response-for-Private-Advertising-Analytics). To read more about Brave Ads and privacy have a look at our [FAQ](https://support.brave.com/hc/en-us/articles/360026361072-Brave-Ads-FAQ).

Brave conducts A/B testing to support research into user engagement with Brave Ads to inform our strategy for choosing and displaying Ads to end-users. We use variables such as type of Ad, placement and timing. This is done in a way that protects end-user privacy - we cannot link data to individuals or their devices and nor can we identify users or their devices from the research.

Brave Wallet[](#brave-wallet "Permalink to this headline")
----------------------------------------------------------

The Brave Wallet is a secure crypto wallet built directly into the Brave browser. You can buy, send, store, and swap thousands of assets (and NFTs) seamlessly on 100+ blockchain networks including Ethereum, Solana, Filecoin, and more. You can learn more about ‘crypto wallets’ and the Brave Wallet [here](https://brave.com/wallet/)

Brave does not track any of the actions you make in your wallet. We strive to put privacy first:

* Brave proxies and strips the IP address associated with access to the Brave Wallet.
* When you make a transaction using a third party that redirects you to their services, such as an on-ramp partner, they will capture your IP address and may conduct identity verification checks in order to meet obligations they have under sanctions and anti-money laundering laws. You should review the privacy notices and terms of service of those third parties.
* We use Decentralised Exchange Aggregators (DEX) such as [0x](https://www.0x.org/about/mission) for swaps made on EVM compatible blockchains and [Jupiter](https://jup.ag/) for swaps completed on the Solana blockchain. They will also process your wallet address, related transaction data and your IP address but will ONLY use this data to fulfil the transaction (including getting a quote).
* We will use anonymized and aggregated statistics from on-ramp partners that include regional volumes of transactions, including daily number of transactions by token/chain; daily $ volume of transactions by token/chain; monthly unique transactions by token/chain. We use this statistical data to understand at a high level which cryptocurrency assets are being used and on which platforms.

Brave News[](#brave-news "Permalink to this headline")
------------------------------------------------------

Brave News is a private, ad-supported content news reader integrated into the Brave browser. It provides news content, Brave offers, display advertising, and promoted content. It is off by default.

When you turn ON Brave News, a range of content is presented by default. The default content is selected using [Brave Search](https://brave.com/search/#search-faq). You can at any time change the default content settings and choose what content you want appearing in your feed. You can also add feeds manually by subscribing directly to publishers’ content using publicly available RSS feeds.

To protect your privacy, Brave employs a combination of methods for delivering content that ensure your browser cannot be identified or tracked by Brave or any third party. Headlines are made available on a public CDN in text files, the same file for all users for each region. Some images from publishers and images in the Brave News user interface are processed to improve performance and ensure they display correctly in the Brave News user experience. Processed images are all delivered through a private and encrypted proxy method. The proxy removes and does not retain IP addresses before passing the encrypted request to the private content server, which then sends the encrypted reply back to the browser via the proxy. All other publisher images are collected directly from the publishers from your device. When you add RSS feeds manually, the text and images are collected directly from the publisher of the RSS feed and included in Brave News on the client. The feed of text and images from Brave and from your RSS feeds is temporarily stored on your device, and it is replaced upon starting or refreshing your Brave News session.

Display advertising and promoted content is delivered to all browsers within a given country that have turned on and enabled Brave News. Images from these are served by Brave using its private and encrypted proxy. If you also enable Brave Ads, advertising will be presented based on your interests, as inferred from your browsing behaviour and done on your device. Brave News remains private to you and anonymous.

Brave News will offer suggestions of sources you might like to follow. If you choose to follow a suggested source it will be added to your Following list; you can always unfollow a source via the Settings panel. The suggestions and your choices are determined on your browser and never leave your device. Your Brave News sessions are not logged or saved by Brave. This information is private to you and only you.

Brave’s source list, [content aggregator](https://github.com/brave/news-aggregator/) and [Suggestions service](https://github.com/brave/source-suggestions/) are open source and available to view via GitHub.

**Please note**: The RSS feed content you add is collected directly from the feed source and not proxied by Brave. The Brave browser fetches it without ever hitting Brave servers, and Brave never knows anything about your chosen RSS feeds.

It’s your choice. You can add, follow, unfollow, or hide content sources any time.

Brave Talk[](#brave-talk-learn "Permalink to this headline")
------------------------------------------------------------

Brave Talk is a private video and/or audio conference tool. What you say or type in the service is not logged or saved. Who you talk to, when, and how, is private to you. [See data processing details](#brave-talk).

Please note that Brave uses the [8x8](https://www.8x8.com/) communications platform, and software (API) capabilities of 8x8 (based on the [Jitsi](https://jitsi.org/) Open Source video conferencing software) to help deliver Brave Talk. 8x8 provides a service on behalf of Brave, and we remain responsible for Brave Talk.

### What information does Brave Talk process?[](#what-information-does-brave-talk-process "Permalink to this headline")

We process the minimum information necessary to provide the Brave Talk service. This includes:

* Your IP address and the URL of the meeting that will be processed only to enable calls; they are not retained after a call ends.
* If you use the chat function, chats will be temporarily cached for the duration of the meeting.
* If you record a meeting that you host, the recording will be temporarily stored on the server for 24 hours to allow you to download it. Your name and email address that you choose to display will be processed and available during the meeting.

While communications are encrypted between the Brave browser and Brave Talk servers via transport layer encryption, they are not encrypted on the server during a call, unless you enable Video Bridge Encryption (VBE). Additional security options are available to you in the settings menu once you initiate a call. These include:

* **Enable Lobby**: This lets you protect your meeting by only allowing people to enter after being approved by a moderator.
* **Add a passcode**: This lets you restrict access to the meeting to people who have been provided the code.
* **Enable Video Bridge Encryption (VBE)**: This is currently experimental. If you enable VBE, it will disable server side services such as recording, live streaming, and phone participation. Note that if you enable VBE but other participants do not, they won’t be able to see or hear you.

Please note that if you upgrade to the Brave Talk Premium plan, Brave will require an email address to initially create a premium account, and subsequently to manage your access to the account using anonymous credentials. We use the third-party payment provider [Stripe](https://stripe.com/gb/checkout/legal) to process payments for premium subscriptions. Stripe will process your email address, name, and payment card data for the purpose of managing your subscription payments only. Brave does not receive nor have access to your payment method details supplied to Stripe, and we cannot associate an account email address or payment details with your communications on Brave Talk.

Web3 calls are a special feature of Brave Talk. They use Web3 services as a gating mechanism to a call, so that only people who can prove ownership of a particular NFT can join a video call.

For each new Web3 Brave Talk call the service will look up NFT addresses that match users’ Brave Wallet addresses, via a service called Simplehash. The address lookup is handled via an anonymous proxy, which means Brave servers never record the addresses and have no visibility of members of a call.

Web3 calls use the same infrastructure as non-Web3 Brave Talk calls. However, the use of NFTs and POAPs (which are publicly available on blockchains) makes the members of Web3 calls anonymous but not private.

[Learn more about Web3 Calls](https://support.brave.com/hc/en-us/articles/15593255342093)

**To avoid scams:** For the avoidance of phishing attacks, note that we at Brave will never contact Brave Browser users in a Brave Talk call.

We do not authenticate users or their associated avatar images. Accordingly, you should never share any confidential information with anyone on Brave Talk unless you are certain that you know who you are talking to. (Of course, this is a good practice regardless of whether you are using Brave Talk, or email, or any other form of communication.)

Brave Translate[](#brave-translate "Permalink to this headline")
----------------------------------------------------------------

Brave removes IP addresses associated with requests submitted to the translation service. Additionally, any text submitted is not retained after the request completes. We do this to protect your privacy.

Brave Firewall + VPN[](#brave-firewall--vpn "Permalink to this headline")
-------------------------------------------------------------------------

You can subscribe to Brave Firewall + VPN in two ways: via [account.brave.com](https://account.brave.com/), or via the applicable app store for your mobile device (iOS App Store or Google Play Store). Brave Firewall + VPN is powered by [Guardian](https://guardianapp.com/), and Guardian also provides technical support for Brave’s Firewall + VPN service. [To learn more about what information we use for subscriptions—and why—see our data processing details](#vpn).

Brave Leo[](#brave-leo "Permalink to this headline")
----------------------------------------------------

The Brave Leo AI private chat feature provides summaries of the webpage you’re browsing via a chat interface that allows you to submit questions and receive responses about the content of that page. You can also ask Brave Leo questions in general and enable automatic suggested questions. Brave browser shares with the server your latest prompt, the context of your current conversation and, when the use case calls for it, the necessary context from the page you’re viewing. Note that once a chat is closed all record of it is erased. 

Brave Leo privacy protections include:

* Reverse proxy: All requests are proxied through an anonymizing server so that the request and the user’s IP address cannot be linked.
* Immediate discarding of responses: Conversations are not persisted on Brave’s servers. We do not collect identifiers that can be linked to you (such as IP address). Responses generated with Brave-hosted models are discarded after they’re generated, and not used for model training; no personal data is retained by Brave-hosted AI models.
    * Note that some non-Brave hosted models (such as Anthropic) will have different data retention policies. If you select a model from Anthropic and submit Leo queries, that data will be processed by Anthropic, and retained on Anthropic’s servers for 30 days. Anthropic acts on our behalf as a data processor for any personal data submitted, but does not use any personal data for its own purposes or to train its AI model. Anthropic are also not allowed to share query inputs and outputs, or link them to Brave.
* No login or account required for access: Users do not need to create a Brave account to use the free version of Leo.
* Unlinkable subscription: If you sign up for Leo Premium, you’re issued unlinkable tokens that validate your subscription when using Leo. This means that Brave can never connect your purchase details with your usage of the product, an extra step that ensures your activity is private to you and only you. The email you used to create your account is unlinkable to your day-to-day use of Leo, making this a uniquely private credentialing experience.

The accuracy of summaries and responses to questions is not guaranteed and may include inaccurate, misleading, and/or false information. You should not submit sensitive or private information in Leo, and should exercise caution with any text related to health, finance, personal safety, or similar cases.

Brave Leo is powered by different AI models which you can select, including self-hosted implementations of open-source models, such as Meta’s Llama 2 and Mistral AI models, and models provided by 3rd parties, such as Anthropic’s Claude models. More information on each model, rate limits, and defaults can be found in the Brave Leo wiki [https://github.com/brave/brave-browser/wiki/Brave-Leo](https://github.com/brave/brave-browser/wiki/Brave-Leo)

Submitting a prompt may include context from the current web page you are viewing, and if you enable automatic suggested questions, the page contents of your navigations will be sent to Leo to generate these suggestions while Leo is open. You can change these options any time in Settings.

The legal basis relied on to process any personal data submitted is that it is necessary for the legitimate interests of Brave and end users.

Web Discovery Project[](#web-discovery-project "Permalink to this headline")
----------------------------------------------------------------------------

The Web Discovery Project is intended to make Brave Search more relevant and useful for everyone. If you opt in, you’ll contribute some anonymous data about searches and web page visits made within the Brave Browser (including pages arrived at via some, but not all, other search engines). This data helps build the Brave Search independent index, and ensure we show relevant results to your search queries and support more relevant experiences with Brave products and services.

Collection is done in a privacy preserving fashion. By default, the Web Discovery Project discards search queries that are too long or suspicious looking (e.g. those that include phone numbers). It also discards odd URLs (e.g. those containing hashes), URLs of pages with a no-index flag, and pages that are not public or require any sort of authentication.

The system is designed so that no data received can be linked back to individuals or their devices. For a URL to be sent it needs to be visited independently by a large number of people. All data received is unlinkable, making it impossible to build profiles or sessions of Web Discovery Project contributors.

[Read a full description of the Web Discovery Project methodology.](https://support.brave.com/hc/en-us/articles/4409406835469-What-is-the-Web-Discovery-Project-)

How we improve Brave[](#how-we-improve-brave "Permalink to this headline")
--------------------------------------------------------------------------

### Diagnostic reports[](#crash "Permalink to this headline")

When Brave crashes or freezes, it creates a report that can be sent to us to help us diagnose and fix whatever caused the problem. This report contains technical information about your computer system and the event causing the problem. The data can’t be used to identify you.

We use a service called Backtrace.io to store the reports. You can choose whether to send us these reports. Even if you have chosen to send reports in the past, you can turn off future reports in [settings](https://support.brave.com/hc/en-us/articles/360017905872-How-do-I-enable-or-disable-automatic-crash-reporting-).

### Privacy Preserving Product Analytics[](#privacy-preserving-product-analytics "Permalink to this headline")

The Browser sends us anonymous reports to alert us to product problems and necessary improvements. None of the information it reports harms your privacy. The report only describes general use of the Browser or other Brave products, such as a general range of how many extensions are installed, a general range of how many tabs are open, and whether features like Shields, Rewards, and Ads are switched on. [See the full list of questions here](https://github.com/brave/brave-browser/wiki/P3A). These reports are stripped of metadata, and aggregated with measurements reported by many other instances of Brave. The data are not personal, and cannot be combined to identify you. You can deactivate Privacy-Preserving Product Analytics in Settings.

### Your feedback[](#your-feedback "Permalink to this headline")

If you submit a Web compatibility report, you’ll have the option to include certain details to help us analyze and address compatibility issues. Providing this information is voluntary, and any data you submit will be deleted from Brave’s servers after 30 days. See our [Web compatibility reports wiki page](https://github.com/brave/brave-browser/wiki/Web-compatibility-reports) for more details on what data is collected.

By submitting Brave AI feedback, you have the option to include additional details to assist us in improving this feature. These details may include the address of the website on which Leo was used. It is important to note that providing this information is entirely voluntary. Submitted data will be deleted from Brave servers after 1 year.

Any personally identifiable information (PII) you provide, such as your contact details, will be handled with strict confidentiality. We do not sell, trade, or transfer your information to any third parties.

We collect this data solely for the purpose of improving our services, enhancing your browsing experience, and resolving compatibility issues.

If you write feedback for Brave, we will use this to improve the product. [See data processing details](#feedback).

### Nightly, Dev, and Beta browser versions[](#dev "Permalink to this headline")

[Nightly](https://brave.com/download-nightly/), [Dev](https://brave.com/download-dev/), and [Beta](https://brave.com/download-beta/) versions of the Brave Browser are experimental previews of new Brave Browser versions. They allow us to test new features so that we can find and fix errors before releasing a new version of the Brave Browser. These test versions of the Browser may automatically send crash reports to Brave so that we can identify and fix problems. A crash report can contain personal information. [See data processing details.](#dev-detail)

**How to switch this feature off.** You can switch off “Automatically send usage statistics and crash reports to Brave Software” in settings.

> **Tip:** you can quickly access settings by copying _**brave://settings**_ into your address bar.

These incomplete versions of Brave represent unfinished and untested work on future versions of Brave, and their incomplete behaviour may not be adequately described by this policy. More information about the safety & reliability of pre-release versions of Brave can be found in our [development documentation](https://github.com/brave/brave-browser/wiki/Release-Channel-Descriptions).

### Location

| Purpose of processing | Categories of personal data processed | Legal basis of processing | Duration of storage |
| --- | --- | --- | --- |
| To estimate the user’s physical location at the request of a website and with the confirmation of the user. | IP address, and information about nearby WiFi access points (MAC address, signal strength, and SSID). | Legitimate interest. | No storage. |

### Brave Rewards

| Purpose of processing | Categories of personal data processed | Legal basis of processing | Duration of storage |
| --- | --- | --- | --- |
| To make and verify Basic Attention Token contributions, (including to detect and prevent fraud). | IP address at time of claiming a grant of BAT tokens or requesting confirmation tokens. | Necessary for the performance of a [contract between us](https://basicattentiontoken.org/user-terms-of-service/) and necessary to provide the requested service.<br><br>Processing for the purposes of fraud prevention is based on the legitimate interests of Brave and users of Brave Rewards. | Generally stored for 7 days. In cases of suspected fraud, stored for up to 60 days. In case of confirmed fraud, stored for up to 2 years. |
| To make and verify Basic Attention Token contributions, (including to detect and prevent fraud). | Rewards Payment ID, declared country code and Custodian ID and custodial country code when verifying a Brave Rewards wallet with a custodial partner. | Necessary for the performance of a [contract between us](https://basicattentiontoken.org/user-terms-of-service/), (and necessary to provide the requested service & to provide customer support).<br><br>Processing for the purposes of fraud prevention is based on the legitimate interests of Brave and users of Brave Rewards. | The duration of the user’s account, plus 4 years in order to comply with US Internal Revenue Service requirements. |
| To make and verify Basic Attention Token contributions to a Solana address, (including to detect and prevent fraud). | Rewards Payment ID and associated Solana address | Necessary for the performance of a [contract between us](https://basicattentiontoken.org/user-terms-of-service/) and necessary to provide the requested service.<br><br>Processing for the purposes of fraud prevention is based on the legitimate interests of Brave and users of Brave Rewards.<br><br>Compliance with legal obligations | The duration of the user’s account, plus 4 years in order to comply with US Internal Revenue Service requirements. |

### Brave News

| Purpose of processing | Categories of personal data processed | Legal basis of processing | Duration of storage |
| --- | --- | --- | --- |
| To collect content from the server in order to display it for the user. | IP addresses. | Legitimate interest. The data are used in order to deliver the service, and the risk of the processing of the data is minimal. | The duration of the request and response |

### Brave Talk

| Purpose of processing | Categories of personal data processed | Legal basis of processing | Duration of storage |
| --- | --- | --- | --- |
| To facilitate communications via Brave Talk. | IP address, meeting URL, chat content, audio and video, recordings of meetings. | Legitimate interest. The processing is necessary to provide the requested service. | Duration of the call, except for recordings of meetings that are temporarily stored for 24 hours. |
| To create a Brave Premium account and manage account access. | Email address | Legitimate interest.<br><br>The data is necessary to establish an account and manage account access. | Until an account is deleted. |

### Brave Firewall + VPN

| Purpose of processing | Categories of personal data processed | Legal basis of processing | Duration of storage |
| --- | --- | --- | --- |
| To send an alert to the user when a firewall rule is triggered. | Pseudonymous user ID, details of the blocked tracker/firewall rule triggered. | Necessary for the performance of the contract (to deliver the service). | 3 days. |
| To create private connections. | IP Address. | Necessary for the performance of the contract (to deliver the service). | None. IP addresses are not logged. |
| To provide customer support. | Email address and other personal data that a user may choose to share when requesting technical support from Guardian. | Necessary for the performance of the contract (to deliver the service). | 12 Months after closing a support ticket. |

### Brave IPFS Public Gateway

| Purpose of processing | Categories of personal data processed | Legal basis of processing | Duration of storage |
| --- | --- | --- | --- |
| To allow access to IPFS content when the user cannot access it via a local IPFS node | IP address | Legitimate interest. The user requested the service, and the risk of the processing of the data is minimal. | Indefinite. (Protocol Labs) |

### Your feedback

| Purpose of processing | Categories of personal data processed | Legal basis of processing | Duration of storage |
| --- | --- | --- | --- |
| To use feedback sent by users to improve the product. | Personal data that a user may include in the text they write when sending feedback through an app store or any other means. | Legitimate interest. The user intends for the data to be used for this purpose, and the risk of the processing of the data is minimal. | 2 years. |

### Browser testing and research (Nightly, Dev, and Beta versions only)

| Purpose of processing | Categories of personal data processed | Legal basis of processing | Duration of storage |
| --- | --- | --- | --- |
| To fix problems in the Brave Browser by acting on issues highlighted by crash reports from Beta and Dev versions of the Browser | Device model, iOS version, language, timezone, CPU architecture, carrier, connection status. Optional: Crash log (crash logs will also be sent if you opted-in when activating iOS) Optional: Comments and screenshots you share if you send feedback through TestFlight. | Our interest in testing the product and fixing problems. The data are used in a way that does not negatively affect your rights or interests. | Apple retains the data for one year. Brave may retain some crash reports indefinitely, if useful for testing. |

Help with privacy settings in Brave[](#help-with-privacy-settings-in-brave "Permalink to this headline")
--------------------------------------------------------------------------------------------------------

You can find guides on how to change privacy settings in Brave [in the Help Center.](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-).

Contacting Brave about your privacy[](#contacting-brave-about-your-privacy "Permalink to this headline")
--------------------------------------------------------------------------------------------------------

We are always interested in hearing and responding to questions and concerns at [twitter.com/brave](https://twitter.com/brave) and at [github.com/brave](https://github.com/brave). More in-depth conversations can be had at [community.brave.com](https://community.brave.com/).

We are represented in Europe by Brave Software Europe Ltd (based in the UK). You can contact our data protection officer and the rest of our privacy team at [privacy@brave.com](mailto:privacy@brave.com). However, from the 1st January 2021, given the UK’s exit from the EU, Brave has appointed an EU nominated representative and which you may contact if you would prefer not to contact Brave directly:

Brave EU Nominated Representative Care of Castlebridge Unit 7, 12 Mountjoy Square, Dublin 1 Ireland

[brave@gdprnomrep.eu](mailto:brave@gdprnomrep.eu)

You can ask to know what information we have about you, update incorrect information, delete it, object to our use of it, or get a copy of it. If you’re in the European Union, you also have the right to complain to your [local data protection authority](https://edpb.europa.eu/about-edpb/about-edpb/members_en) (though everyone should have this right).

We’ll update this policy whenever we make material changes to our practices, and we’ll announce it to let you know. We hope you’ll find any changes agreeable, but if you’re not comfortable with changes to the info we collect or how we use it, we understand your choice to stop using Brave. 

* * *

* * *

1. Data are personal if the data can single a person out (on their own or in combination with other data), without an unlikely degree of effort or expense or technological development. The GDPR definition of “personal data” includes any data that can indirectly contribute to singling out an individual, including unique IDs codes, certain types of IP addresses, and encrypted data that one can decrypt without disproportionate effort. But data that are entirely impossible to access are not personal. [↩︎](#fnref:1)