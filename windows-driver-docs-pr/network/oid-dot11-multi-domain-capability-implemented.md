---
title: OID_DOT11_MULTI_DOMAIN_CAPABILITY_IMPLEMENTED
author: windows-driver-content
description: OID_DOT11_MULTI_DOMAIN_CAPABILITY_IMPLEMENTED
ms.assetid: 5de9d07f-d0d1-4507-8193-331c7bf176f5
ms.author: windowsdriverdev
ms.date: 08/08/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
keywords: 
 -OID_DOT11_MULTI_DOMAIN_CAPABILITY_IMPLEMENTED Network Drivers Starting with Windows Vista
---

# OID\_DOT11\_MULTI\_DOMAIN\_CAPABILITY\_IMPLEMENTED


**Important**  The [Native 802.11 Wireless LAN](https://msdn.microsoft.com/library/windows/hardware/ff560690) interface is deprecated in Windows 10 and later. Please use the WLAN Device Driver Interface (WDI) instead. For more information about WDI, see [WLAN Universal Windows driver model](https://msdn.microsoft.com/library/windows/hardware/dn897672).

 

When queried, the OID\_DOT11\_MULTI\_DOMAIN\_CAPABILITY\_IMPLEMENTED object identifier (OID) requests that the miniport driver return the value of the IEEE 802.11d **dot11MultiDomainCapabilityImplemented** management information base (MIB) object.

If the **dot11MultiDomainCapabilityImplemented** MIB object is **TRUE**, the 802.11 station supports more than one regulatory domain. For more information about 802.11 regulatory domains, refer to the IEEE 802.11d-2001 standard.

The data type for OID\_DOT11\_MULTI\_DOMAIN\_CAPABILITY\_IMPLEMENTED is a BOOLEAN value.

**Note**  A Native 802.11 miniport driver that is designed to run on the Windows Vista or Windows Server 2008 operating systems must always reset this 802.11 MIB OID to its default value. This is the case regardless of the value of the **bSetDefaultMIB** member of the DOT11\_RESET\_REQUEST structure. This requirement applies to a miniport driver that, in a call to the **NdisMSetMiniportAttributes** function, sets **MiniportAttributes** -&gt; **Native\_802\_11\_Attributes** -&gt; **Header** -&gt; **Revision** to NDIS\_MINIPORT\_ADAPTER\_802\_11\_ATTRIBUTES\_REVISION\_1.

 

Requirements
------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Version</p></td>
<td><p>Available in Windows Vista and later versions of the Windows operating systems.</p></td>
</tr>
<tr class="even">
<td><p>Header</p></td>
<td>Windot11.h (include Ndis.h)</td>
</tr>
</tbody>
</table>

## See also


[Native 802.11 MIB OIDs](https://msdn.microsoft.com/library/windows/hardware/ff560645)

[Native 802.11 Wireless LAN OIDs](https://msdn.microsoft.com/library/windows/hardware/ff560691)

 

 




