---
description: 了解详细信息： IHostGCManager：： SuspensionStarting 方法
title: IHostGCManager::SuspensionStarting 方法
ms.date: 03/30/2017
api_name:
- IHostGCManager.SuspensionStarting
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostGCManager::SuspensionStarting
helpviewer_keywords:
- SuspensionStarting method, IHostGCManager interface [.NET Framework hosting]
- IHostGCManager::SuspensionStarting method [.NET Framework hosting]
ms.assetid: c381f524-94cf-4fa2-9298-50f847a03431
topic_type:
- apiref
ms.openlocfilehash: 3a57d47fea735ab004fd0db293bed1ba4d3314e6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99708628"
---
# <a name="ihostgcmanagersuspensionstarting-method"></a><span data-ttu-id="9c15d-103">IHostGCManager::SuspensionStarting 方法</span><span class="sxs-lookup"><span data-stu-id="9c15d-103">IHostGCManager::SuspensionStarting Method</span></span>

<span data-ttu-id="9c15d-104">向宿主通知公共语言运行时 (CLR) 正在暂停执行任务，以执行垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="9c15d-104">Notifies the host that the common language runtime (CLR) is suspending execution of tasks, to perform a garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9c15d-105">语法</span><span class="sxs-lookup"><span data-stu-id="9c15d-105">Syntax</span></span>  
  
```cpp  
HRESULT SuspensionStarting ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="9c15d-106">返回值</span><span class="sxs-lookup"><span data-stu-id="9c15d-106">Return Value</span></span>  
  
|<span data-ttu-id="9c15d-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="9c15d-107">HRESULT</span></span>|<span data-ttu-id="9c15d-108">说明</span><span class="sxs-lookup"><span data-stu-id="9c15d-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="9c15d-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="9c15d-109">S_OK</span></span>|<span data-ttu-id="9c15d-110">`SuspensionStarting` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="9c15d-110">`SuspensionStarting` returned successfully.</span></span>|  
|<span data-ttu-id="9c15d-111">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="9c15d-111">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="9c15d-112">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="9c15d-112">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="9c15d-113">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="9c15d-113">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="9c15d-114">调用超时。</span><span class="sxs-lookup"><span data-stu-id="9c15d-114">The call timed out.</span></span>|  
|<span data-ttu-id="9c15d-115">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="9c15d-115">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="9c15d-116">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="9c15d-116">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="9c15d-117">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="9c15d-117">HOST_E_ABANDONED</span></span>|<span data-ttu-id="9c15d-118">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="9c15d-118">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="9c15d-119">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="9c15d-119">E_FAIL</span></span>|<span data-ttu-id="9c15d-120">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="9c15d-120">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="9c15d-121">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="9c15d-121">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="9c15d-122">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="9c15d-122">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9c15d-123">备注</span><span class="sxs-lookup"><span data-stu-id="9c15d-123">Remarks</span></span>  

 <span data-ttu-id="9c15d-124">CLR 调用 `SuspensionStarting` 来通知主机发生垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="9c15d-124">The CLR calls `SuspensionStarting` to inform the host that garbage collection is occurring.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="9c15d-125">不要重新计划此任务。</span><span class="sxs-lookup"><span data-stu-id="9c15d-125">Do not reschedule this task.</span></span> <span data-ttu-id="9c15d-126">调用 [ThreadIsBlockingForSuspension](ihostgcmanager-threadisblockingforsuspension-method.md) 时，主机必须重新安排任务。</span><span class="sxs-lookup"><span data-stu-id="9c15d-126">The host must reschedule a task when [ThreadIsBlockingForSuspension](ihostgcmanager-threadisblockingforsuspension-method.md) is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9c15d-127">要求</span><span class="sxs-lookup"><span data-stu-id="9c15d-127">Requirements</span></span>  

 <span data-ttu-id="9c15d-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9c15d-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9c15d-129">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="9c15d-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9c15d-130">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9c15d-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9c15d-131">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9c15d-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9c15d-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="9c15d-132">See also</span></span>

- [<span data-ttu-id="9c15d-133">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="9c15d-133">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="9c15d-134">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="9c15d-134">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="9c15d-135">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="9c15d-135">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="9c15d-136">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="9c15d-136">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
- [<span data-ttu-id="9c15d-137">IHostGCManager 接口</span><span class="sxs-lookup"><span data-stu-id="9c15d-137">IHostGCManager Interface</span></span>](ihostgcmanager-interface.md)
