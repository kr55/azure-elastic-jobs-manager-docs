---
layout: default
title: Installation
nav_order: 5
---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

# Installation and activation
{: .no_toc }

## How to install

### Using Azure Elastic Jobs Manager Installer.exe
1. Double-click the installer file `Azure Elastic Jobs Manager Installer.exe` and follow the steps to complete the installation of SSIS Catalog Migration Wizard.

### Manual Mode

**Visual Studio 2017/2019**
1. Double-click on the file `Azure.Elastic.Jobs.Manager.Plugin.20172019.vsix` from the unzipped downloaded folder. It will launch the VSIX Installer.
2. Choose your target Visual Studio and click on Install.
3. Once the installation is done, restart Visual Studio.
4. Click on the Tools menu item. You will see the Azure Elastic Jobs Manager option. Click it to launch.

**Visual Studio 2022**
1. Double-click on the file `Azure.Elastic.Jobs.Manager.Plugin.2022.vsix` from the unzipped downloaded folder. It will launch the VSIX Installer.
2. Choose your target Visual Studio and click on Install.
3. Once the installation is done, restart Visual Studio.
4. Click on the Tools menu item. You will see the Azure Elastic Jobs Manager option. Click it to launch.

**SQL Server Management Studio 18**
1. Extract the file `Azure.Elastic.Jobs.Manager.Plugin.20172019.vsix` content in a folder named `Azure Elastic Jobs Manager` using 7zip.
2. Copy this folder to the location `"C:\Program Files (x86)\Microsoft SQL Server Management Studio 18\Common7\IDE\Extensions"`. You would need admin permissions to do this.
3. Restart SSMS 18.
4. You will now see the "Azure Elastic Jobs Manager" option under the Tools menu item. Click it to Launch.

**SQL Server Management Studio 19**
1. Extract the file `Azure.Elastic.Jobs.Manager.Plugin.20172019.vsix` content in a folder named `Azure Elastic Jobs Manager` using 7zip.
2. Copy this folder to the location `"C:\Program Files (x86)\Microsoft SQL Server Management Studio 19\Common7\IDE\Extensions"`. You would need admin permissions to do this.
3. Restart SSMS 19.
4. You will now see the "Azure Elastic Jobs Manager" option under the Tools menu item. Click it to Launch.

**Standalone installation**
1. Extract the file `Azure.Elastic.Jobs.Manager.Plugin.20172019.vsix` content in a folder named `Azure Elastic Jobs Manager` using 7zip.
2. Place this folder to your preferred location and double-click the `"Azure.Elastic.Jobs.Manager.exe"` file, to launch the application.

## How to activate license key

You would receive the license key via email. You can also find the license key at my-accounts.
1. Launch `Azure Elastic Jobs Manager Installer.exe`.
2. Enter the product key on the landing page screen and click on the 'Activate Product' button. It should activate the product on the machine.

## How to uninstall 

**SQL Server Management Studio 18**
1. Close all instances of SSMS 18.
2. Navigate to the location `"C:\Program Files (x86)\Microsoft SQL Server Management Studio 18\Common7\IDE\Extensions"`. And delete `"Azure Elastic Jobs Manager"` folder. You would need admin permissions to do this.
3. Start SSMS 18. You should not see Azure Elastic Jobs Manager button under the tools menu item anymore.

**SQL Server Management Studio 19** 
1. Close all instances of SSMS 19.
2. Navigate to the location `"C:\Program Files (x86)\Microsoft SQL Server Management Studio 19\Common7\IDE\Extensions"`. And delete `"Azure Elastic Jobs Manager"` folder. You would need admin permissions to do this.
3. Start SSMS 19. You should not see Azure Elastic Jobs Manager button under the tools menu item anymore.

**Visual Studio 2017/2019/2022**
1. Navigate to the Tools menu item and click on Extensions and updates.
2. Locate SSIS Catalog Migration Wizard from installed plugins and click on Uninstall.
3. You would need to restart Visual Studio for changes to take effect.
