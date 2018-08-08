Make sure you have provided the following information:

 - [x] link to your code branch cloned from rhboot/shim-review in the form user/repo@tag
 - [x] completed README.md file with the necessary information
 - [x] shim.efi to be signed
 - [x] public portion of your certificate embedded in shim (the file passed to VENDOR_CERT_FILE)
 - [x] any extra patches to shim via your own git tree or as files
 - [x] any extra patches to grub via your own git tree or as files
 - [x] build logs


###### What organization or people are asking to have this signed:
Broadband Computer Company Ltd (http://www.broadbandcomputer.com)

###### Version of shim:
15

###### Sysdev Submission ID:
We were directed to the shim review board by Microsoft after submitting our shim to them for signing. Subsequently our original sysdev submission has been closed pending approval from the shim review board.

###### What product or service is this for:
Secure COAST 

###### What's the justification that this really does need to be signed for the whole world to be able to boot it:

Secure COAST is a security focused linux distro based on Ubuntu 18.04. 
We encourage our customers to boot our OS with secure boot enabled, hence the need for a 
signed shim.
