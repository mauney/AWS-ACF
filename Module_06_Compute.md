# Compute

## Compute services overview
Virtual Machines
 - Amazon EC2
Serverless Computing
 - AWS Lambda
Container-based Computing
 - Amazon ECS
 - Amaxon EKS
 - AWS Fargate
 - Amazon ECR
Platform as a Service
 - AWS Elsatic Beanstalk

## Amazon EC2
Amazon Elastic Compute Cloud (Amazon EC2)
 - Provides virtual machines—referred to as EC2 instances—in the cloud.
 - Gives you full control over the guest operating system (Windows or Linux) on each instance.
You can launch instances of any size into an Availability Zone anywhere in the world.
 - Launch instances from Amazon Machine Images (AMIs).
 -Launch instances with a few clicks or a line of code, and they are ready in minutes.
You can control traffic to and from instances.

Choices made using the Launch Instance Wizard:
 1. AMI
   - Amazon Machine Image (AMI) is a template that is used to create an EC2 instance (which is a virtual machine, or VM, that runs in the AWS Cloud)
 2. Instance Type
   - The instance type that you choose determines –
     - Memory (RAM)
     - Processing power (CPU)
     - Disk space and disk type (Storage)
     - Network performance
   - Instance type categories –
     - General purpose
     - Compute optimized
     - Memory optimized
     - Storage optimized
     - Accelerated computing
 3. Network settings
   - The network bandwidth (Gbps) varies by instance type.
 4. IAM role
   - Attach an appropriate IAM Role if software on the EC2 instance needs to interact with other AWS services.
   - An AWS Identity and Access Management (IAM) role that is attached to an EC2 instance is kept in an instance profile.
 5. User data
   - Optionally specify a user data script at instance launch
   - Use user data scripts to customize the runtime environment of your instance
     - Script executes the first time the instance starts
   - Can be used strategically
     - For example, reduce the number of custom AMIs that you build and maintain
 6. Storage options
   - Configure the root volume
   - Attach additional storage volumes (optional)
   - For each volume, specify:
     - The size of the disk (in GB)
     - The volume type
     - Different types of solid state drives (SSDs) and hard disk drives (HDDs) are available
     - If the volume will be deleted when the instance is terminated
     - If encryption should be used
   - Options (root volume requires one of first two options)
     - Amazon EBS
     - Amazon EC2 Instance Store
     - Amazon EFS
     - Amazon S3
 7. Tags
 8. Security group
 9. Key pair