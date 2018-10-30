---
title: Opening and Closing a Parallel Port
author: windows-driver-content
description: Opening and Closing a Parallel Port
ms.assetid: 2183ffd9-8265-4848-b5d1-703643e0d0e6
keywords:
- parallel ports WDK , opening
- parallel ports WDK , closing
- parallel ports WDK , sharing
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Opening and Closing a Parallel Port





Clients can share a parallel port. A client must open a file on a parallel port before the client can use other I/O requests or use the [parallel port callback routines](https://msdn.microsoft.com/library/windows/hardware/ff544307). A client must not attempt to communicate with a parallel port after the client has closed its file on the port.

Note that in a Plug and Play environment, a device can be removed or added whenever there are no open files on it. In general, every time a parallel port is added, Plug and Play assigns a different location and resources.

 

 




