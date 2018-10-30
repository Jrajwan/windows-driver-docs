---
Description: You need to write a driver for the connector if your USB Type-C system does not include an embedded controller, otherwise you can load the Microsoft-provided UCSI driver.
title: Developing Windows drivers for USB Type-C connectors
author: windows-driver-content
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Developing Windows drivers for USB Type-C connectors
You need to write a driver for the connector if your USB Type-C system does not implement PD state machine or it implements state machine but does not support UCSI over non-ACPI transport. If it does, you can load the Microsoft-provided [UCSI driver](ucsi.md).

**Intended audience**

-   Driver development guidance for a USB Type-C system does not include an embedded controller.

**Last Updated**

-   March 2016

**Windows version**

-   Windows 10 for desktop editions (Home, Pro, Enterprise, and Education)
-   Windows 10 Mobile

**Important APIs**

-   [UCmCx client driver programming reference](https://msdn.microsoft.com/library/windows/hardware/mt188011)

-   [USB Type-C Port Controller Interface driver class extensions reference](https://msdn.microsoft.com/en-us/library/windows/hardware/mt805826)


![drivers](images/drivers-c.png)

| Hardware/Firmware capabilities                        | Non-detachable    | Add-on card    | 
|------------------------------------------------------ |-------------      |---            |
|USB Type-C connector does not have a PD state machine.  | Write a client driver to UcmTcpciCx. <p>Start with [UcmTcpciCx Port Controller Client Driver](https://github.com/Microsoft/Windows-driver-samples/tree/master/usb/UcmTcpciCxClientSample) </p>| Write a client driver to UcmCx. <p>Start with the [UcmCx sample](https://github.com/Microsoft/Windows-driver-samples/tree/master/usb/UcmCxUcsi).</p>| 
|Connector is UCSI-compliant with ACPI.                  | Load the in-box driver, UcmUcsi.sys.  |N/A| 
|Connector is UCSI-compliant without ACPI.| Write a client driver to UcmCx. <p>Start with the [UcmCx sample](https://github.com/Microsoft/Windows-driver-samples/tree/master/usb/UcmCxUcsi) and replace the ACPI your implementation for the required bus.| Write a client driver to UcmCx. <p>Start with the [UcmCx sample](https://github.com/Microsoft/Windows-driver-samples/tree/master/usb/UcmCxUcsi) and replace the ACPI your implementation for the required bus. |
| Has PD state machine but is not UCSI-compliant.| Write a client driver to UcmCx. <p>Start with the [UcmCx sample](https://github.com/Microsoft/Windows-driver-samples/tree/master/usb/UcmCxUcsi).  |Write a client driver to UcmCx. <p>Start with the [UcmCx sample](https://github.com/Microsoft/Windows-driver-samples/tree/master/usb/UcmCxUcsi). </p>|                 
## In this section
To implementation the proposed solutions in the preceding table, read these topics:
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Topic</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[Architecture: USB Type-C design for a Windows system](architecture--usb-type-c-in-a-windows-system.md)</p></td>
<td><p>Describes a typical hardware design of a USB Type-C system and the Microsoft-provided drivers that support the hardware components.</p></td>
</tr>
<tr class="even">
<td><p>[Bring up the function controller on a USB Type-C Windows system](function-controller-bringup-for-a-usb-type-c-system.md)</p></td>
<td><p>The driver for the function controller informs the operating system about the charging levels that its USB Type-C connector supports and notifies the battery subsystem when it can begin charging and the maximum amount of current the device can draw.</p></td>
</tr>
<tr class="odd">
<td><p>[Bring up the dual-role controller for a USB Type-C Windows system](dual-role-controller-bringup-for-a-usb-type-c-system.md)</p></td>
<td><p>The USB role-switch drivers (URS) are a set of WDF class extension and its client driver that handles the role-switching capability of a dual-role controller. If your system has a dual role controller, you can switch the role of the system depending on the device that is attached to the partner port of the USB Type-C connector of the system. This allows interesting scenarios such as wired docking.</p></td>
</tr>
<tr class="even">
<td><p>[Write a USB Type-C connector driver](bring-up-a-usb-type-c-connector-on-a-windows-system.md)</p></td>
<td><p>Describes the USB connector manager (UCM) that manages a USB Type-C connector and the expected behavior of a connector driver.</p></td>
</tr>
<tr class="odd">
<td><p>[Write a USB Type-C port controller driver](write-a-usb-type-c-port-controller-driver.md)</p></td>
<td><p>Describes how to write a the USB Type-C port controller driver that communicates with a USB Type-C connector without PD state machine. </p></td>

</tr>
</tbody>
</table>

 

**Related sections**

<a href="" id="write-a-usb-role-switch--urs--client-driver"></a>Write a USB role-switch (URS) client driver  
[USB Dual Role Driver Stack Architecture](usb-dual-role-driver-stack-architecture.md)

[USB dual-role controller driver programming reference](https://msdn.microsoft.com/library/windows/hardware/mt628026)

<a href="" id="write-a-usb-function-client-driver"></a>Write a USB function client driver  
[Developing Windows drivers for USB function controllers](developing-windows-drivers-for-usb-function-controllers.md)

[USB function controller programming reference](https://msdn.microsoft.com/library/windows/hardware/mt188013)

## Related topics
[Windows support for USB Type-C connectors](oem-tasks-for-bringing-up-a-usb-typec.md)  



