---
layout: default
title: Grant permission
parent: Prerequisites
nav_order: 4
---

# Grant permission to Elastic jobs database

## Create database users on Elastic jobs database
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

## Manage Firewall Rules for Azure Elastic Jobs Manager

To enable connection to the Elastic Jobs database from the machine where you have installed Azure Elastic Jobs Manager, follow these steps to configure the firewall rule.

1. **Navigate to the Azure Portal**: Log in to the Azure Portal using your credentials.

2. **Locate Elastic Jobs Database**: Find the Elastic Jobs database in the list of Azure resources.

3. **Access Firewall Settings**: Navigate to the "Firewalls and virtual networks" section within the Elastic Jobs database settings.

4. **Add Firewall Rule**: Click on the "Add client IP" button to allow access from the machine where Azure Elastic Jobs Manager is installed. Optionally, you can specify a specific IP range if needed.

5. **Save Changes**: Save the changes made to the firewall rules.



