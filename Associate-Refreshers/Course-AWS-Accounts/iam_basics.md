## Identity and Access Management (IAM) Basics

**IAM Basics**
* In most real-world situations, you want to be able to grant other people in your organization, access to your AWS account (ie might be users, groups, or applications they manage)
* generally want to _restrict_ the access that these people, groups, or applications have 
* BEST PRACTICE: least privileged access - you only give the permissions required to do a job or perform a task (ALWAYS! DO! THIS!)
* problematic only having a single identity in the account (account root user), if the account root user's credentials are leaked, then the damaage could be account-wide
* need a way to allow more control over what access is given to our AWS accounts 
