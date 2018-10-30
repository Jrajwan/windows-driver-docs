---
title: Management of I2S and SCO Resources
description: The Management of I2S and SCO Resources topic discusses the assumptions that were made in the design of this new support for Bluetooth bypass audio streaming in Windows 8.1.
ms.assetid: C6CA73D9-0DCC-496D-8306-CB1625B86AC9
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Management of I2S and SCO Resources


The Management of I2S and SCO Resources topic discusses the assumptions that were made in the design of this new support for Bluetooth bypass audio streaming in Windows 8.1.

At this time Windows assumes that there is only one Bluetooth host controller. And also, the HFP synchronous connection oriented (SCO) bypass support assumes that there is only one bypass connection and that, any channel opened through the HFP device driver interface is associated with that single connection.

Audio drivers should arbitrate this channel and the single bypass connection for a single consumer on a first-come first-serve basis. The simplest way to achieve this is for the driver to allow only a single filter to transition its pins to the ACQUIRE state.

## <span id="related_topics"></span>Related topics
[Theory of Operation](theory-of-operation.md)  



