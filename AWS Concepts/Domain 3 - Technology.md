[[test-topics]]

## Define methods of deploying and operating in the AWS Cloud
- Identify different ways of provisioning and operating in AWS Cloud
	- Programmatic access
	- APIs
	- [[Software Development Kits]]
	- [[AWS Management Console]]
	- [[AWS Command Line Interface]]
	- [[infrastructure-as-code]]
- Identify different types of cloud deployment mdoels
	- Cloud-native
	- Hybrid
	- On-premises
- Identify connectivity options
	- VPN
	- [[AWS Direct Connect]] - establish a dedicated network connection from your data center to AWS
	- Public internet

---

## Define the [[AWS Global Infrastructure]]
- Describe the relationships among [[Region]]s, [[Availability Zone]]s, and [[Edge Locations]]
	- Regions contain many AZs
	- AZs are a single data center or a group of closely-spaced data centers
	- Edge Locations are separate from Regions. Edge Locations are located closer to users than AZs or Regions (often in major cities), so content can be served faster.
		- You can push content from a Region to an Edge Location for faster serving.
		- A subset of services which use Edge Locations:
			- [[Amazon CloudFront]] uses edge locations to cache content and serve it geographically closer to end users
			- [[Amazon Route 53]] serves DNS responses from edge locations so that DNS queries which originate nearby can resolve faster.
- How to achieve high availability through the use of multiple AZs?
	- Use multiple AZs, as AZs do not share a single point of failure.
- When to consider the use of multiple [[Region]]s?
	- Disaster recovery/business continuity
	- Low latency for end users - if you have users worldwide, put content in a Region closer to them (or perhaps cache it in an edge location)
- What are the benefits of [[Edge Locations]]?
	- [[Amazon CloudFront]] - caches static or dynamic content to serve to users
	- [[AWS Global Accelerator]] - speeds up your traffic by routing it through the AWS Global Infrastructure. Achieves this by proxying packets at edge locations.

---

## Identify Core AWS resources:
==Compute==
- There are different compute families
- There are different services which provide compute
	- [[AWS Lambda]]
	- [[Amazon ECS]]
	- [[Amazon EC2]]
	- etc.
- What is the purpose of load balancers?
	- Distribute requests across compute resources

==Storage==
- Identify different AWS storage services
	- [[Amazon S3]] - object-level storage, up to 5TB per object
	- [[Amazon EBS]] - block-level storage, can store petabytes of data, designed for use with a single EC2 server
	- [[Amazon S3 Glacier]] - for data you don't plan to access, longer retrieval times
	- [[AWS Snowball]] - upload data to a device and ship it back to AWS to be uploaded
	- [[Amazon EFS]] - fully managed NFS which utilizes block-level storage
	- [[AWS Storage Gateway]] - hybrid cloud storage services that provides on-premises access to cloud storage
	- [[Amazon Redshift]] - managed petabyte-scale data warehouse. Uses columnar storage and can store either structured or unstructured data.
	- [[Instance Store]] - temporary storage attached to an EC2 instance. All data written to the store is deleted when the EC2 instance is stopped or terminated.

==Network==
- Identify AWS network services:
	- VPC - Virtual Private Cloud
	- Security groups - Acts as a virtual firewall for your EC2 instance to control all inbound and outbound traffic.
	- Identify the purpose of [[Amazon Route 53]]
		- Route 53 is a DNS.
		- It is smarter than the usual 'dumb' DNSs (such as GoDaddy or CloudFlare), because it can be tightly integrated with the rest of your AWS setup.
		- 'Smarter' means Route 53 can monitor the health of your resources, and automatically route traffic only to healthy instances (whereas a 'dumb' DNS will direct traffic exactly where you tell it to - you need to update the DNS yourself if traffic needs to be routed away from a downed instance)
		- You can also create subdomains and handle them within Route 53.
	- Identify VPN, [[AWS Direct Connect]]
		- VPN Virtual Private Network: Amazon has a couple of offerings for this ([[AWS Client VPN]] and [[AWS Site-to-Site VPN]])
			- VPNs allow you to securely connect and transfer data between 2 devices on the internet.
		- AWS Direct Connect: Allows you to ==connect to the cloud from on-premises via a dedicated connection==

==Database==
- Identify different AWS Database services
- Install databases on [[Amazon EC2]] compared to AWS managed databases
	- If you install a database yourself, you need to manage the software, OS, patching, etc.
	- A fully managed service will handle all of that for you.
- Identify [[Amazon RDS]]
	- A managed service compatible with many popular relational databases (MariaDB, PostgreSQL, MySQL, etc)
- Identify [[Amazon DynamoDB]] - A serverless, fully-managed, low latency, highly available NoSQL key-value database. Caters to up to 45 million requests per second.
- Identify [[Amazon Redshift]]
	- Managed ==petabyte-scale== [[Data Warehousing]] solution
	- Stores structured and unstructured data
	- Utilizes columnar storage (this speeds up performance when fetching large sets of contiguous data, as opposed to row storage)

---

## Identify Resources for Technology Support
- Recognize there is documentation
	- Best practices
	- Whitepapers
	- AWS Knowledge Center
	- Forums/blogs
- Identify the various level and scope of AWS Support
	- [[AWS Abuse]] [[need-to-finish]]
	- AWS Support Cases
	- Premium support
	- Technical Account Managers - provide consultative architectural and operational guidance. A TAM will work with you to provide tailored engagements. They will also cover progress made towards your desired outcomes, and validate the planned outcomes in subsequent periods of performance.
- Recognize there is a partner network (marketplace, third-party) including independent software vendors and system integrators.
- Identify sources of AWS technical support and knowledge, including:
	- Professional services
	- Solution architects
	- Training and certification
	- The Amazon Partner Network
- Identify the benefits of [[AWS Trusted Advisor]]
	- Evaluates your account against checks, including:
		- Ways to optimize your AWS infrastructure
		- Improve security
		- Improve reliability
		- Reduce costs
		- ==Monitor service quotas==