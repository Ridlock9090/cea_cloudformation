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

Creating an IAM AWS User and attaching them to an AWS Group. Attaching a certain role/policy to the IAM Group.

Creating a custom Policy for an S3 Bucket in reference to the IAM Role.


---
You can reach me @ ridlock@gmail.com

or add me up on LinkedIn:
www.linkedin.com/in/ken-ong9090

or on Discord:
user: ridlock6090


