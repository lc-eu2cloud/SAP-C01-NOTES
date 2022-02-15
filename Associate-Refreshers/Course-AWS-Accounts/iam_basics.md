## Identity and Access Management (IAM) Basics

**IAM Basics**

Introduction
* In most real-world situations, you want capability to grant other people in your organization, access to your AWS account (ie might be users, groups, or applications they manage)
* generally want to _restrict_ the access that these people, groups, or applications have 
* BEST PRACTICE: least privileged access - you only give the permissions required to do a job or perform a task (ALWAYS! DO! THIS!)
* problematic only having a single identity in the account (account root user), if the account root user's credentials are leaked, then the damage could be account-wide
* need a way to allow more control over what access is given to our AWS accounts (solved by the IAM service)

IAM Service
* Every AWS account comes with its own running copy (database) of IAM
* globally resilient: data always secure across all AWS regions
* An AWS account trusts its own dedicated IAM instance (separate from IAM instances of other AWS accounts)
* operationally same as account root user (trusted fully by AWS account, can do as much as account root user with some restrictions)
  * restrictions around billing control & account closure
* can create different types of identities that it manages
  * if any of these IAM identities allowed to perform an action, AWS account automatically trusts the identity in same way it trusts IAM 
![IAM Service - AWS Account trusts IAM](https://i.postimg.cc/KYfn1BWw/image11.png)

Identity object types in IAM & IAM Policy Document
* can create 3 different types of identity objects in IAM (IAM users, IAM groups, IAM roles)
* IAM users: represent humans or applications that need access to an AWS account
* IAM groups: collections of related users (ie dev team)
* IAM roles: identity that can be used by AWS services or for granting external access to an AWS account
* Choosing between IAM users & IAM roles (general guidelines)
  * IAM users: can identify the individual person or application that will login to a specific IAM user
  * IAM roles: granting access to services in an AWS account to an **_uncertain_** number of entities (principals)
* IAM policy document: can create in IAM to simply define, allow or deny access rights to certain AWS services
* IAM policies are attached to IAM users, IAM groups, or IAM roles; ONLY time IAM policies have any effect (do nothing on their own)

IAM service's 3 main jobs

