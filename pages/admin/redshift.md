---
title: "Redshift"
keywords: documentation
tags: [documentation]
sidebar: admin_sidebar
permalink: redshift.html
summary: Redshift overview and installation
---

## AWS Redshift
Redshift was used for the datastore, but a traditional relational database such as MySql, PostgreSQL, or Microsoft SQL Server would have been more appropriate considering the initial data (America Serves) put into DCA was not very large.  Redshift is optimized for a [columnar](https://docs.aws.amazon.com/redshift/latest/dg/c_columnar_storage_disk_mem_mgmnt.html) schema that can scale for very large datasets.  Primary and Foreign key constraints are recognized in redshift and used for query planning, but the constraints are not enforced.  Therefore, the purpose of the database (i.e. OLTP vs OLAP) should be considered when choosing to use Redshift.  In general, Redshift should be used for OLAP/large datasets and AWS Relational Database Services (RDS) should be used for OLTP.

## Installation
