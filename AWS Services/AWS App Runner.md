
## About
- Service that enables you to build and run containerized web application without any prior container or infrastructure experience.
- Auto-scales your compute resources as you receive requests
	- You specify how many concurrent requests you want a particular instance of your application container to recieve. App Runner auto-distributes incoming requests to containers while staying at or below the target concurrency.

## How it works
- To use App Runner:
	- You supply a containerized application that listens on a port
	- App Runner gives you back a URL
	- You can send traffic to that URL and get a response back from your application.
	- App Runner manages the number of containers powering the application, and the amount of concurrent traffic each container receives.

## App Runner vs [[AWS Fargate]]
- Fargate leaves concurrency and scaling up to you, while App Runner manages those things for you.