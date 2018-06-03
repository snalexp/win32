---
title: ENUM\_PDO\_ENTRY structure
description: This structure describes a single entry in a result set of Physical Device Objects (PDOs) that are enumerated with IOCTL\_EHSTOR\_DEVICE\_ENUMERATE\_PDOS.
ms.assetid: c3f5cc8e-a600-4ca1-8745-d74943feb2c7
keywords:
- ENUM_PDO_ENTRY structure Storage Devices
- PENUM_PDO_ENTRY structure pointer Storage Devices
topic_type:
- apiref
api_name:
- ENUM_PDO_ENTRY
api_location:
- EhStorIoctl.h
api_type:
- HeaderDef
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: structure
ms.date: 05/31/2018
---

# ENUM\_PDO\_ENTRY structure

This structure describes a single entry in a result set of Physical Device Objects (PDOs) that are enumerated with [**IOCTL\_EHSTOR\_DEVICE\_ENUMERATE\_PDOS**](ioctl-ehstor-device-enumerate-pdos.md).

## Syntax


```C++
typedef struct _ENUM_PDO_ENTRY {
  UCHAR type;
  UCHAR state;
  UCHAR capabilities;
  ULONG ulSTID;
  UCHAR bSpecificationMajor;
  UCHAR bSpecificationMinor;
  UCHAR bImplementationMajor;
  UCHAR bImplementationMinor;
  WCHAR wszDeviceInstancePath[(2 * MAX_PATH) + 1];
} ENUM_PDO_ENTRY, *PENUM_PDO_ENTRY;
```



## Members

<dl> <dt>

**type**
</dt> <dd>

This member indicates the type of the PDO that is being identified, as defined by PDO\_TYPE.

</dd> <dt>

**state**
</dt> <dd>

This member contains information about the current PnP state of the PDO, as defined by PDO\_STATE.

</dd> <dt>

**capabilities**
</dt> <dd>

This member contains a bitmask with bits indicating information about the silo represented by the PDO in question, as defined by PDO\_CAPS.

</dd> <dt>

**ulSTID**
</dt> <dd>

This member contains the silo type identifier, as defined and assigned by the IEEE 1667 working group.

</dd> <dt>

**bSpecificationMajor**
</dt> <dd></dd> <dt>

**bSpecificationMinor**
</dt> <dd></dd> <dt>

**bImplementationMajor**
</dt> <dd></dd> <dt>

**bImplementationMinor**
</dt> <dd></dd> <dt>

**wszDeviceInstancePath**
</dt> <dd>

The string contained in this member is the device instance path in a form suitable for use with the Win32 API CreateFile routine.

</dd> </dl>

## Remarks

## Requirements



|                   |                                                                                                                  |
|-------------------|------------------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>EhStorIoctl.h (include EhStorIoctl.h)</dt> </dl> |



## See also

<dl> <dt>

[**IOCTL\_EHSTOR\_DEVICE\_ENUMERATE\_PDOS**](ioctl-ehstor-device-enumerate-pdos.md)
</dt> </dl>

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bstorage\storage%5D:%20ENUM_PDO_ENTRY%20structure%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")





