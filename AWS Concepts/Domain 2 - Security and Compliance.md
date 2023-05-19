[[test-topics]]

## Define the AWS [[Shared Responsibility]] model
- Recognize elements of the [[Shared Responsibility]] model
- Describe the customer's responsibility on AWS
	- Describe how responsibilities may shift, depending on the service (ex: RDS, Lamda, or EC2)
- Describe AWS responsibilities

## Define AWS Cloud Security and compliance concepts
- Identify where to find AWS compliance information
	- Locations of lists of recognized available compliance controls (for example, HIPPA, SOCs)
	- Recognize that compliance requirements vary among AWS services
- At a high level, describe how customers achieve compliance on AWS
	- Identify different encryption options on AWS (ex: In Transit, At Rest)
	- Use [[AWS Key Management Service]] to encrypt data at rest and in transit.
	- Use [[AWS IAM]] policies to specify and enfore that data needs to be encrypted at rest or in transit.
- Describe who enables encryption on AWS for a given service
	- The customer (according to the [[Shared Responsibility]] model)
- Recognize there are services that will aid in auditing and reporting
	- Recognize that logs exist for auditing and monitoring
	- Define:
		- [[Amazon CloudWatch]] - Monitoring service for all AWS services. You can set alarms and view metrics.
		- [[AWS Config]] - Continually analyzes your AWS service configs, provides config change management, assists with troubleshooting service configs.
		- [[AWS CloudTrail]] - logging/monitoringn for all your AWS APIs. Good for auditing and storing the Who/What/When information from any API access.
- Explain the concept of least privileged access

---

## Identify AWS access management capabilities
- Understand the purpose of [[User and Identity Management]]
	- Access keys and password policies (rotation, complexity)
	- Multi-Factor Authentication (MFA)
	- AWS Identity and Access Management ([[AWS IAM]])
		- IAM Principal
			- Is an IAM User, an IAM Role, or an IAM Group.
		- Groups/users
			- An IAM User is an IAM Identity that is associated with a particular person.
			- An IAM Group is an Identity that specifies a group of IAM Users.
		- Roles
			- An identity within your AWS account that has specific permissions
			- It's pretty much like an IAM User, but it's not assigned to a specific person.
			- Use Roles to delegate access to users. applications, or services that don't normally have access to your AWS resources.
		- Policies
			- A policy is an object in AWS that, when associated with an identity or resource, defines their permissions.
			- When an IAM Principal makes a request, AWS evaluated the attached policies and determines whether the request should be allowed or denied.
		- Managed policies compared to custom policies
			- Managed policies are created and maintained by AWS
			- Custom policies are defined and maintained by you.
	- Tasks that require use of root accounts
	- Protection of root accounts

---

## Identify resources for security support
- Recognize there are different network security capabilities
	- Native AWS services ( for example, security groups, Network ACLs, AWS WAS ((Web Application Firewall)) )
	- 3rd party security products from the [[AWS Marketplace]]
- Recognize there is documentation and where to find it
	- AWS Knowledge center, Security Center, security forum, and security blogs
	- Partner Systems Integrations
- Know that security checks are a component of [[AWS Trusted Advisor]]