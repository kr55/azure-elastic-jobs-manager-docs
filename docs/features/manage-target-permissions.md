---
layout: default
title: Manage target permissions
parent: Manage target group
grand_parent: Getting started
permalink: /docs/features/manage-targetgroup/manage-target-permissions/
nav_order: 15
---
# Manage permissions on Targets
All the targets belonging to target group should have minimum required permissions to run the script under job steps. With Microsoft Entra ID support, the job agent will be able to connect to target databases (databases, servers, elastic pools) and output database(s) using the UMI.

### User assigned managed identity credentials:

In case you have added user assigned managed identity on Elastic jobs resource, you need  to grant this user assigned managed ideneity access on all target databases belonging to target group.
  <img src="../../../../media/umi-jobuser.svg" style="width:100%; height:100%">

Image source: [Microsoft learn](https://learn.microsoft.com/en-us/azure/azure-sql/database/elastic-jobs-overview?view=azuresql)

1. Login to each target Azure SQL server with Microsoft Entra ID admin account using any client tools like Azure data studio or SQL Server Management Studio 18/19. 
2. grant minimum permissions to each target database under Azure SQL Server to user assigned managed identity. 

```sql
CREATE USER [jobuserUMI] FROM EXTERNAL PROVIDER;

ALTER ROLE db_datareader ADD MEMBER [jobuserUMI];
ALTER ROLE db_datawriter ADD MEMBER [jobuserUMI];
```

### Database scoped credentials

  <img src="../../../../media/job-credentials.png" style="width:100%; height:100%">

Image source: [Microsoft learn](https://learn.microsoft.com/en-us/azure/azure-sql/database/elastic-jobs-overview?view=azuresql)
1. Login to each target Azure SQL server using any client tools like Azure data studio or SQL Server Management Studio 18/19. 
2. Create login jobuser in master database. The username should be same as that of identity of the job credentials and password should be same as job credentials password. 
```sql
--Master db
CREATE LOGIN [jobuser] WITH PASSWORD '<strong password>';
```
3. Create user jobuser for login jobuser in each target database and grant mininum permissions to the user on target database to execute job steps.
```sql
--target dbs
CREATE USER [jobuser] FROM LOGIN jobuser;
ALTER ROLE db_datareader ADD MEMBER [jobuser];
ALTER ROLE db_datawriter ADD MEMBER [jobuser];
```
