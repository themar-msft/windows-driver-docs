---
title: KSPROPERTY\_PIN\_COMMUNICATION
description: The KSPROPERTY\_PIN\_COMMUNICATION property specifies the direction of IRP flow on pins instantiated by the pin factory.
ms.assetid: d5f62731-39de-4ec4-83d5-f4253373aaa4
keywords: ["KSPROPERTY_PIN_COMMUNICATION Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_PIN_COMMUNICATION
api_location:
- ks.h
api_type:
- HeaderDef
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
---

# KSPROPERTY\_PIN\_COMMUNICATION


The KSPROPERTY\_PIN\_COMMUNICATION property specifies the direction of IRP flow on pins instantiated by the pin factory.

## <span id="ddk_ksproperty_pin_communication_ks"></span><span id="DDK_KSPROPERTY_PIN_COMMUNICATION_KS"></span>


### <span id="Usage_Summary_Table"></span><span id="usage_summary_table"></span><span id="USAGE_SUMMARY_TABLE"></span>Usage Summary Table

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th>Get</th>
<th>Set</th>
<th>Target</th>
<th>Property Descriptor Type</th>
<th>Property Value Type</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Yes</p></td>
<td><p>No</p></td>
<td><p>Pin</p></td>
<td><p>[<strong>KSP_PIN</strong>](https://msdn.microsoft.com/library/windows/hardware/ff566722)</p></td>
<td><p>KSPIN_COMMUNICATION</p></td>
</tr>
</tbody>
</table>

 

Remarks
-------

The KS filter returns one of the following values, which specifies the communication direction of a pin instantiated by this pin factory:

<span id="KSPIN_COMMUNICATION_NONE"></span><span id="kspin_communication_none"></span>KSPIN\_COMMUNICATION\_NONE  
The pin factory does not instantiate any pins.

<span id="KSPIN_COMMUNICATION_SINK"></span><span id="kspin_communication_sink"></span>KSPIN\_COMMUNICATION\_SINK  
The pin factory instantiates IRP sink pins. Such pins can only be connected to IRP source pins.

<span id="KSPIN_COMMUNICATION_SOURCE"></span><span id="kspin_communication_source"></span>KSPIN\_COMMUNICATION\_SOURCE  
The pin factory instantiates IRP source pins. Such pins can only be connected to IRP sink pins.

<span id="KSPIN_COMMUNICATION_BOTH"></span><span id="kspin_communication_both"></span>KSPIN\_COMMUNICATION\_BOTH  
The pin factory instantiates pins that are both IRP sinks and IRP sources.

<span id="KSPIN_COMMUNICATION_BRIDGE"></span><span id="kspin_communication_bridge"></span>KSPIN\_COMMUNICATION\_BRIDGE  
This pin cannot connect to other pins, but instances can be created on it to receive non-KS I/O requests.

Source pins send IRPs to sink pins. A source pin may read or write data, and a sink pin may have data read to it or written from it. For more information, see [**KSPROPERTY\_PIN\_DATAFLOW**](ksproperty-pin-dataflow.md).

Stream minidrivers do not need to handle this property directly; the stream class driver handles this property using Stream Request Blocks to query for more information where necessary.

Requirements
------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Header</p></td>
<td>Ks.h (include Ks.h)</td>
</tr>
</tbody>
</table>

## <span id="see_also"></span>See also


[**KSPROPERTY\_PIN\_DATAFLOW**](ksproperty-pin-dataflow.md)

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bstream\stream%5D:%20KSPROPERTY_PIN_COMMUNICATION%20%20RELEASE:%20%2811/22/2017%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")





