---
title: MetadataBuilderInformation
description: MetadataBuilderInformation
ms.assetid: 94403994-2165-405e-bfa0-974af8e241fe
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# MetadataBuilderInformation

[!include[MBAE deprecation warning](mbae-deprecation-warning.md)]

The MetadataBuilderInformation element specifies information about the application that created the device metadata package.

## <span id="Usage"></span><span id="usage"></span><span id="USAGE"></span>Usage


``` syntax
<MetadataBuilderInformation>
  text
  child elements
</MetadataBuilderInformation>
```

## <span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes


There are no attributes.

## <span id="Text_value"></span><span id="text_value"></span><span id="TEXT_VALUE"></span>Text value


A string that contains between 1 and 256 printable characters inclusive.

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
<td><p>[Application](application-service-schema.md)</p></td>
<td><p>The [Application](application-service-schema.md) element specifies the name of the application software that created the service metadata package.</p></td>
</tr>
<tr class="even">
<td><p>[Version](version.md)</p></td>
<td><p>The [Version](version.md) element specifies the version of the application software that created the service metadata package.</p></td>
</tr>
</tbody>
</table>

 

## <span id="Parent_elements"></span><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent elements


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
<td><p>[PackageInfo](packageinfo.md)</p></td>
<td><p>The [PackageInfo](packageinfo.md) element is the parent element of the [PackageInfo XML schema](packageinfo-xml-schema.md). The child elements of the PackageInfo element specify the attributes of the device metadata package.</p></td>
</tr>
</tbody>
</table>

 

## <span id="XSD"></span><span id="xsd"></span>XSD


``` syntax
<xs:element name="MetadataBuilderInformation" type="tns:MetadataBuilderInformationType" minOccurs="0" /> 

<xs:complexType name="MetadataBuilderInformationType">
  <xs:sequence>
  <xs:element name="Application" type="tns:ApplicationType" />
  <xs:element name="Version" type="tns:VersionType" />
  <xs:any namespace="##other" processContents="lax" minOccurs="0" maxOccurs="unbounded" />
  </xs:sequence>
</xs:complexType> 

<xs:simpleType name="ApplicationType">
  <xs:restriction base="xs:string">
  <xs:minLength value="1" />
  <xs:maxLength value="256" />
  </xs:restriction>
</xs:simpleType> 

<xs:simpleType name="VersionType">
   <xs:restriction base="xs:string">
     <xs:minLength value="1" />
     <xs:maxLength value="256" />
   </xs:restriction> 
</xs:simpleType>
```

## <span id="Remarks"></span><span id="remarks"></span><span id="REMARKS"></span>Remarks


The MetadataBuilderInformation element is not used by any component of the operating system. It is reserved for use by the OEM, IHV, and ISV.

 

 





