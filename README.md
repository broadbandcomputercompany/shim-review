This repo is for review of requests for signing shim.  To create a request for review:

- clone this repo
- edit the template below
- add the shim.efi to be signed
- add build logs
- commit all of that
- tag it with a tag of the form "myorg-shim-arch-YYYYMMDD"
- push that to github
- file an issue at https://github.com/rhboot/shim-review/issues with a link to your tag

Note that we really only have experience with using grub2 on Linux, so asking
us to endorse anything else for signing is going to require some convincing on
your part.

Here's the template:

-------------------------------------------------------------------------------
What organization or people are asking to have this signed:
-------------------------------------------------------------------------------
Broadband Computer Company Ltd (https://www.broadbandcomputercompany.com)

-------------------------------------------------------------------------------
What product or service is this for:
-------------------------------------------------------------------------------
Secure COAST

-------------------------------------------------------------------------------
What's the justification that this really does need to be signed for the whole world to be able to boot it:
-------------------------------------------------------------------------------
Secure COAST is a security focused linux distro based on Ubuntu 18.04. 
We encourage our customers to boot our OS with secure boot enabled, hence the need for a 
signed shim.

-------------------------------------------------------------------------------
Who is the primary contact for security updates, etc.
-------------------------------------------------------------------------------
- Name: Brian Daglish
- Position: CTO
- Email address: brian@broadbandcomputer.com
- PGP key, signed by the other security contacts, and preferably also with signatures that are reasonably well known in the linux community: https://github.com/broadbandcomputer/shim-review/blob/master/bdaglish.key

-------------------------------------------------------------------------------
Who is the secondary contact for security updates, etc.
-------------------------------------------------------------------------------
- Name: Jim Leslie
- Position: CEO
- Email address: jim@broadbandcomputer.com
- PGP key, signed by the other security contacts, and preferably also with signatures that are reasonably well known in the linux community: https://github.com/broadbandcomputer/shim-review/blob/master/jleslie.key

-------------------------------------------------------------------------------
What upstream shim tag is this starting from:
-------------------------------------------------------------------------------
https://github.com/rhboot/shim/tree/15

-------------------------------------------------------------------------------
URL for a repo that contains the exact code which was built to get this binary:
-------------------------------------------------------------------------------
https://github.com/rhboot/shim/tree/15

-------------------------------------------------------------------------------
What patches are being applied and why:
-------------------------------------------------------------------------------
None

-------------------------------------------------------------------------------
What OS and toolchain must we use to reproduce this build?  Include where to find it, etc.  We're going to try to reproduce your build as close as possible to verify that it's really a build of the source tree you tell us it is, so these need to be fairly thorough. At the very least include the specific versions of gcc, binutils, and gnu-efi which were used, and where to find those binaries.
-------------------------------------------------------------------------------
This repo contains the Dockerfile we use to build shim: https://github.com/broadbandcomputer.com/shim-build

-------------------------------------------------------------------------------
Which files in this repo are the logs for your build?   This should include logs for creating the buildroots, applying patches, doing the build, creating the archives, etc.
-------------------------------------------------------------------------------
build.log

-------------------------------------------------------------------------------
Put info about what bootloader you're using, including which patches it includes to enforce Secure Boot here:
-------------------------------------------------------------------------------
GRUB2, as shipped with Ubuntu 18.04 (source - https://launchpad.net/ubuntu/+source/grub2/2.02-2ubuntu8.2). No additional patches applied.

-------------------------------------------------------------------------------
Put info about what kernel you're using, including which patches it includes to enforce Secure Boot here:
-------------------------------------------------------------------------------
Linux Kernel 4.15, as shipped with Ubuntu 18.04. No modifications or patches applied.

