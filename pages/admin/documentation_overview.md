---
title: "Documentation Overview"
keywords: documentation
tags: [documentation]
sidebar: admin_sidebar
permalink: documentation.html
summary: Intended for system administrator audience to assist them in building the data commons infrastructure, move data, manage permissions, and implement AWS security controls
---

## Documentation Goals
The Data Commons-Alpha (DCA) proof of concept was created on Amazon Web Services cloud architecture.  A future version of DCA may be hosted in the Microsoft Azure cloud, and this documentation will be updated accordingly.  This documentation is divided into the following categories:

* Architecture: an overview of the DCA cloud architecture will be described along with recommended free training and installation guides from AWS and other resources.
* Tools: DCA provides two primary ways to interact with loaded data.
1. [The Littlest JupyterHub](https://tljh.jupyter.org/en/latest/) provides a Jupyter notebook interface for general purpose programming in the R and Python languages.  
2. [pgweb](http://sosedoff.github.io/pgweb) - Cross-platform client for PostgreSQL databases
* Security: Security best practices such as Secure Socket Layer (SSL) encryption for data in transit, least privilege user accounts, network segmentation, among other technical security controls
* Data Load: [The AWS provided Schema Conversion Tool(SCT)](https://docs.aws.amazon.com/SchemaConversionTool/latest/userguide/CHAP_Welcome.html) provides an easy and efficient way to bulk transfer data into the cloud.  An overview of the SCT and how it is used to transfer data will be demonstrated.
