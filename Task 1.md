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

Aws Console > Search IAM > Users > Create User > username :- aws-demo-user > Attach Policies > </br>
Amazons3FullAccess </br>
AmazonEc2FullAccess </br>
Create User.

                                                        **Task-3 :- Create s3 Bucket ?**
Aws Console > Search s3 > Buckets > Create Bucket > </br>
name :- aws-demo-bucket </br>
block public Access :- NA </br>
I Acknowledge > Create Bucket.
select Bucket > Upload a file.

**Download AWS Command Line Interface (AWSCLI)**

**go to google :-** awscliv2 download for ubuntu</br>
**install or update the latest version of awscli**> 
**Linux**

**$Sudo apt-get update**
**$sudo apt install unzip**

on chrome :- Installing or updating to the latest version of the AWS CLI,</br>
AWS CLI install and update instructions.</br>
**To install the AWS CLI, run the following commands**</br>

$ curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" </br>

copy zip file and paste in remote cli </br>

$ unzip awscliv2.zip </br>
$ cd aws </br>
$ ls  </br>
$ aws Cat install  </br>
$ sudo ./aws/install  </br>
$ aws --version  </br>

$ aws configure </br>
#Aws Console > IAM > Users > aws-demo-user > create access key > CLI > i understand > next > create Access key.</br>
(i) Access Key   (ii) Secret Access Key </br>
copy and Paste on remote cli </br>

$ aws s3 ls  </br>
check upload file in s3.



