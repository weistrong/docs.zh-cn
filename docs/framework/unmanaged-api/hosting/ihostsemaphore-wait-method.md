---
description: 了解详细信息： IHostSemaphore：： Wait 方法
title: IHostSemaphore::Wait 方法
ms.date: 03/30/2017
api_name:
- IHostSemaphore.Wait
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSemaphore::Wait
helpviewer_keywords:
- IHostSemaphore::Wait method [.NET Framework hosting]
- Wait method, IHostSemaphore interface [.NET Framework hosting]
ms.assetid: 0da962a3-ce55-44dd-ab7a-14ad7105af4a
topic_type:
- apiref
ms.openlocfilehash: 386f9806d6457f30d13e18e7d0d1ab16aafb84ee
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99728424"
---
# <a name="ihostsemaphorewait-method"></a><span data-ttu-id="353c8-103">IHostSemaphore::Wait 方法</span><span class="sxs-lookup"><span data-stu-id="353c8-103">IHostSemaphore::Wait Method</span></span>

<span data-ttu-id="353c8-104">导致当前 [IHostSemaphore](ihostsemaphore-interface.md) 实例等待，直到其拥有或经过指定的时间量。</span><span class="sxs-lookup"><span data-stu-id="353c8-104">Causes the current [IHostSemaphore](ihostsemaphore-interface.md) instance to wait until it is owned or the specified amount of time elapses.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="353c8-105">语法</span><span class="sxs-lookup"><span data-stu-id="353c8-105">Syntax</span></span>  
  
```cpp  
HRESULT Wait (  
    [in] DWORD dwMilliseconds,  
    [in] DWORD option  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="353c8-106">参数</span><span class="sxs-lookup"><span data-stu-id="353c8-106">Parameters</span></span>  

 `dwMilliseconds`  
 <span data-ttu-id="353c8-107">中如果当前实例不属于，则返回前等待的毫秒数 `IHostSemaphore` 。</span><span class="sxs-lookup"><span data-stu-id="353c8-107">[in] The number of milliseconds to wait before returning, if the current `IHostSemaphore` instance is not owned.</span></span>  
  
 `option`  
 <span data-ttu-id="353c8-108">中 [WAIT_OPTION](wait-option-enumeration.md) 值之一，指定主机在此操作阻止的情况下应执行的操作。</span><span class="sxs-lookup"><span data-stu-id="353c8-108">[in] One of the [WAIT_OPTION](wait-option-enumeration.md) values, specifying what action the host should take if this operation blocks.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="353c8-109">返回值</span><span class="sxs-lookup"><span data-stu-id="353c8-109">Return Value</span></span>  
  
|<span data-ttu-id="353c8-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="353c8-110">HRESULT</span></span>|<span data-ttu-id="353c8-111">说明</span><span class="sxs-lookup"><span data-stu-id="353c8-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="353c8-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="353c8-112">S_OK</span></span>|<span data-ttu-id="353c8-113">`Wait` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="353c8-113">`Wait` returned successfully.</span></span>|  
|<span data-ttu-id="353c8-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="353c8-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="353c8-115"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="353c8-115">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="353c8-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="353c8-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="353c8-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="353c8-117">The call timed out.</span></span>|  
|<span data-ttu-id="353c8-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="353c8-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="353c8-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="353c8-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="353c8-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="353c8-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="353c8-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="353c8-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="353c8-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="353c8-122">E_FAIL</span></span>|<span data-ttu-id="353c8-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="353c8-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="353c8-124">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="353c8-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="353c8-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="353c8-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="353c8-126">HOST_E_DEADLOCK</span><span class="sxs-lookup"><span data-stu-id="353c8-126">HOST_E_DEADLOCK</span></span>|<span data-ttu-id="353c8-127">主机在等待间隔期间检测到死锁，并将当前 `IHostSemaphore` 实例选择为死锁牺牲品。</span><span class="sxs-lookup"><span data-stu-id="353c8-127">The host detected a deadlock during the wait interval, and chose the current `IHostSemaphore` instance as a deadlock victim.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="353c8-128">要求</span><span class="sxs-lookup"><span data-stu-id="353c8-128">Requirements</span></span>  

 <span data-ttu-id="353c8-129">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="353c8-129">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="353c8-130">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="353c8-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="353c8-131">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="353c8-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="353c8-132">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="353c8-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="353c8-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="353c8-133">See also</span></span>

- [<span data-ttu-id="353c8-134">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="353c8-134">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="353c8-135">IHostAutoEvent 接口</span><span class="sxs-lookup"><span data-stu-id="353c8-135">IHostAutoEvent Interface</span></span>](ihostautoevent-interface.md)
- [<span data-ttu-id="353c8-136">IHostManualEvent 接口</span><span class="sxs-lookup"><span data-stu-id="353c8-136">IHostManualEvent Interface</span></span>](ihostmanualevent-interface.md)
- [<span data-ttu-id="353c8-137">IHostSemaphore 接口</span><span class="sxs-lookup"><span data-stu-id="353c8-137">IHostSemaphore Interface</span></span>](ihostsemaphore-interface.md)
- [<span data-ttu-id="353c8-138">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="353c8-138">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
