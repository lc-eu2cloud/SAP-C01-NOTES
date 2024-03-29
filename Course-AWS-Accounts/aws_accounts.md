## AWS Accounts

**AWS Account**
* a container of identities & AWS resources (identities aka users)
* users: login to systems such as AWS; AWS resources: resources you provision inside an AWS account
* AWS account creation: need to provide a name for the account, a unique email address only for that specific AWS account, & a payment method (ie credit card, can be used for multiple AWS accounts)
* account root user: special type of identity within the AWS account created from email address provided
  * only identity (user) created with an AWS account & CANNOT overlap with another AWS account  
  * full control over an AWS account & any resources created inside it
  * cannot be restricted (will always have full access to everything within the AWS account it belongs to)
  * results can be disastrous if username & password ever becomes known (everything in that AWS account can be deleted)
* the payment method (ie credit card) provided from AWS account creation, is set as the account payment method
  * any resources you create inside an AWS account with billable usage, will be billed to the account payment method
* AWS Free Tier: certain services including a certain allocation of free usage per month
 
**AWS Account Security**
* the account root user has full control over an AWS account & cannot be restricted
* can create other identities inside the AWS account with the Identity and Access Management (IAM) service (IAM users, IAM groups, & IAM roles)
* all IAM identities start off with no access to the AWS account, but can be given or explicitly granted, full or limited access rights or permissions over this one specific AWS account
* the IAM service is dedicated to your account & unless you specify otherwise, any IAM identities in your AWS account, won't be able to access another AWS account

AWS Account Boundary 
* can keep things inside the account from getting out, & can keep things outside the account from getting in
  * an example of how AWS accounts are really good at containing any damage caused within those accounts  
* an entire business running in one specific AWS account could result in everything being deleted (account root user credential leakage)
* can limit/isolate the damage caused to your AWS account, if you create separate AWS accounts for different uses (a DEV account, test account, & a production account)
* can create AWS accounts for different teams within your business or for different products your business sells
* AWS accounts are great for keeping bad things, inside one specific part of your AWS environment
* by default, ALL access to an AWS account is denied unless you configure otherwise, except for the account root user
* external identities (users) are denied by default, if they attempt to access your AWS account
![External identity explictly granted access to an AWS account-image6](https://user-images.githubusercontent.com/88348559/197242691-cf448d3d-aa52-4102-98e6-6356e5f8a25b.png)
* external identities can be granted access to your AWS account, like Julie in the middle (image above), if you explicitly allow this access
