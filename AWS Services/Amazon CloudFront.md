[[CDN]] [[Edge Locations]]

## About
- A service that helps deliver data, video, applications, and APIs to customers with low latency and high transfer speeds.
- Uses [[Edge Locations]] to store cached copies of your content closer to your customers for faster delivery.

### CloudFront vs. [[AWS Global Accelerator]]
- CloudFront:
	- Improves performance for both cacheable content (images, videos, etc) and dynamic content (API acceleration, dynamic site delivery, etc)
- Global Accelerator:
	- Improves performance for a wide range of applications over TCP or UDP by proxying packets at edge locations.
	- Good fit for non-HTTP cases, such as gaming, IoT, or Voice over IP.
- Both services integrate with [[AWS Shield]] for DDoS protection.