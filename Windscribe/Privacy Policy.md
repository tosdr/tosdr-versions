Data Collection
===============

### When You Visit Our Website

We do not use any 3rd party tracking or analytics services, so your activity on this website stays with us (and your ISP). We use open source Piwik web analytics platform to measure usage on our website, which is hosted on our servers. Piwik is used to analyze in aggregate information about our website visitors. When your web browser loads a page on our site, a small snippet of JavaScript code is executed within your browser which submits information such as your browser user-agent, language, screen resolution, referring website, and a subset of your IP address (first 3 octets). We may set cookies if you were referred to us through our affiliate program in order to compensate the person who referred you, if you choose to sign up. The affiliate does not see any of this information.

### When You Sign Up

We only require a username and password when you signup to our service. Email can be provided if you wish to be able to recover your password in case you forget it, as well as receive periodic service updates. We use 3rd party payment processors. When you pay for a premium account, we store the transaction ID of your payment for a period of 30 days for fraud prevention purposes.

### When You Use Our Service

When you use Windscribe, we keep the following data associated with your account:

* Total amount of bytes transferred in a 30 day period. Bandwidth reset date is in your "My Account" section.
* Timestamp of your last activity on the Windscribe network.

This data is used to enforce free tier limitations, prevent abuse and weed out inactive accounts.

The following data is **NOT** stored:

* Historical record of VPN sessions
* Source IP
* Sites you visited

We are firm believer that one's browsing history should be taken to one's grave.

### When You Are Actively Connected to a Server

For the duration of your connection the following is stored in **server's memory**. This data is immediately discarded when you disconnect:

* OpenVPN/IKEv2 username
* Time of connection
* Amount of data transferred

The following data is stored in a central location:

* Number of parallel connections at any given time to prevent rampant abuse and account sharing.
* A counter is incremented that stores total number of bytes downloaded/uploaded in a 30 day period.

Anything that is not mentioned above is not stored.

[Read More](#)

The following is no longer applicable to Windscribe, as we replaced a bulk of the VPN authentication/bandwidth accounting system with a bespoke one in Q2 2018, which no longer requires us to delete anything after you disconnect, as there is nothing to delete.  
Vast majority if not all of VPN providers use [FreeRadius](https://freeradius.org/) for authentication and parallel connection enforcement which MOST providers have. In default mode, the "raw data" looks like [this](https://i.imgur.com/YyFextX.png). As you see, it shows the openvpn username, server IP connected to, when the session was started, terminated, and how much data was transferred. The column titled "callingstationid", by default, has the connected user's IP address. When we still used this system, we modified our instance to not supply this information. So to check how many parallel connections a user has, you simply look in this table and check how many records exist for a single username, with no session termination timestamp. After the user's session is terminated, the record stays in the database. Unless the provider physically removes the record via a cleanup script, it will stay there forever. Providers that keep logs, store this data for 30 or more days, and then remove it... allegedly.  
Our bespoke system eliminates the need for this session table entirely. This data resides only in server's memory while you're connected, and is immediately discarded by the VPN server when you disconnect. Since it doesn't get logged into a permanent database, there is nothing to delete.

### When You Leave

If for some strange reason you decide not to use our service anymore, the only piece of information that will remain is your username, password and email address (if you provided it). We periodically prune inactive accounts. You can delete your account at any time in the "My Account" section.

### User Data Requests

Since we store the bare minimum for a customer to actually use our service, any request for user data would yield nothing of value. As we do not store any historical logs on who used which IP address, and since IPs are shared by dozens/hundreds of people at any given moment, so we cannot tie any activity to a specific account.

[View Transparency Report](https://windscribe.com/transparency)

### Changes to Policy

We will do our best to avoid any changes, which includes moving the company to a different jurisdiction. If drastic policy changes are required due to a race of giant spiders enslaving all of humanity and forcing us to log our users under the threat of consumption, and we cannot continue providing service under the above mentioned terms, users (with valid email accounts) will be notified. That will be the least of your concern however, you know, because of the giant spiders.