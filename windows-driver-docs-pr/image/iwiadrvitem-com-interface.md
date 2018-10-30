---
title: IWiaDrvItem COM Interface
author: windows-driver-content
description: IWiaDrvItem COM Interface
ms.assetid: 1be2265b-7ae8-4935-9559-588b885526d4
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# IWiaDrvItem COM Interface





The [IWiaDrvItem interface](https://msdn.microsoft.com/library/windows/hardware/ff543896) provides methods that a WIA minidriver uses to manage a tree of **IWiaDrvItem** items. These methods allow a WIA minidriver to manipulate **IWiaDrvItem** objects. The **IWiaDrvItem** interface supplies the following methods.

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
<td><p>[<strong>IWiaDrvItem::AddItemToFolder</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543856)</p></td>
<td><p>Adds the <strong>IWiaDrvItem</strong> object to a folder.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>IWiaDrvItem::DumpItemData</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543863)</p></td>
<td><p>Dumps private driver item data.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>IWiaDrvItem::FindChildItemByName</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543867)</p></td>
<td><p>Locates a child item by full item name.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>IWiaDrvItem::FindItemByName</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543870)</p></td>
<td><p>Locates an item by full item name.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>IWiaDrvItem::GetDeviceSpecContext</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543873)</p></td>
<td><p>Retrieves a pointer to a device-specific context.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>IWiaDrvItem::GetFirstChildItem</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543878)</p></td>
<td><p>Returns the first child of this folder item.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>IWiaDrvItem::GetFullItemName</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543881)</p></td>
<td><p>Retrieves full item name and hierarchy information.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>IWiaDrvItem::GetItemFlags</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543883)</p></td>
<td><p>Returns WIA item flags.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>IWiaDrvItem::GetItemName</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543885)</p></td>
<td><p>Retrieves the item name.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>IWiaDrvItem::GetNextSiblingItem</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543889)</p></td>
<td><p>Finds the next sibling of this item.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>IWiaDrvItem::GetParentItem</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543892)</p></td>
<td><p>Retrieves the parent item of this item.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>IWiaDrvItem::RemoveItemFromFolder</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543899)</p></td>
<td><p>Removes an item from parent folder.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>IWiaDrvItem::UnlinkItemTree</strong>](https://msdn.microsoft.com/library/windows/hardware/ff543901)</p></td>
<td><p>Unlinks the driver item tree.</p></td>
</tr>
</tbody>
</table>

 

 

 




