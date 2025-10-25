# wazuh-siem-aws-integration
A proof-of-concept project demonstrating the deployment and configuration of Wazuh SIEM to monitor multiple AWS tenants, with custom dashboards, alerting, and RBAC integration for secure multi-tenant log management in the cloud.
1. Repository Overview

Title: Monitoring Multiple AWS Tenants with Wazuh: A Proof-of-Concept

Description: Briefly explain the project’s purpose, which in this case, is to provision, configure, and manage a cloud-based SIEM system (Wazuh) that monitors multi-tenant AWS environments.

2. Project Setup Instructions

Prerequisites: List the tools, frameworks, and services required to run the project. For example:

AWS (EC2, S3, IAM, CloudWatch)

Linode Cloud Infrastructure

Wazuh SIEM

OpenSearch (for RBAC)

SMTP server and Relay Server setup

Installation Guide: Step-by-step instructions on setting up the environment, configuring the necessary components (Wazuh, AWS), and provisioning the cloud infrastructure on Linode.

3. Configuration Details

Cloud Infrastructure: Describe how you provisioned and configured Linode cloud infrastructure.

Tenant Simulation: Detail how you simulated multi-tenant workloads using distinct AWS accounts.

Wazuh Setup: Explain the setup of Wazuh, including RBAC configuration using DLS (for tenant separation).

4. Key Features

Multi-Tenant Monitoring: Outline how the setup provides multi-tenant monitoring and the key components used to achieve that (AWS services, Wazuh features).

Alerting and Notifications: Show how the alert system works by integrating SIEM features with a secure SMTP server.

RBAC and Custom Dashboards: Describe the RBAC setup and how you built custom dashboards for tenant environments.

5. Challenges and Solutions

Integration Challenges: Provide details on the issues faced while fetching logs from AWS CloudWatch to Wazuh, and how they were resolved (e.g., adjusting IAM policies).

Tenant Separation Issue: Explain the RBAC issues you faced and how you solved them using OpenSearch DLS features.

System Compromise: Mention the challenge with the Wazuh server and how you managed the recovery by cloning and redeploying the system.

6. Key Learnings

Deploying, configuring, and managing a cloud environment.

Simulating real workloads and handling live systems.

Integrating systems with connectors and agents.


Performing system upgrades and maintenance tasks.

Troubleshooting and fixing system bugs.
