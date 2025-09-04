# AWS_Cloud Day 1
Task 1 :- Create EC2 Instance ?
Task 2 :- Create A User ?
Task 3 :- Create A s3 Bucket ?

**Create EC2 Instance ?**

**Creating an EC2 Instance: Step-by-Step Guide**
**Step 1: Sign in to AWS Console**
Go to https://aws.amazon.com/

Click "Sign In to the Console"

Enter your credentials

**Step 2: Navigate to EC2 Service**
From AWS Management Console

Search for "EC2" in services

Click on "EC2"

**Step 3: Launch Instance**
Click "Launch Instance" button

Choose "Launch Instance" from dropdown

**Step 4: Configure Instance Details**

**1. Name and Tags**
Enter instance name ( "my-web-server")

**2. Choose AMI (Amazon Machine Image)
Select from:**

Ubuntu Server

**3. Instance Type
Select based on needs:**

t2.micro (free tier eligible)

**4. Key Pair**
Create new key pair or use existing

Download .pem file (keep it secure!)

Required for SSH access

**5. Network Settings**
VPC: Default or custom

Subnet: Choose availability zone

Auto-assign Public IP: Enable

Security Groups: Create new or use existing

Add rules: SSH (port 22), HTTP (80), HTTPS (443)

**6. Configure Storage**
Root volume (8 GB)

**Step 5: Review and Launch**
Review all configurations

Click "Launch Instance"

**Step 6: Connect to Instance**
Wait for instance state: "Running"

**Get public IP/DNS from instance details**

SSH connection example:

bash
**ssh -i your-key.pem ec2-user@public-ip**
