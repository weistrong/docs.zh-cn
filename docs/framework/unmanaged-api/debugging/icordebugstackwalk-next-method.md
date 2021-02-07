---
description: 了解详细信息： ICorDebugStackWalk：： Next 方法
title: ICorDebugStackWalk::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugStackWalk.Next Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStackWalk::Next
helpviewer_keywords:
- ICorDebugStackWalk::Next method [.NET Framework debugging]
- Next method, ICorDebugStackWalk interface [.NET Framework debugging]
ms.assetid: 189c36be-028c-4fba-a002-5edfb8fcd07f
topic_type:
- apiref
ms.openlocfilehash: 27a48ca40f6b43cae32511b71b73e68d88eb60c0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99717753"
---
# <a name="icordebugstackwalknext-method"></a><span data-ttu-id="788e8-103">ICorDebugStackWalk::Next 方法</span><span class="sxs-lookup"><span data-stu-id="788e8-103">ICorDebugStackWalk::Next Method</span></span>

<span data-ttu-id="788e8-104">将 [ICorDebugStackWalk](icordebugstackwalk-interface.md) 对象移动到下一帧。</span><span class="sxs-lookup"><span data-stu-id="788e8-104">Moves the [ICorDebugStackWalk](icordebugstackwalk-interface.md) object to the next frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="788e8-105">语法</span><span class="sxs-lookup"><span data-stu-id="788e8-105">Syntax</span></span>  
  
```cpp  
HRESULT Next();  
```  
  
## <a name="return-value"></a><span data-ttu-id="788e8-106">返回值</span><span class="sxs-lookup"><span data-stu-id="788e8-106">Return Value</span></span>  

 <span data-ttu-id="788e8-107">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="788e8-107">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="788e8-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="788e8-108">HRESULT</span></span>|<span data-ttu-id="788e8-109">说明</span><span class="sxs-lookup"><span data-stu-id="788e8-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="788e8-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="788e8-110">S_OK</span></span>|<span data-ttu-id="788e8-111">运行时成功地展开到下一帧 (参阅备注) 。</span><span class="sxs-lookup"><span data-stu-id="788e8-111">The runtime successfully unwound to the next frame (see Remarks).</span></span>|  
|<span data-ttu-id="788e8-112">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="788e8-112">E_FAIL</span></span>|<span data-ttu-id="788e8-113">`ICorDebugStackWalk`对象不能是高级对象。</span><span class="sxs-lookup"><span data-stu-id="788e8-113">The `ICorDebugStackWalk` object could not be advanced.</span></span>|  
|<span data-ttu-id="788e8-114">CORDBG_S_AT_END_OF_STACK</span><span class="sxs-lookup"><span data-stu-id="788e8-114">CORDBG_S_AT_END_OF_STACK</span></span>|<span data-ttu-id="788e8-115">由于此展开导致堆栈结束。</span><span class="sxs-lookup"><span data-stu-id="788e8-115">The end of the stack was reached as a result of this unwind.</span></span>|  
|<span data-ttu-id="788e8-116">CORDBG_E_PAST_END_OF_STACK</span><span class="sxs-lookup"><span data-stu-id="788e8-116">CORDBG_E_PAST_END_OF_STACK</span></span>|<span data-ttu-id="788e8-117">帧指针已位于堆栈末尾;因此，不能访问其他帧。</span><span class="sxs-lookup"><span data-stu-id="788e8-117">The frame pointer is already at the end of the stack; therefore, no additional frames can be accessed.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="788e8-118">例外</span><span class="sxs-lookup"><span data-stu-id="788e8-118">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="788e8-119">备注</span><span class="sxs-lookup"><span data-stu-id="788e8-119">Remarks</span></span>  

 <span data-ttu-id="788e8-120">`Next` `ICorDebugStackWalk` 仅当运行时可以展开当前帧时，方法才将对象前进到调用帧。</span><span class="sxs-lookup"><span data-stu-id="788e8-120">The `Next` method advances the `ICorDebugStackWalk` object to the calling frame only if the runtime can unwind the current frame.</span></span> <span data-ttu-id="788e8-121">否则，对象会前进到运行时能够展开的下一帧。</span><span class="sxs-lookup"><span data-stu-id="788e8-121">Otherwise, the object advances to the next frame that the runtime is able to unwind.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="788e8-122">要求</span><span class="sxs-lookup"><span data-stu-id="788e8-122">Requirements</span></span>  

 <span data-ttu-id="788e8-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="788e8-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="788e8-124">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="788e8-124">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="788e8-125">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="788e8-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="788e8-126">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="788e8-126">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="788e8-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="788e8-127">See also</span></span>

- [<span data-ttu-id="788e8-128">ICorDebugStackWalk 接口</span><span class="sxs-lookup"><span data-stu-id="788e8-128">ICorDebugStackWalk Interface</span></span>](icordebugstackwalk-interface.md)
- [<span data-ttu-id="788e8-129">调试接口</span><span class="sxs-lookup"><span data-stu-id="788e8-129">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="788e8-130">调试</span><span class="sxs-lookup"><span data-stu-id="788e8-130">Debugging</span></span>](index.md)
