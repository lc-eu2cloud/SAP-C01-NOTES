## Identity and Access Management (IAM) Basics

* IAM Basics
  * In most real-world situations, you want to be able to grant, other people in your organization, access to your AWS account (ie might be users, groups, or applications they manage)
    * you generally want to restrict the access that these people, groups, or applications have 
  * BEST PRACTICE: least privileged access - you only give the permissions required to do a job or perform a task (ALWAYS! DO! THIS!)
  * only having, a single identity in the account, is also problematic (if the credentials are leaked for the account root user, then the damaage could be account-wide)
  * what we need, is a way to allow more control over what access is given to our AWS accounts 
