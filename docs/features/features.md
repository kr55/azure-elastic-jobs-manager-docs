---
layout: default
title: Documentation
nav_order: 3
has_children: true
permalink: /docs/features
---

# Azure Elastic Jobs Manager

Azure Elastic Jobs Manager enables seamless management of elastic jobs in Azure directly from your desktop. This tool serves as an extension to Visual Studio versions 2017, 2019, and 2022, as well as SQL Server Management Studio versions 18 and 19, streamlining the process of overseeing your elastic job deployments.
{: .fs-6 .fw-300 }

# Connecting to Azure SQL Database with Elastic Jobs Configured

## Overview
The **Login Screen** allows users to connect to an Azure SQL database where elastic jobs are configured. Users need to provide login details with minimum permissions. The authentication method used is SQL Server Authentication.

## Connection Details

1. **Server Name**
   - Enter the server name of your Azure SQL database in the 'Server name' field.

2. **Authentication**
   - Select 'SQL Server Authentication' from the dropdown menu.
   - Enter your username in the 'User name' field.
   - Enter your password in the 'Password' field.
   - Optionally, check the 'Remember password' box if you want the application to remember your login credentials.

3. **Additional Properties**
    - Click on ‘Options’.
    - Under ‘Connection Properties’, ensure that:
        - ‘Encrypt connection’ is checked if you want to encrypt data sent between your application and SQL Database over the network.
        - ‘Trust server certificate’ is checked if you trust your server’s SSL certificate and want to bypass verification.

4. **Connection Timeout**
    - Set an appropriate timeout period (in seconds) during which a connection attempt will be made before it’s terminated.

5. **Job Database**
    – Select a job database from dropdown or leave it as default if not required.

6. Click on ‘Connect’.

### Note
Ensure that permissions are set up appropriately, adhering to the principle of least privilege, granting only necessary permissions needed for elastic jobs operations.


## Overview
Upon logging in to the Elastic Job Agent, users are presented with the landing screen of Azure Elastic Jobs Manager. This interface serves as the central hub for managing and monitoring various jobs and target groups.

## Interface Elements

### Top Menu Bar
- **New Job**: Allows users to create a new job.
- **New Credentials**: Enables users to add new credentials.
- **New Target Group**: Users can create a new target group.
- **Refresh**: Refreshes the current view.

### Jobs Section
Lists all existing jobs with their names and statuses:
   - DataStore-update index of boarding pe...
   - test j
   - DataStore-Maintenance-full

### Target Groups Section
Displays all target groups:
   - DatabaseGroup1

### Job Credentials Type 
Indicates the type of job credentials being used, e.g., Database-scoped credentials.

### Top 5 Running Jobs 
Displays information about the top 5 running jobs including:
   - Job Name 
   - Time Elapsed 

### Job Status Indicators 
Shows job statuses in various colors indicating:
    - Succeeded (Green)
    - In Progress (Yellow)
    - Failed (Red)
    - Timed Out (Pink)
    - Other (Blue)

Each status is also accompanied by a count of jobs in that particular state within the last 24 hours.

## Navigation Buttons 
At the bottom, there are navigation buttons including Back, Settings, Cancel, and Help for additional options and navigation.

Feel free to explore and manage your jobs efficiently using this interface! 🚀

