[DivestOS Mobile](https://divestos.org/index.html)

[Home](https://divestos.org/index.html)[Search 🔎](https://divestos.org/pages/search)Get Started[Device Downloads](https://divestos.org/pages/devices)[Installation](https://divestos.org/pages/bootloader)[Post Install](https://divestos.org/pages/post_install)[Our Apps](https://divestos.org/pages/our_apps)[Recommended Apps](https://divestos.org/pages/recommended_apps)[Community](https://divestos.org/pages/community)[Donate 🧡](https://divested.dev/donate)Docs[FAQ](https://divestos.org/pages/faq)[News](https://divestos.org/pages/news)[History](https://divestos.org/pages/history)[Screenshots](https://divestos.org/pages/screenshots)[Known Issues](https://divestos.org/pages/broken)[Functionality Tables](https://divestos.org/pages/functionality_tables)[Troubleshooting](https://divestos.org/pages/troubleshooting)[Bug Reporting](https://divestos.org/pages/bug_reporting)[Patch Levels](https://divestos.org/pages/patch_levels)[Patch Counts](https://divestos.org/pages/patch_counts)[Patch History](https://divestos.org/pages/patch_history)[Technical Details](https://divestos.org/pages/technical_details)[Network Connections](https://divestos.org/pages/network_connections)[Saving Data](https://divestos.org/pages/saving_data)[Browser Tables](https://divestos.org/pages/browsers)[Messenger Tables](https://divestos.org/pages/messengers)[Verified Boot Hashes](https://divestos.org/pages/verified_boot_hashes)[Build Guide](https://divestos.org/pages/build)[Source Code on Codeberg](https://codeberg.org/divested-mobile)[Source Code on GitHub](https://github.com/divested-mobile)[Source Code on GitLab](https://gitlab.com/divested-mobile)[About](https://divestos.org/pages/about)  
  

Privacy Policy (2024-07-31)
---------------------------

History of this privacy policy can be viewed: [Codeberg](https://codeberg.org/divested-mobile/divestos-website/blame/branch/master/stubs/privacy_policy.html), [GitHub](https://github.com/Divested-Mobile/DivestOS-Website/blame/master/stubs/privacy_policy.html), [GitLab](https://gitlab.com/divested-mobile/divestos-website/-/blame/master/stubs/privacy_policy.html)

### What data we (Divested Computing Group) collect[¶](#fpCollect)

* Website[¶](#website)

* What is received: Cookies (none currently), Page Visited, Referring Page, User Agent, and IP Address
* How often: On every page visit
* Why it is received: Used to serve the web pages to users
* When it will be deleted: Web server logs are kept for no longer than two weeks
* What else will it be used for: Nothing else
* How to anonymize: Visit the site using the Tor Browser
* Example: `[IP Address] - - [Timestamp] "GET /pages/privacy_policy HTTP/2.0" 200 3441 "-" "Mozilla/5.0 (Windows NT 10.0; rv:91.0) Gecko/20100101 Firefox/91.0"`

* Operating System[¶](#system)

* The operating system does not contain any analytics and any requests are used only for supporting it

* OS: Connectivity Checks[¶](#fpConnectivityChecks)

* What is received: Static User Agent, IP Address
* How often: On every Wi-Fi and cell connection
* Why it is received: Used to determine if there is a working connection and if there is a captive portal
* When it will be deleted: All requests to generate\_204 are never logged
* What else will it be used for: Nothing else
* How to disable: Toggle in settings app (noted below) or `$ adb shell settings put global captive_portal_mode 0;`
* Settings can be accessed via:
    * 14.1/15.1: Settings > Network > Data usage > Disable Captive Portal
    * 16.0/17.1: Settings > Network & Internet > Advanced > Captive portal mode
    * 18.1/19.1/20.0: Settings > Network & Internet > Advanced > Internet connectivity check

* OS: Updater[¶](#systemUpdater)

* What is received: Device Model, Incremental Build ID, Default User Agent, IP Address
* How often: On every boot and also once per week (note: 14.1 only is daily)
* Why it is received: Used to serve system updates
* When it will be deleted: Web server logs are kept for no longer than two weeks
* What else will it be used for: Will be occasionally used to determine how many users we have and what percent are up-to-date or not
* How to anonymize: Install Orbot and enable 'Perform requests over Tor'
* How to disable: Disable 'Auto updates check'
* Settings can be accessed via:
    * 9+: Settings > System > Advanced > DivestOS updates > 3dot > Preferences
    * <9: Settings > About > DivestOS updates > 3dot > Preferences
* Example: `[IP Address] - - [Timestamp] "GET /updater.php?base=LineageOS&device=mata&inc=engemy20210814031730 HTTP/1.1" 200 276 "-" "Dalvik/2.1.0 (Linux; U; Android 11; PH-1 Build/RQ3A.210805.001.A1)"`

* OS: DivestOS F-Droid Repos[¶](#fpRepos)

* What is received: Repo Index Requests/App APK Requests/App Icon Requests, F-Droid Version, IP Address
* How often: Once per day
* Why it is received: Used to serve apps and their updates
* When it will be deleted: Web server logs are kept for no longer than two weeks
* What else will it be used for: Nothing else
* How to anonymize: Install Orbot and enable 'Use Tor' in F-Droid > Settings
* How to reduce: Decrease the 'Automatic update interval' in F-Droid > Settings
* How to disable: Disable the 'DivestOS' repos in F-Droid > Settings > Repositories
* Example: `[IP Address] - - [Timestamp] "HEAD /fdroid/official/index-v1.jar HTTP/1.1" 200 - "-" "F-Droid 1.13.1"`

* App: Hypatia[¶](#hypatia)

* What is received: Signature Database Requests, IP Address
* How often: Manually
* Why it is received: Used to serve signature databases
* When it will be deleted: Web server logs are kept for no longer than two weeks
* What else will it be used for: Nothing else
* How to anonymize: Install Orbot and enable 'Download over Tor'
* Example: `[IP Address] - - [Timestamp] "GET /MalwareScannerSignatures/hypatia-sha1-bloom.bin HTTP/1.1" 304 - "-" "Hypatia"`

* App: Carrion[¶](#carrion)

* What is received: Complaint Number Database Requests, IP Address
* How often: Manually
* Why it is received: Used to serve complaint number databases
* When it will be deleted: Web server logs are kept for no longer than two weeks
* What else will it be used for: Nothing else
* How to anonymize: Install Orbot and set it to handle Carrion
* Example: `[IP Address] - - [Timestamp] "GET complaint_numbers.txt.gz HTTP/1.1" 304 - "-" "Carrion"`

* Chat rooms (MUC) available on xmpp:konvers.me[¶](#xmpp)

* What is received: JID, nickname, avatar, messages you send, your server IP address, your client IP address only if fetching an HTTP uploaded image
* How often: When you join and are connected to a room
* Why it is received: Used to provide the chat service to you
* When it will be deleted: Messages are not deleted per default MAM policy, but are pruned after backups. Access logs are deleted weekly. IP addresses are not stored in the access logs.
* What else will it be used for: Nothing else
* How to anonymize: Use a throwaway JID and nickname. Route your XMPP client over Tor.
* Please note: third party volunteers may be appointed as moderators and be able to see your JID.

### What data third parties collect[¶](#3rdparty)

Third parties are used to support basic functions along with features and apps.

* Website Payments[¶](#stripe)

* Who: Stripe
* What they receive: Name, Bank Card, E-Mail Address, User Agent, Browser Fingerprint, IP Address, Location from Geo-IP
* What we receive: Name, Bank Name, E-Mail Address, User Agent, Location from Geo-IP
* How often: When you donate
* Why they receive: Used to process the payment
* What else will we use it for: Nothing else
* How to anonymize: Use a fake name, debit gift card, disposable e-mail address, and connect via a computer at your local library
* How to disable: Requests to Stripe's servers will not occur until you attempt to donate
* Privacy Policy: [Stripe Privacy Policy](https://stripe.com/us/privacy)

* OS: Connectivity Checks[¶](#googleConnectivityChecks)

* Who: Google
* Description: Used to determine if there is a working connection and if there is a captive portal
* What they receive: Static User Agent, IP Address
* How often: On every Wi-Fi and cell connection
* How to disable: Toggle in settings app (noted below) or `$ adb shell settings put global captive_portal_mode 0;`
* Settings can be accessed via:
    * 14.1/15.1: Settings > Network > Data usage > Disable Captive Portal
    * 16.0/17.1: Settings > Network & Internet > Advanced > Captive portal mode
    * 18.1/19.1/20.0: Settings > Network & Internet > Advanced > Internet connectivity check
* Privacy Policy: [Google Privacy Policy](https://policies.google.com/privacy)

* OS: Network Time Protocol[¶](#ntp)

* Who: pool.ntp.org volunteers
* Description: Used to set an accurate (clock) time
* What they receive: IP Address
* How often: On every boot
* Privacy Policy: unavailable

* OS: Fallback Domain Name System Lookups[¶](#dns)

* Who: Quad9
* Description: Used to translate domain names into IP addresses to establish network connections, only when no other DNS was advertised by the network
* What they receive: DNS requests, IP Address
* How often: Every network request to a non-cached and non-expired domain
* Privacy Policy: [Quad9 Privacy Policy](https://www.quad9.net/privacy/policy)

* OS: F-Droid Official Repo[¶](#fdroid)

* Who: F-Droid
* What they receive: Repo Index Requests/App APK Requests/App Icon Requests, F-Droid Version, IP Address
* How often: Once per day
* Why they receive: Used to serve apps and their updates
* How to anonymize: Install Orbot and enable 'Use Tor' in F-Droid > Settings
* How to reduce: Decrease the 'Automatic update interval' in F-Droid > Settings
* How to disable: Disable the 'F-Droid' repos in F-Droid > Settings > Repositories
* Privacy Policy: [F-Droid Security Information](https://f-droid.org/docs/Security_Model)

[Divested Computing Group](https://divested.dev/) © 2017-2024  
[Search 🔎](https://divestos.org/pages/search)  
[Support our work!](https://divested.dev/donate)  
[Privacy Policy](https://divestos.org/pages/privacy_policy) || [Terms of Service](https://divestos.org/pages/terms_of_service)  
Powered by [mini.css](https://web.archive.org/web/20220418142847/https://minicss.org/) (MIT)  
[Primary](https://divestos.org/)  
[Cloudflare Mirror](https://divestos.eeyo.re/)  
[Onion #1](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion/)  
[Onion #2](http://2ceyag7ppvhliszes2v25n5lmpwhzqrc7sv72apqka6hwggfi42y2uid.onion/)  
[Wayback Machine](https://web.archive.org/web/20300000000000/https://divestos.org/)  
Generated: 2024-11-07T15:15:01+00:00