---
description: 了解详细信息： IHostSemaphore：： ReleaseSemaphore 方法
title: IHostSemaphore::ReleaseSemaphore 方法
ms.date: 03/30/2017
api_name:
- IHostSemaphore.ReleaseSemaphore
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSemaphore::ReleaseSemaphore
helpviewer_keywords:
- ReleaseSemaphore method [.NET Framework hosting]
- IHostSemaphore::ReleaseSemaphore method [.NET Framework hosting]
ms.assetid: a343d197-979a-4ac6-ab8c-cb8a05f3120e
topic_type:
- apiref
ms.openlocfilehash: 368dc5ebe3017e03c0d6e8c57d0f122bc48d439f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707422"
---
# <a name="ihostsemaphorereleasesemaphore-method"></a><span data-ttu-id="e983a-103">IHostSemaphore::ReleaseSemaphore 方法</span><span class="sxs-lookup"><span data-stu-id="e983a-103">IHostSemaphore::ReleaseSemaphore Method</span></span>

<span data-ttu-id="e983a-104">按指定量增加当前 [IHostSemaphore](ihostsemaphore-interface.md) 实例的计数。</span><span class="sxs-lookup"><span data-stu-id="e983a-104">Increases the count of the current [IHostSemaphore](ihostsemaphore-interface.md) instance by the specified amount.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e983a-105">语法</span><span class="sxs-lookup"><span data-stu-id="e983a-105">Syntax</span></span>  
  
```cpp  
HRESULT ReleaseSemaphore (  
    [in]  LONG  lReleaseCount,  
    [out] LONG  *lpPreviousCount  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e983a-106">参数</span><span class="sxs-lookup"><span data-stu-id="e983a-106">Parameters</span></span>  

 `lReleaseCount`  
 <span data-ttu-id="e983a-107">中当前实例的计数的增加量 `IHostSemaphore` 。</span><span class="sxs-lookup"><span data-stu-id="e983a-107">[in] The amount by which to increase the count of the current `IHostSemaphore` instance.</span></span> <span data-ttu-id="e983a-108">此量必须大于零。</span><span class="sxs-lookup"><span data-stu-id="e983a-108">This amount must be greater than zero.</span></span>  
  
 `lpPreviousCount`  
 <span data-ttu-id="e983a-109">弄指向上一个计数的指针; 如果调用方不需要以前的计数，则为 null。</span><span class="sxs-lookup"><span data-stu-id="e983a-109">[out] A pointer to the previous count, or null if the caller does not require the previous count.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e983a-110">返回值</span><span class="sxs-lookup"><span data-stu-id="e983a-110">Return Value</span></span>  
  
|<span data-ttu-id="e983a-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e983a-111">HRESULT</span></span>|<span data-ttu-id="e983a-112">说明</span><span class="sxs-lookup"><span data-stu-id="e983a-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="e983a-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="e983a-113">S_OK</span></span>|<span data-ttu-id="e983a-114">`ReleaseSemaphore` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="e983a-114">`ReleaseSemaphore` returned successfully.</span></span>|  
|<span data-ttu-id="e983a-115">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="e983a-115">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="e983a-116"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="e983a-116">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="e983a-117">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="e983a-117">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="e983a-118">调用超时。</span><span class="sxs-lookup"><span data-stu-id="e983a-118">The call timed out.</span></span>|  
|<span data-ttu-id="e983a-119">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="e983a-119">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="e983a-120">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="e983a-120">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="e983a-121">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="e983a-121">HOST_E_ABANDONED</span></span>|<span data-ttu-id="e983a-122">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="e983a-122">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="e983a-123">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e983a-123">E_FAIL</span></span>|<span data-ttu-id="e983a-124">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="e983a-124">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="e983a-125">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="e983a-125">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="e983a-126">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="e983a-126">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e983a-127">备注</span><span class="sxs-lookup"><span data-stu-id="e983a-127">Remarks</span></span>  

 <span data-ttu-id="e983a-128">CLR 通常会调用 `ReleaseSemaphore` 以通知宿主它已使用完资源，并为参数传递值 1 `lReleaseCount` 。</span><span class="sxs-lookup"><span data-stu-id="e983a-128">The CLR typically calls `ReleaseSemaphore` to notify the host that it has finished using a resource, passing a value of 1 for the `lReleaseCount` parameter.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e983a-129">要求</span><span class="sxs-lookup"><span data-stu-id="e983a-129">Requirements</span></span>  

 <span data-ttu-id="e983a-130">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e983a-130">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e983a-131">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="e983a-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e983a-132">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e983a-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e983a-133">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e983a-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e983a-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="e983a-134">See also</span></span>

- [<span data-ttu-id="e983a-135">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="e983a-135">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="e983a-136">IHostAutoEvent 接口</span><span class="sxs-lookup"><span data-stu-id="e983a-136">IHostAutoEvent Interface</span></span>](ihostautoevent-interface.md)
- [<span data-ttu-id="e983a-137">IHostManualEvent 接口</span><span class="sxs-lookup"><span data-stu-id="e983a-137">IHostManualEvent Interface</span></span>](ihostmanualevent-interface.md)
- [<span data-ttu-id="e983a-138">IHostSemaphore 接口</span><span class="sxs-lookup"><span data-stu-id="e983a-138">IHostSemaphore Interface</span></span>](ihostsemaphore-interface.md)
- [<span data-ttu-id="e983a-139">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="e983a-139">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
