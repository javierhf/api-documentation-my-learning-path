# API Deployment  

## Overview  

**The software is delivered to the production environment, and it is made available to end-users**. Technical Writers assist in creating *deployment guides* and *documenting configuration settings, upgrade paths, and rollback procedures*.  

## Associated Documents: Deployment Guide

Deployment Guide are the documents associated to this stage:   

> Instructions on how to install, configure, and deploy the software to the production environment.  
  
## Example  

**An example of a deployment guide** could be a Cloud Deployment Manual for installing the application on AWS, covering steps for server setup, load balancing, and environment configuration.  

**Check the following fictional sample** of a deployment guide of a Web Application on AWS:    

### Web Application Deployment on AWS - Deployment Guide

#### System Information    

> Version: 1.0    
> Target Environment: AWS EC2, S3, RDS       
> Date: October 22, 2024
 
#### Prerequisites  

- [x] AWS account with necessary permissions.
- [x] AWS CLI installed and configured.
- [x] SSH key for EC2 instance access.  

#### Deployment Steps  

##### Step 1 - Set Up EC2 Instance  

1. Log in to AWS Management Console.  
2. Navigate to EC2 Dashboard.  
3. Launch a new instance:    
> * Choose Amazon Linux 2 as the AMI.  
> * Select t2.micro as the instance type.  
> * Configure network settings (assign to the default VPC).  
> * Add storage (minimum 8GB).  
4. Review and launch the instance.  

##### Step 2 - Install Application Dependencies  

1. SSH into the EC2 instance:
   ```
   ssh -i "your-key.pem" ec2-user@your-ec2-public-ip
   ```
2. Update the instance and install necessary packages:
```
   sudo yum update -y
   sudo yum install httpd php php-mysql -y     
```  

##### Step 3 - Deploy the Web Application  

1. Copy your web application files to the EC2 instance:
   ```
   scp -i "your-key.pem" /local/path/to/app/* ec2-user@your-ec2-public-ip:/var/www/html/     
   ```
2. Start the Apache server:  

   ```
   sudo systemctl start httpd
   sudo systemctl enable httpd   ```
   
##### Step 4 - Database Configuration (RDS)  

1. Set up an RDS instance (MySQL):  
> * Choose the RDS service in the AWS Console.  
> * Launch a new MySQL instance, configure security groups, and note down the connection endpoint.  

2. Connect your application to the RDS database by updating the application’s configuration file with the database connection string.  
  
##### Step 5 - Test and Verify Deployment  

1. Open a browser and navigate to your EC2 instance's public IP.  
2. Ensure the application loads and connects to the database correctly.

