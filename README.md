# Lab-2-Build-a-VPC-and-launching-a-webserver

# Build Your VPC and Launch a Web Server (AWS) 

## Author

* **Name**: R.SRIBALAKUMARAN
* **Register Number**: 212225220104
* **Date of Submission**: 17-08-2026

---

## Objective

The objective of this experiment is to understand how to design and configure a basic network infrastructure in AWS using a Virtual Private Cloud (VPC). This lab focuses on creating a VPC with a public subnet, configuring an Internet Gateway and route table, launching an EC2 instance, and hosting a simple web server that can be accessed over the internet.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity

---

## Tools Used

* AWS Management Console
* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Table
* Security Groups

---

## Tasks Performed

### Task 1: Create a VPC

Create a new Virtual Private Cloud (VPC) with a private IP address range. The VPC acts as a logically isolated network in AWS where all other resources will be deployed.

Students should create a VPC with an appropriate CIDR block (for example, 10.0.0.0/16) and assign a meaningful name.

### Task 2: Create a Public Subnet

Create a subnet inside the VPC to host public resources. Enable auto-assign public IPv4 so that instances launched in this subnet receive a public IP address.

The subnet should use a smaller CIDR range (for example, 10.0.1.0/24).

### Task 3: Create and Attach Internet Gateway

Create an Internet Gateway (IGW) and attach it to the VPC. This allows communication between resources in the VPC and the internet.

### Task 4: Configure Route Table

Create a route table and add a default route (0.0.0.0/0) pointing to the Internet Gateway. Associate this route table with the public subnet.

This step ensures that traffic from the subnet can reach the internet.


### Task 5: Create Security Group

Create a security group to act as a virtual firewall for the EC2 instance. Configure inbound rules to allow:

SSH on port 22

HTTP on port 80


### Task 6: Launch EC2 Instance

Launch an EC2 instance inside the public subnet using Amazon Linux 2 AMI and a suitable instance type (t2.micro).

Attach the previously created security group and key pair.


### Task 7: Configure Web Server

Install and start a web server (Apache HTTPD) on the EC2 instance using user data or manual commands.

Create a simple HTML page and verify that it can be accessed from a web browser using the public IP address of the instance.

## Workflow (Student Explanation)


1. Set up a VPC with public and private subnets.

2. Added extra subnets in a second Availability Zone.

3. Configured the route tables, Internet Gateway, and NAT Gateway.

4. Created a security group and launched an EC2 instance as a web server.

5. Checked the deployed web server using its public DNS address.

---

## Output Screenshots (Attach 3)

### Screenshot 1: VPC and Subnet Details

<img width="1918" height="1078" alt="lab2-1" src="https://github.com/user-attachments/assets/9148ddcd-80dd-4283-86a0-0a9e5ff7306c" />

<img width="1918" height="1078" alt="lab2-1 1" src="https://github.com/user-attachments/assets/56b78fc4-3ffc-4867-97a8-ecf7176dd6c1" />


---

### Screenshot 2: EC2 Instance Running

<img width="1918" height="1078" alt="lab2-2" src="https://github.com/user-attachments/assets/28310c51-2f6e-4cb2-83e6-f9669fc0bb0f" />

<img width="1918" height="1078" alt="lab2-2 1" src="https://github.com/user-attachments/assets/90289dee-ed68-422e-9423-36187b4fd43c" />


---

### Screenshot 3: Web Server Output in Browser

<img width="1918" height="1078" alt="lab2-3" src="https://github.com/user-attachments/assets/d981bc12-6f42-488a-a68e-d7f1268d1506" />

<img width="1918" height="1078" alt="lab2-final" src="https://github.com/user-attachments/assets/a1d4ed37-6b12-402a-be1a-66933b0247ed" />


---

## Result 

This experiment successfully demonstrated the creation of a custom VPC and deployment of a public-facing web server in AWS. By configuring networking components such as subnets, route tables, and security groups, and by launching an EC2 instance with a web server, the basic architecture of a cloud-hosted application was understood.
