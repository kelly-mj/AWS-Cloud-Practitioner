For [[Amazon EKS]] and [[Amazon ECS]], containers refer to [[Docker Containers]]
- These containers run on top of [[Amazon EC2]] instances and run in isolation from each other.
- When you use [[Docker Containers]] on AWS, you need processed to start, stop, restart, and monitor containers running across a cluster of EC2 instances.
	- This is called [[Container Orchestration]]

## How to choose container architecture
- EC2: Run containers on top of EC2 instances when you want:
	- To host traditional applications
	- Full access to the underlying OS
- AWS Lambda:
	- Host short-running functions
	- service-oriented or event-driven applications
	- And you don't want to manage the underlying environment at all
- [[Container Orchestration]]
	- Choose Amazon EKS or ECS
- Container Platform:
	- Run containers in EC2 instances
	- OR Run in a managed serverless environment like AWS Fargate