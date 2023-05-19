[[test-topics]]

- Describe the relationships among [[Region]]s, [[Availability Zone]]s, and [[Edge Locations]]
	- Regions contain many AZs
	- AZs are a single data center or a group of closely-spaced data centers
	- Edge Locations are separate from Regions. Edge Locations are located closer to users than AZs or Regions (often in major cities), so content can be served faster.
		- You can push content from a Region to an Edge Location for faster serving.
		- A subset of services which use Edge Locations:
			- [[Amazon CloudFront]] uses edge location to cache content
			- [[Amazon Route 53]] serves DNS responses from edge locations so that DNS queries which originate nearby can resolve faster.