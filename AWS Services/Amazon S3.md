Amazon Simple Storage Service

## About
- Service which provides ==storage for objects up to 5TB== in size, with no limits on the total storage.
- Amazon uses [[server side encryption]] to encrypt the data at rest in an S3 bucket.
	- AES-256 encryption with Amazon S3-managed keys (SSE-S3)
	- This is considered transparent to the user within an S3 environnment (as opposed to client-side encryption, which is not transparent because the end user is responsible for encrypting each object within S3)
- Each object has a specific URL
- It can hold ==an unlimited amount of data==

### Features
- Prevent delete actions
	- Through versioning (you have multiple version of the same object stored witin the same bucket in S3)
	- MFA - confirm delete actions before the actual deletion take place

### Naming Restrictions/Requirements
- Bucket names must contain:
	- 3-63 characteres
	- Strt with a lowercase letter or a number
- Bucket names may **not** contain:
	- Underscores
	- Upper-case letters
	- IP addresses
- You may not change a bucke name once created
- Bucket names must be unique across the entire AWS infrastructure

### Storage classes
*All storage classes are required to replicate data in a minimum of 3 [[Availability Zone]]s, except for S3 One-Zone IA*
- Standard - General purpose
	- Low latency, high throughput, 99.9999...% durability
- Inteliigent-Tiering - Unknown or changing access
	- Reduces your storage costs by automatically moving data (at an object level) to the most cost-effective access tier based on access frequency
	- Uses the tiers:
		- Frequent, Infrequent, and Archive Instant
- Standard-IA (Infrequent Access)
	- For data that is accessed less frequently, but required rapid access when needed.
	- Low latency, high throughput, 99.9999...% durability, and a lower $/GB
- One-Zone IA
	- For data that is accessed less frequently, and stores data in a single [[Availability Zone]]
- S3 Glacier
	- 3 tiers:
		- Instant (access in seconds)
		- Flexible (access in minutes)
		- Deep Archive (access within 12 hours)

## Data Lake
- A cnetralized repository that allows you to store all your structured and unstructured data at any scale.
- House large amounts of data from a number of different resources in one central location
- Utilize a broad perspective of data science, data analytics, and ML
- Create unique catalogs and utilize tools to anaylize, monitor, and foocus on unique data patterns