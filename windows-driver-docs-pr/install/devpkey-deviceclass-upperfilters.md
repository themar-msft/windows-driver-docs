---
title: DEVPKEY_DeviceClass_UpperFilters
description: DEVPKEY_DeviceClass_UpperFilters
ms.assetid: 9a6a9587-340c-460e-b6e2-1aadfb5b8c2f
keywords: ["DEVPKEY_DeviceClass_UpperFilters Device and Driver Installation"]
topic_type:
- apiref
api_name:
- DEVPKEY_DeviceClass_UpperFilters
api_location:
- Devpkey.h
api_type:
- HeaderDef
---

# DEVPKEY_DeviceClass_UpperFilters


The DEVPKEY_DeviceClass_UpperFilters device property represents a list of the service names of the upper-level filter drivers that are installed for a [device setup class](https://msdn.microsoft.com/library/windows/hardware/ff541509).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Property key</strong></p></td>
<td align="left"><p>DEVPKEY_DeviceClass_UpperFilters</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Property-data-type identifier</strong></p></td>
<td align="left"><p>[<strong>DEVPROP_TYPE_STRING_LIST</strong>](devprop-type-string-list.md)</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Data format</strong></p></td>
<td align="left"><p>&quot;<em>service-name1</em>\0<em>service-name2</em>\0…<em>service-nameN</em>\0\0&quot;</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Property access</strong></p></td>
<td align="left"><p>Read-only access by installation applications and installers after a class filter is installed</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Corresponding SPCRP_</strong><em>Xxx</em> <strong>identifier</strong></p></td>
<td align="left"><p>SPCRP_UPPERFILTERS</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Corresponding registry value name</strong></p></td>
<td align="left"><p><strong>UpperFilters</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Localized?</strong></p></td>
<td align="left"><p>No</p></td>
</tr>
</tbody>
</table>

 

Remarks
-------

The value of DEVPKEY_DeviceClass_UpperFilters is set when a class filter driver is installed. For more information about how to install a class filter driver, see [Installing a Filter Driver](https://msdn.microsoft.com/library/windows/hardware/ff547595) and [**INF ClassInstall32 Section**](https://msdn.microsoft.com/library/windows/hardware/ff546335).

You can call [**SetupDiGetClassProperty**](https://msdn.microsoft.com/library/windows/hardware/ff551086) or [**SetupDiGetClassPropertyEx**](https://msdn.microsoft.com/library/windows/hardware/ff551090) to retrieve the value of DEVPKEY_DeviceClass_UpperFilters.

Windows Server 2003, Windows XP, and Windows 2000 support this property, but do not support the DEVPKEY_DeviceClass_UpperFilters property key. On these earlier versions of Windows, you can access the value of this property by accessing the corresponding **UpperFilters** registry value under the class registry key. For information about how to access this property value on these earlier versions of Windows, see [Accessing Registry Entry Values Under the Class Registry Key](https://msdn.microsoft.com/library/windows/hardware/ff537751).

Requirements
------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Version</p></td>
<td align="left"><p>Available in Windows Vista and later versions of Windows.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Header</p></td>
<td align="left">Devpkey.h (include Devpkey.h)</td>
</tr>
</tbody>
</table>

## See also


[**INF ClassInstall32 Section**](https://msdn.microsoft.com/library/windows/hardware/ff546335)

[**SetupDiGetClassProperty**](https://msdn.microsoft.com/library/windows/hardware/ff551086)

[**SetupDiGetClassPropertyEx**](https://msdn.microsoft.com/library/windows/hardware/ff551090)

[**SetupDiOpenClassRegKeyEx**](https://msdn.microsoft.com/library/windows/hardware/ff552067)

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bdevinst\devinst%5D:%20DEVPKEY_DeviceClass_UpperFilters%20%20RELEASE:%20%2810/9/2017%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")





