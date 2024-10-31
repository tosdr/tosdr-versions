[sourcehut](https://sr.ht/)

[Log in](https://meta.sr.ht/oauth/authorize?client_id=ff4e41c77d9a2ec2&scopes=profile,25ff6e5ce60d7345/data,25ff6e5ce60d7345/info:write&state=%2Fprivacy.md%3F) — [Register](https://meta.sr.ht/)

Privacy policy
--------------

* [article](https://man.sr.ht/~sircmpwn/sr.ht-docs/)
* [source](https://git.sr.ht/~sircmpwn/sr.ht-docs/tree/master/privacy.md?view-source)
* [history](https://git.sr.ht/~sircmpwn/sr.ht-docs/log/master)

### Table of Contents

1. [What we collect and why](#what-we-collect-and-why)
    * [How we share your information with third-parties](#how-we-share-your-information-with-third-parties)
    * [How to access and control the information we've collected](#how-to-access-and-control-the-information-weve-collected)
    * [Changes to this document](#changes-to-this-document)

If you have any questions, please reach out to [sr.ht-support](mailto:~sircmpwn/sr.ht-support@lists.sr.ht) via email.

#### [#](#what-we-collect-and-why)What we collect and why

The only data we require of your account is your email address; a username of your choosing, which must be unique among all users; and a password. Your email and username are stored in "plain text". Your password is stored after processing with bcrypt, from which the original password cannot be devised without a computationally expensive process. However, given your password, we can determine that it matches our stored key without expensive processing. The purpose of this step is to ensure that should our database become compromised, your original password will be difficult to recover. Regardless, you are strongly encouraged to use a unique password for your sr.ht account.

You may choose to give us additional information, which is shown publicly on the site. This includes:

* Your location
* A URL to any website
* A short biography

You may omit or provide fictitious data for this information.

You may be required to provide the following information in order to successfully operate some parts of the service, some of which may be used to uniquely identify you:

* SSH keys
* PGP keys
* Two-factor authorization keys

You may delete this information at any time by visiting your [account details](https://meta.sr.ht/). If you provide a PGP key, you may choose to have email communications from sr.ht encrypted before being sent to you.

We also obtain some information from your web browser as you use our services and store it for up to 30 days:

* Your IP address
* When you accessed the site
* What you did on the site

This information is available to you as an [audit log](https://meta.sr.ht/security). You are not able to delete this information. The purpose of this data collection is to inform both you and sr.ht of any unknown activity on your account. If we permitted deletion of this information, someone who obtains unauthorized access to your account would be able to delete it, too.

We also store various other kinds of information that you explicitly choose to give us, including (but not limited to):

* repositories on git.sr.ht
* tickets on todo.sr.ht
* build logs and secrets on builds.sr.ht

To faciliate automated access to your account for third-party service or your personal use, we also generate and store API keys which can be used to authorize use of your account. A portion of these keys are stored in plaintext — not enough to gain access to your account, but enough for us to quickly look up your account details given the key. The full key is stored only after processing with bcrypt, similar to the process used for your password.

If you choose to use our paid services, we will store a token which is used to bill your payment method. Information like your credit card number cannot be recovered from this token.

We also use cookies to store long-lived authorization data, to remember that you're logged into your account between visits without prompting you for your password again. We also use cookies to store short-lived information, like the fact that we have to tell you on the next page you load that we completed some operation successfully for you.

##### [#](#how-we-share-your-information-with-third-parties)How we share your information with third-parties

Aside from information you choose to make public in the course of your use of sr.ht and information you explicitly choose to share with specific third parties, none of your information is shared with third parties. We do not embed third-party content in our website, with one exception: on the billing page, we embed a script from [Stripe](https://stripe.com/). This measure is taken to improve your privacy and allows us to avoid directly handling your credit card information.

We permit user-generated content to include images from and links to third-party sites. On pages displaying this content, information may be sent to these third-parties. This information includes:

* Your IP address
* Information about your web browser, such as whether you use Firefox or Chrome
* The URL on sr.ht you visited when you saw this content

We are not responsible for any additional information your web browser may send to these third parties.

If you use any of our paid services, we will transmit your payment information to a third-party payment processor. You will be notified of this before the information is transmitted, and given an opportunity to prevent its transmission. We will be unable to provide you with paid services if you decline to transmit this information.

We may also be required to remit your data upon receiving an order from a court of the United States. If permitted by the order, you will be notified if this happens.

##### [#](#how-to-access-and-control-the-information-weve-collected)How to access and control the information we've collected

You may submit a request via email to [support](mailto:~sircmpwn/sr.ht-support@lists.sr.ht) to request an archive of the information we've collected about you, or to request that we remove any information we've collected about you.

You may also reach out to our data protection officer directly: Drew DeVault [sir@cmpwn.com](mailto:sir@cmpwn.com).

##### [#](#changes-to-this-document)Changes to this document

We may make changes to this document with no less than 2 weeks notice. Notice of these changes will be sent to the email on file for your account.

### About this wiki

commit [2363e949b197aaf3ed8c591cf029ae9bd6e56574](https://git.sr.ht/~sircmpwn/sr.ht-docs/commit/2363e949b197aaf3ed8c591cf029ae9bd6e56574)
Author: Gary Kim <gary@garykim.dev>
Date:   2024-10-29T15:22:30-04:00

Update fedora supported versions

Signed-off-by: Gary Kim <gary@garykim.dev>

**Clone this wiki**

[https://git.sr.ht/~sircmpwn/sr.ht-docs](https://git.sr.ht/~sircmpwn/sr.ht-docs) (read-only)  
git@git.sr.ht:~sircmpwn/sr.ht-docs (read/write)