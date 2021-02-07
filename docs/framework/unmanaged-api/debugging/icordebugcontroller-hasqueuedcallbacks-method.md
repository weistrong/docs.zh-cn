---
description: 了解详细信息： ICorDebugController：： HasQueuedCallbacks 方法
title: ICorDebugController::HasQueuedCallbacks 方法
ms.date: 03/30/2017
api_name:
- ICorDebugController.HasQueuedCallbacks
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::HasQueuedCallbacks
helpviewer_keywords:
- HasQueuedCallbacks method [.NET Framework debugging]
- ICorDebugController::HasQueuedCallbacks method [.NET Framework debugging]
ms.assetid: 0d6a1cd9-370b-4462-adbf-e3980e897ea7
topic_type:
- apiref
ms.openlocfilehash: bdc22831b912d3bad565b6abf5c73591d07ffe11
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99764630"
---
# <a name="icordebugcontrollerhasqueuedcallbacks-method"></a><span data-ttu-id="14645-103">ICorDebugController::HasQueuedCallbacks 方法</span><span class="sxs-lookup"><span data-stu-id="14645-103">ICorDebugController::HasQueuedCallbacks Method</span></span>

<span data-ttu-id="14645-104">获取一个值，该值指示当前是否为指定线程排队任何托管回调。</span><span class="sxs-lookup"><span data-stu-id="14645-104">Gets a value that indicates whether any managed callbacks are currently queued for the specified thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="14645-105">语法</span><span class="sxs-lookup"><span data-stu-id="14645-105">Syntax</span></span>  
  
```cpp  
HRESULT HasQueuedCallbacks (  
    [in] ICorDebugThread *pThread,  
    [out] BOOL           *pbQueued  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="14645-106">参数</span><span class="sxs-lookup"><span data-stu-id="14645-106">Parameters</span></span>  

 `pThread`  
 <span data-ttu-id="14645-107">中指向表示线程的 "ICorDebugThread" 对象的指针。</span><span class="sxs-lookup"><span data-stu-id="14645-107">[in] A pointer to an "ICorDebugThread" object that represents the thread.</span></span>  
  
 `pbQueued`  
 <span data-ttu-id="14645-108">弄一个指向值的指针，该值为 `true` ; 如果当前为指定线程排队，则该值为; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="14645-108">[out] A pointer to a value that is `true` if any managed callbacks are currently queued for the specified thread; otherwise, `false`.</span></span>  
  
 <span data-ttu-id="14645-109">如果为该参数指定了 null `pThread` ，则 `HasQueuedCallbacks` 将返回， `true` 如果当前有托管的回调排队等候任何线程。</span><span class="sxs-lookup"><span data-stu-id="14645-109">If null is specified for the `pThread` parameter, `HasQueuedCallbacks` will return `true` if there are currently managed callbacks queued for any thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="14645-110">备注</span><span class="sxs-lookup"><span data-stu-id="14645-110">Remarks</span></span>  

 <span data-ttu-id="14645-111">每次都将调度一个回调，每次调用 [ICorDebugController：： Continue](icordebugcontroller-continue-method.md) 。</span><span class="sxs-lookup"><span data-stu-id="14645-111">Callbacks will be dispatched one at a time, each time [ICorDebugController::Continue](icordebugcontroller-continue-method.md) is called.</span></span> <span data-ttu-id="14645-112">如果要报告同时发生的多个调试事件，则调试器可以检查此标志。</span><span class="sxs-lookup"><span data-stu-id="14645-112">The debugger can check this flag if it wants to report multiple debugging events that occur simultaneously.</span></span>  
  
 <span data-ttu-id="14645-113">调试事件排队后，它们已发生，因此调试器必须释放整个队列，才能确保调试对象的状态。</span><span class="sxs-lookup"><span data-stu-id="14645-113">When debugging events are queued, they have already occurred, so the debugger must drain the entire queue to be sure of the state of the debuggee.</span></span> <span data-ttu-id="14645-114">`ICorDebugController::Continue`用于排出队列的 (调用 ) 。例如，如果队列在线程 *x* 上包含两个调试事件，并且调试器在第一个调试事件之后挂起线程 *x* ，然后调用 `ICorDebugController::Continue` ，则线程 *x* 的第二个调试事件会在线程已挂起的情况下进行调度。</span><span class="sxs-lookup"><span data-stu-id="14645-114">(Call `ICorDebugController::Continue` to drain the queue.) For example, if the queue contains two debugging events on thread *X*, and the debugger suspends thread *X* after the first debugging event and then calls `ICorDebugController::Continue`, the second debugging event for thread *X* will be dispatched although the thread has been suspended.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="14645-115">要求</span><span class="sxs-lookup"><span data-stu-id="14645-115">Requirements</span></span>  

 <span data-ttu-id="14645-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="14645-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="14645-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="14645-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="14645-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="14645-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="14645-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="14645-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="14645-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="14645-120">See also</span></span>
