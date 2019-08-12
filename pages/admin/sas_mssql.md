---
title: "SAS to Microsoft SQL Server (MSSQL)"
keywords: documentation
tags: [documentation]
sidebar: admin_sidebar
permalink: sas_mssql.html
summary: Migrate SAS ETL output to MSSQL
---

## Data model
![data model](/data-commons/images/erd.png)

## Overview
The Serves data is extracted and transformed in an external SAS ETL pipeline that results in a CSV file such as "SE_FINAL_20190630.csv".  This file is conformed to the data model and then loaded into a MS SQL database using PowerShell scripts.

## PowerShell Script
The Powershell script automates the creation of the MS SQL database, its tables, and data load. The script can be downloaded from this [repository](https://github.com/asoa/IVMF). The source file (i.e. SE_FINAL_20190630.csv) and the script should be placed in the same directory on the MSSQL server.  The scripts should be run in the following order through a PowerShell ISE:
1. table_load.ps1 [option 2]
![](/data-commons/images/pshell_drop.png)
2. table_load.ps1 [option 3]
![](/data-commons/images/pshell_create.png)
3. lookup_load.ps1
![](/data-commons/images/pshell_lookup_load.png)
4. table_load.ps1 [option 1]
![](/data-commons/images/pshell_load.png)
