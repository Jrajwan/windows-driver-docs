---
title: CM_PROB_PARTIAL_LOG_CONF
description: CM_PROB_PARTIAL_LOG_CONF
ms.assetid: 1e8b10e8-c2c6-4a71-9af5-575206098148
keywords:
- CM_PROB_PARTIAL_LOG_CONF
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# CM_PROB_PARTIAL_LOG_CONF

This function is reserved for system use.





The device is only partially configured.

### Error Code

16

### Display Message (Windows 2000 and later versions of Windows)

"Windows cannot identify all the resources this device uses. (Code 16)"

"To specify additional resources for this device, click the Resources tab and fill in the missing settings. Check your hardware documentation to find out what settings to use."

### Recommended Resolution (Windows 2000 and later versions of Windows)

Manually configure the resources that the device requires.

To configure device resources, follow these steps:

1.  [Open Device Manager](using-device-manager.md).

2.  Double-click the icon that represents the device in the Device Manager window.

3.  On the device properties sheet that appears, click the **Resources** tab. The device resources are listed in the **resource settings** list on the **Resources** page.

4.  If a resource in the **resource settings** list has a question mark next to it, select that resource to assign it to the device.

5.  If a resource cannot be changed, click **Change Settings**. If **Change Settings** is unavailable, try to clear the **Use automatic settings** check box to make it available.

If the device is not a Plug and Play device, look in the device documentation for more information about how to configure resources for the device.

 

 





