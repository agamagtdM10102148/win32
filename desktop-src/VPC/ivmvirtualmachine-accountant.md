---
title: IVMVirtualMachine Accountant property
description: Retrieves an accountant for this virtual machine.
ms.assetid: '5e512b83-8630-46ee-b521-c8a8193727f5'
keywords: ["Accountant property Virtual PC", "Accountant property Virtual PC , IVMVirtualMachine interface", "IVMVirtualMachine interface Virtual PC , Accountant property"]
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Accountant
- IVMVirtualMachine.get_Accountant
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
---

# IVMVirtualMachine::Accountant property

\[Windows Virtual PC is no longer available for use as of Windows�8. Instead, use the [Hyper-V WMI provider (V2)](https://msdn.microsoft.com/library/windows/desktop/hh850319).\]

Retrieves an accountant for this virtual machine.

This property is read-only.

## Syntax


```C++
HRESULT get_Accountant(
  [out, retval]�IVMAccountant **accountant
);
```



## Property value

The [**IVMAccountant**](ivmaccountant.md) object.

## Error codes



| Name/value                                                                                                                                                    | Meaning                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S\_OK</dt> <dt>0</dt> </dl>                       | The operation was successful.<br/>     |
| <dl> <dt>E\_POINTER</dt> <dt>0x80004003</dt> </dl>         | The parameter is **NULL**.<br/>        |
| <dl> <dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | The configuration is unknown.<br/>     |
| <dl> <dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt> </dl> | An unexpected error has occurred.<br/> |



## Requirements



|                                     |                                                                                               |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�7 \[desktop apps only\]<br/>                                                    |
| Minimum supported server<br/> | None supported<br/>                                                                     |
| End of client support<br/>    | Windows�7<br/>                                                                          |
| Product<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## See also

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

�

�




