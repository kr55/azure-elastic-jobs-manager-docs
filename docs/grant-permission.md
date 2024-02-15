---
layout: default
title: Grant permission
parent: Prerequisites
nav_order: 4
---

# Grant permission to Elastic jobs database

```sql

CREATE USER jobs_manager WITH PASSWORD = '<strong_password>';
EXEC sp_addrolemember 'jobs_resource_manager', 'jobs_manager'
```

```sql

CREATE USER reader WITH PASSWORD = '<strong_password>';
EXEC sp_addrolemember 'jobs_resource_manager', 'reader'
```

```sql

CREATE USER admin WITH PASSWORD = '<strong_password>';
EXEC sp_addrolemember 'jobs_admin', 'admin'
```

Create user assigned maanged identity (Recommended)

Before adding an user assgined managed identity to Azure elastic jobs, please create required identity if it does not exists already. 

Follwo below steps to do that.


Add user assigned maanged identity to Elastic job agent (Recommended)

Follow below steps to achive this.

