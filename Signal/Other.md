[![](/assets/images/header/logo.png)](https://signal.org/#signal)

[Get Signal](https://signal.org/download/) [Help](https://support.signal.org/) [Blog](https://signal.org/blog/) [Developers](https://signal.org/docs/) [Careers](https://signal.org/workworkwork/) [Donate](https://signal.org/donate/)[](https://twitter.com/signalapp)[](https://instagram.com/signal_app/)

Technical information
=====================

Specifications and software libraries for developers

![](/assets/images/header/header-developers.png)

Specifications
--------------

Encryption in messaging environments integrates many ideas which often need to be composed separately in different applications. We make an effort to break out ideas into independent specifications so that they can be integrated as appropriate for different projects.

[XEdDSA and VXEdDSA](https://signal.org/docs/specifications/xeddsa/)

This document describes how to create and verify EdDSA-compatible signatures using public key and private key formats initially defined for the X25519 and X448 elliptic curve Diffie-Hellman functions. This document also describes "VXEdDSA" which extends XEdDSA to make it a verifiable random function, or VRF.

[X3DH](https://signal.org/docs/specifications/x3dh/)

This document describes the "X3DH" (or "Extended Triple Diffie-Hellman") key agreement protocol. X3DH establishes a shared secret key between two parties who mutually authenticate each other based on public keys. X3DH provides forward secrecy and cryptographic deniability.

[PQXDH](https://signal.org/docs/specifications/pqxdh/)

This document describes the "PQXDH" (or "Post-Quantum Extended Diffie-Hellman") key agreement protocol. PQXDH establishes a shared secret key between two parties who mutually authenticate each other based on public keys. PQXDH provides post-quantum forward secrecy and a form of cryptographic deniability but still relies on the hardness of the discrete log problem for mutual authentication in this revision of the protocol.

[Double Ratchet](https://signal.org/docs/specifications/doubleratchet/)

This document describes the Double Ratchet algorithm, which is used by two parties to exchange encrypted messages based on a shared secret key. The parties derive new keys for every Double Ratchet message so that earlier keys cannot be calculated from later ones. The parties also send Diffie-Hellman public values attached to their messages. The results of Diffie-Hellman calculations are mixed into the derived keys so that later keys cannot be calculated from earlier ones. These properties give some protection to earlier or later encrypted messages in case of a compromise of a party's keys.

[Sesame](https://signal.org/docs/specifications/sesame/)

This document describes the Sesame algorithm for managing message encryption sessions in an asynchronous and multi-device setting.

Software libraries
------------------

* [Signal Protocol library](https://github.com/signalapp/libsignal)

© 2013–2024 Signal, a 501c3 nonprofit.  
"Signal", Signal logos, and other trademarks are trademarks or registered trademarks of Signal Technology Foundation in the United States and other countries ([more info here](https://signal.org/brand/)).  
  
For media inquiries, contact [\[email protected\]](https://signal.org/cdn-cgi/l/email-protection)

**Organization**

* [Donate](https://signal.org/donate/)
* [Careers](https://signal.org/workworkwork/)
* [Blog](https://signal.org/blog/)
* [Brand Assets](https://signal.org/brand/)
* [Terms & Privacy Policy](https://signal.org/legal/)

**Download**

* [Android](https://signal.org/download/android/)
* [iPhone & iPad](https://signal.org/download/ios/)
* [Windows](https://signal.org/download/windows/)
* [Mac](https://signal.org/download/macos/)
* [Linux](https://signal.org/download/linux/)

**Social**

* [GitHub](https://github.com/signalapp)
* [Twitter](https://twitter.com/signalapp)
* [Instagram](https://www.instagram.com/signal_app/)

**Help**

* [Support Center](https://support.signal.org/)
* [Community](https://community.signalusers.org/)

© 2013–2024 Signal, a 501c3 nonprofit.  
"Signal", Signal logos, and other trademarks are trademarks or registered trademarks of Signal Technology Foundation in the United States and other countries ([more info here](https://signal.org/brand/)).  
  
For media inquiries, contact [\[email protected\]](https://signal.org/cdn-cgi/l/email-protection)