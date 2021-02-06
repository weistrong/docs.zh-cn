---
description: 了解详细信息： ICorDebugThread：： SetDebugState 方法
title: ICorDebugThread::SetDebugState 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread.SetDebugState
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::SetDebugState
helpviewer_keywords:
- ICorDebugThread::SetDebugState method [.NET Framework debugging]
- SetDebugState method [.NET Framework debugging]
ms.assetid: 6382bdf6-d488-4952-b653-cb09b6e1c6c2
topic_type:
- apiref
ms.openlocfilehash: 40339cbce8d30617738151c0a32466c2361e3a14
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99658797"
---
# <a name="icordebugthreadsetdebugstate-method"></a><span data-ttu-id="62a59-103">ICorDebugThread::SetDebugState 方法</span><span class="sxs-lookup"><span data-stu-id="62a59-103">ICorDebugThread::SetDebugState Method</span></span>

<span data-ttu-id="62a59-104">设置描述此 ICorDebugThread 的调试状态的标志。</span><span class="sxs-lookup"><span data-stu-id="62a59-104">Sets flags that describe the debugging state of this ICorDebugThread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="62a59-105">语法</span><span class="sxs-lookup"><span data-stu-id="62a59-105">Syntax</span></span>  
  
```cpp  
HRESULT SetDebugState (  
    [in] CorDebugThreadState state  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="62a59-106">参数</span><span class="sxs-lookup"><span data-stu-id="62a59-106">Parameters</span></span>  

 `state`  
 <span data-ttu-id="62a59-107">中CorDebugThreadState 枚举值的按位组合，用于指定此线程的调试状态。</span><span class="sxs-lookup"><span data-stu-id="62a59-107">[in] A bitwise combination of CorDebugThreadState enumeration values that specify the debugging state of this thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="62a59-108">备注</span><span class="sxs-lookup"><span data-stu-id="62a59-108">Remarks</span></span>  

 <span data-ttu-id="62a59-109">`SetDebugState` 设置线程的当前调试状态。</span><span class="sxs-lookup"><span data-stu-id="62a59-109">`SetDebugState` sets the current debug state of the thread.</span></span> <span data-ttu-id="62a59-110"> ("当前调试状态" 表示调试状态（如果进程继续），而不是实际的当前状态。 ) 此的正常值 THREAD_RUN 为。</span><span class="sxs-lookup"><span data-stu-id="62a59-110">(The "current debug state" represents the debug state if the process were to be continued, not the actual current state.) The normal value for this is THREAD_RUN.</span></span> <span data-ttu-id="62a59-111">只有调试器才能影响线程的调试状态。</span><span class="sxs-lookup"><span data-stu-id="62a59-111">Only the debugger can affect the debug state of a thread.</span></span> <span data-ttu-id="62a59-112">调试状态完成最后一步，因此，如果想要使某个线程在多个继续 THREAD_SUSPENDed，则可以将其设置一次，这样就无需担心。</span><span class="sxs-lookup"><span data-stu-id="62a59-112">Debug states do last across continues, so if you want to keep a thread THREAD_SUSPENDed over multiple continues, you can set it once and thereafter not have to worry about it.</span></span> <span data-ttu-id="62a59-113">挂起线程并恢复进程可能会导致死锁，但通常不太可能。</span><span class="sxs-lookup"><span data-stu-id="62a59-113">Suspending threads and resuming the process can cause deadlocks, though it's usually unlikely.</span></span> <span data-ttu-id="62a59-114">这是线程和进程的内部质量，并按设计进行。</span><span class="sxs-lookup"><span data-stu-id="62a59-114">This is an intrinsic quality of threads and processes and is by-design.</span></span> <span data-ttu-id="62a59-115">调试器可以异步中断和恢复线程以中断死锁。</span><span class="sxs-lookup"><span data-stu-id="62a59-115">A debugger can asynchronously break and resume the threads to break the deadlock.</span></span> <span data-ttu-id="62a59-116">如果该线程的用户状态包括 USER_UNSAFE_POINT，则该线程可能会阻止垃圾回收 (垃圾回收) 。</span><span class="sxs-lookup"><span data-stu-id="62a59-116">If the thread's user state includes USER_UNSAFE_POINT, then the thread may block a garbage collection (GC).</span></span> <span data-ttu-id="62a59-117">这意味着暂停的线程可能会导致死锁。</span><span class="sxs-lookup"><span data-stu-id="62a59-117">This means the suspended thread has a much higher chance of causing a deadlock.</span></span> <span data-ttu-id="62a59-118">这不会影响已排队的调试事件。</span><span class="sxs-lookup"><span data-stu-id="62a59-118">This may not affect debug events already queued.</span></span> <span data-ttu-id="62a59-119">因此，在挂起或恢复线程之前，调试程序应该通过调用 [ICorDebugController：： HasQueuedCallbacks](icordebugcontroller-hasqueuedcallbacks-method.md)) 来释放整个事件队列 (。</span><span class="sxs-lookup"><span data-stu-id="62a59-119">Thus a debugger should drain the entire event queue (by calling [ICorDebugController::HasQueuedCallbacks](icordebugcontroller-hasqueuedcallbacks-method.md)) before suspending or resuming threads.</span></span> <span data-ttu-id="62a59-120">否则，它可能会在其认为已挂起的线程上获取事件。</span><span class="sxs-lookup"><span data-stu-id="62a59-120">Else it may get events on a thread that it believes it has already suspended.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="62a59-121">要求</span><span class="sxs-lookup"><span data-stu-id="62a59-121">Requirements</span></span>  

 <span data-ttu-id="62a59-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="62a59-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="62a59-123">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="62a59-123">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="62a59-124">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="62a59-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="62a59-125">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="62a59-125">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
