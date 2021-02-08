---
description: 了解详细信息： IHostTask：： SetPriority 方法
title: IHostTask::SetPriority 方法
ms.date: 03/30/2017
api_name:
- IHostTask.SetPriority
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTask::SetPriority
helpviewer_keywords:
- IHostTask::SetPriority method [.NET Framework hosting]
- SetPriority method [.NET Framework hosting]
ms.assetid: cd8c379b-c7a0-434f-8e23-899bd26be75d
topic_type:
- apiref
ms.openlocfilehash: c3e8fee954e5cbea2d084141a4b2d22d2fa5e95b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784634"
---
# <a name="ihosttasksetpriority-method"></a><span data-ttu-id="cd2f7-103">IHostTask::SetPriority 方法</span><span class="sxs-lookup"><span data-stu-id="cd2f7-103">IHostTask::SetPriority Method</span></span>

<span data-ttu-id="cd2f7-104">请求宿主调整当前 [IHostTask](ihosttask-interface.md) 实例所表示的任务的线程优先级别。</span><span class="sxs-lookup"><span data-stu-id="cd2f7-104">Requests that the host adjust the thread priority level for the task represented by the current [IHostTask](ihosttask-interface.md) instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cd2f7-105">语法</span><span class="sxs-lookup"><span data-stu-id="cd2f7-105">Syntax</span></span>  
  
```cpp  
HRESULT SetPriority (  
    [in] int newPriority  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cd2f7-106">参数</span><span class="sxs-lookup"><span data-stu-id="cd2f7-106">Parameters</span></span>  

 `newPriority`  
 <span data-ttu-id="cd2f7-107">中一个整数，表示当前实例表示的任务所请求的线程优先级值 `IHostTask` 。</span><span class="sxs-lookup"><span data-stu-id="cd2f7-107">[in] An integer that represents the requested thread priority value for the task represented by the current `IHostTask` instance.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cd2f7-108">返回值</span><span class="sxs-lookup"><span data-stu-id="cd2f7-108">Return Value</span></span>  
  
|<span data-ttu-id="cd2f7-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="cd2f7-109">HRESULT</span></span>|<span data-ttu-id="cd2f7-110">说明</span><span class="sxs-lookup"><span data-stu-id="cd2f7-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="cd2f7-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd2f7-111">S_OK</span></span>|<span data-ttu-id="cd2f7-112">`SetPriority` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="cd2f7-112">`SetPriority` returned successfully.</span></span>|  
|<span data-ttu-id="cd2f7-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="cd2f7-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="cd2f7-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="cd2f7-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="cd2f7-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="cd2f7-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="cd2f7-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="cd2f7-116">The call timed out.</span></span>|  
|<span data-ttu-id="cd2f7-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="cd2f7-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="cd2f7-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="cd2f7-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="cd2f7-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="cd2f7-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="cd2f7-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="cd2f7-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="cd2f7-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cd2f7-121">E_FAIL</span></span>|<span data-ttu-id="cd2f7-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="cd2f7-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="cd2f7-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="cd2f7-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="cd2f7-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="cd2f7-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cd2f7-125">备注</span><span class="sxs-lookup"><span data-stu-id="cd2f7-125">Remarks</span></span>  

 <span data-ttu-id="cd2f7-126">将使用部分基于线程优先级别的轮循机制为线程授予处理时间。</span><span class="sxs-lookup"><span data-stu-id="cd2f7-126">Threads are granted processing time using a round-robin system that is partly based on a thread's priority level.</span></span> <span data-ttu-id="cd2f7-127">`SetPriority` 允许 CLR 为当前任务设置该线程优先级别。</span><span class="sxs-lookup"><span data-stu-id="cd2f7-127">`SetPriority` allows the CLR to set that thread priority level for the current task.</span></span> <span data-ttu-id="cd2f7-128">支持以下 `newPriority` 值。</span><span class="sxs-lookup"><span data-stu-id="cd2f7-128">The following `newPriority` values are supported.</span></span>  
  
- <span data-ttu-id="cd2f7-129">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="cd2f7-129">THREAD_PRIORITY_ABOVE_NORMAL</span></span>  
  
- <span data-ttu-id="cd2f7-130">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="cd2f7-130">THREAD_PRIORITY_BELOW_NORMAL</span></span>  
  
- <span data-ttu-id="cd2f7-131">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="cd2f7-131">THREAD_PRIORITY_HIGHEST</span></span>  
  
- <span data-ttu-id="cd2f7-132">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="cd2f7-132">THREAD_PRIORITY_IDLE</span></span>  
  
- <span data-ttu-id="cd2f7-133">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="cd2f7-133">THREAD_PRIORITY_LOWEST</span></span>  
  
- <span data-ttu-id="cd2f7-134">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="cd2f7-134">THREAD_PRIORITY_NORMAL</span></span>  
  
- <span data-ttu-id="cd2f7-135">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="cd2f7-135">THREAD_PRIORITY_TIME_CRITICAL</span></span>  
  
 <span data-ttu-id="cd2f7-136">`SetPriority`当用户代码修改了的值时，CLR 将调用 <xref:System.Threading.Thread.Priority%2A?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="cd2f7-136">The CLR calls `SetPriority` when the value of the <xref:System.Threading.Thread.Priority%2A?displayProperty=nameWithType> is modified by user code.</span></span> <span data-ttu-id="cd2f7-137">宿主可以定义自己的线程优先级分配算法，并可以随意忽略此请求。</span><span class="sxs-lookup"><span data-stu-id="cd2f7-137">A host can define its own algorithms for thread priority assignment, and is free to ignore this request.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="cd2f7-138">`SetPriority` 不会报告线程优先级别是否已更改。</span><span class="sxs-lookup"><span data-stu-id="cd2f7-138">`SetPriority` does not report whether the thread priority level was changed.</span></span> <span data-ttu-id="cd2f7-139">调用 [IHostTask：： GetPriority](ihosttask-getpriority-method.md) 以确定任务的线程优先级别的值。</span><span class="sxs-lookup"><span data-stu-id="cd2f7-139">Call [IHostTask::GetPriority](ihosttask-getpriority-method.md) to determine the value of the task's thread priority level.</span></span>  
  
 <span data-ttu-id="cd2f7-140">线程优先级别值由 Win32 `SetThreadPriority` 函数定义。</span><span class="sxs-lookup"><span data-stu-id="cd2f7-140">Thread priority level values are defined by the Win32 `SetThreadPriority` function.</span></span> <span data-ttu-id="cd2f7-141">有关线程优先级的详细信息，请参阅 Windows 平台文档。</span><span class="sxs-lookup"><span data-stu-id="cd2f7-141">For more information about thread priority, see the Windows Platform documentation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cd2f7-142">要求</span><span class="sxs-lookup"><span data-stu-id="cd2f7-142">Requirements</span></span>  

 <span data-ttu-id="cd2f7-143">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cd2f7-143">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cd2f7-144">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="cd2f7-144">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="cd2f7-145">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cd2f7-145">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="cd2f7-146">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cd2f7-146">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cd2f7-147">请参阅</span><span class="sxs-lookup"><span data-stu-id="cd2f7-147">See also</span></span>

- <xref:System.Threading.Thread>
- [<span data-ttu-id="cd2f7-148">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="cd2f7-148">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="cd2f7-149">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="cd2f7-149">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="cd2f7-150">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="cd2f7-150">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="cd2f7-151">GetPriority 方法</span><span class="sxs-lookup"><span data-stu-id="cd2f7-151">GetPriority Method</span></span>](ihosttask-getpriority-method.md)
- [<span data-ttu-id="cd2f7-152">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="cd2f7-152">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
