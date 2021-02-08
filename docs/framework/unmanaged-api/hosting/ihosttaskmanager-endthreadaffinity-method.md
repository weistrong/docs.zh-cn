---
description: 了解详细信息： IHostTaskManager：： EndThreadAffinity 方法
title: IHostTaskManager::EndThreadAffinity 方法
ms.date: 03/30/2017
api_name:
- IHostTaskManager.EndThreadAffinity
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::EndThreadAffinity
helpviewer_keywords:
- EndThreadAffinity method [.NET Framework hosting]
- IHostTaskManager::EndThreadAffinity method [.NET Framework hosting]
ms.assetid: 7738a904-0cd7-4fde-a3eb-2323a5533157
topic_type:
- apiref
ms.openlocfilehash: 0bbe42d8e14d20fb5be18fe7ebb266100ae72fd7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789419"
---
# <a name="ihosttaskmanagerendthreadaffinity-method"></a><span data-ttu-id="31149-103">IHostTaskManager::EndThreadAffinity 方法</span><span class="sxs-lookup"><span data-stu-id="31149-103">IHostTaskManager::EndThreadAffinity Method</span></span>

<span data-ttu-id="31149-104">在之前调用 [IHostTaskManager：： BeginThreadAffinity](ihosttaskmanager-beginthreadaffinity-method.md)时，通知宿主托管代码正在退出不能将当前任务移动到另一个操作系统线程的时间段。</span><span class="sxs-lookup"><span data-stu-id="31149-104">Notifies the host that managed code is exiting the period in which the current task must not be moved to another operating system thread, following an earlier call to [IHostTaskManager::BeginThreadAffinity](ihosttaskmanager-beginthreadaffinity-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="31149-105">语法</span><span class="sxs-lookup"><span data-stu-id="31149-105">Syntax</span></span>  
  
```cpp  
HRESULT EndThreadAffinity ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="31149-106">返回值</span><span class="sxs-lookup"><span data-stu-id="31149-106">Return Value</span></span>  
  
|<span data-ttu-id="31149-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="31149-107">HRESULT</span></span>|<span data-ttu-id="31149-108">说明</span><span class="sxs-lookup"><span data-stu-id="31149-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="31149-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="31149-109">S_OK</span></span>|<span data-ttu-id="31149-110">`EndThreadAffinity` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="31149-110">`EndThreadAffinity` returned successfully.</span></span>|  
|<span data-ttu-id="31149-111">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="31149-111">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="31149-112"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="31149-112">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="31149-113">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="31149-113">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="31149-114">调用超时。</span><span class="sxs-lookup"><span data-stu-id="31149-114">The call timed out.</span></span>|  
|<span data-ttu-id="31149-115">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="31149-115">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="31149-116">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="31149-116">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="31149-117">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="31149-117">HOST_E_ABANDONED</span></span>|<span data-ttu-id="31149-118">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="31149-118">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="31149-119">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="31149-119">E_FAIL</span></span>|<span data-ttu-id="31149-120">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="31149-120">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="31149-121">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="31149-121">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="31149-122">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="31149-122">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="31149-123">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="31149-123">E_UNEXPECTED</span></span>|<span data-ttu-id="31149-124">`EndThreadAffinity` 在没有对的早期调用的情况下调用 `BeginThreadAffinity` 。</span><span class="sxs-lookup"><span data-stu-id="31149-124">`EndThreadAffinity` was called without an earlier corresponding call to `BeginThreadAffinity`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="31149-125">备注</span><span class="sxs-lookup"><span data-stu-id="31149-125">Remarks</span></span>  

 <span data-ttu-id="31149-126">在调用之前，CLR 对当前任务进行相应的调用 `BeginThreadAffinity` `EndThreadAffinity` 。</span><span class="sxs-lookup"><span data-stu-id="31149-126">The CLR makes a corresponding call to `BeginThreadAffinity` on the current task before calling `EndThreadAffinity`.</span></span> <span data-ttu-id="31149-127">如果没有此类对应的调用，主机的 [IHostTaskManager](ihosttaskmanager-interface.md) 实现应返回 E_UNEXPECTED，而不执行任何操作。</span><span class="sxs-lookup"><span data-stu-id="31149-127">In the absence of such a corresponding call, the host's implementation of [IHostTaskManager](ihosttaskmanager-interface.md) should return E_UNEXPECTED, and take no action.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="31149-128">要求</span><span class="sxs-lookup"><span data-stu-id="31149-128">Requirements</span></span>  

 <span data-ttu-id="31149-129">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="31149-129">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="31149-130">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="31149-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="31149-131">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="31149-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="31149-132">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="31149-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="31149-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="31149-133">See also</span></span>

- <xref:System.Threading>
- [<span data-ttu-id="31149-134">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="31149-134">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="31149-135">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="31149-135">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="31149-136">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="31149-136">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="31149-137">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="31149-137">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
