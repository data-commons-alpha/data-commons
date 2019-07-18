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

![blah](/data-commons/images/jhub-fluxogram.jpeg)
* image source: https://jupyterhub.readthedocs.io/en/stable/_images/jhub-fluxogram.jpeg

## Installation
Installing TLJH is extremely easy.  The overall process to install on AWS is:
1. Launch an Ubuntu Server instance in the VPC
2. Update the instance using

## TLJH Database Access
Authorized DCA users receive credentials to TLJH and to the backend database.  The recommended way to interact with the database is by using the Jupyter's built-in "magics" functions for the python-sql library.  Additionally, since Redshift was used, a PostgreSQL adapter is required to interact with Redshift/PostgreSQL databases.  The required dependencies to enable TLJH to communicate with Redshift can be installed by following the instructions [here]().
