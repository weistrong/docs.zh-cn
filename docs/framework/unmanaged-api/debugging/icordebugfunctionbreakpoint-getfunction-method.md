---
description: 了解详细信息： ICorDebugFunctionBreakpoint：： GetFunction 方法
title: ICorDebugFunctionBreakpoint::GetFunction 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFunctionBreakpoint.GetFunction
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunctionBreakpoint::GetFunction
helpviewer_keywords:
- ICorDebugFunctionBreakpoint::GetFunction method [.NET Framework debugging]
- GetFunction method, ICorDebugFunctionBreakpoint interface [.NET Framework debugging]
ms.assetid: 2a62dae5-dd8a-4696-b817-0e1e586c24a0
topic_type:
- apiref
ms.openlocfilehash: 1e407acda81e5e6397da003a9b91a48d4d171e5d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754090"
---
# <a name="icordebugfunctionbreakpointgetfunction-method"></a><span data-ttu-id="13445-103">ICorDebugFunctionBreakpoint::GetFunction 方法</span><span class="sxs-lookup"><span data-stu-id="13445-103">ICorDebugFunctionBreakpoint::GetFunction Method</span></span>

<span data-ttu-id="13445-104">获取一个指向 ICorDebugFunction 的接口指针，该指针引用在其中设置断点的函数。</span><span class="sxs-lookup"><span data-stu-id="13445-104">Gets an interface pointer to an ICorDebugFunction that references the function in which the breakpoint is set.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="13445-105">语法</span><span class="sxs-lookup"><span data-stu-id="13445-105">Syntax</span></span>  
  
```cpp  
HRESULT GetFunction (  
    [out] ICorDebugFunction  **ppFunction  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="13445-106">参数</span><span class="sxs-lookup"><span data-stu-id="13445-106">Parameters</span></span>  

 `ppFunction`  
 <span data-ttu-id="13445-107">弄一个指针，指向设置断点的函数的地址。</span><span class="sxs-lookup"><span data-stu-id="13445-107">[out] A pointer to the address of the function in which the breakpoint is set.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="13445-108">要求</span><span class="sxs-lookup"><span data-stu-id="13445-108">Requirements</span></span>  

 <span data-ttu-id="13445-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="13445-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="13445-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="13445-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="13445-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="13445-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="13445-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="13445-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
