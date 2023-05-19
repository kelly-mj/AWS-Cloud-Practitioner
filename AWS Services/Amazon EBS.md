Amazon Elastic Block Storage

## About
- Persistent [[block-level storage]] designed for use with a single [[Amazon EC2]] server.
	- Block-level storage is when data is broken in equal-sized blocks and stored in uderlying physical storage in a manner optimized for fast access and retrieval.
- Can scale to support petabytes of data, and supports different volume types.

### Volume types
- Magnetic
	- Low-cost, meant for infrequent access data
	- IOPS: 100/s
	- Capacity: 1GB to 1TB
- HDD-backed
	- Good for large I/O sized and larger datasets
	- max throuput: 500 Mb/s
- General Purpose (gp2)
	- Default type, backed by SSD
	- Suitable for in-depth workloads with low-latency apps
	- IOPS: 160 Mb/s, max 10,000 IOPS
- Provisioned IOPS SSD (io1)
	- Lowest possible latency, backed by SSD
	- Performance: 500 Mb/s, max 32,000 IOPS

## Security
- Use [[AWS Key Management Service]] (KMS) keys for EBS encryption.
	- Will create, maintain, and protect your key-management environment
- KMS is used for creation of encrypted snapshots and volumes.
- Encrypts both data at-rest and data in-transit