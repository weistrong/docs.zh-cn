---
description: 了解详细信息： IHostAutoEvent：： Wait 方法
title: IHostAutoEvent::Wait 方法
ms.date: 03/30/2017
api_name:
- IHostAutoEvent.Wait
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostAutoEvent::Wait
helpviewer_keywords:
- Wait method, IHostAutoEvent interface [.NET Framework hosting]
- IHostAutoEvent::Wait method [.NET Framework hosting]
ms.assetid: 535d51c5-9112-401b-8c36-85f35d7ee609
topic_type:
- apiref
ms.openlocfilehash: 0b75b44075dda46a3d84850cebd6b8f3851b055c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789471"
---
# <a name="ihostautoeventwait-method"></a><span data-ttu-id="050ec-103">IHostAutoEvent::Wait 方法</span><span class="sxs-lookup"><span data-stu-id="050ec-103">IHostAutoEvent::Wait Method</span></span>

<span data-ttu-id="050ec-104">导致当前 [IHostAutoEvent](ihostautoevent-interface.md) 实例等待，直到其拥有或经过指定的时间量。</span><span class="sxs-lookup"><span data-stu-id="050ec-104">Causes the current [IHostAutoEvent](ihostautoevent-interface.md) instance to wait until it is owned or a specified amount of time elapses.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="050ec-105">语法</span><span class="sxs-lookup"><span data-stu-id="050ec-105">Syntax</span></span>  
  
```cpp  
HRESULT Wait (  
    [in] DWORD dwMilliseconds,  
    [in] DWORD option  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="050ec-106">参数</span><span class="sxs-lookup"><span data-stu-id="050ec-106">Parameters</span></span>  

 `dwMilliseconds`  
 <span data-ttu-id="050ec-107">中 `IHostAutoEvent` 如果没有线程或纤程取得所有权，则当前实例在返回之前应等待的毫秒数。</span><span class="sxs-lookup"><span data-stu-id="050ec-107">[in] The number of milliseconds the current `IHostAutoEvent` instance should wait before returning, if no thread or fiber takes ownership.</span></span>  
  
 `option`  
 <span data-ttu-id="050ec-108">中 [WAIT_OPTION](wait-option-enumeration.md) 值之一，指定宿主在此操作阻止的情况下应执行的操作。</span><span class="sxs-lookup"><span data-stu-id="050ec-108">[in] One of the [WAIT_OPTION](wait-option-enumeration.md) values, specifying the action the host should take if this operation blocks.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="050ec-109">返回值</span><span class="sxs-lookup"><span data-stu-id="050ec-109">Return Value</span></span>  
  
|<span data-ttu-id="050ec-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="050ec-110">HRESULT</span></span>|<span data-ttu-id="050ec-111">说明</span><span class="sxs-lookup"><span data-stu-id="050ec-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="050ec-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="050ec-112">S_OK</span></span>|<span data-ttu-id="050ec-113">`Wait` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="050ec-113">`Wait` returned successfully.</span></span>|  
|<span data-ttu-id="050ec-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="050ec-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="050ec-115"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="050ec-115">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="050ec-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="050ec-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="050ec-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="050ec-117">The call timed out.</span></span>|  
|<span data-ttu-id="050ec-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="050ec-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="050ec-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="050ec-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="050ec-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="050ec-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="050ec-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="050ec-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="050ec-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="050ec-122">E_FAIL</span></span>|<span data-ttu-id="050ec-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="050ec-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="050ec-124">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="050ec-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="050ec-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="050ec-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="050ec-126">HOST_E_DEADLOCK</span><span class="sxs-lookup"><span data-stu-id="050ec-126">HOST_E_DEADLOCK</span></span>|<span data-ttu-id="050ec-127">主机在等待间隔期间检测到死锁，并选择由当前实例表示的事件 `IHostAutoEvent` 作为死锁牺牲品。</span><span class="sxs-lookup"><span data-stu-id="050ec-127">The host detected a deadlock during the wait interval, and chose the event represented by the current `IHostAutoEvent` instance as the deadlock victim.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="050ec-128">要求</span><span class="sxs-lookup"><span data-stu-id="050ec-128">Requirements</span></span>  

 <span data-ttu-id="050ec-129">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="050ec-129">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="050ec-130">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="050ec-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="050ec-131">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="050ec-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="050ec-132">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="050ec-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="050ec-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="050ec-133">See also</span></span>

- [<span data-ttu-id="050ec-134">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="050ec-134">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="050ec-135">IHostAutoEvent 接口</span><span class="sxs-lookup"><span data-stu-id="050ec-135">IHostAutoEvent Interface</span></span>](ihostautoevent-interface.md)
- [<span data-ttu-id="050ec-136">IHostManualEvent 接口</span><span class="sxs-lookup"><span data-stu-id="050ec-136">IHostManualEvent Interface</span></span>](ihostmanualevent-interface.md)
- [<span data-ttu-id="050ec-137">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="050ec-137">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
