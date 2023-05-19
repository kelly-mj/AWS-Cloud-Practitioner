- AWS:
	- Operates, manages, and controls the components from the host OS and virtualization layer.
	- Physical security of the facilities in which the service operates.
- The customer assumes:
	- Resonsibility and management of the guest OS (including updates and security patches)
	- Other associated application software
	- Configuration of the AWS provided security group firewall

## Controls
- Shared controls
	- Patch Management controls
		- AWS patches the underlying platform
		- Customer patches guest OS/software
	- Configuration management
		- AWS is responsible for the infrastrcture devices
		- The cusomter is responsible for supporting their own OSs and software.
	- Awareness and Training
		- AWS: Responsible for awareness and training of AWS resources
		- Customer: Responsible for learning and training their own people
- Customer-specific controls
	- Network traffic
	- Data identity and integrity
	- Client and server-side data
	- Encryption
	- Authentication
	- Creation, installation, and development of application which reside on an [[Amazon EC2]] instance