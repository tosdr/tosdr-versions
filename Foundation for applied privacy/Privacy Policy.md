[Skip to main content](#content)

Toggle navigation [Foundation for Applied Privacy](https://applied-privacy.net/)

* [Blog](https://applied-privacy.net/blog)
* [Services](#)
    * [Overview](https://applied-privacy.net/services)
    * [DNS Privacy](https://applied-privacy.net/services/dns)
    * [Tor Relays](https://applied-privacy.net/services/tor)
* [Donate](https://applied-privacy.net/donate)
* [Infrastructure](https://applied-privacy.net/infrastructure)
* [Presentations](https://applied-privacy.net/presentations)
* [Contact](https://applied-privacy.net/contact)
* [Membership](https://applied-privacy.net/membership)
* [Privacy Policy](https://applied-privacy.net/privacy-policy)

* [Deutsch](https://applied-privacy.net/de/)

[Privacy Policy](https://applied-privacy.net/privacy-policy/)
=============================================================

### Also available in:

[Deutsch](https://applied-privacy.net/de/privacy-policy/)

Data Minimization
-----------------

We strive to minimize data collection and logging at the technical level to avoid having much sensitive data in the first place. The fewer sensitive data we have the fewer effort it will take us to make unauthorized access to the data we have, hard.

Since you can use our services anonymously (without registration) we do not have to store any personal information persistently by design.

DNS Privacy Services
--------------------

* We do NOT log your IP address.
* We do NOT log your DNS query.
* We do NOT share query data with third parties.

We aggregate and store the following non-sensitive operational performance metrics for one year for capacity planning and error detection:

* how many queries we get for each protocol (via DNS-over-TLS and DNS-over-HTTPS)
* amount of concurrently open DoH and DoT connections
* how fast we answer queries (in ranges: <=1ms, <=10ms, <=50ms, ...)
* how many queries we answer directly from the cache (cache hits)
* how many queries we get via IPv4 vs. IPv6
* DoH HTTP response codes (200, 502, ...)
* Avg. queries per connection
* Avg. connection duration
* TLS version (v1.2, v1.3, ...)
* new vs. resumed TLS sessions
* TLS handshake failure reasons (unsupportedProtocol, dhKeyTooSmall, ...)
* amount of queries by DNS flag (DNSSEC OK, EDNS OPT present, recursion desired, auth. answer, ...)
* amount of queries by type (A, AAAA, PTR, ...)
* amount of DNS answers by return code (NOERROR, FORMERR, SERVFAIL, NXDOMAIN, REFUSED, ...)

Website
-------

When you visit this [website](https://applied-privacy.net/) we log the following information and store it for 30 days:

* timestamp
* HTTP request and response code
* HTTP Referer
* User Agent
* TLS protocol version/cipher

(We do NOT log your IP address.)

An aggregated version of that data (amount of HTTP requests per TLS protocol/cipher per user agent string per month) is stored for one year.

We collect that data to make informed decisions on when we can disable specific TLS versions.

The frequency of HTTP requests are stored for one year.

In the unlikely case, when your browser detects a security problem on our website, it will submit details about this security event to us via a third party service ([report-uri.com](https://report-uri.com/home/privacy_policy)). This allows us to detect and to respond to security issues.

Email
-----

If you send us an email to our domain your email will be processed by servers operated by [Mailbox.org](https://mailbox.org/). You can encrypt your emails to us using [PGP](https://applied-privacy.net/files/gpg-pubkeys/Foundation_for_Applied_Privacy.asc).

3rd Party Content
-----------------

Your browser will send requests to 3rd party service providers when you visit the following sub-domains:

* [donate.applied-privacy.net](https://donate.applied-privacy.net/) / [spenden.applied-privacy.net](https://spenden.applied-privacy.net/) ([Donorbox](https://donorbox.org/privacy), [Stripe](https://stripe.com/us/privacy), [Google](https://policies.google.com/privacy), [Amazon](https://aws.amazon.com/privacy/))

We have no control over their logging and privacy practices.

We recommend to use [Tor Browser](https://www.torproject.org/download/download-easy.html.en) for the web and GPG for email.

Changes
-------

* 2021-08-07: remove status.applied-privacy.net from 3rd party section
* 2020-11-15: DNS Privacy Services: We no longer store country level source information. Added more operational metrics (dnsdist prometheus).
* 2020-02-11: added: IP-version logging to better understand the impact of IPv6 issues.
* 2019-12-23: Update DNS domains from appliedprivacy.net -> applied-privacy.net
* 2019-05-31: added: DoH error logging to understand and solve software bugs

[![](../files/img/mastodon.png)](https://mastodon.social/@applied_privacy) [![](../files/img/email.png)](mailto:contact(at)appliedprivacy.net) [![](../files/img/twitter.png)](https://twitter.com/applied_privacy) - [Imprint](https://applied-privacy.net/imprint)