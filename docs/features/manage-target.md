---
layout: default
title: Manage target
parent: Manage target group
grand_parent: Getting started
permalink: /docs/features/manage-targetgroup/manage-target/
nav_order: 14
---
# Adding targets to target group
The **Add Target** screen allows users to specify and add targets to a previously created target group. Targets represent databases where jobs will be executed. Users can choose from three target types: SqlServer, SqlElasticPool, and SqlDatabase.

## Steps to Add a New Target

1. **Navigate to the Add Target Screen**
   - Click on "Add target to target group" from the previous screen to open this interface.

      <img src="../../../../media/target-screen.png" style="width:65%; height:65%">

2. **Select Target Type**
   - Choose one of the following target types:
     - **SqlServer**: Select the server name and refresh credential name.
     - **SqlElasticPool**: Provide the server name, refresh credential name, and elastic pool name.
     - **SqlDatabase**: Specify the server name and refresh credential name.

3. **Fill in Additional Fields**
   - Depending on the selected target type, additional fields will appear:
     - For SqlElasticPool: Enter the elastic pool name.
     - For other types: No additional fields are required.

4. **Click OK to Add the New Target**
   - Confirm your choices and add the target to the target group.

## Steps to Delete a target from Target group

1. **Open the target group properties**
   - Open the target group containing the target you would like to delete.

2. **Select the target from the grid**
   - Select the target from the target grid you would like to delete and scroll the row to the right.
   - Click on Delete action button.
   - Click Yes on the confirmation screen to delete the target. 
  
     <img src="../../../../media/delete-target-screen.png" style="width:65%; height:65%">
  
   

