
AKA: EIP

- A static and public IP address that AWS uses to allow their customer to use as they see fit.
- These IP addreses are pooled and used based on the customer's AWS account.
- EIPs have associated costs whether they are used or not.
- EIPs are fixed to a [[Region]] and cannot be used in other Regions.
- EIPs are synonymous with your netowrk interface and are assigned to instances within your [[Amazon VPC]].
- You are limited to 5 EIPs per Amazon account
- Only supports IPv4 addresses (not IPv6)
- You can only assign 1 EIP to 1 [[Amazon EC2]] instance at a time

- Main benefit: ==You can move network attributes from one instance to another in one single step==