---
title: DIFx Guidelines
description: DIFx Guidelines
ms.assetid: de34f810-0e90-4626-b84d-160ac61541ad
ms.author: windowsdriverdev
ms.date: 05/24/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# DIFx Guidelines

Starting in Windows 10 Version 1607 (Redstone 1), the Driver Install Frameworks (DIFx) tools are no longer included in the WDK.  Instead, we recommend providing your driver as a standalone package that doesn't require an installer, ideally through Windows Update.  To add your driver to Windows Update, the first step is to submit your driver package to the [Sysdev Driver Portal](http://sysdev.microsoft.com).

If you choose to use DIFx anyway, you should be aware of a couple caveats:

* If your driver package specifies only **TargetOSVersion** values of Windows 8.1 or later, you cannot use DIFxApp.  **TargetOSVersion** is specified in the [INF Manufacturer Section](inf-manufacturer-section.md). DIFxApp exposes MSI custom actions such as MsiProcessDrivers, MsiInstallDrivers, and MsiUninstallDrivers.  If your driver package specifies only **TargetOSVersion** values of Windows 8.1 or later, you cannot use these custom actions in your MSI.
* Starting in Windows 8.1, applications that link to `Difxapi.dll` must contain an app manifest targeting the OS version on which the application is intended to run.  This is due to DIFxAPI's dependency on [**GetVersionEx**](https://msdn.microsoft.com/library/windows/desktop/ms724451), an API that changed starting in Windows 8.1.  For more on changes to **GetVersionEx** in Windows 8.1, see [Targeting your application for Windows](https://msdn.microsoft.com/library/windows/desktop/dn481241).
* Use DIFx version 2.1, which is available in the Windows 7 WDK through the Windows 10 Version 1511 WDK.  Although DIFx version 2.1 was available in earlier versions of the WDK, it was not properly compatible with Windows 7 and later versions of Windows.

Although it's no longer being updated, you can find API reference documentation for DIFx at [Difxapi.h](https://docs.microsoft.com/previous-versions/windows/hardware/difxapi/).
