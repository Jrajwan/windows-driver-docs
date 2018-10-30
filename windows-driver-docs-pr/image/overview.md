---
title: Distributed Scan Management (DSM) overview
author: windows-driver-content
description: Distributed Scan Management (DSM) enables IT administrators to manage scanning services for organizations with many users.
ms.assetid: e9a45ae0-0ec8-4d6c-8486-ae88bdaa1f8c
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Distributed Scan Management (DSM) overview


Distributed Scan Management (DSM) enables IT administrators to manage scanning services for organizations with many users. DSM is implemented in Windows Server 2008 R2 and uses Web Services on Devices (WSD) technologies to integrate scanning devices into the system.

For a list of helpful DSM terms and definitions, see [DSM Terminology](dsm-terminology.md).

A device that supports DSM can be a network-connected image scanner, or it can be a scanner function in a network-connected copier or multifunction printer. A DSM scan device works in conjunction with a DSM scan server. DSM Scan Server is a feature in Windows Server 2008 R2 and the user can select the Print and Document Services Role to enable this feature. During a scanning job, the scan device acquires images from the documents that it scans and sends the images to the scan server. The scan server processes and stores the images.

A user initiates a scanning job from the user interface of a DSM device instead of from the user interface of an application running on a desktop computer. To configure the device for the scanning job, the user selects a scan process--a set of instructions for acquiring and processing images--that was previously created by an administrator. The scan process contains the following information:

-   A scan ticket that contains the image-acquisition settings for the DSM device.

-   A DSM scan server to send the acquired images.

-   A set of scan processing instructions to specify how the images acquired by the device are to be processed and stored by the DSM scan server.

    **Note**   In other contexts, the term *process* can have other meanings. For example, *process* might refer to a program instance that is scheduled and executed by an operating system. To avoid confusion with this usage, this section always uses the term *scan process* in full and never abbreviates it as *process*.

     

The communication protocols defined for Distributed Scan Management operate in conjunction with the Web Services on Devices for scanners (WS-Scan) protocol, which was introduced in Windows Vista. The WS-Scan protocol is based on the [Devices Profile for Web Services](http://go.microsoft.com/fwlink/p/?linkid=59069) (DPWS) specification. WS-Scan has these features:

-   Easy discovery of network-connected DSM devices.

-   An eventing model to inform the user of changes in the scanner hardware status and image-processing activity.

-   A seamless administrative experience for managing scanning operations.

In Windows Server 2008 R2, to complement WS-Scan, Distributed Scan Management provides the following features to meet the needs of organizations with many users:

-   A new user interface, the Windows Scan-Management Console (SMC), to enable IT administrators to manage scanning activities across an organization. Administrators use the SMC to define scan processes for various groups of users. The SMC is part of the Microsoft Management Console (MMC) Windows Server technology.

-   A DSM scan server, to process and store images acquired by a DSM device.

-   The SMC and the Distributed Scan Server are integrated with Active Directory, which stores scan processes and determines which scan processes are available to a user.

-   Full support for push-scan operations. In fact, Distributed Scan Management supports only push-scan operations. A scanning operation with Distributed Scan Management can be initiated only by a user who interacts directly with the DSM device.

 

 




