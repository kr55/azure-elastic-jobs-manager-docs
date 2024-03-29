---
layout: default
title: Add job steps
parent: Create a job
grand_parent: Getting started
permalink: /docs/features/create-job/add-step/
nav_order: 10
---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Managing job steps

This section describes how to create/modify steps within a job.

   <img src="../../../../media/job-steps-screen.png" style="width:80%; height:80%">

   - Navigate to `Job Properties` for the specific job you want to edit.
   - Click on `Steps` in the navigation pane on the left side.

## Manage Step General Properties

The **Step Properties** screen allows users to manage individual job steps within a job. When a user clicks on a specific step from the steps page of a job, this screen opens. Here are the details of the elements and options available on this screen:

   <img src="../../../../media/step-general-screen.png" style="width:80%; height:80%">

1. **Step Name**: Users can view or edit the name of the selected step here.
2. **Credentials**: A dropdown menu allows users to select or add new credentials to execute this step.
3. **Target Group**: Users can assign or change target groups using this dropdown menu.
4. **Command Field**: Allows users to input or edit commands associated with this job step.


## Managing Step Retry Settings

The **Advanced** page of the step properties allows users to configure retry settings for optimizing the performance and reliability of their job steps. Below are the options available:

   <img src="../../../../media/step-advanced-screen.png" style="width:80%; height:80%">

1. **Step Timeout**
- **Description**: The maximum amount of time allocated for a step to complete.
- **Default Value**: 43200 seconds (12 hours).

2. **Max Parallelism**
- **Description**: The maximum number of parallel executions allowed for a step. A value of 0 means null, indicating no limit on parallel executions.
- **Default Value**: 0 (null).

3. **Retry Attempts**
- **Description**: The number of times the system will attempt to retry executing a step in case of failure.
- **Default Value**: 2 attempts.

4. **Initial Retry Interval**
- **Description**: The initial time interval before the first retry attempt is made after a failure.
- **Default Value**: 1 second.

5. **Maximum Retry Interval**
- **Description**: The maximum time interval between retry attempts. Each subsequent retry (after the initial) will double the interval time until this maximum value is reached.
- **Default Value**: 120 seconds.

6. **Retry Interval Backoff Multiplier** 
- **Description**: This multiplier increases the interval between retries exponentially to reach up to the Maximum Retry Interval.
- **Default Value**: 2

{: .note } 
These are default values except for Max Parallelism which has a default value of 0 meaning null (unlimited parallel executions allowed).

## Configuring Job Step Output to Database Table

The **Output** page in the Step Properties dialog box allows users to enable and configure the output of a job step to a database table. This feature is particularly useful for logging and monitoring job execution.

   <img src="../../../../media/step-output-screen.png" style="width:80%; height:80%">

1. Check the `Enable output` checkbox.
2. Enter or select the server name where your database is hosted.
3. In case user-assigned managed identity is not enabled, choose from existing credentials or create a new one by clicking on `New`.
4. Input the name of the output database.
5  Enter the table schema name and table name where job step outputs will be stored.

{: .note } 
Ensure that you have the necessary permissions to write data into the specified database table.
Verify server connectivity before enabling job step output.
