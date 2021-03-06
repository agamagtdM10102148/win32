---
title: isnan (Corecrt\_math.h)
description: Determines if the specified value is NAN or QNAN.
ms.assetid: 09085634-e610-4793-848e-abda8241f1cc
keywords:
- isnan HLSL
topic_type:
- apiref
api_name:
- isnan
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
---

# isnan

Determines if the specified value is NAN or QNAN.



| *ret* isnan(*x*) |
|------------------|



 

## Parameters



| Item                                                   | Description                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[in\] The specified value.<br/> |



 

## Return Value

Returns a value of the same size as the input, with a value set to **True** if the *x* parameter is NAN or QNAN. Otherwise, **False**.

## Type Description



| Name  | [**Template Type**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Component Type**](dx-graphics-hlsl-intrinsic-functions.md) | Size     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| *x*   | [**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix** | [**float**](https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types)                        | any      |
| *ret* | [**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix** | [**bool**](https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types)                         | as input |



 

## Minimum Shader Model

This function is supported in the following shader models.



| Shader Model                                                                       | Supported           |
|------------------------------------------------------------------------------------|---------------------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models | yes                 |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | yes (vs\_1\_1 only) |



 

## Requirements



|                   |                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Corecrt\_math.h</dt> </dl> |



## See also

<dl> <dt>

[**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





