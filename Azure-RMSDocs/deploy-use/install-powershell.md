---
# required metadata

title: Install PowerShell for Azure Rights Management - AIP
description: Instructions to install Windows PowerShell for the Azure Rights Management service from Azure Information Protection. The name of this module is AADRM.
author: cabailey
ms.author: cabailey
manager: mbaldwin
ms.date: 01/17/2018
ms.topic: article
ms.prod:
ms.service: information-protection
ms.technology: techgroup-identity
ms.assetid: 0d665ed6-b1de-4d63-854a-bc57c1c49844

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: esaggese
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Installing Windows PowerShell for Azure Rights Management

>*Applies to: Azure Information Protection, Office 365*

Use the following information to help you install the Windows PowerShell module for the Azure Rights Management service from Azure Information Protection.

You can use this PowerShell module to administer the Azure Rights Management service from the command line by using any computer that has an Internet connection and that meets the prerequisites listed in the next section. Windows PowerShell for [!INCLUDE[aad_rightsmanagement_1](../includes/aad_rightsmanagement_1_md.md)] supports scripting for automation or might be necessary for advanced configuration scenarios. For more information about the administration tasks and configurations that the module supports, see [Administering Azure Rights Management by Using Windows PowerShell](administer-powershell.md).

## Prerequisites
This table lists the prerequisites to install and use Windows PowerShell for [!INCLUDE[aad_rightsmanagement_1](../includes/aad_rightsmanagement_1_md.md)].

|Requirement|More information|
|---------------|--------------------|
|A version of Windows that supports the [!INCLUDE[aad_rightsmanagement_2](../includes/aad_rightsmanagement_2_md.md)] administration module|Check the list of supported operating systems in the **System Requirements** section of the [download page for the Azure Rights Management Administration Tool](http://go.microsoft.com/fwlink/?LinkId=257721).|
|Minimum version of Windows PowerShell: 2.0<br /><br /> |By default, most Windows operating systems install with at least version 2.0 of Windows PowerShell. If you need to install this minimum supported version, see [Install Windows PowerShell 2.0](https://msdn.microsoft.com/library/ff637750.aspx).<br /><br />Tip: You can confirm the version of Windows PowerShell that you are running by typing `$PSVersionTable` in a PowerShell session. <br /><br /> If you have this minimum version, you need to manually load the module in your PowerShell session by running `Import-Module AADRM` before you can use any cmdlet from the Rights Management administration module. When you have Windows PowerShell v3 and later, the module loads automatically and you do not need this extra command.|
|Minimum version of the Microsoft .NET Framework: 4.5<br /><br />Note: This version of the Microsoft .NET Framework is included with the later operating systems, so you should  need to manually install it only if your client operating system is less than Windows 8.0 or your server operating system is less than Windows Server 2012.|If the minimum version of the  Microsoft .NET Framework is not already installed, you can download [Microsoft .NET Framework 4.5](http://www.microsoft.com/download/details.aspx?id=30653).<br /><br />This minimum version of the Microsoft .NET Framework is required for some of the classes that the [!INCLUDE[aad_rightsmanagement_2](../includes/aad_rightsmanagement_2_md.md)] administration module uses.|

> [!NOTE]
> Starting with version 2.5.0.0 of the Rights Management administration module, the Microsoft Online Services Sign-In Assistant is no longer required.
> 
> If you had a previous version of the Rights Management administration module installed, use **Programs and Features** to uninstall **Windows Azure AD Rights Management Administration** before you install the latest version.


## How to install the Rights Management administration module

1. Go to the Microsoft Download Center and locate the [Azure Rights Management Administration Tool](https://go.microsoft.com/fwlink/?LinkId=257721), which contains the [!INCLUDE[aad_rightsmanagement_1](../includes/aad_rightsmanagement_1_md.md)] administration module for Windows PowerShell.

2. Download and save the [!INCLUDE[aad_rightsmanagement_2](../includes/aad_rightsmanagement_2_md.md)] installer file, **WindowsAzureADRightsManagementAdministration_x64**. Then double-click this file to start the Azure AD Rights Management Administration Setup Wizard.

3.  Complete the wizard.

Windows PowerShell for [!INCLUDE[aad_rightsmanagement_1](../includes/aad_rightsmanagement_1_md.md)] is now installed.

## Next steps
Start a Windows PowerShell session and confirm the version of the installed module. This check is particularly important if you upgraded from an older version:

```
(Get-Module AADRM –ListAvailable).Version
```

Note: If this command fails, first run **Import-Module AADRM**.

To see which cmdlets are available, type the following:

```
Get-Command -Module AADRM
```

Use the `Get-Help <cmdlet_name>` command to see the Help for a specific cmdlet, and use the **-online** parameter to see the latest help on the Microsoft documentation site. For example:

```
Get-Help Connect-AadrmService -online
```


For more information:

-   Full list of cmdlets available: [AADRM Module](/powershell/aadrm/vlatest/rightsmanagement)

-   List of main configuration scenarios that support  PowerShell: [Administering Azure Rights Management by Using Windows PowerShell](administer-powershell.md)

Before you can run any commands that configure the [!INCLUDE[aad_rightsmanagement_1](../includes/aad_rightsmanagement_1_md.md)] service, you must connect to the service by using the [Connect-AadrmService](/powershell/aadrm/vlatest/connect-aadrmservice) cmdlet. 

When you have finished running your configuration commands, as a best practice, disconnect from the service by using the [Disconnect-AadrmService](/powershell/aadrm/vlatest/disconnect-aadrmservice) cmdlet. If you do not disconnect, the connection is automatically disconnected after a period of inactivity. Because of the automatic disconnection behavior, you might find that you need to occasionally reconnect in a PowerShell session. 

> [!NOTE]
> If the Azure Rights Management service is not yet activated, you can do this after you have connected to the service, by using the [Enable-Aadrm](/powershell/aadrm/vlatest/enable-aadrm) cmdlet.


[!INCLUDE[Commenting house rules](../includes/houserules.md)]