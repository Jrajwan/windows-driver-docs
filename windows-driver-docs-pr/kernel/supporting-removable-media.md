---
title: Supporting Removable Media
author: windows-driver-content
description: Supporting Removable Media
ms.assetid: f70c404c-8a38-4f53-8681-6efb52b30656
keywords: ["removable media WDK kernel", "removable media WDK kernel , about removable-media devices", "IRPs WDK kernel , removable media", "kernel-mode drivers WDK , removable media"]
ms.author: windowsdriverdev
ms.date: 06/16/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Supporting Removable Media





File systems and removable-media device drivers share the responsibility for ensuring that the correct media is mounted when a file is opened on a removable-media device and that the correct media remains mounted during operations that access the media. Any intermediate driver layered between a file system and a removable-media device driver also shares this responsibility.

Drivers that work with removable-media devices therefore should be capable of doing one or more of the following:

[Responding to check-verify requests from the file system](responding-to-check-verify-requests-from-the-file-system.md)

[Notifying the file system of possible media changes](notifying-the-file-system-of-possible-media-changes.md)

[Checking flags in the device object](checking-flags-in-the-device-object.md)

[Setting up IRPs in intermediate drivers](setting-up-irps-in-intermediate-drivers.md)

 

 




