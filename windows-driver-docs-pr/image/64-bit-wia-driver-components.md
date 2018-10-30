---
title: 64-Bit WIA Driver Components
author: windows-driver-content
description: 64-Bit WIA Driver Components
ms.assetid: c5951977-1ac9-4ef3-9427-f964cab9725e
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# 64-Bit WIA Driver Components


A 64-bit WIA minidriver is loaded into the WIA service's process, which is a 64-bit process in 64-bit editions of the Windows operating system. As a result, a WIA driver for the x64-based versions of Windows XP, Windows Server 2003, and Windows Vista can contain only 64-bit driver components. For example, it must contain a 64-bit minidriver, 64-bit WIA minidriver UI extensions, and potentially a 64-bit kernel-mode driver.

 

 




