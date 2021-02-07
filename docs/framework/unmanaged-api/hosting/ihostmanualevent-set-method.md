---
description: 了解详细信息： IHostManualEvent：： Set 方法
title: IHostManualEvent::Set 方法
ms.date: 03/30/2017
api_name:
- IHostManualEvent.Set
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostManualEvent::Set
helpviewer_keywords:
- Set method, IHostManualEvent interface [.NET Framework hosting]
- IHostManualEvent::Set method [.NET Framework hosting]
ms.assetid: e930c174-f71d-4faa-bb59-f0fb3df4d77b
topic_type:
- apiref
ms.openlocfilehash: e2de1fde2f8c0f512733ecde43d5240a94f84264
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707925"
---
# <a name="ihostmanualeventset-method"></a><span data-ttu-id="ca8fd-103">IHostManualEvent::Set 方法</span><span class="sxs-lookup"><span data-stu-id="ca8fd-103">IHostManualEvent::Set Method</span></span>

<span data-ttu-id="ca8fd-104">将当前的 [IHostManualEvent](ihostmanualevent-interface.md) 实例设置为终止状态。</span><span class="sxs-lookup"><span data-stu-id="ca8fd-104">Sets the current [IHostManualEvent](ihostmanualevent-interface.md) instance to a signaled state.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ca8fd-105">语法</span><span class="sxs-lookup"><span data-stu-id="ca8fd-105">Syntax</span></span>  
  
```cpp  
HRESULT Set ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="ca8fd-106">返回值</span><span class="sxs-lookup"><span data-stu-id="ca8fd-106">Return Value</span></span>  
  
|<span data-ttu-id="ca8fd-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ca8fd-107">HRESULT</span></span>|<span data-ttu-id="ca8fd-108">说明</span><span class="sxs-lookup"><span data-stu-id="ca8fd-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ca8fd-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca8fd-109">S_OK</span></span>|<span data-ttu-id="ca8fd-110">`Set` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="ca8fd-110">`Set` returned successfully.</span></span>|  
|<span data-ttu-id="ca8fd-111">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ca8fd-111">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="ca8fd-112"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="ca8fd-112">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="ca8fd-113">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ca8fd-113">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="ca8fd-114">调用超时。</span><span class="sxs-lookup"><span data-stu-id="ca8fd-114">The call timed out.</span></span>|  
|<span data-ttu-id="ca8fd-115">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="ca8fd-115">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="ca8fd-116">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="ca8fd-116">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="ca8fd-117">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="ca8fd-117">HOST_E_ABANDONED</span></span>|<span data-ttu-id="ca8fd-118">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="ca8fd-118">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="ca8fd-119">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ca8fd-119">E_FAIL</span></span>|<span data-ttu-id="ca8fd-120">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="ca8fd-120">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="ca8fd-121">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="ca8fd-121">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="ca8fd-122">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="ca8fd-122">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ca8fd-123">要求</span><span class="sxs-lookup"><span data-stu-id="ca8fd-123">Requirements</span></span>  

 <span data-ttu-id="ca8fd-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ca8fd-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ca8fd-125">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="ca8fd-125">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ca8fd-126">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ca8fd-126">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ca8fd-127">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ca8fd-127">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ca8fd-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="ca8fd-128">See also</span></span>

- [<span data-ttu-id="ca8fd-129">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="ca8fd-129">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="ca8fd-130">IHostAutoEvent 接口</span><span class="sxs-lookup"><span data-stu-id="ca8fd-130">IHostAutoEvent Interface</span></span>](ihostautoevent-interface.md)
- [<span data-ttu-id="ca8fd-131">IHostManualEvent 接口</span><span class="sxs-lookup"><span data-stu-id="ca8fd-131">IHostManualEvent Interface</span></span>](ihostmanualevent-interface.md)
- [<span data-ttu-id="ca8fd-132">IHostSemaphore 接口</span><span class="sxs-lookup"><span data-stu-id="ca8fd-132">IHostSemaphore Interface</span></span>](ihostsemaphore-interface.md)
- [<span data-ttu-id="ca8fd-133">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="ca8fd-133">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
