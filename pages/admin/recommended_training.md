---
title: "Recommended Training/Reading"
keywords: documentation
tags: [documentation]
sidebar: admin_sidebar
permalink: training.html
summary: Recommended training and resources to learn AWS and the tools that DCA uses
---

## Amazon Web Services (AWS)
* AWS offers lots of free training to help you understand the various services and tools that they offer.  To create the [DCA architecture](), it would be beneficial to first complete the free [AWS Cloud Practitioner Essentials (Second Edition)](https://aws.amazon.com/training/course-descriptions/cloud-practitioner-essentials/) course.  To sign up the course, click on "Find a class near you" and sign up for an [AWS training](https://www.aws.training).  This is a short (6 hours) introductory course to AWS and is beneficial to both system administrators and non-technical users who want to know more about AWS.
* DCA uses the following AWS VPC components and services:
1. [Internet Gateway](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Internet_Gateway.html): Connects the VPC to the Internet and to other AWS products.
2. [NAT Gateway](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html): Enables instances in the private subnet to connect to the internet or other AWS services, but prevent the internet from initiating a connection with those instances.
3. [Client VPN](https://docs.aws.amazon.com/vpn/latest/clientvpn-admin/what-is.html): AWS Client VPN is a managed client-based VPN service that enables you to securely access your AWS resources and resources in your on-premises network.  
4. [Redshift](https://docs.aws.amazon.com/redshift/index.html): Amazon Redshift is a fast, fully managed, petabyte-scale data warehouse service that makes it simple and cost-effective to efficiently analyze all your data using your existing business intelligence tools.
5. [S3](https://docs.aws.amazon.com/AmazonS3/latest/dev/Welcome.html): Amazon Simple Storage Service is storage for the Internet. It is designed to make web-scale computing easier for developers.
