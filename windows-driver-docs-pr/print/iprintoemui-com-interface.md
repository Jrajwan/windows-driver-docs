---
title: IPrintOemUI COM Interface
author: windows-driver-content
description: IPrintOemUI COM Interface
ms.assetid: 7fd4071a-11ce-49e6-9e23-4f0643da1d98
keywords:
- IPrintOemUI
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# IPrintOemUI COM Interface





The `IPrintOemUI` COM interface is the means by which the [printer interface DLL](printer-interface-dll.md) for Unidrv or Pscript5 communicates with a UI plug-in. The `IPrintOemUI` interface is implemented by each UI plug-in.

The following table lists and describes all the methods that the `IPrintOemUI` interface supplies. UI plug-ins must define all listed methods. If a method is not needed, it can simply return E\_NOTIMPL.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Method</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[<strong>IPrintOemUI::CommonUIProp</strong>](https://msdn.microsoft.com/library/windows/hardware/ff554159)</p></td>
<td><p>Enables a UI plug-in to modify an existing printer property sheet page or document property sheet page.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>IPrintOemUI::DeviceCapabilities</strong>](https://msdn.microsoft.com/library/windows/hardware/ff554162)</p></td>
<td><p>Enables a UI plug-in to specify customized device capabilities.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>IPrintOemUI::DevicePropertySheets</strong>](https://msdn.microsoft.com/library/windows/hardware/ff554165)</p></td>
<td><p>Enables a UI plug-in to add a new page to a printer device's printer property sheet.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>IPrintOemUI::DevMode</strong>](https://msdn.microsoft.com/library/windows/hardware/ff554167)</p></td>
<td><p>Performs operations on a UI plug-in's private [<strong>DEVMODEW</strong>](https://msdn.microsoft.com/library/windows/hardware/ff552837) members.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>IPrintOemUI::DevQueryPrintEx</strong>](https://msdn.microsoft.com/library/windows/hardware/ff554172)</p></td>
<td><p>Enables a UI plug-in to help determine if a print job is printable.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>IPrintOemUI::DocumentPropertySheets</strong>](https://msdn.microsoft.com/library/windows/hardware/ff554173)</p></td>
<td><p>Enables a UI plug-in to add a new page to a printer device's document property sheet.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>IPrintOemUI::DriverEvent</strong>](https://msdn.microsoft.com/library/windows/hardware/ff554175)</p></td>
<td><p>Called by the print spooler when processing driver-specific events that might require action by the printer driver.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>IPrintOemUI::FontInstallerDlgProc</strong>](https://msdn.microsoft.com/library/windows/hardware/ff554176)</p></td>
<td><p>Replaces the Unidrv font installer's user interface.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>IPrintOemUI::GetInfo</strong>](https://msdn.microsoft.com/library/windows/hardware/ff554178)</p></td>
<td><p>(Implementation required.) Returns a UI plug-in's identification information.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>IPrintOemUI::PrinterEvent</strong>](https://msdn.microsoft.com/library/windows/hardware/ff554182)</p></td>
<td><p>Enables a UI plug-in to process printer events.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>IPrintOemUI::PublishDriverInterface</strong>](https://msdn.microsoft.com/library/windows/hardware/ff554184)</p></td>
<td><p>(Implementation required.) Supplies a pointer to the Unidrv or Pscript5 driver's [IPrintOemDriverUI COM interface](iprintoemdriverui-com-interface.md), [IPrintCoreUI2 COM interface](iprintcoreui2-com-interface.md), [IPrintCoreHelperPS interface](https://msdn.microsoft.com/library/windows/hardware/ff552906), or [IPrintCoreHelperUni interface](https://msdn.microsoft.com/library/windows/hardware/ff552940).</p></td>
</tr>
<tr class="even">
<td><p>[<strong>IPrintOemUI::QueryColorProfile</strong>](https://msdn.microsoft.com/library/windows/hardware/ff554186)</p></td>
<td><p>Enables a printer interface DLL to specify an ICC profile for color management.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>IPrintOemUI::UpdateExternalFonts</strong>](https://msdn.microsoft.com/library/windows/hardware/ff554188)</p></td>
<td><p>Enables a printer interface DLL to update a printer's [Unidrv font format files](customized-font-management.md#ddk-unidrv-font-format-files-gg).</p></td>
</tr>
<tr class="even">
<td><p>[<strong>IPrintOemUI::UpgradePrinter</strong>](https://msdn.microsoft.com/library/windows/hardware/ff554189)</p></td>
<td><p>Enables a UI plug-in to upgrade device option values that are stored in the registry.</p></td>
</tr>
</tbody>
</table>

 

For more information, see [Implementing Printer Driver COM Interfaces](implementing-printer-driver-com-interfaces.md).

 

 




