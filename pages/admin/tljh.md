---
title: "The Littlest JupyterHub"
keywords: documentation
tags: [documentation]
sidebar: admin_sidebar
permalink: tljh.html
summary: Overview and installation of TLJH
---

## The Littlest JupyterHub (TLJH)
DCA uses the opensource distribution, TLJH, as one of the analytic front-ends for researchers.  TLJH is the little brother of [JupyterHub](https://jupyterhub.readthedocs.io/en/stable/).  TLJH supports 0-100 users while JupyterHub can be scaled to many more.  As the DCA scales to support more than 100 users, future development efforts for the Data Commons should strongly consider using JupyterHub installed on [Kubernetes](http://z2jh.jupyter.org/en/latest/#).

![](/data-commons/images/jhub-fluxogram.jpeg)
* image source: https://jupyterhub.readthedocs.io/en/stable/_images/jhub-fluxogram.jpeg

## Installation
Installing TLJH is extremely easy.  The overall process to install on AWS is:
1. Launch an Ubuntu Server instance in the VPC
2. Follow the instructions [here](https://tljh.jupyter.org/en/latest/install/custom-server.html) to install TLJH

## Managing Users
The administrator account created during the installation steps can create user accounts by logging in to TLJH at "http://IP_OF_TLJH:80".  
* CAUTION: TLJH, by default, is installed without SSL enabled.  It is highly recommended to install SSL to encrypt all traffic (i.e. usernames and passowrds) going to/form to TLJH is well documented [here](https://tljh.jupyter.org/en/latest/howto/admin/https.html).

Users will request access to TLJH by browsing to "http://IP_OF_TLJH/hub/signup" and entering in their chosen username and password. Users will not have access until an administrator approves their account.  Administrators approve accounts at "http://IP_OF_TLJH/hub/authorize"; an example is depicted below.

![](/data-commons/images/tljh_signup.png)

![](/data-commons/images/tljh_authorize.png)

## TLJH Database Access
Authorized DCA users receive credentials to TLJH and to the backend database.  The recommended way to interact with the database is by using the Jupyter's built-in "magics" functions for the python-sql library.  Additionally, since Redshift was used, a PostgreSQL adapter is required to interact with Redshift/PostgreSQL databases.  The required dependencies to enable TLJH to communicate with Redshift can be installed by following the instructions [here](https://blog.rjmetrics.com/2016/02/08/setting-up-your-analytics-stack-with-jupyter-notebook-aws-redshift/); the dependencies only need to be installed once by an administrator will apply to all users.
