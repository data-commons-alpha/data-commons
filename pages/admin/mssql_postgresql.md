---
title: "MSSQL to PostgreSQL"
keywords: documentation
tags: [documentation]
sidebar: admin_sidebar
permalink: mssql_postgresql.html
summary: Using Pgloader to migrate data from MSSQL to PostgreSQL
---

## Overview
DCA uses PostgreSQL as its relational database. DCA users can access the database either by using JupyterHub or Pgweb.  Users that prefer to interact with the database through a programming language (Python, R) or use a dataframe data structure should JupyterHub; while users that prefer SQL queries only should use Pgweb.  

The graphic below shows the components, highlighted in green, that are involved in the data migration.  
![](/data-commons/images/mssql_postgresql_migration.png)

## Data migration steps
1. Use Openvpn client from the MSSQL server to connect to the DCA VPN gateway; MSSQL server will now be able to connect to the PostgreSQL as if they were on the same local subnet.  
2. Install pgloader for Windows using the directions outlined in this github [repository](https://github.com/dimitri/pgloader)
3. Once pgloader is installed, run the following pgloader command to migrate all tables from the SQL server to the PostgreSQL database:
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
