[';--](https://haveibeenpwned.com/)

* [Home](https://haveibeenpwned.com/)
* [Notify me](https://haveibeenpwned.com/NotifyMe)
* [Domain search](https://haveibeenpwned.com/DomainSearch)
* [Who's been pwned](https://haveibeenpwned.com/PwnedWebsites)
* [Passwords](https://haveibeenpwned.com/Passwords)
* [API](#)
    * [Overview](https://haveibeenpwned.com/API/v3)
    * [API key](https://haveibeenpwned.com/API/Key)
* [About](#)
    * [Who, what & why](https://haveibeenpwned.com/About)
    * [Privacy](https://haveibeenpwned.com/Privacy)
    * [FAQs](https://haveibeenpwned.com/FAQs)
    * [Pastes](https://haveibeenpwned.com/Pastes)
    * [Opt-out](https://haveibeenpwned.com/OptOut)
    * [Twitter](https://twitter.com/haveibeenpwned)
    * [Facebook](https://www.facebook.com/haveibeenpwned/)
    * [Mastodon](https://infosec.exchange/@haveibeenpwned)
    * [Suggest a feature](https://haveibeenpwned.uservoice.com/)
    * [Breaches](http://feeds.feedburner.com/HaveIBeenPwnedLatestBreaches)
* [Donate](https://haveibeenpwned.com/Donate)

Privacy policy
==============

How we protect your personal information
----------------------------------------

### About us and what we do

HaveIBeenPwned.com (**HIBP**) is owned and operated by Superlative Enterprises Pty Ltd ABN 62 085 442 020 (**"Superlative"**, **"we"** or **"us"**), a small business based in the state of Queensland, Australia. We have created this policy to explain what limited personal information we collect when you use the HIBP site and how we handle and protect your personal information.

HIBP's purpose is to help individuals and organisations combat violations of privacy by enabling them to identify when information has been involved in a data leak. HIBP helps create visibility as to how personal data spreads. Individuals and organisations may no longer be able to control information once it is breached, however, they can at least understand what has been leaked, where it has been leaked from and what precautionary measures should be taken as a result.

HIBP delivers a range of free and paid services to individuals and organisations anywhere in the world to help them determine if they have been impacted by a data breach, including:

* a point-in-time search to check whether an email address entered by an individual into the HIBP search engine has been involved in a data breach;
* a point-in-time search to find all breached email addresses on a domain verified as controlled by the enquirer;
* a point-in-time search for real world passwords previously exposed in data breaches;
* a subscriber service for verified individuals to be notified of data breaches connected to their email address; and
* a subscriber service for enterprises and individuals to assist in monitoring breaches.

### What kinds of personal information do we collect and hold?

When we use the term personal information, we mean any information or an opinion about an individual who is identified or reasonably identifiable to us. Personal information is sometimes also referred to as personal data. We only collect the limited personal information we need for the purposes of providing our services.

We collect and hold email addresses for the purposes of providing our subscription services to verified email addresses.

We collect and hold only the bare minimum logging information required to keep the service operational and combat malicious activity. This includes transient web server logs, Google Analytics to assess usage patterns and Application Insights for performance metrics. These logs may include information submitted in a form by the user, browser headers such as the user agent string and, in some cases, the user's IP address.

We do not collect or store your personal information when you conduct a search in the HIBP database. Searching for an email address or phone number only ever retrieves the data from storage then returns it in the response. The data from the search is not explicitly stored anywhere.

We also store some lists of data classes that were impacted in a particular data leak that is loaded into HIBP. For example, we will state that email addresses and passwords appeared in a leak but will not provide any information about which email addresses had corresponding compromised passwords.

The information we collect is not always personal information, as it may not relate to an identified individual or we otherwise may not be able to identify you from it.

[The Pwned Passwords feature](https://haveibeenpwned.com/Passwords) searches compromised passwords from data leaks for the presence of a user-provided password. The password is hashed client-side with the SHA-1 algorithm then only the first 5 characters of the hash are sent to HIBP following [the Cloudflare k-anonymity implementation](https://blog.cloudflare.com/validating-leaked-passwords-with-k-anonymity/). HIBP never receives the original password nor enough information to discover the original password. No identifying information about who the password belongs to is stored.

Sensitive information is a subset of personal information that includes health information and other forms of sensitive personal information, and generally requires a higher level of privacy protection than other types of personal information. We do not collect sensitive information.

### How do we collect, hold and use personal information?

_Collection_

We collect personal information:

* from individuals directly, who subscribe to our services; and
* from third parties, such as breached organisations, where Superlative can verify the legitimacy of a breach.

_Storage_

When a data breach is loaded into HIBP by Superlative, the email addresses are stored in the online system. In limited cases, phone numbers are loaded in separately where they exist in an isolated data store not attached to any other personal information. Phone numbers are not linked to any corresponding email addresses. No other data of any kind (like names) is stored on data load.

Superlative securely stores the personal information we hold in a Western United States of America Microsoft Azure data centre.

_Uses_

We use the personal information we hold for the purpose of providing our services.

Our subscriber database is checked when new breach data is loaded to establish if the subscriber appears in a new breach, and to send an email notification to the subscriber if required. These email notifications are only ever sent to subscribers who ‘double' opt-in to receive notifications. This involves entering an email address on the notification page or domain search page, and then successfully proving control of the email address through email verification. The verification email contains a unique link which must be followed to confirm the subscriber opts-in. Anti-automation measures are in place to limit attempts to subscribe email addresses in bulk.

_Sensitive data breaches_

Data breaches that we flag as sensitive are not returned in public searches, they can only be viewed by using the subscription service and verifying ownership of the relevant email address first. Sensitive breaches are also searchable by domain owners who prove they control the domain using the domain search feature. For more information about how we flag sensitive breaches, see [Here's how I'm going to handle the Ashley Madison data](https://www.troyhunt.com/heres-how-im-going-to-handle-ashley/).

### Who do we disclose your information to, and why?

We only disclose the limited personal information required for the purposes of providing our services.

_Domain searches_

Domain searches allow the exposure of all email addresses on that domain to be returned in a single search. Only someone who controls the domain or the website it is bound to can perform a search via one of the verification processes:

* Via email address on the WHOIS record
* Via a common security or administrative email address (security@, hostmaster@, postmaster@, webmaster@)
* Via a meta tag with a unique code placed on the website
* Via a file with a unique code uploaded to the website
* Via a txt entry on the DNS record with a unique code
* A domain search logs the domain name and requestor's IP address as part of anti-abuse measures.

If you ask Superlative to notify you of future appearance of email addresses on that domain and you provide your email address so it can be notified, that email address is also stored. Anti-automation measures are in place to limit attempts to automate searches.

When someone subscribes to notifications or searches a domain, that information is not passed to any third parties under any circumstances other than to send email using the SendGrid service.

### Will we disclose your information overseas?

We store all personal information securely in a Western United States of America Microsoft Azure data centre. This data is not shared or disclosed to any third parties overseas.

### How do we protect your data?

Security on HIBP is handled by a "defence in depth" approach, that is the service employs many different layers of security including (but not limited to):

* all data transmitted over the internet is done over HTTPS;
* Cloudflare is used extensively to block potentially malicious requests;
* rate limits on APIs are implemented at both the code level and via Cloudflare;
* regular security scans are performed to identify code or configuration vulnerabilities;
* firewalls are employed to limit access to services running on Microsoft Azure; and
* disclosure of any security vulnerabilities are encouraged via [the security.txt file](https://haveibeenpwned.com/.well-known/security.txt).
* Third party components are kept well-maintained (see [OWASP's Using Components with Known Vulnerabilities](https://owasp.org/www-project-top-ten/2017/A9_2017-Using_Components_with_Known_Vulnerabilities.html)).

### Access to and correction of your personal information

_Access_

You may access the limited information we hold about you in the HIBP platform in real time. Where there are sensitive breaches, we verify that the requester is the person to whom the information relates prior to allowing access.

_Correction_

To ensure the quality and accuracy of the information we publish, we limit the information we collect and take steps to verify identified and reported breaches. Once we receive personal information known to be involved in a verified data breach, the information cannot be changed retroactively.

_Sensitive data breaches_

Data breaches flagged as sensitive are not returned in public searches. If you wish to prevent any other breached information from being publicly associated with your email address, please utilise our opt-out feature detailed below.

In certain circumstances, subscribers may request correction to their personal information, such as their contact email address, by contacting us. Our contact details are set out below.

### Unsubscribing and opt-out

_By email_

Every breach notification email that we send contains an unsubscribe link in the footer. If you would like to unsubscribe but cannot find a recent email from us, use [the notification service](https://haveibeenpwned.com/NotifyMe) to send another email to yourself and that will contain the unsubscribe link.

_Using our opt-out feature_

Superlative provides [an opt-out feature](https://haveibeenpwned.com/OptOut) for HIBP that, if used, removes an email address from public visibility. The opt-out feature provides you with 3 different ways to control how your personal data is stored and accessed:

* Just removal from public searches: The public email address search no longer returns your address. Your address is still stored, you can still see breaches against it by verifying control with the notification service and anyone control the domain your address is on can continue to see breaches against it using the domain search feature.
* Remove all current and future breaches: No existing breaches impacting your address nor any occurring in the future will be stored against your address. No searches of any kind will return a breach associated with your address. Your address is retained alongside instructions to never load future breaches against it.
* Remove the email address entirely: The address and associated breaches are permanently removed. If a future breach is loaded that includes your address, it will become publicly searchable again.

### Questions, concerns or complaints

If you have any questions, concerns or complaint about the way in which we have handled your personal information, you should contact us in the first instance. Our contact details are set out below.

We will endeavour to reply to you within a reasonable time following receipt of the complaint and, where appropriate, will advise you of the general reasons for the outcome of the complaint.

If you remain unsatisfied with the way in which we have handled a privacy issue, you may approach an independent advisor. There is more information and guidance on the website of the Office of the Australian Information Commissioner ([www.oaic.gov.au](https://www.oaic.gov.au/)) about protecting your privacy.

### Our contact details

If you have any questions, please contact us at:

Superlative Enterprises  
Level 11  
2 Corporate Court  
Bundall 4217  
Queensland  
Australia  
[support.haveibeenpwned.com](https://support.haveibeenpwned.com/)  
[support@haveibeenpwned.com](mailto:support@haveibeenpwned.com)

### Changes to this policy

From time to time, we may change our Privacy Policy on how we handle personal information or the types of personal information which we hold. Any changes to our Privacy Policy will be published on our website.

You may obtain a copy of our current Policy from our website or by contacting us at the contact details above.

×

#### Notify me

Get notified when future pwnage occurs and your account is compromised.

Using Have I Been Pwned is subject to [the terms of use](https://haveibeenpwned.com/TermsOfUse)

You've just been sent a verification email, all you need to do now is confirm your address by clicking on the link when it hits your mailbox and you'll be automatically notified of future pwnage. In case it doesn't show up, check your junk mail and if you _still_ can't find it, you can always repeat this process.

* * *

add another address[](https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Fhaveibeenpwned.com)[](https://twitter.com/intent/tweet?url=https%3A%2F%2Fhaveibeenpwned.com&text=Have%20you%20been%20pwned%3F%20Get%20told%20when%20you%20are%20with%20a%20free%20%40haveibeenpwned%20subscription)

* * *

[Privacy policy](https://haveibeenpwned.com/Privacy) | [Terms of use](https://haveibeenpwned.com/TermsOfUse)

[](https://www.facebook.com/haveibeenpwned)[](https://twitter.com/haveibeenpwned)[](https://www.troyhunt.com/contact/)