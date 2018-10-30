---
title: Option Attributes for the ColorMode Feature
author: windows-driver-content
description: Option Attributes for the ColorMode Feature
ms.assetid: e6f68a50-f044-406e-b92c-8449d126bceb
keywords:
- ColorMode Feature
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Option Attributes for the ColorMode Feature





The following table lists the attributes associated with the ColorMode feature. For more information about the ColorMode feature, see [Standard Features](standard-features.md).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribute Name</th>
<th>Attribute Parameter</th>
<th>Comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>*<strong>Color?</strong></p></td>
<td><p><strong>TRUE</strong> or <strong>FALSE</strong>, indicating whether the option produces color.</p></td>
<td><p>Optional. If not specified, the default value is <strong>TRUE</strong> for *<strong>DrvBPP</strong> &gt; 1. To create gray scaling, set to <strong>FALSE</strong> with *<strong>DrvBPP</strong> &gt; 1.</p></td>
</tr>
<tr class="even">
<td><p>*<strong>ColorPlaneOrder</strong></p></td>
<td><p>LIST indicating the order in which Unidrv should send color plane data.</p>
<p>Examples:</p>
LIST (YELLOW, MAGENTA, CYAN, BLACK)
LIST (RED, GREEN, BLUE)
<p>Colors can be repeated in the list.</p></td>
<td><p>Required if *<strong>DevNumOfPlanes</strong> is greater than 1. The number of colors specified must equal *<strong>DevNumOfPlanes</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>*<strong>DevBPP</strong></p></td>
<td><p>Numeric value indicating the number of bits per pixel of color data supported by the printer.</p></td>
<td><p>Optional. If not specified, the default value is 1.</p></td>
</tr>
<tr class="even">
<td><p>*<strong>DevNumOfPlanes</strong></p></td>
<td><p>Numeric value indicating the number of color planes supported by the printer.</p></td>
<td><p>Optional. If not specified, the default value is 1. (For color printers, a value of 1 is referred to as pixel mode.)</p></td>
</tr>
<tr class="odd">
<td><p>*<strong>DrvBPP</strong></p></td>
<td><p>Numeric value indicating the number of bits per pixel that Unidrv should use for its bitmap rendering buffer. The bitmap format is a Windows [<em>device-independent bitmap (DIB)</em>](https://msdn.microsoft.com/library/windows/hardware/ff556277#wdkgloss-device-independent-bitmap--dib-), and valid values are 1, 4, 8, 16, 24, or 32.</p></td>
<td><p>Optional. If not specified, the default value is 1. (For color printers, a value of 1 is referred to as &quot;planar mode&quot;.)</p>
<p>Windows DIBs always use one color plane.</p></td>
</tr>
<tr class="even">
<td><p>*<strong>IPCallbackID</strong></p></td>
<td><p>Positive numeric value, passed to the rendering plug-in's [<strong>IPrintOemUni::ImageProcessing</strong>](https://msdn.microsoft.com/library/windows/hardware/ff554261) method as its <strong>IPCallbackID</strong> argument.</p></td>
<td><p>Required if a [rendering plug-in](rendering-plug-ins.md) is supplied that contains an <strong>IPrintOemUni::ImageProcessing</strong> method.</p></td>
</tr>
<tr class="odd">
<td><p>*<strong>PaletteProgrammable?</strong></p></td>
<td><p><strong>TRUE</strong> or <strong>FALSE</strong>, indicating whether the color palette is programmable.</p></td>
<td><p>Optional. If not specified, the default value is <strong>FALSE</strong>.</p></td>
</tr>
<tr class="even">
<td><p>*<strong>PaletteSize</strong></p></td>
<td><p>Numeric value representing the number of entries in the color palette used with the specified option.</p></td>
<td><p>Optional. If not specified, the default value is 2.</p></td>
</tr>
<tr class="odd">
<td><p>*<strong>RasterMode</strong></p></td>
<td><p>DIRECT or INDEXED, indicating whether the raster data is sent directly to the printer or is indexed through a color palette.</p></td>
<td><p>Optional. If not specified, the default value is INDEXED.</p></td>
</tr>
</tbody>
</table>

 

For examples, see the [sample GPD files](sample-gpd-files.md).

For information about additional option attributes, see [Option Attributes for All Features](option-attributes-for-all-features.md).

Also see [Controlling Image Quality](controlling-image-quality.md).

 

 




