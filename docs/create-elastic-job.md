---
layout: default
title: Create Elastic Jobs agent
parent: Prerequisites
nav_order: 3
---

# Create Elastic Job agent resource in Azure

# Creating Azure Elastic Jobs

Follow the steps below to create elastic jobs in Azure:

1. Open the [Azure portal](https://portal.azure.com/) and search for [Azure Elastic Jobs](https://portal.azure.com/#create/Microsoft.SQLElasticJobAgentg):
   - Define a unique Elastic Job agent name.
   - Select the Subscription and Resource group.

2. Configure the Elastic Job agent:
   - Choose the Azure SQL Database server and Job database.
   - Select the Service tier for the Job database (S1 or above).
   - Optional settings:
     - Configure Managed identity and Tags.
     - Enable Geo-redundancy for regional failover (optional, increases cost).
     - Choose the Storage redundancy level (LRS, GRS, GZRS).

3. Create a new job database:
   - Define the Job database name.
   - Choose the Compute + storage tier (default: Standard - S1).
   - Optional settings:
     - Configure database for further customization (service tier, backup, threat protection).

4. Review and create:
   - Review the summary of your chosen configurations.
   - Click Review + create to provision the Elastic Job Agent.
   - Optionally use Previous to edit earlier settings.

Additional Notes:
- This is a preview feature, so agree to preview terms before creating.
- Refer to [Microsoft documentation](https://learn.microsoft.com/en-us/azure/azure-sql/database/job-automation-overview) for more details.
