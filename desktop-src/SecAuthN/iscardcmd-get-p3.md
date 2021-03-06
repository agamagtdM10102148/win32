---
Description: Retrieves the third parameter (P3) byte from the application protocol data unit (APDU).
ms.assetid: 5fe90686-f542-42be-91ed-6600eaee3e7b
title: ISCardCmd::get_P3 method (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type: 
- APIRef
- kbSyntax
api_name: 
- ISCardCmd.get_P3
api_type: 
- COM
api_location: 
- Scardssp.dll
---

# ISCardCmd::get\_P3 method

\[The **get\_P3** method is available for use in the operating systems specified in the Requirements section. It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The [Smart Card Modules](https://msdn.microsoft.com/library/Dd627652(v=VS.85).aspx) provide similar functionality.\]

The **get\_P3** method retrieves the third parameter (P3) byte from the [*application protocol data unit*](https://msdn.microsoft.com/library/ms721532(v=VS.85).aspx) (APDU). This read-only byte value represents the size of the data portion of the APDU.

## Syntax


```C++
HRESULT get_P3(
  [out] BYTE *pbyP3
);
```



## Parameters

<dl> <dt>

*pbyP3* \[out\]
</dt> <dd>

Pointer to the byte that is the P3 from the APDU on return.

</dd> </dl>

## Return value

The method returns one of the following possible values.



| Return code                                                                                   | Description                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S\_OK**</dt> </dl>          | Operation completed successfully.<br/>    |
| <dl> <dt>**E\_INVALIDARG**</dt> </dl>  | The *pbyP3* is not valid.<br/>            |
| <dl> <dt>**E\_POINTER**</dt> </dl>     | A bad pointer was passed in *pbyP3*.<br/> |
| <dl> <dt>**E\_OUTOFMEMORY**</dt> </dl> | Out of memory.<br/>                       |



 

## Remarks

The P3 parameter is read-only, and therefore cannot be set.

To get the P1 or P2 parameters, call [**get\_P1**](iscardcmd-get-p1.md) and [**get\_P2**](iscardcmd-get-p2.md) respectively.

For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).

In addition to the COM error codes listed above, this interface may return a [*smart card*](https://msdn.microsoft.com/library/ms721625(v=VS.85).aspx) error code if a smart card function was called to complete the request. For more information, see [Smart Card Return Values](authentication-return-values.md).

## Examples

The following example shows how to retrieve the third parameter (P3) byte from the [*application protocol data unit*](https://msdn.microsoft.com/library/ms721532(v=VS.85).aspx) (APDU). The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.


```C++
BYTE  byP3;
HRESULT  hr;

// Retrieve the P3 byte.
hr = pISCardCmd->get_P3(&byP3);
if (FAILED(hr))
{
  printf("Failed get_P3\n");
  // Take other error handling action as needed.
}
```



## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows XP \[desktop apps only\]<br/>                                             |
| Minimum supported server<br/> | Windows Server 2003 \[desktop apps only\]<br/>                                    |
| End of client support<br/>    | Windows XP<br/>                                                                   |
| End of server support<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Type library<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## See also

<dl> <dt>

[**get\_P1**](iscardcmd-get-p1.md)
</dt> <dt>

[**get\_P2**](iscardcmd-get-p2.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 




