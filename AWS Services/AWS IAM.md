AWS Identity and Access Management

## About
- A web service that helps you securely control access to AWS resources.
	- You can centrally manage permissions that control which AWS resources users can access.

## User Account Best Practices
- Use MFA on the IAM user account
- Add a condition to the policy that only grants permissions based on a specific IP address
- Set a password policy on the account

## AWS Identities
- AWS root account user
	- Has complete access to all AWS services and resources in the account
	- Created when you first create an AWS account
- IAM Users
	- An identity within your AWS account that has specific permissions for a single person or application
	- Where possible, use short-term credentials for security
- IAM User Groups
	- An identity that specifies a group of IAM Users
	- Use groups to set permissions for multiple users at a time
- IAM Roles
	- An identity within your AWS account that has specific permissions
	- It's like an IAM User in that it is an AWS Identity that has specific permissions, but does not have a specific person assigned to it.
	- You can use roles to delegate access to users, applications, or services that don't normally have access to your AWS resources.


## Policies
### What can you do with policies?
- You can specify and enforce that data needs to be encrypted at rest or in transit

### What's in a policy?
- Effects
	- Determines the behaviors and actions of what the policy will allow

### Policy Types
*A principal entity can be a user, group, or role*
- A policy is an object in AWS that, when associated with an identity or resource, defines their permissions.
- When an IAM Principal makes a request, AWS evaluated the attached policies and determines whether the request should be allowed or denied.
- AWS Managed Policy`
	- A standalone policy that is created an administered by AWS
	- "Standalone" means the policy has its own Amazon Resource Name (ARN) that includes the policy name.
	- You can pick and choose managed policies to apply to principal entities
- Customer Managed Policy
	- When you create your own standalone policies in your AWS account that you then attach to principal entities
- Inline Policy
	- An inline policy is created for a single IAM entity (a user, group, or role).
	- Inline policies maintain a strict 1:1 relationship between a policy and an identity

### How to create an IAM policy
1. With the visual editor
	1. Select an action
	2. Choose a service
2. Without the visual editor
	1. Add a JSON policy document