---
description: 了解详细信息： IHostManualEvent：： Reset 方法
title: IHostManualEvent::Reset 方法
ms.date: 03/30/2017
api_name:
- IHostManualEvent.Reset
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostManualEvent::Reset
helpviewer_keywords:
- Reset method, IHostManualEvent interface [.NET Framework hosting]
- IHostManualEvent::Reset method [.NET Framework hosting]
ms.assetid: 0d101168-b5e3-49ce-90c7-85cf2db83c4c
topic_type:
- apiref
ms.openlocfilehash: 84debb8b37c2cdfdbf294bff6736b081424f9e52
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99708068"
---
# <a name="ihostmanualeventreset-method"></a><span data-ttu-id="b2349-103">IHostManualEvent::Reset 方法</span><span class="sxs-lookup"><span data-stu-id="b2349-103">IHostManualEvent::Reset Method</span></span>

<span data-ttu-id="b2349-104">将当前 [IHostManualEvent](ihostmanualevent-interface.md) 实例重置为非终止状态。</span><span class="sxs-lookup"><span data-stu-id="b2349-104">Resets the current [IHostManualEvent](ihostmanualevent-interface.md) instance to a non-signaled state.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b2349-105">语法</span><span class="sxs-lookup"><span data-stu-id="b2349-105">Syntax</span></span>  
  
```cpp  
HRESULT Reset ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="b2349-106">返回值</span><span class="sxs-lookup"><span data-stu-id="b2349-106">Return Value</span></span>  
  
|<span data-ttu-id="b2349-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="b2349-107">HRESULT</span></span>|<span data-ttu-id="b2349-108">说明</span><span class="sxs-lookup"><span data-stu-id="b2349-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="b2349-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="b2349-109">S_OK</span></span>|<span data-ttu-id="b2349-110">`Reset` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="b2349-110">`Reset` returned successfully.</span></span>|  
|<span data-ttu-id="b2349-111">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="b2349-111">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="b2349-112"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="b2349-112">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="b2349-113">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b2349-113">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="b2349-114">调用超时。</span><span class="sxs-lookup"><span data-stu-id="b2349-114">The call timed out.</span></span>|  
|<span data-ttu-id="b2349-115">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="b2349-115">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="b2349-116">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="b2349-116">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="b2349-117">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="b2349-117">HOST_E_ABANDONED</span></span>|<span data-ttu-id="b2349-118">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="b2349-118">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="b2349-119">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="b2349-119">E_FAIL</span></span>|<span data-ttu-id="b2349-120">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="b2349-120">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="b2349-121">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="b2349-121">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="b2349-122">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="b2349-122">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b2349-123">要求</span><span class="sxs-lookup"><span data-stu-id="b2349-123">Requirements</span></span>  

 <span data-ttu-id="b2349-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b2349-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b2349-125">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="b2349-125">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b2349-126">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b2349-126">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b2349-127">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b2349-127">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b2349-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="b2349-128">See also</span></span>

- [<span data-ttu-id="b2349-129">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="b2349-129">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="b2349-130">IHostAutoEvent 接口</span><span class="sxs-lookup"><span data-stu-id="b2349-130">IHostAutoEvent Interface</span></span>](ihostautoevent-interface.md)
- [<span data-ttu-id="b2349-131">IHostManualEvent 接口</span><span class="sxs-lookup"><span data-stu-id="b2349-131">IHostManualEvent Interface</span></span>](ihostmanualevent-interface.md)
- [<span data-ttu-id="b2349-132">IHostSemaphore 接口</span><span class="sxs-lookup"><span data-stu-id="b2349-132">IHostSemaphore Interface</span></span>](ihostsemaphore-interface.md)
- [<span data-ttu-id="b2349-133">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="b2349-133">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
