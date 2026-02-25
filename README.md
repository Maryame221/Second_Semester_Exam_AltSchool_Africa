# Second_Semester_Exam_AltSchool_Africa
Hands-on AWS project: deployed an Ubuntu Apache web server on EC2 via SSH and hosted a public object using Amazon S3. Includes configuration steps, networking setup, and security group configuration.

AWS EC2 Web Server & S3 Object Hosting Project
Overview
This project demonstrates the deployment of a basic web server in the AWS cloud and the use of object storage for public file access.
As part of my AltSchool Africa Cloud Engineering second semester practical exam, I provisioned an Ubuntu instance on AWS EC2, configured secure remote access, installed and configured Apache, and served a custom HTML page. I also created an Amazon S3 bucket and made an uploaded object publicly accessible through a direct URL.
The goal of this project was to gain hands-on experience with infrastructure provisioning, Linux server administration, and cloud storage permissions.

Architecture:
AWS EC2 (Ubuntu 22.04 LTS)
SSH remote access
Apache2 Web Server
Security Groups (Firewall rules)
Amazon S3 (Object Storage)
EC2 Setup

1. Instance Configuration
Instance type: t2.micro (Free Tier)
Operating System: Ubuntu Server 22.04
Key Pair authentication (.pem)
Security Group rules:
SSH (Port 22) – My IP
HTTP (Port 80) – Anywhere

2. Connect to the Server
chmod 400 mykey.pem
ssh -i mykey.pem ubuntu@<my_public-ip>

3. Install Apache
sudo apt update
sudo apt install apache2 -y

5. Configure Web Page
Custom HTML page displayed my name and confirmed the server was running.

5. Access the Web Server
The web page was accessed using:

http://<my_public-ip>

S3 Setup
1. Bucket Creation
Created a unique S3 bucket
Disabled block public access (required for the assignment)

2. Upload Object
Uploaded an HTML file/image into the bucket.

3. Public Access Configuration
Configured public read permission on the object to allow access via the Object URL.

Challenges Faced
Understanding AWS security defaults
Differentiating bucket permissions vs object permissions
Public access initially blocked by S3
Ensuring security group rules allowed HTTP traffic

What I Learned
Basic cloud infrastructure provisioning
Linux server management via SSH
Web server configuration using Apache
Cloud storage and access control in S3
Importance of secure default configurations in AWS
Project Documentation

Full walkthrough and explanation available here: https://medium.com/@maryame68/secure-web-application-project-deployment-on-aws-using-a-bastion-host-ansible-and-an-alb-3a4992553a8c

Author
Maryame Diom
Cloud & Cybersecurity Enthusiast
