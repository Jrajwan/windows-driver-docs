---
title: HID Transports
author: windows-driver-content
description: HID Transports
ms.assetid: E442CB87-992B-475A-A97F-9C22468BA877
keywords:
- HID Transports
- USB transport
- Bluetooth transport
- Bluetooth
- Bluetooth LE
- I2C
- transport minidriver
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# HID Transports


HID transports supported in current and previous versions of Windows.

| Transport    | In-box minidriver | Windows 7 | Windows 8 | Windows 10 | Notes                                                                                                 |
|--------------|-------------------|-----------|-----------|------------|-------------------------------------------------------------------------------------------------------|
| USB          | Hidusb.sys        | Yes       | Yes       | Yes        | Support for USB HID 1.11+ is provided on Windows operating systems dating back to Windows 2000.       |
| Bluetooth    | Hidbth.sys        | Yes       | Yes       | Yes        | Support for Bluetooth HID 1.1+ is provided on Windows operating systems dating back to Windows Vista. |
| Bluetooth LE | HidBthLE.dll      | No        | Yes       | Yes        | Windows 8 introduces support for HID over Bluetooth LE.                                               |
| I²C          | Hidi2c.sys        | No        | Yes       | Yes        | Windows 8 introduces support for HID over I2C.                                                        |
| GPIO         | Hidinterrupt.sys  | No        | No        | Yes        | Windows Windows 10 introduces support for general-purpose I/O (GPIO) buttons.                         |

 

Microsoft recommends that whenever possible, you use in-box drivers for the transports listed in the preceding table.

If your device requires a transport other than USB, Bluetooth, Bluetooth LE, or I²C, you can develop a miniport driver which is described in the [Transport Minidrivers](transport-minidrivers.md) topic

## HID transport limits


-   **Report Descriptor Length**

    A transport minidriver submits report descriptors to Hidclass in a [**HID\_DESCRIPTOR**](https://msdn.microsoft.com/library/windows/hardware/ff539885) structure. Regardless of the size defined by the transport protocol for transferring HID report descriptor with their devices, the actual report descriptor size is limited during the communication between Hidclass and HID minidrivers.

-   **TLCs in a Report Descriptor**

    The Hidclass/Hidparse driver pair is aware of the number of TLCs in a Report Descriptor. HID miniport drivers do not know that information. Each TLC has at least 2 bytes to start a collection and 1 byte to end the collection.

-   **Input/Output/Feature Report Length**

    The Hidclass/Hidparse driver pair defines lengths of HID Input, Output, and Feature Reports. The limit is 8 KB (minus 1 bit). Even if a HID minidriver can request a transfer of more than 8 KB for a report, only reports smaller than 8 KB are successfully transferred.

| In-box minidriver | Report Descriptor Length | TLCs in One Report Descriptor | Input/Output/Feature Report Length |
|-------------------|--------------------------|-------------------------------|------------------------------------|
| Hidclass/Hidparse | 65535 bytes              | 21845                         | 8 KB - 1 bit                       |
| Hidusb            | 65535 bytes              | N/A                           | 64 KB                              |
| Hidbth            | 65535 bytes              | N/A                           | 64 KB                              |
| HidBthLE          | 65535 bytes              | N/A                           | 64 KB                              |
| Hidi2c            | 65535 bytes              | N/A                           | 64 KB                              |

 

 

 




