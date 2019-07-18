---
title: "Documentation Overview"
keywords: documentation
tags: [documentation]
sidebar: admin_sidebar
permalink: documentation.html
summary: Intended for system administrator audience to assist them in building the data commons infrastructure, move data, manage permissions, and implement AWS security controls
---

## Documentation Goals
The Data Commons-Alpha (DCA) proof of concept was created on Amazon Web Services cloud architecture.  A future version of DCA may be hosted in the Microsoft Azure cloud, and this documentation will be updated accordingly.  A detailed version of the AWS Virtual Private Cloud (VPC) will not be included here for security purposes, but will be released as needed (hit the Feedback link to request it).  DCA currently provides the following tools/capabilities that can be used to explore and perform analysis on data:

* [JupyterHub](https://jupyter.org/hub) - JupyterHub brings the power of notebooks to groups of users
* [pgweb](http://sosedoff.github.io/pgweb) - Cross-platform client for PostgreSQL databases
* [AWS Redshift](https://aws.amazon.com/redshift/) - AWS hosted columnar optimized data warehouse

## AWS Redshift
Redshift was used for the datastore, but a traditional relational database such as MySql, PostgreSQL, or Microsoft SQL Server would have been more appropriate considering the initial data (America Serves) put into DCA was not very large.  Redshift is optimized for a [columnar](https://docs.aws.amazon.com/redshift/latest/dg/c_columnar_storage_disk_mem_mgmnt.html) schema that can scale for very large datasets.  Primary and Foreign key constraints are recognized in redshift and used for query planning, but the constraints are not enforced.  Therefore, the purpose of the database (i.e. OLTP vs OLAP) should be considered when choosing to use Redshift.  In general, Redshift should be used for OLAP/large datasets and AWS Relational Database Services (RDS) should be used for OLTP.
