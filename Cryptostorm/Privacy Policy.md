Toggle navigation [![tiny logo](/images/cs-tiny-logo.png)](https://cryptostorm.is/#section1)

* [privacy](https://cryptostorm.is/#section2)
* [security](https://cryptostorm.is/#section3)
* [benefits](https://cryptostorm.is/#section4)
* [locations](https://cryptostorm.is/#smap)
* [buy](https://cryptostorm.is/#section5)
* [connect](https://cryptostorm.is/#section6)
* [contact](https://cryptostorm.is/#section7)
* [faq](https://cryptostorm.is/faq)
* [blog](https://cryptostorm.is/blog/)
* You are NOT connected to cryptostorm
    
    Your IP address is: 2001:41d0:801:1000::9de

* [sitemap](https://cryptostorm.is/map)

![](/images/cs-logo.png)
========================

[GDPR](https://en.wikipedia.org/wiki/General_Data_Protection_Regulation) update  
(Last updated in 2024)
--------------------------------------------------------------------------------------------------------

The old privacy policy was written in 2013, which might make it seem outdated, but the fact is we haven't ever updated it because our data policies have remained the same.  
cryptostorm has no active business entities in any EU member state at the moment, but we do believe that every nation should be creating and enforcing data protection legislation like the GDPR.  
For that reason, we thought we'd rewrite the old privacy policy and see if we could provide more (probably too many) technical details on exactly how the whole ordering/connecting process works, what's being logged, and what to do if you don't want us to retain what little data we do have.  
  
The first step any potential customer would take is visiting this site, [https://cryptostorm.is](https://cryptostorm.is/). This is an [Apache](https://httpd.apache.org/) webserver that has mostly default logging, which means the log will contain visitor IPs, user agents (browser), referrer (where you came from), the file you're requesting, and the time/date of the request. We have no reason to maintain historical records of our web visitors, so those logs are rotated/deleted automatically after 2 weeks. The reason these logs exist is because it's virtually impossible to maintain security on a web server without these access/error logs.  
If you don't want your real IP address to show up in those web logs, you can also reach this website at the [.onion](https://en.wikipedia.org/wiki/.onion) address [stormwayszuh4juycoy4kwoww5gvcu2c4tdtpkup667pdwe4qenzwayd.onion](http://stormwayszuh4juycoy4kwoww5gvcu2c4tdtpkup667pdwe4qenzwayd.onion/).  
If visiting this website on the [clearnet](https://en.wikipedia.org/wiki/Clearnet_(networking)) is necessary, or not a big deal in your [threat model](https://en.wikipedia.org/wiki/Threat_model#Threat_Modeling_Methodologies_for_IT_Purposes), you can also visit this website using [Tor Browser](https://www.torproject.org/download/download-easy.html.en), any type of proxy, or a competitor's VPN service.  
To keep your browser/user agent hidden from us, you can use any one of the many user agent changing browser addons, such as [User Agent Switcher and Manager](https://addons.mozilla.org/en-US/firefox/addon/user-agent-string-switcher/) for Firefox, or [User-Agent Switcher](https://chrome.google.com/webstore/detail/user-agent-switcher-for-c/djflhoibgkdhkhhcedjiklpkjnoahfmg) for Chrome.  
For the referrer, browser addons such as [Toggle Referrer](https://addons.mozilla.org/en-US/firefox/addon/togglereferrer/) for Firefox or [Referer Control](https://chrome.google.com/webstore/detail/referer-control/hnkcfpcejkafcihlgbojoidoihckciin) for Chrome is what you're looking for.  
If for whatever reason you can't wait the 2 weeks for the web logs to purge themselves, you can always email [support@cryptostorm.is](mailto:support@cryptostorm.is) and ask us to remove you from the web logs early.  
  
The second step in the ordering process is selecting a payment method to use on the [https://cryptostorm.is/#section5](https://cryptostorm.is/#section5) page.  
No matter what payment method you choose, the data we retain is always the same: email, token delivered, and a transaction ID provided by the payment processor.  
The email address is not saved (or requested) for the XMR/Monero and NOWPayments options since those payment methods only do in-browser delivery.  
There's also a new option in the token delivery page where you can remove your plaintext token from our database (provided you agree not to hold us responsible if you lose it).  
It's at the bottom of the token delivery page, the dark green "DELETE TOKEN" button.  
For the payment methods that do ask for an email, the address you provide is only used to deliver the token, and the token is retained for re-delivery in case you lose your token.  
The transaction ID is used to prevent duplicate orders from being processed twice, which is necessary because the entire ordering/delivery process is fully automated.  
In the case of Bitcoin payments through Bitpay, we also provide an option that allows you to opt-out of email delivery. When you choose that option, we send Bitpay a local '@cryptostorm.is' email address for the order, because Bitpay requires an email address, and since we host our email on the same server as this website, the email never leaves for the internet.  
At the moment, we can't offer the same option for PayPal orders due to limitations in the PayPal IPN.  
The tokens used by the automated delivery process come from a simple flat database that is manually loaded after minting the tokens on a separate server that holds the authentication database.  
Again, if for some reason you want your token/email removed from our delivery log, just email [support@cryptostorm.is](mailto:support@cryptostorm.is) and ask.  
  
The third step, once a customer has their token, is connecting to cryptostorm.  
Whenever a customer connects to any node, that node will authenticate the provided token by connecting to a separate/dedicated web server that hosts an API that accesses the actual authentication database running on the same server.  
That authentication database is a simple MySQL database that uses the following columns:

+---------------+--------------+------+-----+---------+-------+
| Field         | Type         | Null | Key | Default | Extra |
+---------------+--------------+------+-----+---------+-------+
| activated\_at  | varchar(20)  | YES  |     | NULL    |       |
| duration      | int(11)      | YES  |     | NULL    |       |
| hash          | varchar(129) | YES  |     | NULL    |       |
| session\_count | int(11)      | YES  |     | NULL    |       |
+---------------+--------------+------+-----+---------+-------+

The 'activated\_at' field is [NULL](https://en.wikipedia.org/wiki/Null_(SQL)) to begin with, then later filled with the current time/date in [UNIX time](https://en.wikipedia.org/wiki/Unix_time) format whenever the customer connects for the first time. This field allows tokens to expire whenever they're supposed to.  
The 'duration' field contains the token's length, or duration, in days (i.e., 31, 7, 365, etc.). This field is used by [https://cryptostorm.nu](https://cryptostorm.nu/) to let customers know how many days their token has left until expiration, and it's also used to enforce simultanous connection limits.  
The 'hash' field is the sha512 hash of the plaintext token. Whenever tokens are minted, the hash goes into this database on the auth server, and the plaintext token goes into the delivery server's flat database. That keeps the authentication database from knowing the plaintext token after minting, and it keeps the nodes from ever knowing the plaintext token.  
And finally, 'session\_count' is self-explanatory. OpenVPN on the server increases this field when a customer connects, using the script available at [https://cryptostorm.is/conf/session\_up.sh.txt](https://cryptostorm.is/conf/session_up.sh.txt), and it decreases this field using [https://cryptostorm.is/conf/session\_down.sh.txt](https://cryptostorm.is/conf/session_down.sh.txt) when they disconnect.  
The OpenVPN server-side authentication is done by using the --auth-user-pass-verify script available at [https://cryptostorm.is/conf/auth.sh.txt](https://cryptostorm.is/conf/auth.sh.txt)  
As you can see from the above three scripts, the only data ever sent from the nodes to the authentication server API is your token's sha512 hash, and it's always sent using HTTPS.  
  
On the node itself, logging is disabled for everything

\[root@singapore ~\]# ls -la /var/log/
total 4
drwxr-xr-x  2 root root   18 Jan 13 17:41 .
drwxr-xr-x 15 root root 4096 Dec 28 21:16 ..
lrwxrwxrwx  1 root root    9 Dec 28 21:19 btmp -> /dev/null

That btmp file is only there because a few programs break if the file doesn't exist, but since we don't actually need it for anything, it's symlinked to /dev/null.  
Historical bandwidth usage data is also collected by [vnstat](https://humdi.net/vnstat/), but this data is NOT per-session or per-instance, it's for the entire server. We use this data to determine whether or not a node is getting so much traffic that it needs a secondary server to balance things out.  
  
I hope this information is useful to anyone curious about how our systems work, and if you have any more questions that aren't answered here, feel free to email [support@cryptostorm.is](mailto:support@cryptostorm.is).