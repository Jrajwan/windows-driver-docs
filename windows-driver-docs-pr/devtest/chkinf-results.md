---
title: ChkINF Results
description: ChkINF Results
ms.assetid: b098f16d-2168-4fe1-bf1d-c8eeabe2e433
keywords:
- Perl scripts WDK INF files
- ChkINF WDK , results
- INF files WDK , syntax checker
- syntax checker WDK INF files
- verifying INF files
- checking INF files
- errors WDK ChkINF
- scripts WDK ChkINF
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# ChkINF Results


## <span id="ddk_chkinf_results_tools"></span><span id="DDK_CHKINF_RESULTS_TOOLS"></span>


ChkINF generates output in several reports and it writes data to the command line.

### <span id="chkinf_command_line_output"></span><span id="CHKINF_COMMAND_LINE_OUTPUT"></span>ChkINF Command-Line Output

At the command line, ChkINF displays the name of the INF file that it is validating and the HTM file that it created to stores the results for that INF file in the following format:

```
Processing INFFile -> HTMFile
```

For example,

```
Processing c:\windows\inf\ntprint.inf -> .\htm\c#+windows+inf+__ntprint.htm
```

It also displays the names of device-class-specific Perl modules that it is using to validate the file.

For example,

```
Module "PRINTER" Loaded  (Ver 5.2.3790.3)
```

It ends with the elapsed time of the run. For example,

```
Elapsed time  :  00h 00m 01s
```

### <span id="chkinf_results_files"></span><span id="CHKINF_RESULTS_FILES"></span>ChkINF Results Files

ChkINF creates a subdirectory named htm in the current directory and stores its HTML output files in that directory.

ChkINF produces three types of files:

-   **Summary of results** (Summary.htm). Lists the INF files that were checked and the number of errors and warnings for each file. Each INF file name in Summary.htm is a link to the ChkINF results file for that INF file.

-   **Results file** (&lt;INFFileName&gt;.htm). Lists the errors and warning conditions for the named INF file. The name of the results file is based on the name of the INF file.

-   **Text file**. An optional results file in text format. ChkINF creates this file when you use the **/B** parameter. It contains results for all of the INF files that ChkINF validate. You must specify a name for the text file. If you do not specify a path for the log file, ChkINF places the log file in the local directory, not in the htm subdirectory.

Each Results File has the following sections:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Section</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Errors</strong></p></td>
<td align="left"><p>A list of the errors found in the INF file.</p>
<p>Each error entry consists of the line number of the error in the INF file, an error number, and a description of the error.</p>
<p>The line number is a link to the Annotated INF section.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Warnings</strong></p></td>
<td align="left"><p>A list of the warning conditions detected in the INF file.</p>
<p>Each warning entry consists of the line number of the warning condition in the INF file, a warning number, and a description of the warning.</p>
<p>The line number is a link to the Annotated INF section.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Annotated INF</strong></p></td>
<td align="left"><p>The complete source for the INF file, with warning and error messages displayed adjacent to the line where the warning or error was detected.</p></td>
</tr>
</tbody>
</table>

 

 

 





