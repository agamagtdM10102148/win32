---
title: MOUNTMGR\_CHANGE\_NOTIFY\_INFO structure
description: The MOUNTMGR\_CHANGE\_NOTIFY\_INFO structure is used by the mount manager to send epic numbers to its clients and vice versa.
ms.assetid: '3b1bb2be-2abb-414a-bf68-9d06e53c2808'
keywords: ["MOUNTMGR_CHANGE_NOTIFY_INFO structure Storage Devices", "PMOUNTMGR_CHANGE_NOTIFY_INFO structure pointer Storage Devices"]
topic_type:
- apiref
api_name:
- MOUNTMGR_CHANGE_NOTIFY_INFO
api_location:
- mountmgr.h
api_type:
- HeaderDef
---

# MOUNTMGR\_CHANGE\_NOTIFY\_INFO structure

The MOUNTMGR\_CHANGE\_NOTIFY\_INFO structure is used by the mount manager to send epic numbers to its clients and vice versa.

## Syntax


```C++
typedef struct _MOUNTMGR_CHANGE_NOTIFY_INFO {
  ULONG EpicNumber;
} MOUNTMGR_CHANGE_NOTIFY_INFO, *PMOUNTMGR_CHANGE_NOTIFY_INFO;
```



## Members

<dl> <dt>

**EpicNumber**
</dt> <dd>

Contains the value of a counter used by the mount manager to determine if a client has up-to-date information concerning changes in mount manager's persistent ID database.

</dd> </dl>

## Remarks

For a general discussion of the mount manager and how it communicates with its clients, see [Supporting Mount Manager Requests in a Storage Class Driver](https://msdn.microsoft.com/library/windows/hardware/ff567603).

## Requirements



|                   |                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Mountmgr.h (include Mountmgr.h)</dt> </dl> |



## See also

<dl> <dt>

[**IOCTL\_MOUNTMGR\_CHANGE\_NOTIFY**](ioctl-mountmgr-change-notify.md)
</dt> </dl>

�

�

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bstorage\storage%5D:%20MOUNTMGR_CHANGE_NOTIFY_INFO%20structure%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")





