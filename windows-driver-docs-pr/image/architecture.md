---
title: Architecture
author: windows-driver-content
description: Architecture
ms.assetid: af6a338a-feb2-47a4-a8ed-eedbc4c11797
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Architecture


The following figure shows an overview of the DSM Scan Management architecture.

![diagram illustrating dsm scan-management architecture](images/wsdbizscan.png)

In addition to the Active Directory server, the preceding figure shows the following components:

-   The DSM Device is a network-connected standalone scanner device, or the scanner function in a network-connected copier or multifunction printer.

-   The DSM Control Point is a desktop computer from which an IT administrator runs the Windows scan-management console (SMC) to manage the scanning activities in the organization.

-   The DSM Scan Server processes and stores image data acquired from the DSM device.

The communication paths shown between components are network connections.

### **DISTRIBUTED SCAN DEVICE WEB SERVICE**

A scan-management console (SMC) running on a control point uses the Distributed Scan Device Web Service (WS-DSD) protocol to communicate with a DSM device. This protocol uses a subset of the XML schema elements defined in the WS Scan Service Version 1.0 specification. For more information about this schema, see [Web Services on Devices Scan Service Schema](https://msdn.microsoft.com/library/windows/hardware/ff547963).

An administrator runs the SMC to discover DSM devices and to create scan processes for those devices. Through the SMC, the administrator retrieves scanner elements, device status, and device configuration information from a device. After the administrator creates a scan ticket for the device, the SMC can ask the device to validate the scan ticket. The SMC stores the completed scan process, including the validated scan ticket, in Active Directory.

For more information about the Distributed Scan Device Web Service protocol, see [Distributed Scan Device Web Service Protocol Summary](distributed-scan-device-web-service-protocol-summary.md).

### <a href="" id="distributed-scan-configuration-web-service--ws-dsc-"></a>Distributed Scan Configuration Web Service (WS-DSC)

A scan-management console (SMC) running on a control point uses the Distributed Scan Configuration Web Service (WS-DSC) protocol to communicate with a DSM scan server.

For more information, see the description of the WS-DSC schema in the Windows SDK documentation.

**Note** WS-DSC is related to MS-BDSRR (Scan Repository Capabilities and Status Retrieval Protocol Specification (MS-BDSRR). For more information about MS-BDSRR, see the [Scan Repository Capabilities and Status Retrieval Protocol Specification](http://go.microsoft.com/fwlink/p/?linkid=154735).

A DSM device uses the Distributed Scan Processing Web Service protocol to communicate with a DSM scan server. This protocol uses the XML schema described in [Distributed Scan Processing Web Service Schema](https://msdn.microsoft.com/library/windows/hardware/ff541133).

Before a user can initiate a push-scan operation from a DSM device, the device authenticates the user. For example, the device might have an attached badge reader. The device then sends the user's X.509 certificate to Active Directory. Following authorization, the device obtains from Active Directory a list of the scan processes that the user is authorized to use. The device asks the user to select a scan process from this list, and the device downloads the selected scan process from Active Directory.

After the user selects a scan process, the DSM device can use the Distributed Scan Processing Web Service protocol to communicate with the DSM scan server identified in the scan process. The device asks the scan server to create a post-scan processing job--an instance of the selected scan process--and the scan server validates the parameters requested for the job against the scan process description stored in Active Directory. After the device creates the job, the device sends the images that it acquires to the scan server to be processed and stored.

For more information about the Distributed Scan Processing Web Service protocol, see [Distributed Scan Processing Web Service Protocol Summary](distributed-scan-processing-web-service-protocol-summary.md). For more information about X.509 certificates, see [X.509 Certificate Profile](http://go.microsoft.com/fwlink/p/?linkid=70416).

 

 




