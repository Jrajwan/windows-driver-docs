---
title: Common Distributed Scan Processing Web Service Operation Error Codes
author: windows-driver-content
description: Common Distributed Scan Processing Web Service Operation Error Codes
ms.assetid: d31898d2-3536-4cc2-8480-c78e952fcdbb
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Common Distributed Scan Processing Web Service Operation Error Codes


This topic lists error codes that are common to all Distributed Scan Processing Web Service operations. If an operation results in multiple errors, the service should return the code that most specifically describes the error. For a general discussion of Distributed Scan Processing Web Service operation errors, see [Distributed Scan Processing Web Service Operation Error Reporting](distributed-scan-processing-web-service-operation-error-reporting.md).

### wsa:ActionNotSupported

The Distributed Scan Processing Web Service host returns this fault when a client requests an operation that the service does not support.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Fault property</th>
<th>Definition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[Code]</p></td>
<td><p>soap:Sender</p></td>
</tr>
<tr class="even">
<td><p>[Subcode]</p></td>
<td><p>wsa:ActionNotSupported</p></td>
</tr>
<tr class="odd">
<td><p>[Reason]</p></td>
<td><p>The [wsa:Action] cannot be processed at the receiver.</p></td>
</tr>
<tr class="even">
<td><p>[Detail]</p></td>
<td><p><em>The invalid operation name</em></p></td>
</tr>
</tbody>
</table>

 

### InvalidArgs

The Distributed Scan Processing Web Service host returns this fault when a client sends an invalid argument as part of an operation. An argument might be invalid for any of the following reasons:

-   There are not enough *in* arguments.

-   There are too many *in* arguments.

-   There is no *in* argument by that name.

-   One or more *in* arguments are of the wrong data type.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Fault property</th>
<th>Definition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[Code]</p></td>
<td><p>soap:Sender</p></td>
</tr>
<tr class="even">
<td><p>[Subcode]</p></td>
<td><p>dsp:InvalidArgs</p></td>
</tr>
<tr class="odd">
<td><p>[Reason]</p></td>
<td><p>At least one input argument is invalid.</p></td>
</tr>
<tr class="even">
<td><p>[Detail]</p></td>
<td><p><em>The invalid argument</em></p></td>
</tr>
</tbody>
</table>

 

### OperationFailed

The Distributed Scan Processing Web Service host can return this fault when the current state of the service prevents the service from performing the requested operation.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Fault property</th>
<th>Definition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[Code]</p></td>
<td><p>soap:Receiver</p></td>
</tr>
<tr class="even">
<td><p>[Subcode]</p></td>
<td><p>dsp:OperationFailed</p></td>
</tr>
<tr class="odd">
<td><p>[Reason]</p></td>
<td><p>The service cannot perform the requested operation.</p></td>
</tr>
<tr class="even">
<td><p>[Detail]</p></td>
<td><p><em>None</em></p></td>
</tr>
</tbody>
</table>

 

### ServerErrorTemporaryError

The Distributed Scan Processing Web Service host returns this fault when the service experiences a temporary error while processing the operation. The client can try the unmodified request again, at a later time, with the expectation that the temporary internal error condition might have been cleared. If a more specific error code (for example, for a disk-full condition) is available to describe the temporary error, the service host should return that code instead of ServerErrorTemporaryError.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Fault property</th>
<th>Definition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[Code]</p></td>
<td><p>soap:Receiver</p></td>
</tr>
<tr class="even">
<td><p>[Subcode]</p></td>
<td><p>dsp:ServerErrorTemporaryError</p></td>
</tr>
<tr class="odd">
<td><p>[Reason]</p></td>
<td><p>The service had an unexpected error.</p></td>
</tr>
<tr class="even">
<td><p>[Detail]</p></td>
<td><p><em>None</em></p></td>
</tr>
</tbody>
</table>

 

### ServerErrorInternalError

The Distributed Scan Processing Web Service host returns this fault when the service encounters an unexpected condition that prevents it from fulfilling the request. This error differs from ServerErrorTemporaryError in that it implies a more permanent type of internal error, for which resending the operation will return the same fault.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Fault property</th>
<th>Definition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[Code]</p></td>
<td><p>soap:Receiver</p></td>
</tr>
<tr class="even">
<td><p>[Subcode]</p></td>
<td><p>dsp:ServerErrorInternalError</p></td>
</tr>
<tr class="odd">
<td><p>[Reason]</p></td>
<td><p>The service had an unexpected error.</p></td>
</tr>
<tr class="even">
<td><p>[Detail]</p></td>
<td><p><em>None</em></p></td>
</tr>
</tbody>
</table>

 

 

 




