[Skip to main content](#main-content)

 [![logo](/hc/theming_assets/01HZH483AFP40K6C397WVA97SZ) ![logo](/hc/theming_assets/01HZH483EMG5ACQN09F3CQ9JF0)](https://fastmail.com/)

[Help Center](https://www.fastmail.com/hc/en-us)

[View or create a support ticket](https://support.fastmail.com/support) [Try for free](https://www.fastmail.com/signup/)

How can we help?

 

1. [Fastmail](https://www.fastmail.com/hc/en-us)
2. [Security](https://www.fastmail.com/hc/en-us/categories/360006005393-Security)
3. [Security basics](https://www.fastmail.com/hc/en-us/sections/1500000062142-Security-basics)

How Fastmail provides a secure service
======================================

We have a great responsibility at Fastmail to keep your email secure. We continually review our code and processes for potential vulnerabilities and we take new measures wherever possible to further secure your data. On this page, we list some of the core things we do to maintain security.

* [Customer data](#customerdata)
* [Secure access to mail](#secureaccess)
* [Encrypted sending/receiving](#encryptedsendreceive)
* [Content security policy](#contentsecurity)
* [Necessary communications](#communications)
* [Software updates](#updates)
* [Software system security](#serioussecurity)
* [Image loading privacy](#imageloading)
* [Bug bounty](#bugbounty)
* [Physical location security](#physicalsecurity)
* [On-disk encryption](#diskencryption)
* [Staff access to your data](#staffaccess)
* [Password encryption](#passwordencryption)
* [Transfer of data with third parties](#transferdata)
* [Destruction of data](#datadelete)
* [Limitations](#limitations)

Customer data
-------------

We know that email is free-form, and could contain all kinds of information about our customers and other people they correspond with, including data of the most confidential sort. Due to the nature of our business (hosting and forwarding free-form emails), our systems process large amounts of potentially highly confidential data.

For this reason, we treat all personal data belonging to our customers as Customer Confidential (**“your data**”), which is the highest level of protection within our data modeling.

To provide the services we offer, it is necessary for our computer systems to process unencrypted and unobfuscated data (for example: to build the search indexes which allow fast message retrieval, or to push alarm notifications for calendar events).

Secure access to mail
---------------------

We mandate all connections to our servers use [Transport Layer Security (TLS) and Secure Sockets Layer (SSL)](https://en.wikipedia.org/wiki/Transport_Layer_Security) encryption, for all connections including webmail, the [Fastmail official app](https://www.fastmail.help/hc/en-us/articles/360060590873), and IMAP/POP/SMTP email client access. This prevents eavesdropping, tampering, and message forgery on any communication between your computer or phone and our servers.

We have full support for [Perfect Forward Secrecy](https://en.wikipedia.org/wiki/Perfect_forward_secrecy) (PFS) with our encrypted connections, which ensures that even if we were somehow compromised in the future, no previous communication could be decrypted. All connections in supporting browsers have been protected by PFS since July 2012.

A [Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security) header is sent with all of our webpages. This tells all modern browsers to **only** connect to us over an encrypted connection, even if you have a bookmark, click a link or type a URL to an insecure page at our site.

Encrypted sending/receiving
---------------------------

Whenever you send a message to someone outside of Fastmail we have to send it across the open internet. Since January 2010 we have fully encrypted all connections between us and the receiving server whenever the other server supports it, preventing passive eavesdropping, tampering or forgery. Similarly, we have accepted encrypted connections for mail delivery **to** our servers since April 2009, and we encourage all servers connecting to us to use it.

Content security policy
-----------------------

Within our web interface we set a [Content Security Policy](http://content-security-policy.com/) header, which ensures that only scripts we've written can be run. This means that a potentially-malicious email that somehow managed to slip through our filters would still not be able to do anything dangerous.

We use isolated domains to separate out untrusted content from the pages we generate. For example, when you open an attachment, it opens at `fastmailusercontent.com` rather than `fastmail.com`. Thanks to browser cross-origin security restrictions, this means that a rogue attachment can never access any of your data.

Similarly, [user websites](https://www.fastmail.help/hc/en-us/articles/1500000280141) are hosted on subdomains of `user.fm`, keeping them isolated from our site as well.

We only allow necessary communications
--------------------------------------

Many unexpected forms of attack come from failing to close potential vulnerabilities, including database port access, SSH port access, and so forth. We use [kernel-level firewalling](http://www.netfilter.org/) to only allow connections to the services provided by each machine.

We keep track of software updates
---------------------------------

Software contains bugs. We track the software we use and any security vulnerabilities, and upgrade as soon as an issue is reported.

We use software systems that take security seriously
----------------------------------------------------

We use [Debian](https://www.debian.org/security/) and [Joyent SmartOS](https://www.joyent.com/smartos) as our operating systems because they both take their security responsibilities and updates seriously. In most cases, an update for a security problem will be available within hours of the original report.

Privacy: Image loading
----------------------

When accessing your email through our web interface, we protect your privacy by fetching all referenced images through our servers. This prevents the owner of the image from being sent additional information about you such as your internet address (which reveals your rough location), browser information, and sometimes even tracking cookies.

Bug bounty
----------

We run a tight ship, but we're only human and humans can make mistakes. That's why we run a [bug bounty](https://www.fastmail.com/about/bugbounty.html) program to encourage responsible disclosure of security issues and to reward security researchers who take the time to help us keep Fastmail safe.

Physical location security
--------------------------

Our main servers are located at 365 Data Centers in Bridgewater, New Jersey, USA. Their facility is a high-security, video-monitored location with backup power, air conditioning, fire systems, 24x7x365 monitoring, and onsite technical support. 

365 does a whole lot more to ensure security, including their hardware, best-practices, and routines. You can read all about them [on their homepage](https://365datacenters.com/).

Our secondary sites at 365's Seattle location have equivalent physical security.

We use “remote hands” staff from the data centers to perform routine maintenance on our servers (e.g. replacing hard disks or installing new machines), however, they do not have logins or the ability to access your data.

Our data center vendors provide us with power, cooling, and network links (public internet) but do not manage or have permitted access to our internal network between servers. All public internet-facing machines have a firewall.

All data transfer between our datacentres is over an encrypted VPN (virtual private network) managed by us.

On-disk encryption
------------------

All your data is stored on encrypted disk volumes, including backups. We believe this level of protection strikes the correct balance between confidentiality and availability.

At this stage, some system log data (which could contain personal information) is temporarily stored on un-encrypted disks on individual servers, however, we have an ongoing project to bring encryption to all system logging as well.

Staff access to your data
-------------------------

We limit staff access to customer data as stringently as their roles allow.

Due to the nature of their jobs, it is necessary for our operations staff to have access to the systems where customer data is processed. The staff who do require access to production servers for their jobs are aware of their responsibility to protect the confidentiality of your data, and only access that data where it’s required either to provide customer support or for operational necessity.

Where possible, our systems are designed to allow our support and operational staff to perform their duties without being exposed to your data. Where possible, obfuscated data is presented (like to debug display problems).

Where possible, your explicit consent is sought if viewing unobfuscated data is necessary. In most cases, Fastmail support does this by asking a user to create a folder named “forwebmaster” and place the emails in it. If the folder is titled exactly "forwebmaster" or “for webmaster,” the contents of only this folder will be automatically deobfuscated. This allows support to see specific emails that are moved to the folder, while all other messages in the account remain obfuscated. When support has resolved the issue and no longer needs to look at the message, the user can move the email back out of the folder, and the email will be obfuscated once again. This method can be useful for troubleshooting issues with specific emails, such as problems related to how the message is displayed in our interface. Contents of system Spam folders are also unobfuscated by default.

Due to the nature of their jobs, it may be necessary for our security and fraud staff to have access to deobfuscated customer data or other personal information. 

Sometimes we anonymize your information, for example creating a test case that reproduces a bug found with your data, by making a case that will trigger the same bug without containing any confidential or personally-identifying information.

Password encryption
-------------------

Where you are using a password to access our systems, we store that password in a non-reversible encryption scheme using current best practices.

Where we are storing a password used to access other systems on your behalf (for example, POP links and calendar links), the password is stored with reversible encryption using a key that is stored separately from the encrypted data.

For external sites, passwords for other systems are encrypted, so they can only be decrypted by hardware security modules in our datacenters.

Transfer of confidential data with third parties
------------------------------------------------

Fastmail’s value proposition is “service in exchange for money.” We don’t ever sell or monetize confidential data or even “aggregate customer data.”

As part of our commitment to open source, we do sometimes share statistical data (for example the average size of emails, or the percentage of email traffic which is encrypted or in written particular languages) which is useful in the broader email community to help drive software design.

We also share reports of spam, including spam false positives and false negatives, as well as spam intelligence with our partner organizations who provide us with spam feeds.

We use third-party hosted services for bug tracking, support, exception alerting, and communications. While we don’t send bulk data through any of these services, small pieces of your data may wind up in core dumps, in support ticket updates, inside bug descriptions (we obfuscate where possible, but sometimes the raw data is needed), or in chat messages where colleagues share snapshots of what they’re looking at.

Destruction of data
-------------------

Some of the features of our products are designed specifically around **not** losing data, so while you want us to retain your data, it is replicated to multiple systems and backed up.

When you request destruction of your data by deleting specific items or closing your account, the data is removed in a time-delayed manner. This both allows you to change your mind (undo, or restore from backup), and allows for the possibility that if your account is compromised and the attacker tries to delete everything, we can recover the data.

We also collect some data which is personally identifiable as a side effect of the system monitoring and logging which we require for our operational stability.

**Destruction of system logs**

System logs are retained for 150 to 180 days before being deleted. We have a legitimate interest in having those logs available both to ensure the reliable operation of our systems, and to provide evidence of activity when users report unexpected states in their account.

**Destruction of deleted emails, contacts, and calendars**

Emails, contacts, calendars, and other personal data including notes that have been deleted in Fastmail or Pobox Mailstore are kept in backups for 7 days after deletion.

**Destruction of backup and search index data**

The backup copies of email and search indexes are pruned on an “as-needed” basis based on the ratio of space that would saved by re-compacting them. At the moment there is no guarantee that a particular message will be purged on a timeline, however our support can perform an immediate prune for a particular account on request.

**Destruction of data after account closure**

After an account is terminated, data and backups are purged within a timeframe of between 37 days to 1 year after closure depending on how long the account was active for, whether a custom domain purchased through Fastmail is still present, and whether the account was explicitly closed or lapsed due to lack of payment.

Limitations
-----------

While communication between your computer and our servers is encrypted, any email that you send to another server _may_ have to pass over the internet in an unencrypted form (although we encrypt it wherever possible).

The _only_ way to ensure end-to-end security with email is to use email encryption software such as [Pretty Good Privacy (PGP)](https://en.wikipedia.org/wiki/Pretty_Good_Privacy) or [Secure/Multipurpose Internet mail Extensions (S/MIME)](https://en.wikipedia.org/wiki/Smime). Both of these systems require the creation of certificates, run on your computer, and are attached to your email client to encrypt/decrypt messages.

Providing secure end-to-end encryption via webmail is impossible. There are basically two options, both flawed:

1. Keep a private key on the server and encrypt email on the server
    
    Although all traffic between the server and client may be encrypted via TLS, and then the email itself is encrypted on the server before being sent to the world, the unencrypted email is still available on the server between the TLS and encryption stages.
    
2. Use Java or JavaScript to encrypt email in the browser
    
    Because the script has to run on the user's browser, you could look at the code to see it's secure. In reality, no one would ever do that. In addition, this method can't prevent someone using malicious scripts to send encrypted messages back to the server, as well as the encryption key, for the server to decrypt.
    

In 2007, encrypted email provider [Hushmail](https://www.hushmail.com/) admitted that the U.S. government compelled them to turn over the [unencrypted emails](http://www.wired.com/2007/11/encrypted-e-mai/) of a number of users.

Their contention on how secure they are then relates to what it requires to get a court order. In a [Wired article](http://www.wired.com/2007/11/encrypted-e-mai/), Hushmail stated:

> All Hushmail users agree to our terms of service, which state that Hushmail is not to be used for illegal activity. However, when using Hushmail, users can be assured that no access to data, including server logs, etc., will be granted without a specific court order.

A similar requirement applies to Fastmail, as our [Privacy Policy](https://www.fastmail.com/about/privacy.html) states. We won't release any data without the required legal authorization from an Australian court.

Was this article helpful?

Yes No

258 out of 303 found this helpful

Need help? [Contact our support team](https://support.fastmail.com/support)

##### Get Support

* [Help center](https://www.fastmail.help/)
* [Contact us](https://www.fastmail.com/support/)
* [System status](https://www.fastmailstatus.com/)
* [Report a security issue](https://www.fastmail.com/about/bugbounty/)

[](https://www.fastmail.com/)

[Privacy policy](https://www.fastmail.com/about/privacy/) [Terms of service](https://www.fastmail.com/about/tos/)