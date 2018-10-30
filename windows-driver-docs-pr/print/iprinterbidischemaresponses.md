---
title: IPrinterBidiSchemaResponses interface
author: windows-driver-content
description: The IPrinterBidiSchemaResponses interface represents a set of bidi responses populated by USB Bidi Extension JavaScript methods getSchemas and getStatus.
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: 2E68C4AA-D235-46D2-81D6-D6C7E84C2FEF
keywords: ["IPrinterBidiSchemaResponses interface Print Devices", "IPrinterBidiSchemaResponses interface Print Devices , described"]
topic_type:
- apiref
api_name:
- IPrinterBidiSchemaResponses
api_type:
- COM
ms.localizationpriority: medium
---

# IPrinterBidiSchemaResponses interface


The IPrinterBidiSchemaResponses interface represents a set of bidi responses populated by USB Bidi Extension JavaScript methods **getSchemas** and **getStatus**.

Members
-------

The **IPrinterBidiSchemaResponses** interface inherits from the [**IUnknown**](https://msdn.microsoft.com/library/windows/desktop/ms680509) interface. **IPrinterBidiSchemaResponses** also has these types of members:

-   [Methods](#methods)

### <span id="methods"></span>Methods

The **IPrinterBidiSchemaResponses** interface has these methods.

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
<td>[<strong>AddBool</strong>](iprinterbidischemaresponses--addbool.md)</td>
<td><p>The AddBool method adds a new response of type BIDI_BOOL to the collection.</p></td>
</tr>
<tr class="even">
<td>[<strong>AddInt32</strong>](iprinterbidischemaresponses--addint32.md)</td>
<td><p>The AddInt32 method adds a new response of type BIDI_INT to the collection.</p></td>
</tr>
<tr class="odd">
<td>[<strong>AddBlob</strong>](iprinterbidischemaresponses-addblob.md)</td>
<td><p>The AddBlob method adds a new response of type BIDI_BLOB to the collection.</p></td>
</tr>
<tr class="even">
<td>[<strong>AddEnum</strong>](iprinterbidischemaresponses-addenum.md)</td>
<td><p>The AddEnum method adds a new response of type BIDI_ENUM to the collection.</p></td>
</tr>
<tr class="odd">
<td>[<strong>AddFloat</strong>](iprinterbidischemaresponses-addfloat.md)</td>
<td><p>The AddFloat method adds a new response of type BIDI_FLOAT to the collection.</p></td>
</tr>
<tr class="even">
<td>[<strong>AddNull</strong>](iprinterbidischemaresponses-addnull.md)</td>
<td><p>The AddNull method adds a new response of type BIDI_NULL to the collection.</p></td>
</tr>
<tr class="odd">
<td>[<strong>AddRequeryKey</strong>](iprinterbidischemaresponses-addrequerykey.md)</td>
<td><p>The AddRequeryKey method adds a new QueryKey to re-query upon return from the getSchemas call.</p></td>
</tr>
<tr class="even">
<td>[<strong>AddString</strong>](iprinterbidischemaresponses-addstring.md)</td>
<td><p>The AddString method adds a new response of type BIDI_STRING to the collection.</p></td>
</tr>
<tr class="odd">
<td>[<strong>AddText</strong>](iprinterbidischemaresponses-addtext.md)</td>
<td><p>The AddText method adds a new response of type BIDI_TEXT to the collection.</p></td>
</tr>
</tbody>
</table>

 

 

 




