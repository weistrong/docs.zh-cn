---
description: 了解详细信息： ICorDebugStepperEnum：： Next 方法
title: ICorDebugStepperEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugStepperEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepperEnum::Next
helpviewer_keywords:
- Next method, ICorDebugStepperEnum interface [.NET Framework debugging]
- ICorDebugStepperEnum::Next method [.NET Framework debugging]
ms.assetid: d0ea0f30-e8d2-48b0-8477-e1a029ceb4dd
topic_type:
- apiref
ms.openlocfilehash: e0c17fbc570d5ea8a4a56c89a5a2c855ed045bd7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99717428"
---
# <a name="icordebugstepperenumnext-method"></a><span data-ttu-id="58ab3-103">ICorDebugStepperEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="58ab3-103">ICorDebugStepperEnum::Next Method</span></span>

<span data-ttu-id="58ab3-104">从当前位置开始，从枚举中获取指定数量的 ICorDebugStepper 实例。</span><span class="sxs-lookup"><span data-stu-id="58ab3-104">Gets the specified number of ICorDebugStepper instances from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="58ab3-105">语法</span><span class="sxs-lookup"><span data-stu-id="58ab3-105">Syntax</span></span>  
  
```cpp  
HRESULT Next(  
    [in] ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugStepper *steppers[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="58ab3-106">参数</span><span class="sxs-lookup"><span data-stu-id="58ab3-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="58ab3-107">中 `ICorDebugStepper` 要检索的实例数。</span><span class="sxs-lookup"><span data-stu-id="58ab3-107">[in] The number of `ICorDebugStepper` instances to be retrieved.</span></span>  
  
 `steppers`  
 <span data-ttu-id="58ab3-108">弄指针的数组，其中每个都指向一个 `ICorDebugStepper` 对象。</span><span class="sxs-lookup"><span data-stu-id="58ab3-108">[out] An array of pointers, each of which points to an `ICorDebugStepper` object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="58ab3-109">弄一个指针，指向 `ICorDebugStepper` 实际返回的实例数。</span><span class="sxs-lookup"><span data-stu-id="58ab3-109">[out] Pointer to the number of `ICorDebugStepper` instances actually returned.</span></span> <span data-ttu-id="58ab3-110">如果为1，则此值可以为 null `celt` 。</span><span class="sxs-lookup"><span data-stu-id="58ab3-110">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="58ab3-111">要求</span><span class="sxs-lookup"><span data-stu-id="58ab3-111">Requirements</span></span>  

 <span data-ttu-id="58ab3-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="58ab3-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="58ab3-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="58ab3-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="58ab3-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="58ab3-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="58ab3-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="58ab3-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
