About
-----

[This site](https://ip.wtf/) shows you information about your [IP address](https://en.wikipedia.org/wiki/IP_address) and web browser.

It's not going to try to sell you a VPN. Don't listen to the misinformation about VPNs, instead watch [this excellent](https://www.youtube.com/watch?v=WVDQEoe6ZWY) Tom Scott video.

API
---

Is there an API? Yes.

At its simplest you can do:

    
    $ curl ip.wtf
    [your IP]

To get the IP address you're connecting from; the API detects access from curl and automatically defaults to just the text version.

In code add a header `Accept: text/plain` to get the plain text version. You can also use `application/json` to get a bit more information.

JavaScript example:

    let res = await fetch("https://ip.wtf", { headers: { Accept: "application/json" } });
    let data = await res.json();
    console.log(data);
    

Which gives you:

If you use the hostname `ip.wtf` the client (browser or other HTTP client) will pick the IP protocol to use. You can also use the hostnames `v4.ip.wtf` or `v6.ip.wtf` to force a particular protocol, or otherwise ask the client to pick the relevant protocol.

For example with curl you can do:

    $ curl -4 ip.wtf
    $ curl -6 ip.wtf
    

Access works over http or https; API access from a non-browser is never redirected to HTTPS (browsers may choose to use HTTPS though). If you want to force HTTP you can use the hostnames `nossl.ip.wtf` or `neverssl.ip.wtf`. (You can also use those hostnames manually in a similar way to [neverssl.com](http://neverssl.com/).)

Reasonable use is fine (i.e. 1 req/hour per source IP and not in something that is widely deployed). If you need more contact us first, we reserve the right to block unreasonable access otherwise.

Fun
---

For a little easter egg try: `curl ip.wtf/moo`

There's a small collection of fun things, which is slowly growing into a set of demos; see [ip.wtf/fun](https://ip.wtf/fun).

Privacy
-------

This site collects data about your device and connection to the site in order to implement its primary purpose of showing you this information.

The information displayed includes your IP address and hostname.

Depending on your configuration some of the tests performed by this site may reveal a different IP address; this data is only aggregated client side and never stored on a server.

In order to look up your hostname a reverse DNS lookup is performed, this uses a third party DNS provider (Google Public DNS, see [privacy](https://developers.google.com/speed/public-dns/privacy)).

Any information collected that identifies your IP address is not stored for longer than one day, unless necessary to prevent abuse of the site, or if you otherwise share the data with us (e.g. send us an email, etc.).

This site does not use cookies, or store data on your device.

Licenses
--------

This product includes GeoLite2 data created by MaxMind, available from [https://www.maxmind.com](https://www.maxmind.com/).

On Windows the flag emojis are provided by Twemoji, via [country-flag-emoji-polyfill](https://github.com/talkjs/country-flag-emoji-polyfill), via [Mozilla's Twemoji-colr](https://github.com/mozilla/twemoji-colr/blob/master/LICENSE.md) used under CC-BY-4.0; Copyright 2019 Twitter, Inc and other contributors.

The site itself is available under the 0BSD licence, see [http://©.st/dgl](http://xn--gba.st/dgl).

Sponsor
-------

This site is open source, [contributions welcome](https://github.com/dgl/ip.wtf). If you like this, you can say thank you: [ko-fi.com/webgl](https://ko-fi.com/webgl). See [dgl.cx](https://dgl.cx/) for more on my projects.

Contact
-------

You can

[email me](https://dgl.cx/contact)

(click twice due to abuse prevention measures).