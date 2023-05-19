- This is for checking you are not over- or under-utilizing resources, not for monitoring the health of your resources
- Evaluates your account by using checks, including:
	- Identify ways to optimize your AWS infrastructure
	- Improve security and performance
	- Reduce costs
	- Monitor service quotas
- Categories (very not inclusive):
	- Performance
		- Allows you to validate service limits - shows you usage and limits related to a specific AWS resource currently being used.
		- Ex: For an API, you can modify the throttle rate, increase auto-scaling limits, and discovery service limits.

## Examples
### Situations where Trusted Advisor would recommend actions
- Weak [[AWS IAM]] user password policies (security)
- EBS volumes with no snapshots (fault tolerance)
- MFA not turned on for root user (security)
- EC2 instances not properly launched across AZs (service quotas?)
- An idle RDS instance (reduce costs)