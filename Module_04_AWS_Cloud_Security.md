# AWS Cloud Security

## AWS shared responsibility model
AWS is responsible for security _of_ the cloud
Customer is responsible for security _in_ the cloud

AWS responsibilities:
 - Physical security of data centers
   - Controlled, need-based access
 - Hardware and software infrastructure
   - Storage decommissioning, host operating system (OS) access logging, and auditing
 - Network infrastructure
   - Intrusion detection
 - Virtualization infrastructure
   - Instance isolation

Customer responsibilities:
 - Amazon Elastic Compute Cloud (Amazon EC2) instance operating system
   - Including patching, maintenance
 - Applications
   - Passwords, role-based access, etc.
 - Security group configuration
 - OS or host-based firewalls
   - Including intrusion detection or prevention systems
 - Network configurations
 - Account management
   - Login and permission settings for each user

## AWS Identity and Access Management (IAM)
IAM user: A person or application that can authenticate with an AWS account

IAM group: A collection of IAM users that are granted identical authorization.

IAM policy: The document that defines which resources can be accessed and the level of access to each resource.

IAM role: Useful mechanism to grant a set of permissions for making AWS service requests.

Authenticate as an IAM user to gain access
Programmatic access
 - Authenticate using:
   - Access key ID
   - Secret access key
 - Provides AWS CLI and AWS SDK access
AWS Management Console access
 - Authenticate using:
   - 12-digit Account ID or alias
   - IAM user name
   - IAM password
 - If enabled, multi-factor authentication (MFA) prompts for an authentication code.

Best practice: Follow the principle of least privilege.

Key points
 - IAM policies are constructed with JavaScript Object Notation (JSON) and define permissions.
   - IAM policies can be attached to any IAM entity
   - Entities are IAM users, IAM groups, and IAM roles.
 - An IAM user provides a way for a person, application, or service to authenticate to AWS.
 - An IAM group is a simple way to attach the same policies to multiple users.
- An IAM role can have permissions policies attached to it, and can be used to delegate temporary access to users or applications.

## Securing a new AWS account

Best practice: Do not use the AWS account root user except when necessary

Stop using the account root user as soon as possible.
 - The account root user has unrestricted access to all your resources.
 - To stop using the account root user:
   1. While you are logged in as the account root user, create an IAM user for yourself. Save the access keys if needed.
   2. Create an IAM group, give it full administrator permissions, and add the IAM user to the group.
   3. Disable and remove your account root user access keys, if they exist.
   4. Enable a password policy for users.
   5. Sign in with your new IAM user credentials.
   6. Store your account root user credentials in a secure place.

Best practices to secure an AWS
account:
 - Secure logins with multi-factor authentication (MFA).
 - Delete account root user access keys.
 - Create individual IAM users and grant permissions according to the principle of least privilege.
 - Use groups to assign permissions to IAM users.
 - Configure a strong password policy.
 - Delegate using roles instead of sharing credentials.
 - Monitor account activity by using AWS CloudTrail.

## Securing accounts
AWS Organizations enables you to consolidate multiple AWS accounts so that you centrally manage them.

Service control policies (SCPs) offer centralized control over accounts.

AWS Key Management Service (AWS KMS) enables you to create and manage encryption keys.

Amazon Cognito adds user sign-up, sign-in, and access control to your web and mobile applications.

AWS Shield is a managed distributed denial of service (DDoS) protection service.

## Securing data on AWS
AWS supports encryption of data at rest and of data in transit.

Newly created S3 buckets and objects are private and protected by default.

## Working to ensure compliance

AWS Config: Assess, audit, and evaluate the configurations of AWS resources.

AWS Artifact is a resource for compliance-related information, providing access to security and compliance reports.