![Whatbox Logo](/static/logo/logo.min.svg) 

[Plans](https://whatbox.ca/plans) [FAQ](https://whatbox.ca/faq) [Wiki](https://whatbox.ca/wiki)

[Register](https://whatbox.ca/register) [Login](https://whatbox.ca/login)

Data Handling Policy
--------------------

Username

#### Why do we need it?

A username is how you identify yourself when logging in to services.

#### How do we collect it?

You provide this to us on registration.

#### Where and how do we store it?

| Location | Safety |
| --- | --- |
| SiteDB | Encrypted at rest |
| ServerDB | Cleartext |
| App configs | Cleartext |

#### Who do we share it with?

| Group | Reason |
| --- | --- |
| Whatbox Staff | Providing customer support |
| Same-server users | Technical limitations\[1\] |
| Registering users | Technical limitations\[2\] |

1. There are currently known issues where a username may be visible to other users sharing the same server. We are actively working to address the technical issues where this is still happening.
2. If someone attempts to register with the same username as you, we will tell them it is in use.

#### How long do we store it?

Indefinitely

#### How can it be modified or removed?

Not currently possible.

Email

#### Why do we need it?

We use your email to send you necessary account alerts and to recover your account if you forget your password.

#### How do we collect it?

You provide this to us on registration.

#### Where and how do we store it?

| Location | Safety |
| --- | --- |
| SiteDB | Encrypted at rest |

#### Who do we share it with?

| Group | Reason |
| --- | --- |
| [Amazon Web Services](https://aws.amazon.com/compliance/data-privacy-faq/) | AWS provides our email infrastructure |
| Registering users | Technical limitations\[1\] |

1. If someone attempts to register with the same email as you, we will tell them it is in use.

#### How long do we store it?

Indefinitely

#### How can it be modified or removed?

You can change your email address in your [preferences](https://whatbox.ca/preferences/email) or remove it by [deleting your account](https://whatbox.ca/preferences/delete).

Password

#### Why do we need it?

We need a password to authenticate you and prevent strangers from logging into your account.

#### How do we collect it?

You provide this to us on registration.

#### Where and how do we store it?

| Location | Safety |
| --- | --- |
| SiteDB | Cryptographically hashed & Encrypted at rest |
| ServerDB | Cryptographically hashed |
| App configs | Cryptographically hashed\[1\] |

1. Not all apps are compatible with best practices for password hashing. Some app configuration files may contain cryptographic hashes considered weak by modern standards.

#### Who do we share it with?

Nobody.

#### How long do we store it?

Indefinitely

#### Haw can it be modified or removed?

You can change your password in your [preferences](https://whatbox.ca/preferences/password) or remove it by [deleting your account](https://whatbox.ca/preferences/delete).

Mobile phone number

#### Why do we need it?

A phone number is optional.

We will send you account alerts via SMS if you provide a phone number.

#### How do we collect it?

You provide this to us on registration or set it in the [preferences](https://whatbox.ca/preferences/mobile).

#### Where and how do we store it?

| Location | Safety |
| --- | --- |
| SiteDB | Encrypted at rest |

#### Who do we share it with?

| Group | Reason |
| --- | --- |
| [Amazon Web Services](https://aws.amazon.com/compliance/data-privacy-faq/) | AWS provides our SMS infrastructure |

#### How long do we store it?

Indefinitely

#### How can it be modified or removed?

You can change or remove your mobile phone number in your [preferences](https://whatbox.ca/preferences/mobile) or by [deleting your account](https://whatbox.ca/preferences/delete).

Contact information

#### Why do we need it?

This is not actually required information. You do not need to provide it.

Contact information is optional.

You will need to provide this information if you want your name, business name, or address included on invoices.

#### How do we collect it?

You provide this to us by filling in the section in the [preferences](https://whatbox.ca/preferences/contact_information).

#### Where and how do we store it?

| Location | Safety |
| --- | --- |
| SiteDB | Encrypted at rest |

#### Who do we share it with?

Nobody.

#### How long do we store it?

Indefinitely

#### How can it be modified or removed?

You can change or remove your contact information in your [preferences](https://whatbox.ca/preferences/contact_information) or by [deleting your account](https://whatbox.ca/preferences/delete).

Province

#### Why do we need it?

We need your province to charge you the appropriate sales tax amount.

#### How do we collect it?

You provide this to us on registration.

#### Where and how do we store it?

| Location | Safety |
| --- | --- |
| SiteDB | Encrypted at rest |

#### Who do we share it with?

Nobody.

#### How long do we store it?

Indefinitely

#### How can it be modified or removed?

You can change province in your [preferences](https://whatbox.ca/preferences/province).

Timezone

#### Why do we need it?

To provide your localized dates and times in communication.

#### How do we collect it?

Collected from your browesr on registration.

#### Where and how do we store it?

| Location | Safety |
| --- | --- |
| SiteDB | Encrypted at rest |

#### Who do we share it with?

Nobody.

#### How long do we store it?

Indefinitely

#### How can it be modified or removed?

You can change province in your [preferences](https://whatbox.ca/preferences/timezone).

Credit card

#### Why do we need it?

A credit card is an accepted payment method.

We require your credit card number, CVC, and expiry to charge your credit card successfully.

#### How do we collect it?

When adding a credit card, you provide this directly to our credit card provider. For security, we avoid handling this information ourselves.

#### Where and how do we store it?

| Piece | Location | Safety |
| --- | --- | --- |
| Full number | Stripe | PCI-DSS |
| CVC | Stripe | PCI-DSS |
| Expiry | Stripe | PCI-DSS |
| Last 4 | SiteDB | Encrypted at rest |

#### Who do we share it with?

| Group | Reason |
| --- | --- |
| [Stripe](https://stripe.com/en-ca/privacy) | Stripe provides our credit card infrastructure |

#### How long do we store it?

We will delete saved credit cards after six months of account inactivity.

#### How can it be modified or removed?

You can change or remove your credit cards in your [preferences](https://whatbox.ca/preferences/credit_cards).

Invoices (PayPal)

#### Why do we need it?

Invoices are a permanent payment record, and we require them for bookkeeping.

#### How do we collect it?

We generate the invoices when you make a payment.

#### Where and how do we store it?

| Piece | Location | Safety |
| --- | --- | --- |
| PayPal Transaction ID | SiteDB | Encrypted at rest |

#### Who do we share it with?

| Group | Reason |
| --- | --- |
| [PayPal](https://www.paypal.com/ca/webapps/mpp/ua/privacy-full) | PayPal facilited the payment |
| Whatbox Staff | Providing customer support and refunds |

#### How long do we store it?

Indefinitely

#### How can it be modified or removed?

Invoices cannot be modified or removed.

Invoices (Credit card)

#### Why do we need it?

Invoices are a permanent payment record, and we require them for bookkeeping.

#### How do we collect it?

We generate the invoices when you make a payment.

#### Where and how do we store it?

| Piece | Location | Safety |
| --- | --- | --- |
| Stripe Transaction ID | SiteDB | Encrypted at rest |
| Issuance country | SiteDB | Encrypted at rest |

#### Who do we share it with?

| Group | Reason |
| --- | --- |
| [Stripe](https://stripe.com/en-ca/privacy) | Stripe facilited the payment |
| Whatbox Staff | Providing customer support and refunds |
| [Statistics Canada](https://www.statcan.gc.ca/en/reference/privacy) | (Aggregate only) Total sales by Issuance country |

#### How long do we store it?

Indefinitely

#### How can it be modified or removed?

Invoices cannot be modified or removed.

Invoices (Crypto)

#### Why do we need it?

Invoices are a permanent payment record, and we require them for bookkeeping.

#### How do we collect it?

We generate the invoices when you make a payment.

#### Where and how do we store it?

| Piece | Location | Safety |
| --- | --- | --- |
| Blockchain Identifier | SiteDB | Encrypted at rest |
| Confirmo Transaction ID | SiteDB | Encrypted at rest |

#### Who do we share it with?

| Group | Reason |
| --- | --- |
| [Confirmo](https://confirmo.net/legal/privacy-policy) | Confirmo facilited the payment |
| Whatbox Staff | Providing customer support and refunds |

#### How long do we store it?

Indefinitely

#### How can it be modified or removed?

Invoices cannot be modified or removed.

Analytics

#### Why do we need it?

Analytics help us understand our customers' geography, hardware, and software. Knowing this helps us improve your experience.

#### How do we collect it?

We collect this information all the time.

#### Where and how do we store it?

| Piece | Location | Safety |
| --- | --- | --- |
| Approximate user location | SiteDB | Anonymized & Encrypted at rest |
| Software versions | SiteDB | Anonymized & Encrypted at rest |
| Internet Service Provider | SiteDB | Anonymized & Encrypted at rest |
| Upload & download speed | SiteDB | Anonymized & Encrypted at rest |

#### Who do we share it with?

| Group | Reason |
| --- | --- |
| Whatbox Staff | (Aggregate only) Data-driven decisions about compatibility and performance |

#### How long do we store it?

Indefinitely

#### How can it be modified or removed?

We can't identify which portion of this data originated with you, so it cannot be modified or removed.

Errors

#### Why do we need it?

Collecting relevant application information in the event of an error or crash helps us to fix these issues and provide a more reliable service.

#### How do we collect it?

We collect this information when an error occurs.

#### Where and how do we store it?

We do not store it.

#### Who do we share it with?

| Group | Reason |
| --- | --- |
| [Sentry](https://sentry.io/privacy/) | We use Sentry's [error monitoring system](https://github.com/getsentry/sentry) |
| Whatbox Staff | To investigate and resolve the errors |

#### How long do we store it?

90 days

#### How can it be modified or removed?

It will be automatically removed after [90 days](https://sentry.io/security/#data-retention).

Authentication Logs

#### Why do we need it?

Automated security software reviews access logs to block malicious parties attempting to break into your account and steal your Hosted Data.

#### How do we collect it?

Many services collect your IP and Username on every login, successful or failed.

#### Where and how do we store it?

| Piece | Location | Safety |
| --- | --- | --- |
| Username | Server Log | Cleartext |
| IP Address | Server Log | Cleartext |

#### Who do we share it with?

| Group | Reason |
| --- | --- |
| Whatbox Staff | To investigate security incidents |

#### How long do we store it?

30 days

#### How can it be modified or removed?

We will automatically delete it after 30 days.

Hosted Data

#### Why do we need it?

We cannot provide services that function without files for the hosted applications to use.

#### How do we collect it?

You upload it to your server or download it to your server using an application.

#### Where and how do we store it?

| Piece | Location | Safety |
| --- | --- | --- |
| Files | Server | Cleartext |

#### Who do we share it with?

| Group | Reason |
| --- | --- |
| Whatbox Staff | To provide customer support |

#### How long do we store it?

We store it as long as you are a customer and for a short period afterward (allowing you time to renew).

#### How can it be modified or removed?

You can remove your hosted data at any time using any of the [available methods](https://whatbox.ca/wiki/file_downloading_and_uploading) to manage your data.

### Policies

* [Terms of Service](https://whatbox.ca/policies/terms)
    * [Acceptable Use](https://whatbox.ca/policies/acceptable_use)
    * [Refund](https://whatbox.ca/policies/refund)
    * [Uptime](https://whatbox.ca/policies/sla)
    * [Traffic](https://whatbox.ca/policies/traffic)
    * [Data Handling](https://whatbox.ca/policies/data_handling)
* [Sales Tax](https://whatbox.ca/policies/tax)
* [Cookies](https://whatbox.ca/policies/cookies)
* [Security](https://whatbox.ca/policies/security)
* [Report Abuse](https://whatbox.ca/policies/abuse)

[Terms of Service](https://whatbox.ca/policies/terms) · [Report Abuse](https://whatbox.ca/policies/abuse)