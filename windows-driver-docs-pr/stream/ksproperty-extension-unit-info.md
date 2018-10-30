---
title: KSPROPERTY\_EXTENSION\_UNIT\_INFO
description: The KSPROPERTY\_EXTENSION\_UNIT\_INFO property retrieves the guidExtensionCode, bNumControls, bNrInPins, and baSourceID members of the Extension Unit Descriptor.
ms.assetid: a7a2f655-8df7-4260-883f-53d6f5a7c6f3
keywords: ["KSPROPERTY_EXTENSION_UNIT_INFO Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_EXTENSION_UNIT_INFO
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

# KSPROPERTY\_EXTENSION\_UNIT\_INFO


The KSPROPERTY\_EXTENSION\_UNIT\_INFO property retrieves the guidExtensionCode, bNumControls, bNrInPins, and baSourceID members of the Extension Unit Descriptor.

## <span id="ddk_ksproperty_extension_unit_info_ks"></span><span id="DDK_KSPROPERTY_EXTENSION_UNIT_INFO_KS"></span>


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
<td><p>No</p></td>
<td><p>Filter node</p></td>
<td><p>[<strong>KSP_NODE</strong>](https://msdn.microsoft.com/library/windows/hardware/ff566720)</p></td>
<td><p>PVOID</p></td>
</tr>
</tbody>
</table>

 

Remarks
-------

This property is available in Windows Vista and later, and the SDK for Microsoft DirectX 9.2 or later versions.

During device startup, the system-supplied USB Video Class driver (*Usbvideo.sys*) caches information from the device's extension unit descriptor. *Usbvideo.sys* then uses this cached information to respond to KSPROPERTY\_EXTENSION\_UNIT\_INFO.

Therefore, the fields returned by this property are identical to those provided by the device in the extension unit descriptor. For an example of such a descriptor, see [Sample Extension Unit Descriptor](https://msdn.microsoft.com/library/windows/hardware/ff568133).

Specifically, KSPROPERTY\_EXTENSION\_UNIT\_INFO returns the extension unit GUID followed by the data fields from the descriptor as shown in the following table.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>bNumControls</p></td>
<td><p>Number of controls in this extension unit.</p></td>
</tr>
<tr class="even">
<td><p>bNrInPins</p></td>
<td><p>Number of input pins in the extension unit.</p></td>
</tr>
<tr class="odd">
<td><p>baSourceID(n)</p></td>
<td><p>Identifier of the unit or terminal to which pin <em>n</em> of this extension unit is connected. This is a hardware identifier and not a DirectShow identifier.</p></td>
</tr>
</tbody>
</table>

 

The following code example shows how to submit KSPROPERTY\_EXTENSION\_UNIT\_INFO, taken from the complete sample shown in [Sample Extension Unit Plug-in DLL](https://msdn.microsoft.com/library/windows/hardware/ff568134):

```
ExtensionProp.Property.Set = PROPSETID_VIDCAP_EXTENSION_UNIT;
    ExtensionProp.Property.Id = KSPROPERTY_EXTENSION_UNIT_INFO;
    ExtensionProp.Property.Flags = KSPROPERTY_TYPE_GET | 
                                   KSPROPERTY_TYPE_TOPOLOGY;
    ExtensionProp.NodeId = m_dwNodeId;

    hr = m_pKsControl->KsProperty(
        (PKSPROPERTY) &amp;ExtensionProp,
        sizeof(ExtensionProp),
        NULL,
        0,
        &amp;ulBytesReturned);
```

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
<td><p>Available in Windows Vista and later versions of the operating system,and the SDK for Microsoft DirectX 9.2 or later versions.</p></td>
</tr>
<tr class="even">
<td><p>Header</p></td>
<td>Ksmedia.h (include Ksmedia.h)</td>
</tr>
</tbody>
</table>

 

 





