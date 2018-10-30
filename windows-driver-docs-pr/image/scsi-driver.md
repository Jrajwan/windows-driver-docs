---
title: SCSI Driver
author: windows-driver-content
description: SCSI Driver
ms.assetid: e69e3ac6-6726-4f63-afdb-2da1255dde19
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# SCSI Driver





The kernel-mode still image driver for SCSI buses supports **ReadFile** by creating a command descriptor block (CDB) that includes a SCSI **Read** command. It supports **WriteFile** by creating a CDB that includes a SCSI **Write** command. User-mode minidrivers can specify customized CDBs by calling [**DeviceIoControl**](https://msdn.microsoft.com/library/windows/desktop/aa363216). For more information, see [SCSI Still Image I/O Control Codes](https://msdn.microsoft.com/library/windows/hardware/ff548003). See the Microsoft Windows SDK documentation for descriptions of **ReadFile** and **WriteFile**.

 

 




