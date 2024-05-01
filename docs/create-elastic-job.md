---
layout: default
title: Create Elastic Jobs agent
parent: Prerequisites
nav_order: 3
---

# Create Elastic Job agent resource in Azure

{% include youtubePlayer.html id="slSKtdSeg-k" %}

Follow the steps below to create elastic jobs in Azure:
### Select Azure Elastic Jobs resource in Azure portal:
   - Open the [Azure portal](https://portal.azure.com/) and search for [Azure Elastic Jobs](https://portal.azure.com/#create/Microsoft.SQLElasticJobAgentg):
   - Define a unique Elastic Job agent name.
   - Select the Subscription and Resource group.

      <img src="../media/prerequisites/open-azure-portal.png" style="width:100%; height:100%">

### Configure the Elastic Job agent:
   - Choose the Azure SQL Database server and Job database.
   - Select the Service tier for the Job database (S1 or above).
   - Optional settings:
     - Configure Managed identity and Tags.
     - Enable Geo-redundancy for regional failover (optional, increases cost).
     - Choose the Storage redundancy level (LRS, GRS, GZRS).

      <img src="../media/prerequisites/create-azure-sql-server.png" style="width:100%; height:100%">

### Create a new job database:
   - Define the Job database name.
   - Choose the Compute + storage tier (default: Standard - S1).
   - Optional settings:
     - Configure database for further customization (service tier, backup, threat protection).

      <img src="../media/prerequisites/create-azure-sql-database.png" style="width:100%; height:100%">

### Review and create:
   - Review the summary of your chosen configurations.
   - Click Review + create to provision the Elastic Job Agent.
   - Optionally use Previous to edit earlier settings.

      <img src="../media/prerequisites/review-and-create-elastic-jobs.png" style="width:100%; height:100%">


