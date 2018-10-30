---
title: Synchronizing Operations on a SAN
description: Synchronizing Operations on a SAN
ms.assetid: 9bbceecc-652e-44a7-b969-57578d2ebe68
keywords:
- synchronization WDK SANs
- SAN synchronizations WDK
- Windows Sockets Direct WDK , SAN synchronizations
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Synchronizing Operations on a SAN





The Windows Sockets switch uses its session protocol to handle almost all synchronization between a SAN service provider and applications. That is, the switch, in conjunction with the TCP/IP provider, handles most **WSPAsyncSelect**, **WSPEventSelect**, and **WSPSelect** calls from applications. The switch does not forward these calls to a SAN service provider except when specifying the FD\_ACCEPT and FD\_CONNECT network event codes in calls to a SAN service provider's [**WSPEventSelect**](https://msdn.microsoft.com/library/windows/hardware/ff566287) function, as described in [Setting Up a SAN Connection](setting-up-a-san-connection.md).

 

 





