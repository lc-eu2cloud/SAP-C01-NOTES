## Multi-factor Authentication (MFA) ##

#### MFA Overview ####
* #### when usernames & passwords leaked, anyone can be you when logging into an application (impersonate your identity; why MFA needed) ####
* #### Factors - different pieces of evidence used to prove one's identity/identities (single factor authentication only uses one of these factors) ####
  * Knowledge - something you know (usernames, passwords, PINs) 
  * Posssession - something you have (bank card: ATM requires bank card (something you have) & PIN (something you know), example of 2-factor MFA; MFA device/app)
  * Inherent - something you are (fingerprint, face scan, voice recognition, or iris scan)
  * Location - physical location (particular set of coordinates anywhere in the world), or type of network logged into to access a system (corporate network or home wifi)
  * More factors lead to more security & identities that harder to fake, but can be inconvenient (need balance between convenience & security)
    * highly secure but inconvenient login process: must use username & password, MFA device/app, fingerprint or facial scan, & only within corporate network
#### MFA within AWS ####
* start with AWS acccount & by default, only requires username & password to log in (something you know - single factor authentication)
* to setup MFA, need to configure MFA for identity within AWS account (ie account root user)
  * activate MFA for account root user, AWS generates secret key (randomly generated) & all associated information the MFA app can use visually (username linked to secret key & name of the service)
  * that information eventually needs to be entered into a MFA application (ie Google Authenticator)
  * to make this easier, AWS uses all generated information from MFA activation & generates a QR code which encodes that information into a visual pattern
  * Using MFA application on your phone, scan AWS generated QR code which transfers information in the QR code into MFA application as a new entry
  * this entry in the MFA application, provides a code that generates periodically (never the same)
  * MFA application holds one or more virtual MFAs (each virtual MFA, a virtual MFA device), each representing identities in different services (AWS, Gmail, Azure, GCP, etc)

* with MFA configured for specific user, now required to enter username, password, & prompted to enter MFA code
  * MFA code needs to be current code for correct virtual MFA on your specific authenticator application on your phone or on another device
  * providing username & password (something you know) with MFA code (something you have) means your identity within AWS is secured using multi-factor authentication
  * have to have all 3 to login (username, password, correct MFA code) 
  * can still be protected if username & password leaked or you lose your MFA device (bad actor has MFA device & code) as long as they don't know your username & password
* generally on most modern phones, MFA application will be protected with multi-factor authentication (requiring PIN code to login & potentially fingerprint/face scan to access MFA application) 
