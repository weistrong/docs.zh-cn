---
description: 了解详细信息： IHostManualEvent：： Wait 方法
title: IHostManualEvent::Wait 方法
ms.date: 03/30/2017
api_name:
- IHostManualEvent.Wait
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostManualEvent::Wait
helpviewer_keywords:
- IHostManualEvent::Wait method [.NET Framework hosting]
- Wait method, IHostManualEvent interface [.NET Framework hosting]
ms.assetid: 1fbb7d8b-8a23-4c2b-8376-1a70cd2d6030
topic_type:
- apiref
ms.openlocfilehash: f9e681e5075f1de34dc45ed2b2485a0e1269cb11
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707861"
---
# <a name="ihostmanualeventwait-method"></a><span data-ttu-id="f0772-103">IHostManualEvent::Wait 方法</span><span class="sxs-lookup"><span data-stu-id="f0772-103">IHostManualEvent::Wait Method</span></span>

<span data-ttu-id="f0772-104">导致当前 [IHostManualEvent](ihostmanualevent-interface.md) 实例等待，直到其拥有或经过指定的时间量。</span><span class="sxs-lookup"><span data-stu-id="f0772-104">Causes the current [IHostManualEvent](ihostmanualevent-interface.md) instance to wait until it is owned, or a specified amount of time elapses.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f0772-105">语法</span><span class="sxs-lookup"><span data-stu-id="f0772-105">Syntax</span></span>  
  
```cpp  
HRESULT Wait (  
    [in] DWORD dwMilliseconds,  
    [in] DWORD option  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f0772-106">参数</span><span class="sxs-lookup"><span data-stu-id="f0772-106">Parameters</span></span>  

 `dwMilliseconds`  
 <span data-ttu-id="f0772-107">中如果当前实例不属于，则返回前等待的毫秒数 `IHostManualEvent` 。</span><span class="sxs-lookup"><span data-stu-id="f0772-107">[in] The number of milliseconds to wait before returning, if the current `IHostManualEvent` instance is not owned.</span></span>  
  
 `option`  
 <span data-ttu-id="f0772-108">中 [WAIT_OPTION](wait-option-enumeration.md) 值之一，指示当此操作阻止时宿主应执行的操作。</span><span class="sxs-lookup"><span data-stu-id="f0772-108">[in] One of the [WAIT_OPTION](wait-option-enumeration.md) values, indicating the action the host should take if this operation blocks.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f0772-109">返回值</span><span class="sxs-lookup"><span data-stu-id="f0772-109">Return Value</span></span>  
  
|<span data-ttu-id="f0772-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f0772-110">HRESULT</span></span>|<span data-ttu-id="f0772-111">说明</span><span class="sxs-lookup"><span data-stu-id="f0772-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f0772-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="f0772-112">S_OK</span></span>|<span data-ttu-id="f0772-113">`Wait` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="f0772-113">`Wait` returned successfully.</span></span>|  
|<span data-ttu-id="f0772-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="f0772-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="f0772-115"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="f0772-115">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="f0772-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f0772-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="f0772-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="f0772-117">The call timed out.</span></span>|  
|<span data-ttu-id="f0772-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="f0772-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="f0772-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="f0772-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="f0772-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="f0772-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="f0772-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="f0772-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="f0772-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f0772-122">E_FAIL</span></span>|<span data-ttu-id="f0772-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="f0772-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="f0772-124">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="f0772-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="f0772-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="f0772-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="f0772-126">HOST_E_DEADLOCK</span><span class="sxs-lookup"><span data-stu-id="f0772-126">HOST_E_DEADLOCK</span></span>|<span data-ttu-id="f0772-127">主机在等待间隔期间检测到死锁，并选择当前 `IHostManualEvent` 实例作为死锁牺牲品。</span><span class="sxs-lookup"><span data-stu-id="f0772-127">The host detected a deadlock during the wait interval, and chose the current `IHostManualEvent` instance as the deadlock victim.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f0772-128">要求</span><span class="sxs-lookup"><span data-stu-id="f0772-128">Requirements</span></span>  

 <span data-ttu-id="f0772-129">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f0772-129">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f0772-130">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="f0772-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f0772-131">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f0772-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f0772-132">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f0772-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f0772-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="f0772-133">See also</span></span>

- [<span data-ttu-id="f0772-134">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="f0772-134">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="f0772-135">IHostAutoEvent 接口</span><span class="sxs-lookup"><span data-stu-id="f0772-135">IHostAutoEvent Interface</span></span>](ihostautoevent-interface.md)
- [<span data-ttu-id="f0772-136">IHostManualEvent 接口</span><span class="sxs-lookup"><span data-stu-id="f0772-136">IHostManualEvent Interface</span></span>](ihostmanualevent-interface.md)
- [<span data-ttu-id="f0772-137">IHostSemaphore 接口</span><span class="sxs-lookup"><span data-stu-id="f0772-137">IHostSemaphore Interface</span></span>](ihostsemaphore-interface.md)
- [<span data-ttu-id="f0772-138">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="f0772-138">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
