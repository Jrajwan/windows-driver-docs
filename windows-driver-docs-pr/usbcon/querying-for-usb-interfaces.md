---
Description: Instead of using the I/O Request Packet (IRP) mechanism, a USB client driver can get a reference to a bus driver interface and use it to access bus driver routines.
title: Querying for Bus Driver Interfaces
author: windows-driver-content
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Querying for Bus Driver Interfaces


Instead of using the I/O Request Packet (IRP) mechanism, a USB client driver can get a reference to a bus driver interface and use it to access bus driver routines.




Using a bus driver interface gives the client driver several advantages:

-   It can use the interface's services without allocating an IRP.

-   It can call the interface's routines at raised IRQL.

In Windows Vista USB, client drivers can themselves expose an interface to assist the [USB Common Class Generic Parent Driver](usb-common-class-generic-parent-driver.md) in defining interface collections for the device it manages.

To get a bus driver interface, the client driver must send an [**IRP\_MN\_QUERY\_INTERFACE**](https://msdn.microsoft.com/library/windows/hardware/ff551687) request to the bus driver. In your client driver:

1.  Create an IRP of the type IRP\_MN\_QUERY\_INTERFACE in the next stack location.
    ```
    irpstack = IoGetNextIrpStackLocation(irp);
    irpstack->MajorFunction= IRP_MJ_PNP;
    irpstack->MinorFunction= IRP_MN_QUERY_INTERFACE;
    ```

2.  Allocate memory for the interface and make the stack point to the new memory. For example to allocate memory for the [**USB\_BUS\_INTERFACE\_USBDI\_V0**](https://msdn.microsoft.com/library/windows/hardware/ff539210) interface:
    ```
    irpstack->Parameters.QueryInterface.Interface = (USB_BUS_INTERFACE_USBDI_V0) newly allocated interface buffer;
    ```

3.  Set **InterfaceSpecificData** to NULL.
    ```
    irpstack->Parameters.QueryInterface.InterfaceSpecificData = NULL;
    ```

4.  Initialize the IRP stack with the appropriate interface GUID, the size of the interface, and the version of the interface.
    ```
    irpstack->Parameters.QueryInterface.InterfaceType = &USB_BUS_INTERFACE_USBDI_GUID;
    irpstack->Parameters.QueryInterface.Size = sizeof(USB_BUS_INTERFACE_USBDI_V0);
    irpstack->Parameters.QueryInterface.Version = USB_BUSIF_USBDI_VERSION_0;
    ntStatus = IoCallDriver(PDO that the client passes URBs to, irp);
    ```

5.  Call [**IoCallDriver**](https://msdn.microsoft.com/library/windows/hardware/ff548336) to pass the query interface IRP down the stack.
    ```
    ntStatus = IoCallDriver(PDO that the client passes URBs to, irp);
    ```

For further information about USB interfaces see [Bus Driver Interface Routines for USB Client Drivers](https://msdn.microsoft.com/library/windows/hardware/ff540134#usbdi).

## Related topics
[Developing Windows client drivers for USB devices](usb-driver-development-guide.md)  



