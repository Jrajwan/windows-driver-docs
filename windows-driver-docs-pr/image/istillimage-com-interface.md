---
title: IStillImage COM Interface
author: windows-driver-content
description: IStillImage COM Interface
ms.assetid: eb60a3fd-e7e2-4d3c-973e-af8cb3c3c511
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# IStillImage COM Interface





The **IStillImage** COM interface provides access to the [Still Image Event Monitor](overview-of-sti-components.md#ddk-still-image-event-monitor-si) so applications can register themselves as "push-model aware". Applications can use this interface to obtain information about the system's still image devices.

The interface provides some application management functions, such as enabling event notification and starting an application, for use by customized application control software.

Additionally, the **IStillImage** interface provides access to the [IStiDevice COM Interface](istidevice-com-interface.md), which allows applications to perform I/O operations on still image devices.

The following table lists and describes all of the **IStillImage** interface's methods. The table indicates the types of clients that typically must call each method.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Method</th>
<th>Description</th>
<th>Typical Callers</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[<strong>IStillImage::CreateDevice</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543778)</p></td>
<td><p>Creates an instance of the COM object that defines the <strong>IStiDevice</strong> interface, and returns a pointer to the interface.</p></td>
<td><p>Image Acquisition APIs</p></td>
</tr>
<tr class="even">
<td><p>[<strong>IStillImage::EnableHwNotifications</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543780)</p></td>
<td><p>Enables or disables the notification of applications when [Still Image Device Events](still-image-device-events.md) occur for a specified device.</p></td>
<td><p>Still image event monitor</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>IStillImage::GetDeviceInfo</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543782)</p></td>
<td><p>Returns hardware characteristics for a specified still image device.</p></td>
<td><p>Image Acquisition APIs</p></td>
</tr>
<tr class="even">
<td><p>[<strong>IStillImage::GetDeviceList</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543784)</p></td>
<td><p>Returns hardware characteristics for all installed still image devices.</p></td>
<td><p>Scanners and Cameras Control Panel, Image Acquisition APIs</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>IStillImage::GetDeviceValue</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543786)</p></td>
<td><p>Returns registry information associated with a specified still image device.</p></td>
<td><p>Image Acquisition APIs, Scanners and Cameras Control Panel</p></td>
</tr>
<tr class="even">
<td><p>[<strong>IStillImage::GetHwNotificationState</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543788)</p></td>
<td><p>Indicates whether applications will be notified when still image device events occur on a specified device.</p></td>
<td><p>Still image event monitor</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>IStillImage::GetSTILaunchInformation</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543790)</p></td>
<td><p>Returns the reason the calling still image application was started, if the still image event monitor started it.</p></td>
<td><p>Push-model aware applications</p></td>
</tr>
<tr class="even">
<td><p>[<strong>IStillImage::Initialize</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543793)</p></td>
<td><p>Initializes the object instance.</p></td>
<td><p>Not called directly</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>IStillImage::LaunchApplicationForDevice</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543796)</p></td>
<td><p>Starts a specified application for a specified still image device.</p></td>
<td><p>Still image event monitor</p></td>
</tr>
<tr class="even">
<td><p>[<strong>IStillImage::RegisterLaunchApplication</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543798)</p></td>
<td><p>Adds an application to the still image event monitor's list of push-model aware applications.</p></td>
<td><p>Push-model aware applications or their installers</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>IStillImage::Release</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543799)</p></td>
<td><p>Closes the object instance and removes access to the <strong>IStillImage</strong> interface.</p></td>
<td><p>All <strong>IStillImage</strong> interface clients</p></td>
</tr>
<tr class="even">
<td><p>[<strong>IStillImage::SetDeviceValue</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543801)</p></td>
<td><p>Sets registry information for a specified still image device.</p></td>
<td><p>Scanners and Cameras Control Panel</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>IStillImage::SetupDeviceParameters</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543803)</p></td>
<td><p>Allows clients of the <strong>IStillImage</strong> interface to modify a still image device's stored characteristics.</p></td>
<td><p>Scanners and Cameras Control Panel</p></td>
</tr>
<tr class="even">
<td><p>[<strong>IStillImage::StiCreateInstance</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543804)</p></td>
<td><p>Creates an instance of the COM object that defines the <strong>IStillImage</strong> interface, and returns a pointer to the interface.</p></td>
<td><p>All <strong>IStillImage</strong> interface clients</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>IStillImage::UnregisterLaunchApplication</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543806)</p></td>
<td><p>Removes an application from the still image event monitor's list of push-model aware applications.</p></td>
<td><p>Push-model aware applications or their installers</p></td>
</tr>
<tr class="even">
<td><p>[<strong>IStillImage::WriteToErrorLog</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543807)</p></td>
<td><p>Writes a message to the still image error log.</p></td>
<td><p>All <strong>IStillImage</strong> interface clients</p></td>
</tr>
</tbody>
</table>

 

 

 




