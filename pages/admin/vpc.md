---
title: "VPC Installation"
keywords: documentation
tags: [documentation]
sidebar: admin_sidebar
permalink: vpc.html
summary: VPC installation
---

## VPC installation
AWS documentation "User Guides" are really good and should be generally be the first resource used when trying to learn how to implement a particular AWS service.  Therefore,
we will forego recreating another guide about how to create an AWS VPC and instead direct you [here](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html). A few tidbits to assist this effort:

* Definitely recommend using Vizio or some other network diagram creation software -- such as [Lucidchart](https://www.lucidchart.com/pages/) to create a visual depiction of your VPC as you add components. This will really help you to understand the data flow of your VPC and will aid in troubleshooting. Most of the diagrams in this documentation were created using Lucidchart.  
* All of the VPC installation tasks can be completed using the AWS Console.  However, AWS also offers a command line interface, AWS CLI, that can be used as well.  [AWS CloudFormation](https://aws.amazon.com/cloudformation/) can be used to automate the provisioning of the VPC programmatically. As DCA grows, CloudFormation and other orchestration tools such as [Terraform](https://www.terraform.io) will streamline the VPC deployment.
* Network segmentation can be achieved using NACLs or Security Groups. Security Groups are AWS' implementation of a host-based firewall.  Security Group rules are stateful and instances that share a security group can communicate with each other over the explicitly stated rules for the security group. All other traffic not explicitly allowed in the security group is blocked. 
