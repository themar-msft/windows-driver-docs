---
title: OID_GEN_CO_PROTOCOL_OPTIONS
author: windows-driver-content
description: This topic describes the OID_GEN_CO_PROTOCOL_OPTIONS object identifier (OID).
ms.assetid: 5c1212e4-1fd2-435a-ae8c-9f75522cbca6
keywords:
- OID_GEN_CO_PROTOCOL_OPTIONS
ms.author: windowsdriverdev
ms.date: 11/02/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
---

# OID_GEN_CO_PROTOCOL_OPTIONS

A bitmask that defines optional properties of the protocol driver. A protocol informs NDIS of its properties, which can optionally take advantage of them. If the protocol driver does not set its flags on a binding, NDIS assumes they are all clear.

The following flags are currently defined:

NDIS_PROT_OPTION_ESTIMATED_LENGTH  
Indicates that packets can be indicated at the worst-case estimate of packet size, instead of an exact value, to this protocol.

NDIS_PROT_OPTION_NO_LOOPBACK  
The protocol does not require loopback support on the binding.

NDIS_PROT_OPTION_NO_RSVD_ON_RCVPKT  
The protocol does not use the **ProtocolReserved** section of indicated receive packets. This allows NDIS to indicate a receive packet to more than one protocol.

## Requirements

| | |
| --- | --- |
| Version | Windows Vista and later |
| Header | Ntddndis.h (include Ndis.h) |

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bnetvista\netvista%5D:%20OID_WWAN_DEVICE_CAPS_EX%20%20RELEASE:%20%288/8/2017%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")