# AWS Network Configuration

## 1. VPC
Created a custom Virtual Private Cloud (VPC) to isolate AWS resources.

## 2. Subnets
- Public Subnet: Used for internet-facing resources.
- Private Subnet: Used for resources that should not be directly accessible from the internet.

## 3. Internet Gateway
Attached an Internet Gateway to the VPC to provide internet connectivity to resources in the public subnet.

## 4. Route Tables
Configured route tables to control network traffic.

- Public Route Table: Routes internet-bound traffic through the Internet Gateway.
- Private Route Table: Controls private subnet traffic according to the configured network design.

## 5. Security Groups
Configured inbound and outbound rules to control traffic to EC2 instances.

## 6. EC2 Web Servers
Launched Linux EC2 instances in the configured subnets and installed Apache.

## Network Flow
Internet → Internet Gateway → Public Subnet → Load Balancer → EC2 Web Servers

**Note:** Update this document to match your actual AWS configuration.