[[Serverless computing]]

## About
- Allows you to run containers without having to manage servers or clusters of EC2 instances.
- AWS Fargate is a serverless compute platform for [[Amazon EKS]] or [[Amazon ECS]]
- You pay only for the resources required to run your containers.


## Fargate vs. [[AWS App Runner]]
- AWS App Runner will run your container, and manage horizontal scaling and concurrency as required (you just set the rules).
- Fargate - you manage the scaling and concurrency rules.
	- You can create scaling rules, which for example:
		- Can be based on metrics that [[Amazon ECS]] captures, such as CPU or memory consumption.
		- Can be based on metrics from the load balancer, such as concurrent requests or request latency.
		- You can create custom scaling metrics powered by the application itself.