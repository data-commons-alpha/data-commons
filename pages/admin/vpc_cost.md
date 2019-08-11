---
title: "VPC Cost"
keywords: documentation
tags: [documentation]
sidebar: admin_sidebar
permalink: vpc_cost.html
summary: AWS cost for VPC Infrastructure
---

## VPC Overview

## Price Influencers
* Intra-[availability zone](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html) traffic is free. Therefore all DCA services are built using the same availability zone (i.e. us-east-2a).  
* An [Elastic IP](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/elastic-ip-addresses-eip.html) is needed for the NAT gateway. The NAT gateway is required to provide out-going internet access to instances in the private subnet (i.e updates).
* The VPN gateway allows administrators to connect to instances in the private subnet and for on-premise resources (i.e. SQL Server) to connect to private subnet instances (i.e. SQL Server data migration to PostgreSQL). The VPN gateway costs for every hour of operation. Costs could be reduced significantly by scripting the provision/decommission of using the AWS CLI.

## Compute and Storage Summary
* DCA has three core services: The Littlest JupyterHub (TLJH), Pgweb, and the Elastic Stack.  Combined, they have 56 computing cores, 176 GB of RAM, and more than 1.5 terabytes of secondary storage
* DCA has an additional terabyte of S3 storage

## Compute/Storage by EC2 Instance

| Instance | CPU Cores | RAM | Storage
| --- | --- | --- |
| JupyterHub | 32 | 128 | 1 TB |
| PostgreSQL | 4 | 16 | 20 GB |
| Pgweb | 8 | 16 | 25 GB |
| Elastic Stack | 16 | 32 | 500 GB |

## Cost Highlights

| VPC Service | Service Price/Month |
| --- | --- |
| PostgreSQL database | $212.28 |
| NAT Gateway | $33.17 |
| VPN Gateway | $17.2 |
| Developer Support Plan | $29.00 |

| EC2 |  Price/Year |
| --- | --- |
| JupyterHub | $7158.00
| Pgweb | $1051.00
| Elastic Stack | $2102.00

## Itemized Cost Breakdown (Paid up-front)
* Assumes services will run 24/7
* Prices for EC2 instances assume service costs for the year are paid up front, resulting in approximately 50% savings when compared to the on-demand, hourly costs.

|  Service Type | Components | Region | Component Price | Service Price |
| --- | --- | --- | --- | --- |
|  Amazon EC2 Service (US East (Ohio)) |  |  |  | $10544.24 |
|   | Compute: | US East (Ohio) | $0 |  |
|   | EBS Volumes: | US East (Ohio) | $152.5 |  |
|   | EBS IOPS: | US East (Ohio) | $0 |  |
|   | EBS Snapshots: | US East (Ohio) | $77.02 |  |
|   | Reserved Instances (One-time Fee): | US East (Ohio) | $10311 |  |
|   | Elastic IPs: | US East (Ohio) | $3.72 |  |
|  Amazon S3 Service (US East (Ohio)) |  |  |  | $23.56 |
|   | S3 Standard Storage: | US East (Ohio) | $23.56 |  |
|  Amazon Route 53 Service |  |  |  | $0.9 |
|   | Hosted Zones: | Global | $0.5 |  |
|   | Standard Queries: | Global | $0.4 |  |
|  Amazon RDS Service (US East (Ohio)) |  |  |  | $224.08 |
|   | DB instances: | US East (Ohio) | $212.28 |  |
|   | Storage: | US East (Ohio) | $2.3 |  |
|   | Backups: | US East (Ohio) | $9.5 |  |
|  Amazon VPC Service (US East (Ohio)) |  |  |  | $50.37 |
|   | VPN Connection: | US East (Ohio) | $17.2 |  |
|   | NAT Gateway | US East (Ohio) | $33.17 |  |
|  AWS Data Transfer In |  |  |  | $0 |
|   | US East (Ohio) Region: | Global | $0 |  |
|  AWS Data Transfer Out |  |  |  | $0.54 |
|   | US East (Ohio) Region: | Global | $0.54 |  |
|  AWS Support (Developer) |  |  |  | $325.14 |
|   | Support for all AWS services: |  | $29 |  |
|   | Support for Reserved Instances (One-time Fee): |  | $296.14 |  |
|   |  | Free Tier Discount: |  | $-6.01 |
|   |  | Total One-Time Payment: |  | $10607.14 |
|   |  | Total Monthly Payment: |  | $555.68 |
