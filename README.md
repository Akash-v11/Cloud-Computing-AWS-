Common and Shared FSx Across Two EC2 Windows Server Instances
Description
This project demonstrates how to set up a shared Amazon FSx file system between two EC2 Windows Server instances. It enables seamless file sharing and centralized storage management.

Prerequisites
Before setting up FSx, ensure you have the following:

An AWS account

Two EC2 Windows Server instances

Amazon FSx for Windows File Server

AWS CLI installed and configured

Architecture Diagram (Optional)
(You can add a diagram showing how EC2 instances connect to FSx.)

Setup Instructions
Step 1: Create Amazon FSx File System
Navigate to the AWS FSx Console

Choose FSx for Windows File Server

Configure networking, security groups, and permissions

Deploy the FSx file system and note the DNS Name

Step 2: Configure EC2 Instances
Launch two Windows Server EC2 instances

Ensure they are in the same VPC and security group

Open Remote Desktop Connection (RDP) to access the instances

Step 3: Mount FSx to EC2
Open PowerShell on each EC2 instance

Run the following command to map the shared drive:

powershell
Copy
Edit
net use X: \\<FSx-DNS-Name>\share
Verify shared storage access on both instances

Usage
Store and access shared files between EC2 instances

Ideal for applications requiring centralized storage

Security Best Practices
Restrict FSx access using security groups

Enable AWS Backup for FSx

Use IAM policies for access control

References
AWS FSx Documentation

Amazon EC2 Documentation

