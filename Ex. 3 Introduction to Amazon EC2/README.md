# Lab 3 – Introduction to Amazon Elastic Compute Cloud (EC2)

## Author

* **Name**: PRIYA DHARSHINI R
* **Register Number**: 212224050033
* **Date of Submission**: 13.05.2026

---

## Objective

The objective of this experiment is to understand the fundamentals of Amazon Elastic Compute Cloud (EC2). This lab focuses on launching and managing a virtual server, understanding instance types and AMIs, connecting to an EC2 instance, monitoring its status, and performing basic instance operations such as start, stop, and terminate.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity
* Basic knowledge of Linux commands (optional)

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Key Pair
* Security Group
* SSH Client (PuTTY / Terminal)

---

## Tasks Performed

### Task 1: Explore Amazon EC2 Dashboard

Explore the EC2 service dashboard in the AWS Management Console. Observe the different sections such as Instances, AMIs, Instance Types, Key Pairs, Security Groups, and Elastic IPs.

---

### Task 2: Launch an EC2 Instance

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type (t2.micro) under the free tier. Configure basic settings such as instance name, key pair, and security group.

---

### Task 3: Configure Security Group

Configure a security group to allow inbound access:

* SSH (Port 22) from your IP address
* HTTP (Port 80) from anywhere (0.0.0.0/0)

This security group acts as a firewall for the instance.

---

### Task 4: Connect to EC2 Instance

Connect to the running EC2 instance using SSH. Use the downloaded key pair and connect via terminal or PuTTY.

For Amazon Linux:

```
ssh -i "keyname.pem" ec2-user@<Public-IP>
```

---

### Task 5: Perform Basic Instance Operations

Perform the following operations from the EC2 console:

* Stop the instance
* Start the instance
* Reboot the instance

Observe the state changes of the instance.

---

### Task 6: Monitor EC2 Instance

Monitor the EC2 instance using the Monitoring tab. Observe metrics such as CPU utilization, network in/out, and instance status checks.

---

### Task 7: Terminate EC2 Instance

Terminate the EC2 instance after completing the experiment to avoid unnecessary AWS charges.

---

## Workflow (Student Explanation)

(Write the steps you followed in your own words)

1. Launched an Amazon EC2 instance named **Web Server** with termination protection and stop protection enabled.

2. Configured and monitored the EC2 instance using status checks, system logs, and monitoring tools to verify proper working of the web server.

3. Updated the security group by allowing HTTP traffic on port 80 and successfully accessed the web page displaying **“Hello From Your Web Server!”**

4. Resized the EC2 instance from **t2.micro** to **t2.small** and increased the EBS storage volume from **8 GiB to 10 GiB** for better performance and storage capacity.

5. Explored EC2 service quotas and tested stop protection by enabling and disabling it before successfully stopping the instance.


## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Dashboard / Instance List

<img width="1901" height="813" alt="Screenshot 2026-05-13 173203" src="https://github.com/user-attachments/assets/856ac9e4-1461-4eb7-a74e-fc39f9d93264" />

### Screenshot 2: SSH Connection to Instance

<img width="1919" height="823" alt="Screenshot 2026-05-13 173604" src="https://github.com/user-attachments/assets/fc626e1a-4f47-41ef-b58e-84499daed3c7" />
<img width="1914" height="580" alt="Screenshot 2026-05-13 174238" src="https://github.com/user-attachments/assets/a74a4939-24d4-4976-b092-e98fb70bd949" />

### Screenshot 3: Instance Monitoring / Status

<img width="1906" height="811" alt="Screenshot 2026-05-13 180906" src="https://github.com/user-attachments/assets/c5fbc6de-875e-4c4e-bce3-a850c86c07e5" />


## Result 

This experiment provided hands-on experience with Amazon EC2 by demonstrating how to launch, connect, manage, and monitor a virtual server in AWS. It helped in understanding the concept of Infrastructure as a Service (IaaS) and how compute resources can be provisioned and controlled on demand in the cloud.
