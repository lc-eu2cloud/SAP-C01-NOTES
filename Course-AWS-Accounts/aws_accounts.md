## AWS Accounts

* AWS account
  * a container of identities (aka users) & AWS resources
    * users: use to login to systems such as AWS; AWS resources: resources that you provision inside an AWS account
  * when creating an AWS account, you need to provide a name for the account, a unique email address (ie something@gmail.com, that unique email address only for that specific AWS account), & a payment method (ie credit card: can be used with multiple AWS accounts)
  * the email address that you provide when creating an AWS account is used to create a special type of identity within the AWS account which is known as the account root user
    * account root user is the only identity (user) that is created with an AWS account 
    * every AWS account will have its own account root user which cannot overlap with another AWS account
    * account root user has full control over an AWS account & any resources created inside it
    * account root user cannot be restricted (will always have full access to everything within the AWS account it belongs to)
    * if username & password of account root user ever become known, results can be disastrous (everything in the AWS account can be deleted)
   * credit card you provide when you create the AWS account is set as the account payment method
     * when you create resources within an AWS account, any of those resources with billable usage will be billed to the account payment method (aside: AWS known as pay-as-you-go platform)
    * certain services include certain allocation of free usage per month (known as AWS free tier)
    * 
