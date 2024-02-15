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