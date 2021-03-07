---
title: Policy CSP - Storage
description: Policy CSP - Storage
ms.author: maricia
ms.topic: article
ms.prod: w10
ms.technology: windows
author: MariciaAlforque
ms.date: 08/27/2018
---

# Policy CSP - Storage

> [!WARNING]
> Some information relates to prereleased product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.


<hr/>

<!--Policies-->
## Storage policies  

<dl>
  <dd>
    <a href="#storage-allowdiskhealthmodelupdates">Storage/AllowDiskHealthModelUpdates</a>
  </dd>
  <dd>
    <a href="#storage-enhancedstoragedevices">Storage/EnhancedStorageDevices</a>
  </dd>
  <dd>
    <a href="#storage-removablediskdenywriteaccess">Storage/RemovableDiskDenyWriteAccess</a>
  </dd>
</dl>


<hr/>

<!--Policy-->
<a href="" id="storage-allowdiskhealthmodelupdates"></a>**Storage/AllowDiskHealthModelUpdates**  

<!--SupportedSKUs-->
<table>
<tr>
	<th>Home</th>
	<th>Pro</th>
	<th>Business</th>
	<th>Enterprise</th>
	<th>Education</th>
	<th>Mobile</th>
	<th>Mobile Enterprise</th>
</tr>
<tr>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>3</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>3</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>3</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>3</sup></td>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
</tr>
</table>

<!--/SupportedSKUs-->
<!--Scope-->
[Scope](./policy-configuration-service-provider.md#policy-scope):

> [!div class = "checklist"]
> * Device

<hr/>

<!--/Scope-->
<!--Description-->
Added in Windows 10, version 1709.  Allows disk health model updates.



Value type is integer.

<!--/Description-->
<!--ADMXMapped-->
ADMX Info:  
-   GP English name: *Allow downloading updates to the Disk Failure Prediction Model*
-   GP name: *SH_AllowDiskHealthModelUpdates*
-   GP path: *System/Storage Health*
-   GP ADMX file name: *StorageHealth.admx*

<!--/ADMXMapped-->
<!--SupportedValues-->
The following list shows the supported values:

-   0 - Do not allow
-   1 (default) - Allow

<!--/SupportedValues-->
<!--/Policy-->

<hr/>

<!--Policy-->
<a href="" id="storage-enhancedstoragedevices"></a>**Storage/EnhancedStorageDevices**  

<!--SupportedSKUs-->
<table>
<tr>
	<th>Home</th>
	<th>Pro</th>
	<th>Business</th>
	<th>Enterprise</th>
	<th>Education</th>
	<th>Mobile</th>
	<th>Mobile Enterprise</th>
</tr>
<tr>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
</tr>
</table>

<!--/SupportedSKUs-->
<!--Scope-->
[Scope](./policy-configuration-service-provider.md#policy-scope):

> [!div class = "checklist"]
> * Device

<hr/>

<!--/Scope-->
<!--Description-->
This policy setting configures whether or not Windows will activate an Enhanced Storage device.

If you enable this policy setting, Windows will not activate unactivated Enhanced Storage devices.

If you disable or do not configure this policy setting, Windows will activate unactivated Enhanced Storage devices.

<!--/Description-->
> [!TIP]
> This is an ADMX-backed policy and requires a special SyncML format to enable or disable.  For details, see [Understanding ADMX-backed policies](./understanding-admx-backed-policies.md).

> You must specify the data type in the SyncML as &lt;Format&gt;chr&lt;/Format&gt;. For an example SyncML, refer to [Enabling a policy](./understanding-admx-backed-policies.md#enabling-a-policy).

> The payload of the SyncML must be XML-encoded; for this XML encoding, there are a variety of online encoders that you can use. To avoid encoding the payload, you can use CDATA if your MDM supports it.  For more information, see [CDATA Sections](http://www.w3.org/TR/REC-xml/#sec-cdata-sect).

<!--ADMXBacked-->
ADMX Info:  
-   GP English name: *Do not allow Windows to activate Enhanced Storage devices*
-   GP name: *TCGSecurityActivationDisabled*
-   GP path: *System/Enhanced Storage Access*
-   GP ADMX file name: *enhancedstorage.admx*

<!--/ADMXBacked-->
<!--/Policy-->

<hr/>

<!--Policy-->
<a href="" id="storage-removablediskdenywriteaccess"></a>**Storage/RemovableDiskDenyWriteAccess**  

<!--SupportedSKUs-->
<table>
<tr>
	<th>Home</th>
	<th>Pro</th>
	<th>Business</th>
	<th>Enterprise</th>
	<th>Education</th>
	<th>Mobile</th>
	<th>Mobile Enterprise</th>
</tr>
<tr>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td></td>
	<td></td>
</tr>
</table>

<!--/SupportedSKUs-->
<!--Scope-->
[Scope](./policy-configuration-service-provider.md#policy-scope):

> [!div class = "checklist"]
> * Device

<hr/>

<!--/Scope-->
<!--Description-->
If you enable this policy setting, write access is denied to this removable storage class. If you disable or do not configure this policy setting, write access is allowed to this removable storage class. Note: To require that users write data to BitLocker-protected storage, enable the policy setting "Deny write access to drives not protected by BitLocker," which is located in "Computer Configuration\Administrative Templates\Windows Components\BitLocker Drive Encryption\Removable Data Drives."

Supported values:  
-  0 - Disable
-  1 - Enable

<!--/Description-->
<!--ADMXMapped-->
ADMX Info:  
-   GP English name: *Removable Disks: Deny write access*
-   GP name: *RemovableDisks_DenyWrite_Access_2*
-   GP element: *RemovableDisks_DenyWrite_Access_2*
-   GP path: *System/Removable Storage Access*
-   GP ADMX file name: *RemovableStorage.admx*

<!--/ADMXMapped-->
<!--SupportedValues-->

<!--/SupportedValues-->
<!--Example-->

<!--/Example-->
<!--Validation-->

<!--/Validation-->
<!--/Policy-->
<hr/>

Footnote:

-   1 - Added in Windows 10, version 1607.
-   2 - Added in Windows 10, version 1703.
-   3 - Added in Windows 10, version 1709.
-   4 - Added in Windows 10, version 1803.
-   5 - Added in Windows 10, version 1809.
-   6 - Added in the next major release of Windows 10.

<!--Policy-->
<a href="" id="storage-allowstoragesenseglobal"></a>**Storage/AllowStorageSenseGlobal**  

<!--SupportedSKUs-->
<table>
<tr>
	<th>Home</th>
	<th>Pro</th>
	<th>Business</th>
	<th>Enterprise</th>
	<th>Education</th>
	<th>Mobile</th>
	<th>Mobile Enterprise</th>
</tr>
<tr>
	<td></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td></td>
	<td></td>
</tr>
</table>

<!--/SupportedSKUs-->
<!--Scope-->
[Scope](./policy-configuration-service-provider.md#policy-scope):

> [!div class = "checklist"]
> * Device

<hr/>

<!--/Scope-->
<!--Description-->
Storage Sense can automatically clean some of the user’s files to free up disk space. By default, Storage Sense is automatically turned on when the machine runs into low disk space and is set to run whenever the machine runs into storage pressure. This cadence can be changed in Storage settings or set with the "Configure Storage Sense cadence" group policy.

Enabled:
Storage Sense is turned on for the machine, with the default cadence as ‘during low free disk space’. Users cannot disable Storage Sense, but they can adjust the cadence (unless you also configure the "Configure Storage Sense cadence" group policy).

Disabled:
Storage Sense is turned off the machine. Users cannot enable Storage Sense.

Not Configured:
By default, Storage Sense is turned off until the user runs into low disk space or the user enables it manually. Users can configure this setting in Storage settings.
<!--/Description-->
<!--ADMXMapped-->
ADMX Info:  
-   GP English name: *Allow Storage Sense*
-   GP name: *SS_AllowStorageSenseGlobal*
-   GP path: *SOFTWARE/Policies/Microsoft/Windows/StorageSense*
-   GP ADMX file name: *StorageSense.admx*

<!--/ADMXMapped-->
<!--SupportedValues-->

<!--/SupportedValues-->
<!--Example-->

<!--/Example-->
<!--Validation-->

<!--/Validation-->
<!--/Policy-->

<!--Policy-->
<a href="" id="storage-configstoragesenseglobalcadence"></a>**Storage/ConfigStorageSenseGlobalCadence**  

<!--SupportedSKUs-->
<table>
<tr>
	<th>Home</th>
	<th>Pro</th>
	<th>Business</th>
	<th>Enterprise</th>
	<th>Education</th>
	<th>Mobile</th>
	<th>Mobile Enterprise</th>
</tr>
<tr>
	<td></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td></td>
	<td></td>
</tr>
</table>

<!--/SupportedSKUs-->
<!--Scope-->
[Scope](./policy-configuration-service-provider.md#policy-scope):

> [!div class = "checklist"]
> * Device

<hr/>

<!--/Scope-->
<!--Description-->
Storage Sense can automatically clean some of the user’s files to free up disk space.
If the group policy "Allow Storage Sense" is disabled, then this policy does not have any effect.

Enabled:
You must provide the desired Storage Sense cadence. Supported options are: 

1 – Daily
7 – Weekly
30 – Monthly
0 – During Low Free Disk Space

The default is 0 (during low free disk space).

Not Configured:
By default, the Storage Sense cadence is set to “during low free disk space”. Users can configure this setting in Storage settings.

<!--/Description-->
<!--ADMXMapped-->
ADMX Info:  
-   GP English name: *Configure Storage Sense cadence*
-   GP name: *RemovableDisks_DenyWrite_Access_2*
-   GP path: *SOFTWARE/Policies/Microsoft/Windows/StorageSense*
-   GP ADMX file name: *StorageSense.admx*

<!--/ADMXMapped-->
<!--SupportedValues-->

<!--/SupportedValues-->
<!--Example-->

<!--/Example-->
<!--Validation-->

<!--/Validation-->
<!--/Policy-->

<!--Policy-->
<a href="" id="storage-allowstoragesensetemporaryfilescleanup"></a>**Storage/AllowStorageSenseTemporaryFilesCleanup**  

<!--SupportedSKUs-->
<table>
<tr>
	<th>Home</th>
	<th>Pro</th>
	<th>Business</th>
	<th>Enterprise</th>
	<th>Education</th>
	<th>Mobile</th>
	<th>Mobile Enterprise</th>
</tr>
<tr>
	<td></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td></td>
	<td></td>
</tr>
</table>

<!--/SupportedSKUs-->
<!--Scope-->
[Scope](./policy-configuration-service-provider.md#policy-scope):

> [!div class = "checklist"]
> * Device

<hr/>

<!--/Scope-->
<!--Description-->
When Storage Sense runs, it can delete the user’s temporary files that are not in use.

If the group policy "Allow Storage Sense" is disabled, then this policy does not have any effect.

Enabled:
Storage Sense will delete the user’s temporary files that are not in use. Users cannot disable this setting in Storage settings.

Disabled:
Storage Sense will not delete the user’s temporary files. Users cannot enable this setting in Storage settings.

Not Configured:
By default, Storage Sense will delete the user’s temporary files. Users can configure this setting in Storage settings.

<!--/Description-->
<!--ADMXMapped-->
ADMX Info:  
-   GP English name: *Allow Storage Sense Temporary Files cleanup*
-   GP name: *SS_AllowStorageSenseTemporaryFilesCleanup*
-   GP path: *System/StorageSense*
-   GP ADMX file name: *StorageSense.admx*

<!--/ADMXMapped-->
<!--SupportedValues-->

<!--/SupportedValues-->
<!--Example-->

<!--/Example-->
<!--Validation-->

<!--/Validation-->
<!--/Policy-->

<!--Policy-->
<a href="" id="storage-configstoragesenserecyclebincleanupthreshold"></a>**Storage/ConfigStorageSenseRecycleBinCleanupThreshold**  

<!--SupportedSKUs-->
<table>
<tr>
	<th>Home</th>
	<th>Pro</th>
	<th>Business</th>
	<th>Enterprise</th>
	<th>Education</th>
	<th>Mobile</th>
	<th>Mobile Enterprise</th>
</tr>
<tr>
	<td></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td></td>
	<td></td>
</tr>
</table>

<!--/SupportedSKUs-->
<!--Scope-->
[Scope](./policy-configuration-service-provider.md#policy-scope):

> [!div class = "checklist"]
> * Device

<hr/>

<!--/Scope-->
<!--Description-->
When Storage Sense runs, it can delete files in the user’s Recycle Bin if they have been there for over a certain amount of days.

If the group policy "Allow Storage Sense" is disabled, then this policy does not have any effect.

Enabled:
You must provide the minimum age threshold (in days) of a file in the Recycle Bin before Storage Sense will delete it. Support values are: 0 - 365.
If you set this value to zero, Storage Sense will not delete files in the user’s Recycle Bin. The default is 30 days.

Disabled or Not Configured:
By default, Storage Sense will delete files in the user’s Recycle Bin that have been there for over 30 days. Users can configure this setting in Storage settings.

<!--/Description-->
<!--ADMXMapped-->
ADMX Info:  
-   GP English name: *Configure Storage Sense Recycle Bin cleanup threshold*
-   GP name: *SS_ConfigStorageSenseRecycleBinCleanupThreshold*
-   GP path: *System/StorageSense*
-   GP ADMX file name: *StorageSense.admx*

<!--/ADMXMapped-->
<!--SupportedValues-->

<!--/SupportedValues-->
<!--Example-->

<!--/Example-->
<!--Validation-->

<!--/Validation-->
<!--/Policy-->

<!--Policy-->
<a href="" id="storage-configstoragesensedownloadscleanupthreshold"></a>**Storage/ConfigStorageSenseDownloadsCleanupThreshold**  

<!--SupportedSKUs-->
<table>
<tr>
	<th>Home</th>
	<th>Pro</th>
	<th>Business</th>
	<th>Enterprise</th>
	<th>Education</th>
	<th>Mobile</th>
	<th>Mobile Enterprise</th>
</tr>
<tr>
	<td></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td></td>
	<td></td>
</tr>
</table>

<!--/SupportedSKUs-->
<!--Scope-->
[Scope](./policy-configuration-service-provider.md#policy-scope):

> [!div class = "checklist"]
> * Device

<hr/>

<!--/Scope-->
<!--Description-->
When Storage Sense runs, it can delete files in the user’s Downloads folder if they have been there for over a certain amount of days.

If the group policy "Allow Storage Sense" is disabled, then this policy does not have any effect.

Enabled:
You must provide the minimum age threshold (in days) of a file in the Downloads folder before Storage Sense will delete it. Support values are: 0 - 365.
If you set this value to zero, Storage Sense will not delete files in the user’s Downloads folder. The default is 0, or never deleting files in the Downloads folder.

Disabled or Not Configured:
By default, Storage Sense will not delete files in the user’s Downloads folder. Users can configure this setting in Storage settings.

<!--/Description-->
<!--ADMXMapped-->
ADMX Info:  
-   GP English name: *Configure Storage Storage Downloads cleanup threshold*
-   GP name: *SS_ConfigStorageSenseDownloadsCleanupThreshold*
-   GP path: *System/StorageSense*
-   GP ADMX file name: *StorageSense.admx*

<!--/ADMXMapped-->
<!--SupportedValues-->

<!--/SupportedValues-->
<!--Example-->

<!--/Example-->
<!--Validation-->

<!--/Validation-->
<!--/Policy-->

<!--Policy-->
<a href="" id="storage-configstoragesensecloudcontentdehydrationthreshold"></a>**Storage/ConfigStorageSenseCloudContentDehydrationThreshold**  

<!--SupportedSKUs-->
<table>
<tr>
	<th>Home</th>
	<th>Pro</th>
	<th>Business</th>
	<th>Enterprise</th>
	<th>Education</th>
	<th>Mobile</th>
	<th>Mobile Enterprise</th>
</tr>
<tr>
	<td></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>5</sup></td>
	<td></td>
	<td></td>
</tr>
</table>

<!--/SupportedSKUs-->
<!--Scope-->
[Scope](./policy-configuration-service-provider.md#policy-scope):

> [!div class = "checklist"]
> * Device

<hr/>

<!--/Scope-->
<!--Description-->
When Storage Sense runs, it can dehydrate cloud-backed content that hasn’t been opened in a certain amount of days.

If the group policy "Allow Storage Sense" is disabled, then this policy does not have any effect.

Enabled:
You must provide the number of days since a cloud-backed file has been opened before Storage Sense will dehydrate it. Support values are: 0 - 365.
If you set this value to zero, Storage Sense will not dehydrate any cloud-backed content. The default value is 0, or never dehydrating cloud-backed content.

Disabled or Not Configured:
By default, Storage Sense will not dehydrate any cloud-backed content. Users can configure this setting in Storage settings.

<!--/Description-->
<!--ADMXMapped-->
ADMX Info:  
-   GP English name: *Configure Storage Sense Cloud Content dehydration threshold*
-   GP name: *SS_ConfigStorageSenseCloudContentDehydrationThreshold*
-   GP path: *System/StorageSense*
-   GP ADMX file name: *StorageSense.admx*

<!--/ADMXMapped-->
<!--SupportedValues-->

<!--/SupportedValues-->
<!--Example-->

<!--/Example-->
<!--Validation-->

<!--/Validation-->
<!--/Policy-->


<!--/Policies-->

