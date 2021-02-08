---
description: 了解详细信息： IHostSyncManager：： CreateCrst 方法
title: IHostSyncManager::CreateCrst 方法
ms.date: 03/30/2017
api_name:
- IHostSyncManager.CreateCrst
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSyncManager::CreateCrst
helpviewer_keywords:
- CreateCrst method [.NET Framework hosting]
- IHostSyncManager::CreateCrst method [.NET Framework hosting]
ms.assetid: ac278cc8-2540-4a6c-b5c6-b90c3970b4f4
topic_type:
- apiref
ms.openlocfilehash: 7d1880f1553d159f62efe65afe8368a60b5bf9cc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784803"
---
# <a name="ihostsyncmanagercreatecrst-method"></a><span data-ttu-id="7b35b-103">IHostSyncManager::CreateCrst 方法</span><span class="sxs-lookup"><span data-stu-id="7b35b-103">IHostSyncManager::CreateCrst Method</span></span>

<span data-ttu-id="7b35b-104">创建用于同步的临界区对象。</span><span class="sxs-lookup"><span data-stu-id="7b35b-104">Creates a critical section object for synchronization.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7b35b-105">语法</span><span class="sxs-lookup"><span data-stu-id="7b35b-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateCrst (  
    [out] IHostCrst** ppCrst  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7b35b-106">参数</span><span class="sxs-lookup"><span data-stu-id="7b35b-106">Parameters</span></span>  

 `ppCrst`  
 <span data-ttu-id="7b35b-107">弄指向主机实现的 [IHostCrst](ihostcrst-interface.md) 实例的地址的指针; 如果无法创建关键节，则为 null。</span><span class="sxs-lookup"><span data-stu-id="7b35b-107">[out] A pointer to the address of an [IHostCrst](ihostcrst-interface.md) instance implemented by the host, or null if the critical section could not be created.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7b35b-108">返回值</span><span class="sxs-lookup"><span data-stu-id="7b35b-108">Return Value</span></span>  
  
|<span data-ttu-id="7b35b-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="7b35b-109">HRESULT</span></span>|<span data-ttu-id="7b35b-110">说明</span><span class="sxs-lookup"><span data-stu-id="7b35b-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="7b35b-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="7b35b-111">S_OK</span></span>|<span data-ttu-id="7b35b-112">`CreateCrst` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="7b35b-112">`CreateCrst` returned successfully.</span></span>|  
|<span data-ttu-id="7b35b-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="7b35b-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="7b35b-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="7b35b-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="7b35b-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="7b35b-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="7b35b-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="7b35b-116">The call timed out.</span></span>|  
|<span data-ttu-id="7b35b-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="7b35b-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="7b35b-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="7b35b-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="7b35b-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="7b35b-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="7b35b-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="7b35b-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="7b35b-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="7b35b-121">E_FAIL</span></span>|<span data-ttu-id="7b35b-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="7b35b-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="7b35b-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="7b35b-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="7b35b-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="7b35b-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="7b35b-125">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="7b35b-125">E_OUTOFMEMORY</span></span>|<span data-ttu-id="7b35b-126">没有足够的内存可用于创建请求的关键部分。</span><span class="sxs-lookup"><span data-stu-id="7b35b-126">Not enough memory was available to create the requested critical section.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7b35b-127">备注</span><span class="sxs-lookup"><span data-stu-id="7b35b-127">Remarks</span></span>  

 <span data-ttu-id="7b35b-128">临界区对象提供与 mutex 对象提供的同步，只不过临界区只能由单个进程的线程使用。</span><span class="sxs-lookup"><span data-stu-id="7b35b-128">Critical section objects provide synchronization similar to that provided by a mutex object, except that critical sections can be used only by the threads of a single process.</span></span> <span data-ttu-id="7b35b-129">`CreateCrst` 对 Win32 函数进行镜像 `InitializeCriticalSection` 。</span><span class="sxs-lookup"><span data-stu-id="7b35b-129">`CreateCrst` mirrors the Win32 `InitializeCriticalSection` function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7b35b-130">要求</span><span class="sxs-lookup"><span data-stu-id="7b35b-130">Requirements</span></span>  

 <span data-ttu-id="7b35b-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7b35b-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7b35b-132">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="7b35b-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="7b35b-133">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7b35b-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="7b35b-134">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7b35b-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7b35b-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="7b35b-135">See also</span></span>

- [<span data-ttu-id="7b35b-136">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="7b35b-136">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="7b35b-137">IHostCrst 接口</span><span class="sxs-lookup"><span data-stu-id="7b35b-137">IHostCrst Interface</span></span>](ihostcrst-interface.md)
- [<span data-ttu-id="7b35b-138">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="7b35b-138">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
- [<span data-ttu-id="7b35b-139">IHostSemaphore 接口</span><span class="sxs-lookup"><span data-stu-id="7b35b-139">IHostSemaphore Interface</span></span>](ihostsemaphore-interface.md)
- [<span data-ttu-id="7b35b-140">Mutex</span><span class="sxs-lookup"><span data-stu-id="7b35b-140">Mutexes</span></span>](../../../standard/threading/mutexes.md)
- [<span data-ttu-id="7b35b-141">Semaphore 和 SemaphoreSlim</span><span class="sxs-lookup"><span data-stu-id="7b35b-141">Semaphore and SemaphoreSlim</span></span>](../../../standard/threading/semaphore-and-semaphoreslim.md)
