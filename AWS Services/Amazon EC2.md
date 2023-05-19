AWS Elastic Cloud Computing

## About
- EC2 instances are virtual machines that you can provision with minimal friction to get up and running on AWS.

### Pricing & Contract Types
- On-Demand Instance
	- Pay for compute capacity by the hour or second with no long-term commitments.
	- Ideal for short-term, irregular workloads which can be interrupted.
- Reserved Instance
	- A billing discount applied to the used of On-Demand Instances in your account.
	- ==Standard Reserved==: You are not allowed to make changes during the term of your contract (1- or 3-year contract)
	- ==Convertible Reserved==: During your contract, you can exchange your instance to update the instance type, platform, etc. Contracts are 1- or 3-year terms.
	- ==Scheduled Reserved==: [[need-to-finish]]
	- Must choose one of two contract lengths: 1 or 3 years
		- Unless you choose ==full or partial upfront== - then you are not bound to term limits
	- At the end of a Reserved Instance term, you can continue to use the EC2 instance without interruption. You are charged On-Demand rates until you either terminate the instance, or purchase a new Reserved instance that matches the instance attributes.
	- ==An abnormal increase in workload should be handled with Spot or On-Demand instances==
- Spot Instance
	- Least costly option (discount of up to 90% compared to On-Demand instances)
	- Ideal for workloads with flexible start/end times, or can withstand interruptions.
	- Ex: Good for a workload that runs for a total of 6 months, and can withstand interruptions.
	- Also good for: security testing, developing, integration, and validating overall loads on a system
- Dedicated Instance
	- Runs in a [[Virtual Private Cloud]] on hardware dedicated to a single customer.
	- Has a higher cost than other instance types, which run on shared hardware.
	- Ideal for short-term, irregular workloads which **cannot** be interrupted.
- EC2 Savings Plan
	- Reduce your bill by up to 73% compared to On-Demand prices, in exchange for a commitment to a consistent amount of usage (measured in $/hour) for a 1- or 3-year term.
	- Any usage up to the committment is charged at the discounted Savings rate. Any usage after the committment is charged at regular On-Demand rates.
	- [[AWS Cost Explorer]] can provide recommentations on Savings Plans, based on previous EC2 usage and the hourly commitment required.

### Instance Types
- ==General purpose==: A balance of compute, memory, and networking resources. Good for application servers, gaming servers, backend servers, and small-medium databases.
- ==Memory optimized==: Ideal for workloads that process large datasets in memory, such as high-performance databases, or sorting large amounts of data in memory.
	- You could use Memory Optimized for a ==high-performance database==, (NOT the Storage Ooptimized option), because the extra memory enables your instance to hold LARGE amounts of data in memory and process it.
- ==Compute optimized==: Ideal for workloads which benefit from a high-performance workload, such as batch processing, high-performance web servers, compute-intensice application servers, and dedicated gaming servers.
- ==Storage optimized==: Designed for workloads which require high, sequential read-write access to large datasets on local storage. Good for high IOPS (input/output operations per second) workloads.
- ==Accelearated computing==: Uses hardware accelerators to perform some functions more efficiently than with the processor alone. Good for floating-point calcs, graphics processing, and data pattern matching. Ideal workloads include graphics applications, game streaming, and application streaming.


## Scaling
### EC2 Auto-Scaling
- Automatically add or remove EC2 instances in response to changing demand.
- ==Dynamic scaling== responds to changing demand
- ==Predictive scaling== schedules EC2 instances based on past demand.

#### Creating an Auto-Scaling group
- Set the minimum capacity (the number of EC2 instances that must be running at all times)
- Set the desired capacity  (defaults to the minimum capacity, if not set)
- Set the maximum capacity

### Auto-Scaling plans
- **Maintain current level**: have a specific or minimum number of instances running 24/7. Unhealthy or stopped instances are automatically replaced.
	- Does not respond to changes in demand.
- **Dynamic Scaling**: Scales based on changing demand.
- **Scheduled scaling**: Scales at predetermined times
- **Manual scaling**: Manually manage your instances in the Amazon EC2 console.

## [[Shared Responsibility]]
- AWS
- Customer
	- Patching instances with OS and software updates
	- Setting up scaling for the instances
	- Ensuring you've architected your solutions to be highly available.

## Security
### Security groups
- Acts as a virtual firewall for your EC2 instance to control all incoming and outgoing traffic.
- You can specify one or more security groups.
- Default security group allows all outbound traffic, and denys all inbound traffic.

### Best Practices
- Create a primary function for each EC2 instance, such as separating web servers from database servers

### Common attacks
- Botnets - includes Trojan horses and worms. A virus that attempts to infect a large set of EC2 instances and can be controlled by en external entity.
- SPAM - places a system under siege by having an attacker distribute large amounts of unsolicited mail throughout your network.

## Monitoring
- Basic monitoring updates in 5-minute increments.
- Detailed monitoring enables monitoring in 1-minute increments.

## How it works
- If you have applications that you want to run in EC2, you must:
	- Provision instances
	- Upload your code
	- Continue to manage the instances while your application is running

### Best Practices
- Run EC2 instances for your applications in multiple AZs, to guard against application failure if one AZ were to go down.