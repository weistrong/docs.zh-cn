---
description: 了解详细信息： ICorDebugStackWalk：： GetFrame 方法
title: ICorDebugStackWalk::GetFrame 方法
ms.date: 03/30/2017
api_name:
- ICorDebugStackWalk.GetFrame Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStackWalk::GetFrame
helpviewer_keywords:
- GetFrame method [.NET Framework debugging]
- ICorDebugStackWalk::GetFrame method [.NET Framework debugging]
ms.assetid: 4083b505-5b59-44fb-8c5d-129db6a96c10
topic_type:
- apiref
ms.openlocfilehash: b00ddb6a475aff4263a922f5a20b866cd0e1b2ed
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794736"
---
# <a name="icordebugstackwalkgetframe-method"></a><span data-ttu-id="fd021-103">ICorDebugStackWalk::GetFrame 方法</span><span class="sxs-lookup"><span data-stu-id="fd021-103">ICorDebugStackWalk::GetFrame Method</span></span>

<span data-ttu-id="fd021-104">获取 [ICorDebugStackWalk](icordebugstackwalk-interface.md) 对象中的当前帧。</span><span class="sxs-lookup"><span data-stu-id="fd021-104">Gets the current frame in the [ICorDebugStackWalk](icordebugstackwalk-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fd021-105">语法</span><span class="sxs-lookup"><span data-stu-id="fd021-105">Syntax</span></span>  
  
```cpp  
HRESULT GetFrame([out] ICorDebugFrame ** pFrame);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fd021-106">参数</span><span class="sxs-lookup"><span data-stu-id="fd021-106">Parameters</span></span>  

 `pFrame`  
 <span data-ttu-id="fd021-107">中指向所创建的帧对象的地址的指针，该对象表示堆栈中的当前帧。</span><span class="sxs-lookup"><span data-stu-id="fd021-107">[in] A pointer to the address of the created frame object that represents the current frame in the stack.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fd021-108">返回值</span><span class="sxs-lookup"><span data-stu-id="fd021-108">Return Value</span></span>  

 <span data-ttu-id="fd021-109">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="fd021-109">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="fd021-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="fd021-110">HRESULT</span></span>|<span data-ttu-id="fd021-111">说明</span><span class="sxs-lookup"><span data-stu-id="fd021-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="fd021-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="fd021-112">S_OK</span></span>|<span data-ttu-id="fd021-113">运行时成功返回了当前帧。</span><span class="sxs-lookup"><span data-stu-id="fd021-113">The runtime successfully returned the current frame.</span></span>|  
|<span data-ttu-id="fd021-114">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="fd021-114">E_FAIL</span></span>|<span data-ttu-id="fd021-115">当前帧未返回。</span><span class="sxs-lookup"><span data-stu-id="fd021-115">The current frame was not returned.</span></span>|  
|<span data-ttu-id="fd021-116">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="fd021-116">S_FALSE</span></span>|<span data-ttu-id="fd021-117">当前帧是本机堆栈帧。</span><span class="sxs-lookup"><span data-stu-id="fd021-117">The current frame is a native stack frame.</span></span>|  
|<span data-ttu-id="fd021-118">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="fd021-118">E_INVALIDARG</span></span>|<span data-ttu-id="fd021-119">`pFrame` 为 null。</span><span class="sxs-lookup"><span data-stu-id="fd021-119">`pFrame` is null.</span></span>|  
|<span data-ttu-id="fd021-120">CORDBG_E_PAST_END_OF_STACK</span><span class="sxs-lookup"><span data-stu-id="fd021-120">CORDBG_E_PAST_END_OF_STACK</span></span>|<span data-ttu-id="fd021-121">帧指针已位于堆栈末尾;因此，不能访问其他帧。</span><span class="sxs-lookup"><span data-stu-id="fd021-121">The frame pointer is already at the end of the stack; therefore, no additional frames can be accessed.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="fd021-122">例外</span><span class="sxs-lookup"><span data-stu-id="fd021-122">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fd021-123">备注</span><span class="sxs-lookup"><span data-stu-id="fd021-123">Remarks</span></span>  

 <span data-ttu-id="fd021-124">`ICorDebugStackWalk` 仅返回实际的堆栈帧。</span><span class="sxs-lookup"><span data-stu-id="fd021-124">`ICorDebugStackWalk` returns only actual stack frames.</span></span> <span data-ttu-id="fd021-125">使用 [ICorDebugThread3：： GetActiveInternalFrames](icordebugthread3-getactiveinternalframes-method.md) 方法返回内部帧。</span><span class="sxs-lookup"><span data-stu-id="fd021-125">Use the [ICorDebugThread3::GetActiveInternalFrames](icordebugthread3-getactiveinternalframes-method.md) method to return internal frames.</span></span> <span data-ttu-id="fd021-126"> (内部帧是由运行时推送到堆栈上的数据结构，用于存储临时数据。 ) </span><span class="sxs-lookup"><span data-stu-id="fd021-126">(Internal frames are data structures pushed onto the stack by the runtime to store temporary data.)</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fd021-127">要求</span><span class="sxs-lookup"><span data-stu-id="fd021-127">Requirements</span></span>  

 <span data-ttu-id="fd021-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fd021-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fd021-129">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fd021-129">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fd021-130">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fd021-130">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fd021-131">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fd021-131">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fd021-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="fd021-132">See also</span></span>

- [<span data-ttu-id="fd021-133">ICorDebugStackWalk 接口</span><span class="sxs-lookup"><span data-stu-id="fd021-133">ICorDebugStackWalk Interface</span></span>](icordebugstackwalk-interface.md)
- [<span data-ttu-id="fd021-134">调试接口</span><span class="sxs-lookup"><span data-stu-id="fd021-134">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="fd021-135">调试</span><span class="sxs-lookup"><span data-stu-id="fd021-135">Debugging</span></span>](index.md)
