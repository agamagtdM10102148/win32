---
title: FreeSystemHealthAgentState function
description: Frees a SystemHealthAgentState data structure.
ms.assetid: 'e9bfa8ee-c335-416e-94cf-28646709d419'
keywords: ["FreeSystemHealthAgentState function NAP"]
topic_type:
- apiref
api_name:
- FreeSystemHealthAgentState
api_location:
- qutil.dll
api_type:
- DllExport
---

# FreeSystemHealthAgentState function

> [!Note]  
> The Network Access Protection platform is not available starting with Windows�10

�

The **FreeSystemHealthAgentState** function frees a [**SystemHealthAgentState**](systemhealthagentstate-struct.md) data structure.

## Syntax


```C++
NAPAPI VOID WINAPI FreeSystemHealthAgentState(
  _In_�SystemHealthAgentState *state
);
```



## Parameters

<dl> <dt>

*state* \[in\]
</dt> <dd>

A pointer to the [**SystemHealthAgentState**](systemhealthagentstate-struct.md) data structure to free.

</dd> </dl>

## Remarks

All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):

-   **In** parameters are allocated and freed by the caller.
-   **Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.
-   **In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.

All NAP functions for freeing memory also free all embedded pointers.

## Requirements



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�Vista \[desktop apps only\]<br/>                                       |
| Minimum supported server<br/> | Windows Server�2008 \[desktop apps only\]<br/>                                 |
| Header<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



�

�




