# cea-cloudformation
**Site for my own CloudFormation Templates.**

**This Repository includes the following:**

**1. asg.yaml**
- CloudFormation Template for VPC with AutoScalingGroup

Summary:

Forms an AWS VPC with High Availability of minimum 2 AZs attached to an AutoScalingGroup with Desired Capactiy of 2 Instances for High Availability and Resiliency. Comprises of 1 Public Subnet and 2 Private Subnets in each AZ for a total of 6 subnet groups. 

An Attached Internet Gateway to communicate publicly with a Security Group that allows HTTP Access. 

AutoScalingGroup with CloudWatch Alarm trigger when CPU Utilization is greater than 70%, horizontally scales the instance up to a maximum of 3.  

---

**2. ec2.yaml**
- CloudFormation Template for VPC with LoadBalancing

Summary:

Forms an AWS VPC with High Availability of minimum 2 AZs attached to a LoadBalancer attached to a Listener for HTTP traffic with a Target of 2 WebServer Instances for Load Balancing of traffic. Template comprises of 1 Public Subnet and 2 Private Subnets in each AZ for a total of 6 subnet groups.

An Attached Internet Gateway to communicate publicly with a Security Group that allows HTTP Access. 

Two (2) Web Server Instances with the basic yum and systemctl installed to verify if the LoadBalancer is working as it should. 

---

**3. iam.yaml**
- CloudFormation Template for IAM services

Summary:

Creating an IAM AWS User and attaching them to an AWS Group. Attaching a certain role and policy to the IAM Group.

Creating a custom Policy for an S3 Bucket in reference to the IAM Role.

This setup is typical for granting EC2 instances permissions to interact with S3 while maintaining good security practices through the use of roles and policies.

---

**4. index.html**
- Simple .HTML index file

Summary:

Title: The page is titled "My S3 Hosted Website."
Heading: Displays a main heading: "My S3 Hosted Website."
Paragraph: Contains a brief description stating - "This is a static website on S3."
The structure includes a header and basic HTML elements.

---

**5. rds.yaml**
- This AWS CloudFormation template creates an infrastructure setup for a database-driven application, including a VPC with public and private subnets across two availability zones (AZs).
  
Summary:

The template defines a VPC (MyVPC) with public and private subnets to host various resources. It includes an Internet Gateway for external access, a Bastion host for secure SSH access, and multiple EC2 instances for application deployment, each with associated security groups to manage inbound traffic. A subnet group for an RDS MySQL database instance is also created, along with the database itself, ensuring it operates within the private subnets. Overall, this configuration establishes a secure and organized environment for deploying a web application with a backend database.

---

**6. rds2.yaml**
- This AWS CloudFormation template creates a MySQL RDS (Relational Database Service) instance.
  
Summary:
The template defines a single RDS database instance (rdsDBInstance) with a storage allocation of 20 GB and a class type of db.t3.micro. It specifies a backup retention period of 7 days, ensuring data recovery options are available. The instance is identified as MyNewRDSInstance, and it is configured with a master username (admin) and password (password). This setup provides a simple yet functional MySQL database ready for use in applications.

---

**7. s3-bucket.yaml**
- This AWS CloudFormation template creates an Amazon S3 bucket.

Summary:
The template defines a single S3 bucket resource (`S3Bucket`) with the name `ridlock-s3-bucket-yaml`. This setup allows for the storage and management of objects in the cloud, providing a scalable and durable solution for data storage. The configuration is straightforward, focusing on establishing a specific S3 bucket for various storage needs.

---

**8. s3-staticsite.yaml**
- This AWS CloudFormation template sets up an S3 bucket for static website hosting.

Summary:
The template defines an S3 bucket (`MyS3Bucket`) named `ridlock-s3-static-site`, configured for website hosting with `index.html` as the index document. It allows public access by setting `RestrictPublicBuckets` to false. Additionally, a bucket policy (`BucketPolicy`) is created to permit public read access (`s3:GetObject`) to all objects within the bucket, enabling users to access the hosted website content. This configuration effectively establishes a public static website on S3.

---
**9. vpc-dif-key.yaml**
- This AWS CloudFormation template establishes a Virtual Private Cloud (VPC) infrastructure with multiple subnets and security configurations.

Summary:
The template creates a VPC (`MyVPC`) with a CIDR block of `172.16.0.0/16`, enabling DNS support and hostnames. It defines several subnets, including two public subnets and four private subnets across two availability zones. An Internet Gateway is attached for external access, and a public route table directs traffic accordingly. A bastion host EC2 instance is set up in one of the public subnets for secure SSH access, while other EC2 instances are created in the private subnets for application deployment. Security groups are configured to manage access between the instances, allowing SSH and ICMP traffic as needed. This comprehensive setup enables secure and organized networking for applications hosted within the VPC.

---

**10. vpc.yaml**
- This AWS CloudFormation template sets up a complete Virtual Private Cloud (VPC) environment with associated subnets, instances, and security configurations.

Summary:
The template creates a VPC (`MyVPC`) with a CIDR block of `172.16.0.0/16`, enabling DNS support and hostnames. It defines multiple subnets, including two public subnets and four private subnets across two availability zones, allowing for organized resource allocation. An Internet Gateway is attached to provide external access, along with a public route table to route traffic. A bastion host EC2 instance is deployed in one of the public subnets for secure SSH access, while application instances are created in the private subnets. Security groups are established to control traffic, enabling SSH access from the bastion host and ICMP access between instances, thus ensuring secure communication within the network. This configuration supports a robust and scalable cloud architecture.

---
You can reach me @ ridlock@gmail.com

or add me up on LinkedIn:
www.linkedin.com/in/ken-ong9090

or on Discord:
user: ridlock6090


