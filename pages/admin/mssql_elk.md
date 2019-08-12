---
title: "MSSQL to ELK"
keywords: documentation
tags: [documentation]
sidebar: admin_sidebar
permalink: mssql_elk.html
summary: MSSQL data migration to the Elastic Stack (ELK)
---

## Overview
The Elastic Stack is a distributed document database that integrates with streaming and batch data shippers (i.e. Spark, Hadoop) as well as with relational databases.  Data ingested into the ELK Stack is visualized using Kibana.  Kibana allows users to iteratively discover/analyze data using user-friendly widgets and build dashboards of common visualizations (i.e. pie/bar/line charts, geo maps, etc.)  The Elastic Stack is the recommended DCA tool for users without programming/SQL experience or for stakeholders that just want to view dashboards.

## Components of the Elastic Stack
1. [Elasticsearch](https://www.elastic.co/products/elasticsearch): Elasticsearch is a distributed, RESTful search and analytics engine capable of addressing a growing number of use cases
2. [Logstash](https://www.elastic.co/products/logstash): Logstash is an open source, server-side data processing pipeline that ingests data from a multitude of sources simultaneously, transforms it, and then sends it to your favorite "stash."
3. [Kibana](https://www.elastic.co/products/kibana): Kibana lets you visualize your Elasticsearch data and navigate the Elastic Stack so you can do anything from tracking query load to understanding the way requests flow through your apps.

## Migration
