---
description: 了解详细信息： ICorProfilerCallback：： RuntimeThreadSuspended 方法
title: ICorProfilerCallback::RuntimeThreadSuspended 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RuntimeThreadSuspended
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RuntimeThreadSuspended
helpviewer_keywords:
- RuntimeThreadSuspended method [.NET Framework profiling]
- ICorProfilerCallback::RuntimeThreadSuspended method [.NET Framework profiling]
ms.assetid: de830a8b-6ee1-4900-ace3-4237108f6b12
topic_type:
- apiref
ms.openlocfilehash: f7c2f5baf5a320375d9a2606ca05b13d522336be
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99657328"
---
# <a name="icorprofilercallbackruntimethreadsuspended-method"></a><span data-ttu-id="9cbe3-103">ICorProfilerCallback::RuntimeThreadSuspended 方法</span><span class="sxs-lookup"><span data-stu-id="9cbe3-103">ICorProfilerCallback::RuntimeThreadSuspended Method</span></span>

<span data-ttu-id="9cbe3-104">通知探查器指定的线程已挂起或将要挂起。</span><span class="sxs-lookup"><span data-stu-id="9cbe3-104">Notifies the profiler that the specified thread has been suspended or is about to be suspended.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9cbe3-105">语法</span><span class="sxs-lookup"><span data-stu-id="9cbe3-105">Syntax</span></span>  
  
```cpp  
HRESULT RuntimeThreadSuspended(  
    [in] ThreadID threadId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9cbe3-106">参数</span><span class="sxs-lookup"><span data-stu-id="9cbe3-106">Parameters</span></span>  

 `threadId`  
 <span data-ttu-id="9cbe3-107">中已挂起的线程的 ID。</span><span class="sxs-lookup"><span data-stu-id="9cbe3-107">[in] The ID of the thread that has been suspended.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9cbe3-108">备注</span><span class="sxs-lookup"><span data-stu-id="9cbe3-108">Remarks</span></span>  

 <span data-ttu-id="9cbe3-109">在 `RuntimeThreadSuspended` [ICorProfilerCallback：： RuntimeSuspendStarted](icorprofilercallback-runtimesuspendstarted-method.md) 与关联的 [ICorProfilerCallback：： RuntimeResumeStarted](icorprofilercallback-runtimeresumestarted-method.md) 回调之间随时会发生通知。</span><span class="sxs-lookup"><span data-stu-id="9cbe3-109">The `RuntimeThreadSuspended` notification can occur any time between the [ICorProfilerCallback::RuntimeSuspendStarted](icorprofilercallback-runtimesuspendstarted-method.md) and the associated [ICorProfilerCallback::RuntimeResumeStarted](icorprofilercallback-runtimeresumestarted-method.md) callbacks.</span></span> <span data-ttu-id="9cbe3-110">在 [ICorProfilerCallback：： RuntimeSuspendFinished](icorprofilercallback-runtimesuspendfinished-method.md) 之间发生的通知， `RuntimeResumeStarted` 适用于已在非托管代码中运行并在进入运行时时挂起的线程。</span><span class="sxs-lookup"><span data-stu-id="9cbe3-110">Notifications that occur between [ICorProfilerCallback::RuntimeSuspendFinished](icorprofilercallback-runtimesuspendfinished-method.md) and `RuntimeResumeStarted` are for threads that had been running in unmanaged code and were suspended upon entry to the runtime.</span></span>  
  
 <span data-ttu-id="9cbe3-111">通常，此回调恰好在挂起线程之后发生。</span><span class="sxs-lookup"><span data-stu-id="9cbe3-111">Generally, this callback occurs just after a thread is suspended.</span></span> <span data-ttu-id="9cbe3-112">但是，如果当前正在执行的线程 (调用此回调的线程) 为挂起的线程，则该回调将在线程挂起之前发生。</span><span class="sxs-lookup"><span data-stu-id="9cbe3-112">However, if the currently executing thread (the thread that called this callback) is the one that is being suspended, this callback will occur just before the thread is suspended.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9cbe3-113">要求</span><span class="sxs-lookup"><span data-stu-id="9cbe3-113">Requirements</span></span>  

 <span data-ttu-id="9cbe3-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9cbe3-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9cbe3-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="9cbe3-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="9cbe3-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9cbe3-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9cbe3-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9cbe3-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9cbe3-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="9cbe3-118">See also</span></span>

- [<span data-ttu-id="9cbe3-119">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="9cbe3-119">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="9cbe3-120">RuntimeThreadResumed 方法</span><span class="sxs-lookup"><span data-stu-id="9cbe3-120">RuntimeThreadResumed Method</span></span>](icorprofilercallback-runtimethreadresumed-method.md)
