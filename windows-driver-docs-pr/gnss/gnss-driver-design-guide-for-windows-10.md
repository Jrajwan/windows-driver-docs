---
title: GNSS driver design guide for Windows 10
author: windows-driver-content
description: Describes design requirements and architecture of the Universal Windows driver for GNSS (UMDF 2.0) for the converged Windows Location stack in Windows 10.
ms.assetid: FD8503DC-A43F-43B2-A1E9-D80778E326F9
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# GNSS driver design guide for Windows 10


This guide describes the design and architecture of the Universal Windows driver for GNSS (UMDF 2.0) for the converged Windows Location stack in Windows 10.

## In this section


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
<td><p>[GNSS driver overview](gnss-driver-overview.md)</p></td>
<td><p>Use the GNSS driver design guide to learn how to implement the <strong>DeviceIoControl</strong> APIs with the GNSS driver so that a high level operating system component (HLOS) like the GNSS adapter can access the desired GNSS functionality.</p></td>
</tr>
<tr class="even">
<td><p>[GNSS driver requirements](gnss-driver-requirements.md)</p></td>
<td><p>Describes requirements, assumptions, and constraints to consider when developing a GNSS driver for Windows 10.</p></td>
</tr>
<tr class="odd">
<td><p>[GNSS driver architecture](gnss-driver-architecture.md)</p></td>
<td><p>Provides an overview of GNSS UMDF 2.0 driver architecture, I/O considerations, and discusses several types of tracking and fix sessions.</p></td>
</tr>
<tr class="even">
<td><p>[GNSS driver design](gnss-driver-design.md)</p></td>
<td><p>Discusses design principles to consider when developing a GNSS driver for Windows 10 including data structures, error reporting, and driver versioning.</p></td>
</tr>
</tbody>
</table>

 

 

 




