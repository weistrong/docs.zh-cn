---
description: 了解详细信息： ICorDebugStackWalk：： SetContext 方法
title: ICorDebugStackWalk::SetContext 方法
ms.date: 03/30/2017
api_name:
- ICorDebugStackWalk.SetContext Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStackWalk::SetContext
helpviewer_keywords:
- SetContext method [.NET Framework debugging]
- ICorDebugStackWalk::SetContext method [.NET Framework debugging]
ms.assetid: bac0b156-31a3-4e7f-be4d-ab21789c81f1
topic_type:
- apiref
ms.openlocfilehash: 20e18460d237a63e4c2695b9e7cbfa766ed3908f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794710"
---
# <a name="icordebugstackwalksetcontext-method"></a><span data-ttu-id="2b3a3-103">ICorDebugStackWalk::SetContext 方法</span><span class="sxs-lookup"><span data-stu-id="2b3a3-103">ICorDebugStackWalk::SetContext Method</span></span>

<span data-ttu-id="2b3a3-104">将 [ICorDebugStackWalk](icordebugstackwalk-interface.md) 对象的当前上下文设置为线程的有效上下文。</span><span class="sxs-lookup"><span data-stu-id="2b3a3-104">Sets the [ICorDebugStackWalk](icordebugstackwalk-interface.md) object’s current context to a valid context for the thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2b3a3-105">语法</span><span class="sxs-lookup"><span data-stu-id="2b3a3-105">Syntax</span></span>  
  
```cpp  
HRESULT SetContext([in] CorDebugSetContextFlag flag,  
                   [in] ULONG32 contextSize,  
                   [in, size_is(contextSize)] BYTE context[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2b3a3-106">参数</span><span class="sxs-lookup"><span data-stu-id="2b3a3-106">Parameters</span></span>  

 `flag`  
 <span data-ttu-id="2b3a3-107">中 [CorDebugSetContextFlag](cordebugsetcontextflag-enumeration.md) 标志，用于指示上下文是否来自堆栈上的活动帧，或通过展开堆栈获取的上下文。</span><span class="sxs-lookup"><span data-stu-id="2b3a3-107">[in] A [CorDebugSetContextFlag](cordebugsetcontextflag-enumeration.md) flag that indicates whether the context is from the active frame on the stack, or a context obtained by unwinding the stack.</span></span>  
  
 `contextSize`  
 <span data-ttu-id="2b3a3-108">中缓冲区的已分配大小 `CONTEXT` 。</span><span class="sxs-lookup"><span data-stu-id="2b3a3-108">[in] The allocated size of the `CONTEXT` buffer.</span></span>  
  
 `context`  
 <span data-ttu-id="2b3a3-109">中 `CONTEXT` 缓冲区。</span><span class="sxs-lookup"><span data-stu-id="2b3a3-109">[in] The `CONTEXT` buffer.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2b3a3-110">返回值</span><span class="sxs-lookup"><span data-stu-id="2b3a3-110">Return Value</span></span>  

 <span data-ttu-id="2b3a3-111">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="2b3a3-111">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="2b3a3-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="2b3a3-112">HRESULT</span></span>|<span data-ttu-id="2b3a3-113">说明</span><span class="sxs-lookup"><span data-stu-id="2b3a3-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="2b3a3-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="2b3a3-114">S_OK</span></span>|<span data-ttu-id="2b3a3-115">`ICorDebugStackWalk`已成功设置对象的上下文。</span><span class="sxs-lookup"><span data-stu-id="2b3a3-115">The `ICorDebugStackWalk` object's context was successfully set.</span></span>|  
|<span data-ttu-id="2b3a3-116">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="2b3a3-116">E_FAIL</span></span>|<span data-ttu-id="2b3a3-117">`ICorDebugStackWalk`未设置对象的上下文。</span><span class="sxs-lookup"><span data-stu-id="2b3a3-117">The `ICorDebugStackWalk` object's context was not set.</span></span>|  
|<span data-ttu-id="2b3a3-118">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="2b3a3-118">E_INVALIDARG</span></span>|<span data-ttu-id="2b3a3-119">上下文为 null。</span><span class="sxs-lookup"><span data-stu-id="2b3a3-119">The context is null.</span></span>|  
|<span data-ttu-id="2b3a3-120">HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</span><span class="sxs-lookup"><span data-stu-id="2b3a3-120">HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</span></span>|<span data-ttu-id="2b3a3-121">上下文缓冲区太小。</span><span class="sxs-lookup"><span data-stu-id="2b3a3-121">The context buffer is too small.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="2b3a3-122">例外</span><span class="sxs-lookup"><span data-stu-id="2b3a3-122">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2b3a3-123">备注</span><span class="sxs-lookup"><span data-stu-id="2b3a3-123">Remarks</span></span>  

 <span data-ttu-id="2b3a3-124">此方法不会更改线程的当前上下文。</span><span class="sxs-lookup"><span data-stu-id="2b3a3-124">This method does not alter the current context of the thread.</span></span>  
  
 <span data-ttu-id="2b3a3-125">将当前上下文设置为无效上下文可能会导致堆栈查看程序产生不可预知的结果。</span><span class="sxs-lookup"><span data-stu-id="2b3a3-125">Setting the current context to an invalid context may cause unpredictable results from the stack walker.</span></span>  
  
 <span data-ttu-id="2b3a3-126">可以通过立即调用 [ICorDebugStackWalk：： GetContext](icordebugstackwalk-getcontext-method.md) 方法来检索此上下文的精确按位副本。</span><span class="sxs-lookup"><span data-stu-id="2b3a3-126">You can retrieve an exact bitwise copy of this context by immediately calling the [ICorDebugStackWalk::GetContext](icordebugstackwalk-getcontext-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2b3a3-127">要求</span><span class="sxs-lookup"><span data-stu-id="2b3a3-127">Requirements</span></span>  

 <span data-ttu-id="2b3a3-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2b3a3-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2b3a3-129">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2b3a3-129">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2b3a3-130">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2b3a3-130">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2b3a3-131">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2b3a3-131">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2b3a3-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="2b3a3-132">See also</span></span>

- [<span data-ttu-id="2b3a3-133">调试接口</span><span class="sxs-lookup"><span data-stu-id="2b3a3-133">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="2b3a3-134">调试</span><span class="sxs-lookup"><span data-stu-id="2b3a3-134">Debugging</span></span>](index.md)
