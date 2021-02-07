---
description: 了解详细信息： IHostGCManager：： SuspensionEnding 方法
title: IHostGCManager::SuspensionEnding 方法
ms.date: 03/30/2017
api_name:
- IHostGCManager.SuspensionEnding
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostGCManager::SuspensionEnding
helpviewer_keywords:
- SuspensionEnding method, IHostGCManager interface [.NET Framework hosting]
- IHostGCManager::SuspensionEnding method [.NET Framework hosting]
ms.assetid: 8849a1db-17f0-44b7-880a-bd36d431eb91
topic_type:
- apiref
ms.openlocfilehash: 43ec3db76e6e6448719f9c40ef2476da4e2ccf9c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99708614"
---
# <a name="ihostgcmanagersuspensionending-method"></a><span data-ttu-id="d1ba7-103">IHostGCManager::SuspensionEnding 方法</span><span class="sxs-lookup"><span data-stu-id="d1ba7-103">IHostGCManager::SuspensionEnding Method</span></span>

<span data-ttu-id="d1ba7-104">向宿主通知公共语言运行时 (CLR) 正在继续执行已挂起垃圾回收的线程上的任务。</span><span class="sxs-lookup"><span data-stu-id="d1ba7-104">Notifies the host that the common language runtime (CLR) is resuming execution of tasks on threads that had been suspended for a garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d1ba7-105">语法</span><span class="sxs-lookup"><span data-stu-id="d1ba7-105">Syntax</span></span>  
  
```cpp  
HRESULT SuspensionEnding (  
    [in] DWORD generation  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d1ba7-106">参数</span><span class="sxs-lookup"><span data-stu-id="d1ba7-106">Parameters</span></span>  

 `generation`  
 <span data-ttu-id="d1ba7-107">中刚完成的垃圾回收生成，线程将从该生成中恢复。</span><span class="sxs-lookup"><span data-stu-id="d1ba7-107">[in] The garbage collection generation that is just finishing, from which the thread is resuming.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d1ba7-108">返回值</span><span class="sxs-lookup"><span data-stu-id="d1ba7-108">Return Value</span></span>  
  
|<span data-ttu-id="d1ba7-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="d1ba7-109">HRESULT</span></span>|<span data-ttu-id="d1ba7-110">说明</span><span class="sxs-lookup"><span data-stu-id="d1ba7-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="d1ba7-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="d1ba7-111">S_OK</span></span>|<span data-ttu-id="d1ba7-112">`SuspensionEnding` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="d1ba7-112">`SuspensionEnding` returned successfully.</span></span>|  
|<span data-ttu-id="d1ba7-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="d1ba7-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="d1ba7-114">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="d1ba7-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="d1ba7-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="d1ba7-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="d1ba7-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="d1ba7-116">The call timed out.</span></span>|  
|<span data-ttu-id="d1ba7-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="d1ba7-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="d1ba7-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="d1ba7-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="d1ba7-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="d1ba7-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="d1ba7-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="d1ba7-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="d1ba7-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="d1ba7-121">E_FAIL</span></span>|<span data-ttu-id="d1ba7-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="d1ba7-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="d1ba7-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="d1ba7-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="d1ba7-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="d1ba7-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d1ba7-125">备注</span><span class="sxs-lookup"><span data-stu-id="d1ba7-125">Remarks</span></span>  

 <span data-ttu-id="d1ba7-126">CLR 在 `SuspensionEnding` 执行垃圾回收后调用，以通知宿主线程正在继续执行。</span><span class="sxs-lookup"><span data-stu-id="d1ba7-126">The CLR calls `SuspensionEnding` after it performs a garbage collection, to inform the host that the thread is resuming execution.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="d1ba7-127">不要重新安排从其进行方法调用的线程。</span><span class="sxs-lookup"><span data-stu-id="d1ba7-127">Do not reschedule the thread the method call was made from.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d1ba7-128">要求</span><span class="sxs-lookup"><span data-stu-id="d1ba7-128">Requirements</span></span>  

 <span data-ttu-id="d1ba7-129">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d1ba7-129">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d1ba7-130">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="d1ba7-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="d1ba7-131">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d1ba7-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d1ba7-132">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d1ba7-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d1ba7-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="d1ba7-133">See also</span></span>

- [<span data-ttu-id="d1ba7-134">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="d1ba7-134">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="d1ba7-135">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="d1ba7-135">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="d1ba7-136">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="d1ba7-136">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="d1ba7-137">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="d1ba7-137">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
- [<span data-ttu-id="d1ba7-138">IHostGCManager 接口</span><span class="sxs-lookup"><span data-stu-id="d1ba7-138">IHostGCManager Interface</span></span>](ihostgcmanager-interface.md)
