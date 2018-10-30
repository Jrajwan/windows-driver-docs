---
title: PackageInfo
description: PackageInfo
ms.assetid: b74bfc2a-6779-4f53-9e46-71ca8ae26fda
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# PackageInfo

[!include[MBAE deprecation warning](mbae-deprecation-warning.md)]

The PackageInfo element is the parent element of the [PackageInfo XML schema](packageinfo-xml-schema.md). The child elements of the PackageInfo element specify the attributes of the service metadata package.

## <span id="Usage"></span><span id="usage"></span><span id="USAGE"></span>Usage


``` syntax
<PackageInfo>
  child elements
</PackageInfo>
```

## <span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes


There are no attributes.

## <span id="Child_elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child elements


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[MetadataBuilderInformation](metadatabuilderinformation.md)</p></td>
<td><p>The [MetadataBuilderInformation](metadatabuilderinformation.md) element specifies information about the application that created the service metadata package.</p></td>
</tr>
<tr class="even">
<td><p>[MetadataKey](metadatakey.md)</p></td>
<td><p>The [MetadataKey](metadatakey.md) element specifies the attributes of the service metadata package. These include the following:</p>
<ul>
<li><p>The identifier for each hardware function supported by the device.</p></li>
<li><p>The language-specific locale for the text strings within the package.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>[PackageStructure](packagestructure.md)</p></td>
<td><p>The [PackageStructure](packagestructure.md) element specifies the XML schemas which are referenced by the service metadata package.</p></td>
</tr>
<tr class="even">
<td><p>[Relationships](relationships.md)</p></td>
<td><p>The [Relationships](relationships.md) element, through its child elements, specifies data that is used to track a service metadata package within the device metadata cache.</p></td>
</tr>
</tbody>
</table>

 

## <span id="Parent_elements"></span><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent elements


There are no parent elements.

## <span id="XSD"></span><span id="xsd"></span>XSD


``` syntax
<xs:element name="PackageInfo" type="tns:PackageInfoType" />

<xs:complexType name="PackageInfoType">
  <xs:sequence>
    <xs:element name="MetadataKey" type="tns:MetadataKeyType" />
    <xs:element name="PackageStructure" type="tns:PackageStructureType" />
    <xs:element name="Relationships" type="tns:RelationshipsType" minOccurs="0" />
    <xs:element name="MetadataBuilderInformation" type="tns:MetadataBuilderInformationType" minOccurs="0" />
    <xs:any namespace="##other" processContents="lax" minOccurs="0"
      maxOccurs="unbounded" />
  </xs:sequence>
</xs:complexType>
```

## <span id="Remarks"></span><span id="remarks"></span><span id="REMARKS"></span>Remarks


The PackageInfo element must contain one instance of the [MetadataKey](metadatakey.md), [PackageStructure](packagestructure.md), and [Relationships](relationships.md) elements.

 

 





