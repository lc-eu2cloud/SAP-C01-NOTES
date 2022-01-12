## AWS Accounts

* AWS account
  * a container of identities & AWS resources, where identities aka users
    * users: what you use, to login to systems such as AWS; AWS resources: resources you provision inside an AWS account
  * when you create an AWS account, you need to provide a name for the account, a unique email address only for that specific AWS account, & a payment method (ie credit card, which can also be used for multiple AWS accounts)
  * the email address that you provide when creating the AWS account, is used to create a special type of identity within the AWS account, known as the account root user
    * the account root user is the only identity (user) created with an AWS account 
    * every AWS account will have its own account root user, which cannot overlap with another AWS account
    * the account root user has full control over an AWS account & any resources created inside it
    * the account root user cannot be restricted (it will always have full access to everything within the AWS account it belongs to) (t)
    * if the username & password of the account root user ever becomes known, the results can be disastrous (everything in that AWS account can be deleted) (t)
  * the credit card you provide when you create the AWS account, is set as the account payment method (t)
    * any resources you create inside an AWS account with billable usage, will be billed to the account payment method
  * certain services include a certain allocation of free usage per month, known as the AWS free tier
 
* AWS account security
  * as before, the account root user has full control over an AWS account & cannot be restricted
  * with the Identity and Access Management (IAM) service, you can create other identities inside the account
    * different types of identities such as IAM users, IAM groups, & IAM roles
    * all of these IAM identities start off with no access to the AWS account, but can be given or explicitly granted, full or limited access rights or permissions over this one specific AWS account
  * the IAM service is dedicated to your account & unless you specify otherwise, any IAM identities in your account, won't be able to access another account
  * AWS Account Boundary: can keep things inside the account from getting out, & can keep things outside the account from getting in
    * an example of how AWS accounts are really good at containing any damage caused within those accounts (t)
      * like a mistake caused by inexperienced system administrator or a bad actor attempting to intentionally harm your account  
    * if the account root user's credentials are leaked, can be very bad if your entire business runs from that account, as everything inside that one specific AWS account could be deleted (t)
    * if you create separate AWS accounts for different uses (a DEV account, test account, & a production account), then you can limit the damage caused, by the following: (t) 
      * any credential leakage or system administrators causing resources to be deleted (these generally, will be isolated to that one specific AWS account) (t)
    * you can also create AWS accounts for different teams within your business or for different products your business sells
    * AWS accounts are great for keeping bad things, inside one specific part of your AWS environment
  * by default, all access to an AWS account is denied, unless you configure otherwise, except for the account root user (which always has full control)
    * this means external identities (users) are denied, by default, if they attempt to access your AWS account
![External identity explictly granted access to an AWS account](https://i.postimg.cc/PxTqNt2m/image6.png)
  * external identities, can be granted access to your AWS account, like Julie in the middle (image above), if you explicitly allow this access
