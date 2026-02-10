# 🌩️ AWS Practical Implementation Tasks

## 📌 Overview

This repository contains hands-on AWS cloud implementation tasks
covering compute, storage, networking, security, automation, monitoring,
and high availability architecture. These tasks demonstrate practical
knowledge of cloud infrastructure and DevOps fundamentals using Amazon
Web Services (AWS).

------------------------------------------------------------------------

## ⚠️ AWS Free Tier Notice

All tasks were implemented using **AWS Free Tier eligible resources**.\
Infrastructure was created only for testing and learning purposes and
terminated after validation to avoid billing.\
Screenshots and documentation are included as proof of implementation.

------------------------------------------------------------------------

# 🚀 Task Implementations

------------------------------------------------------------------------

## ✅ TASK 1 -- AWS Services Overview

**Date:** 30-07-2025

### Objective

Identify AWS services and understand their functionality with real-world
examples.

### AWS Service Categories

#### 🔹 Compute Services

-   **Amazon EC2** -- Virtual servers for running applications\
    *Example:* Hosting web applications\
-   **AWS Lambda** -- Serverless computing\
    *Example:* Running backend code without managing servers

#### 🔹 Storage Services

-   **Amazon S3** -- Object storage for files and static websites\
    *Example:* Hosting static websites\
-   **Amazon EBS** -- Block storage for EC2\
    *Example:* Persistent storage for operating systems\
-   **Amazon Glacier** -- Archival storage\
    *Example:* Long-term backup storage

#### 🔹 Database Services

-   **Amazon RDS** -- Managed relational database\
    *Example:* MySQL database for web applications\
-   **Amazon DynamoDB** -- NoSQL database\
    *Example:* Real-time mobile app data storage

#### 🔹 Networking Services

-   **Amazon VPC** -- Virtual private network\
-   **Route 53** -- DNS management

#### 🔹 Security Services

-   **IAM** -- Access and permission management\
-   **AWS WAF & Shield** -- Application security

#### 🔹 Monitoring Services

-   **Amazon CloudWatch** -- Resource monitoring\
-   **AWS CloudTrail** -- Activity logging

------------------------------------------------------------------------

## ✅ TASK 2 -- EC2 Instance Families & Pricing Models

**Date:** 31-07-2025

### Objective

Understand EC2 instance types and pricing models.

### Instance Families

  Family                  Purpose
  ----------------------- --------------------------------------
  General Purpose         Balanced compute, memory, networking
  Compute Optimized       High CPU workloads
  Memory Optimized        Large database workloads
  Storage Optimized       High disk throughput
  Accelerated Computing   GPU workloads and ML

### Pricing Models

-   **On-Demand** -- Pay per usage
-   **Reserved Instances** -- Long-term discounted pricing
-   **Spot Instances** -- Low-cost unused capacity
-   **Savings Plans** -- Flexible pricing discounts

------------------------------------------------------------------------

## ✅ TASK 3 -- File Transfer Using SCP

**Date:** 02-08-2025

### Objective

Transfer files securely between servers.

### Implementation

-   Local to EC2 transfer\
-   EC2 to EC2 transfer

### Sample Commands

``` bash
scp file.txt ec2-user@public-ip:/home/ec2-user
scp ec2-user@server1:/file ec2-user@server2:/destination
```

------------------------------------------------------------------------

## ✅ TASK 4 -- EC2 Monitoring Using CloudWatch

### Objective

Launch EC2 instance and monitor system performance.

### Monitoring Metrics

-   CPU Utilization\
-   Storage Metrics\
-   Network Usage

### Tools Used

-   CloudWatch Dashboard\
-   Performance Monitoring Alerts

------------------------------------------------------------------------

## ✅ TASK 5 -- S3 Pricing Models & Static Website Hosting

**Date:** 04-08-2025

### Objective

Understand S3 pricing and deploy a static website.

### S3 Pricing Models

-   Standard Storage\
-   Intelligent Tiering\
-   Glacier Storage\
-   Deep Archive

### Implementation Steps

1.  Created S3 bucket\
2.  Enabled static website hosting\
3.  Uploaded website files\
4.  Configured public access

------------------------------------------------------------------------

## ✅ TASK 6 -- AWS CLI S3 Operations

**Date:** 04-08-2025

### Objective

Manage S3 using AWS CLI commands.

### Commands Used

``` bash
aws s3 mb s3://bucket-name
aws s3 sync local-folder s3://bucket-name
aws s3 sync s3://bucket-name local-folder
aws s3 rm s3://bucket-name --recursive
aws s3 rb s3://bucket-name
```

------------------------------------------------------------------------

## ✅ TASK 7 -- VPC & Web Server Deployment

### Objective

Create custom network infrastructure and deploy web application.

### Implementation Steps

1.  Created VPC with CIDR `10.0.0.0/16`
2.  Created Public Subnet `10.0.1.0/24`
3.  Launched EC2 instance inside subnet
4.  Selected Amazon Linux AMI
5.  Installed Apache Web Server
6.  Deployed Hello World web application
7.  Configured production-ready server setup

------------------------------------------------------------------------

## ✅ TASK 8 -- Auto Scaling & Load Balancing

### Objective

Ensure high availability during peak traffic hours (8 PM -- 8 AM).

### Implementation

-   Configured Auto Scaling Group\
-   Created scaling policies based on load\
-   Implemented Application Load Balancer\
-   Attached Auto Scaling Group to Load Balancer

### Outcome

-   Automatic server scaling\
-   Balanced traffic distribution\
-   Improved application reliability

------------------------------------------------------------------------

## ✅ TASK 9 -- IAM User & Group Management

### Objective

Implement role-based access control using IAM.

### Users Created

  User        Permissions
  ----------- ---------------------------
  Prod User   EC2 Full Access
  Dev User    S3 Read Only
  Test User   EC2 & S3 Full Access
  UAT User    EC2, S3, Lambda Read Only

### Groups Created

-   Prod Group\
-   Dev Group\
-   Test Group\
-   UAT Group

### Implementation

Users were assigned to appropriate groups based on access requirements.
