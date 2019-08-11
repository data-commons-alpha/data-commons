---
title: "Architecture Overview"
keywords: documentation
tags: [documentation]
sidebar: admin_sidebar
permalink: arch_overview.html
summary: High-Level overview of DCA architecture deployed in AWS
---

## Virtual Private Cloud (VPC)
A detailed version of the AWS Virtual Private Cloud (VPC) will not be included here for security purposes, but will be released as needed (hit the Feedback link to request it).  
![vpc](/data-commons/images/vpc_arch.png)

* The VPC consists of a public, private and VPN subnets.  Communication between the subnets are controlled by security group/host-based firewall rules applied at the instance level.  For example, only certain ipv4 addresses and ports from the public subnet are allowed to communicate to the private subnet

* DCA uses the following AWS VPC components and services:
1. [Internet Gateway](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Internet_Gateway.html): Connects the VPC to the Internet and to other AWS products.
2. [NAT Gateway](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html): Enables instances in the private subnet to connect to the internet or other AWS services, but prevent the internet from initiating a connection with those instances.
3. [Client VPN](https://docs.aws.amazon.com/vpn/latest/clientvpn-admin/what-is.html): AWS Client VPN is a managed client-based VPN service that enables you to securely access your AWS resources and resources in your on-premises network.  
4. [PostgreSQL](https://www.postgresql.org): Open source object-relational database system
5. [Redshift](https://docs.aws.amazon.com/redshift/index.html): Amazon Redshift is a fast, fully managed, petabyte-scale data warehouse service that makes it simple and cost-effective to efficiently analyze all your data using your existing business intelligence tools.
6. [S3](https://docs.aws.amazon.com/AmazonS3/latest/dev/Welcome.html): Amazon Simple Storage Service is storage for the Internet. It is designed to make web-scale computing easier for developers.
7. [Route 53](https://aws.amazon.com/route53/): Amazon Route 53 is a highly available and scalable cloud Domain Name System (DNS) web service.
