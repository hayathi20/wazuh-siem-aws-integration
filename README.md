Wazuh Multi-Tenant Monitoring on AWS - Proof-of-Concept
Project Overview

This is a proof-of-concept project that demonstrates the deployment and configuration of Wazuh SIEM to monitor multiple AWS tenants. The project includes the setup of AWS infrastructure, the integration of Wazuh for log monitoring, and the implementation of Role-Based Access Control (RBAC) with custom dashboards. It aims to provide a cost-effective, cloud-ready SIEM solution for monitoring multi-tenant AWS environments.

Key Features

Multi-Tenant Monitoring: Set up Wazuh SIEM to monitor multiple AWS accounts using custom tenant configurations.

RBAC Integration: Configured RBAC using OpenSearch DLS to ensure proper tenant isolation and access control.

Alerting & Notification System: Integrated alert notifications using built-in SIEM features and SMTP/Relay Server setup for secure communication.

Cloud Infrastructure Setup: Provisioned Linode cloud infrastructure to deploy Wazuh components in a single-node architecture.

Project Setup Instructions
Prerequisites

To run this project, you'll need the following:

AWS Account: EC2, S3, IAM, CloudWatch services.

Linode Cloud Infrastructure: For deploying Wazuh components.

Wazuh SIEM: For log management and monitoring.

OpenSearch: For Role-Based Access Control (RBAC) configuration.

SMTP/Relay Server: For alert notifications.

Installation Guide

Provision AWS Resources:

Set up AWS EC2 instances and configure IAM policies.

Set up CloudWatch for log collection.

Provision Linode Infrastructure:

Create Linode instances to host Wazuh components.

Ensure secure SSH access and configure your firewall.

Deploy Wazuh SIEM:

Install Wazuh manager and agent on your EC2 instances.

Set up and configure the Wazuh server on Linode for log aggregation and monitoring.

Configure RBAC:

Set up OpenSearch for RBAC and create custom dashboards.

Integrate Wazuh with OpenSearch for tenant isolation and security.

Configure Alerts:

Set up an SMTP server to send email alerts.

Configure Wazuh to notify based on predefined rules.
Configuration Details
Cloud Infrastructure

AWS: Utilized EC2, S3, and IAM for secure cloud operations.

Linode: Provisioned Linode to deploy Wazuh SIEM components and manage the logs from AWS tenants.

Wazuh Setup

Single-Node Architecture: Deployed Wazuh components (manager, agents) in a single-node architecture on Linode.

Multi-Tenant Simulation: Used two distinct AWS accounts to simulate multi-tenant workloads.

Role-Based Access Control (RBAC)

OpenSearch DLS: Used OpenSearch’s DLS feature for tenant isolation.

Custom Dashboards: Configured custom dashboards per tenant for clear segregation of monitoring data.
Challenges & Solutions
1. Log Fetching Error

Problem: Encountered unsuccessful log fetching from AWS CloudWatch to Wazuh.

Solution: Adjusted IAM policies using the least privilege model and granted full access for the POC deployment.

2. RBAC Issues

Problem: RBAC rules caused failure in tenant dashboard segregation.

Solution: Implemented Wazuh RBAC using OpenSearch DLS to resolve the issues and allow full cluster permissions.

3. System Compromise

Problem: Wazuh server was uninstalled due to misconfiguration.

Solution: Cloned the existing server configuration on Linode, migrated data, and deployed the latest version of Wazuh.
Key Learnings

Cloud Deployment: Gained hands-on experience in deploying and configuring cloud environments.

Real-Time Troubleshooting: Worked on handling live systems and troubleshooting issues in real-time.

System Integration: Integrated multiple systems (AWS, Linode, Wazuh, OpenSearch) to provide comprehensive monitoring.

RBAC Management: Learned how to configure and manage Role-Based Access Control in a multi-tenant environment.

System Maintenance: Performed system upgrades, maintenance tasks, and bug fixing to ensure seamless operations.
