---
description: 了解详细信息： IHostTaskManager 接口
title: IHostTaskManager 接口
ms.date: 03/30/2017
api_name:
- IHostTaskManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager
helpviewer_keywords:
- IHostTaskManager interface [.NET Framework hosting]
ms.assetid: 4a0b05b9-3ef1-4607-b7c8-bd4dd43647a0
topic_type:
- apiref
ms.openlocfilehash: 67574550ba26970189ea53b8e6bdb867fea8549b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707448"
---
# <a name="ihosttaskmanager-interface"></a><span data-ttu-id="c2f40-103">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="c2f40-103">IHostTaskManager Interface</span></span>

<span data-ttu-id="c2f40-104">提供一些方法，使公共语言运行时 (CLR) 可以通过主机使用任务，而不是使用标准操作系统线程处理或纤程函数。</span><span class="sxs-lookup"><span data-stu-id="c2f40-104">Provides methods that allow the common language runtime (CLR) to work with tasks through the host instead of using the standard operating system threading or fiber functions.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="c2f40-105">方法</span><span class="sxs-lookup"><span data-stu-id="c2f40-105">Methods</span></span>  
  
|<span data-ttu-id="c2f40-106">方法</span><span class="sxs-lookup"><span data-stu-id="c2f40-106">Method</span></span>|<span data-ttu-id="c2f40-107">说明</span><span class="sxs-lookup"><span data-stu-id="c2f40-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="c2f40-108">BeginDelayAbort 方法</span><span class="sxs-lookup"><span data-stu-id="c2f40-108">BeginDelayAbort Method</span></span>](ihosttaskmanager-begindelayabort-method.md)|<span data-ttu-id="c2f40-109">通知宿主托管代码输入的时间段不得中止当前任务。</span><span class="sxs-lookup"><span data-stu-id="c2f40-109">Notifies the host that managed code is entering a period in which the current task must not be aborted.</span></span>|  
|[<span data-ttu-id="c2f40-110">BeginThreadAffinity 方法</span><span class="sxs-lookup"><span data-stu-id="c2f40-110">BeginThreadAffinity Method</span></span>](ihosttaskmanager-beginthreadaffinity-method.md)|<span data-ttu-id="c2f40-111">通知宿主托管代码正在输入一个时间段，在此期间，不能将当前任务移动到另一个操作系统线程。</span><span class="sxs-lookup"><span data-stu-id="c2f40-111">Notifies the host that managed code is entering a period in which the current task must not be moved to another operating system thread.</span></span>|  
|[<span data-ttu-id="c2f40-112">CallNeedsHostHook 方法</span><span class="sxs-lookup"><span data-stu-id="c2f40-112">CallNeedsHostHook Method</span></span>](ihosttaskmanager-callneedshosthook-method.md)|<span data-ttu-id="c2f40-113">使宿主能够指定公共语言运行时是否可将指定的调用内联到非托管函数。</span><span class="sxs-lookup"><span data-stu-id="c2f40-113">Enables the host to specify whether the common language runtime can inline the specified call to an unmanaged function.</span></span>|  
|[<span data-ttu-id="c2f40-114">CreateTask 方法</span><span class="sxs-lookup"><span data-stu-id="c2f40-114">CreateTask Method</span></span>](ihosttaskmanager-createtask-method.md)|<span data-ttu-id="c2f40-115">请求宿主创建新任务。</span><span class="sxs-lookup"><span data-stu-id="c2f40-115">Requests that the host create a new task.</span></span>|  
|[<span data-ttu-id="c2f40-116">EndDelayAbort 方法</span><span class="sxs-lookup"><span data-stu-id="c2f40-116">EndDelayAbort Method</span></span>](ihosttaskmanager-enddelayabort-method.md)|<span data-ttu-id="c2f40-117">向宿主通知托管代码，在之前对的调用之后不得中止当前任务 `BeginDelayAbort` 。</span><span class="sxs-lookup"><span data-stu-id="c2f40-117">Notifies the host that managed code is exiting the period in which the current task must not be aborted, following an earlier call to `BeginDelayAbort`.</span></span>|  
|[<span data-ttu-id="c2f40-118">EndThreadAffinity 方法</span><span class="sxs-lookup"><span data-stu-id="c2f40-118">EndThreadAffinity Method</span></span>](ihosttaskmanager-endthreadaffinity-method.md)|<span data-ttu-id="c2f40-119">向宿主通知托管代码，即在之前对的调用之后，不能将当前任务移到另一个操作系统线程 `BeginThreadAffinity` 。</span><span class="sxs-lookup"><span data-stu-id="c2f40-119">Notifies the host that managed code is exiting the period in which the current task must not be moved to another operating system thread, following an earlier call to `BeginThreadAffinity`.</span></span>|  
|[<span data-ttu-id="c2f40-120">EnterRuntime 方法</span><span class="sxs-lookup"><span data-stu-id="c2f40-120">EnterRuntime Method</span></span>](ihosttaskmanager-enterruntime-method.md)|<span data-ttu-id="c2f40-121">通知宿主对非托管方法的调用（如平台调用方法）正在将执行控制返回到 CLR。</span><span class="sxs-lookup"><span data-stu-id="c2f40-121">Notifies the host that a call to an unmanaged method, such as a platform invoke method, is returning execution control to the CLR.</span></span>|  
|[<span data-ttu-id="c2f40-122">GetCurrentTask 方法</span><span class="sxs-lookup"><span data-stu-id="c2f40-122">GetCurrentTask Method</span></span>](ihosttaskmanager-getcurrenttask-method.md)|<span data-ttu-id="c2f40-123">获取一个接口指针，该指针指向正在进行此调用的操作系统线程上当前正在执行的任务。</span><span class="sxs-lookup"><span data-stu-id="c2f40-123">Gets an interface pointer to the task that is currently executing on the operating system thread from which this call is made.</span></span>|  
|[<span data-ttu-id="c2f40-124">GetStackGuarantee 方法</span><span class="sxs-lookup"><span data-stu-id="c2f40-124">GetStackGuarantee Method</span></span>](ihosttaskmanager-getstackguarantee-method.md)|<span data-ttu-id="c2f40-125">获取在堆栈操作完成之后但在关闭进程之前保证可用的堆栈空间量。</span><span class="sxs-lookup"><span data-stu-id="c2f40-125">Gets the amount of stack space that is guaranteed to be available after a stack operation completes, but before the closing of a process.</span></span>|  
|[<span data-ttu-id="c2f40-126">LeaveRuntime 方法</span><span class="sxs-lookup"><span data-stu-id="c2f40-126">LeaveRuntime Method</span></span>](ihosttaskmanager-leaveruntime-method.md)|<span data-ttu-id="c2f40-127">通知宿主托管代码将要对非托管函数进行调用。</span><span class="sxs-lookup"><span data-stu-id="c2f40-127">Notifies the host that managed code is about to make a call to an unmanaged function.</span></span>|  
|[<span data-ttu-id="c2f40-128">ReverseEnterRuntime 方法</span><span class="sxs-lookup"><span data-stu-id="c2f40-128">ReverseEnterRuntime Method</span></span>](ihosttaskmanager-reverseenterruntime-method.md)|<span data-ttu-id="c2f40-129">通知宿主从非托管代码向公共语言运行时 (CLR) 发出调用。</span><span class="sxs-lookup"><span data-stu-id="c2f40-129">Notifies the host that a call is being made into the common language runtime (CLR) from unmanaged code.</span></span>|  
|[<span data-ttu-id="c2f40-130">ReverseLeaveRuntime 方法</span><span class="sxs-lookup"><span data-stu-id="c2f40-130">ReverseLeaveRuntime Method</span></span>](ihosttaskmanager-reverseleaveruntime-method.md)|<span data-ttu-id="c2f40-131">通知宿主控件离开 CLR，并进入从托管代码调用的非托管函数。</span><span class="sxs-lookup"><span data-stu-id="c2f40-131">Notifies the host that control is leaving the CLR and entering an unmanaged function that was, in turn, called from managed code.</span></span>|  
|[<span data-ttu-id="c2f40-132">SetCLRTaskManager 方法</span><span class="sxs-lookup"><span data-stu-id="c2f40-132">SetCLRTaskManager Method</span></span>](ihosttaskmanager-setclrtaskmanager-method.md)|<span data-ttu-id="c2f40-133">向宿主提供一个接口指针，该指针指向 CLR 实现的 [ICLRTaskManager](iclrtaskmanager-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="c2f40-133">Provides the host with an interface pointer to an [ICLRTaskManager](iclrtaskmanager-interface.md) instance implemented by the CLR.</span></span>|  
|[<span data-ttu-id="c2f40-134">SetLocale 方法</span><span class="sxs-lookup"><span data-stu-id="c2f40-134">SetLocale Method</span></span>](ihosttaskmanager-setlocale-method.md)|<span data-ttu-id="c2f40-135">通知宿主 CLR 已更改当前任务的区域设置。</span><span class="sxs-lookup"><span data-stu-id="c2f40-135">Notifies the host that the CLR has changed the locale on the current task.</span></span>|  
|[<span data-ttu-id="c2f40-136">SetStackGuarantee 方法</span><span class="sxs-lookup"><span data-stu-id="c2f40-136">SetStackGuarantee Method</span></span>](ihosttaskmanager-setstackguarantee-method.md)|<span data-ttu-id="c2f40-137">保留以仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="c2f40-137">Reserved for internal use only.</span></span>|  
|[<span data-ttu-id="c2f40-138">SetUILocale 方法</span><span class="sxs-lookup"><span data-stu-id="c2f40-138">SetUILocale Method</span></span>](ihosttaskmanager-setuilocale-method.md)|<span data-ttu-id="c2f40-139">通知宿主用户界面区域设置在当前任务上已更改。</span><span class="sxs-lookup"><span data-stu-id="c2f40-139">Notifies the host that the user interface locale has been changed on the current task.</span></span>|  
|[<span data-ttu-id="c2f40-140">Sleep 方法</span><span class="sxs-lookup"><span data-stu-id="c2f40-140">Sleep Method</span></span>](ihosttaskmanager-sleep-method.md)|<span data-ttu-id="c2f40-141">通知宿主当前任务将要进入睡眠状态。</span><span class="sxs-lookup"><span data-stu-id="c2f40-141">Notifies the host that the current task is going to sleep.</span></span>|  
|[<span data-ttu-id="c2f40-142">SwitchToTask 方法</span><span class="sxs-lookup"><span data-stu-id="c2f40-142">SwitchToTask Method</span></span>](ihosttaskmanager-switchtotask-method.md)|<span data-ttu-id="c2f40-143">通知宿主应切换到当前任务。</span><span class="sxs-lookup"><span data-stu-id="c2f40-143">Notifies the host that it should switch out the current task.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c2f40-144">备注</span><span class="sxs-lookup"><span data-stu-id="c2f40-144">Remarks</span></span>  

 <span data-ttu-id="c2f40-145">`IHostTaskManager` 允许 CLR 创建和管理任务，以便在控制从托管到非托管代码的传输时，为宿主提供挂钩，并指定在代码执行期间宿主可以和不能执行的某些操作。</span><span class="sxs-lookup"><span data-stu-id="c2f40-145">`IHostTaskManager` allows the CLR to create and manage tasks, to provide hooks for the host to take action when control transfers from managed to unmanaged code and vice versa, and to specify certain actions the host can and cannot take during code execution.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c2f40-146">要求</span><span class="sxs-lookup"><span data-stu-id="c2f40-146">Requirements</span></span>  

 <span data-ttu-id="c2f40-147">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c2f40-147">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c2f40-148">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="c2f40-148">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c2f40-149">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c2f40-149">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c2f40-150">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c2f40-150">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c2f40-151">请参阅</span><span class="sxs-lookup"><span data-stu-id="c2f40-151">See also</span></span>

- [<span data-ttu-id="c2f40-152">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="c2f40-152">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="c2f40-153">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="c2f40-153">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="c2f40-154">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="c2f40-154">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="c2f40-155">承载接口</span><span class="sxs-lookup"><span data-stu-id="c2f40-155">Hosting Interfaces</span></span>](hosting-interfaces.md)
