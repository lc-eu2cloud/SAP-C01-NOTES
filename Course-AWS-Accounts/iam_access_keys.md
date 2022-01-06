## IAM Access Keys - Encryption 101 Refresher recommended

#### Introduction ####
* Authentication to access AWS using the command line or within other applications using APIs, is not done via username, password, & MFA but using IAM access keys instead
* access keys and a username & password within AWS are known as long-term credentials (used with IAM users)
* if you're authenticating to AWS using an IAM user identity, you'll either provide a username & password when using console UI or access keys when using the CLI (command-line interface)
* access keys, username & password are called long-term credentials because they don't change regularly or rotate (the owner must change/update these credentials explicitly)
![Long-term credentials](https://i.postimg.cc/hGfC0jyP/image3.png)
* #### IAM Access Keys & Username & Password ####
  * whilst access keys are similar to the username & password an IAM user identity within AWS uses, there are some crucial differences to understand 
    * an IAM user can only have 1 username & 1 password (even when the password is changed, max of 1 at a time), but can have max of 2 access keys (0,1 & no more than 2)
    * access keys can be created, deleted, made inactive or made active (made active by default when created)
  * IAM users used only for the CLI or API access, do not require a password (password on IAM user is optional)
  * with usernames & passwords, username is the public part, whilst password is the private part (okay if username exposed, bad if username & password exposed; MFA additional private part to one's credentials, making it harder to leak full set of credentials: username, password, MFA)
* #### How IAM Access Keys are Formed ####
  * first part: access key ID
  * second part: secret access key (looks longer & more complex, shown below)
![IAM Access Key structure](https://i.postimg.cc/3wVtfTVj/image4.png)
  * when you create access keys (access key ID, secret access key) both of these parts are provided by AWS
    * once provided with these parts, there's no way to get access to the secret key again (AWS doesn't allow future downloads of secret access key)
    * NOTE: important to note down secret access key & store it safely and securely when AWS initially provides it
    * both access key ID (public) & secret access key (private) are used when making a request to AWS using the command line
    * since AWS stores access key ID, they'll know when you're using the secret access key to sign the request, making it a valid request

