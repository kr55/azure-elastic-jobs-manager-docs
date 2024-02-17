---
layout: default
title: Grant permission
parent: Prerequisites
nav_order: 4
---

# Grant permission to Elastic jobs database
This section outlines the process of granting permissions within the Azure Elastic Jobs Database by creating users and assigning them specific roles. These roles dictate the level of access and the actions users can perform within the database environment.

### Creating Jobs manager User:

```sql
CREATE USER jobsmanager WITH PASSWORD = '<strong_password>';
EXEC sp_addrolemember 'jobs_resource_manager', 'jobsmanager';
```
Creates a user 'jobsmanager' with a strong password and assigns the 'jobs_resource_manager' role to enable management of resources in the Elastic Jobs Database.

### Creating Jobs Reader User

```sql
CREATE USER jobsreader WITH PASSWORD = '<strong_password>';
EXEC sp_addrolemember 'jobs_reader', 'jobsreader'
```
Creates a user 'jobsreader' with a strong password and grants access by assigning the 'jobs_reader' role. This role is specifically designed to provide read access to Elastic Jobs objects, making it useful for tasks like job monitoring.

### Creating Jobs Admin User

```sql
CREATE USER jobsadmin WITH PASSWORD = '<strong_password>';
EXEC sp_addrolemember 'jobs_admin', 'jobsadmin'
```
Creates a user 'jobsadmin' with a strong password and assigns the 'jobs_admin' role for administrative privileges in the Elastic Jobs Database.

# Add user assigned maanged identity to Elastic job agent (Recommended)
This section advises on the recommended practice of adding a user-assigned managed identity to the Azure Elastic Job Agent. By doing so, you enhance security and streamline authentication processes within your Elastic Jobs environment.

## Create user assigned maanged identity resource in Azure
This step describes how to create user-assigned managed identity within the Azure portal. If such an identity already exists, skip this step. However, if the identity is not present, proceed with creating it. Once created, this managed identity can be associated with the Elastic Job Agent, facilitating secure authentication with other Azure resources.



