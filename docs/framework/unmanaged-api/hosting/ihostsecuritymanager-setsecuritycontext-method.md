---
description: 了解详细信息： IHostSecurityManager：： SetSecurityContext 方法
title: IHostSecurityManager::SetSecurityContext 方法
ms.date: 03/30/2017
api_name:
- IHostSecurityManager.SetSecurityContext
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSecurityManager::SetSecurityContext
helpviewer_keywords:
- SetSecurityContext method [.NET Framework hosting]
- IHostSecurityManager::SetSecurityContext method [.NET Framework hosting]
ms.assetid: e4372384-ee69-48d7-97e0-8fab7866597a
topic_type:
- apiref
ms.openlocfilehash: ee2de40e043e626aba1d75540faab3cae4c8fb7e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99671472"
---
# <a name="ihostsecuritymanagersetsecuritycontext-method"></a><span data-ttu-id="f2095-103">IHostSecurityManager::SetSecurityContext 方法</span><span class="sxs-lookup"><span data-stu-id="f2095-103">IHostSecurityManager::SetSecurityContext Method</span></span>

<span data-ttu-id="f2095-104">设置当前正在执行的线程的安全上下文。</span><span class="sxs-lookup"><span data-stu-id="f2095-104">Sets the security context of the currently executing thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f2095-105">语法</span><span class="sxs-lookup"><span data-stu-id="f2095-105">Syntax</span></span>  
  
```cpp  
HRESULT SetSecurityContext (  
    [in]  EContextType eContextType,  
    [out] IHostSecurityContext** ppSecurityContext  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f2095-106">参数</span><span class="sxs-lookup"><span data-stu-id="f2095-106">Parameters</span></span>  

 `eContextType`  
 <span data-ttu-id="f2095-107">中 [EContextType](econtexttype-enumeration.md) 值之一，指示公共语言运行时 (CLR) 在主机上放置的上下文的类型。</span><span class="sxs-lookup"><span data-stu-id="f2095-107">[in] One of the [EContextType](econtexttype-enumeration.md) values, indicating what type of context the common language runtime (CLR) is placing on the host.</span></span>  
  
 `ppSecurityContext`  
 <span data-ttu-id="f2095-108">弄指向新 [IHostSecurityContext](ihostsecuritycontext-interface.md) 对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="f2095-108">[out] A pointer to the address of a new [IHostSecurityContext](ihostsecuritycontext-interface.md) object.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f2095-109">返回值</span><span class="sxs-lookup"><span data-stu-id="f2095-109">Return Value</span></span>  
  
|<span data-ttu-id="f2095-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f2095-110">HRESULT</span></span>|<span data-ttu-id="f2095-111">说明</span><span class="sxs-lookup"><span data-stu-id="f2095-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f2095-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="f2095-112">S_OK</span></span>|<span data-ttu-id="f2095-113">`SetSecurityContext` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="f2095-113">`SetSecurityContext` returned successfully.</span></span>|  
|<span data-ttu-id="f2095-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="f2095-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="f2095-115">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="f2095-115">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="f2095-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f2095-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="f2095-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="f2095-117">The call timed out.</span></span>|  
|<span data-ttu-id="f2095-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="f2095-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="f2095-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="f2095-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="f2095-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="f2095-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="f2095-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="f2095-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="f2095-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f2095-122">E_FAIL</span></span>|<span data-ttu-id="f2095-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="f2095-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="f2095-124">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="f2095-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="f2095-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="f2095-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f2095-126">备注</span><span class="sxs-lookup"><span data-stu-id="f2095-126">Remarks</span></span>  

 <span data-ttu-id="f2095-127">CLR `SetSecurityContext` 在多个方案中调用。</span><span class="sxs-lookup"><span data-stu-id="f2095-127">The CLR calls `SetSecurityContext` in several scenarios.</span></span> <span data-ttu-id="f2095-128">在执行类和模块构造函数和终结器之前，CLR 将调用 `SetSecurityContext` 以防止执行失败。</span><span class="sxs-lookup"><span data-stu-id="f2095-128">Before it executes class and module constructors and finalizers, the CLR calls `SetSecurityContext` to protect the host from execution failures.</span></span> <span data-ttu-id="f2095-129">然后，在执行构造函数或终结器后，通过使用对的另一调用，将安全上下文重置为其原始状态 `SetSecurityContext` 。</span><span class="sxs-lookup"><span data-stu-id="f2095-129">It then resets the security context to its original state after execution of the constructor or finalizer, by using another call to `SetSecurityContext`.</span></span> <span data-ttu-id="f2095-130">I/o 完成时，会出现类似的模式。</span><span class="sxs-lookup"><span data-stu-id="f2095-130">A similar pattern occurs with I/O completion.</span></span> <span data-ttu-id="f2095-131">如果主机实现 [IHostIoCompletionManager](ihostiocompletionmanager-interface.md)，则 CLR 会在 `SetSecurityContext` 主机调用 [ICLRIoCompletionManager：： OnComplete](iclriocompletionmanager-oncomplete-method.md)后调用。</span><span class="sxs-lookup"><span data-stu-id="f2095-131">If the host implements [IHostIoCompletionManager](ihostiocompletionmanager-interface.md), the CLR calls `SetSecurityContext` after the host calls [ICLRIoCompletionManager::OnComplete](iclriocompletionmanager-oncomplete-method.md).</span></span>  
  
 <span data-ttu-id="f2095-132">在工作线程中的异步点，CLR 在 `SetSecurityContext` <xref:System.Threading.ThreadPool.QueueUserWorkItem%2A?displayProperty=nameWithType> [IHostThreadPoolManager：： QueueUserWorkItem](ihostthreadpoolmanager-queueuserworkitem-method.md)内或内调用，具体取决于宿主或 CLR 是否实现线程池。</span><span class="sxs-lookup"><span data-stu-id="f2095-132">At asynchronous points in worker threads, the CLR calls `SetSecurityContext` within <xref:System.Threading.ThreadPool.QueueUserWorkItem%2A?displayProperty=nameWithType> or within [IHostThreadPoolManager::QueueUserWorkItem](ihostthreadpoolmanager-queueuserworkitem-method.md), depending on whether the host or the CLR is implementing the thread pool.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f2095-133">要求</span><span class="sxs-lookup"><span data-stu-id="f2095-133">Requirements</span></span>  

 <span data-ttu-id="f2095-134">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f2095-134">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f2095-135">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="f2095-135">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f2095-136">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f2095-136">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f2095-137">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f2095-137">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2095-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="f2095-138">See also</span></span>

- <xref:System.Threading.ThreadPool?displayProperty=nameWithType>
- [<span data-ttu-id="f2095-139">EContextType 枚举</span><span class="sxs-lookup"><span data-stu-id="f2095-139">EContextType Enumeration</span></span>](econtexttype-enumeration.md)
- [<span data-ttu-id="f2095-140">ICLRIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="f2095-140">ICLRIoCompletionManager Interface</span></span>](iclriocompletionmanager-interface.md)
- [<span data-ttu-id="f2095-141">IHostIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="f2095-141">IHostIoCompletionManager Interface</span></span>](ihostiocompletionmanager-interface.md)
- [<span data-ttu-id="f2095-142">IHostSecurityContext 接口</span><span class="sxs-lookup"><span data-stu-id="f2095-142">IHostSecurityContext Interface</span></span>](ihostsecuritycontext-interface.md)
- [<span data-ttu-id="f2095-143">IHostSecurityManager 接口</span><span class="sxs-lookup"><span data-stu-id="f2095-143">IHostSecurityManager Interface</span></span>](ihostsecuritymanager-interface.md)
- [<span data-ttu-id="f2095-144">IHostThreadPoolManager 接口</span><span class="sxs-lookup"><span data-stu-id="f2095-144">IHostThreadPoolManager Interface</span></span>](ihostthreadpoolmanager-interface.md)
