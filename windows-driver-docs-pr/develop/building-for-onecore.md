---
ms.assetid: ee46801a-4fa5-465a-aa81-5e76eb83d315
title: Building for OneCore
description: You can build a single binary that targets pre-Windows 10 and OneCore editions.
ms.author: windowsdriverdev
ms.date: 07/19/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Building for OneCore

When you use Visual Studio to build user-mode code for Windows 10, you can customize linker options to target specific versions of Windows.  Consider the following factors:

* Should the built binary run on only the most recent version of Windows?  Or should it run on *downlevel* versions, meaning Windows 7 and later?  

* Does your project have any [UWP](https://docs.microsoft.com/windows/uwp/get-started/whats-a-uwp) dependencies?

By default, when you create a new UMDF v2 driver project, Visual Studio links to `OneCoreUAP.lib`.  This results in a binary that runs on the most recent version of Windows, and it permits addition of UWP functionality.

However, depending on your requirements, you might choose instead to link to one of the following:

|Library|Scenario|
|-|-|
|`OneCore.lib`|All editions of latest OS version, no UWP support|
|`OneCoreUAP.lib`|UWP editions (Desktop, IoT, HoloLens, but not Nano Server) of latest OS version|
|`OneCore_downlevel.lib`|Windows 7 and later, all editions of Windows 10, no UWP support|
|`OneCoreUAP_downlevel.lib`|Windows 7 and later, UWP editions (Desktop, IoT, HoloLens, but not Nano Server) of Windows 10|

When you use a downlevel option, a subset of APIs compile fine but return immediately on non-Desktop OneCore editions (for example Mobile or IoT).

For example, the [**InstallApplication**](https://msdn.microsoft.com/library/aa374307) function returns ERROR_ NOT_SUPPORTED on non-Desktop OneCore editions.

If you link to `OneCoreUAP.lib` or `OneCore.lib`, you will get a slight load time performance boost over the downlevel options.

To change linker options in Visual Studio, choose project properties and navigate to **Linker->Input->Additional Dependencies**.

## Recommended actions

Review the linker options above and update your Visual Studio project accordingly.

Use the [ApiValidator](validating-universal-drivers.md) tool in the WDK.  This tool runs automatically when you build a driver in Visual Studio.

Use runtime testing to verify that your user-mode code runs as you expect on non-Desktop OneCore editions.  Note that stubbed APIs may generate different error codes.

See also
---
[OneCore](https://docs.microsoft.com/windows-hardware/get-started/what-s-new-in-windows)

<!--API BOILERPLATE: Compiles using onecore_downlevel.lib, but always returns ERROR_CALL_NOT_IMPLEMENTED on non-Desktop OneCore editions.-->
