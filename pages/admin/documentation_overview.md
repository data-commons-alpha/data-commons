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
* Tools: DCA provides three ways to interact with loaded data.
1. [The Littlest JupyterHub](https://tljh.jupyter.org/en/latest/) provides a Jupyter notebook interface for general purpose programming in the R and Python languages.  
2. [pgweb](http://sosedoff.github.io/pgweb) - Cross-platform client for PostgreSQL databases
3. [Elastic Stack](https://www.elastic.co/products/elastic-stack) - That's Elasticsearch, Kibana, Beats, and Logstash (also known as the ELK Stack). Reliably and securely take data from any source, in any format, then search, analyze, and visualize it in real time.
* Extract, Transform, Load (ETL): CSV file output from the SAS ETL pipeline is conformed to a normalized data model, enriched with geolocation data, and programmatically loaded into a relational and document databases.
* Security: Security best practices such as Secure Socket Layer (SSL) encryption for data in transit, least privilege user accounts, network segmentation, among other technical security controls.
* Cost Analysis: Summary and itemized prices are provided for the AWS Virtual Private Cloud (VPC) infrastructure and DCA analysis tools.
