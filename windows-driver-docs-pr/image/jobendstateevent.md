---
title: JobEndStateEvent element
description: The required JobEndStateEvent element informs the client that the scanner has finished processing a job.
ms.assetid: 2d5307fb-9c64-413d-8c5c-439012a44a19
keywords: ["JobEndStateEvent element Imaging Devices"]
topic_type:
- apiref
api_name:
- wscn JobEndStateEvent
api_type:
- Schema
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# JobEndStateEvent element


The required **JobEndStateEvent** element informs the client that the scanner has finished processing a job.

Usage
-----

``` syntax
<wscn:JobEndStateEvent>
  child elements
</wscn:JobEndStateEvent>
```

Attributes
----------

There are no attributes.

## Child elements


<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[<strong>JobEndState</strong>](jobendstate.md)</p></td>
</tr>
</tbody>
</table>

## Parent elements


There are no parent elements.

Remarks
-------

The WSD Scan Service sends a **JobEndStateEvent** event element to the client when the scanner has finished processing a job. **JobEndStateEvent** contains data elements that identify the completed job and details about its completion.

Examples
--------

The following code example shows how the scan device notifies the client of the final state and status of Job 253.

```
<soap:Envelope
  xmlns:soap="http://www.w3.org/2003/05/soap-envelope"
  xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing"
  xmlns:wse="http://schemas.xmlsoap.org/ws/2004/08/eventing"
  xmlns:wscn="http://schemas.microsoft.com/windows/2006/01/wdp/scan"
  soap:encodingStyle=&#39;http://www.w3.org/2002/12/soap-encoding&#39;>

  <soap:Header>
    <wsa:To>AddressofEventSink</wsa:To>
    <wsa:Action>
      http://schemas.microsoft.com/windows/2006/01/wdp/scan/JobEndStateEvent
    </wsa:Action>
    <wsa:MessageID>uuid:UniqueMsgId</wsa:MessageID>
  </soap:Header>

  <soap:Body>
    <wscn:JobEndStateEvent>
      <wscn:JobEndState>
        <wscn:JobId>253</wscn:JobId>
        <wscn:JobCompletedState>Completed</wscn:JobCompletedState>
        <wscn:JobCompletedStateReasons>
          <wscn:JobStateReason>JobCompletedWithWarnings</wscn:JobStateReason>
        </wscn:JobCompletedStateReasons>
        <wscn:JobName>Scan from Imaging App</wscn:JobName>
        <wscn:JobOriginatingUserName>User</wscn:JobOriginatingUserName>
        <wscn:ScansCompleted>7</wscn:ScansCompleted>
        <wscn:JobCompletedTime>2006-01-24T11:37:05.673Z</wscn:JobCompletedTime>
      </wscn:JobEndState>
    </wscn:JobEndStateEvent>
  </soap:Body
</soap:Envelope>
```

## <span id="see_also"></span>See also


[**JobEndState**](jobendstate.md)

 

 






