# Lab 6 – Scale and Load Balance Your Architecture

## Title

Scale and Load Balance Your Architecture
Author : your name PRIYA DHARSHINI R
Reg no : 212224050033
yours   Date : 31.05.2026

---

## Objective

The objective of this lab is to understand how to design a scalable and highly available architecture on AWS using Auto Scaling and Elastic Load Balancing. This experiment focuses on distributing incoming traffic across multiple EC2 instances, automatically scaling resources based on demand, and validating fault tolerance.

---

## Prerequisites

* Basic knowledge of Amazon EC2 and VPC
* Completion of previous labs (IAM, EC2, EBS, Database Server)
* AWS Academy Lab access
* Stable internet connection

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Elastic Load Balancer (ELB / ALB)
* Auto Scaling Groups (ASG)
* Amazon CloudWatch

---

## Tasks Performed

### Task 1: Review Existing Architecture

Students review the existing EC2-based application architecture created in previous experiments.

### Task 2: Create a Launch Template

Students create a launch template that defines the EC2 instance configuration including AMI, instance type, security group, and user data.

### Task 3: Create an Auto Scaling Group

Students create an Auto Scaling Group using the launch template and configure minimum, maximum, and desired instance capacity.

### Task 4: Configure an Application Load Balancer

Students create an Application Load Balancer and configure target groups for routing traffic to EC2 instances.

### Task 5: Register Auto Scaling Group with Load Balancer

Students attach the Auto Scaling Group to the target group of the load balancer.

### Task 6: Configure Scaling Policies

Students configure scaling policies based on CPU utilization using Amazon CloudWatch alarms.

### Task 7: Test Load Balancing and Scaling

Students test the setup by generating traffic and observing automatic scaling and load distribution.

---

## Workflow (To be filled by Student)

Describe step-by-step how you performed this experiment in your own words.

---1. Created an AMI named **WebServerAMI** from the existing **Web Server 1** instance in Amazon EC2.

2. Created a Target Group (**LabGroup**) and an Application Load Balancer (**LabELB**) to distribute traffic across multiple EC2 instances.

3. Created a Launch Template (**LabConfig**) and configured an Auto Scaling Group with minimum 2 and maximum 6 instances.

4. Verified load balancing by accessing the application through the Load Balancer DNS and confirmed that target instances were healthy.

5. Tested Auto Scaling using a load test, observed CloudWatch alarms triggering, additional EC2 instances launching automatically, and finally terminated **Web Server 1**.


## Output Screenshots 

<img width="1826" height="749" alt="Screenshot 2026-05-15 090855" src="https://github.com/user-attachments/assets/3170c289-cd30-47a3-9dbb-62f53094c469" />


<img width="1899" height="818" alt="Screenshot 2026-05-31 231342" src="https://github.com/user-attachments/assets/eea25029-456a-4a43-b82f-dec29dd52fa8" />

<img width="1901" height="805" alt="Screenshot 2026-05-31 225505" src="https://github.com/user-attachments/assets/114aef6b-b605-498c-8247-a45c13162c29" />

## Result

This experiment demonstrated how to build a scalable and fault-tolerant cloud architecture using Auto Scaling Groups and Elastic Load Balancing. The system automatically adjusted resources based on workload and ensured continuous service availability by distributing traffic across multiple instances.
