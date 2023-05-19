
## About
- A tool to track and take action on your AWS costs and usage
- Use AWS Budgets to monitor your aggregate utilization and coverage metrics for your [[Amazon EC2]] Reserved Instances or Savings Plans.

### Simple to complex cost and usage tracking
- Set a monthly cost budget with a fixed target amount to track all costs associated with your account.
	- you can choose to be alerted for both actual (after accruing) and forecasted (before accruing) spends.
- Set a monthly cost budget with a variable target amount, with each subsequent month growing the budget target by 5%.
- Set a monthly budget to ensure you are staying within service limits for an individual service.
	- You can also set it to make sure you stay in the AWS Free Tier.
- Set a daily utilization or coverage budget to track your Reserved Instance or Savings Plans.

### Create budgets
- Cost budgets - Plan how much you want to spend on a service
- Usage budgets - Plan how much you want to use one or more services.
- RI utilization budgets - Define a utilization threshold and receive alerts when your RI falls below the threshold (see if RIs are being unused or underutilized).
- RI coverage budgets - Define a coverage threshold and receive alerts when the number of instance 

### Budgets vs. [[AWS Cost Explorer]]
- Budgets is meant for *forecasting*
	- Focus on cost planning, enforcement, and forecasting costs that have yet to occur
	- Budgets displays current, budgeted, and forecasted cost and usage data.
- AWS Cost Explorer is for *analyzing usage and cost data*
	- Focus on visualizing and analyzing report costs after incurring them.
	- Cost Explorer provides recommendations for optimizing you cloud spend, in addition to analyzing historical information