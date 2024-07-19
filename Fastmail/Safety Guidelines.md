[Skip to main content](#main-content)

[Home](https://www.fastmail.com/)

 Open menu Hide menu

* [Product tour](https://www.fastmail.com/features/)
* [For business](https://www.fastmail.com/business/)
* Support & Resources
    
    * Support
        
        * [Help center](https://fastmail.help/hc/en-us/)
        * [Contact us](https://support.fastmail.com/support/)
        * [System status](https://fastmailstatus.com/)
        * [Report a security issue](https://www.fastmail.com/bug-bounty/)
    * How to
        
        * [Move from Gmail](https://www.fastmail.com/how-to/move-from-gmail/)
        * [Move from Outlook](https://www.fastmail.com/how-to/move-from-outlook/)
        * [Move from Yahoo](https://www.fastmail.com/how-to/move-from-yahoo/)
        * [Move from Proton](https://www.fastmail.com/how-to/move-from-proton/)
        * [Move from HEY](https://www.fastmail.com/how-to/move-from-hey/)
        * [Get email for your domain](https://www.fastmail.com/how-to/email-for-your-domain/)
        * [Stop spam](https://www.fastmail.com/how-to/stop-spam/)
        * [Achieve inbox zero](https://www.fastmail.com/how-to/inbox-zero/)
    * Resources
        
        * [Blog](https://www.fastmail.com/blog/)
        * [Podcast](https://www.fastmail.com/digitalcitizen/)
        * [About us](https://www.fastmail.com/company/about/)
        * [Our values](https://www.fastmail.com/company/values/)
        * [API Documentation](https://www.fastmail.com/dev/)
        * [Policies](https://www.fastmail.com/policies/)
    * Download the app
        
        * [App Store Download Fastmail on the App Store](https://apps.apple.com/us/app/fastmail-email-calendar/id931370077)
        * [Google Play Download Fastmail on Google Play](https://play.google.com/store/apps/details?id=com.fastmail.app)
    
* [Pricing](https://www.fastmail.com/pricing/)
* [Log in](https://app.fastmail.com/)[Try for free](https://app.fastmail.com/signup/)

* [Try for free](https://app.fastmail.com/signup/)
* [Log in](https://app.fastmail.com/)

How can we help?

 

1. [Fastmail](https://www.fastmail.com/hc/en-us)
2. [Security](https://www.fastmail.com/hc/en-us/categories/360006005393-Security)
3. [Security basics](https://www.fastmail.com/hc/en-us/sections/1500000062142-Security-basics)

Using two-step verification (2FA)
=================================

Two-step verification, also called "two-factor authentication" or "2FA", increases the security of your account by requiring two steps - your password plus an additional security step - in order to log in to your account. We support two-step verification with either an app on your phone or a dedicated security device that plugs into your computer. SMS can also be used as a backup mechanism.

It is not required to have 2FA set up on your Fastmail account, but it is recommended if you want additional security.

* [Why should I use two-step verification?](#why2fa)
* [How to set up two-step verification](#setup2fa)
* [How to log in with two-step verification](#login2fa)
* [Using two-step verification with a mail client](#client2fa)
* [Why do I have to add a recovery phone number to set up two-step verification?](#recovery2fa)
* [Which two-step verification method should I use?](#whichone)
* [How do authenticator apps and security keys work?](#howappswork)
* [Fastmail security principles](#fmsecurity)

Why should I use two-step verification?
---------------------------------------

In an ideal world, all passwords would be a secret. But the more a password is used, the more exposed it becomes to malicious attackers. They might try to steal it (through [phishing](https://en.wikipedia.org/wiki/Phishing) or [malware/spyware](https://en.wikipedia.org/wiki/Malware)), or guess it (through brute force repeated [dictionary attacks](https://en.wikipedia.org/wiki/Dictionary_attack)).

With two-step verification, if someone does manage to steal your password, they still can't use it to log in to your account without your verification device.

How to set up two-step verification
-----------------------------------

### General Setup Instructions

1. Open the [Settings → Privacy & Security](https://app.fastmail.com/settings/security/general?sessionpicker=1) screen.
2. If this is your first time enabling two-step verification for this account, you must add a recovery phone to your account (see "Account Recovery Credentials" below).
3. If you have a recovery phone on your account, click **Manage** next to Two-Step verification. On the following page, click **Add verification device**.
4. A Verify it's you box will appear. Enter your password and click Continue. _(For more information, see our_ _[Password-protected actions](https://www.fastmail.help/hc/en-us/articles/5730579789583)_ _help page.)_
5. Select which kind of verification device you're adding to your account. If you have an older YubiKey without support for modern security standards (U2F/Webauthn), you can select "Yubico OTP" instead at the bottom of the page. Skip to the "Authenticator App (TOTP)" or "Security keys and Yubico OTP" instructions below for instructions on adding your verification device. 

### Account Recovery Credentials

To help make sure that you are not locked out of your own account, before you can enable two-step verification, you must add a recovery phone to your account. If you ever lose access to your primary form of two-step verification, your recovery phone can be used to prevent you from being locked out of your account. You get a code sent to your phone instead to complete your second step when you log in.

1. Go to the [Settings → Privacy & Security](https://app.fastmail.com/settings/security/general?sessionpicker=1) screen, then go to the **Account recovery** section and click **Set up now**.
2. Click the **Add recovery phone** button.
3. A **Verify it's you** box will appear. Enter your password and click **Continue**. _(For more information, see our [Password-protected actions](https://www.fastmail.help/hc/en-us/articles/5730579789583) help page.)_
4. Enter your phone number and click **Send verification code**. Clicking this button will send a verification code to your recovery phone.
5. Once you've received your verification code, enter the code and click **Verify**. This will add your recovery phone to your account.
6. A confirmation screen will appear. Click **Done** to return to the [Privacy & Security](https://app.fastmail.com/settings/security/general?sessionpicker=1) screen.

On the [Account Recovery](https://app.fastmail.com/settings/security/recovery?sessionpicker=1) screen, you can also see your recovery code, which is randomly generated for your account. If you forget your password or lose your security device, you can use the recovery code as part of the recovery process to reset your password and restore access to your account. We **strongly recommend** writing down or printing out your recovery code and keeping it somewhere safe.

### Authenticator App (TOTP)

1. Once you've installed the authenticator app on your phone or tablet, select to **add a new account**.
2. Use your device's camera to **scan the QR code** on the screen (or manually type in the key on the screen into the authenticator app). If you're setting up an OTP device, select "Set a custom key" and enter the key that came with your device.
3. **Enter the 6-digit code** the app gives you into the Fastmail web interface.
4. **Name this device** so you can keep track of your verification devices and remove them if needed in the future.

### Security keys and Yubico OTP

1. **Insert the device** into the USB port on your computer.
2. **Touch the button** on the device once it lights up.
3. **Name this device** so you can keep track of your verification devices and remove them if needed in the future.

How to log in with two-step verification
----------------------------------------

Start by navigating to our [login page](https://app.fastmail.com/login/), then:

1. Enter your username and your password. Click **Log In**.
2. Enter the current **verification code** from your authenticator app or OTP device, or plug in your security key and touch the button if it has one. If you have more than one two-step method on your account, click **Verify another way** to switch to another method.
3. You can also declare this computer as trusted which means you don't need to use two-step verification again when logging in on that computer.

If you use 1Password to manage your passwords, we have instructions on using 1Password with Fastmail at our [Using 1Password on Fastmail web interface](https://www.fastmail.help/hc/en-us/articles/360060590513) help page.

If you'd like to revoke a computer's trusted status, you can also do that on the [Privacy & Security](https://app.fastmail.com/settings/security) screen. The next time you log in on that device, you will need to re-authenticate using your 2FA.

Using two-step verification with a mail client
----------------------------------------------

Other than the [Fastmail app](https://www.fastmail.help/hc/en-us/articles/360060590873), most mail and calendaring computer programs and phone/tablet apps don't support two-step verification.

You'll need to set up [app passwords](https://www.fastmail.help/hc/en-us/articles/360058752854) for each device instead.

Why do I have to add a recovery phone number to set up two-step verification?
-----------------------------------------------------------------------------

Keeping your account safe from attackers is very important, but so is making sure you don't get locked out of your own account. Requiring a phone as a backup option balances security (no one else can read your data) and availability (you can read your data). For most users, the risk of losing their two-step verification device is far greater than the risk of someone hacking their SMS. If you lose your phone, the TOTP key is lost, but normally you can get a new SIM card with the same number from your carrier.

Please note, if two-step verification is enabled, access to the phone number itself is not sufficient to gain access to an account: you still need two factors (your password AND the SMS).

Users who accept the risk of being locked out of their account may remove the recovery phone number from their account after two-step verification has been enabled. **Once the phone number is removed from the account, SMS is no longer an option as the second factor for verification.** If you choose to do this, we **strongly recommend** you write down or print your recovery code and store it in a safe location, and that you set up at least two security keys or authenticator devices. Should you lose access to all two-step verification devices and do not have your recovery code, **you may be permanently locked out of your own account.**

Which two-step verification method should I use?
------------------------------------------------

**Note**: You can set up more than one two-step verification device on your account.

### Authenticator app (TOTP)

With this option, you can install an app on your device (usually your phone) that will generate a random 2FA code that you can enter when logging in to your account. There are free authenticator apps that can be used. If you're new to using 2FA, using an authenticator app would generally be the easiest method.

Not sure which authenticator app to use? We recommend:

* iPhone: [Google Authenticator](https://apps.apple.com/us/app/google-authenticator/id388497605), [Authy](https://apps.apple.com/au/app/authy/id494168017), or [Duo Mobile](https://apps.apple.com/us/app/duo-mobile/id422663827)
* Android: [Google Authenticator](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2), [Authy](https://play.google.com/store/apps/details?id=com.authy.authy), or [Duo Mobile](https://play.google.com/store/apps/details?id=com.duosecurity.duomobile&hl=en)

If you have a different phone, you may still be able to use TOTP. Any app supporting Time-based One-Time Password (TOTP) from the Initiative for Open Authentication (OATH) as specified in [RFC 6238](https://tools.ietf.org/html/rfc6238) should work.

**Note**: Neither the Google Authenticator app nor our server implementation is specific to Google in any way, nor does it ever communicate with Google systems as part of its operation (or with any other system). "Google Authenticator" is the name of Google's TOTP app, which has become synonymous with the authentication method itself.

### Security keys and Yubico OTP

Both security keys and Yubico OTP require the use of a hardware device during login, rather than entering a code. For **security keys**, they are domain specific. This would be the most secure option as it protects you against phishing. For **Yubico OTP**, please note that it is a legacy security key format. There is no reason to use this unless you have an old key that does not support WebAuthn/U2F authentication.

U2F is an older form of authentication that has been superseded by WebAuthn. We only support WebAuthn entries. However, WebAuthn works with U2F-compatible security keys, which means that if you have a U2F key, you can still use it in Fastmail. Any security key that supports WebAuthn or U2F should work. We do recommend newer YubiKey devices that support WebAuthn/U2F, as in our experience these have the best build quality, a slim profile, and are reliable. You can buy one from [Yubico](https://www.yubico.com/store/), or [Yubico's Amazon store](https://www.amazon.com/Yubico/b/?node=10358012011&field-lbr_brands_browse-bin=Yubico).

### Security device: OTP

This requires the use of a hardware device, but does not require a mobile device or USB port. A code needs to be entered in during login. This method is useful if you can't use an authenticator app and can't plug a device into a computer.

Many manufacturers are now selling standalone OTP devices, often in a credit card or key fob form-factor. We've tested with [Feitian c200](http://www.ftsafe.com/products/OTP/Single_Button_OTP) devices, but any device implementing the TOTP standard should work. We support devices with HEX or BASE32-encoded keys with a 30- or 60-second time step. If your particular device doesn't work, please let us know the make and model of the device and we'll look into adding support for it.

When adding these devices to your account, use the **Authenticator App (TOTP)** option. This is because OTP devices use the same mechanism (TOTP) as authenticator apps described above.

### SMS code

This method involves a code being sent to your phone via text message, and the code will need to be entered in during login. It does not require additional charges and is free.

**Note**: SMS can be used as a backup mechanism in case you lose your security device. This can only be used if you already have two-step verification enabled through an authenticator app or security device.

How do authenticator apps and security keys work?
-------------------------------------------------

Interested in what's happening under the hood to keep you safe? Learn more about [how TOTP works](https://www.fastmail.com/blog/how-totp-authenticator-apps-work/), [how U2F works](https://www.fastmail.com/blog/how-u2f-security-keys-work/), or how [YubiKey OTP](https://www.fastmail.com/blog/how-yubico-otp-works/) works.

Fastmail security principles
----------------------------

We take security seriously at Fastmail and design our systems to improve the confidentiality, availability, and integrity of our customers' data. The user login process and account recovery process are a particularly important part of our security.

When you turn on two-step verification, we understand that you value the confidentiality of your account more highly and take extra steps to ensure that. If you lose access to your account when you have two-step verification enabled, the recovery process still requires two independent factors. If a recovery attempt is successful, we delay the final recovery step for 24 hours. In this time, we notify the account owner via email and give them the opportunity to cancel the recovery if they weren't the person who requested it.

For more information on how we designed our security system, see our [blog post](https://www.fastmail.com/blog/security-account-recovery/) about the design and thought process.

Was this article helpful?

Yes No

215 out of 296 found this helpful

Need help? [Contact our support team](https://support.fastmail.com/support)

Footer navigation
-----------------

Email and calendar made better

### Product

* [Product tour](https://www.fastmail.com/features/)
* [For business](https://www.fastmail.com/business/)
* [Pricing](https://www.fastmail.com/pricing/)
* [Security](https://www.fastmail.com/features/security/)
* [Privacy](https://www.fastmail.com/features/privacy/)

### How to

* [Move from Gmail](https://www.fastmail.com/how-to/move-from-gmail/)
* [Move from Outlook](https://www.fastmail.com/how-to/move-from-outlook/)
* [Move from Yahoo](https://www.fastmail.com/how-to/move-from-yahoo/)
* [Move from Proton](https://www.fastmail.com/how-to/move-from-proton/)
* [Move from HEY](https://www.fastmail.com/how-to/move-from-hey/)
* [Get email for your domain](https://www.fastmail.com/how-to/email-for-your-domain/)
* [Stop spam](https://www.fastmail.com/how-to/stop-spam/)
* [Achieve inbox zero](https://www.fastmail.com/how-to/inbox-zero/)

### Support & Resources

* [Blog](https://www.fastmail.com/blog/)
* [Podcast](https://www.fastmail.com/digitalcitizen/)
* [Help center](https://fastmail.help/hc/en-us/)
* [Contact us](https://support.fastmail.com/support/)
* [API Documentation](https://www.fastmail.com/dev/)
* [Report a security issue](https://www.fastmail.com/bug-bounty/)

### Company

* [About us](https://www.fastmail.com/company/about/)
* [Our values](https://www.fastmail.com/company/values/)
* [Careers](https://apply.workable.com/fastmail-1/)
* [Open source and standards](https://www.fastmail.com/company/open-source/)
* [Partner with us](https://www.fastmail.com/company/partners/)
* [Policies](https://www.fastmail.com/policies/)
* [Media kit](https://www.fastmail.com/media-kit/)

* © 2024 Fastmail Pty Ltd. All rights reserved.
* [System status](https://fastmailstatus.com/)
* [Terms of service](https://www.fastmail.com/policies/terms-of-service/)

* [Mastodon](https://mastodon.social/@fastmail)
* [X](https://twitter.com/Fastmail)
* [LinkedIn](https://www.linkedin.com/company/fastmail)
* [Facebook](https://www.facebook.com/Fastmail/)

* [Download Fastmail on Google Play](https://play.google.com/store/apps/details?id=com.fastmail.app)
* [Download Fastmail on the App Store](https://apps.apple.com/us/app/fastmail-email-calendar/id931370077)