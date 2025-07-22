---
layout: default
title: Installation
nav_order: 5
---
# Installation and activation
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Order a license key

Unlock the full power of Azure Elastic Jobs Manager by purchasing a license key.
The licensed version removes trial limitations and enables full features of the tool.

[Get License Key](https://azureops.org/product/azure-elastic-jobs-manager/){: .btn .btn-green .mr-2 }

## How to install

### Using the Installer
1. Double-click the installer file `Azure Elastic Jobs Manager Installer.exe` and follow the steps to complete the installation of Azure Elastic Jobs Manager.

<img src="../../media/aejm-installer.png"  style="width:70%; height:70%">

### Manual Mode

**Visual Studio 2017/2019**

1. Open Visual Studio 2017 or 2019. 
2. Click `Tools` menu item and click `Extension and Updates`.
3. Under `Online` section, search for `Azure Elastic Jobs Manager` and click `Download`.
<img src="../../media/vs-extension-and-updates.png"  style="width:100%; height:100%">
3. Once the download is done, restart Visual Studio and complete the installation.
4. Click on the Tools menu item. You will see the `Azure Elastic Jobs Manager` option. Click it to launch.

**Visual Studio 2022**

1. Open Visual Studio 2022. 
2. Click `Extensions` menu item and click `Manage Extensions`.
3. Under `Online` section, search for `Azure Elastic Jobs Manager` and click `Download`.
<img src="../../media/vs-extension-and-updates2022.png"  style="width:100%; height:100%">
3. Once the download is done, restart Visual Studio and complete the installation.
4. Click on the Tools menu item. You will see the `Azure Elastic Jobs Manager` option. Click it to launch.

**SQL Server Management Studio 18**

[Download Visual Studio 2017/2019 Extension](https://marketplace.visualstudio.com/items?itemName=AzureOps.elasticjobsmanager1719){: .btn .btn-purple .mr-2 }

1. Extract the file `Azure.Elastic.Jobs.Manager.Plugin.20172019.vsix` content in a folder named `Azure Elastic Jobs Manager` using 7zip.
2. Copy this folder to the location `C:\Program Files (x86)\Microsoft SQL Server Management Studio 18\Common7\IDE\Extensions`. You would need admin permissions to do this.
3. Restart SSMS 18.
4. You will now see the "Azure Elastic Jobs Manager" option under the Tools menu item. Click it to Launch.

**SQL Server Management Studio 19**

[Download Visual Studio 2017/2019 Extension](https://marketplace.visualstudio.com/items?itemName=AzureOps.elasticjobsmanager1719){: .btn .btn-purple .mr-2 }

1. Extract the file `Azure.Elastic.Jobs.Manager.Plugin.20172019.vsix` content in a folder named `Azure Elastic Jobs Manager` using 7zip.
2. Copy this folder to the location `C:\Program Files (x86)\Microsoft SQL Server Management Studio 19\Common7\IDE\Extensions`. You would need admin permissions to do this.
3. Restart SSMS 19.
4. You will now see the "Azure Elastic Jobs Manager" option under the Tools menu item. Click it to Launch.

**SQL Server Management Studio 20**

[Download Visual Studio 2017/2019 Extension](https://marketplace.visualstudio.com/items?itemName=AzureOps.elasticjobsmanager1719){: .btn .btn-purple .mr-2 }

1. Extract the file `Azure.Elastic.Jobs.Manager.Plugin.20172019.vsix` content in a folder named `Azure Elastic Jobs Manager` using 7zip.
2. Copy this folder to the location `C:\Program Files (x86)\Microsoft SQL Server Management Studio 20\Common7\IDE\Extensions`. You would need admin permissions to do this.
3. Restart SSMS 20.
4. You will now see the "Azure Elastic Jobs Manager" option under the Tools menu item. Click it to Launch.   

**Standalone installation**
1. Extract the file `Azure.Elastic.Jobs.Manager.Plugin.20172019.vsix` content in a folder named `Azure Elastic Jobs Manager` using 7zip.
2. Place this folder in your preferred location and double-click the `Azure.Elastic.Jobs.Manager.exe` file, to launch the application.

## How to activate license key

[Get License Key](https://azureops.org/product/azure-elastic-jobs-manager/){: .btn .btn-green .mr-4 }

Once you order the License, you will receive the license key via email. You can also find the license key at [my-accounts](https://azureops.org/my-account/view-license-keys/).
1. Launch `Azure Elastic Jobs Manager Installer.exe`.
<img src="../../media/aejm-activation.png"  style="width:70%; height:70%">
2. Enter the product key on the landing page screen and click on the 'Activate Product' button. It should activate the product on the machine.

## How to uninstall 

**SQL Server Management Studio 18**
1. Close all instances of SSMS 18.
2. Navigate to the location `C:\Program Files (x86)\Microsoft SQL Server Management Studio 18\Common7\IDE\Extensions`. And delete `Azure Elastic Jobs Manager` folder. You would need admin permissions to do this.
3. Start SSMS 18. You should not see Azure Elastic Jobs Manager button under the tools menu item anymore.

**SQL Server Management Studio 19** 
1. Close all instances of SSMS 19.
2. Navigate to the location `C:\Program Files (x86)\Microsoft SQL Server Management Studio 19\Common7\IDE\Extensions`. And delete `Azure Elastic Jobs Manager` folder. You would need admin permissions to do this.
3. Start SSMS 19. You should not see Azure Elastic Jobs Manager button under the tools menu item anymore.

**SQL Server Management Studio 20** 
1. Close all instances of SSMS 20.
2. Navigate to the location `C:\Program Files (x86)\Microsoft SQL Server Management Studio 20\Common7\IDE\Extensions`. And delete `Azure Elastic Jobs Manager` folder. You would need admin permissions to do this.
3. Start SSMS 20. You should not see Azure Elastic Jobs Manager button under the tools menu item anymore.   

**Visual Studio 2017/2019/2022**
1. Navigate to the `Tools` menu item and click on `Extensions and updates`.
2. Locate `Azure Elastic Jobs Manager` from installed plugins and click on `Uninstall` button.
3. You would need to restart Visual Studio for changes to take effect.
