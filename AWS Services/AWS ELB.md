AWS Elastic Load Balancing

## About
- A load balancer act as a single point of contact for all incoming web traffic to your Auto Scaling group, then the requests are spread over multiple resources.
- You can distribute traffic across multiple targets (including EC2, [[Amazon ECS]], and [[AWS Lambda]])

### Locality
- ELB is a regional construct - apparently this will be explained later
	- Explanation: ELB runs at a [[Region]] level rather than on individual [[Amazon EC2]] instances

### Scaling
- ELB is automatically scalable - it will handle additional throuput **with no change to the hourly cost**.
- **Scaling up**: EC2 fleet will notify ELB when the fleet auto-scales out, so ELB can direct traffic to the newly online instances.
- **Scaling down/in**: When an EC2 fleet scales in , ELB:
	- ELB stops all new traffic
	- ELB waits for the existing requests to drain out (complete)
	- Once the existing request shave drained, the auto-scaling engine xan terminate the instances without disruption to existing customers.

## How It Works
- A single URL is used to route traffic to your servers.

## Security
- Predefined security policies are used to determine which protocols and ciphers are occurring between the load balancer and the client

## Use Cases
- External traffic
	- Obvioiusly
- Insternal traffic
	- Ex: Use ELB to route traffic between a network of backend servers and several UI servers. This is truly decoupled architecture, as the frontend doesn't know and doesn't care about how many backend instances are running.