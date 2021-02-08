---
description: 了解详细信息： IHostSyncManager：： CreateCrstWithSpinCount 方法
title: IHostSyncManager::CreateCrstWithSpinCount 方法
ms.date: 03/30/2017
api_name:
- IHostSyncManager.CreateCrstWithSpinCount
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSyncManager::CreateCrstWithSpinCount
helpviewer_keywords:
- CreateCrstWithSpinCount method [.NET Framework hosting]
- IHostSyncManager::CreateCrstWithSpinCount method [.NET Framework hosting]
ms.assetid: 7280fa8c-3639-4abf-91cb-bc343da742d1
topic_type:
- apiref
ms.openlocfilehash: 3c43f1a3d52eb7174844ecb4079cf54413f20853
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784816"
---
# <a name="ihostsyncmanagercreatecrstwithspincount-method"></a><span data-ttu-id="95698-103">IHostSyncManager::CreateCrstWithSpinCount 方法</span><span class="sxs-lookup"><span data-stu-id="95698-103">IHostSyncManager::CreateCrstWithSpinCount Method</span></span>

<span data-ttu-id="95698-104">使用自旋计数为同步创建一个临界区对象。</span><span class="sxs-lookup"><span data-stu-id="95698-104">Creates a critical section object with spin count for synchronization.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="95698-105">语法</span><span class="sxs-lookup"><span data-stu-id="95698-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateCrstWithSpinCount (  
    [in]  DWORD dwSpinCount,  
    [out] IHostCrst** ppCrst  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="95698-106">参数</span><span class="sxs-lookup"><span data-stu-id="95698-106">Parameters</span></span>  

 `dwSpinCount`  
 <span data-ttu-id="95698-107">中为临界区对象指定自旋计数。</span><span class="sxs-lookup"><span data-stu-id="95698-107">[in] Specifies the spin count for the critical section object.</span></span>  
  
 `ppCrst`  
 <span data-ttu-id="95698-108">弄指向 [IHostCrst](ihostcrst-interface.md) 实例的地址的指针; 如果无法创建关键节，则为 null。</span><span class="sxs-lookup"><span data-stu-id="95698-108">[out] A pointer to the address of an [IHostCrst](ihostcrst-interface.md) instance, or null if the critical section could not be created.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="95698-109">返回值</span><span class="sxs-lookup"><span data-stu-id="95698-109">Return Value</span></span>  
  
|<span data-ttu-id="95698-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="95698-110">HRESULT</span></span>|<span data-ttu-id="95698-111">说明</span><span class="sxs-lookup"><span data-stu-id="95698-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="95698-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="95698-112">S_OK</span></span>|<span data-ttu-id="95698-113">`CreateCrstWithSpinCount` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="95698-113">`CreateCrstWithSpinCount` returned successfully.</span></span>|  
|<span data-ttu-id="95698-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="95698-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="95698-115"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="95698-115">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="95698-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="95698-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="95698-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="95698-117">The call timed out.</span></span>|  
|<span data-ttu-id="95698-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="95698-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="95698-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="95698-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="95698-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="95698-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="95698-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="95698-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="95698-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="95698-122">E_FAIL</span></span>|<span data-ttu-id="95698-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="95698-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="95698-124">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="95698-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="95698-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="95698-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="95698-126">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="95698-126">E_OUTOFMEMORY</span></span>|<span data-ttu-id="95698-127">没有足够的内存可用于创建请求的关键部分。</span><span class="sxs-lookup"><span data-stu-id="95698-127">Not enough memory was available to create the requested critical section.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="95698-128">备注</span><span class="sxs-lookup"><span data-stu-id="95698-128">Remarks</span></span>  

 <span data-ttu-id="95698-129">自旋计数仅在多处理器系统上使用。</span><span class="sxs-lookup"><span data-stu-id="95698-129">A spin count is used only on a multi-processor system.</span></span> <span data-ttu-id="95698-130">自旋计数指定调用线程在与不可用关键部分关联的信号量上执行等待操作之前必须旋转的次数。</span><span class="sxs-lookup"><span data-stu-id="95698-130">The spin count specifies the number of times a calling thread must spin before it performs a wait operation on a semaphore that is associated with an unavailable critical section.</span></span> <span data-ttu-id="95698-131">如果在自旋操作期间关键部分变为免费，则调用线程将避免等待操作。</span><span class="sxs-lookup"><span data-stu-id="95698-131">If the critical section becomes free during the spin operation, the calling thread avoids the wait operation.</span></span> <span data-ttu-id="95698-132">`CreateCrstWithSpinCount` 对 Win32 函数进行镜像 `InitializeCriticalSectionAndSpinCount` 。</span><span class="sxs-lookup"><span data-stu-id="95698-132">`CreateCrstWithSpinCount` mirrors the Win32 `InitializeCriticalSectionAndSpinCount` function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="95698-133">要求</span><span class="sxs-lookup"><span data-stu-id="95698-133">Requirements</span></span>  

 <span data-ttu-id="95698-134">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="95698-134">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="95698-135">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="95698-135">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="95698-136">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="95698-136">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="95698-137">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="95698-137">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="95698-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="95698-138">See also</span></span>

- [<span data-ttu-id="95698-139">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="95698-139">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="95698-140">IHostSemaphore 接口</span><span class="sxs-lookup"><span data-stu-id="95698-140">IHostSemaphore Interface</span></span>](ihostsemaphore-interface.md)
- [<span data-ttu-id="95698-141">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="95698-141">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
