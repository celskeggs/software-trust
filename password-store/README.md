# Password store

Password store is hosted at https://www.passwordstore.org/

There is one version of the software in this directory, version 1.6.5.

# Summary

I believe that the software contained here is reasonably trustworthy, as
detailed below, except for the following elements, which I have either not
inspected, or have not understood well enough to inspect:

* The emacs integration
* The importers (except for the LastPass importer)

# Checklist

This software passes the following checks:

1. Passed. Only hidden file is .gitignore.
2. All code appears to pass formatting checks.
3. All code has been briefly inspected, except for:
     * The emacs integration (I lack the necessary skill)
     * The importers, except for lastpass2pass.rb, which has been briefly
       inspected.
4. PGP key chain of trust:
   * 0xEEA31BFF444304ABB246A0B6C634D0420F825B91: Cel A. Skeggs <cela.at.mit.edu>

     I trust myself. I believe that I sign keys correctly and keep my key
     material reasonably safe.
   * 0x95A2E697058CE1EBE12ACC95D0BF6A7BF7291809: Adam Suhl <ashul.at.mit.edu>

     I trust them directly, and believe that they would sign keys correctly and
     keep their key material reasonably safe.
   * 0xE9A271C071964891AA57663D9EA33414F5852F4E: Benjamin Mako Hill <mako.at.mit.edu>

     I trust their identity indirectly. Due to publicly available information
     on their website and on Wikipedia, I believe that it is likely that they
     would sign keys correctly and keep their key material reasonably safe.
   * 0xEB32D67638C4E3D8AA2403F0BEBD933335FC140B: Moray Allan <moray.at.sermisy.org>

     I trust their identity indirectly. Their involvement in Debian makes it
     PLAUSIBLE that they would sign keys correctly and keep their key material
     reasonably safe.
   * 0xB8FAC2E250475B8CE940A91957930DAB0B86B067: Joost E. van Baal (Nederland, 1970)

     I trust their identity indirectly. The information available on their
     website makes it likely that they would sign keys correctly and keep their
     key material reasonably safe.
   * 0xAB9942E6D4A4CFC3412620A749FC7012A5DE03AE: Jason A. Donenfeld <Jason.at.zx2c4.com>

     I trust their identity indirectly. This was the key used to sign the git
     tag that I verified for this version of the software. The code contained
     in the tag matches the code in the version kept here exactly.
5. The author appears to be a reasonably trustworthy software developer, and
   appears to be accomplished and skilled in the area.
6. The name isn't the most clear, but it does not appear that there is any
   other easily-searchable website claiming to host the same software.
7. There appears to be an active community for the software.

# Notes of Concern

The following are places where I noticed something that could potentially be a
bug or vulnerability, and that requires further thought. It also includes the
reasons that these do not disqualify the software from verification.

1. In password-store.sh:81, GPG recipients are, in some cases, loaded from
   files in data storage that might be able to be tampered with. However, this
   is a documented feature and an unlikely attack vector.
2. In password-store.sh:93, a temporary filename is generated via ${RANDOM},
   rather than a temporary file generation utility. However, the file is stored
   along with the stored file itself, meaning that if the directory is
   accessible to an attacker, there are worse problems than temporary file
   generation race conditions.
3. In password-store.sh:100, 'eval' is used, perhaps unnecessarily. On the
   other hand, this appears to be the recommended solution from the referenced
   question on Stack Exchange.
