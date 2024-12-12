This site needs Javascript for some functionality to work properly

[Skip to main content](#main)

[![Mullvad logo, to the homepage](/_app/immutable/assets/logo.Ba5MUFAA.svg)](https://mullvad.net/en/)

* [About](https://mullvad.net/en/about)
* [Products](#)
    * [VPN](https://mullvad.net/en/vpn)
    * [Browser](https://mullvad.net/en/browser)
    * [Search](https://leta.mullvad.net/)
    * [Encrypted DNS](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls)
    * [Browser Extension](https://mullvad.net/en/help/mullvad-browser-extension)
* [Blog](https://mullvad.net/en/blog)
* [Pricing](https://mullvad.net/en/pricing)
* [Servers](https://mullvad.net/en/servers)
* [Downloads](https://mullvad.net/en/download)
* [Help](https://mullvad.net/en/help)

 Snow [Account](https://mullvad.net/en/account) [Get started](https://mullvad.net/en/account/create)

No-logging of user activity policy
==================================

[Policies](https://mullvad.net/en/help?Topic=policies) 

Last updated: May 16, 2024

We do not keep activity logs of any kind. Learn more about what this means and why we choose to operate this way.

What this policy covers
-----------------------

* [Policy overview](#overview)
* [Our anonymous, numbered accounts](#numbered)
* [How we handle payment information](#payments)
* [Information that we do not log](#no-logs)
* [Other data that we do handle](#data-handling)
* [How we handle emails and problem reports](#email)

### All of our policies regarding data and its storage

* [No logging of user activity policy](https://mullvad.net/help/no-logging-data-policy/)
* [Cookie policy](https://mullvad.net/help/cookie-policy)
* [Privacy policy](https://mullvad.net/help/privacy-policy) (including GDPR)
* [Swedish legislation relevant to us as a VPN provider](https://mullvad.net/help/swedish-legislation/)
* [Terms of service](https://mullvad.net/help/terms-service/)

Policy overview
---------------

The underlying policy of Mullvad is that we never store any activity logs of any kind. We strongly believe in having a minimal data retention policy because we want you to remain anonymous.

However, in some situations we might process your personal data if you, for example, are making payments by a bank wire, PayPal, Swish, Stripe or are sending an e-mail or reporting a problem. In those cases, we might process your personal data and the General Data Protection Regulation (“GDPR”) and other data protection laws may apply. For more information please [read our Privacy Policy](https://mullvad.net/help/privacy-policy).

Our anonymous, numbered accounts
--------------------------------

We want you to remain anonymous. When you sign up for Mullvad, we do not ask for any personal information – no username, no password, no email address. Instead, a random account number is generated, a so-called numbered account. This number is the only identifier a person needs in order to use a Mullvad account. This is a fundamental difference that sets us apart from most other services.

Anyone at anytime can create as many numbered accounts as they wish on our website. An account can be used by multiple people or by someone other than the person who initially generated it.

A Mullvad account has two properties: the account number and the time remaining on that account.

**Question:** How many numbered accounts does Mullvad have?  
**Answer:** At the time of writing this post, Mullvad has 555,541 numbered accounts. These accounts could have been created by 555,541 unique people, or by one person 555,541 times.

Data that we store for an account¹

account number | expiry date
xxxxxxxxxxx    | 20170730

Data stored for WireGuard@ configuration (if used)

account number | pubkey    | tunnel address
xxxxxxxxxxxx   | xxxxxxxx  | x

How Mullvad handles payment information
---------------------------------------

You can pay money to the numbered account and therefore acquire more VPN time. Mullvad accepts cash, Bitcoin, Bitcoin Cash, Monero, bank wire, credit card, PayPal, and Swish. You can find more information on how we handle each type of payment below.

Some types of payment mean that personal data will be processed (such as e.g. bank account number and PayPal-ID). If you choose a payment method where you are providing your personal data to Mullvad, such as PayPal, we will process and protect your information according to the GDPR and other applicable legislations. For more information please read our [Privacy policy](https://mullvad.net/help/privacy-policy/).

### Cash

Put the money in an envelope together with the payment token and send it to us. We will open the envelope, add time to the account (corresponding to the amount of cash sent), and then use a shredder to destroy the envelope and its non-money contents.

We have no way of knowing who made the payment and who the account belongs to. Even if a person were to address the envelope, there is still no way to prove that he or she generated the account or is even using it. Please avoid writing your name or address on the envelope.

The GDPR does not apply in this case since the personal data on the envelope does not form a part of a filing system and are not intended to form part of a filing system.

This is what we store when a cash payment comes in¹:

    payment | account number | amount | currency | timestamp
    xxxxxx  | xxxxxxxxxxxx   | 5.0    | USD      | 2016-12-09 10:38:23

### Cryptocurrencies

We support payments in the following cryptocurrencies:

* Bitcoin
* Bitcoin Cash
* Monero

We run our own full node for each currency and we self-host all wallets. No third parties are involved. The record of a cryptocurrency transaction contains the amount, currency, and a timestamp which is truncated to only store the date after 40 days. In the case of Bitcoin and Bitcoin Cash we also store the unique receiving address that is generated for each payment. This is also removed after 40 days. For Monero payments we store the transaction hash, or tx\_hash. This is stored beyond 40 days in order to prevent double-crediting.

### Credit card, PayPal, Swish, and bank wire

For credit card, PayPal, Swish, and bank wire, we do use third parties: Stripe, PayPal, and our bank SEB (which handles both Swish and bank wire). These kinds of companies log everything. For that reason alone, it is out of our control that they have records showing which people have paid us money (i.e. processing of personal data).

As a customer of their services, these entities would allow us to request this information if we chose to do so. In short, your payment actions with these two methods are not anonymous and the GDPR and other relevant data protection regulations may apply if you are making a payment by credit card, PayPal, Swish or by bank wire.

The data must be kept for the statutory retention period described in  applicable local laws such as the Swedish Accounting Act (some information must be stored for seven years from the end of the fiscal year). If not required by law, the data will be stored for no longer than necessary for the purpose. After the periods, the data will be permanently deleted.

Here's the information we store for bank wires¹:

    payment | account number | amount | currency | timestamp           | transaction_id*
    xxxxxx  | xxxxxxxxxxxx   | 30     | EUR      | 2016-12-09 00:01:06 | xxxxxxxxx
    

`*transaction_id is deleted 40 days after payment`

Here's the information we store for credit card payments via Stripe¹:

    payment | account number | amount | currency | timestamp*          | stripe_charge_id*
    xxxxxx  | xxxxxxxxxxxx   | 10     | EUR      | 2016-12-15 20:42:26 | xxxxxxxxx
    

`*`stripe\_charge\_id and the time part (hh:mm:ss) of timestamp is deleted 40 days after payment

Here's the information we store for Swish¹:

    payment | account number | amount | currency | timestamp           | swish_request_id
    xxxxxx  | xxxxxxxxxxxx   | 50     | SEK      | 2016-12-15 20:42:26 | xxxxxxxxx
    

`*`swish\_request\_id and the time part (hh:mm:ss) of timestamp is deleted 40 days after payment  

Here's the information we store for PayPal transactions¹:

    payment | account number | amount | currency | timestamp*          | transaction_id* 
    xxxxxx  | xxxxxxx        | 15     | EUR      | 2016-12-10 06:40:00 | xxxxxxxxxxxxx    

\*transaction\_id and the time part (hh:mm:ss) of timestamp are deleted 40 days after payment

**Question:** Why do you store transaction\_id and payment tokens?  
**Answer:** Since we support 30-day refunds and because we encounter certain transaction issues from PayPal (for example, double payments and subscription problems), we need to be able to track payments in order to give customers the service we offer. We only duplicate the information since PayPal already has it.

It's important to note that payment processors like PayPal and Stripe do not have your Mullvad account number. We send them a token\* to link the payment to your account. If, however, you send a bank wire payment, the account number will exist in the "message" field of the transaction.

You should also use a token\* when sending us cash. Do not write down the account number.

### Activation codes

Here's the information we store for activation codes¹:

    payment | account number | amount | timestamp           | voucher id | activation code
    xxxxxx  | xxxxxxxxxxxx   | 30     | 2016-12-09 00:01:06 | xxxxxx     | xxxxxxxxxxx
    

### in-app purchases on iOS

Here's the information we store for iOS purchases:

    payment | account number | amount | timestamp           
    xxxxxx  | xxxxxxxxxxxx   | 5      | 2016-12-09 00:01:06 

### Partner accounts

For accounts created by partners, we don't store payment information.  
Instead we store information on when time was added to or refunded from an account:

event id | time added/removed | account number | timestamp          
xxxxxx   | 1234               | xxxxxxxxxxxx   | 2016-12-09 00:01:06

### Tokens

A token is created for all payment methods except cryptocurrencies and bank wire. The token, instead of your account number, is sent to the payment processor and used as a reference to link a payment to your account.

This token expires after 40 days and is no longer possible to link to your account. Cash tokens that haven’t been accounted for, however, are stored for 120 days in case postal service is slow.

What we don't log
-----------------

We log nothing whatsoever that can be connected to a numbered account's activity:

* no logging of traffic
* no logging of DNS requests
* no logging of connections, including when one is made, when it disconnects, for how long, or any kind of timestamp
* no logging of IP addresses
* no logging of user bandwidth
* no logging of account activity except total simultaneous connections (explained below) and the payment information detailed in this post.

Our OpenVPN server log configuration:

    verb 0
    log-append /dev/null

**Question:** How can you limit the maximum number of simultaneous connections if you're not logging that information?  
**Answer:** Each VPN server reports to a central service. When a customer connects to a VPN server, the server asks the central service to validate the account number, whether or not the account has any remaining time, if the account has reached its allowed number of connections, and so on. Everything is performed in temporary memory only; none of this information is permanently stored to disk.

Providing a reliable service
----------------------------

We want to ensure that everyone using our VPN experiences a reliable and stable service. Through the years we have implemented changes to ensure that even if our API fails we can still continue to provide a VPN that can be relied upon.

This was a way of resolving [MUL-03-002 WP2 from our Infrastructure Audit](https://mullvad.net/blog/2021/1/20/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit/) in 2020.

For our OpenVPN relays we have implemented Fail2ban to block non-authorized or malicious attempts at gaining account time.

Fail2ban works by reading from a frequently wiped list of malicious unauthorized IP addresses in RAM (tmpfs). Regular paying customers and successful connections are not included in this, it is only to prevent any bruteforce attempts.

**Question**: Does that mean if I try to authenticate to an OpenVPN server I will have my IP address logged?

**Answer**: No. We do not log customers that have a valid account token. This blocking is limited to bad actors trying to gain free account time with non-existent, invalid account numbers.

Other data that we do handle
----------------------------

Our servers send two types of data to our monitoring system:

* aggregated application data, such as total number of current vpn connections
* generic system metrics, such as CPU load per core and total bandwidth used by the server.

We log the total sum of each of these statistics in order to monitor the health of each individual VPN server. We ensure that the system isn't overloaded, and we monitor the servers for potential attacks, bugs, and network issues.

We also monitor the real-time state of total connections per account as we only allow for five connections simultaneously. As we do not save this information, we cannot, for example, tell you how many connections your account had five minutes ago.

With regard to our web servers, we handle certain types of information in the following ways:

* We store Nginx access logs for up to 5 minutes in the following format (which does not contain IPs): $server\_name \[$time\_local\] $request $status
* Information older than 5 minutes is deleted, and only aggregated information about the number of requests and their response codes is saved.
* We refrain from sending usage statistics to external parties such as Google Analytics.
* Our website utilizes a minimum amount of cookies. Please read [our cookie policy](https://mullvad.net/help/cookie-policy) for more information.

How we handle emails and problem reports
----------------------------------------

Our support staff answers questions, resolves problems, and gives general support to customers who actively send an email to support@mullvadvpn.net or submit a problem report via our app/client.

Please consider the following statements about how we handle support-related communication should you ever need to contact us.

1. If privacy is of utmost concern, we recommend that you refrain from communicating any personal data to us since plain-text email is not a safe media for communication. If necessary, [use PGP-encrypted email](https://mullvad.net/help/using-encrypted-email/).
2. After "solving" or "closing" a support case, all related emails are archived (removed from the inbox).
3. After 6 months, all emails sent to our support address are automatically, permanently erased (from inbox, deleted items, sent items, trash, and archives).
4. We do use a third party to operate our email service, so we remind you to carefully read #1 again.
5. No private information  not even your email address  will ever actively be passed to third parties (except the third party which operates our email service on behalf of us), unless you explicitly ask us to.
6. Please note that an e-mail address is generally considered as personal data and even the information in the e-mail message may include personal data.

App telemetry
-------------

To make sure that the user have the most secure version and to inform the user of any issues with the current version that is running, the app performs version checks automatically. This sends the app version and operating system version to Mullvad servers. Mullvad keeps counters on number of used app versions and Android versions. The data is never stored or used in any way that can identify the user or anything about them.  
  
If the split tunneling feature is used on Android, then the app queries the system for a list of all installed applications in order to let the user choose which apps should communicate outside the VPN tunnel. This list is only retrieved in the split tunneling view. The list of installed applications is never sent from the device.  
 

Browser data handling
---------------------

Here are the full list of requests Mullvad Browser makes by default:  
  
    1. Browser update (Mullvad)  
    2. Mullvad Browser Extension update (Mullvad)  
    3. Mullvad DoH (Mullvad)  
    4. NoScript/Ublock Origin update (Mozilla)  
    5. Certificates & Domains update (Mozilla)  
    6. Ublock Origin filter lists update (various lists)  
  
Mullvad does not collect any personal information in relation to above requests.  
 

Mullvad
-------

* [About](https://mullvad.net/en/about)
* [Help](https://mullvad.net/en/help)
* [Servers](https://mullvad.net/en/servers)
* [Pricing](https://mullvad.net/en/pricing)
* [Blog](https://mullvad.net/en/blog)
* [Mullvad VPN](https://mullvad.net/en/vpn)
* [Mullvad Browser](https://mullvad.net/en/browser)
* [Why privacy matters](https://mullvad.net/en/why-privacy-matters)
* [Why Mullvad VPN?](https://mullvad.net/en/why-mullvad-vpn)
* [What is a VPN?](https://mullvad.net/en/vpn/what-is-vpn)
* [Downloads](https://mullvad.net/en/download)
* [Stop chat control](https://mullvad.net/en/chatcontrol)
* [Press](https://mullvad.net/en/press)
* [Jobs](https://www.mullvad.careers/)

Policies
--------

* [Policies](https://mullvad.net/en/policies)
* [Open source](https://mullvad.net/en/open-source)
* [Privacy policy](https://mullvad.net/en/help/privacy-policy)
* [Cookies](https://mullvad.net/en/help/cookie-policy)
* [Terms of service](https://mullvad.net/en/help/terms-service)
* [Partnerships and resellers](https://mullvad.net/en/help/partnerships-and-resellers)
* [Reviews, ads and affiliates](https://mullvad.net/en/help/policy-reviews-advertising-and-affiliates)
* [Reporting a bug or vulnerability](https://mullvad.net/en/help/how-report-bug-or-vulnerability)

Address
-------

Mullvad VPN AB

Box 53049

400 14 Gothenburg

Sweden

[support@mullvadvpn.net](mailto:support@mullvadvpn.net)

* [GPG key](https://mullvad.net/static/gpg/mullvadvpn-support-mail.asc)
* [Onion service](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion/)

Follow us
---------

* [@mullvadnet](https://www.x.com/mullvadnet)
* [@mullvadnet](https://mastodon.online/@mullvadnet)
* [Mullvad VPN](https://www.youtube.com/c/MullvadVPNNet)
* [mullvad](https://github.com/mullvad)

Language
--------

English

* [العربيّة](https://mullvad.net/en/setlocale/ar?page=/en/help/no-logging-data-policy)
* [Dansk](https://mullvad.net/en/setlocale/da?page=/en/help/no-logging-data-policy)
* [Deutsch](https://mullvad.net/en/setlocale/de?page=/en/help/no-logging-data-policy)
* [English](https://mullvad.net/en/setlocale/en?page=/en/help/no-logging-data-policy)
* [Español](https://mullvad.net/en/setlocale/es?page=/en/help/no-logging-data-policy)
* [فارسی](https://mullvad.net/en/setlocale/fa?page=/en/help/no-logging-data-policy)
* [Suomi](https://mullvad.net/en/setlocale/fi?page=/en/help/no-logging-data-policy)
* [Français](https://mullvad.net/en/setlocale/fr?page=/en/help/no-logging-data-policy)
* [Italiano](https://mullvad.net/en/setlocale/it?page=/en/help/no-logging-data-policy)
* [日本語](https://mullvad.net/en/setlocale/ja?page=/en/help/no-logging-data-policy)
* [한국어](https://mullvad.net/en/setlocale/ko?page=/en/help/no-logging-data-policy)
* [Nederlands](https://mullvad.net/en/setlocale/nl?page=/en/help/no-logging-data-policy)
* [Norsk](https://mullvad.net/en/setlocale/no?page=/en/help/no-logging-data-policy)
* [Polski](https://mullvad.net/en/setlocale/pl?page=/en/help/no-logging-data-policy)
* [Português](https://mullvad.net/en/setlocale/pt?page=/en/help/no-logging-data-policy)
* [Русский](https://mullvad.net/en/setlocale/ru?page=/en/help/no-logging-data-policy)
* [Svenska](https://mullvad.net/en/setlocale/sv?page=/en/help/no-logging-data-policy)
* [ภาษาไทย](https://mullvad.net/en/setlocale/th?page=/en/help/no-logging-data-policy)
* [Türkçe](https://mullvad.net/en/setlocale/tr?page=/en/help/no-logging-data-policy)
* [简体中文](https://mullvad.net/en/setlocale/zh-hans?page=/en/help/no-logging-data-policy)
* [繁體中文](https://mullvad.net/en/setlocale/zh-hant?page=/en/help/no-logging-data-policy)