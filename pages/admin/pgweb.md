---
title: "PostgreSQL/Pgweb"
keywords: documentation
tags: [documentation]
sidebar: admin_sidebar
permalink: postgresql_pgweb.html
summary: Pgweb overview and installation
---

## Overview
Pgweb is a cross-platform, web-interface for PostgreSQL databases. Pgweb provides another way to interact with the database by using Structured Query Language (SQL), and doesn't require DCA users to set up a programming environment; only a web-browser is needed.  The example below demonstrates a SQL query to find the distribution of service requests.

Pgweb was built using docker containers; the logical flow of the Pgweb architecture is outlined below:

![](/data-commons/images/pgweb_arch.png)

## Components
The Pgweb/PostgreSQL architecture consists of the following components:
1. [Adminer](https://www.adminer.org): Opensource PHP database management tool
2. [Pgweb](http://sosedoff.github.io/pgweb/): Cross-platform, web-interface for PostgreSQL databases
3. [PostgreSQL](https://www.postgresql.org): Open source object-relational database system
4. [Pgloader](https://pgloader.io): Open source data migration tool

## Docker
Docker is a lightweight virtualization, software as a service, platform that companies use to package and distribute microservices. The components listed above are microservices for a PostgreSQL database and associated management and data transfer capabilities.  Installing Docker on AWS can be achieved by first launching an EC2 Amazon Machine Image (AMI), and then following the directions [here](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/docker-basics.html) to install docker.  After docker is installed, clone this [github]() repository to the working directory of the AMI, and then run the following command from a bash terminal:
```bash
docker-compose up
```

At this point, Adminer, Pgweb, and PostgreSQL containers have been created.  The following image shows the login prompt for Adminer and the management interface.  The management interface shows not tables because PostgreSQL doesn't have data yet.

![](/data-commons/images/adminer_login.png)
![](/data-commons/images/adminer_mgt.png)

Pgloader will be used to migrate data hosted on the on-prem SQL server to the PostgreSQL in the AWS private subnet. The following pgloader command will migrate all the tables from the SQL server to the PostgreSQL database:
```bash
pgloader sql.load
```
* the contents of the sql.load file is explained in the pgloader [documentation](https://pgloader.readthedocs.io/en/latest/ref/mssql.html)
```
# sql.load
load database
    from mssql://azure_ds:<password@localhost/SERVES2
    into postgres://postgres:<password>@localhost:5432/serves
;
```

The Pgloader terminal output lists any errors that occurred during the data transfer and the results of the transfer

![](/data-commons/images/pgloader_output.png)

## Pgweb
The relational data from the MS SQL server is now in the PostgreSQL server and can queried using pgweb.  

![](/data-commons/images/pgweb_query.png)
