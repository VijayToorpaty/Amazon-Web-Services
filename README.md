# Amazon-Web-Services
AWS Solutions Architect Associate SAA-C01 + SAA-C02

**************************** Notes ***********************************

Cloud Computing : 
===============
-It can be defined as delivering computing power( CPU, RAM, Network Speeds, Storage OS software) a service over a network (usually on the internet) rather than physically having the computing resources at the customer location.

Example:
========
AWS, Azure, Google Cloud

Basic Constructs :
================

IAM User: 
========
IAM user is an entity that represents a person or a service.
-> It can be assigned an access key ID and secret access key for programmatic access to the AWS API, CLI, SDK and other development tools
-> A password for access to the management console
-> By default users cannot access anything in your account
-> The account root user credentials are the email address used to create the account and a password.
-> The root account has full administrative permissions and these cannot be restricted
** Best practice for root accounts: **
-> Don't use the root user credentials
-> Don't share the root user credentials
-> Create an IAM user and assign the administrative permissions as required.
-> Enable multi-factor authentication (MFA)
-> IAM users can be created to represent applications and these are known as "service account"
-> You can have upto 5000 users per AWS account
-> Each user account has a friendly name and an Amazon Resource Name (ARN) which uniquely identifies the user across AWS.
-> You should create individual IAM accounts for users best practice not to share accounts.
-> A password policy can be defined for enforcing password length, complexity etc (applies to all users).


IAM Groups:
===========
-> Groups are collections of users and have policies attached to them
-> A group is not an identity and cannot be identified as a principal in an IAM policy.
-> Use groups to assign permissions to users
-> Use the principal of least privilege when assigning permissions
-> You cannot nest groups (groups within groups)


IAM Roles:
==========
-> Roles are created and then "assumed" by trusted entities and define a set of permissions for making AWS service requests
-> With IAM Roles you can delegate permissions to resources for users and services without using permanent credentials (e.g. username and password)
-> IAM users or AWS services can assume a role to obtain temporary security credentials that can be used to make AWS API calls.


IAM Policies:
============
-> Policies are documents that define permissions and can be applied to users, groups and roles
-> Policy documents are written in JSON (key value pair that consists of an attribute and a value)
-> All permissions are implicitly denied by default
-> The most restrictive policy is applied
-> The IAM policy simulator is a tool to help you understand, test and validate the effects of access control policies.
-> The condition element can be used to apply further conditional logic
