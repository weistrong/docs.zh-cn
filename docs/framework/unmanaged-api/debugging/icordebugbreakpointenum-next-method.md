---
description: 了解详细信息： ICorDebugBreakpointEnum：： Next 方法
title: ICorDebugBreakpointEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugBreakpointEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugBreakpointEnum::Next
helpviewer_keywords:
- Next method, ICorDebugBreakpointEnum interface [.NET Framework debugging]
- ICorDebugBreakpointEnum::Next method [.NET Framework debugging]
ms.assetid: 2e6bbaea-79ba-448c-a0e3-7c90fc7c2939
topic_type:
- apiref
ms.openlocfilehash: 966494bbabaca99b6b5168db6fb7616c15c537e1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711669"
---
# <a name="icordebugbreakpointenumnext-method"></a><span data-ttu-id="b98c4-103">ICorDebugBreakpointEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="b98c4-103">ICorDebugBreakpointEnum::Next Method</span></span>

<span data-ttu-id="b98c4-104">从当前位置开始，从枚举中获取指定数量的 ICorDebugBreakpoint 实例。</span><span class="sxs-lookup"><span data-stu-id="b98c4-104">Gets the specified number of ICorDebugBreakpoint instances from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b98c4-105">语法</span><span class="sxs-lookup"><span data-stu-id="b98c4-105">Syntax</span></span>  
  
```cpp  
HRESULT Next (  
    [in] ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugBreakpoint *breakpoints[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b98c4-106">参数</span><span class="sxs-lookup"><span data-stu-id="b98c4-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="b98c4-107">中 `ICorDebugBreakpoint` 要检索的实例数。</span><span class="sxs-lookup"><span data-stu-id="b98c4-107">[in] The number of `ICorDebugBreakpoint` instances to be retrieved.</span></span>  
  
 `breakpoints`  
 <span data-ttu-id="b98c4-108">弄指针的数组，其中每个都指向 `ICorDebugBreakpoint` 表示断点的对象。</span><span class="sxs-lookup"><span data-stu-id="b98c4-108">[out] An array of pointers, each of which points to an `ICorDebugBreakpoint` object that represents a breakpoint.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="b98c4-109">弄一个指针，指向 `ICorDebugBreakpoint` 实际返回的实例数。</span><span class="sxs-lookup"><span data-stu-id="b98c4-109">[out] A pointer to the number of `ICorDebugBreakpoint` instances actually returned.</span></span> <span data-ttu-id="b98c4-110">如果为1，则此值可以为 null `celt` 。</span><span class="sxs-lookup"><span data-stu-id="b98c4-110">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b98c4-111">要求</span><span class="sxs-lookup"><span data-stu-id="b98c4-111">Requirements</span></span>  

 <span data-ttu-id="b98c4-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b98c4-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b98c4-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b98c4-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b98c4-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b98c4-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b98c4-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b98c4-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
