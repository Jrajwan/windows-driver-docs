---
title: Create a new WLK device certification submission
description: Create a new WLK device certification submission
ms.assetid: e812eee1-768d-42d6-918e-c716b5c29ea2
ms.author: 
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Create a new WLK device certification submission


To prepare your hardware for certification, you must create and submit a **WQReady.xml** file. Submitting this file allows the dashboard to test your device and return a report on its performance. The report includes a detailed list of how the device compares to Windows standards.

# Creating a WQReady.xml file

1.  Download the [Windows Logo Kit (WLK)](http://go.microsoft.com/fwlink/p/?LinkId=219237). Be sure to test your driver or drivers with the appropriate certification kit on each operating system that you want certification for.

2.  Open the Winqual Submission Tool (WST) and click **Add**.

3.  Browse to the **.cpk** file (WLK test results) and click **Load**.

4.  If the device isn't inbox, enter the **Driver Package**, **Driver Locales**, and **Symbols (optional)**.

5.  Close the **Add DTM Results** dialog box.

6.  You can edit the new entry by selecting it and clicking **Edit**.

7.  After you add all of the entries, create the **.cab** submission package by clicking **Create Package**.

8.  If the tool finds an error, the packaging stops and the entry with the errors is highlighted in red. To view the error, click **View Errors**. Fix errors by clicking **Edit** and updating the driver or the test result. All errors must be fixed before the package can be created.

9.  The tool generates the **WQReady.xml** file, which is used for submission.

    **Note**  
    **WQReady.xml** is the default file name, but you can rename it.

     

## Submitting your file

1.  Sign in to the Hardware Dev Center dashboard with your Microsoft account, and then click **Hardware compatibility**.

2.  On the **Hardware compatibility** page, click **Create WLK submission**.

3.  On the **Hardware logo** page, browse to find the **WQReady.xml** file you want to submit, and then click **Next**.

4.  On the **Product information** page, complete the following information:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Field</th>
    <th>Description</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>Division</p></td>
    <td><p>Select the appropriate division from the list. (Required)</p></td>
    </tr>
    <tr class="even">
    <td><p>Qualifications</p></td>
    <td><p>The list of operating systems and architectures you've already tested.</p>
    <p>For Windows XP, Windows XP (x64), and <strong>Windows 2000</strong>, you can also select one or more earlier versions if WST</p>
    <p>determined that your driver is properly decorated for one or more of those operating systems. They aren't certified, but Microsoft signs your driver for the specified operating system at no cost. (Optional)</p>
    <p></p></td>
    </tr>
    <tr class="odd">
    <td><p>Product name</p></td>
    <td><p>Enter a name for the product. (Required for all Device and System submissions)</p></td>
    </tr>
    <tr class="even">
    <td><p>Marketing name</p></td>
    <td><p>Enter a marketing name and part number, if available, and select the locales that you want to submit for certification. (Optional)</p></td>
    </tr>
    <tr class="odd">
    <td><p>Device metadata category</p></td>
    <td><p>Select an icon for your device from a list of default icons based on your device category. This determines which icon appears in Devices and Printers. (Required for device submissions only.) For information about delivering a rich experience with Windows Device Stage, see [Device Metadata](https://msdn.microsoft.com/library/windows/hardware/br230800.aspx).</p>
    <p></p></td>
    </tr>
    <tr class="even">
    <td><p>Distribution to Windows Update</p></td>
    <td><p>Enter the earliest date on which you want your drivers to be released. They become available to your users the next day. (Optional)</p></td>
    </tr>
    <tr class="odd">
    <td><p>Publication into various catalogs</p></td>
    <td><p>Confirm that you want an announcement of your product included on the Windows Server Catalog, the Windows Logo'd Product List, and CNET, and enter the date when you want this to happen. (Optional)</p></td>
    </tr>
    </tbody>
    </table>

     

> [!NOTE]  
> The company, category, and subcategory are prepopulated based on information in the **WQReady.xml** file.

     

5.  On the **Confirm** page, review the details, and then click **Submit**.

6.  On the **Upload** page, browse for the **WQReady.cab** file that you created using the Winqual Submission Tool, and then click **Upload**.

7.  When the submission completes, you and your administrator receive an email containing the results of the verification.

    Review the results, and, if you choose, make changes to your product and resubmit.

 

 






