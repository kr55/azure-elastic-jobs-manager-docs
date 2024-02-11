---
layout: default
title: Manage credentials
parent: Documentation
nav_order: 8
---

# Managing credentials

## Overview
The **New Credential** screen is launched when a user clicks on "Create Credentials". This interface is used for creating credentials for elastic jobs. Note that these credentials are only relevant when elastic jobs do not have user assigned managed identity enabled.

## Fields and Options

### User Name
- A text field where users enter the username associated with the credential.

### Password
- A text field for entering the password. It's masked for security purposes.

### Identity 
- A dropdown menu to select the identity, providing options based on the available identities.

### Create Master Key 
- An option available to create a master key if required.

### Create Button 
- Clicking this will attempt to create the credential with the provided information.

### Cancel Button 
- Discards any entered information and closes the credential creation window.

## Usage
Users should fill out all necessary fields, ensuring that correct information is provided before clicking on "Create". If there’s an error or if users wish to discard their input, they can click "Cancel".

### Important Note
Credentials are essential for accessing and managing elastic jobs effectively but are not required when user assigned managed identity is enabled.
