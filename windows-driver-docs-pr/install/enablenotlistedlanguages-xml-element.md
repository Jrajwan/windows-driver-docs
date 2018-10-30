---
title: enableNotListedLanguages XML Element
description: The enableNotListedLanguages XML element is an empty element that sets the enableNotListedLanguages flag to ON, which configures DPInst to enable all of the supported languages that are not explicitly enabled by language XML elements in a DPInst.xml file.
ms.assetid: 7584b222-71b0-4532-84be-3444a4a7003b
keywords: ["enableNotListedLanguages XML Element Device and Driver Installation"]
topic_type:
- apiref
api_name:
- enableNotListedLanguages XML Element
api_type:
- NA
ms.localizationpriority: medium
---

# enableNotListedLanguages XML Element


\[DIFx is deprecated, for more info, see [DIFx Guidelines](https://msdn.microsoft.com/windows/hardware/drivers/install/difx-guidelines).\]

The **enableNotListedLanguages** XML element is an empty element that sets the **enableNotListedLanguages** flag to ON, which configures DPInst to enable all of the supported languages that are not explicitly enabled by [**language**](language-xml-element.md) XML elements in a *DPInst.xml* file.

### Element Tag

```
<enableNotListedLanguages>
```

### XML Attributes

None

### Element Information

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Parent elements</strong></p></td>
<td align="left"><p>[<strong>dpinst</strong>](dpinst-xml-element.md)</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Child elements</strong></p></td>
<td align="left"><p>None permitted</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Data contents</strong></p></td>
<td align="left"><p>None permitted</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Duplicate child elements</strong></p></td>
<td align="left"><p>None permitted</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="comments"></a>Remarks

By default, all of the DPInst-supported languages are enabled if a *DPInst.xml* file does not contain any **language** elements. However, if the *DPInst.xml* file contains **language** elements, only the languages that are explicitly specified by the **language** elements are enabled and all of the other languages are implicitly disabled. To enable all of the languages that are implicitly disabled, set the **enableNotListedLanguages** flag to ON by including an **enableNotListedLanguages** element as a child element of a **dpinst** XML element or use the **/el** command-line switch.

The following code example demonstrates an **enableNotListedLanguages** element.

```
<dpinst>
  ...
  <enableNotListedLanguages/>
  ...
</dpinst>
```

## See also


[**dpinst**](dpinst-xml-element.md)

 

 






