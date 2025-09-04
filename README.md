# AWS_Cloud Day 1
Task 1 :- Create EC2 Instance ? </br>
Task 2 :- Create A User ? </br>
Task 3 :- Create A s3 Bucket ?

**Task-1 :- Create EC2 Instance ?**

**Step 1: Sign in to AWS Console** </br>
Go to https://aws.amazon.com/

Click "Sign In to the Console"

Enter your credentials

**Step 2: Navigate to EC2 Service**</br>
From AWS Management Console

Search - "EC2" > Click on "EC2"

**Step 3: Launch Instance**</br>
Click "Launch Instance" button

**Step 4: Configure Instance Details**

**1. Name and Tags**</br>
Enter instance name ( "AWS-Demo")

**2. Choose AMI (Amazon Machine Image)** </br>

Ubuntu Server

**3. Instance Type </br>
Select based on needs:** </br>

t2.micro (free tier eligible)

**4. Key Pair** </br>
Create new key pair </br>
Name :- aws-demo

.pem file (keep it secure!) </br>

Required for SSH access </br>

**5. Network Settings** </br>
VPC: Default

Subnet:Default

Auto-assign Public IP: Enable

Security Groups: Create new

Add rules: SSH (port 22), HTTP (80), HTTPS (443)

**6. Configure Storage** </br>
Root volume (8 GB)

**Step 5: Review and Launch** </br>
Review all configurations </br>

Click "Launch Instance"

**Step 6: Connect to Instance** </br>
Wait for instance state: "Running"

**Connect SSh to local Terminal** </br>

SSH connection example: </br>
**ssh -i your-key.pem ec2-user@public-ip** 


 Copy :- ssh -i "aws-demo.pem" ubuntu@ec2-3-90-26-52.compute-1.amazonaws.com
Log into Local Terminal:- Run Commands

$ ls -a </br>
$ chmod 400 aws-demo.pem </br>
$ ssh -i "aws-demo.pem" ubuntu@ec2-3-90-26-52.compute-1.amazonaws.com </br>

Enter </br>
Now you are connected to remote Server on Local Cli.


                                                         **Task-2 :- Create a User ?**
