
## About
- MySQL and PostreSQL compatible database engine for [[Amazon RDS]] that was built for the cloud.
- Consists of an Aurora database cluster housing multiple volumes, created across multiple [[Availability Zone]]s.
- Consists of 2 types of database instances:
	- The main database for direct reads and writes
	- The read replica (also called the Aurora replica)
- An Aurora DB can have up to 15 read replicas