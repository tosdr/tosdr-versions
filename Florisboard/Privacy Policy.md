 [![FlorisBoard app icon](/images/app-icon.png) FlorisBoard](https://florisboard.org/)

[![](/images/github-logo.png)](https://github.com/florisboard/florisboard)

 en ▼

[es](https://florisboard.org/es/legal/privacy/)

[fr](https://florisboard.org/fr/legal/privacy/)

Privacy policy
==============

Last modified: Aug 25, 2022

FlorisBoard (the “Project”) is a privacy-respecting open-source keyboard primarily developed and maintained by Patrick Goldinger ([@patrickgold](https://github.com/patrickgold)), together with the amazing support of this Project’s community. This privacy policy exists to give you a better understanding what personal data must be accessed and/or locally stored at a minimum to even provide you with a keyboard service.

Data access and usage
---------------------

This Project’s core commitment is to access and store as little personal data as possible while still delivering a good personalized experience. Any personal data that is accessed or stored is exclusively kept locally either in-memory or in the private app data directory and is **never** shared with anyone.

### What personal data does FlorisBoard access and why?

Any time you focus a text field and FlorisBoard is the default input method editor (the “IME”), FlorisBoard has access to the full contents of that text field. It will monitor and store a small window around the cursor in-memory to keep track of the current state and to improve performance. Additionally as a default IME FlorisBoard has access to the system clipboard and actively keeps track of the latest primary clipboard item to privide you with clipboard features. Furthermore FlorisBoard has access to the system user dictionary, only reading the actual contents though if either spell checking, suggestions or glide typing is enabled.

Unless otherwise stated in the next section, any accessed personal data is only stored temporarily in-memory and will get discarded once the text field looses focus or once the keyboard process ends.

### What personal data does FlorisBoard store and why?

Some features require personal data to be persisted locally on-disk in order to be reused later on. This applies to:

* **Spell checking, suggestions and glide typing**  
    To be able to automatically create personalized dictionaries and to provide dynamic suggestions based on your previous input FlorisBoard needs to monitor your typing behavior, learn from it and save the results locally. Typing behavior tracking is fully stopped if the keyboard is in incognito mode or if no feature is enabled that requires this option.
* **Clipboard history**  
    To be able to store and show multiple clipboard items FlorisBoard stores clipboard items in a local database. The database is only maintained and used if the clipboard history feature is enabled.

### Does any of the stored personal data leave the device?

No. Any personal data that is persisted is stored locally and **never** leaves your device.

Other
-----

For information about the list of permissions requested by FlorisBoard, please read [this](https://github.com/florisboard/florisboard/wiki/List-of-permissions-FlorisBoard-requests) document.

### Updates to this privacy policy

We reserve the right to periodically review and update this policy. Changes to this policy will be announced publicly and will be linked in the corresponding changelog of the version the new policy takes effect. Continued use of FlorisBoard will be deemed acceptance of such changes.

### Contact

If you have additional questions, comments or concerns regarding this privacy policy, please contact [patrick@patrickgold.dev](mailto:patrick@patrickgold.dev) or file an issue in the FlorisBoard [issue tracker](https://github.com/florisboard/florisboard/issues).

© 2022 Patrick Goldinger • [Privacy policy](https://florisboard.org/legal/privacy/)