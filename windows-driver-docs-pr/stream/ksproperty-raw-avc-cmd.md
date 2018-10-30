---
title: KSPROPERTY\_RAW\_AVC\_CMD
description: The KSPROPERTY\_RAW\_AVC\_CMD property issues a raw AV/C command. Raw AV/C commands are supported only for IEEE 1394 bus devices.
ms.assetid: f3ff3815-0f4f-4fcb-89bd-e77d8002813c
keywords: ["KSPROPERTY_RAW_AVC_CMD Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_RAW_AVC_CMD
api_location:
- ksmedia.h
api_type:
- HeaderDef
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# KSPROPERTY\_RAW\_AVC\_CMD


The KSPROPERTY\_RAW\_AVC\_CMD property issues a raw AV/C command. Raw AV/C commands are supported only for IEEE 1394 bus devices.

## <span id="ddk_ksproperty_extxport_raw_avc_cmd_ks"></span><span id="DDK_KSPROPERTY_EXTXPORT_RAW_AVC_CMD_KS"></span>


### <span id="Usage_Summary_Table"></span><span id="usage_summary_table"></span><span id="USAGE_SUMMARY_TABLE"></span>Usage Summary Table

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th>Get</th>
<th>Set</th>
<th>Target</th>
<th>Property descriptor type</th>
<th>Property value type</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Device</p></td>
<td><p>[<strong>KSPROPERTY_EXTXPORT_S</strong>](https://msdn.microsoft.com/library/windows/hardware/ff565167)</p></td>
<td><p>Embedded <strong>RawAVC</strong> structure</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) is the embedded **RawAVC** member of the KSPROPERTY\_EXTXPORT\_S structure that describes the raw AV/C command to run.

Remarks
-------

This property can only be used with devices that can support AV/C commands and where [**KSPROPERTY\_EXTDEVICE\_PORT**](ksproperty-extdevice-port.md) returns DEV\_PORT\_1394 in the **DevPort** member of the [**KSPROPERTY\_EXTDEVICE\_S**](https://msdn.microsoft.com/library/windows/hardware/ff565156) structure.

Driver developers for IEEE 1394 devices may optionally support this property in their drivers in order to extend the device transport controls that are not supported by standard interfaces (such as the user-mode **IAMExtTransport** COM interface methods **put\_Mode** and **get\_Mode**).

It is not necessary to implement support for this property on USB devices because the [USB Video Class Driver](https://msdn.microsoft.com/library/windows/hardware/ff568649) provides this functionality. Normally applications can use the **IKsControl** COM interface to control an IEEE 1394 device. However, the **IKsControl** COM interface does not provide a standard method to support tape seek that is portable across USB and IEEE 1394 buses. Therefore, to perform a tape seek a caller must use the **DeviceIoControl** function instead of the **IKsControl** COM interface. Callers perform a tape seek on 1394 AV/C devices by using a raw AV/C command with an absolute track number (ATN) or time code to seek to. This is a primary reason why this property does not apply to USB devices.

See the [Digital Video Application Compatibility](http://go.microsoft.com/fwlink/p/?linkid=32135) white paper for more information about the differences between tape location searches on USB and 1394 devices.

Requirements
------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Header</p></td>
<td>Ksmedia.h (include Ksmedia.h)</td>
</tr>
</tbody>
</table>

## <span id="see_also"></span>See also


[**KSPROPERTY**](https://msdn.microsoft.com/library/windows/hardware/ff564262)

[**KSPROPERTY\_EXTXPORT\_S**](https://msdn.microsoft.com/library/windows/hardware/ff565167)

 

 






