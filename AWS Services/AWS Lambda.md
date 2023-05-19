[[Serverless computing]]

## About
- You upload code, and it automagically executes in the cloud!
- Lambda functions are run in a managed environment which is automatically scalable, highly available, and all the maintenance is handled by AWS.
- **Lambda is designed to run code under 15 minutes**.

## Cost structure
- You pay for the compute time that you consume. Charges only apply while your code is running.

## Use Cases
- AWS Lambda is suited for:
	- Quick processing like a web backend
	- Handling requests
	- Backend report processing service, where each invocation takes less than 15 mintues to complete.
- AWS Lambda is not suited for:
	- Deep learning

## How it works
- You upload code into what's called a Lambda function
- Then you configure a trigger
- When the trigger is detected, the code is automatically run in a managed environment which is automatically scalable, highly available, and all the maintenance is handled by AWS.