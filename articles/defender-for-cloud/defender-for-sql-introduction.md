---
title: Benefits and features of Microsoft Defender for Azure SQL
description: Learn how Microsoft Defender for Azure SQL helps you discover, track, and mitigate vulnerabilities, and alerts you to potential threats.
ms.date: 03/12/2024
ms.topic: overview
ms.custom: references_regions
ms.author: dacurwin
author: dcurwin
#customer intent: As a database administrator, I want to understand the benefits and features of Microsoft Defender for Azure SQL so that I can protect my databases effectively.
---

# Overview of Microsoft Defender for Azure SQL

Microsoft Defender for Azure SQL helps you discover and mitigate potential [database vulnerabilities](sql-azure-vulnerability-assessment-overview.md) and alerts you to [anomalous activities](#advanced-threat-protection) that might indicate a threat to your databases.

- [Vulnerability assessment](#discover-and-mitigate-vulnerabilities): Scan databases to discover, track, and remediate vulnerabilities. Learn more about [vulnerability assessment](sql-azure-vulnerability-assessment-overview.md).
- [Threat protection](#advanced-threat-protection): Receive detailed security alerts and recommended actions based on SQL Advanced Threat Protection to mitigate threats. Learn more about [SQL Advanced Threat Protection](/azure/azure-sql/database/threat-detection-overview).

When you enable Defender for Azure SQL, all supported resources within the subscription are protected. Future resources created on the same subscription will also be protected.

Defender for Azure SQL is billed as shown on the [pricing page](https://azure.microsoft.com/pricing/details/defender-for-cloud/).

Defender for Azure SQL protects read-write replicas of the following SQL versions of :
-  Azure SQL [single databases](/azure/azure-sql/database/single-database-overview) and [elastic pools](/azure/azure-sql/database/elastic-pool-overview).
- [Azure SQL Managed Instance](/azure/azure-sql/managed-instance/sql-managed-instance-paas-overview).
- [Azure Synapse Analytics (formerly SQL DW) dedicated SQL pool](/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-overview-what-is).

Defender for Azure SQL protects the following SQL versions:
- SQL Server version: 2012, 2014, 2016, 2017, 2019, 2022.
- [SQL on Azure virtual machines](/azure/azure-sql/virtual-machines/windows/sql-server-on-azure-vm-iaas-what-is-overview)
- [SQL Server on Azure Arc-enabled servers](/sql/sql-server/azure-arc/overview).

## What are the benefits of Microsoft Defender for Azure SQL?

### Discover and mitigate vulnerabilities

A vulnerability assessment service discovers, tracks, and helps you fix potential database vulnerabilities. Assessment scans provide an overview of your SQL machines' security state and details of any security findings. Defender for Azure SQL helps you identify and mitigate potential database vulnerabilities and detect anomalous activities that could indicate threats to your databases.

Learn more about [vulnerability assessment for Azure SQL Database](./sql-azure-vulnerability-assessment-overview.md).

### Advanced threat protection

An advanced threat protection service continuously monitors your SQL servers for threats like SQL injection, brute-force attacks, and privilege abuse. This service provides action-oriented security alerts in Microsoft Defender for Cloud with details of the suspicious activity, guidance on how to mitigate the threats, and options for continuing your investigations with Microsoft Sentinel. Learn more about [advanced threat protection](/azure/azure-sql/database/threat-detection-overview).

Threat intelligence-enriched security alerts are triggered when there are:

- **Potential SQL injection attacks** - including vulnerabilities detected when applications generate a faulty SQL statement in the database.
- **Anomalous database access and query patterns** - such as, an abnormally high number of failed sign-in attempts with different credentials (a brute force attempt).
- **Suspicious database activity** - such as, a legitimate user accessing an SQL Server from a breached computer that communicated with a crypto-mining C&C server.

Alerts include details of the incident that triggered them and recommendations on how to investigate and remediate threats. Learn more about the [security alerts for SQL servers](alerts-sql-database-and-azure-synapse-analytics.md).

## Next steps

In this article, you learned about Microsoft Defender for Azure SQL. Now you can:

- [Enable Microsoft Defender for Azure SQL](quickstart-enable-database-protections.md)
- [How Microsoft Defender for Azure SQL can protect SQL servers anywhere](https://www.youtube.com/watch?v=V7RdB6RSVpc).
- [Set up email notifications for security alerts](configure-email-notifications.md)
