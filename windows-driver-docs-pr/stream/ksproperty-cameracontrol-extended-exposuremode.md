---
title: KSPROPERTY\_CAMERACONTROL\_EXTENDED\_EXPOSUREMODE
description: The exposure control property specifies the whether auto processing occurs for exposure or a manual time value is used instead.
ms.assetid: 54D4F286-09F2-48B5-9A7A-9445999972BD
keywords: ["KSPROPERTY_CAMERACONTROL_EXTENDED_EXPOSUREMODE Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_CAMERACONTROL_EXTENDED_EXPOSUREMODE
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

# KSPROPERTY\_CAMERACONTROL\_EXTENDED\_EXPOSUREMODE


The exposure control property specifies the whether auto processing occurs for exposure or a manual time value is used instead.

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

 

The property value (operation data) contains a [**KSCAMERA\_EXTENDEDPROP\_HEADER**](https://msdn.microsoft.com/library/windows/hardware/dn567563) structure and a [**KSCAMERA\_EXTENDEDPROP\_VIDEOPROCSETTING**](https://msdn.microsoft.com/library/windows/hardware/dn567566) structure.

The total property data size is **sizeof**(KSCAMERA\_EXTENDEDPROP\_HEADER) + **sizeof**(KSCAMERA\_EXTENDEDPROP\_VIDEOPROCSETTING). The **Size** member of [**KSCAMERA\_EXTENDEDPROP\_HEADER**](https://msdn.microsoft.com/library/windows/hardware/dn567563) is set to this total property data size.

The **Capability** member of [**KSCAMERA\_EXTENDEDPROP\_HEADER**](https://msdn.microsoft.com/library/windows/hardware/dn567563) contains a bitwise OR combination of one or more of the following video processing options.

| Processing mode                               | Description                                                                  |
|-----------------------------------------------|------------------------------------------------------------------------------|
| KSCAMERA\_EXTENDEDPROP\_VIDEOPROCFLAG\_AUTO   | Camera driver uses its own processing logic for video.                       |
| KSCAMERA\_EXTENDEDPROP\_VIDEOPROCFLAG\_MANUAL | Camera driver uses a preset processing method or a temperature based method. |
| KSCAMERA\_EXTENDEDPROP\_VIDEOPROCFLAG\_LOCK   | The current video processing method is locked.                               |

 

The **Flags** member of [**KSCAMERA\_EXTENDEDPROP\_HEADER**](https://msdn.microsoft.com/library/windows/hardware/dn567563) contains the video processing flag currently set for the camera. The KSCAMERA\_EXTENDEDPROP\_VIDEOPROCFLAG\_AUTO setting may be combined with KSCAMERA\_EXTENDEDPROP\_VIDEOPROCFLAG\_LOCK.

This property control is asynchronous and cancelable.

Remarks
-------

### <span id="Processing_modes"></span><span id="processing_modes"></span><span id="PROCESSING_MODES"></span>Processing modes

<span id="KSCAMERA_EXTENDEDPROP_VIDEOPROCFLAG_AUTO"></span><span id="kscamera_extendedprop_videoprocflag_auto"></span>KSCAMERA\_EXTENDEDPROP\_VIDEOPROCFLAG\_AUTO  
This indicates that auto processing is supported. The driver will use its internal logic to optimize the video processing. For a KSPROPERTY\_TYPE\_GET request, the **VideoProc** member of [**KSCAMERA\_EXTENDEDPROP\_VIDEOPROCSETTING**](https://msdn.microsoft.com/library/windows/hardware/dn567566) must contain the current driver determined value for the video processing.

This flag may be combined with KSCAMERA\_EXTENDEDPROP\_VIDEOPROCFLAG\_LOCK as a bitwise OR value. When locked, the expected behavior of the camera driver is to converge on white balance and lock the white balance value to the converged value, not attempting to auto-white balance again, until a new white balance command is received.

Locking, without combining Auto mode, an already locked control should be treated as a no-op by the camera driver. Locking, in combination with Auto mode, an already locked control should trigger a new convergence.

This flag must not be combined with KSCAMERA\_EXTENDEDPROP\_VIDEOPROCFLAG\_MANUAL.

<span id="KSCAMERA_EXTENDEDPROP_VIDEOPROCFLAG_MANUAL"></span><span id="kscamera_extendedprop_videoprocflag_manual"></span>KSCAMERA\_EXTENDEDPROP\_VIDEOPROCFLAG\_MANUAL  
Manual indicates that for this video processing, the specific values are provided. Specific values are provided to the driver.

This flag must not be combined with KSCAMERA\_EXTENDEDPROP\_VIDEOPROCFLAG\_AUTO or KSCAMERA\_EXTENDEDPROP\_VIDEOPROCFLAG\_LOCK.

<span id="KSCAMERA_EXTENDEDPROP_VIDEOPROCFLAG_LOCK"></span><span id="kscamera_extendedprop_videoprocflag_lock"></span>KSCAMERA\_EXTENDEDPROP\_VIDEOPROCFLAG\_LOCK  
The lock option flag indicates that the current video processing is locked to whatever value is currently programmed. For example, an application may request auto mode until a specific exposure is determined. At that point the application will decide to take a sequence of photos all with the same exposure. In such a case, the application may specify the KSCAMERA\_EXTENDEDPROP\_VIDEOPROCFLAG\_LOCK flag. The camera driver will ensure the white balance information does not change across the different photos.

This flag must not be combined with KSCAMERA\_EXTENDEDPROP\_VIDEOPROCFLAG\_MANUAL.

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
<td><p>sizeof(KSCAMERA_EXTENDEDPROP_HEADER) + sizeof(KSCAMERA_EXTENDEDPROP_VIDEOPROCSETTING)</p></td>
</tr>
<tr class="even">
<td>Result</td>
<td>0</td>
</tr>
<tr class="odd">
<td>Capability</td>
<td>KSCAMERA_EXTENDEDPROP_CAPS_ASYNCCONTROL | (Video processing mode supported)</td>
</tr>
<tr class="even">
<td>Flags</td>
<td>The current video processing mode.</td>
</tr>
</tbody>
</table>

 

If no exposure mode was previously set, then the driver sets **Flags** to KSCAMERA\_EXTENDEDPROP\_VIDEOPROCFLAG\_AUTO (default). The members of the [**KSCAMERA\_EXTENDEDPROP\_VIDEOPROCSETTING**](https://msdn.microsoft.com/library/windows/hardware/dn567566) structure that follows [**KSCAMERA\_EXTENDEDPROP\_HEADER**](https://msdn.microsoft.com/library/windows/hardware/dn567563) are set according to the requirements of the processing mode.

The **VideoProp.Value.ull** value must contain the current exposure setting when the mode is KSCAMERA\_EXTENDEDPROP\_VIDEOPROCFLAG\_AUTO.

### <span id="Setting_the_property"></span><span id="setting_the_property"></span><span id="SETTING_THE_PROPERTY"></span>Setting the property

When the property is set, a KSPROPERTY\_TYPE\_SET request, the **Flags** member of [**KSCAMERA\_EXTENDEDPROP\_HEADER**](https://msdn.microsoft.com/library/windows/hardware/dn567563) will contain the exposure mode to set. The **VideoProc.Value** member of [**KSCAMERA\_EXTENDEDPROP\_VIDEOPROCSETTING**](https://msdn.microsoft.com/library/windows/hardware/dn567566) must be ignored when **Flags** contains the KSCAMERA\_EXTENDEDPROP\_VIDEOPROCFLAG\_AUTO mode flag.

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

[**KSCAMERA\_EXTENDEDPROP\_VIDEOPROCSETTING**](https://msdn.microsoft.com/library/windows/hardware/dn567566)

[**KSPROPERTY\_CAMERACONTROL\_EXTENDED\_WHITEBALANCEMODE**](ksproperty-cameracontrol-extended-whitebalancemode.md)

 

 






