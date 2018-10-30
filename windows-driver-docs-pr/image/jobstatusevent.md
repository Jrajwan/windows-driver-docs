---
title: JobStatusEvent element
description: The required JobStatusEvent element informs the client that a job's status has changed.
ms.assetid: 8cb510ef-9622-48d0-859d-e52c9b5b8190
keywords: ["JobStatusEvent element Imaging Devices"]
topic_type:
- apiref
api_name:
- wscn JobStatusEvent
api_type:
- Schema
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# JobStatusEvent element


The required **JobStatusEvent** element informs the client that a job's status has changed.

Usage
-----

``` syntax
<wscn:JobStatusEvent>
  child elements
</wscn:JobStatusEvent>
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
<td><p>[<strong>JobStatus</strong>](jobstatus.md)</p></td>
</tr>
</tbody>
</table>

## Parent elements


There are no parent elements.

Remarks
-------

A WSD Scan Service sends a **JobStatusEvent** element to the client when a job's status has changed. **JobStatusEvent** contains a [**JobStatus**](jobstatus.md) element that defines all of the information about the job's current status. The first **JobStatusEvent** message will typically include the [**JobId**](jobid.md) element and a [**JobState**](jobstate.md) of **Started**.

Examples
--------

The following code example shows how the scan device notifies a client about the current state of Job 253.

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
      http://schemas.microsoft.com/windows/2006/01/wdp/scan/JobStatusEvent
    </wsa:Action>
    <wsa:MessageID>uuid:UniqueMsgId</wsa:MessageID>
  </soap:Header>

  <soap:Body>
    <wscn:JobStatusEvent>
      <wscn:JobStatus>
        <wscn:JobId>253</wscn:JobId>
        <wscn:JobState>Processing</wscn:JobState>
        <wscn:JobStateReasons>
          <wscn:JobStateReason>JobScanning</wscn:JobStateReason>
        </wscn:JobStateReasons>
        <wscn:ScansCompleted>4</wscn:ScansCompleted>
        <wscn:JobCreatedTime>2006-01-24T11:34:35.8345Z</wscn:JobCreatedTime>
      </wscn:JobStatus>
    </wscn:JobStatusEvent>
  </soap:Body
</soap:Envelope>

```

## <span id="see_also"></span>See also


[**JobId**](jobid.md)

[**JobState**](jobstate.md)

[**JobStatus**](jobstatus.md)

 

 






