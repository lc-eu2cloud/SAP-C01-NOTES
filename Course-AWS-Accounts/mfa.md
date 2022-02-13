## Multi-factor Authentication (MFA) ##

#### MFA Overview ####
* #### need for MFA: username & password leakage means anyone can be you & impersonate your identity to login into an application ####
* #### Factors - different pieces of evidence used to prove one's identity/identities (single factor authentication uses only 1 factor) ####
  * Knowledge - something you know (usernames, passwords, PINs) 
  * Posssession - something you have (MFA device/app, bank card)
  * Inherent - something you are (fingerprint, face scan, voice recognition, or iris scan)
  * Location - physical (particular set of coordinates anywhere in the world), or network (corporate or home wifi)
* #### More factors lead to more security & identities that harder to fake, but need balance between convenience & security
  * requiring username & password, MFA device/app, fingerprint or facial scan, & only within corporate network (highly secure, but inconvenient)
#### MFA within AWS ####
* start with AWS account & by default, login only requires username & password (something you know - single factor authentication)
* MFA setup needs to configure MFA for identity within AWS account: (ie account root user)
  * MFA activation: AWS randomly generates secret key linked to username (ie account root user)
  * AWS generates QR code from MFA activation information, encoding it into a visual pattern
  * MFA phone application scans QR code, transferring information from QR code into MFA application as a new entry
  * this entry in the MFA application provides a periodically generated code (never the same)

NOTE: Each virtual MFA (a virtual MFA device) in MFA application represents identities in different services (AWS, Gmail, Azure, GCP, etc)
* with MFA configured for specific user, login now requires username, password, & MFA code
  * MFA code needs to be current code from correct virtual MFA on specific authenticator application (a phone or another device) 
* providing username & password (something you know) with MFA code (something you have) means your identity within AWS is secured using multi-factor authentication
* protected if username & password leaked or if bad actor has MFA device & code, but not username & password
