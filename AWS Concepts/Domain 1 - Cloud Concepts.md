[[test-topics]]

## Define the AWS Cloud and its value proposition
- Define the benefits of AWS cloud, including:
	- Security - AWS has strict security controls
	- Reliability - how your application responds to failure. 5 key concepts:
		- Automatically recover from failure
		- Test recovery procedures
		- Scale horizontally to increase aggregate workload availability - use many small resources instead of one big one (avoid that single point of failure)
		- Stop guessing capacity - reduce chances of resource saturation by auto scaling resources to meet demand
		- Manage change in automation - changes to your infrastructure should be made using automation so they can be tracked and reviewed.
	- High Availability - horizontally scale resources, use multiple AZs, use load balancing
	- Elasticity - auto-scale your resources to meet demand
	- Agility - quick and easy to provision & deploy new resources
	- Pay-as-you-go pricing
	- Scalability
	- Global reach
	- Economy of scale
- Explain how the AWS cloud allows users to focus on business value
	- Shifting technical resources to revenue-generating activities as opposed to managing infrastructure

## Identify aspects of AWS Cloud economics
- Define items that would be part of a Total Cost of Ownership proposal
	- OpEx (Operational Expenditures) - 
	- CapEx (Capital expenditures) - 
	- Understand labor costs associated with on-premises operations
	- Understand the impact of software licensing costs when moving to the cloud [[need-to-finish]]
		- [[AWS License Manager]] can be used to manage software licenses from severla vendors in a centralized way.
- Identify which operations will reduce costs by moving to the cloud
	- Right-sized infrastructure
	- Benefits of automation
	- Reduce compliance scope (for example, reporting)
	- Managed services ([[Amazon RDS]], [[Amazon ECS]], [[Amazon EKS]], [[Amazon DynamoDB]])
- Explain the different cloud architecture design principles
	- Design for failure
	- Decouple components vs monolithic architecture
	- Implement elasticity in the cloud vs on-premises
	- Think parallel