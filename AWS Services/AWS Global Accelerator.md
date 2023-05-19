

## About
- AWS networking service that routes your traffic through the AWS global network, increasing the overall speed through optimizations by AWS.

### AWS Global Accelerator vs. [[Amazon CloudFront]]
- CloudFront:
	- Improves performance for both cacheable content (images, videos, etc) and dynamic content (API acceleration, dynamic site delivery, etc)
- Global Accelerator:
	- Improves performance for a wide range of applications over TCP or UDP by proxying packets at [[edge locations]].
	- Good fit for non-HTTP cases, such as gaming, IoT, or Voice over IP.
- Both services integrate with [[AWS Shield]] for DDoS protection.