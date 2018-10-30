---
title: Installing Serenum Devices
author: windows-driver-content
description: Installing Serenum Devices
ms.assetid: abb58ce0-7afb-43eb-81e0-1942d451355a
keywords:
- Serenum driver WDK , device installations
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Installing Serenum Devices





To install a device that is enumerated by Serenum, use the following [*hardware ID*](https://msdn.microsoft.com/library/windows/hardware/ff556288#wdkgloss-hardware-id) format for the device:

Serenum\\*XxxxYyyy*

Where: *Xxxx* is a field of four ASCII characters that specify the EISA Manufacturing ID; *Yyyy* is a field of four ASCII characters that specify the Product ID. Serenum IDs are documented in the [Plug and Play External COM Device Specification](http://msdn.microsoft.com/windows/hardware/gg463189.aspx).

 

 




