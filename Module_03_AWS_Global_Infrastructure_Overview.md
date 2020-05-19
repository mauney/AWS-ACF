# AWS Global Infrastructure Overview

## AWS Global Infrastructure
AWS Region is geographical area
Data is not automatically replicated outside of a specific regions
Each Region has two or more Availability Zones

Determine the right Region for your services, applications, and data based on:
 - Data governance and legal requirements
 - Proximity t0 customers (latency)
 - Services available within a given Region
 - Costs, which vary by region

Availability Zone - AWS recommends replicating data and resources across Availability Zones for resiliency

Each Availability Zone
 - physically separate from other Availability Zones
 - has redundant power, networking, and connectivity

Edge locations and Regional edge caches improve performance by caching content closer to users.

## AWS services and service category overview
The AWS global infrastructure can be broken down into three elements
 - Regions
 - Availability Zones
 - Points of presence (which include edge locations)