Privacy Policy
==============

Last updated on 2024-06-01


=============================================================

1\. When You Visit Our Website
------------------------------

We do not use any 3rd party tracking or analytics services, so your activity on this website stays with us (and your ISP). We use open source Piwik web analytics platform to measure usage on our website, which is hosted on our servers. Piwik is used to analyze and aggregate information about our website visitors. When your web browser loads a page on our site, a small snippet of JavaScript code is executed within your browser which submits information such as your browser user-agent, language, screen resolution, referring website, and a subset of your IP address (first 3 octets).

2\. When You Sign Up
--------------------

We store the email address associated with your account and the date of registration. When you pay for a premium account, we store the transaction ID of your payment so we can track it down for refund purpose or fraud mitigation.

3\. When You Use Our Service
----------------------------

When you use ControlD, we keep the following data associated with your account:

* Timestamp of your last activity in the dashboard or apps
* Your source IP address which is required to make ControlD work

**This only applies to Premium resolvers that enforce custom DNS profiles. Free resolvers listed on the homepage do not store this or any other data including but not limited to IP addresses, timestamps or DNS queries themselves.**

We use a custom implementation of EDNS Client Subnet which does not expose the source IP address to authoritative DNS servers. Query Name Minimisation is enforced.

3.1 Source IP Storage JustificationUnlike a VPN, ControlD operates at the DNS layer, which means there is no way for you to supply your authentication credentials along with the request. In order for the DNS server to know who you are, so it can apply the correct rules, the only anchor we have is the source IP the request came from. This requirement is mitigated if you're using DNS-over-HTTPS or DNS-over-TLS resolvers. However, your source IP is still needed when communicating with our transparent proxies as it must be known to our firewall so access can be granted.

3.2 Privacy ImplicationsEven though we store the IP address associated with each account, the threat to user privacy is very limited. Typically, 3rd parties will supply a timestamp + IP address when requesting user data. The IP address will be that of the proxy that was used at the time (if one was using a proxy). At any given moment, there are hundreds or thousands of people that could be sharing the same IP address. Since ControlD does not keep logs of which proxy server IPs were used by which user, nor do we even have access to this data, we have no way to trace any activity to any individual account.

3.3 Sale or Transfer of DataWe prioritize user privacy by not retaining, selling, or transferring personal information, IP addresses, user identifiers, or user query patterns to any third party. We do not combine collected data in a manner that can identify individual users, and we strictly prohibit the sale, licensing, sublicensing, or granting of user data rights to any other entity.

4\. When you leave
------------------

If for some strange reason you decide not to use our service anymore, you can delete your account at any time in the "My Account" section. All data is immediately and permanently deleted from our database.

5\. User Data Requests
----------------------

Since we store the bare minimum for a customer to actually use our service, any request for user data that supplies an IP + timestamp would yield nothing of value as we do not store any historical logs on who used which IP address, and since IPs are shared by dozens/hundreds of people at any given moment, so we cannot tie any activity to a specific account. Much like any other service, if a valid Canadian subpoena includes the exact email associated with an account, we have no choice but to provide all details associated with the account. This data is limited to what was mentioned above.

6\. Changes to Policy
---------------------

We will do our best to avoid any changes, which includes moving the company to a different jurisdiction if required. If drastic policy changes are needed and we cannot continue providing service under the above mentioned terms, users with valid emails will be notified.

General[Pricing](https://controld.com/pricing)[Personal Use](https://controld.com/personal/?noRedirect=true)[Free DNS](https://controld.com/free-dns)[Help](https://docs.controld.com/docs/)[Privacy](https://controld.com/privacy)[Terms](https://controld.com/terms)

Features[Malware Blocking](https://controld.com/features/malware-blocking)[Web Filtering](https://docs.controld.com/docs/feature-web-filtering)[Service Filtering](https://docs.controld.com/docs/feature-service-filtering)[Custom Filtering](https://docs.controld.com/docs/feature-custom-filtering)[Modern Protocols](https://docs.controld.com/docs/feature-modern-protocols)[Analytics](https://docs.controld.com/docs/feature-analytics)[Data Streaming (SIEM)](https://docs.controld.com/docs/feature-data-streaming-siem)[Traffic Redirection](https://docs.controld.com/docs/feature-traffic-redirection)[Multi-Tenancy](https://docs.controld.com/docs/feature-multi-tenancy)[Admin Logs](https://docs.controld.com/docs/feature-admin-logs)

Industries[Start-Ups](https://docs.controld.com/docs/industry-startups)[Small Businesses](https://docs.controld.com/docs/industry-smbs)[Public Wi-Fi](https://docs.controld.com/docs/industry-public-wifi)[Education](https://docs.controld.com/docs/industry-schools)[Hospitality](https://docs.controld.com/docs/industry-airbnb-hosts)[MSPs](https://docs.controld.com/docs/industry-msps)[Non-Profits](https://docs.controld.com/docs/industry-non-profits)

Resources[Knowledge Base](https://docs.controld.com/docs/)[API Docs](https://docs.controld.com/reference)[Blog](https://controld.com/blog)[Network](https://controld.com/network)[Changelog](https://docs.controld.com/changelog)[Status](https://controld.com/status)[Support](https://controld.com/contact)

* * *

© CONTROLD, Inc.

[](https://twitter.com/controldns)[](https://www.reddit.com/r/ControlD/)[](https://discord.gg/dns)

OrganizationPersonal

Log inGet Started