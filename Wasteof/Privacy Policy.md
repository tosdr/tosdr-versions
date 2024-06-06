[![](/brand/nav-logo.svg)](https://wasteof.money/)

* [home](https://wasteof.money/)
* [explore](https://wasteof.money/explore)
* [join](https://wasteof.money/join)
* [login](https://wasteof.money/login)

privacy

_Last updated 8 August 2022_

Note: All users must be 13 years of age or older to use wasteof.money, including the wiki.

wasteof.money is a hobby project and does not collect data which can be used to directly identify real people. I just want to make a cool social media project, and I have no intentions on collecting data for the purpose of being sold later.

That being said, some data collection is required for the site to function. This data includes, IP addresses, usernames, bcrypt hashed and salted passwords, email addresses and any other data explicitly entered into the website.

To power login using external services, wasteof.money will only store user IDs from external services (Google, Github). User IDs are stored because they don't change, and are used to make sure the user is who they claim to be. It may be possible to use user IDs to identify real people, depending on the third party provider and how much data they have about a user. External service user IDs are not shared with third parties and are only visible to administrators with database access. They can be removed from an account by pressing "Remove this authentication method" in the settings page. Public account information from OAuth providers will be used to build a public wasteof.money profile for users who chose to sign up using them. For instance, when logging in with GitHub, the user's wasteof.money username will be decided based on their public GitHub username. The same goes for Google account names, which may be full names based on what a user shared with Google. Usernames can be completely changed from within the account settings page. OAuth tokens are not stored, and are only used to get public profile information each time the "login with" button is pressed. Using Google or GitHub login is completely optional, and can be bypassed by chosing to use password authentication. 

Google specific privacy information:

\- wasteof.money will only request Google User data when chosing to login with Google, or when linking a Google account for login. 

\- wasteof.money uses the "userinfo.profile" scope for Google OAuth login. This means that it can "See your personal info, including any personal info you've made publicly available"

\- wasteof.money uses this scope to get your User ID from the Google API. A User ID is a unique number that identifies your Google account.

\- wasteof.money directly stores only your User ID. No other data is stored from Google Account, except for when signing up for the first time, wasteof.money will use your public Google account name, to generate a wasteof.money username. Depending on what data you have shared with Google, this may be your full name. You can change your username from within the settings page at any time.

\- wasteof.money uses this User ID when you press the "login with Google" button, to find the correct wasteof.money account to log you into. (or whether to create a new account)

\- Your Google User ID is only visible to administrators with direct database access. It is not shared with any third-parties.

\- You can unlink/remove your Google account data from wasteof.money by pressing "Remove this authentication method" under Google Account at wasteof.money/settings. You may have to also change your username if it was based on your Google account name.

wasteof.money is self hosted in Switzerland, however it makes use of the following third party services which help it stay online. Further privacy information can be found on each's respective websites. Cloudflare, GitHub, Google

wasteof.money uses Google reCAPTCHA for sign up. [Privacy](https://www.google.com/intl/en/policies/privacy/) [Terms](https://www.google.com/intl/en/policies/terms/).

For analytics purposes, wasteof.money makes use of [Plausible Analytics](https://plausible.io/) (self hosted) to track privacy friendly web analytics. Information about the data tracked by Plausible can be found on their website. If you would not like to be tracked, block the analytics.jeffalo.net domain on your device/network.

If you would like data deletion from the servers, please [contact me](https://wasteof.money/contact), and I will help you out. In the future, there will be an account deletion button accessible in the settings page.

Note that wasteof.money is currently in heavy development, and there will be many changes in a short time period. You must check this document regularly, and remember that this is just a fun hobby project from a teenager in Switzerland.