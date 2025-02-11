---
title: Internet exposure analysis
description: Learn how Defender for Cloud detects, assesses, and mitigates internet exposure for your multicloud resources to enhance security.
author: dcurwin
ms.author: dacurwin
ms.service: defender-for-cloud
ms.topic: concept-article
ms.date: 01/14/2025
ms.custom: template-concept
#customer intent: As a user, I want to understand how Defender for Cloud detects and assesses internet exposure for my multicloud resources. This knowledge will help me identify and mitigate potential security risks effectively.
---

# Internet exposure analysis

Internet exposure analysis in Microsoft Defender for Cloud lets you understand which of your multicloud resources are exposed to the internet. Defender for Cloud uses internet exposure to determine the risk level of your misconfigurations, vulnerabilities, and other issues.

## How Defender for Cloud detects internet exposure

Defender for Cloud assesses connected cloud resources to see if they're configured for internet exposure. Detecting internet exposure can be as simple as checking if a virtual machine (VM) has a public Internet Protocol (IP) address. However, the process can be more complex. Defender for Cloud attempts to locate internet-exposed resources in complex multicloud architectures. For example, a VM might not be directly exposed to the internet but could be behind a load balancer, which distributes network traffic across multiple servers to ensure no single server becomes overwhelmed.

The following table lists the resources that Defender for Cloud assesses for internet exposure: 

| Category | Services/Resources |
|--|--|
| Virtual machines | Azure VM <br> Amazon Web Service (AWS) EC2 <br> Google Cloud Platform (GCP) compute instance |
| Virtual machine clusters | Azure Virtual Machine Scale Set <br> GCP instance groups |
| Databases (DB) | Azure SQL <br> Azure PostgreSQL <br> Azure MySQL <br> Azure SQL Managed Instance <br> Azure MariaDB <br> Azure Cosmos DB <br> Azure Synapse <br> AWS Relational Database Service (RDS) DB <br> GCP SQL admin instance |
| Storage | Azure Storage <br> AWS S3 buckets <br> GCP storage buckets |
| AI | Azure OpenAI Service <br> Azure AI Services <br> Azure Cognitive Search |
| Containers | Azure Kubernetes Service (AKS) <br> AWS EKS <br> GCP GKE |
| API | Azure API Management Operations |

The following table lists the network components that Defender for Cloud assesses for internet exposure:

| Category | Services/Resources |
|----------|--------------------|
| Azure    | Application gateway <br> Load Balancer <br> Azure Firewall <br> Network Security Groups |
| AWS      | Elastic load balancer |
| GCP      | Load balancer |

## How to view internet exposed resources

Defender for Cloud offers a few different ways to view internet-exposed resources.

- [Cloud Security Explorer](how-to-manage-cloud-security-explorer.md) - The Cloud Security Explorer lets you run graph-based queries on the Cloud Security Graph. On the Cloud Security Explorer page, you can run a query to find resources exposed to the internet. This query returns all your attached resources exposed to the internet and lets you view any associated details.

- [Attack Path Analysis](how-to-manage-attack-path.md) -  The Attack Path Analysis page lets you view attack paths that an attacker could take to reach a specific resource. With Attack Path Analysis, you can view a visual representation of the attack path and see which resources are exposed to the internet. Internet exposure often serves as an entry point for attack paths, especially when the resource has vulnerabilities. Internet-exposed resources often lead to targets with sensitive data.

- [Recommendations](review-security-recommendations.md) - Defender for Cloud prioritizes recommendations based on their exposure to the internet.

## Defender External Attack Surface Management integration

Defender for Cloud also integrates with Defender External Attack Surface Management to assess resources for internet exposure by attempting to contact them from an external source and seeing if they respond.

Learn more about the [Defender External Attack Surface Management integration](concept-easm.md).

## Related content

- [Investigating risk with security explorer/attack paths](concept-attack-path.md)
- [Identify and remediate attack paths](how-to-manage-attack-path.md)
- [Remediate recommendations](implement-security-recommendations.md)
