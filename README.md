1. Project Title
Common and Shared FSx Across Two EC2 Windows Server Instances

2. Description
This project demonstrates setting up a shared Amazon FSx file system between two EC2 Windows Server instances. It enables seamless file sharing and centralized storage management.

3. Prerequisites
AWS account

Two EC2 Windows Server instances

Amazon FSx for Windows File Server

AWS CLI installed and configured

4. Architecture Diagram (Optional)
You can include a diagram showing how EC2 instances connect to FSx.

5. Setup Instructions
Step 1: Create Amazon FSx File System
Navigate to AWS FSx Console

Choose FSx for Windows File Server

Configure networking, security groups, and permissions

Deploy and note the DNS Name

Step 2: Configure EC2 Instances
Launch two Windows Server EC2 instances

Ensure they are in the same VPC and security group

Open Remote Desktop Connection (RDP) to access the instances

Step 3: Mount FSx to EC2
Open PowerShell on each EC2 instance

Run the following command to map the drive:

powershell
Copy
Edit
net use X: \\<FSx-DNS-Name>\share
Verify shared storage access

6. Usage
Store and access shared files between EC2 instances

Ideal for applications requiring centralized storage

7. Security Best Practices
Restrict FSx access using security groups

Enable AWS Backup for FSx

Use IAM policies for access control

8. References
AWS FSx Documentation

Amazon EC2 Documentation
