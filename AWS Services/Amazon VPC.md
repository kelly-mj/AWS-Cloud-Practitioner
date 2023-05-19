Amazon Virtual Private Cloud

## About
- Logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network that you define.
- Closely resembles a traditional network that you'd operate in your own data center.
- You can add subnets after creating a VPC.
- Default number of VPCs per [[Region]] is 5. You need to request a quota increase to get more in a Region.

- When your VPC is created, it automatically comes with a route table that can be modified.

### Subnets
- A subnet is a range of IP addresses in your VPC.
- Each subnet must reside entirely in one [[Availability Zone]] and cannot span zones.
- Subnets operate as a subdomain within your organization's domain.
- Each subnet is required to be associated to a route table.
- If you don't have a specified routing table for a subnet, it will use the default route table.

## Virtual Private Gatweay
- Establishes connection between your VPC and a private netowork, such as on-prem data cnter or internal corpoarte natwork
- Only allows traffic from approved sources

## The VPC only consists of two unique endpoints - Gateway and Interface
- Gateway type endpoint
	- Does not require an Internet gateway
	- Has a primary function to link between your VPC and AWS services
	- This particular type only works with [[Amazon DynamoDB]] and [[Amazon S3]] services.
- Interface type endpoint
	- Creates a private connection to AWS services on your side of the network that links your company resources to AWS using [[AWS Direct Connect]].
	- Supports more services than just DynamoDB and S3.


## VPC to VPC Conectivity
- VPC Peering
	- Uses private IPv4 or IPv6 addresses to ==connect Amazon VPCs in the same [[Region]]==, allowing them to communicate as if they were in the same network.
- [[AWS Transit Gateway]]
	- ==Regional router connections== between VPCs
- Software Site-to-Site VPN - VPN connections between VPCs ==using software appliances==
- Software VPN-to-AWS Managed VPN - Connectivity between VPCs through software appliance to VPN connections
- AWS Managed VPN - Customer-managed ==VPC-to-VPC routing using IPSec VPN connections==
- [[AWS PrivateLink]] - AWS uses ==interface endpoints to provide network connectivity between two VPCs==

## Internet connectivity to a VPC
- You must create a public subnet and have that subnet use the Internet. There are 3 critical tasks:
	- Configure the security group and NACL to permit Internet traffic from and to your [[Amazon EC2]] instance
	- Create a subnet rule that sends non-loacl traffic using (0.0.0.0/0) to the Internet Gateway (IGW)
	- Attach an IGW component to the VPC in question

## Security
### Security groups
- Acts as a virtual firewall for your EC2 instance to control all incoming and outgoing traffic.
- You can specify one or more security groups.
- Default security group allows all outbound traffic, and denys all inbound traffic.
- You must specify a new security group for a new VPC.
- Considered stateful (as opposed to NACLs, which are considered stateless)

### NACLs
- Network Access Control Lists
- Allows or denies specific inbound or outbound traffic ==at the subnet level==
- Stateless

### View details about network traffic within your VPC
- Use VPC FLow Logs
	- Gives you the ability to gather details regarding IP addresses going from and to different network components within your VPC
	- Gets stored in [[Amazon CloudWatch]]
	- You're not charged for VPC Flow Logs, but you are charged for CloudWatch logs.