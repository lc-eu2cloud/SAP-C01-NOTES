## Multi-factor Authentication (MFA) ##

* when usernames & passwords leaked, anyone can be you when logging into an application (impersonate your identity; why MFA needed)
* Factors - different pieces of evidence used to prove one's identity/identities (single factor authentication only uses one of these factors)
  * Knowledge - something you know (usernames, passwords)
  * Posssession - something you have (bank card: using bank card at ATM requires bank card (something you have) & pin (something you know), example of MFA (2); MFA device/app)
  * Inherent - something you are (fingerprint, face scan, voice recognition, or iris scan)
  * Location - physical location (particular set of coordinates anywhere in the world), or type of network logged into to access a system (corporate network or home wifi)
  * More factors leads to more security & identities that harder to fake (balance between convenience & security)
    * highly secure but inconvenient login process: must use username & password, MFA device/app, fingerprint or facial scan, & only within corporate network
* MFA within AWS
