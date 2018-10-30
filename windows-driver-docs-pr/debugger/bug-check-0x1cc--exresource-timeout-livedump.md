---
title: Bug Check 1CC EXRESOURCE_TIMEOUT_LIVEDUMP 
description: The EXRESOURCE_TIMEOUT_LIVEDUMP bug check has a value of 0x000001CC.
keywords: ["Bug Check 0x1CC EXRESOURCE_TIMEOUT_LIVEDUMP", "EXRESOURCE_TIMEOUT_LIVEDUMP"]
ms.author: domars
ms.date: 04/19/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
topic_type:
- apiref
api_name:
- EXRESOURCE_TIMEOUT_LIVEDUMP
api_type:
- NA
ms.localizationpriority: medium
---

# Bug Check Bug Check 0x1CC: EXRESOURCE\_TIMEOUT\_LIVEDUMP

**Important** This topic is for programmers. If you are a customer who has received a blue screen error code while using your computer, see [Troubleshoot blue screen errors](http://windows.microsoft.com/windows-10/troubleshoot-blue-screen-errors).

The EXRESOURCE_TIMEOUT_LIVEDUMP bug check has a value of 0x000001CC.

A kernel ERESOURCE has timed out. This can indicate a deadlock condition or heavy contention which can cause performance issues.


## EXRESOURCE\_TIMEOUT\_LIVEDUMP Parameters

The following parameters are displayed on the blue screen.

Parameter | Description 
|---------|--------------|
1 | The ERESOURCE that has timed out.
2 | The thread that detected the timeout
3 | The ERESOURCE contention count
4 | The configured timeout in seconds



