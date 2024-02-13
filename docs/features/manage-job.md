---
layout: default
title: Manage job
parent: Documentation
has_children: true
nav_order: 9
---

# Manage a job
{: .no_toc }
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Create or alter the job

Follow these steps to create a new job using the **Azure Elastic Job Agent** interface:

<img src="../../media/job-general-screen.png"  style="width:60%; height:60%">

1. **Navigation**
   - On the top panel, select `New Job` to open the job creation window.
   - Double-click on an existing job to edit the job.
   - Right-click on an existing job and click on `Properties` to edit the job.

2. **General Information**
   - **Name:** Enter the name of your job in the `Name` field.
   - **Description:** Provide description of your job in the `Description` field.

3. **Job Execution Details**
   - **Last Run Outcome:** This field will display the outcome of the last run once the job has been executed.
   - **Last Executed:** Indicates when this particular job was last executed.
     
4. **Script & Help Options**
   - Click on `Script` if you want to script the changes made in the job. This is a SQL script that will be executed against the agent job database when users saves job changes.
   - Click on `Help` for assistance and documentation related to this interface.

5. **Save or Cancel**
   - Click `OK` to save and create or alter the job.
   - Click `Cancel` to discard the changes.

{: .note }
Ensure all required fields are filled out before clicking "OK" to avoid errors and ensure smooth creation of your new Azure elastic jobs.

---

## Start job
 **Steps to start an elastic job**
   - On the left panel of the landing screen, right click on the job under 'Jobs' tree view.
   - From the menu items, click 'Start job' button.

## Stop job
 **Steps to stop an elastic job**
   - On the left panel of the landing screen, right click on the job under 'Jobs' tree view.
   - From the menu items, click 'Stop job' button.

## Enable/Disable job
 **Steps to enable/disable an elastic job**
   - On the left panel of the landing screen, right click on the job under 'Jobs' tree view.
   - From the menu items, click 'Enable'/'Disable' button. 

Note: Enable or Disable button in the menu list will apoear deoending on the current activation status of the job.

## View history
The **Job History Viewer** screen provides detailed information about the execution history of specific jobs. Users can access this screen by clicking on the "View History" menu item of a job.

### Features and Information Displayed:
{: .no_toc }
1. **Job List:**
   - Displays a list of jobs with their names, creation times, start times, end times, lifecycle statuses, and messages.
   - Users can select a job to view its specific steps and details.

2. **Step Details:**
   - Upon selecting a job, users are presented with the steps associated with that job.
   - Information includes step name, start time, end time, lifecycle status, target type, and target server name.

3. **Execution Message:**
   - At the bottom of the screen is a message displaying the success or failure status of the step execution along with additional details.

### Navigation:
{: .no_toc }
Users can navigate through different jobs and their steps to monitor and analyze their execution histories.

For further assistance, click on the ‘Help’ icon at the top-right corner of the dialog box.

