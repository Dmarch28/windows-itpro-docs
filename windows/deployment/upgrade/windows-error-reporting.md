---
title: Windows error reporting - Windows IT Pro
description: Resolve Windows 10 upgrade errors for ITPros. Technical information for IT professionals to help diagnose Windows setup errors.
keywords: deploy, error, troubleshoot, windows, 10, upgrade, code, rollback, ITPro
ms.prod: w10
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: deploy
author: greg-lindsay
ms.date: 03/30/2018
ms.localizationpriority: medium
ms.topic: article
---

# Windows error reporting

**Applies to**
-   Windows 10

>[!NOTE]
>This is a 300 level topic (moderately advanced).<br>
>See [Resolve Windows 10 upgrade errors](resolve-windows-10-upgrade-errors.md) for a full list of topics in this article.


When Windows Setup fails, the result and extend code are recorded as an informational event in the Application log by Windows Error Reporting as event 1001. The event name is **WinSetupDiag02**.  You can use Event Viewer to review this event, or you can use Windows PowerShell.

To use Windows PowerShell, type the following commands from an elevated Windows PowerShell prompt:

```
$events = Get-WinEvent -FilterHashtable @{LogName="Application";ID="1001";Data="WinSetupDiag02"}
$event = [xml]$events[0].ToXml()
$event.Event.EventData.Data
```

To use Event Viewer: 
1. Open Event Viewer and navigate to **Windows Logs\Application**.
2. Click **Find**, and then search for **winsetupdiag02**.
3. Double-click the event that is highlighted.

Note: For legacy operating systems, the Event Name was WinSetupDiag01. 

Ten parameters are listed in the event:
<br>
<table border="0">
<tr><td>P1: The Setup Scenario (1=Media,5=WindowsUpdate,7=Media Creation Tool)</td></tr>
<tr><td>P2: Setup Mode (x=default,1=Downlevel,5=Rollback)</td></tr>
<tr><td>P3: New OS Architecture (x=default,0=X86,9=AMD64)</td></tr>
<tr><td>P4: Install Result (x=default,0=Success,1=Failure,2=Cancel,3=Blocked)</td></tr>
<tr><td><b>P5: Result Error Code</b>  (Ex: 0xc1900101)</td></tr>
<tr><td><b>P6: Extend Error Code</b>  (Ex: 0x20017)</td></tr>
<tr><td>P7: Source OS build (Ex: 9600)</td></tr>
<tr><td>P8: Source OS branch (not typically available)</td></tr>
<tr><td>P9: New OS build (Ex: 16299}</td></tr>
<tr><td>P10: New OS branch (Ex: rs3_release}</td></tr>
</table>

The event will also contain links to log files that can be used to perform a detailed diagnosis of the error.  An example of this event from a successful upgrade is shown below.

![Windows Error Reporting](../images/event.png)

## Related topics

[Windows 10 FAQ for IT professionals](https://technet.microsoft.com/windows/dn798755.aspx)
<br>[Windows 10 Enterprise system requirements](https://technet.microsoft.com/windows/dn798752.aspx)
<br>[Windows 10 Specifications](https://www.microsoft.com/en-us/windows/Windows-10-specifications)
<br>[Windows 10 IT pro forums](https://social.technet.microsoft.com/Forums/en-US/home?category=Windows10ITPro)
<br>[Fix Windows Update errors by using the DISM or System Update Readiness tool](https://support.microsoft.com/kb/947821)
