---
layout: default
title: Enable Managed identity
parent: Prerequisites
nav_order: 3
---

# Enable User Assigned Managed Identity for Elastic Job Agent (Recommended)
Optional
{: .label .label-blue }

This section guides the recommended practice of integrating a user-assigned managed identity with the Azure Elastic Job Agent. This approach enhances security and streamlines authentication processes within your Elastic Jobs environment. 

## Create User Assigned Managed Identity Resource in Azure

This step outlines the process of creating a user-assigned managed identity within the Azure portal. If such an identity already exists, skip this step. However, if the identity is not present, proceed with creating it. Once established, this managed identity can be associated with the Elastic Job Agent, facilitating secure authentication with other Azure resources.

1. Navigate to the Azure portal and create a User Assigned Managed Identity resource [here](https://portal.azure.com/#create/Microsoft.ManagedIdentity).
2. Provide a name for the UMI, review the options, and click 'Review + create'.

      <img src="../media/prerequisites/create-umi-in-azure.png" style="width:100%; height:100%">

## Add User Assigned Managed Identity to Elastic Job Agent

1. Access the Elastic Job Agent resource in the Azure portal. Navigate to the 'Identity' option under the security section.
2. Click the 'Add User Assigned Managed Identity' button.
3. Select the desired UMI from the options and click 'Add'.
4. Save your changes.

      <img src="../media/prerequisites/add-umi-to-elastic-agent.png" style="width:100%; height:100%">

{: .note } 
Only one UMI can be added to an Elastic Job Agent.
