---
description: 了解详细信息： ICLRTask：： Reset 方法
title: ICLRTask::Reset 方法
ms.date: 03/30/2017
api_name:
- ICLRTask.Reset
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask::Reset
helpviewer_keywords:
- ICLRTask::Reset method [.NET Framework hosting]
- Reset method, ICLRTask interface [.NET Framework hosting]
ms.assetid: 1bfb5d3a-0ffd-4bb4-9bf6-aec00cb675b7
topic_type:
- apiref
ms.openlocfilehash: d30738b98003e0543c1a2a31c7471b15811efe5f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99636983"
---
# <a name="iclrtaskreset-method"></a><span data-ttu-id="2f60e-103">ICLRTask::Reset 方法</span><span class="sxs-lookup"><span data-stu-id="2f60e-103">ICLRTask::Reset Method</span></span>

<span data-ttu-id="2f60e-104">通知公共语言运行时 (CLR) 宿主已经完成了一个任务，并使 CLR 能够重复使用当前 [ICLRTask](iclrtask-interface.md) 实例来表示其他任务。</span><span class="sxs-lookup"><span data-stu-id="2f60e-104">Informs the common language runtime (CLR) that the host has completed a task, and enables the CLR to reuse the current [ICLRTask](iclrtask-interface.md) instance to represent another task.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2f60e-105">语法</span><span class="sxs-lookup"><span data-stu-id="2f60e-105">Syntax</span></span>  
  
```cpp  
HRESULT Reset (  
    [in] BOOL fFull  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2f60e-106">参数</span><span class="sxs-lookup"><span data-stu-id="2f60e-106">Parameters</span></span>  

 `fFull`  
 <span data-ttu-id="2f60e-107">[in] `true` 如果除了与当前实例相关的安全性和区域设置信息，运行时还应重置与线程相关的所有静态值， `ICLRTask` 则为; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="2f60e-107">[in] `true`, if the runtime should reset all thread-related static values in addition to the security and locale information related to the current `ICLRTask` instance; otherwise, `false`.</span></span>  
  
 <span data-ttu-id="2f60e-108">如果该值为 `true` ，则运行时将重置使用或存储的数据 <xref:System.Threading.Thread.AllocateDataSlot%2A> <xref:System.Threading.Thread.AllocateNamedDataSlot%2A> 。</span><span class="sxs-lookup"><span data-stu-id="2f60e-108">If the value is `true`, the runtime resets data that was stored using <xref:System.Threading.Thread.AllocateDataSlot%2A> or <xref:System.Threading.Thread.AllocateNamedDataSlot%2A>.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2f60e-109">返回值</span><span class="sxs-lookup"><span data-stu-id="2f60e-109">Return Value</span></span>  
  
|<span data-ttu-id="2f60e-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="2f60e-110">HRESULT</span></span>|<span data-ttu-id="2f60e-111">说明</span><span class="sxs-lookup"><span data-stu-id="2f60e-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="2f60e-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="2f60e-112">S_OK</span></span>|<span data-ttu-id="2f60e-113">`Reset` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="2f60e-113">`Reset` returned successfully.</span></span>|  
|<span data-ttu-id="2f60e-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="2f60e-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="2f60e-115">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="2f60e-115">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call.</span></span> <span data-ttu-id="2f60e-116">顺利</span><span class="sxs-lookup"><span data-stu-id="2f60e-116">successfully</span></span>|  
|<span data-ttu-id="2f60e-117">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="2f60e-117">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="2f60e-118">调用超时。</span><span class="sxs-lookup"><span data-stu-id="2f60e-118">The call timed out.</span></span>|  
|<span data-ttu-id="2f60e-119">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="2f60e-119">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="2f60e-120">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="2f60e-120">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="2f60e-121">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="2f60e-121">HOST_E_ABANDONED</span></span>|<span data-ttu-id="2f60e-122">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="2f60e-122">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="2f60e-123">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="2f60e-123">E_FAIL</span></span>|<span data-ttu-id="2f60e-124">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="2f60e-124">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="2f60e-125">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="2f60e-125">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="2f60e-126">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="2f60e-126">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2f60e-127">备注</span><span class="sxs-lookup"><span data-stu-id="2f60e-127">Remarks</span></span>  

 <span data-ttu-id="2f60e-128">CLR 可以回收以前创建的 `ICLRTask` 实例，以避免在每次需要全新任务时重复创建新实例的系统开销。</span><span class="sxs-lookup"><span data-stu-id="2f60e-128">The CLR can recycle previously created `ICLRTask` instances to avoid the overhead of repeatedly creating new instances every time it needs a fresh task.</span></span> <span data-ttu-id="2f60e-129">主机完成任务后，将通过调用 `ICLRTask::Reset` 而不是 [ICLRTask：： ExitTask](iclrtask-exittask-method.md) 来启用此功能。</span><span class="sxs-lookup"><span data-stu-id="2f60e-129">The host enables this feature by calling `ICLRTask::Reset` instead of [ICLRTask::ExitTask](iclrtask-exittask-method.md) when it has completed a task.</span></span> <span data-ttu-id="2f60e-130">下面的列表总结了实例的正常生命周期 `ICLRTask` ：</span><span class="sxs-lookup"><span data-stu-id="2f60e-130">The following list summarizes the normal life cycle of an `ICLRTask` instance:</span></span>  
  
1. <span data-ttu-id="2f60e-131">运行时创建一个新的 `ICLRTask` 实例。</span><span class="sxs-lookup"><span data-stu-id="2f60e-131">The runtime creates a new `ICLRTask` instance.</span></span>  
  
2. <span data-ttu-id="2f60e-132">运行时调用 [IHostTaskManager：： GetCurrentTask](ihosttaskmanager-getcurrenttask-method.md) 以获取对当前宿主任务的引用。</span><span class="sxs-lookup"><span data-stu-id="2f60e-132">The runtime calls [IHostTaskManager::GetCurrentTask](ihosttaskmanager-getcurrenttask-method.md) to get a reference to the current host task.</span></span>  
  
3. <span data-ttu-id="2f60e-133">运行时调用 [IHostTask：： SetCLRTask](ihosttask-setclrtask-method.md) 以将新实例与宿主任务相关联。</span><span class="sxs-lookup"><span data-stu-id="2f60e-133">The runtime calls [IHostTask::SetCLRTask](ihosttask-setclrtask-method.md) to associate the new instance with the host task.</span></span>  
  
4. <span data-ttu-id="2f60e-134">任务执行并完成。</span><span class="sxs-lookup"><span data-stu-id="2f60e-134">The task executes and completes.</span></span>  
  
5. <span data-ttu-id="2f60e-135">宿主通过调用销毁任务 `ICLRTask::ExitTask` 。</span><span class="sxs-lookup"><span data-stu-id="2f60e-135">The host destroys the task by calling `ICLRTask::ExitTask`.</span></span>  
  
 <span data-ttu-id="2f60e-136">`Reset` 通过两种方式改变此方案。</span><span class="sxs-lookup"><span data-stu-id="2f60e-136">`Reset` alters this scenario in two ways.</span></span> <span data-ttu-id="2f60e-137">在上面的步骤5中，主机将调用 `Reset` 以将任务重置为干净状态，然后将该 `ICLRTask` 实例从其关联的 [IHostTask](ihosttask-interface.md) 实例中分离。</span><span class="sxs-lookup"><span data-stu-id="2f60e-137">In step 5 above, the host calls `Reset` to reset the task to a clean state, and then decouples the `ICLRTask` instance from its associated [IHostTask](ihosttask-interface.md) instance.</span></span> <span data-ttu-id="2f60e-138">如果需要，主机还可以缓存 `IHostTask` 实例以供重复使用。</span><span class="sxs-lookup"><span data-stu-id="2f60e-138">If desired, the host can also cache the `IHostTask` instance for reuse.</span></span> <span data-ttu-id="2f60e-139">在上面的步骤1中，运行时 `ICLRTask` 从缓存中提取回收，而不是创建新的实例。</span><span class="sxs-lookup"><span data-stu-id="2f60e-139">In step 1 above, the runtime pulls a recycled `ICLRTask` from the cache instead of creating a new instance.</span></span>  
  
 <span data-ttu-id="2f60e-140">当主机还具有可重复使用的辅助角色任务池时，此方法非常有效。</span><span class="sxs-lookup"><span data-stu-id="2f60e-140">This approach works well when the host also has a pool of reusable worker tasks.</span></span> <span data-ttu-id="2f60e-141">当主机销毁其某个实例时 `IHostTask` ，它会 `ICLRTask` 通过调用销毁相应的 `ExitTask` 。</span><span class="sxs-lookup"><span data-stu-id="2f60e-141">When the host destroys one of its `IHostTask` instances, it destroys the corresponding `ICLRTask` by calling `ExitTask`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2f60e-142">要求</span><span class="sxs-lookup"><span data-stu-id="2f60e-142">Requirements</span></span>  

 <span data-ttu-id="2f60e-143">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2f60e-143">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2f60e-144">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="2f60e-144">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="2f60e-145">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2f60e-145">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2f60e-146">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2f60e-146">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2f60e-147">请参阅</span><span class="sxs-lookup"><span data-stu-id="2f60e-147">See also</span></span>

- [<span data-ttu-id="2f60e-148">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="2f60e-148">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="2f60e-149">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="2f60e-149">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="2f60e-150">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="2f60e-150">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="2f60e-151">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="2f60e-151">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
