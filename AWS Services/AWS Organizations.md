## About
- An account management service that enables you to consolidate multiple AWS accounts into an *organization* that you create and centrally manage.
- Includes:
	- Account management
	- Billing consolidation
- Helps you achieve your business needs better:
	- Budgetary
	- Security
	- Compliance
- As an organization administrator, you can:
	- Create new accounts in your organization
	- Invite existing accounts to join the organization

### Features
- Centralized management of all your AWS accounts
- Consolidated billing for all member accounts
	- Management accounts can also access the billing information, account information, and account activity of member accounts in the organization.
	- This may be used in tandem with [[AWS Cost Explorer]], which can help management accounts improve their organization's cost performance.
- Hierarchical grouping of accounts
	- You can group accounts into organizational units (OUs), and attach different policies to each OU.
	- You can nest OUs within other OUs (max depth of 5 levels)
	- For example, if an OU cannot have access to a service due to regulatory requirements, you can attach a policy to the OU that blocks access to the service.
- Policies to centralize control over the AWS services and API actions that each account can access
	- You can use Service Control Policies (SCPs) to specify the max permissions for member accounts.
		- You can restrict AWS services, resources, and individual API actions.
		- You can define conditions on when the restrictions apply
- Policies to standardize tags across the resources in your accounts
- Policies on how AWS AI/ML services can collect and store data
- Policies to configure automatic backups for the resources in your org's accounts
- Integration and support for [[AWS IAM]]