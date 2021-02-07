---
description: 了解详细信息： IHostTaskManager：： ReverseLeaveRuntime 方法
title: IHostTaskManager::ReverseLeaveRuntime 方法
ms.date: 03/30/2017
api_name:
- IHostTaskManager.ReverseLeaveRuntime
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::ReverseLeaveRuntime
helpviewer_keywords:
- IHostTaskManager::ReverseLeaveRuntime method [.NET Framework hosting]
- ReverseLeaveRuntime method [.NET Framework hosting]
ms.assetid: 4837d398-16a1-4e32-902c-022cd1aad3ca
topic_type:
- apiref
ms.openlocfilehash: 2fed157f6ea05243270b957cacdb00ba5a47a88f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99680845"
---
# <a name="ihosttaskmanagerreverseleaveruntime-method"></a><span data-ttu-id="69ee7-103">IHostTaskManager::ReverseLeaveRuntime 方法</span><span class="sxs-lookup"><span data-stu-id="69ee7-103">IHostTaskManager::ReverseLeaveRuntime Method</span></span>

<span data-ttu-id="69ee7-104">向宿主通知控制是否正在离开公共语言运行时 (CLR) 并输入从托管代码调用的非托管函数。</span><span class="sxs-lookup"><span data-stu-id="69ee7-104">Notifies the host that control is leaving the common language runtime (CLR) and entering an unmanaged function that was, in turn, called from managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="69ee7-105">语法</span><span class="sxs-lookup"><span data-stu-id="69ee7-105">Syntax</span></span>  
  
```cpp  
HRESULT ReverseLeaveRuntime ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="69ee7-106">返回值</span><span class="sxs-lookup"><span data-stu-id="69ee7-106">Return Value</span></span>  
  
|<span data-ttu-id="69ee7-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="69ee7-107">HRESULT</span></span>|<span data-ttu-id="69ee7-108">说明</span><span class="sxs-lookup"><span data-stu-id="69ee7-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="69ee7-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="69ee7-109">S_OK</span></span>|<span data-ttu-id="69ee7-110">`ReverseLeaveRuntime` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="69ee7-110">`ReverseLeaveRuntime` returned successfully.</span></span>|  
|<span data-ttu-id="69ee7-111">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="69ee7-111">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="69ee7-112">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="69ee7-112">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="69ee7-113">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="69ee7-113">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="69ee7-114">调用超时。</span><span class="sxs-lookup"><span data-stu-id="69ee7-114">The call timed out.</span></span>|  
|<span data-ttu-id="69ee7-115">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="69ee7-115">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="69ee7-116">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="69ee7-116">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="69ee7-117">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="69ee7-117">HOST_E_ABANDONED</span></span>|<span data-ttu-id="69ee7-118">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="69ee7-118">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="69ee7-119">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="69ee7-119">E_FAIL</span></span>|<span data-ttu-id="69ee7-120">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="69ee7-120">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="69ee7-121">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="69ee7-121">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="69ee7-122">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="69ee7-122">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="69ee7-123">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="69ee7-123">E_OUTOFMEMORY</span></span>|<span data-ttu-id="69ee7-124">没有足够的内存可用来完成请求的资源分配。</span><span class="sxs-lookup"><span data-stu-id="69ee7-124">Not enough memory is available to complete the requested resource allocation.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="69ee7-125">备注</span><span class="sxs-lookup"><span data-stu-id="69ee7-125">Remarks</span></span>  

 <span data-ttu-id="69ee7-126">CLR 调用 `ReverseLeaveRuntime` 以通知宿主当前正在执行的任务正在将控制权返回给非托管函数，而该函数又通过平台调用从托管代码调用。</span><span class="sxs-lookup"><span data-stu-id="69ee7-126">The CLR calls `ReverseLeaveRuntime` to inform the host that the currently executing task is returning control to an unmanaged function that was, in turn, called from managed code through platform invoke.</span></span> <span data-ttu-id="69ee7-127">对的每个调用都 `ReverseLeaveRuntime` 匹配对 [ReverseEnterRuntime](ihosttaskmanager-reverseenterruntime-method.md)的相应调用。</span><span class="sxs-lookup"><span data-stu-id="69ee7-127">Each call to `ReverseLeaveRuntime` matches a corresponding call to [ReverseEnterRuntime](ihosttaskmanager-reverseenterruntime-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="69ee7-128">要求</span><span class="sxs-lookup"><span data-stu-id="69ee7-128">Requirements</span></span>  

 <span data-ttu-id="69ee7-129">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="69ee7-129">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="69ee7-130">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="69ee7-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="69ee7-131">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="69ee7-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="69ee7-132">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="69ee7-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="69ee7-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="69ee7-133">See also</span></span>

- [<span data-ttu-id="69ee7-134">CallNeedsHostHook 方法</span><span class="sxs-lookup"><span data-stu-id="69ee7-134">CallNeedsHostHook Method</span></span>](ihosttaskmanager-callneedshosthook-method.md)
- [<span data-ttu-id="69ee7-135">EnterRuntime 方法</span><span class="sxs-lookup"><span data-stu-id="69ee7-135">EnterRuntime Method</span></span>](ihosttaskmanager-enterruntime-method.md)
- [<span data-ttu-id="69ee7-136">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="69ee7-136">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="69ee7-137">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="69ee7-137">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="69ee7-138">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="69ee7-138">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="69ee7-139">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="69ee7-139">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
- [<span data-ttu-id="69ee7-140">LeaveRuntime 方法</span><span class="sxs-lookup"><span data-stu-id="69ee7-140">LeaveRuntime Method</span></span>](ihosttaskmanager-leaveruntime-method.md)
- <span data-ttu-id="69ee7-141">[平台调用详解](/previous-versions/dotnet/netframework-4.0/0h9e9t7d(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="69ee7-141">[A Closer Look at Platform Invoke](/previous-versions/dotnet/netframework-4.0/0h9e9t7d(v=vs.100))</span></span>
