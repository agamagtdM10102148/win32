---
Description: 'The get\_SourceTop method retrieves the top coordinate of the current source rectangle.'
ms.assetid: '78dbd1e6-f591-487e-b9fe-fcbda55f5338'
title: 'CBaseControlVideo.get\_SourceTop method'
---

# CBaseControlVideo.get\_SourceTop method

The `get_SourceTop` method retrieves the top coordinate of the current source rectangle.

## Syntax


```C++
HRESULT get_SourceTop(
  �long *pSourceTop
);
```



## Parameters

<dl> <dt>

*pSourceTop* 
</dt> <dd>

Pointer to the top coordinate of the source rectangle.

</dd> </dl>

## Return value

Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.



| Return code                                                                                           | Description                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E\_FAIL**</dt> </dl>                | Failure.<br/>                                                              |
| <dl> <dt>**E\_POINTER**</dt> </dl>             | **NULL** pointer argument.<br/>                                            |
| <dl> <dt>**VFW\_E\_NOT\_CONNECTED**</dt> </dl> | The operation cannot be performed because the pins are not connected.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>                | Success.<br/>                                                              |



�

## Remarks

This member function implements the [**IBasicVideo::get\_SourceTop**](ibasicvideo-get-sourcetop.md) method.

An application can change the source and destination rectangles for the video through the [**IBasicVideo**](ibasicvideo.md) interface. The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played. The destination rectangle is relative to the client area of the window in which it is playing. The upper-left corner of the window is coordinate (0,0).

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CBaseControlVideo Class**](cbasecontrolvideo.md)
</dt> </dl>

�

�



