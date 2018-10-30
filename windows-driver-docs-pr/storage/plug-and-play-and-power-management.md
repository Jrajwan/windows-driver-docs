---
title: Plug and Play and Power Management
author: windows-driver-content
description: Plug and Play and Power Management
ms.assetid: 9e5d545d-ec24-42ac-a9e5-290502548fc0
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Plug and Play and Power Management


The LsiU3AdapterControl routine allows for special adapter control routines to be implemented without changing its HW\_INITIALIZATION\_DATA structure. It contains support for the StopAdapter and ScsiRestartAdapter ControlTypes, which replace the HwFindAdapter and HwInitialize routines for adapters going through a power management cycle. In addition, the LsiU3StartIo routine adds handling of SRBs with function code SRB\_FUNCTION\_POWER for HBA shutdown.

 

 




