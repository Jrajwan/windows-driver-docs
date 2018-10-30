---
title: KSPROPERTY\_CAMERACONTROL\_EXTENDED\_OPTIMIZATIONHINT
description: Camera drivers may optimize their capture operation based on hints provided by the application. This property informs the driver to set its performance strategy based on what operation is likely used the most.
ms.assetid: FEA3D355-B490-4E67-905D-EE5507E91150
keywords: ["KSPROPERTY_CAMERACONTROL_EXTENDED_OPTIMIZATIONHINT Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_CAMERACONTROL_EXTENDED_OPTIMIZATIONHINT
api_location:
- Ksmedia.h
api_type:
- HeaderDef
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# KSPROPERTY\_CAMERACONTROL\_EXTENDED\_OPTIMIZATIONHINT


Camera drivers may optimize their capture operation based on hints provided by the application. This property informs the driver to set its performance strategy based on what operation is likely used the most. For example, when optimized for photo, the camera driver may program the sensor to optimize sensor exposure speed and resolution for lower latency from photo capture trigger to image capture. Similarly, when optimized for video, the camera driver may program the sensor for higher frame rate but at a lower resolution.

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
<td><p>Filter</p></td>
<td><p>[<strong>KSPROPERTY</strong>](https://msdn.microsoft.com/library/windows/hardware/ff564262)</p></td>
<td><p>[<strong>KSCAMERA_EXTENDEDPROP_HEADER</strong>](https://msdn.microsoft.com/library/windows/hardware/dn567563)</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) contains a [**KSCAMERA\_EXTENDEDPROP\_HEADER**](https://msdn.microsoft.com/library/windows/hardware/dn567563) structure and a [**KSCAMERA\_EXTENDEDPROP\_VALUE**](https://msdn.microsoft.com/library/windows/hardware/dn567564) structure.

The total property data size is **sizeof**(KSCAMERA\_EXTENDEDPROP\_HEADER) + **sizeof**(KSCAMERA\_EXTENDEDPROP\_VALUE). The **Size** member of [**KSCAMERA\_EXTENDEDPROP\_HEADER**](https://msdn.microsoft.com/library/windows/hardware/dn567563) is set to this total property data size.

The **Capability** member of [**KSCAMERA\_EXTENDEDPROP\_HEADER**](https://msdn.microsoft.com/library/windows/hardware/dn567563) contains a bitwise OR combination of one or more of the following optimization hints.

| Optimization hint                           | Description                               |
|---------------------------------------------|-------------------------------------------|
| KSCAMERA\_EXTENDEDPROP\_OPTIMIZATION\_PHOTO | Camera operation is optimized for photos. |
| KSCAMERA\_EXTENDEDPROP\_OPTIMIZATION\_VIDEO | Camera operation is optimized for video.  |

 

The **Flags** member of [**KSCAMERA\_EXTENDEDPROP\_HEADER**](https://msdn.microsoft.com/library/windows/hardware/dn567563) contains the optimization currently set for the camera (one value).

The default optimization type is KSCAMERA\_EXTENDEDPROP\_OPTIMIZATION\_PHOTO. If this property is supported by the camera driver, then both optimization types must be supported.

This property control is synchronous.

Remarks
-------

### <span id="Optimization_modes"></span><span id="optimization_modes"></span><span id="OPTIMIZATION_MODES"></span>Optimization modes

<span id="KSCAMERA_EXTENDEDPROP_OPTIMIZATION_PHOTO"></span><span id="kscamera_extendedprop_optimization_photo"></span>KSCAMERA\_EXTENDEDPROP\_OPTIMIZATION\_PHOTO  
All camera drivers must be in this mode until explicitly informed to use the KSCAMERA\_EXTENDEDPROP\_OPTIMIZATION\_VIDEO mode. The purpose of this mode is to optimize the camera hardware for photo operations. Video operations must still be functional in this mode.

<span id="KSCAMERA_EXTENDEDPROP_OPTIMIZATION_VIDEO"></span><span id="kscamera_extendedprop_optimization_video"></span>KSCAMERA\_EXTENDEDPROP\_OPTIMIZATION\_VIDEO  
This mode indicates that the camera will likely be used for video operations. The camera driver should optimize the hardware for video operations for this mode. Photo operations must be functional, but there resource usage priority is for video operations.

### <span id="Getting_the_property"></span><span id="getting_the_property"></span><span id="GETTING_THE_PROPERTY"></span>Getting the property

When responding to a KSPROPERTY\_TYPE\_GET request, the driver sets the members of the [**KSCAMERA\_EXTENDEDPROP\_HEADER**](https://msdn.microsoft.com/library/windows/hardware/dn567563) to the following.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Member</th>
<th>Value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Version</td>
<td>1</td>
</tr>
<tr class="even">
<td>PinId</td>
<td>KSCAMERA_EXTENDEDPROP_FILTERSCOPE (0xFFFFFFFF).</td>
</tr>
<tr class="odd">
<td>Size</td>
<td><p>sizeof(KSCAMERA_EXTENDEDPROP_HEADER) + sizeof(KSCAMERA_EXTENDEDPROP_VALUE)</p></td>
</tr>
<tr class="even">
<td>Result</td>
<td>0</td>
</tr>
<tr class="odd">
<td>Capability</td>
<td>Optimization values supported.</td>
</tr>
<tr class="even">
<td>Flags</td>
<td>The current optimization value setting.</td>
</tr>
</tbody>
</table>

 

If no optimization mode was previously set, then the driver sets **Flags** to KSCAMERA\_EXTENDEDPROP\_OPTIMIZATION\_PHOTO (default).

### <span id="Setting_the_property"></span><span id="setting_the_property"></span><span id="SETTING_THE_PROPERTY"></span>Setting the property

When the property is set, a KSPROPERTY\_TYPE\_SET request, the **Flags** member of [**KSCAMERA\_EXTENDEDPROP\_HEADER**](https://msdn.microsoft.com/library/windows/hardware/dn567563) will contain the optomization mode to set.

Requirements
------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Version</p></td>
<td><p>Available starting with Windows 8.1.</p></td>
</tr>
<tr class="even">
<td><p>Header</p></td>
<td>Ksmedia.h (include Ksmedia.h)</td>
</tr>
</tbody>
</table>

## <span id="see_also"></span>See also


[**KSCAMERA\_EXTENDEDPROP\_HEADER**](https://msdn.microsoft.com/library/windows/hardware/dn567563)

[**KSCAMERA\_EXTENDEDPROP\_VALUE**](https://msdn.microsoft.com/library/windows/hardware/dn567564)

 

 






