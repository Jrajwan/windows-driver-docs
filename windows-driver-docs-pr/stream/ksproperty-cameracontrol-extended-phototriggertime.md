---
title: KSPROPERTY\_CAMERACONTROL\_EXTENDED\_PHOTOTRIGGERTIME
description: This property controls the trigger time for the camera driver. The trigger time is used in determining a reference frame for a photo sequence.
ms.assetid: C0DE5F4D-9566-4D8C-9061-D397577E89E2
keywords: ["KSPROPERTY_CAMERACONTROL_EXTENDED_PHOTOTRIGGERTIME Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_CAMERACONTROL_EXTENDED_PHOTOTRIGGERTIME
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

# KSPROPERTY\_CAMERACONTROL\_EXTENDED\_PHOTOTRIGGERTIME


This property controls the trigger time for the camera driver. The trigger time is used in determining a reference frame for a photo sequence.

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
<td><p>Pin</p></td>
<td><p>[<strong>KSPROPERTY</strong>](https://msdn.microsoft.com/library/windows/hardware/ff564262)</p></td>
<td><p>[<strong>KSCAMERA_EXTENDEDPROP_HEADER</strong>](https://msdn.microsoft.com/library/windows/hardware/dn567563)</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) contains a [**KSCAMERA\_EXTENDEDPROP\_HEADER**](https://msdn.microsoft.com/library/windows/hardware/dn567563) structure and a [**KSCAMERA\_EXTENDEDPROP\_VALUE**](https://msdn.microsoft.com/library/windows/hardware/dn567564) structure. The photo trigger time, in 100 nanosecond units, is set or returned as value in **KSCAMERA\_EXTENDEDPROP\_VALUE**.

The total property data size is **sizeof**(KSCAMERA\_EXTENDEDPROP\_HEADER) + **sizeof**(KSCAMERA\_EXTENDEDPROP\_VALUE). The **Size** member of [**KSCAMERA\_EXTENDEDPROP\_HEADER**](https://msdn.microsoft.com/library/windows/hardware/dn567563) is set to this total property data size.

The trigger time is set or cleared using the one of the following flags in the **Flags** member of [**KSCAMERA\_EXTENDEDPROP\_HEADER**](https://msdn.microsoft.com/library/windows/hardware/dn567563).

| Trigger time flag                           | Description                     |
|---------------------------------------------|---------------------------------|
| KSPROPERTY\_CAMERA\_PHOTOTRIGGERTIME\_CLEAR | Clear the trigger time setting. |
| KSPROPERTY\_CAMERA\_PHOTOTRIGGERTIME\_SET   | Set a new trigger time value.   |

 

This property control is synchronous.

Remarks
-------

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
<td>The pin ID for the photo pin.</td>
</tr>
<tr class="odd">
<td>Size</td>
<td><p>sizeof(KSCAMERA_EXTENDEDPROP_HEADER) +</p>
<p>sizeof(KSCAMERA_EXTENDEDPROP_VALUE)</p></td>
</tr>
<tr class="even">
<td>Result</td>
<td><p>An error value resulting from the attempt to read the max frame rate.</p>
<p>Otherwise, 0.</p></td>
</tr>
<tr class="odd">
<td>Capability</td>
<td>0</td>
</tr>
<tr class="even">
<td>Flags</td>
<td>Set or Clear flag</td>
</tr>
</tbody>
</table>

 

If the trigger time is not currently set to any time value, the **Flags** member of [**KSCAMERA\_EXTENDEDPROP\_HEADER**](https://msdn.microsoft.com/library/windows/hardware/dn567563) must contain KSPROPERTY\_CAMERA\_PHOTOTRIGGERTIME\_CLEAR value.

### <span id="Setting_the_Property"></span><span id="setting_the_property"></span><span id="SETTING_THE_PROPERTY"></span>Setting the Property

When the property is set, the **ull** member of [**KSCAMERA\_EXTENDEDPROP\_VALUE**](https://msdn.microsoft.com/library/windows/hardware/dn567565) will contain the trigger time value. The trigger time is set or cleared based on the operation flag. When the flag is KSPROPERTY\_CAMERA\_PHOTOTRIGGERTIME\_CLEAR the value in **KSCAMERA\_EXTENDEDPROP\_VALUE** is not used and is ignored.

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

 

 





