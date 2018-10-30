---
title: KSPROPERTY\_VPCONFIG\_SETCONNECTINFO
description: The KSPROPERTY\_VPCONFIG\_SETCONNECTINFO property sets the video port configuration with user-defined connection information. It is a pointer to an array of DDVIDEOPORTCONNECT structures as returned by the KSPROPERTY\_VPCONFIG\_GETCONNECTINFO property.
ms.assetid: 120f6889-cd67-4c05-b4b8-adab3efd7f2c
keywords: ["KSPROPERTY_VPCONFIG_SETCONNECTINFO Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_VPCONFIG_SETCONNECTINFO
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

# KSPROPERTY\_VPCONFIG\_SETCONNECTINFO


The KSPROPERTY\_VPCONFIG\_SETCONNECTINFO property sets the video port configuration with user-defined connection information. It is a pointer to an array of [**DDVIDEOPORTCONNECT**](https://msdn.microsoft.com/library/windows/hardware/ff550388) structures as returned by the KSPROPERTY\_VPCONFIG\_GETCONNECTINFO property.

## <span id="ddk_ksproperty_vpconfig_setconnectinfo_ks"></span><span id="DDK_KSPROPERTY_VPCONFIG_SETCONNECTINFO_KS"></span>


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
<td><p>No</p></td>
<td><p>Yes</p></td>
<td><p>Pin</p></td>
<td><p>[<strong>KSPROPERTY</strong>](https://msdn.microsoft.com/library/windows/hardware/ff564262)</p></td>
<td><p>[<strong>DDVIDEOPORTCONNECT</strong>](https://msdn.microsoft.com/library/windows/hardware/ff550388)</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) is a DDVIDEOPORTCONNECT structure that describes the configuration of a video port connection.

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


[**DDVIDEOPORTCONNECT**](https://msdn.microsoft.com/library/windows/hardware/ff550388)

[**KSPROPERTY\_VPCONFIG\_GETCONNECTINFO**](ksproperty-vpconfig-getconnectinfo.md)

 

 






