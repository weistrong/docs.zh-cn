---
description: 了解详细信息： ICLRTask 接口
title: ICLRTask 接口
ms.date: 03/30/2017
api_name:
- ICLRTask
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask
helpviewer_keywords:
- ICLRTask interface [.NET Framework hosting]
ms.assetid: b3a44df3-578a-4451-b55e-70c8e7695f5e
topic_type:
- apiref
ms.openlocfilehash: f48216b19dd2c1d0d0ba64117169b74767dbdf2b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799522"
---
# <a name="iclrtask-interface"></a><span data-ttu-id="3268a-103">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="3268a-103">ICLRTask Interface</span></span>

<span data-ttu-id="3268a-104">提供一些方法，这些方法允许宿主向 clr)  (公共语言运行时，或向 CLR 提供有关关联任务的通知。</span><span class="sxs-lookup"><span data-stu-id="3268a-104">Provides methods that allow the host to make requests of the common language runtime (CLR), or to provide notification to the CLR about the associated task.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3268a-105">方法</span><span class="sxs-lookup"><span data-stu-id="3268a-105">Methods</span></span>  
  
|<span data-ttu-id="3268a-106">方法</span><span class="sxs-lookup"><span data-stu-id="3268a-106">Method</span></span>|<span data-ttu-id="3268a-107">说明</span><span class="sxs-lookup"><span data-stu-id="3268a-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3268a-108">Abort 方法</span><span class="sxs-lookup"><span data-stu-id="3268a-108">Abort Method</span></span>](iclrtask-abort-method.md)|<span data-ttu-id="3268a-109">请求 CLR 中止当前 `ICLRTask` 实例表示的任务。</span><span class="sxs-lookup"><span data-stu-id="3268a-109">Requests that the CLR abort the task that the current `ICLRTask` instance represents.</span></span>|  
|[<span data-ttu-id="3268a-110">ExitTask 方法</span><span class="sxs-lookup"><span data-stu-id="3268a-110">ExitTask Method</span></span>](iclrtask-exittask-method.md)|<span data-ttu-id="3268a-111">通知 CLR 与当前实例关联的任务 `ICLRTask` 正在结束，并尝试正常关闭任务。</span><span class="sxs-lookup"><span data-stu-id="3268a-111">Notifies the CLR that the task associated with the current `ICLRTask` instance is ending, and attempts to shut the task down gracefully.</span></span>|  
|[<span data-ttu-id="3268a-112">GetMemStats 方法</span><span class="sxs-lookup"><span data-stu-id="3268a-112">GetMemStats Method</span></span>](iclrtask-getmemstats-method.md)|<span data-ttu-id="3268a-113">获取有关由当前实例表示的任务对内存资源的使用情况的统计信息 `ICLRTask` 。</span><span class="sxs-lookup"><span data-stu-id="3268a-113">Gets statistical information on the use of memory resources by the task represented by the current `ICLRTask` instance.</span></span>|  
|[<span data-ttu-id="3268a-114">LocksHeld 方法</span><span class="sxs-lookup"><span data-stu-id="3268a-114">LocksHeld Method</span></span>](iclrtask-locksheld-method.md)|<span data-ttu-id="3268a-115">获取任务当前持有的锁的数目。</span><span class="sxs-lookup"><span data-stu-id="3268a-115">Gets the number of locks currently held on the task.</span></span>|  
|[<span data-ttu-id="3268a-116">NeedsPriorityScheduling 方法</span><span class="sxs-lookup"><span data-stu-id="3268a-116">NeedsPriorityScheduling Method</span></span>](iclrtask-needspriorityscheduling-method.md)|<span data-ttu-id="3268a-117">获取一个值，该值指示宿主是否应分配高优先级来重新安排当前实例所表示的任务 `ICLRTask` 。</span><span class="sxs-lookup"><span data-stu-id="3268a-117">Gets a value indicating whether the host should assign a high priority to rescheduling the task represented by the current `ICLRTask` instance.</span></span>|  
|[<span data-ttu-id="3268a-118">Reset 方法</span><span class="sxs-lookup"><span data-stu-id="3268a-118">Reset Method</span></span>](iclrtask-reset-method.md)|<span data-ttu-id="3268a-119">通知 CLR 宿主已经完成了一个任务，并使 CLR 可以重复使用当前 `ICLRTask` 实例来表示其他任务。</span><span class="sxs-lookup"><span data-stu-id="3268a-119">Informs the CLR that the host has completed a task, and enables the CLR to reuse the current `ICLRTask` instance to represent another task.</span></span>|  
|[<span data-ttu-id="3268a-120">RudeAbort 方法</span><span class="sxs-lookup"><span data-stu-id="3268a-120">RudeAbort Method</span></span>](iclrtask-rudeabort-method.md)|<span data-ttu-id="3268a-121">使 CLR 立即中止当前实例表示的任务 `ICLRTask` ，而不保证将执行终结器。</span><span class="sxs-lookup"><span data-stu-id="3268a-121">Causes the CLR to abort the task represented by the current `ICLRTask` instance immediately, without a guarantee that finalizers will be executed.</span></span>|  
|[<span data-ttu-id="3268a-122">SetTaskIdentifier 方法</span><span class="sxs-lookup"><span data-stu-id="3268a-122">SetTaskIdentifier Method</span></span>](iclrtask-settaskidentifier-method.md)|<span data-ttu-id="3268a-123">为当前实例所表示的任务设置唯一标识符 `ICLRTask` ，以便在调试时使用。</span><span class="sxs-lookup"><span data-stu-id="3268a-123">Sets a unique identifier for the task represented by the current `ICLRTask` instance, for use in debugging.</span></span>|  
|[<span data-ttu-id="3268a-124">SwitchIn 方法</span><span class="sxs-lookup"><span data-stu-id="3268a-124">SwitchIn Method</span></span>](iclrtask-switchin-method.md)|<span data-ttu-id="3268a-125">向 CLR 通知当前实例表示的任务处于 `ICLRTask` 可使用状态。</span><span class="sxs-lookup"><span data-stu-id="3268a-125">Notifies the CLR that the task represented by the current `ICLRTask` instance is in an operable state.</span></span>|  
|[<span data-ttu-id="3268a-126">SwitchOut 方法</span><span class="sxs-lookup"><span data-stu-id="3268a-126">SwitchOut Method</span></span>](iclrtask-switchout-method.md)|<span data-ttu-id="3268a-127">通知 CLR 由当前实例表示的任务 `ICLRTask` 不再处于可使用状态。</span><span class="sxs-lookup"><span data-stu-id="3268a-127">Notifies the CLR that the task represented by the current `ICLRTask` instance is no longer in an operable state.</span></span>|  
|[<span data-ttu-id="3268a-128">YieldTask 方法</span><span class="sxs-lookup"><span data-stu-id="3268a-128">YieldTask Method</span></span>](iclrtask-yieldtask-method.md)|<span data-ttu-id="3268a-129">请求 CLR 使处理器时间可供其他任务使用。</span><span class="sxs-lookup"><span data-stu-id="3268a-129">Requests that the CLR make processor time available to other tasks.</span></span> <span data-ttu-id="3268a-130">CLR 不保证任务将处于可产生处理时间的状态。</span><span class="sxs-lookup"><span data-stu-id="3268a-130">The CLR makes no guarantee that the task will be put in a state where it can yield processing time.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3268a-131">备注</span><span class="sxs-lookup"><span data-stu-id="3268a-131">Remarks</span></span>  

 <span data-ttu-id="3268a-132">`ICLRTask`是 CLR 任务的表示形式。</span><span class="sxs-lookup"><span data-stu-id="3268a-132">An `ICLRTask` is the representation of a task for the CLR.</span></span> <span data-ttu-id="3268a-133">在代码执行过程中的任意时刻，都可以将任务描述为正在运行或等待运行。</span><span class="sxs-lookup"><span data-stu-id="3268a-133">At any point during code execution, a task can be described either as running or waiting to run.</span></span> <span data-ttu-id="3268a-134">宿主调用 `ICLRTask::SwitchIn` 方法，以通知 CLR 当前实例所表示的任务 `ICLRTask` 现在处于可使用状态。</span><span class="sxs-lookup"><span data-stu-id="3268a-134">The host calls the `ICLRTask::SwitchIn` method to notify the CLR that the task that the current `ICLRTask` instance represents is now in an operable state.</span></span> <span data-ttu-id="3268a-135">调用后 `ICLRTask::SwitchIn` ，宿主可以在任何操作系统线程上计划任务，但运行时需要线程关联的情况除外，这是由对 [IHostTaskManager：： BeginThreadAffinity](ihosttaskmanager-beginthreadaffinity-method.md) 和 [IHostTaskManager：： EndThreadAffinity](ihosttaskmanager-endthreadaffinity-method.md) 方法的调用指定的。</span><span class="sxs-lookup"><span data-stu-id="3268a-135">After a call to `ICLRTask::SwitchIn`, the host can schedule the task on any operating system thread, except in cases where the runtime requires thread-affinity, as specified by calls to the [IHostTaskManager::BeginThreadAffinity](ihosttaskmanager-beginthreadaffinity-method.md) and [IHostTaskManager::EndThreadAffinity](ihosttaskmanager-endthreadaffinity-method.md) methods.</span></span> <span data-ttu-id="3268a-136">稍后，操作系统可能决定从线程中删除任务并将其置于非运行状态。</span><span class="sxs-lookup"><span data-stu-id="3268a-136">Some time later, the operating system might decide to remove the task from the thread and place it in a non-running state.</span></span> <span data-ttu-id="3268a-137">例如，每当任务阻止同步基元或等待 i/o 操作完成时，就会发生这种情况。</span><span class="sxs-lookup"><span data-stu-id="3268a-137">For example, this might happen whenever the task blocks on synchronization primitives, or waits for I/O operations to complete.</span></span> <span data-ttu-id="3268a-138">主机调用 [SwitchOut](iclrtask-switchout-method.md) 来通知 CLR 当前实例所表示的任务 `ICLRTask` 不再处于可使用状态。</span><span class="sxs-lookup"><span data-stu-id="3268a-138">The host calls [SwitchOut](iclrtask-switchout-method.md) to notify the CLR that the task represented by the current `ICLRTask` instance is no longer in an operable state.</span></span>  
  
 <span data-ttu-id="3268a-139">任务通常在代码执行结束时终止。</span><span class="sxs-lookup"><span data-stu-id="3268a-139">A task typically terminates at the end of code execution.</span></span> <span data-ttu-id="3268a-140">此时，主机将调用 `ICLRTask::ExitTask` 以销毁关联的 `ICLRTask` 。</span><span class="sxs-lookup"><span data-stu-id="3268a-140">At that time, the host calls `ICLRTask::ExitTask` to destroy the associated `ICLRTask`.</span></span> <span data-ttu-id="3268a-141">但是，还可以使用对的调用来回收任务，这样就可以 `ICLRTask::Reset` `ICLRTask` 再次使用实例。</span><span class="sxs-lookup"><span data-stu-id="3268a-141">However, tasks can also be recycled by using a call to `ICLRTask::Reset`, which allows the `ICLRTask` instance to be used again.</span></span> <span data-ttu-id="3268a-142">此方法可防止重复创建和销毁实例的系统开销。</span><span class="sxs-lookup"><span data-stu-id="3268a-142">This approach prevents the overhead of repeatedly creating and destroying instances.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3268a-143">要求</span><span class="sxs-lookup"><span data-stu-id="3268a-143">Requirements</span></span>  

 <span data-ttu-id="3268a-144">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3268a-144">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3268a-145">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="3268a-145">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3268a-146">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3268a-146">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3268a-147">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3268a-147">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3268a-148">请参阅</span><span class="sxs-lookup"><span data-stu-id="3268a-148">See also</span></span>

- [<span data-ttu-id="3268a-149">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="3268a-149">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="3268a-150">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="3268a-150">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="3268a-151">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="3268a-151">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
- [<span data-ttu-id="3268a-152">承载接口</span><span class="sxs-lookup"><span data-stu-id="3268a-152">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="3268a-153">ICLRTask2 接口</span><span class="sxs-lookup"><span data-stu-id="3268a-153">ICLRTask2 Interface</span></span>](iclrtask2-interface.md)
