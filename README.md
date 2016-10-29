# software-trust

This repository contains software that passes my requirements for being
trustworthy. The idea is that, if you trust me, and trust my ability to verify
software, you can trust the contents of this repository.

You can be assured that, if I place software in this repository, I trust it
enough to use it myself. Make sure to read the README.md for any piece of
software, as some pieces of software may have only received partial inspection.

Keep in mind that I have only verified the software in this repository, not any
newer versions of any software.

Every commit to this repository will be signed by my public key, with
fingerprint EEA31BFF444304ABB246A0B6C634D0420F825B91. Verify this key's
fingerprint out of band, and expect all commits to be signed by it.

# Requirements

All software in this repository has been checked against this list. This list
has no particular order.

Because I don't have the skill or time to thoroughly audit the software, my
verification process includes non-technical elements.

1. Software must not contain any hidden files without a clear rationale. For
   example, .gitignores are allowed.
2. Software must not contain any code in violation of standard indentation and
   whitespace rules. (Code that could be misleading in purpose.)
3. All files must have contents that make sense on their surface. I look for
   obvious bugs, flaws, and vulnerabilities, but I am likely to miss some of
   these.
4. All code must be signed by a PGP key that passes a reasonable level of
   scrutiny. I must be able to establish a reasonable-length path through the
   web of trust, and find enough information on each link to plausibly trust
   that the key could be correct.
5. The PGP-validated author of the code must appear to be reasonably trustworth
   and must appear to be competent in the relevant area.
5. Software must be named in a way that avoids confusion with other software.
6. There must be an active community for the software.

Note: I do not perform security audits and do not confirm that I understand
100% of the code.

# Index

The following software is included here:

1. password-store 1.6.5

# Suggestions and contributions

I haven't taken any suggestions or contributions yet. Feel free to submit them,
but keep in mind that I am ultimately responsible for this repository and may
disagree or discard any suggestions or contributions for any reason.
